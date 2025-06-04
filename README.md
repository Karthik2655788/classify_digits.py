# classify_digits.py

# ✍️ Handwritten Digit Classification with SVM

This project demonstrates the use of a **Support Vector Machine (SVM)** classifier to recognize handwritten digits from the **scikit-learn `digits` dataset**. It involves data preprocessing, model training, evaluation, and visualization of predictions.

## 📁 Project Structure

```
├── digit_classification_svm.py  # Main script
├── README.md                    # Project description
```

## 🧪 Dependencies

Make sure the following Python libraries are installed:

* `numpy`
* `matplotlib`
* `scikit-learn`

Install them via pip:

```bash
pip install numpy matplotlib scikit-learn
```

## 📊 Dataset

The [scikit-learn `digits`](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_digits.html) dataset contains 8x8 pixel grayscale images of handwritten digits (0 to 9). It includes:

* **Images**: 1797 grayscale 8×8 images
* **Targets**: Integer labels (0 to 9)

## ⚙️ Workflow

1. **Data Loading**: Import the digits dataset.
2. **Preprocessing**:

   * Flatten 8x8 images into 64-length vectors.
   * Split into training and test sets (50/50).
   * Standardize features using `StandardScaler`.
3. **Modeling**:

   * Train a Support Vector Classifier (`SVC`) with `gamma=0.001`.
4. **Evaluation**:

   * Print a classification report (precision, recall, f1-score).
5. **Visualization**:

   * Show a few test images with predicted labels using Matplotlib.

## 📈 Sample Output

```text
Classification report:
              precision    recall  f1-score   support

           0       1.00      1.00      1.00        88
           1       0.97      0.97      0.97        91
           ...
           9       0.97      0.93      0.95        92

    accuracy                           0.97       899
   macro avg       0.97      0.97      0.97       899
weighted avg       0.97      0.97      0.97       899
```

### 🖼️ Visualization

The script also displays a few test digit images with their corresponding predicted labels:

![Digit Prediction Sample](#)

## 💡 Notes

* The model uses `SVC` with a very small `gamma` value, which controls the decision boundary complexity.
* Standardizing the data is critical for SVM performance, especially for datasets with pixel values.

## 📌 Enhancements (Optional)

* Try other classifiers like `RandomForestClassifier` or `KNeighborsClassifier`.
* Use Grid Search (`GridSearchCV`) for hyperparameter tuning.
* Add confusion matrix visualization.

