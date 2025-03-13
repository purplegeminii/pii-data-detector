# PII Detection

## Authors
Victor Quagraine, Hutton Amison-Addy, Delali Nsiah Asare

## Problem Statement
Personally Identifiable Information (PII) includes details that can be used to identify individuals, such as names, addresses, phone numbers, and social security numbers. The goal of this project is to develop a model capable of identifying PII in textual documents.

## Approach
To address this problem, we leveraged Natural Language Processing (NLP) techniques since our dataset consists of text with contextual relationships. We selected a **Bidirectional Long Short-Term Memory (BiLSTM) model** to analyze the context of words within a document, capturing dependencies before and after each token to enhance PII detection accuracy.

## Data Handling
### Data Loading
Our dataset is provided in JSON format, containing:
- Document IDs
- Documents
- Token labels indicating PII presence

### Data Preprocessing
The dataset is divided into:
- **Training and validation sets** for model development
- **A held-out test set** for final evaluation

We implemented a **load unpack function** to extract tokens from documents, forming a structured dataset of tokens and labels. This function returns:
- Row ID
- Document text
- Corresponding PII labels

## Model Development
The **BiLSTM model** was trained on the preprocessed dataset to learn token classifications based on their context. The model architecture includes:
- **Embedding layer** for text representation
- **Bidirectional LSTM layers** for capturing long-range dependencies
- **Dense layers** for classification

## Results and Evaluation
The model was evaluated based on standard NLP classification metrics:
- **Precision**: Measures the proportion of correctly identified PII instances.
- **Recall**: Measures the model's ability to detect actual PII.
- **F1-score**: Balances precision and recall for overall effectiveness.

The evaluation results indicate the effectiveness of the BiLSTM model in detecting PII across various documents.

## Future Work
- **Model Optimization**: Exploring Transformer-based models like BERT for improved performance.
- **Real-time Deployment**: Implementing a web API for real-time PII detection in text.
- **Data Augmentation**: Enhancing the training dataset to improve generalization.

## License
This project is licensed under the MIT License.

## Contact
For further inquiries, reach out to the authors:  
- [Victor Quagraine](https://github.com/quagrain)  
- [Hutton Amison-Addy](https://github.com/Argivist)  
- [Delali Nsiah-Asare](https://github.com/purplegeminii)
