# Homework 1
###New rpc : mergetx [arg1(addressA)] [arg2(colorB)]

	arg1 : string:Gcoin address
	arg2 : int:color
	output : hash

## 效果  
> 創造一type為MERGE的transaction  
> 1. 其input為wallet中所有target address為addressA，且color為colorB的utxo  
> 2. output value為1.中總和  
> 3. output address為addressA, color為colorB  
> 4. 需收取1COIN的color 1當作手續費  
> 5. 將其送進memerypool中  
> 6. 收進block

## 相關檔案

	src/main.
	src/wallet/
	rpcwallet.cpp
	wallet.
	src/miner.
	src/primitives/transaction.h
	src/rpcclient.
	src/rpcserver.

測試方式 : 

	$gcoind -daemon // 背景執行，類似 &

	$gcoin-cli setgenerate true // 全速開始挖礦，只少需有一筆Tx才開始

	$gcoin-cli mint 1 0 // 1 為你想發行貨幣的數量（總共1元）、0 為這個貨幣的color = 0
	
	$gcoin-cli mint 1 0 // 再做一次、原因？(等10個block, 可用gcoin-cli getinfo來看看目前block height)
	
	$gcoin-cli keypoolrefill 1 // 把keypool 的cache填滿。（keypool就是 未使用、預先生成的key）
	
	$gcoin-cli listwalletaddress // 列出wallet中的那一堆addresses
	            (假設吐出address A)

	// 把一筆license Tx, （color 為 1） 送到 address A
	$gcoin-cli sendlicensetoaddress addressA 1 72110100046e616d6503646573046164647201000000000000000000000000046164647200000000000000000000000001046c696e6b0000000000000000000000000000000000000000000000000000000000000000

	// 把一筆license Tx, （color 為 2） 送到 address A
	$gcoin-cli sendlicensetoaddress addressA 2 72110100046e616d6503646573046164647201000000000000000000000000046164647200000000000000000000000001046c696e6b0000000000000000000000000000000000000000000000000000000000000000
	
	$gcoin-cli mint 100 1 //鑄造color 為1, 數量100的錢幣，回傳這筆type為mint的 Tx 的id
	
	$gcoin-cli mint 100 2 //鑄造color 為2, 數量100的錢幣，回傳Tx 的id
	
	$gcoin-cli sendtoaddress addressA 40 2 // 把color為2, 數量40的錢幣送到address A，回傳這筆type為 ??? 的 Tx 的id
	
	$gcoin-cli mergetx addressA 2 // wallet中所有target address為addressA，且color為2的utxo，其總和為output 的value，記得扣掉fee
	            (吐回txhash : hashA)
	
	$gcoin-cli getrawtransaction hashA 1 // 1代表要decode，否則看不懂
	
	
	
	
	
