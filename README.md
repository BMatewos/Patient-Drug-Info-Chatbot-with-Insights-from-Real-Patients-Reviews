# 2024_ia651_Berhe_Nyamuchengwa
## Patient Drug Info Chatbot with Insights from Real Patients Reviews
### Project Overview
The main aim of our project is to create an intuitive chatbot that provides users with quick, reliable insights on various medications, drawing from real patient reviews. By using  natural language processing (NLP) techniques, the chatbot will assist users in exploring information about a drug’s effectiveness, common side effects, and overall satisfaction ratings based on feedback from other patients. This user-friendly tool supports informed decision-making, enhancing patient confidence in managing their health.

#### Objective:
Create a chatbot that provides drug-related information and insights based on real patient reviews, using Natural Language Processing (NLP).

#### Dataset Link:https://archive.ics.uci.edu/dataset/462/drug+review+dataset+drugs+com
### Dataset Description
The dataset has 7 columns and 161297 rows

 <img width="653" alt="dataset" src="https://github.com/user-attachments/assets/72658d14-1db7-45b6-b3a3-5a159b5dc7d2">





| Column       | Description            | Data Type   |
|--------------|------------------------|-------------|
| ID            | A unique identifier for each entry in the dataset                    | Integer     |
| drugName     | The name of the drug being reviewed     | Categorical |
| condition    | The medical condition for which the drug was used     | Categorical |
| review       | The textual review or feedback provided by the patient about the drug.      | Categorical |
| rating       | The rating given by the patient for the drug, likely on a specific scale (e.g., 1-5 or 1-10).          | Categorical |
| date         | The date when the review was submitted.          | Date        |
| usefulCount  | The count of how many users found the review useful  | Categorical |




#### Feature of the chatbot
Personalized Drug Recommendations: Based on user inputs like symptoms, concerns, or preferences, the chatbot can suggest drugs or present reviews that match the user’s specific needs, helping them make more informed decisions.

### Steps :
Clean the reviews by removing unnecessary characters (e.g., punctuation, HTML tags).
Tokenize the text, remove stopwords, and normalize the text (e.g., lowercasing, stemming, or lemmatization).
Label the data for training (e.g., effectiveness, side effects, dosage)
