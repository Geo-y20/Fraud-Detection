<!DOCTYPE html>
<html>
<head>
</head>
<body>
    <h1>Fraud Detection Model</h1>

<h2> Overview</h2>
    <p>This project focuses on the development of a sophisticated fraud detection model for credit card transactions. Detecting fraudulent transactions is of paramount importance for credit card companies to safeguard their customers from unauthorized charges. The dataset used in this project contains credit card transactions made by European cardholders in September 2013.</p>

<h2>Dataset</h2>
    <p>The dataset can be found <a href="https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?datasetId=310">here</a>.</p>

<h2>Data License</h2>
    <p>The dataset is available under the MIT License, granting you the freedom to use, modify, and distribute the data for various purposes. For specific licensing details, please refer to the <a href="https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?datasetId=310">dataset source</a>.</p>

<h2>Data Preprocessing</h2>
    <p>Before building the model, extensive data preprocessing was performed, including:</p>
    <ul>
        <li>Data normalization</li>
        <li>Handling missing values (none in this dataset)</li>
        <li>Feature engineering</li>
        <li>Class imbalance mitigation (undersampling)</li>
    </ul>

<h2>Model Building</h2>
    <p>We employed a Logistic Regression model for its simplicity and interpretability. The model was trained on the preprocessed data to predict fraudulent transactions.</p>

<h2>Model Evaluation</h2>
    <p>The model's performance was evaluated using various metrics, including the classification report and confusion matrix:</p>
    
<h3>Classification Report:</h3>
    <pre>
        precision        recall          f1-score   support

0       0.89      0.98          0.93        88
1       0.98      0.89          0.93       102

accuracy                        0.93       190
   macro avg       0.93      0.93      0.93       190
weighted avg       0.94      0.93      0.93       190
    </pre>

<h3>Confusion Matrix:</h3>
    <pre>
     [[86  2]
     [11 91]]
    </pre>

<p>Recall score is 0.892, precision score is 0.978, and the F1 score is 0.933, indicating strong model performance in detecting fraudulent transactions.</p>

<h2>Model Prediction</h2>
    <p>With the trained model, you can make real-time predictions to identify potentially fraudulent transactions. Simply provide the transaction details, and the model will classify them as "Actual" or "Fraud."</p>

<p>For example:</p>
    <pre>
    input_data = np.array([1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1])
    FraudDetection = input_data.reshape(1, -1)
    pred = log.predict(FraudDetection)
    if pred == 0:
        print('Actual')
    else:
        print('Fraud')
    </pre>

<p>The model predicts whether a transaction is "Actual" or "Fraud" based on the provided input data.</p>

<h2>Conclusion</h2>
    <p>This project demonstrates the development of an effective fraud detection model using machine learning techniques. The model showcases strong performance in identifying fraudulent credit card transactions, thereby enhancing security and trust in financial transactions.</p>

<p>Feel free to explore the code and dataset provided to gain a deeper understanding of the project. For any questions or feedback, please reach out. Thank you for visiting this repository!</p>
</body>
</html>
