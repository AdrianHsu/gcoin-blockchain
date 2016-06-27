# 一、與比特幣的關係


## Bitcoin's Blockchain

#### Blockchain
```
由後往前、有序連接的data structure（公開帳簿）。由一個包含元數據的區塊頭、
以及有序連接的一長串交易（Transaction）組成。
```

####Flat file
```
"flat", which means it has no structure for indexing and there
 are usually no structural relationships between the records.
```
#### LevelDB
```
Google提供的database，用於Bitcoin Core客戶端。
```
####Height
```
任一區塊與創世區塊的距離。
```
####SHA256
```
在每個區塊上加密hash生成hash值。hash值中包含父區塊hash區段，
可透過此值一路溯及創世區塊。
```

### 區塊鏈分叉
```
一個區塊暫時出現多個子區塊，只發生於多個不同區塊同時被不同Miners發現時。
```

### 改動父區塊不易，以維護不可改變性
```
若父區塊的hash改變，則子區塊的父區塊hash區段改變，進而一代代皆需修改，耗費計算量。
因此長區塊鏈的越深層、越穩定，維護不可改變性。（區塊鏈可以想成冰川岩芯樣品）
```

### 區塊頭
```
包含三組區塊元數據（BlockMeta）。
1. 父區塊hash值存放組，和前一塊連接。
2. 難度、timestamp、Nonce，與挖礦競爭相關。
3. Merkle 樹的樹根
```
### 區塊鏈共享帳本更新機制
	1. 點對點傳輸的共享ledger
	2. 每個區塊，隨時都有最新同步的總帳備份
	3. 每個區塊都更新對自己有利的信息
	4. 每個節點能選擇receive別的節點發起的信息，request並verify後傳遞
	5. 可選擇不同意、可自己重新發起訊息
	6. 網路的最終目的為，共同同意某一個訊息、並更新到ledger上。
	7. Bitcoin的區塊鏈上以PoW實作
 
## 區塊頭hash值與區塊高度

### 區塊頭hash值
```
區塊頭通過SHA256兩次hash計算得到的digital fingerprint。
只有區塊頭被用於計算。
```

## Merkle Tree
```
屬於hash二叉樹。每個區塊包含產生於該區塊內的所有transactions，
並為整筆transactions生成一個Digital Fingerprint。
若遇上奇數個leaves，則最後一個transaction節點複製一份、以構成偶數。
```



# 二、共識算法


## 拜占庭將軍問題

	distributed node transmission會碰上的共識問題，
	由互不信任的各方構成的網路，但各方又有共同的使命。
	特色：所有國家中的城邦們，都使用著即刻同一版本的「信使即時傳遞的十人圖章表格」 。
	亦即：所有網路上的節點們，都使用著即刻同一版本的總帳。
	城邦 = 節點；信使即時傳遞的十人圖章表格 = 每個節點此刻同意與否的state

## PoW

	1. 工作量證明（Proof of Work），一種共識機制。
	2. 為訊息傳遞的行為加入成本，以降低傳遞速率。
	3. 加入一個random 元素，保證一個time interval內只有一個節點、有權傳遞訊息
### Random 元素的作法
	元素丟進去、讓節點進行隨機hash算完之後，獲得64bit的字符串（hash值）。
	只有前13個字符是0的字串，能被bitcoin blockchain系統接收，成爲PoW。
	
### 新的區塊如何產生？
	1. 某個城邦（節點）發現一行有效的64bit hash值
	2. 把同時所有接收到的訊息、並附上自己的訊息、簽名圖章，向網路各處重新廣播
	3. 其他所有城邦們，接收並驗證這筆hash值
	4. 產生一個新區塊
	5. 更新共享帳本
	6. 把新的帳本作為新的random元素

# 三、區塊鏈與可信任運算

# 四、分佈式帳本