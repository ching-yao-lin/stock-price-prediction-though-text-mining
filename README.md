# 股價預測專案 

(English version is provided below)<br>
<br>
此項專案透過文字探勘技術預測股價。<br>
專案目標：告訴投資者，什麼時候看漲、什麼時候持平、什麼時候看跌。<br>
主要程式碼，位於 `股價預測.ipynb` 檔案中。<br>

**專案的核心技術： 取出「黃金交叉」與「死亡交叉」的關鍵字**
* 分別找出訓練資料中所有「黃金交叉」與「死亡交叉」n天前的文件
* 分別萃取這些文件的關鍵字，作為「黃金交叉」與「死亡交叉」的預測變數/特徵

定義：
* **「黃金交叉」**
  *  週均線由下而上穿過月均線
  *  上升幅度在 3 天內超過 3%
* **「死亡交叉」**
  *  週均線由上而下穿過月均線
  *  下降幅度在 3 天內超過 3%

### 黃金交叉(示意圖：以台積電 2018 年股票為例)
![](/images/golden_cross.png)

### 死亡交叉(示意圖：以台積電 2018 年股票為例)
![](/images/death_cross.png)

# (Eng Ver.) Stock Price Prediction through Text Mining
This project attemps to predict stock prices using text-mining techniques.<br>
Project Goal: Tell investors whether and when a stock price is likely to rise, hold, or fall.<br>
The main code is presented in `股價預測.ipynb`<br>

**The core technique of this project: Extract keywords about Golden-Crosses and Death-Crosses**
* Find the documents occurred within n days before Golden-Crosses and Death-Crosses
* Extract the keywords from these documents as predictors/features

Definition: 
* **Golden-Crosses**, denoted "serious ups" in the code:
  * the week_rolling_mean crosses month_rolling_mean from below (黃金交叉);
  * the markup rate has exceeded r=0.03 within n=3 days
* **Death-Crosses**, denoted "serious downs" in the code:
  * the week_rolling_mean crosses month_rolling_mean from above (死亡交叉);
  * the markdown rate has exceeded r=0.03 within n=3 days

### Golden Cross (Illustration: Taking TSMC stock price in 2018 as an Example)
![](/images/golden_cross.png)

### Death Cross (Illustration: Taking TSMC stock price in 2018 as an Example)
![](/images/death_cross.png)
