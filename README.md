# AI-CUP 多模態病理嗓音分類競賽

[AI 競賽官方網站](https://tbrain.trendmicro.com.tw/Competitions/Details/27)

## 競賽說明

本競賽主題將聚焦於生醫產業領域應用，期盼利用人工智慧技術提升人類的健康福祉。 近年，隨著高壓的生活環境，各式各樣的文明病引起醫學界的注意，其中嗓音疾病常見於職 業上需要大量用聲族群，如老師、業務、講師、零售攤販等，由於聲帶位處於喉部深處，喉 部嗓音疾病檢測相當不易，需專業醫師操作特定儀器方能對病患進行診斷及治療，再加上現 代人工作繁忙，不時有延誤就醫之情形。在近年 COVID-19 盛行期間，張口進行內視鏡檢查恐有飛沫傳播之風險。若能將人工智慧應用於非接觸式，透過嗓音訊號(動態聲音)結合病史紀錄(靜態文字)偵測喉部病徵並分類，有機會早期發現，早期治療，將會是所有嗓音患者之一大福音。競賽歡迎具人工智慧、機器學習、深度學習相關領域之專家或欲學習此領域之高手一同參與競賽，設計與開發模型。

## 1. 資料集說明

本競賽之 Open Data 仍於規劃中，在公開釋出資料集前，若參賽者希望取得 Test Label，可請來信 TBrain 索取。惟，僅限於學術使用，禁止任何形式的商業使用。未來若有任何學術發表，須註明資料來源為：亞東醫院 耳鼻喉科嗓音資料庫。

## 2. 資料前處理

! Remember to unzip the Training Dataset.zip before running any code
於 eda.ipynb 中，我們將資料集進行探索式資料分析(Exploratory Data Analysis)，並將資料集視覺化，以利後續模型訓練以及特徵選取。

## 3. 模型訓練(分類)

- ML:
  Scikit-learn - RandomForestClassifier
  Scikit-learn - LogisticRegression
  Scikit-learn - SVC

- DL:
  Pytorch - FCN

## 4. 模型預測

此準確度為使用部分資料集進行訓練，並使用部分資料集進行預測。

- full data put into training(Accuracy):

  - LogisticRegression: 0.63
  - RandomForestClassifier: 0.65
  - SVC: 0.63
  - FCN: 0.64

- feature data put into training(Accuracy):

  - LogisticRegression: 0.64
  - RandomForestClassifier: 0.64
  - SVC: 0.65
  - FCN: 0.64

- feature data: 由原始資料分離出的特徵資料
  ```
  ['Sex', 'Age', 'Narrow pitch range', 'Decreased volume', 'Fatigue', 'Dryness', 'Lumping', 'heartburn', 'Choking', 'Eye dryness', 'PND', 'Smoking', 'PPD', 'Drinking', 'frequency', 'Noise at work', 'Occupational vocal demand', 'Voice handicap index - 10']
  ```

# Github

https://github.com/LittleFish-Coder/multimodal-pathological-voice-classification-competition
