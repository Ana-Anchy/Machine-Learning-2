# Machine-Learning-2
Kunskapskontroll 2
# ⚙️ Machine Learning Project – MNIST Handwritten Digit Recognition

## 🔎 Overview
This project demonstrates a complete machine learning workflow for classifying handwritten digits using the MNIST dataset. We compare three different models—**Random Forest**, **Extra Trees**, and **Support Vector Machine (SVM)**—to determine which approach balances accuracy and computational efficiency most effectively. Additionally, a **Streamlit** application is provided for real-time digit prediction using JPG images.

---

## 🏗️ Project Workflow

1. **🔬 Exploratory Data Analysis (EDA)**
   - Loaded the MNIST dataset from `fetch_openml('mnist_784')`.
   - Checked dataset size and distribution of digit classes.
   - Visualized a few samples to confirm data integrity.

2. **🧹 Data Preprocessing**
   - Split the dataset into training (50k), validation (10k), and test (10k) sets.
   - Applied `StandardScaler` to normalize features, improving model performance and training stability.

3. **🤖 Model Training**
   - **Random Forest**: Built an ensemble of decision trees on random subsets of data and features.
   - **Extra Trees**: Similar to Random Forest but introduces additional randomness in choosing split points.
   - **SVM**: Used an RBF kernel for nonlinear separation, which can yield high accuracy but may increase training time.
   - **Linear Support Vector Classifier**

4. **📊 Model Evaluation**
   - Trained each model on the training set, then compared performance on the validation set.
   - Used **accuracy** as the primary metric, along with classification reports and confusion matrices for deeper insights.
   - Selected the best-performing model and evaluated it on the test set to estimate real-world performance.

5. **🚀 Deployment (Optional)**
   - Created a Streamlit application to allow users to upload JPG images of handwritten digits.
   - The app provides on-the-fly predictions using the trained model.

---

## 📂 Data
- **Source**: [MNIST Dataset](http://yann.lecun.com/exdb/mnist/), loaded via `fetch_openml('mnist_784')`.
- **Format**: Each image is 28×28 pixels, flattened into a 784-dimensional feature vector.
- **Size**: 70,000 images (digits 0–9).

---

## 🤔 Models

### 🌳 Random Forest
- Ensemble method constructing multiple decision trees.
- Final prediction made by majority voting among the trees.
- Often balances accuracy and speed well.

### 🌱 Extra Trees
- Variant of Random Forest with more randomness in splitting nodes.
- Potentially faster training and lower variance.

### 🏆 SVM
- Attempts to find the optimal hyperplane separating classes with maximum margin.
- RBF kernel provides flexibility for complex boundaries but can be more computationally intensive.

### Linear SVC

