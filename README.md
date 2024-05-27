# Case Study: Automatic Ticket Classification

#### Problem Statement
A financial company seeks to enhance its customer support by automating the classification of customer complaints. These complaints, which are unstructured text data, traditionally require manual evaluation and assignment to the appropriate department. As the company grows, this manual process becomes increasingly burdensome and inefficient. The goal is to develop a model that can automatically classify these complaints based on the products and services mentioned in the tickets, thereby improving resolution times and customer satisfaction.

#### Business Goal
The objective is to create a model capable of classifying customer complaints into specific categories:
- Credit card / Prepaid card
- Bank account services
- Theft/Dispute reporting
- Mortgages/loans
- Others

This classification will help in quickly routing tickets to the appropriate departments, leading to faster issue resolution and continuous improvement in services.

#### Approach
The approach involves using Non-Negative Matrix Factorization (NMF) for topic modeling to detect patterns and recurring words in the tickets. This will help in identifying key features for each cluster, enabling the mapping of tickets to their respective categories. Subsequently, this categorized data will be used to train a supervised machine learning model for the automatic classification of new tickets.

### Expected Tasks
To complete the assignment, you need to perform the following eight major tasks:

1. **Data Loading**
   - Load the customer complaints data from the provided .json file.
   - Inspect the structure and contents of the data to understand its format and fields.

2. **Text Preprocessing**
   - Clean and preprocess the text data to make it suitable for analysis. Steps include:
     - Converting text to lowercase.
     - Removing punctuation, numbers, and special characters.
     - Removing stopwords.
     - Performing stemming or lemmatization to reduce words to their root forms.

3. **Exploratory Data Analysis (EDA)**
   - Analyze the data to understand the distribution and characteristics of the complaints.
   - Visualize the most common words and phrases using techniques such as word clouds and frequency distributions.
   - Explore relationships between different words and potential clusters.

4. **Feature Extraction**
   - Convert the preprocessed text into numerical features suitable for modeling. Techniques include:
     - TF-IDF (Term Frequency-Inverse Document Frequency)
     - Bag-of-Words
     - Word embeddings (optional, for more advanced models)

5. **Topic Modelling**
   - Apply Non-Negative Matrix Factorization (NMF) to the text data to identify patterns and recurring words.
   - Determine the top words for each topic to understand the themes of customer complaints.
   - Map each complaint to a topic/category based on the NMF results.

6. **Model Building Using Supervised Learning**
   - Use the labeled data (from the NMF topic modeling) to train a supervised machine learning model.
   - Possible models include:
     - Logistic Regression
     - Decision Tree
     - Random Forest
     - Support Vector Machines (SVM)
     - Neural Networks (optional, for advanced performance)

7. **Model Training and Evaluation**
   - Split the data into training and test sets.
   - Train the selected model(s) on the training data.
   - Evaluate the model's performance using metrics such as accuracy, precision, recall, and F1-score.
   - Fine-tune the model parameters to improve performance.

8. **Model Inference**
   - Use the trained model to classify new customer complaints.
   - Validate the model's predictions and ensure they align with business needs.
   - Deploy the model in a production environment for real-time classification.

### Expected Outcome
By implementing this approach, the company can efficiently classify customer complaints into predefined categories, significantly reducing manual effort and improving response times. The use of NMF for topic modeling helps in understanding the core issues in the complaints, aiding in better service improvement strategies. The trained supervised model will automate the classification of new tickets, ensuring a scalable and efficient solution for handling customer complaints.
