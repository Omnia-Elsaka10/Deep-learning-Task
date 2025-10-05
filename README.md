# 🧠 Deep Learning Model – Adult Income Classification  

## 📌 Project Overview  
This project predicts whether an individual earns more than **$50K per year** based on demographic and employment data using the **Adult Income Dataset**.  
We applied full preprocessing, encoding, normalization, and built a deep learning model to classify income efficiently.  

---

## ⚙️ Project Steps  

### 1️⃣ Data Loading & Cleaning  
- Loaded the **Adult Income dataset** from OpenML.  
- Removed missing or inconsistent values.  
- Handled categorical and numerical features separately.  
- Encoded categorical variables using **One-Hot Encoding**.  
- Normalized numerical features for better model convergence.  

### 2️⃣ Data Splitting  
- Divided the dataset into **70% training**, **15% validation**, and **15% testing** sets for fair evaluation.

### 3️⃣ Model Design  
- Built a **Neural Network** using **TensorFlow/Keras** with the following layers:  
  - Input Layer (based on feature size)  
  - Dense Layer (128 neurons, ReLU activation)  
  - Dense Layer (64 neurons, ReLU activation)  
  - Output Layer (1 neuron, Sigmoid activation) for binary classification  

### 4️⃣ Regularization & Optimization  
- Applied **Dropout (0.3–0.5)** and **L2 regularization** to reduce overfitting.  
- Compared optimizers: **SGD**, **SGD with Momentum**, and **Adam**.  
- Used **EarlyStopping** to stop training when validation loss stopped improving.  

### 5️⃣ Model Evaluation & Visualization  
- Visualized **accuracy** and **loss curves** for training and validation sets.  
- Observed that Dropout improved validation accuracy and model stability.  
- Compared optimizers and batch sizes for performance differences.  

---

## 📊 Key Insights  

| Component | Choice | Reason |
|------------|---------|--------|
| Optimizer | Adam | Fast convergence and adaptive learning rate |
| Batch Size | 32–128 | Balanced stability and generalization |
| Regularization | Dropout (0.3–0.5) + L2 | Reduced overfitting effectively |
| Early Stopping | Enabled (patience=3–5) | Prevents overfitting and saves time |
| Data Split | 70/15/15 | Balanced between training and evaluation |

### Summary of Findings  
- **Dropout** effectively improved generalization and reduced overfitting.  
- **Adam** optimizer showed the fastest and most stable convergence.  
- **Smaller batch sizes (32–64)** generalized better on unseen data.  
- **EarlyStopping** ensured efficient training and better validation performance.  

---

## 🧩 Tools & Libraries  
- **Python 3.10+**  
- **TensorFlow / Keras**  
- **NumPy**  
- **Pandas**  
- **Matplotlib**  
- **Scikit-learn**  

---

## 🏁 Results  
✅ Final model achieved **high validation accuracy** and **stable loss curves**.  
✅ Overfitting reduced significantly after applying **Dropout + EarlyStopping**.  
✅ Adam optimizer provided the **best performance** overall.  



