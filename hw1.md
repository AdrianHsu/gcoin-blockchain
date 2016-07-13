# Homework 1
###New rpc : mergetx [arg1(addressA)] [arg2(colorB)]

	arg1 : string:Gcoin address
	arg2 : int:color
	output : hash

## 效果  
> 創造一type為MERGE的transaction  
> 其input為wallet中所有target address為addressA且color為colorB的utxo  
> output value為1.中總和  
> output address為addressA, color為colorB  
> 需收取1COIN的color 1當作手續費  
> 並將其送進memerypool中並收進block

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

	$gcoind -daemon

	$gcoin-cli setgenerate true

	$gcoin-cli mint 1 0
	
	$gcoin-cli mint 1 0 
	            (等10個block, 可用gcoin-cli getinfo來看看目前block height)
	
	$gcoin-cli keypoolrefill 1
	
	$gcoin-cli listwalletaddress
	            (假設吐出address A)

	$gcoin-cli sendlicensetoaddress addressA 1 72110100046e616d6503646573046164647201000000000000000000000000046164647200000000000000000000000001046c696e6b0000000000000000000000000000000000000000000000000000000000000000
	
	$gcoin-cli sendlicensetoaddress addressA 2 72110100046e616d6503646573046164647201000000000000000000000000046164647200000000000000000000000001046c696e6b0000000000000000000000000000000000000000000000000000000000000000
	
	$gcoin-cli mint 100 1
	
	$gcoin-cli mint 100 2
	
	$gcoin-cli sendtoaddress addressA 40 2
	
	$gcoin-cli mergetx addressA 2
	            (吐回txhash : hashA)
	
	$gcoin-cli getrawtransaction hashA 1
	
	
	
	
	
