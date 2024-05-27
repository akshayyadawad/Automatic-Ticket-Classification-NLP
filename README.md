# Case Study: Automatic Ticket Classification

### Problem Statement

A financial company seeks to enhance its customer support by automating the classification of customer complaints. These complaints, which are unstructured text data, traditionally require manual evaluation and assignment to the appropriate department. As the company grows, this manual process becomes increasingly burdensome and inefficient. The goal is to develop a model that can automatically classify these complaints based on the products and services mentioned in the tickets, thereby improving resolution times and customer satisfaction.

### Business Goal

The objective is to create a model capable of classifying customer complaints into specific categories:
1. Credit card / Prepaid card
2. Bank account services
3. Theft/Dispute reporting
4. Mortgages/loans
5. Others

This classification will help in quickly routing tickets to the appropriate departments, leading to faster issue resolution and continuous improvement in services.

### Approach

The approach involves using Non-Negative Matrix Factorization (NMF) for topic modeling to detect patterns and recurring words in the tickets. This will help in identifying key features for each cluster, enabling the mapping of tickets to their respective categories. Subsequently, this categorized data will be used to train a supervised machine learning model for the automatic classification of new tickets.

### Steps to Implement

1. **Data Preprocessing**: 
   - Load the .json data containing customer complaints.
   - Clean and preprocess the text data (e.g., removing stop words, punctuation, and performing lemmatization).

2. **Topic Modeling with NMF**:
   - Apply NMF to identify topics within the tickets.
   - Analyze the words associated with each topic to map topics to the predefined categories.

3. **Labeling Data**:
   - Use the results from the NMF to label the tickets with their respective categories.
   
4. **Feature Extraction**:
   - Convert the text data into numerical features using techniques such as TF-IDF (Term Frequency-Inverse Document Frequency).

5. **Model Training**:
   - Split the labeled data into training and testing sets.
   - Train a supervised learning model (e.g., logistic regression, decision tree, random forest) on the training data.
   - Evaluate the model's performance on the testing data.

6. **Model Evaluation**:
   - Assess the model using metrics such as accuracy, precision, recall, and F1-score.
   - Fine-tune the model parameters to improve performance if necessary.

7. **Deployment**:
   - Deploy the trained model to automatically classify new incoming customer complaints.

### Expected Outcome

By implementing this approach, the company can efficiently classify customer complaints into predefined categories, significantly reducing manual effort and improving response times. The use of NMF for topic modeling helps in understanding the core issues in the complaints, aiding in better service improvement strategies. The trained supervised model will automate the classification of new tickets, ensuring a scalable and efficient solution for handling customer complaints.
