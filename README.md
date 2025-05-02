
> Make sure the folder is unzipped and placed in `/content/dataset` when running in Google Colab.

---

## 🚀 Model Workflow

### 1. **Preprocessing**
- download dataset from https://www.kaggle.com/datasets/mikulhe/3d-printing-errors
- Images are resized to 128x128
- Normalized with `rescale=1./255`
- Dataset is split: 80% training, 20% validation using `ImageDataGenerator`

### 2. **Model Architecture**
- 3 Convolutional + MaxPooling layers
- 1 Dense hidden layer
- 1 Output layer (Sigmoid activation for binary classification)

### 3. **Training**
- Binary cross-entropy loss
- Adam optimizer
- 10 epochs

### 4. **Evaluation**
- Confusion matrix
- Classification report (precision, recall, F1-score)
- Accuracy/loss training graphs

---

## 🧪 How to Use

1. Upload the dataset to Colab as `dataset.zip`
2. Unzip the folder and confirm the structure
3. Run the script to:
   - Train the model
   - Evaluate performance
   - Visualize accuracy and loss

---

## 📊 Output

- **Classification Report**: shows how well the model distinguishes good vs. bad prints
- **Confusion Matrix**: to analyze misclassifications
- **Accuracy/Loss Graphs**: for visual training feedback

---

## 📦 Requirements

Install in local environment if needed:

```bash
pip install tensorflow numpy matplotlib scikit-learn
