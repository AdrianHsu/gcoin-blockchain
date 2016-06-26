# 區塊鏈是什麼？

分散式資料庫系統，分散在世界各地的電腦。
舉例：一份資料、需要七個資料庫系統儲存，則這七個資料庫系統則稱為七個區塊。
七個資料庫系統，分散在世界各地。把七個資料庫系統連結在一起的技術，則稱為區塊鏈。
以比特幣網路舉例：
儲存貨幣交易紀錄，就是使用各個區塊儲存。
## 礦工是什麼？
區塊由誰創造？由全世界各地的礦工所創造。

## 去中心化是什麼？

區塊鏈打破集權。
交易的紀錄（Transaction），儲存在多個區塊；區塊鏈扮演Ledger帳冊的功能。

管理交易資訊、擁有帳冊所有權、擁有交易認證權力。
過去：集中於一個機構上，資料儲存於此。
區塊鏈：不需中心機構，任何人皆不可擁有交易資訊。

## P2P Bitcoin System？
利用分散式資料庫儲存transaction ledger。
e.g. 保險公司、不用經過保險公司進行簽約。

## Distributed Ledger是什麼？
分散式帳冊，分散地儲存在區塊鏈的各個區塊中。
付款者：利用電子錢包，產生一筆transaction
請求付款者：用電子錢包接收transaction
Blockchain = Distributed Ledger，前者是技術面，後者是對Bitcoin的應用面。

## Transaction的組成
交易的資訊共三項：address, label（商品資訊）, amount
請求付款者（店家）生成QR Code->QR Code傳給付款者（客戶）->付款人透過address產生transaction。

## Blockchain Data API

e.g.
Single Address
```
https://blockchain.info/ru/address/$bitcoin_address?format=json
```
獲得這個address、對應的每一筆transaction資訊。

## Bitcoin Transaction是什麼？

一筆Transaction就是BTC所有權轉移的過程。付款者掃QR Code後，通知Bitcoin Network，已核准將0.15 BTC的所有權轉移給店家。

## 所有權鏈 Chain of Ownership
