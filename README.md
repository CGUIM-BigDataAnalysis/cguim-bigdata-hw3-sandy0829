長庚大學 大數據分析方法 作業三
================

網站資料爬取
------------

``` r
##這是R Code Chunk
##第一次使用要先安裝 install.packages("rvest")
##read_html
##html_nodes
##html_text
##install.packages("rvest")
library(rvest)
```

    ## Warning: package 'rvest' was built under R version 3.3.3

    ## Loading required package: xml2

    ## Warning: package 'xml2' was built under R version 3.3.3

``` r
PPT<- "https://www.ptt.cc/bbs/Tech_Job/index.html"
postTitle<- read_html(PPT) %>%
html_nodes(".title") %>%
html_text()
postPushNum<- read_html(PPT) %>%
html_nodes(".nrec") %>%
html_text()
postAuthor<- read_html(PPT) %>%
html_nodes(".author") %>%
html_text()
df1<- data.frame(Title=postTitle,PushNum=postPushNum,Author=postAuthor)
PPT<- "https://www.ptt.cc/bbs/Tech_Job/index2588.html"
postTitle<- read_html(PPT) %>%
html_nodes(".title") %>%
html_text()
postPushNum<- read_html(PPT) %>%
html_nodes(".nrec") %>%
html_text()
postAuthor<- read_html(PPT) %>%
html_nodes(".author") %>%
html_text()
df2<- data.frame(Title=postTitle,PushNum=postPushNum,Author=postAuthor)
PPT<- "https://www.ptt.cc/bbs/Tech_Job/index2587.html"
postTitle<- read_html(PPT) %>%
html_nodes(".title") %>%
html_text()
postPushNum<- read_html(PPT) %>%
html_nodes(".nrec") %>%
html_text()
postAuthor<- read_html(PPT) %>%
html_nodes(".author") %>%
html_text()
df3<- data.frame(Title=postTitle,PushNum=postPushNum,Author=postAuthor)
PPT<- "https://www.ptt.cc/bbs/Tech_Job/index2586.html"
postTitle<- read_html(PPT) %>%
html_nodes(".title") %>%
html_text()
postPushNum<- read_html(PPT) %>%
html_nodes(".nrec") %>%
html_text()
postAuthor<- read_html(PPT) %>%
html_nodes(".author") %>%
html_text()
df4<- data.frame(Title=postTitle,PushNum=postPushNum,Author=postAuthor)
PPT<- "https://www.ptt.cc/bbs/Tech_Job/index2585.html"
postTitle<- read_html(PPT) %>%
html_nodes(".title") %>%
html_text()
postPushNum<- read_html(PPT) %>%
html_nodes(".nrec") %>%
html_text()
postAuthor<- read_html(PPT) %>%
html_nodes(".author") %>%
html_text()
df5<- data.frame(Title=postTitle,PushNum=postPushNum,Author=postAuthor)
PPT<- "https://www.ptt.cc/bbs/Tech_Job/index2584.html"
postTitle<- read_html(PPT) %>%
html_nodes(".title") %>%
html_text()
postPushNum<- read_html(PPT) %>%
html_nodes(".nrec") %>%
html_text()
postAuthor<- read_html(PPT) %>%
html_nodes(".author") %>%
html_text()
df6<- data.frame(Title=postTitle,PushNum=postPushNum,Author=postAuthor)
total<- rbind(df1,df2,df3,df4,df5,df6)
total
```

    ##                                                                                  Title
    ## 1                                  \n\t\t\t\n\t\t\t\t[請益] 晶睿的二面\n\t\t\t\n\t\t\t
    ## 2              \n\t\t\t\n\t\t\t\t[討論] 台北東區以東 有做server的公司?\n\t\t\t\n\t\t\t
    ## 3                            \n\t\t\t\n\t\t\t\tRe: [討論] 台積電VS中油\n\t\t\t\n\t\t\t
    ## 4                          \n\t\t\t\n\t\t\t\t(本文已被刪除) [pinkkate]\n\t\t\t\n\t\t\t
    ## 5            \n\t\t\t\n\t\t\t\t(已被mmkntust刪除) <lovebridget> 板規三\n\t\t\t\n\t\t\t
    ## 6         \n\t\t\t\n\t\t\t\t[新聞] 晶圓代工誰技術領先？ 英特爾：我最強\n\t\t\t\n\t\t\t
    ## 7                    \n\t\t\t\n\t\t\t\t[請益] 大立光製成助理工程師職務\n\t\t\t\n\t\t\t
    ## 8      \n\t\t\t\n\t\t\t\t[情報] 區塊鏈是採用大型主機銀行的完美資料保護\n\t\t\t\n\t\t\t
    ## 9                 \n\t\t\t\n\t\t\t\t(已被mmkntust刪除) <yryang> 板規一\n\t\t\t\n\t\t\t
    ## 10                     \n\t\t\t\n\t\t\t\t[討論] 南茂南科測試產品工程師\n\t\t\t\n\t\t\t
    ## 11          \n\t\t\t\n\t\t\t\t[新聞] 晶片中心授課講師費惹議 國研院澄清\n\t\t\t\n\t\t\t
    ## 12                     \n\t\t\t\n\t\t\t\t[請益] 億光 樹林廠 研發工程師\n\t\t\t\n\t\t\t
    ## 13                    \n\t\t\t\n\t\t\t\tRe: 請問55歲以上的RD都去那了？\n\t\t\t\n\t\t\t
    ## 14     \n\t\t\t\n\t\t\t\t[請益]大家在校園徵才登入投遞履歷收到面試了嗎?\n\t\t\t\n\t\t\t
    ## 15      \n\t\t\t\n\t\t\t\t律師為您解惑－線上勞動法免費諮詢即日為勞工 …\n\t\t\t\n\t\t\t
    ## 16                  \n\t\t\t\n\t\t\t\t[公告] Tech_Job板板規 2014.03.01\n\t\t\t\n\t\t\t
    ## 17                        \n\t\t\t\n\t\t\t\t[公告] 置底 檢舉/推薦 文章\n\t\t\t\n\t\t\t
    ## 18                                \n\t\t\t\n\t\t\t\t[免費]工作人生顧問\n\t\t\t\n\t\t\t
    ## 19                        \n\t\t\t\n\t\t\t\t[請益] offer請益 友達/華碩\n\t\t\t\n\t\t\t
    ## 20               \n\t\t\t\n\t\t\t\t[請益] 什麼狀況下會選擇"不"出國工作\n\t\t\t\n\t\t\t
    ## 21       \n\t\t\t\n\t\t\t\t[新聞] 《國際產業》人腦結合電腦抗AI，傳馬斯\n\t\t\t\n\t\t\t
    ## 22                     \n\t\t\t\n\t\t\t\tRe: [請益] 關於台積電分紅制度\n\t\t\t\n\t\t\t
    ## 23           \n\t\t\t\n\t\t\t\tRe: [請益] 什麼狀況下會選擇"不"出國工作\n\t\t\t\n\t\t\t
    ## 24                      \n\t\t\t\n\t\t\t\t(本文已被刪除) [Heymandiyya]\n\t\t\t\n\t\t\t
    ## 25     \n\t\t\t\n\t\t\t\t[新聞] 【大立光小心囉～】原來蘋果2013年起　就\n\t\t\t\n\t\t\t
    ## 26           \n\t\t\t\n\t\t\t\tRe: [請益] 什麼狀況下會選擇"不"出國工作\n\t\t\t\n\t\t\t
    ## 27                     \n\t\t\t\n\t\t\t\t[請益] Offer請益 應材CSE/其它\n\t\t\t\n\t\t\t
    ## 28                           \n\t\t\t\n\t\t\t\t(本文已被刪除) [c08516]\n\t\t\t\n\t\t\t
    ## 29                   \n\t\t\t\n\t\t\t\tRe: [請益] 南部 or 北部工作問題\n\t\t\t\n\t\t\t
    ## 30                 \n\t\t\t\n\t\t\t\tRe: [請益] 漢民客服工程師（中科）\n\t\t\t\n\t\t\t
    ## 31                         \n\t\t\t\n\t\t\t\t[請益] 河洛半導體 光學FAE\n\t\t\t\n\t\t\t
    ## 32                \n\t\t\t\n\t\t\t\t(已被lovewsc刪除) <zxc45693>版規七\n\t\t\t\n\t\t\t
    ## 33                           \n\t\t\t\n\t\t\t\tRe: [討論] 台積電VS中油\n\t\t\t\n\t\t\t
    ## 34              \n\t\t\t\n\t\t\t\t[討論] 電的問題對科技業是否影響頗大?\n\t\t\t\n\t\t\t
    ## 35     \n\t\t\t\n\t\t\t\t[新聞] 盼台積電落腳路竹　花媽喊話：給高雄一個\n\t\t\t\n\t\t\t
    ## 36                     \n\t\t\t\n\t\t\t\t(本文已被刪除) [blowblow5566]\n\t\t\t\n\t\t\t
    ## 37                       \n\t\t\t\n\t\t\t\t[請益] 光學+通訊   不錯嗎？\n\t\t\t\n\t\t\t
    ## 38                       \n\t\t\t\n\t\t\t\t[請益] 億達薄膜工程師評價？\n\t\t\t\n\t\t\t
    ## 39                       \n\t\t\t\n\t\t\t\t[聘書] 昇陽光電 VS 漢磊科技\n\t\t\t\n\t\t\t
    ## 40                    \n\t\t\t\n\t\t\t\tRe: [心得] 皮卡丘 五年工作心得\n\t\t\t\n\t\t\t
    ## 41                        \n\t\t\t\n\t\t\t\t宜特 Ic 測試助理工程師面試\n\t\t\t\n\t\t\t
    ## 42                       \n\t\t\t\n\t\t\t\t(本文已被刪除) [KEEPLOVING]\n\t\t\t\n\t\t\t
    ## 43                            \n\t\t\t\n\t\t\t\t(本文已被刪除) [scntu]\n\t\t\t\n\t\t\t
    ## 44      \n\t\t\t\n\t\t\t\t[新聞] 就是要力挺！仁寶參與樂視致新現增7億人\n\t\t\t\n\t\t\t
    ## 45          \n\t\t\t\n\t\t\t\t[情報] 智慧醫療人才培育計畫 徵求赴美人才\n\t\t\t\n\t\t\t
    ## 46       \n\t\t\t\n\t\t\t\t[情報] 智慧機械及航太研發補助計畫宣導說明會\n\t\t\t\n\t\t\t
    ## 47                     \n\t\t\t\n\t\t\t\t[請益] 漢民客服工程師（中科）\n\t\t\t\n\t\t\t
    ## 48        \n\t\t\t\n\t\t\t\t[情報] 台灣史丹福醫材人培計畫 徵求赴美人才\n\t\t\t\n\t\t\t
    ## 49                       \n\t\t\t\n\t\t\t\t[請益] 有人聽過縯忠實業嗎？\n\t\t\t\n\t\t\t
    ## 50                             \n\t\t\t\n\t\t\t\t[請益] 30歲製造業轉職\n\t\t\t\n\t\t\t
    ## 51               \n\t\t\t\n\t\t\t\tRe: [請益] 新規則，休息日加班請假？\n\t\t\t\n\t\t\t
    ## 52       \n\t\t\t\n\t\t\t\t[問卷] 科技業知識分享影響之探討(抽小七禮卷)\n\t\t\t\n\t\t\t
    ## 53                                 \n\t\t\t\n\t\t\t\t[請益] 台塑網面試\n\t\t\t\n\t\t\t
    ## 54                       \n\t\t\t\n\t\t\t\t(本文已被刪除) [d062637776]\n\t\t\t\n\t\t\t
    ## 55                          \n\t\t\t\n\t\t\t\t(本文已被刪除) [shrines]\n\t\t\t\n\t\t\t
    ## 56                                          \n\t\t\t\n\t\t\t\tj:引戰文\n\t\t\t\n\t\t\t
    ## 57                     \n\t\t\t\n\t\t\t\t(本文已被刪除) [likeyoutoboy]\n\t\t\t\n\t\t\t
    ## 58                           \n\t\t\t\n\t\t\t\t[請益] 桃園和台北的薪水\n\t\t\t\n\t\t\t
    ## 59                        \n\t\t\t\n\t\t\t\t[心得] 皮卡丘 五年工作心得\n\t\t\t\n\t\t\t
    ## 60                           \n\t\t\t\n\t\t\t\t[請益] 請問南科統新光訊\n\t\t\t\n\t\t\t
    ## 61                   \n\t\t\t\n\t\t\t\t[請益] 新規則，休息日加班請假？\n\t\t\t\n\t\t\t
    ## 62      \n\t\t\t\n\t\t\t\t[新聞]新日光永旺能源獲8億聯貸 持續擴建太陽能\n\t\t\t\n\t\t\t
    ## 63           \n\t\t\t\n\t\t\t\t[新聞] 工程師癱瘓全台YouBike 恐賠2242萬\n\t\t\t\n\t\t\t
    ## 64                     \n\t\t\t\n\t\t\t\t(本文已被刪除) [hebeisme5566]\n\t\t\t\n\t\t\t
    ## 65                            \n\t\t\t\n\t\t\t\t[請益] 台達研究院面試?\n\t\t\t\n\t\t\t
    ## 66                    \n\t\t\t\n\t\t\t\t[問卷]數位族群數位金融潛力研究\n\t\t\t\n\t\t\t
    ## 67                           \n\t\t\t\n\t\t\t\t[請益] 高雄日月光 offer\n\t\t\t\n\t\t\t
    ## 68                           \n\t\t\t\n\t\t\t\tRe: [討論] 台積電VS中油\n\t\t\t\n\t\t\t
    ## 69                                   \n\t\t\t\n\t\t\t\t[請益] 暢星科技\n\t\t\t\n\t\t\t
    ## 70            \n\t\t\t\n\t\t\t\t[新聞] IC設計兩岸較勁 台廠轉型壓力加劇\n\t\t\t\n\t\t\t
    ## 71                           \n\t\t\t\n\t\t\t\t(本文已被刪除) [Kalisi]\n\t\t\t\n\t\t\t
    ## 72                              \n\t\t\t\n\t\t\t\t[討論] 工程師的定義?\n\t\t\t\n\t\t\t
    ## 73  \n\t\t\t\n\t\t\t\tFw: [徵才]台中外商徵angular / hybrid app開發人員\n\t\t\t\n\t\t\t
    ## 74                        \n\t\t\t\n\t\t\t\t[請益] Offer請益 怡利/友達\n\t\t\t\n\t\t\t
    ## 75                       \n\t\t\t\n\t\t\t\t(本文已被刪除) [sercet0728]\n\t\t\t\n\t\t\t
    ## 76                             \n\t\t\t\n\t\t\t\t(本文已被刪除) [Pand]\n\t\t\t\n\t\t\t
    ## 77           \n\t\t\t\n\t\t\t\t[徵才] 北科車輛所徵求碩士級專任助理兩名\n\t\t\t\n\t\t\t
    ## 78                        \n\t\t\t\n\t\t\t\t[請益] 利得儀器-工程部助工\n\t\t\t\n\t\t\t
    ## 79                           \n\t\t\t\n\t\t\t\tRe: [討論] 台積電VS中油\n\t\t\t\n\t\t\t
    ## 80                                 \n\t\t\t\n\t\t\t\t[請益] 台積vs世界\n\t\t\t\n\t\t\t
    ## 81                               \n\t\t\t\n\t\t\t\t[請益] 暑期實習請益\n\t\t\t\n\t\t\t
    ## 82                 \n\t\t\t\n\t\t\t\tFw: [台北] 推手媒體誠徵後端工程師\n\t\t\t\n\t\t\t
    ## 83                          \n\t\t\t\n\t\t\t\t(本文已被刪除) [sheu123]\n\t\t\t\n\t\t\t
    ## 84                       \n\t\t\t\n\t\t\t\t[請益] Offer請益(仁寶/緯創)\n\t\t\t\n\t\t\t
    ## 85                          \n\t\t\t\n\t\t\t\t[新聞] 台積i8單 下月量產\n\t\t\t\n\t\t\t
    ## 86                               \n\t\t\t\n\t\t\t\t[討論] 聯穎光電面試\n\t\t\t\n\t\t\t
    ## 87                               \n\t\t\t\n\t\t\t\t[請益] 大中積體電路\n\t\t\t\n\t\t\t
    ## 88                      \n\t\t\t\n\t\t\t\t[請益] 弘馳公司 面試前的準備\n\t\t\t\n\t\t\t
    ## 89                           \n\t\t\t\n\t\t\t\t[討論] 離職最後一根稻草\n\t\t\t\n\t\t\t
    ## 90       \n\t\t\t\n\t\t\t\t[請益]力成panel fan-out 製程整合 & 群創製程\n\t\t\t\n\t\t\t
    ## 91                       \n\t\t\t\n\t\t\t\tRe: [討論] 試用期超過三個月\n\t\t\t\n\t\t\t
    ## 92                          \n\t\t\t\n\t\t\t\t[討論] （樹林）瑞傳  smt\n\t\t\t\n\t\t\t
    ## 93                         \n\t\t\t\n\t\t\t\t[請益] 關於AirU x FinTech\n\t\t\t\n\t\t\t
    ## 94        \n\t\t\t\n\t\t\t\t[新聞] 虧得一塌糊塗 太陽能矽晶圓廠等待黎明\n\t\t\t\n\t\t\t
    ## 95                           \n\t\t\t\n\t\t\t\t[請益] 台積測試設備助工\n\t\t\t\n\t\t\t
    ## 96                     \n\t\t\t\n\t\t\t\t[請益] 推薦的layout工程師工作\n\t\t\t\n\t\t\t
    ## 97                       \n\t\t\t\n\t\t\t\t[討論] 一天實際工作的時數？\n\t\t\t\n\t\t\t
    ## 98                      \n\t\t\t\n\t\t\t\t[請益] 面試要報告的 碩士論文\n\t\t\t\n\t\t\t
    ## 99                                     \n\t\t\t\n\t\t\t\t捷普 綠點刀具\n\t\t\t\n\t\t\t
    ## 100                                \n\t\t\t\n\t\t\t\t[請益] 日商安立知\n\t\t\t\n\t\t\t
    ## 101       \n\t\t\t\n\t\t\t\t[情報] 蘋果申請具備iPhone核心之Macbook產品\n\t\t\t\n\t\t\t
    ## 102    \n\t\t\t\n\t\t\t\t[請益]有人收到德州儀器技術行銷工程師面試邀請?\n\t\t\t\n\t\t\t
    ## 103                      \n\t\t\t\n\t\t\t\t[請益] 請問陸資的IC設計公司\n\t\t\t\n\t\t\t
    ## 104                    \n\t\t\t\n\t\t\t\t[請益] 德州儀器設備工程師實習\n\t\t\t\n\t\t\t
    ## 105                              \n\t\t\t\n\t\t\t\t[討論] 國家光電好嗎\n\t\t\t\n\t\t\t
    ## 106                  \n\t\t\t\n\t\t\t\tRe: [請益] 請問陸資的IC設計公司\n\t\t\t\n\t\t\t
    ## 107                      \n\t\t\t\n\t\t\t\t[請益] 是否該調往偏鄉工作？\n\t\t\t\n\t\t\t
    ## 108                          \n\t\t\t\n\t\t\t\t(本文已被刪除) [lponnn]\n\t\t\t\n\t\t\t
    ## 109                        \n\t\t\t\n\t\t\t\t[請益] 關於科技業或是保險\n\t\t\t\n\t\t\t
    ## 110                       \n\t\t\t\n\t\t\t\t[請益] Advantest二手設備商\n\t\t\t\n\t\t\t
    ## 111                              \n\t\t\t\n\t\t\t\tFw: [請益] 夜間進修\n\t\t\t\n\t\t\t
    ## 112                                  \n\t\t\t\n\t\t\t\t[請益] 華通電腦\n\t\t\t\n\t\t\t
    ## 113           \n\t\t\t\n\t\t\t\t[討論] 矽品好像沒有板上說的那麼不好吧~\n\t\t\t\n\t\t\t
    ## 114                        \n\t\t\t\n\t\t\t\t(本文已被刪除) [ScrewYou]\n\t\t\t\n\t\t\t
    ## 115                              \n\t\t\t\n\t\t\t\t[討論] 台積電VS中油\n\t\t\t\n\t\t\t
    ## 116                        \n\t\t\t\n\t\t\t\t(本文已被刪除) [p4818046]\n\t\t\t\n\t\t\t
    ## 117                          \n\t\t\t\n\t\t\t\t[請益] 金屬工業中心面試\n\t\t\t\n\t\t\t
    ## 118              \n\t\t\t\n\t\t\t\t[請益] 在職碩班選擇請益，中興vs中央\n\t\t\t\n\t\t\t
    ##     PushNum       Author
    ## 1         1       tiyico
    ## 2         5     sustaned
    ## 3         3     tomtowin
    ## 4         9            -
    ## 5         6            -
    ## 6        12   momoko0581
    ## 7         4     S0031104
    ## 8               chunnitu
    ## 9         4            -
    ## 10                chag06
    ## 11            nickerChen
    ## 12               amo1126
    ## 13               zxc0312
    ## 14                 wer11
    ## 15       爆          pzs
    ## 16        7     mmkntust
    ## 17       爆     mmkntust
    ## 18       爆       zodiac
    ## 19       17    s98115145
    ## 20       43   douglennon
    ## 21       10       BBMADE
    ## 22        9  magic704226
    ## 23       11   kenshin528
    ## 24       11            -
    ## 25       19 qazxc1156892
    ## 26        8  lovebridget
    ## 27        8      Chaobig
    ## 28                     -
    ## 29        3       Hatake
    ## 30        8    sendtony6
    ## 31        7  zeromichael
    ## 32       X2            -
    ## 33        9     va1kyrie
    ## 34       37     lovepork
    ## 35       33     zzzz8931
    ## 36       14            -
    ## 37       17    a40232145
    ## 38        2  lattecoffee
    ## 39        7    qazwsx517
    ## 40        5  magic704226
    ## 41        3        yens1
    ## 42                     -
    ## 43        1            -
    ## 44       11     wahaha23
    ## 45               Gojilla
    ## 46             gil729181
    ## 47       15  qoo63112000
    ## 48               Gojilla
    ## 49               foc0327
    ## 50        9     shesaya1
    ## 51        7     eladamri
    ## 52                awkman
    ## 53        1   pttstrider
    ## 54        1            -
    ## 55                     -
    ## 56       X2            -
    ## 57                     -
    ## 58        7         J774
    ## 59       23   xx10231202
    ## 60        3    ggyy08957
    ## 61       17   ggg1356114
    ## 62              moonth66
    ## 63       28      kellywu
    ## 64        1            -
    ## 65        3    Aloha0527
    ## 66               olivesu
    ## 67       12  RacingSport
    ## 68       10 FcukYouChina
    ## 69            Eighteen18
    ## 70        8    Nicher116
    ## 71        6            -
    ## 72       31    nhcuejunk
    ## 73                uborek
    ## 74        8      ccc0901
    ## 75                     -
    ## 76        2            -
    ## 77             Pocky5566
    ## 78               shinfon
    ## 79        8     tomtowin
    ## 80       55       q7w8s5
    ## 81        5        quasi
    ## 82          ssmartdan841
    ## 83        1            -
    ## 84       14  johnnypk321
    ## 85       20       unrest
    ## 86               key9028
    ## 87          pieceofacake
    ## 88        3     AlioAlio
    ## 89       51    NTUlosers
    ## 90        5      vacfann
    ## 91        4        dakkk
    ## 92              usa71111
    ## 93        1       Wizarc
    ## 94       17        ErioT
    ## 95       24       qlb144
    ## 96        7   ihavejason
    ## 97        8    lukenming
    ## 98        2       KIRA47
    ## 99        3     tn372845
    ## 100       5       pjc202
    ## 101       4       zxcvxx
    ## 102       4        wer11
    ## 103      10   DigiTalent
    ## 104       4         oeys
    ## 105               chag06
    ## 106      20   DigiTalent
    ## 107      54     NakiXIII
    ## 108       5            -
    ## 109       3       dfg512
    ## 110       5         CA42
    ## 111             neon2102
    ## 112       6 jackjack0805
    ## 113      62     goodlike
    ## 114      15            -
    ## 115      13        ej4g4
    ## 116       1            -
    ## 117       1     huaygina
    ## 118      11         AKFG

爬蟲結果呈現
------------

``` r
#這是R Code Chunk
knitr::kable(total) ##請將iris取代為上個步驟中產生的爬蟲資料資料框
```

| Title                                              | PushNum | Author       |
|:---------------------------------------------------|:--------|:-------------|
| \[請益\] 晶睿的二面                                | 1       | tiyico       |
| \[討論\] 台北東區以東 有做server的公司?            | 5       | sustaned     |
| Re: \[討論\] 台積電VS中油                          | 3       | tomtowin     |
| (本文已被刪除) \[pinkkate\]                        | 9       | -            |
| (已被mmkntust刪除) <lovebridget> 板規三            | 6       | -            |
| \[新聞\] 晶圓代工誰技術領先？ 英特爾：我最強       | 12      | momoko0581   |
| \[請益\] 大立光製成助理工程師職務                  | 4       | S0031104     |
| \[情報\] 區塊鏈是採用大型主機銀行的完美資料保護    |         | chunnitu     |
| (已被mmkntust刪除) <yryang> 板規一                 | 4       | -            |
| \[討論\] 南茂南科測試產品工程師                    |         | chag06       |
| \[新聞\] 晶片中心授課講師費惹議 國研院澄清         |         | nickerChen   |
| \[請益\] 億光 樹林廠 研發工程師                    |         | amo1126      |
| Re: 請問55歲以上的RD都去那了？                     |         | zxc0312      |
| \[請益\]大家在校園徵才登入投遞履歷收到面試了嗎?    |         | wer11        |
| 律師為您解惑－線上勞動法免費諮詢即日為勞工 …       | 爆      | pzs          |
| \[公告\] Tech\_Job板板規 2014.03.01                | 7       | mmkntust     |
| \[公告\] 置底 檢舉/推薦 文章                       | 爆      | mmkntust     |
| \[免費\]工作人生顧問                               | 爆      | zodiac       |
| \[請益\] offer請益 友達/華碩                       | 17      | s98115145    |
| \[請益\] 什麼狀況下會選擇"不"出國工作              | 43      | douglennon   |
| \[新聞\] 《國際產業》人腦結合電腦抗AI，傳馬斯      | 10      | BBMADE       |
| Re: \[請益\] 關於台積電分紅制度                    | 9       | magic704226  |
| Re: \[請益\] 什麼狀況下會選擇"不"出國工作          | 11      | kenshin528   |
| (本文已被刪除) \[Heymandiyya\]                     | 11      | -            |
| \[新聞\] 【大立光小心囉～】原來蘋果2013年起　就    | 19      | qazxc1156892 |
| Re: \[請益\] 什麼狀況下會選擇"不"出國工作          | 8       | lovebridget  |
| \[請益\] Offer請益 應材CSE/其它                    | 8       | Chaobig      |
| (本文已被刪除) \[c08516\]                          |         | -            |
| Re: \[請益\] 南部 or 北部工作問題                  | 3       | Hatake       |
| Re: \[請益\] 漢民客服工程師（中科）                | 8       | sendtony6    |
| \[請益\] 河洛半導體 光學FAE                        | 7       | zeromichael  |
| (已被lovewsc刪除) <zxc45693>版規七                 | X2      | -            |
| Re: \[討論\] 台積電VS中油                          | 9       | va1kyrie     |
| \[討論\] 電的問題對科技業是否影響頗大?             | 37      | lovepork     |
| \[新聞\] 盼台積電落腳路竹　花媽喊話：給高雄一個    | 33      | zzzz8931     |
| (本文已被刪除) \[blowblow5566\]                    | 14      | -            |
| \[請益\] 光學+通訊 不錯嗎？                        | 17      | a40232145    |
| \[請益\] 億達薄膜工程師評價？                      | 2       | lattecoffee  |
| \[聘書\] 昇陽光電 VS 漢磊科技                      | 7       | qazwsx517    |
| Re: \[心得\] 皮卡丘 五年工作心得                   | 5       | magic704226  |
| 宜特 Ic 測試助理工程師面試                         | 3       | yens1        |
| (本文已被刪除) \[KEEPLOVING\]                      |         | -            |
| (本文已被刪除) \[scntu\]                           | 1       | -            |
| \[新聞\] 就是要力挺！仁寶參與樂視致新現增7億人     | 11      | wahaha23     |
| \[情報\] 智慧醫療人才培育計畫 徵求赴美人才         |         | Gojilla      |
| \[情報\] 智慧機械及航太研發補助計畫宣導說明會      |         | gil729181    |
| \[請益\] 漢民客服工程師（中科）                    | 15      | qoo63112000  |
| \[情報\] 台灣史丹福醫材人培計畫 徵求赴美人才       |         | Gojilla      |
| \[請益\] 有人聽過縯忠實業嗎？                      |         | foc0327      |
| \[請益\] 30歲製造業轉職                            | 9       | shesaya1     |
| Re: \[請益\] 新規則，休息日加班請假？              | 7       | eladamri     |
| \[問卷\] 科技業知識分享影響之探討(抽小七禮卷)      |         | awkman       |
| \[請益\] 台塑網面試                                | 1       | pttstrider   |
| (本文已被刪除) \[d062637776\]                      | 1       | -            |
| (本文已被刪除) \[shrines\]                         |         | -            |
| j:引戰文                                           | X2      | -            |
| (本文已被刪除) \[likeyoutoboy\]                    |         | -            |
| \[請益\] 桃園和台北的薪水                          | 7       | J774         |
| \[心得\] 皮卡丘 五年工作心得                       | 23      | xx10231202   |
| \[請益\] 請問南科統新光訊                          | 3       | ggyy08957    |
| \[請益\] 新規則，休息日加班請假？                  | 17      | ggg1356114   |
| \[新聞\]新日光永旺能源獲8億聯貸 持續擴建太陽能     |         | moonth66     |
| \[新聞\] 工程師癱瘓全台YouBike 恐賠2242萬          | 28      | kellywu      |
| (本文已被刪除) \[hebeisme5566\]                    | 1       | -            |
| \[請益\] 台達研究院面試?                           | 3       | Aloha0527    |
| \[問卷\]數位族群數位金融潛力研究                   |         | olivesu      |
| \[請益\] 高雄日月光 offer                          | 12      | RacingSport  |
| Re: \[討論\] 台積電VS中油                          | 10      | FcukYouChina |
| \[請益\] 暢星科技                                  |         | Eighteen18   |
| \[新聞\] IC設計兩岸較勁 台廠轉型壓力加劇           | 8       | Nicher116    |
| (本文已被刪除) \[Kalisi\]                          | 6       | -            |
| \[討論\] 工程師的定義?                             | 31      | nhcuejunk    |
| Fw: \[徵才\]台中外商徵angular / hybrid app開發人員 |         | uborek       |
| \[請益\] Offer請益 怡利/友達                       | 8       | ccc0901      |
| (本文已被刪除) \[sercet0728\]                      |         | -            |
| (本文已被刪除) \[Pand\]                            | 2       | -            |
| \[徵才\] 北科車輛所徵求碩士級專任助理兩名          |         | Pocky5566    |
| \[請益\] 利得儀器-工程部助工                       |         | shinfon      |
| Re: \[討論\] 台積電VS中油                          | 8       | tomtowin     |
| \[請益\] 台積vs世界                                | 55      | q7w8s5       |
| \[請益\] 暑期實習請益                              | 5       | quasi        |
| Fw: \[台北\] 推手媒體誠徵後端工程師                |         | ssmartdan841 |
| (本文已被刪除) \[sheu123\]                         | 1       | -            |
| \[請益\] Offer請益(仁寶/緯創)                      | 14      | johnnypk321  |
| \[新聞\] 台積i8單 下月量產                         | 20      | unrest       |
| \[討論\] 聯穎光電面試                              |         | key9028      |
| \[請益\] 大中積體電路                              |         | pieceofacake |
| \[請益\] 弘馳公司 面試前的準備                     | 3       | AlioAlio     |
| \[討論\] 離職最後一根稻草                          | 51      | NTUlosers    |
| \[請益\]力成panel fan-out 製程整合 & 群創製程      | 5       | vacfann      |
| Re: \[討論\] 試用期超過三個月                      | 4       | dakkk        |
| \[討論\] （樹林）瑞傳 smt                          |         | usa71111     |
| \[請益\] 關於AirU x FinTech                        | 1       | Wizarc       |
| \[新聞\] 虧得一塌糊塗 太陽能矽晶圓廠等待黎明       | 17      | ErioT        |
| \[請益\] 台積測試設備助工                          | 24      | qlb144       |
| \[請益\] 推薦的layout工程師工作                    | 7       | ihavejason   |
| \[討論\] 一天實際工作的時數？                      | 8       | lukenming    |
| \[請益\] 面試要報告的 碩士論文                     | 2       | KIRA47       |
| 捷普 綠點刀具                                      | 3       | tn372845     |
| \[請益\] 日商安立知                                | 5       | pjc202       |
| \[情報\] 蘋果申請具備iPhone核心之Macbook產品       | 4       | zxcvxx       |
| \[請益\]有人收到德州儀器技術行銷工程師面試邀請?    | 4       | wer11        |
| \[請益\] 請問陸資的IC設計公司                      | 10      | DigiTalent   |
| \[請益\] 德州儀器設備工程師實習                    | 4       | oeys         |
| \[討論\] 國家光電好嗎                              |         | chag06       |
| Re: \[請益\] 請問陸資的IC設計公司                  | 20      | DigiTalent   |
| \[請益\] 是否該調往偏鄉工作？                      | 54      | NakiXIII     |
| (本文已被刪除) \[lponnn\]                          | 5       | -            |
| \[請益\] 關於科技業或是保險                        | 3       | dfg512       |
| \[請益\] Advantest二手設備商                       | 5       | CA42         |
| Fw: \[請益\] 夜間進修                              |         | neon2102     |
| \[請益\] 華通電腦                                  | 6       | jackjack0805 |
| \[討論\] 矽品好像沒有板上說的那麼不好吧~           | 62      | goodlike     |
| (本文已被刪除) \[ScrewYou\]                        | 15      | -            |
| \[討論\] 台積電VS中油                              | 13      | ej4g4        |
| (本文已被刪除) \[p4818046\]                        | 1       | -            |
| \[請益\] 金屬工業中心面試                          | 1       | huaygina     |
| \[請益\] 在職碩班選擇請益，中興vs中央              | 11      | AKFG         |

解釋爬蟲結果
------------

``` r
#這是R Code Chunk
nrow(total)
```

    ## [1] 118

``` r
##總共有110篇文章，其中最多文章是請教別人問題的文章；或者是發一些有關工作的新聞
```

解釋解釋解釋解釋

``` r
#這是R Code Chunk
table(total$Author)
```

    ## 
    ##            -      amo1126       chag06     chunnitu     mmkntust 
    ##           21            1            2            1            2 
    ##   momoko0581   nickerChen          pzs     S0031104     sustaned 
    ##            1            1            1            1            1 
    ##       tiyico     tomtowin        wer11       zodiac      zxc0312 
    ##            1            2            2            1            1 
    ##    a40232145       BBMADE      Chaobig   douglennon       Hatake 
    ##            1            1            1            1            1 
    ##   kenshin528  lattecoffee  lovebridget     lovepork  magic704226 
    ##            1            1            1            1            2 
    ## qazxc1156892    s98115145    sendtony6     va1kyrie  zeromichael 
    ##            1            1            1            1            1 
    ##     zzzz8931       awkman     eladamri      foc0327    gil729181 
    ##            1            1            1            1            1 
    ##      Gojilla         J774   pttstrider    qazwsx517  qoo63112000 
    ##            2            1            1            1            1 
    ##     shesaya1     wahaha23        yens1    Aloha0527      ccc0901 
    ##            1            1            1            1            1 
    ##   Eighteen18 FcukYouChina   ggg1356114    ggyy08957      kellywu 
    ##            1            1            1            1            1 
    ##     moonth66    nhcuejunk    Nicher116      olivesu    Pocky5566 
    ##            1            1            1            1            1 
    ##  RacingSport      shinfon       uborek   xx10231202     AlioAlio 
    ##            1            1            1            1            1 
    ##        dakkk        ErioT   ihavejason  johnnypk321      key9028 
    ##            1            1            1            1            1 
    ##       KIRA47    lukenming    NTUlosers pieceofacake       q7w8s5 
    ##            1            1            1            1            1 
    ##       qlb144        quasi ssmartdan841       unrest     usa71111 
    ##            1            1            1            1            1 
    ##      vacfann       Wizarc         AKFG         CA42       dfg512 
    ##            1            1            1            1            1 
    ##   DigiTalent        ej4g4     goodlike     huaygina jackjack0805 
    ##            2            1            1            1            1 
    ##     NakiXIII     neon2102         oeys       pjc202     tn372845 
    ##            1            1            1            1            1 
    ##       zxcvxx 
    ##            1

``` r
##每個作者的發文數都差不多都只有一篇或兩篇，被刪文的有16篇
```

解釋解釋解釋解釋

人工結論與解釋解釋解釋解釋解釋解釋解釋

雖然在PTT上問問題的人很多，但是這種文章通常都不太會有推文數，反而是其他公告事情或是新聞的文章，比較多人關注
