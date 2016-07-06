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
	3. 部分Nodes屬於 Full, 部分Nodes不屬於、則稱為SPV Nodes(不包含 B 的 node)
	4. SPV nodes = Lightweight nodes
## Miner

	1. 若為SPV & Mining Nodes, 則只可以pool mining
	2. 若為Full & Mining Nodes, 則可以一般mining

## Wallet

	1. Full & Wallet Node (e.g. 桌面版bitcoin client)
	2. SPV & Wallet Node (e.g. 手機版)