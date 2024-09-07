# British Museum Tweet Sentiment Analysis

## Introduction
This project aims to analyze the sentiment of tweets related to the British Museum, using a fine-tuned BERT model for multi-class sentiment classification. The analysis categorizes tweets into different sentiment classes such as happy, sad, angry, disgust, surprise, and not-relevant, with the goal of understanding public perception of the museum on social media.

## Objective
To classify tweets into sentiment categories to provide insights into public opinion and identify areas of concern or satisfaction.

## Dataset
The dataset consists of tweets mentioning the British Museum, labeled with the following sentiment categories:
- **happy**
- **sad**
- **angry**
- **disgust**
- **surprise**
- **not-relevant**

Each tweet is pre-processed and then classified into one of these categories using a BERT-based model.

## Approach
### 1. **Data Preprocessing**
   - Tokenization using **BERT Tokenizer** to transform raw text into a format that BERT can process.
   - Labels are encoded using **LabelEncoder** for multi-class classification.

### 2. **Modeling**
   - We used **BERT (Bidirectional Encoder Representations from Transformers)** for sequence classification. Specifically, we fine-tuned a BERT model to classify the sentiment of each tweet.
   - Data was split into training and test sets using **train_test_split** from scikit-learn.

### 3. **Training and Optimization**
   - We trained the BERT model using **AdamW** optimizer and a linear learning rate schedule provided by **get_linear_schedule_with_warmup**.
   - The training data was loaded into **TensorDatasets** and batched using PyTorch's **DataLoader**.

### 4. **Evaluation**
   - The model's performance was evaluated using **accuracy** and **F1 score** on the test set.
   - Each class was evaluated individually to highlight model performance across different sentiment categories.

## Results
The model's performance was evaluated across each sentiment class, with the following accuracies:

- **Class: happy**  
  Accuracy: 168/171  
- **Class: not-relevant**  
  Accuracy: 1/32  
- **Class: angry**  
  Accuracy: 0/9  
- **Class: disgust**  
  Accuracy: 0/1  
- **Class: sad**  
  Accuracy: 0/5  
- **Class: surprise**  
  Accuracy: 0/5  

These results indicate that the model performed well for certain classes (e.g., happy), but struggled with others (e.g., angry, sad, surprise). Further tuning and data balancing may improve performance for the underrepresented classes.

## Conclusion
The fine-tuned BERT model was successful in predicting sentiment for the majority class (happy) but had difficulty in classifying other sentiments, particularly those with fewer training samples. This indicates the need for better data balancing or alternative modeling techniques for minority classes.

## Technologies Used
- **Python Libraries**: Pandas, NumPy, PyTorch, Transformers, scikit-learn
- **Pre-trained Model**: BERT (Bidirectional Encoder Representations from Transformers)
- **Optimization**: AdamW optimizer, learning rate scheduler

## Future Work
- **Data Augmentation**: Increase the size of underrepresented sentiment classes to improve model performance.
- **Model Tuning**: Experiment with other transformer models and hyperparameters for better classification accuracy.
