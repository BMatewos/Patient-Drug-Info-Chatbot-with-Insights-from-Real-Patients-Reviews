# 2024_ia651_Berhe_Nyamuchengwa
## Patient Drug Info Chatbot with Insights from Real Patients Reviews
### Project Overview
#### Dataset Link:https://archive.ics.uci.edu/dataset/462/drug+review+dataset+drugs+com
### Dataset Description
The dataset has 7 columns and 161297 rows
<img width="592" alt="dataset brief" src="https://github.com/user-attachments/assets/d37dec41-ca2d-44c3-b751-1b116aaf57db">


| Column       | Description            | Data Type   |
|--------------|------------------------|-------------|
| ID            | A unique identifier for each entry in the dataset                    | Integer     |
| drugName     | The name of the drug being reviewed     | Categorical |
| condition    | The medical condition for which the drug was used     | Categorical |
| review       | The textual review or feedback provided by the patient about the drug.      | Categorical |
| rating       | The rating given by the patient for the drug, likely on a specific scale (e.g., 1-5 or 1-10).          | Categorical |
| date         | The date when the review was submitted.          | Date        |
| usefulCount  | The count of how many users found the review useful  | Categorical |



#### Objective:
Create a chatbot that provides drug-related information and insights based on real patient reviews, using Natural Language Processing (NLP).
#### Feature of the chatbot
Personalized Drug Recommendations: Based on user inputs like symptoms, concerns, or preferences, the chatbot can suggest drugs or present reviews that match the user’s specific needs, helping them make more informed decisions.

### Steps :
Clean the reviews by removing unnecessary characters (e.g., punctuation, HTML tags).
Tokenize the text, remove stopwords, and normalize the text (e.g., lowercasing, stemming, or lemmatization).
Label the data for training (e.g., effectiveness, side effects, dosage)
