# Fraud_Assignments_IITH

   <p>This repository contains a comprehensive approach to credit card fraud detection using various advanced techniques. The main methods implemented are Variational Autoencoders (VAE), Autoencoders (AE), and Cost-sensitive Logistic Regression using the Bahnsen and Nikou Günnemann method and clustring the data using g Node2Vec, Spectral and GCN Embeddings. Additionally, we explore synthetic data generation using VAE to enhance our model's performance.</p>

   <h2>Table of Contents</h2>
    <ul>
        <li><a href="#introduction">Introduction</a></li>
        <li><a href="#dataset">Dataset</a></li>
        <li><a href="#methods">Methods</a>
            <ul>
                <li><a href="#variational-autoencoders-vae">Variational Autoencoders (VAE)</a></li>
                <li><a href="#autoencoders-ae">Autoencoders (AE)</a></li>
                <li><a href="#cost-sensitive-logistic-regression">Cost-sensitive Logistic Regression</a></li>
                <li><a href="#synthetic-data-generation">Synthetic Data Generation</a></li>
               <li><a href="#node2vec">Node 2 Vector</a></li>
               <li><a href="#spectral">Spectral Clustering </a></li>
               <li><a href="#gcn">Graph Convolution Networks Clustering</a></li>
            </ul>
        </li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#usage">Usage</a></li>
        <li><a href="#results">Results</a></li>
        <li><a href="#conclusion">Conclusion</a></li>
        <li><a href="#references">References</a></li>
        <li><a href="#acknowledgements">Acknowledgements</a></li>
    </ul>

   <h2 id="introduction">Introduction</h2>
    <p>Credit card fraud detection is a critical issue in the financial sector. This project aims to detect fraudulent transactions by leveraging machine learning and deep learning techniques. By using a combination of Variational Autoencoders, Autoencoders, and Cost-sensitive Logistic Regression, we strive to achieve high accuracy and robustness in identifying fraudulent activities.</p>

   <h2 id="dataset">Dataset</h2>
    <p>The dataset used in this project is a credit card transaction dataset that includes both legitimate and fraudulent transactions. The dataset used are </p>
    <ul>
       <li>https://drive.google.com/drive/folders/1fv6AZqbr9bsBUbMxCO8bN_kFpQed-SBE?usp=drive_link</li>
    </ul>

   <h2 id="methods">Methods</h2>
    <h3 id="variational-autoencoders-vae">Variational Autoencoders (VAE)</h3>
    <p>VAEs are used to learn the distribution of legitimate transactions. By reconstructing transactions, we can identify anomalies (fraudulent transactions) that deviate significantly from the learned distribution.</p>

   <h3 id="autoencoders-ae">Autoencoders (AE)</h3>
    <p>AEs are trained to reconstruct the input data. Fraudulent transactions, which are rare and deviate from normal patterns, are expected to have higher reconstruction errors compared to legitimate transactions.</p>

   <h3 id="cost-sensitive-logistic-regression">Cost-sensitive Logistic Regression</h3>
    <p>This method involves modifying the logistic regression model to account for the cost associated with different types of misclassification. The Bhasen and Nikoee Guenman method is used to assign higher penalties to false negatives, ensuring better detection of fraudulent transactions.</p>

   <h3 id="synthetic-data-generation">Synthetic Data Generation</h3>
    <p>To address the class imbalance, we use VAE to generate synthetic data that mimics the characteristics of legitimate transactions. This synthetic data is used to augment the training set, helping to improve the model's performance on imbalanced datasets.</p>

   <h2 id="installation">Installation</h2>
    <p>To run the project, follow these steps:</p>
    <ol>
        <li>Clone this repository:
            <pre><code>git clone https://github.com/yourusername/credit-card-fraud-detection.git
cd credit-card-fraud-detection</code></pre>
        </li>
        <li>Install the required dependencies:
            <pre><code>pip install -r requirements.txt</code></pre>
        </li>
    </ol>

   <h2 id="usage">Usage</h2>
    <ol>
        <li>Preprocess the dataset:
            <pre><code>python preprocess.py</code></pre>
        </li>
        <li>Train the models:
            <pre><code>python train_vae.py
python train_ae.py
python train_cost_sensitive_lr.py</code></pre>
        </li>
        <li>Generate synthetic data:
            <pre><code>python generate_synthetic_data.py</code></pre>
        </li>
        <li>Evaluate the models:
            <pre><code>python evaluate_models.py</code></pre>
        </li>
    </ol>

   <h2 id="results">Results</h2>
    <p>The results of our experiments are documented in the <code>results</code> directory. We provide detailed performance metrics, including precision, recall, F1-score, and ROC-AUC for each method.</p>

   <h2 id="conclusion">Conclusion</h2>
    <p>This project demonstrates the effectiveness of combining Variational Autoencoders, Autoencoders, and Cost-sensitive Logistic Regression for credit card fraud detection. The use of synthetic data generation further enhances the model's ability to handle imbalanced datasets, leading to improved detection of fraudulent transactions.</p>

   <h2 id="references">References</h2>
    <ul>
        <li>Kingma, D. P., & Welling, M. (2013). Auto-Encoding Variational Bayes. arXiv preprint arXiv:1312.6114.</li>
        <li>Bhasen, B., & Nikoee Guenman, N. (Year). Title of the paper on cost-sensitive logistic regression. Journal Name, Volume(Issue), Page numbers.</li>
    </ul>

   <h2 id="acknowledgements">Acknowledgements</h2>
    <p>We would like to thank the contributors of the credit card dataset and the authors of the referenced papers for their valuable work, which has significantly contributed to this project.</p>

   <p>Feel free to open an issue or submit a pull request if you have any questions or suggestions for improvement.</p>
</body>
</html>
