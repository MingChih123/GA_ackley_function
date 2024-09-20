# 演化計算導論
姓名：李名智

學號：1102924

主題：GA_Ackley function
### 一、計畫目標：
基因演算法是一種優化演算法，依“進化論”中所提出的「物競天擇，適者生存，不適者淘汰」的生物演化法則而來，本專案模擬基因的優勝劣汰，以進行最佳化的計算。簡單步驟，產生初始群集並利用Ackley function將此群集基因有較好的品質，Fitness越小則越佳。
Ackley function是一個經典的多峰優化問題，適合用來測試演算法在解決全域優化問題時的表現。這個函數有很多局部極小值點（local minima），但只有一個全域極小值點（global minimum），因此對於演算法來說，能否避開局部極小值並找到全域最小值具有挑戰性的。
### 二、計畫內容：
利用隨機變數來產生基因，並將基因(Chromosome)存至群集(Poplution)中，利用Ackley function當作fitness，其中值越小代表基因具有較好的品質，選擇方式利用菁英挑選法(預設3菁英)，挑選前幾名fitness較好的菁英基因來做交配及突變，交配方式利用單點交配(設定交配率為0.9)，利用隨機變數來決定是否交配，突變利用單點突變(突變率為0.2)，亦是利用隨機變數來決定是否突變。另外全部數量設為30，維度設為5，菁英及bit數個別設為3及4，希望選擇方法1000次迭代後，最佳fitness值為0，且該最佳基因為[0,0,0,0,0]。
### 三、計畫執行之方法與步驟： 
利用python來實行，步驟設置個流程之函式，生成基因並放置族群，設置fitness function(本計畫使用Ackley function)，選方式用挑選前幾名fitness較好菁英挑選法，交配利用單點交配(交配率0.9)，突變利用單點突變(突變率0.2)，主程式利用以上函式找出最佳值。

### 四、實驗結果
#### 1.利用不同菁英挑選的方式
![image](https://github.com/user-attachments/assets/05f5710f-bcb0-4156-bd8f-d40b3be345ca)
![image](https://github.com/user-attachments/assets/5419297e-6bd2-4fed-b2c1-2f3c10d8eefe)
![image](https://github.com/user-attachments/assets/9a5b49e1-f5aa-4906-8735-f0c753f85432)

#### 2.改變最大迭代次數(1000vs10000)


##### Test1:左為迭代1000(共花0秒，最佳值約7.7)，右為迭代10000(共花10秒，最佳值約2.4)

![image](https://github.com/user-attachments/assets/563959ed-3bc8-4a24-91a8-8a1a9bebc300)

##### Test2:左為迭代1000(共花1秒，最佳值約4.9)，右為迭代10000(共花7秒，最佳值約4.2)

![image](https://github.com/user-attachments/assets/9b9d562a-bae8-4739-b8df-5f0e55e6e203)

##### Test3:左為迭代1000(共花0秒，最佳值約7.9)，右為迭代10000(共花6秒，最佳值約3.9)

![image](https://github.com/user-attachments/assets/f9cfab4f-5ddb-4535-ad3d-e8413a0d8d6b)

### 五、結論
結論，迭代多次花的時間比較久但可以找到更好的最佳值。

程式碼網址；https://colab.research.google.com/drive/16Ckip0VgOJOJTlA2WKW8NmeVW2f99qFN?usp=sharing
