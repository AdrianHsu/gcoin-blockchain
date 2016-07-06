# Chapter 5 Transactions

## Intro
	1. what Tx contains
	2. how to create Tx
	3. how Tx is verified
	4. how Tx become part of the permanant record of all Tx

## Tx 生命週期

### Tx 生成

### Broadcast Tx 到 Bitcoin 網路

### 傳遞 Tx on Bitcoin 網路

## Tx 的結構

## TX 鎖定時間

## Txout

### Spending conditions (Encumbrances)
	1. 大部分 Wallet Apps 有自己的小database of UTXO, 而這些 UTXO 被locked(encumber)、利用wallets 自己的key.
	2. 收錢者的wallet，會包含a copy of Txout from 給錢者的Tx
	3. Txout assigns a new owner to the coin value, 透過將一個key與owner連結起來。
	4. 這個destination key 就是encumbrance
### TXout的架構


## Txin

### Txin的架構

## Transctions fees

## 如何把Fees加入transaction

## Tx Chainging & Orphan Tx

## Tx Scripts

## Script 建構（Lock & Unlock）

## Scripting 的語言

## Turing 不完備

## Stateless(無State的) Verification

## 標準的Tx

## P2PKH

## P2PK

## 多重簽章

## Data Output(OP_RETURN)

## P2SH