# PyTorch 深度學習：實作與應用 🧠

機器學習課程作業合集，從線性分類器出發，逐步深入至卷積神經網路與遷移學習，並以醫療影像分類作為期末專題收尾。

---

## 學習路線

```
ADALINE → scikit-learn → MLP → CNN → 資料增強 → Transfer Learning → 醫療影像應用
```

---

## 作業總覽

### HW1 — ADALINE 線性分類器

**技術：** NumPy、梯度下降

- 手刻 ADALINE（Adaptive Linear Neuron）模型，不依賴任何 ML 框架
- 以亂數產生兩群二維資料（常態分布）
- 實作梯度下降法更新權重，並繪製訓練誤差收斂曲線與分類決策邊界

📓 [`HW1_ADALINE/HW1_ADALINE.ipynb`](HW1_ADALINE/HW1_ADALINE.ipynb)

---

### HW2 — scikit-learn 多模型比較

**技術：** scikit-learn、Logistic Regression、SVM、KNN

- 使用 `make_blobs` 產生三群高斯資料
- 比較多種分類器的訓練/測試準確率與決策區域
- 視覺化各模型的決策邊界

📓 [`HW2_scikit_learn/HW2_scikit_learn.ipynb`](HW2_scikit_learn/HW2_scikit_learn.ipynb)

---

### HW3 — CIFAR-10 圖像分類（MLP）

**技術：** TensorFlow / Keras、MLP

- 載入 CIFAR-10（32×32 彩色圖片，10 類，共 60,000 張）
- 將圖像展平為 3072 維向量，輸入 MLP
- 調整層數與神經元數，尋找測試集最佳準確率

📓 [`HW3_cifar10_MLP/HW3_cifar10.ipynb`](HW3_cifar10_MLP/HW3_cifar10.ipynb)

---

### HW4 — EuroSAT 衛星影像分類（MLP vs CNN）

**技術：** TensorFlow Datasets、MLP、CNN

- 使用 EuroSAT RGB 衛星圖像資料集（27,000 張，10 類地表類型）
- 同一資料集分別以 MLP 與 CNN 建模
- 對比兩種架構的準確率與收斂速度，驗證 CNN 在影像任務的優勢

📓 [`HW4_eurosat_MLP_CNN/HW4_eurosat.ipynb`](HW4_eurosat_MLP_CNN/HW4_eurosat.ipynb)

---

### HW5 — Cats vs Dogs（CNN + 資料增強）

**技術：** TensorFlow Datasets、CNN、Data Augmentation

- 使用 TFDS `cats_vs_dogs` 資料集（二元分類）
- 比較三種架構：MLP、CNN、CNN + 資料增強（隨機翻轉、裁剪等）
- 驗證資料增強對模型泛化能力的提升效果

📓 [`HW5_cats_vs_dogs/HW5_cats_vs_dogs.ipynb`](HW5_cats_vs_dogs/HW5_cats_vs_dogs.ipynb)

---

### HW6 — 街景數字辨識（Transfer Learning + Fine-tuning）

**技術：** SVHN 資料集、Transfer Learning、Fine-tuning

- 以交通場景視覺符號辨識為主題，辨識街景門牌數字
- 從 `torchvision.models` 載入預訓練模型進行遷移學習
- 實作 Fine-tuning，觀察凍結層數對收斂速度與準確率的影響

📓 [`HW6_transfer_learning/HW6_transfer_learning.ipynb`](HW6_transfer_learning/HW6_transfer_learning.ipynb)

---

### 期末報告 — 瘧疾細胞影像分類

**技術：** TensorFlow、CNN、MobileNetV2、醫療影像

🔗 **[程式碼（Google Colab）](https://colab.research.google.com/drive/1H_tkPPHeYq-oCneCc8B9Pd_l2xq8Ug7i?usp=sharing)**

- 資料集：TensorFlow Datasets malaria（27,558 張細胞顯微鏡圖像，二元分類）
- 比較三種模型：基礎 CNN、自創優化 CNN、MobileNetV2 遷移學習
- 最佳模型（自創 4 層 CNN + BN + Dropout）達到 **94–96% 準確率**
- 驗證在醫療影像領域，針對性設計的架構優於通用預訓練模型

📓 [`final_malaria/`](final_malaria/)

---

## 技術棧

| 類別 | 工具 |
|------|------|
| 深度學習框架 | TensorFlow / Keras |
| ML 工具 | scikit-learn |
| 數值運算 | NumPy |
| 資料集 | TensorFlow Datasets（TFDS）|
| 視覺化 | Matplotlib |
| 開發環境 | Google Colab、Jupyter Notebook |

---

## 學習成果

- 從零實作 ADALINE，理解梯度下降的核心原理
- 比較 MLP 與 CNN 在影像分類任務的效能差異
- 掌握 Batch Normalization、Dropout 等正規化技術
- 實作 Transfer Learning 與 Fine-tuning，理解預訓練模型的遷移能力
- 將深度學習應用於醫療影像（瘧疾篩檢）實際場景
