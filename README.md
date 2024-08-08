# 演化計算導論
姓名：李名智
學號：1102924
主題：GA_Ackley function
### 一、計畫目標：
產生初始群集並利用Ackley function將此群集基因有較好的品質，Fitness越小則越佳。
### 二、計畫內容：
利用隨機變數來產生基因，並將基因(Chromosome)存至群集(Poplution)中，利用Ackley function當作fitness，其中值越小代表基因具有較好的品質，選擇方式利用菁英挑選法(預設3菁英)，挑選前幾名fitness較好的菁英基因來做交配及突變，交配方式利用單點交配(設定交配率為0.9)，利用隨機變數來決定是否交配，突變利用單點突變(突變率為0.2)，亦是利用隨機變數來決定是否突變。另外全部數量設為30，維度設為5，菁英及bit數個別設為3及4，希望選擇方法1000次迭代後，最佳fitness值為0，且該最佳基因為[0,0,0,0,0]。
### 三、計畫執行之方法與步驟： 
利用python來實行，步驟設置個流程之函式，生成基因並放置族群，設置fitness function(本計畫使用Ackley function)，選方式用挑選前幾名fitness較好菁英挑選法，交配利用單點交配(交配率0.9)，突變利用單點突變(突變率0.2)，主程式利用以上函式找出最佳值。
