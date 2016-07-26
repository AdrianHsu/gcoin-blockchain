## PART 1
區塊鏈是種分散式資料庫技術、採用分散式共識(Consensus)演算法，比特幣是以區塊鏈架構的一種應用。其他應用包含食安的食品履歷、Smart Contract。臺大目前開源釋出的GCoin、Linux基金會的Hyperledger和Ripple，都是不同於比特幣的新區塊鏈協議。

## PART 2
每個address代表一個錢包，其中包含很多筆transactions，Tx本身不重要，重要的是Txout，沒用完的會變成UTXO變成下一個Tx的Txin。

## PART 3
區塊鏈用的一個壓縮加密技術是Merkle Tree。利用SHA256加密、把一個Block內部的所有Tx兩兩作hash，若湊不齊偶數則複製，最後再把所有hash合在一起做一次hash，稱為Merkle root，就能用這筆存在block header的hash代表所有筆Tx，類似樹的root有個pointer存在header、用以找到整棵樹。

## PART 4
挖礦制度是bitcoin吸引miner的誘因，因為可以賺錢。Miner是種特殊的client，跟client一樣有錢包，但miner會買高運算GPU的電腦主機，經過申請後成為全世界挖礦競爭者的一員。挖礦就像是全世界同時公佈一題數學難題，因為數字很大、情況很多種所以要算很久，這種規則成為Proof of Work, PoW，只要算出來代表你已經做很多功，你好不容易挖到值得獎勵。這筆獎勵是在block第一次被生成時創造的，成為coinbase Tx，會給挖到礦的第一人當作辛勞的獎勵。

## PART 5
Memory pool與orphan pool。memory pool是在一筆Tx生成後、還沒被塞入某個block前，暫時放的地方。
若a這筆tx的某筆output是b這筆tx的input，也就是a的UTXO，則b就是a的child。一串txs在前進時，若child跑得比較快，會先放進orphan pool，等到這筆child的parent跑到這個node之後，才能取出。

## PART 6
SPV Node、相較於Full Node是種佔記憶體小的Node，只存重要的東西。