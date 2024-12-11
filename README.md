# Persian-NER-Models  

This repository contains multiple **Named Entity Recognition (NER)** models for Persian text, built and trained using a rich dataset of formal Persian sentences. The models leverage advanced techniques like **BiLSTM**, **CNN**, and **Transformers** for entity recognition, utilizing **GloVe 300D embeddings** and optimized loss functions for high performance.

---

### Models  
1. **BiLSTM Base**  
   - Loss Function: `sparse_categorical_crossentropy`  
   - A baseline model using a simple BiLSTM architecture.

2. **BiLSTM + CNN (Best Result)**  
   - Loss Function: `focal_loss`  
   - Embeddings: **GloVe 300D**  
   - Combines BiLSTM and CNN layers for improved feature extraction and performance.

3. **BiLSTM + CNN + Transformer**  
   - Loss Function: `focal_loss`  
   - Embeddings: **GloVe 300D**  
   - Enhances the BiLSTM and CNN architecture with a Transformer layer for advanced sequence modeling.

---

### Dataset  
The dataset contains over **18,600 labeled formal Persian sentences**, combining data from **Arman**, **Peyma**, and web-scraped sources. The data has undergone preprocessing steps including:  
- Sentence segmentation.  
- Word tokenization.  
- Additional cleaning and preparation necessary for NER tasks.  

Each token in the dataset is labeled as:  
- `1`: Token is a name.  
- `0`: Token is not a name.  

---

### Workflow  
1. **Load and Preprocess Dataset**  
   - Notebooks handle loading the dataset and applying all necessary preprocessing steps.

2. **Build Model Architectures**  
   - Models are constructed based on the selected architecture (e.g., BiLSTM, CNN, Transformer).  

3. **Train Models**  
   - The preprocessed dataset is used to train each model.  
   - Training incorporates GloVe embeddings and optimized loss functions.  

4. **Make Predictions**  
   - Models predict token labels (`1` for names, `0` otherwise) on input sentences.

---

### Evaluation Metrics  
The models are evaluated using the following metrics:  
- **Precision**: Measures the proportion of true positive predictions out of all positive predictions.  
- **Recall**: Measures the proportion of true positives out of all actual positive labels.  
- **F1-Score**: The harmonic mean of precision and recall, balancing the two.  
- **Sentence-Level Accuracy**: A custom metric that calculates the percentage of sentences from the dataset that are predicted entirely correctly.  

---

### Features  
- Multiple NER model architectures for comparison and flexibility.  
- Pretrained **GloVe 300D embeddings** for semantic understanding.  
- Use of `focal_loss` for improved handling of imbalanced data.  
- Comprehensive preprocessing pipeline included in the notebooks.  

---

### Requirements  
- **Python 3.12** or higher  
- Libraries:  
  - `numpy`  
  - `tensorflow`  

---

### Resources  
- **Dataset**: [Download here](https://www.dropbox.com/scl/fi/ln64xjqlwd4665u9sp2bq/Full_Dataset.rar?rlkey=g5aa4zefy2xpj98n3x8ihjcp2&st=bg907w5p&dl=0)  
- **GloVe 300D Embeddings**: [Download here](https://raw.githubusercontent.com/HaniehP/PersianNER/refs/heads/master/glove300d.txt.zip)  

---

**All rights reserved to Mostafa Modaberi.**
