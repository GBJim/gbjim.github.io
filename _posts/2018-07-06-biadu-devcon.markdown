---
layout: post
title:  "2018 Baidu Developer Conference -- The Ambition of Apollo"
date:   2018-07-08 00:59:29 +0800
categories: conference
ref: baidu-devcon
lang: en
comments: true
---
### **Prologue**
Attending Baidu Developer Conference is one of the task my business trip to Beijing. As an Autonomous Driving Engineer, I will focus on Apollo project in this article.  
Although this conference claims to target the developers as the audience, there are not much technical information presented. It is more like a promotion to convince the potential allies to join to join the League of Apollo.  
I summarized the message of Baidu as follows: **Look at me, I am freaking awesome. There are so many successful cases of Apollo. Join us and make the Apollo the Chinese Standard of Autonomous Driving**

<br />

![intro](/assets/img/bc-con.jpg){:class="img-responsive"}
*The conference was hold in China National Convention Center*  
<br />

### **General Feeling of the Presentations**
A great beginning that goes down.
After the intro of awesome electronic music and Dubsteps, Robin Li, CEO of Baidu, started the presentation. His smooth tone and good-looking gives him the great charisma on the stage. During his presentation, a live stream shows the moment of the 100th production of self-driving L4 minibus in Xiamen factory. This is truly a shocking moment to me.  
After the CEO opening, each presentations got worse and even more. The contents keep repeating it's self and speakers were not able to talk naturally. There were even a speaker recites the whole presentation. I believe the Baidu talking bot can do a better job.  
In the other hand, the organization of events are confusing. The traffic flow was badly managed and the some of the agenda were modified without any notifications. I would say this disappointing for a Chinese leading company like Baidu.  
Nevertheless, I had learned lots of lessons from the conference. Let's get started.

=================================Under Construction==================================
### **四大開放大平台**
會議重點圍繞這下面這四個開放給所有開發者的平台

#### **DuerOS**
就是一個語音交互系統, 百度希望開發者們一同開發各種功能, 並說服客戶裝上DuerOS  
我不理解這有什麼商機潛力, 在車上裝個DuerOS或許可以為無法動手的司機提供便利的互動, 但是一隻手機完全可以作到這些功能, 更不用說放在家中的智慧音箱了, 相當多餘    
另外語音交互僅是一種操作介面, 可以視為鍵盤或是滑鼠的替代, 系統能不能藉由你的輸入產生極度智慧的動作, 是另一碼子事  
#### **百度大腦**
一個具有200種功能的大雜燴平台, 你能想到的它都有  
這種平台能夠處理被一些被良好定義的經典Machine Learning問題,  讓沒有ML相關知識的開發者解決簡單的問題, **簡單的問題並非沒有價值**  
李彥宏當時在台上邀請了一位來自**西藏的醫師**, 這位醫師利用百度的平台訓練了一個**辨識水中寄生蟲**的模型, 高辨識精度的模型能夠取代寄生蟲專家的識別, 這在西藏這樣地廣人稀的地方極其珍貴  
這讓我相當感動, 這位醫生用科技改善生活, 讓世界變得更好, 而不是那種多塞幾個鏡頭到手機上, 讓物質更加奢侈的努力
![doctor](/assets/img/bc-doctor.jpg){:class="img-responsive"}
*建立寄生蟲檢測模型的西藏醫師, 這個世界需要更多這樣的人*
<br />

#### **百度小程序**
簡單來說就是百度搞一個APP大平台, 所有功能都在百度APP之下實現, 有點類似微信小程序  
一位講者提到了一個有趣的現象: **玻璃花園**, 描述網際網路的發展由當時的自由開放, 走向**被網路巨頭寡佔的割裂時代**, 網路巨頭提供的大平台能夠各式各樣的功能, 使用者只需要生活在這個平台之中即可, 如同一個巨大的玻璃花園, 騰訊的微信便是一個很好的例子  
講者宣稱他們提出的小程序平台能夠打破玻璃花園的藩籬, 讓網路回到自由開放的田園時光,  這完全**狗屁不通**, 白痴都能看出來百度想自己搞個玻璃花園  
![lie](/assets/img/bc-lie.jpeg){:class="img-responsive"}
<br />

#### **Apollo**
本次大會的主角, 與金龍客車量產的小巴士:**阿波龍**, 是最大的亮點, 另外還有農用車的擴展: **阿波牛**,  我會在下面的篇幅詳細介紹它們
<br />
<br />

### **園區小巴的量產-阿波龍**
![bus](/assets/img/bc-bus.jpg){:class="img-responsive"}
*金龍的無人小巴士和sensor設計圖*
<br />

在園區內行駛, 表明阿波龍的駕駛能力並沒有達到消費者所期待的都市級L4, 但這個**量產經驗**對百度來說仍然相當重要  
量產是搞Demo是兩碼子事, 量產需要一個高效且嚴格的生產標準來達成高品質和低成本, 其中百度提到了兩個技術案例, 多傳感器的校正及GPS與傳感間的的校正  
另外量產後的車輛也能不斷蒐集寶貴的數據, 讓百度能夠快速迭代下一代產品  
<br />

![sesonr1](/assets/img/bc-sensor-cali1.jpg){:class="img-responsive"}
*在金龍廈門工廠建造的標定空間, 利用牆壁上的上二維碼達到激光雷達與攝影機的校正*
<br />

![sensor2](/assets/img/bc-sensor-cali.jpg){:class="img-responsive"}
*激光雷達與GPS間的校正則利用繞八字的方式完成, 原理我尚未明白(掩面)*
<br />



### **從車輛到機器人-阿波牛**
與造車廠保守的車本位思想不同, 互聯網企業能夠更靈活的**拓展自動駕駛的範疇**, 除了只載貨物的物流車之外,其中有兩家公司利用了Apollo框架搭建了機器人, 讓人眼睛一亮  
深圳的酷哇機器人動起了清掃自動化的頭腦, 打算用機器人滿足中國龐大的清掃需求  
另外青島的托爾泰克則搞了一台自動噴藥車, 名為阿波牛, 這種科技結合土地的案例太讓我興奮啦！
![cow](/assets/img/bc-cow.jpg){:class="img-responsive"}
*在青島噴藥的阿波牛*
<br />

### **商業模式的探索與代碼的演進**
從17年7月, Apollo開源, 百度就有建立生態圈的想法了, 當時的1.0相當不完整, 許多模塊只有空殼框架, 缺少實現功能的代碼, 被評價為一場商業宣傳  
而後版本更迭, 開始將低成本傳感器方案以及量產的概念融入代碼, 體現了百度在無人車商業化的探索, 從目標尚未明確的散彈槍式宣傳, 到後來目標明確的園區車量產    
相信之後的商業模式變遷也會反應在Apollo這個項目上
![evolve](/assets/img/bc-evolve.png){:class="img-responsive"}
*Apollo的演進與版本重點*
<br />
<br />
### **成為中國標準的野心**
利用Apollo建立一個自駕同盟的計畫進展的相當順利, 百度這次除了拉到了比亞迪汽車一起站台外, 其他大大小小的車廠也有著不同規模的合作, 像是現代汽車搭載了語音互動的系統, 傳感器廠商提供Apollo的硬體支持等等    
這次百度更進一步的提出了硬體整合平台, 讓硬體廠更有彈性的相容於Apollo, 甚至提出了百度認證車輛的概念, 想成為中國標準的野心一目了然  
![number](/assets/img/bc-number.jpeg){:class="img-responsive"}
*Apollo同盟的統計數據*
<br />
<br />

儘管百度沒有生產車輛的能耐, 但憑藉互聯網公司高速釋出產品和快速迭代的能力, 利用代碼開源打了一場閃電戰, 快速組織出了一個自駕同盟, 雖然如此還不能為百度帶來現金收益, 但已經為將來的發展打下了扎實的基礎
![for-all](/assets/img/bc-for-all.jpg){:class="img-responsive"}
*百度的無人車野心*
