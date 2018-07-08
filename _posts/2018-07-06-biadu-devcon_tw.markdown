---
layout: post
title:  "2018 百度開發者大會"
date:   2018-07-06 00:59:29 +0800
categories: conference
ref: baidu-devcon
lang: 繁中
comments: true
---
### **前言**
這次來到北京出差, 參訪百度的開發者大會是一大重要工作, 作為一名自駕車工程師, 我會在這裡著重於百度Apollo的發展情況與自己的一些分析  
儘管名為開發者大會, 但沒有太多技術分享, 重點的是各項開放平台的宣傳, 這場大會更像是對潛在合作廠商的信心喊話
百度在這個大會上要傳遞的訊息我總結如此: **你看我百度無人車這麼屌, 這麼多合作案例, 你還不快來加入我們, 讓Apollo成為中國自駕標準**  

### **大會整體感受**
會議精彩度開高走低  
開頭先是各種聲光電音加上震耳欲聾的Dubstep, 接著CEO李彥宏開場, 長相帥氣的百度頭頭說話不急不徐, 在宣告各項突破的時候,語氣仍然知性, 沒有不自然的亢奮,舞台魅力十足
與金龍客運老總現場連線, 即時轉播第100台L4無人駕駛車在廈門工廠順利生產, 讓我震撼不已  
但後來各部門大老的分別報告, 就沒有這麼精彩了, 內容開始不斷重複, 講者一個比一個木訥, 甚至有講者用死背朗誦的方式報告, 比百度的語音機器人更加機械  
另外一方面, 兩天下來活動籌劃的相當混亂, 與會者的動線安排和講者上台的時間全都跑了套, 讓人失望  
儘管如此, 仍有不錯的收穫, 以下開始進入正題

### **四大開放大平台**
會議重點圍繞這下面這四個開放給所有開發者的平台
[image]

#### DuerOS
就是一個語音交互系統, 百度希望眾多的開發者協助他們開發各種客能, 並說服客戶裝上DuerOS  
我個人並不理解這其中有什麼巨大商機, 在車上裝個DuerOS或許可以為無法動手的司機提供便利的功能, 但是一隻手機完全可以作到這些功能, 更不用說放在家中的智慧音箱了
另外語音交互只是一種操作介面罷了, 可以將他作為鍵盤或是滑鼠的替代, 系統能不能藉由你的對話產生極度智慧的動作, 是另一碼子事  
#### 百度大腦
一個具有200種功能的大雜燴平台, 你能想到的它都有:  
[image]
這種平台能夠處理被一些被良好定義的經典Machine Learning問題,  讓沒有ML相關知識的開發者解決簡單的問題, 簡單的問題並非沒有價值  
李彥宏當時在台上邀請了一位來自西藏的醫師, 這位醫師利用百度的平台訓練了一個辨識水中寄生蟲的模型, 高辨識精度的模型能夠取代寄生蟲專家的識別, 這在西藏這樣地廣人稀的地方極其珍貴  
這讓我相當感動, 這位醫生用科技改善生活的努力, 是實實在在讓世界更好的努力, 而不是那種塞兩個鏡頭到手機上那種讓物質更加奢侈的努力
#### 百度小程序
簡單來說就是百度搞一個APP大平台, 所有功能都在百度APP之下實現, 有點類似微信小程序  
一位講者提到了一個有趣的現象: **玻璃花園**, 描述網際網路的發展由當時的自由開放, 走向被網路巨頭寡佔的割裂時代, 網路巨頭提供的大平台能夠各式各樣的功能, 使用者只需要生活在這個平台之中即可, 如同一個巨大的玻璃花園, 騰訊的微信便是一個很好的例子  
講者宣稱他們提出的小程序平台能夠打破玻璃花園的藩籬, 讓網路回到自由開放的田園時光,  這完全狗屁不通, 白痴都能看出來百度想搞個自己玻璃花園
#### Apollo
本次大會的主角, 與金龍客車量產的小巴士:**阿波龍**, 是最大的亮點, 另外還有農用車的擴展: **阿波牛**,  我會在下面的篇幅詳細介紹它們

###園區小巴的量產-阿波龍
在園區內行駛, 表明阿波龍的駕駛能力並沒有達到消費者所期待的都市級L4, 在這個**量產**對百度來說及其重要  
####生產過程中學習的經驗
搞一台Demo機和量產是兩碼子事情, 量產需要一個高效且嚴格的生產標準來確保商品質量和低成本的生產, 其中百度提到了兩個例子, 多傳感器的校正及傳感器-GPS間的的校正
[image]

[image]

###從車輛到機器人-阿波牛
###商業模式的探索與代碼的演進
###成為中國標準的野心



此時我們就需要D-Star-Lite, Dynamic版本的A\*. 它是A\*的擴展  
當環境發生變化的時候, 它能更新必要的路徑, 有效率的計算新的cost
<br />
<br />

### **Min-Queue 與 DP傳播**

開始介紹算法觀念之前, 我們先看看A\*算法的視覺化

![a-star](/assets/img/a_star.gif){:class="img-responsive"}

你可以看到, 計算由起點**擴散**到終點, 更準確的來說, 計算是由cost低的節點往cost高的節點擴散的. 這個是 **min-queue**和**DP擴散**所導致的  
min-queue確保cost小的node可以比cost高的node更優先計算, 而DP(Dynamic Programming)擴散意味著cost是在node中相互傳遞

這兩個便是A\*以及D-Star-Lite的核心概念

#### **Min Queue**:
<br />
<br />
![minq](/assets/img/d-star-minq.png){:class="img-responsive"}

在Min-quque中, 有當前最小值的節點總是優先被選中, 導致計算總是由最小的節點開始, 一步步往cost高的節點移動
<br />
<br />
#### **DP 傳播公式**
<br />
<br />

$$
g(s) =
\begin{cases}
0 & \text{if s is start point} \\
min_{s' \in Preds(s)} (c(s, s') + g(s')) & \text{otherwise,}
\end{cases}
$$
<br/>
<br />
<br />

![dp](/assets/img/d-star-dp.png){:class="img-responsive"}

從這個式子可以看出, 一個節點的cost的計算依賴於它的母節點  
另外, 如果這個節點的cost夠小, 它也會**傳播**給它的子節點  
這種傳播導致了節點會有**上游**以及**下游**的概念, 上游節點的資訊傳播給下游節點


### **D-Star-Lite**:
這兩個核心概念如何處理動態環境呢？ 相當簡單, 當環境發生變動, 我們便更新對應的節點, 這個被更新的節點便**擴散**到他的鄰近節點, 鄰近節點再擴散它的周圍,形成一種計算漣漪   
DP傳播定義了**cost如何擴散**, 而Min-queue則決定了**擴散的順序**
<br />
<br />
![propa](/assets/img/d-star-propa.png){:class="img-responsive"}

D-Star-Lite引進了兩個數值來實現這個像法, ***g(s)***以及***rhs(s)***  
***g(s)*** 與A\*中的***g(s)***類似, 差別在於這個g值代表著節點***s***的歷史值  
在動態環境中, 我們需要一個機制去記憶cost的變化

至於***rhs(s)***,意思是 right-hand-side value, 它的數值最終會和***g(s)***相等, 但它的角色是去取得節點***s***最即時的更新, ***rhs(s)***總是可以拿到比***g(s)***更新的資訊  
<br />

$$
rhs(s) =
\begin{cases}
0 & \text{if s is start point} \\
min_{s' \in Succ(s)} (c(s, s') + g(s')) & \text{otherwise,}
\end{cases}
$$
<br />

當環境變動的時候, 我們可以利用,***rhs(s)***以及***g(s)***, 來決定是否要更新節點***s***,

<br/>
```
In a node s:
  If rhs(s) == g(s) ---> 更新完畢, s的cost已經計算完成
  If rhs(s) != g(s) ---> 需要更新, cost已經過時了,把s扔進min-queue之中等待更新,
```


由於我們引進了兩個值的關係, min-quque需要一種新的比大小方法, 我們用兩種key value, ***K1***和***K2***來處理大小的比較

$$
key(s) = [k_1(s), k_2(s)]\\
= [\min(g(s), rhs(s)) + h(s),\\
min(g(s), rhs(s)) ]\\
$$
```
Node u  > v
  when K1(u) > K1(v) or K1(U) == K1(U), K2(u) > K2(v)
```
<br />
與A\*相當類似, 差別在於我們現在比較***g(s), rhs(s)***兩者中的最小值. 另外K1和K2的差別只在於是否引進了heuristic value ***h(s)***. 當兩個***K1***相等的時候, 我們便可以用***K2***來進行額外的比較

### 來看看**Pseudo code**吧


Main function中 最關鍵的是 ***ComputerShortestPath()*** 以及 ***UpdateVertex(u)***.  
***ComputerShortestPath()***計算出起點到終點的最小路徑  
 ***UpdateVertex()*** 負責更新環境的變動
```
main():
  Initialize()
  Forever:
    ComputerShortestPath() #pop each s from min-queue and making g(s) = rhs(s)
      if change happens:
        for all directed edges(u, v) with cost changed:
          update the edge cost c(u, v)
          UpdateVertex(u) #Update the rhs(u) and put it into min-queue

```

在初始化的過程中, 將所有cost assign為無限大, 除了起點的rhs ***rhs(s_start)*** assign成0  
這會導致起點的g值與rhs值不一致, 讓演算法開始由起點開始擴散
```
Initalize（）:
  for all nodes s in graph:
    g(s) = rhs(s) = INF
  rhs(s_start) = 0
  min_queue.insert(s_start)
```
在最小路徑的計算中, 我們從min-queue中不斷pop出最小的node, 並計算這個node的cost, 這個while迴圈會不斷執行, 直到我們找到從起到終點的最小路徑, 而且這個數值不能是過時的, 也就是***g(s_start) == rhs(s_start)***
<br />
<br />
當 ***g(s)*** > ***rhs(s)***, 我們將 ***g(s)***  assign 為***rhs(s)***, 代表這個節點完成了更新, 另外這個更新傳播給他的子節點
<br />
<br />
當情況是 ***g(s)*** < ***rhs(s)***, 我們將 ***g(s)*** 設為無限大, 並更新這個節點自身以及他的子節點  
為什麼不跟上一個case一樣, 將***rhs(s)*** 的值塞給 ***g(s)*** ？
因為 ***g(s)*** 的角色是**歷史值**. 即時 ***g(s)*** 是queue中的最小值, 它很有可能已經過時了, 他的**上游**可能還在queue中等著呢, 我們利用把它塞回queue的方式, 讓它能夠正確的**收斂**cost
```
ComputerShortestPath():
  While min_queue.min() < s_start or g(s_star) != rhs(s_start):  #Keep compute until we find a reliable cost of s_start
    u = min_queue.pop() #Get the minimum of the queue
    if(g(u) > rhs(u)):  #Converge u in this case
      g(u) = rhs(u)
      for all u' in successors of u"
        UpdateVertex(u')
    elif(g(u) < rhs(u)): #node u needs to update the value again.
      g(u) = inf
      UpdateVertex(u')
      for all u' in successors of u"
        UpdateVertex(u')

  min_queue.remove(u) if u in min_queue
  min_queue.insert(u) if g(u) != rhs(u)
```

節點更新非常簡單, 只要更新按照公式更新rhs值,並把情況符合***g(u) != rhs(u)***的節點塞進queue中即可

```
UpdateVertex(u):
  rhs(u) = g(u') + c(u', u) where u' has the minimal rhs among predecessor of u
  min_queue.remove(u) if u in min_queue
  min_queue.insert(u) if g(u) != rhs(u)
```
來看看D-Star-Lite的計算如何擴散的
![dp](https://raw.githubusercontent.com/GBJim/d-star-lite/master/demo.gif){:class="img-responsive"}
<br />
<br />

如果想知道實做的更多細節,你可以參考我的repo:
https://github.com/GBJim/d-star-lite


{% include disqus.html %}
