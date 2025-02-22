# Wine Classification: Predicting Wine Quality

## Project Description

This project aims to classify Portuguese **white wines** as *good* or *bad* based on their chemical properties.\
The dataset used is **Wine Quality Dataset**, which contains physicochemical features of both red and white wines.

## Objective

- Build machine learning models to predict whether a white wine is **good (1)** or **bad (0)**.
- Compare different classification models and choose the best-performing one.
- Test the model on **red wines** to evaluate generalization.

## Dataset

The dataset includes **6497 wine samples** (4898 white and 1599 red).\
Each wine has **12 chemical features** and a **quality score (0-10)**.

**Feature Overview:**

- **Fixed Acidity, Volatile Acidity, Citric Acid**: Acidity levels.
- **Residual Sugar**: Sugar remaining after fermentation.
- **Chlorides**: Salt content.
- **Sulfur Dioxide (Free & Total)**: Preservatives affecting freshness.
- **Density, pH**: Measures of acidity and body.
- **Sulphates**: Contribute to aroma.
- **Alcohol**: Alcohol percentage.

### **Preprocessing Steps**

- **Handled missing values** using median for skewed distributions and mean for normal distributions.
- **Filtered only white wines** for model training.
- **Created a binary label (**\`\`**)**:
  - **Good Wine (1)**: `quality > 5`
  - **Bad Wine (0)**: `quality ≤ 5`
- **Standardized features** with `StandardScaler`.

---

## Models Tested

**Three classifiers**:

1. **Logistic Regression**
2. **Decision Tree**
3. **Support Vector Machine (SVM)**

Each model was evaluated using:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **ROC-AUC Curve**

### **Final Results**

**SVM** achieved the best results and was chosen as the final model.

| Model               | Accuracy | Precision | Recall   | F1-Score |
| ------------------- | -------- | --------- | -------- | -------- |
| Logistic Regression | 0.74     | 0.77      | 0.87     | 0.82     |
| Decision Tree       | 0.78     | 0.84      | 0.82     | 0.83     |
| **SVM**             | **0.78** | **0.82**  | **0.86** | **0.84** |

---

## Testing on Red Wines

To test generalization, we **applied the white wine-trained SVM to red wines**.\
The results were **poor**, proving that red and white wines **require separate models**.

**SVM Model on Red Wines:**

- **Accuracy: 52%**
- **Recall (Good Wines): 13%**
- **F1-Score (Good Wines): 0.23**

🔹 **Conclusion**: White and red wines have different chemical properties, making generalization ineffective.

---

## How to Run the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/gustavofoligno/wine-quality-classification.git
   cd wine-quality-classification
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open and run the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Execute `wine_classification.ipynb` step by step.

---

## 📝 Author & Contact

- Created by **Gustavo Barcelos Foligno**
- Email: gustavofoligno@hotmail.com
- LinkedIn: https://www.linkedin.com/in/gustavofoligno/
- GitHub: https://github.com/gustavofoligno

---

