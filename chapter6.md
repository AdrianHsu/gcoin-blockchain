# Chapter 6

## Bitcoin Node

a collection of 4 functions:

	1. Network routing Node
	2. Blockchain database
	3. Mining 
	4. Wallet services

## Routing

	1. Networking routing node
	2. 有routing function的nodes, 可以validate, propogate Tx 和 Blocks

## Full Blockchain
	
	1. 包含 B 的 node, 稱為Full nodes
	2. 維護 complete & up-to-date 的 copy of 整個Blockchain
	3. 部分Nodes屬於 Full, 部分Notodes不屬於、則稱為SPV Nodes(不包含 B 的 node)
	4. SPV nodes = Lightweight nodes
	5. SPV只下載block header, Full 下載header + 所有blocks的header底下接的transactions
## Miner

	1. 若為SPV & Mining Nodes, 則只可以pool mining
	2. 若為Full & Mining Nodes, 則可以一般mining

## Wallet

	1. Full & Wallet Node (e.g. 桌面版bitcoin client)
	2. SPV & Wallet Node (e.g. 手機版)

## 什麼是 Bitcoin Core?

	1. 又稱Reference Client
	2. 就是包含四功能的Bitcoin Node
	3. Bitcoin Core Client is full blockchain node

## extended bitcoin network

	1. bitcoin P2P protocol
	2. pool mining protocol
	3. Stratum protocol


## Exchanging Inventory

	1. 假設有個node only has genesis block
	2. 從peers收到一筆 inv message 包含hashes of the next 500 blocks
	3. 這個node開始從所有跟它連接著的peers, 執行request blocks
	4. spreading the load
	5. ensure 這個node不會overwhelm其他有requests的peers

## Bloom Filter

	1. 機率搜尋篩選器
	2. express a search pattern while protecting privacy
	3. 功能：SPV nodes用bloom filter來specify a search pattern for Tx
	4. search pattern越精準，則透露越多自己資訊（越危險）
## Bloom filter 流程
	1. 把新的pattern "A", 加進bloom filter
	2. 再把新的pattern "B", 加進bloom filter
	3. 丟pattern "X" 進去，詢問 whether X included
	4. 兩種回答：Maybe Yes, 或 Definitely NOT

## 陌生地的旅客, analogy of "Full & SPV Nodes"
	1. Full node 持有完整城市地圖
	2. SPV node 沒有地圖，用asking random strangers的方式，每個turn問一次往左、往右或直走
	3. SPV node 用 bloom filter，就像是用一種資料不完全顯現的問路方式
	4. 原因：問得太明顯，就會被發現目的地是哪（正確address被peers知道，危險）
	5. 方式：「我要去江 _ 街，你知道這附近哪裡有嗎？」，可能有江南街、江西街...etc
	6. peers回答後，SPV node自己知道哪個回答是他要的（只想知道江南街、其他不管）

## Transaction Pools
	
	1. 幾乎每個node，都維護一個"unconfirmed", "verified" Tx的清單，稱為Tx Pool
	2. e.g. a node holds user's wallet 會利用 Tx pool 來追蹤incoming payments to the user's wallet
	3. 而這些incoming payments 都是已經被Network接收、但仍是unconfirmed
	4. Tx pools的Tx都是verfied的，所以會propagate，只是unconfirmed而已

## Orphan Pools 流程

Orphan Tx 代表這筆Tx的 Txin為未知。
流程就是從Tx pool 中的某筆Txout，檢查是否為這筆Orphan Tx的Txin。

	1. 假設一筆Tx 加入 Tx pool
	2. orphan pools會檢查有沒有任何orphans和這筆Tx的output有關
	3. 若成功matching, 則這些orphans被移出orphan pools, 並移入Tx pools