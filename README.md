# 2024_ia651_Berhe_Nyamuchengwa
## Patient Drug Info Chatbot with Insights from Real Patients Reviews
### Project Overview
The main aim of our project is to create an intuitive chatbot that provides users with quick, reliable insights on various medications, drawing from real patient reviews. By using  natural language processing (NLP) techniques, the chatbot will assist users in exploring information about a drug’s effectiveness, common side effects, and overall satisfaction ratings based on feedback from other patients. This user-friendly tool supports informed decision-making, enhancing patient confidence in managing their health.

#### Objective:
Our main Objective is to Develop a chatbot to answer user questions about medications, providing easy-to-understand insights from patient experiences. It will address drug effectiveness, side effects, satisfaction ratings, and alternative options, offering users authentic, data-driven guidance.

#### Feature of the chatbot
Question Recognition: Responds to basic questions on drug effectiveness and side effects, such as “What are the side effects of [drug-name]?”
Sentiment Summary: Provides a simple positive or negative summary of patient reviews for each drug.
Drug Ratings: Shares an average rating for each drug for a quick perception overview.
Highlighted Reviews: Displays top-rated patient reviews for deeper insights.
Simple Text Interface: Allows users to ask questions and receive clear, concise responses based on available data.
 

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

### steps to Achieve this:
<img width="557" alt="Screenshot 2024-11-14 215248" src="https://github.com/user-attachments/assets/17fdbbfc-c597-4a6b-a946-bed974e314d8">


## Section 1:Data Collection and Preprocessing
The dataset had no missing or duplicate values making it godd data whic satisfy some requirements of quality and good data.

## Step 2 :Exploratory Data Analysis
<img width="466" alt="review length" src="https://github.com/user-attachments/assets/852e96b5-27ba-435d-b4f5-a67d433dcf3a">


 The distribution is heavily skewed to the left, with the vast majority of reviews having relatively short lengths. Most of the reviews fall within a small range of lengths 
 on the lower end.The majority of reviews have lengths below 2,000, as shown by the high concentration of bars in that range.There are a few reviews with significantly higher lengths (extending up to 10,000 or more), though these are relatively rare. These could indicates that a significant portion of the reviews are quite short, with many of them likely being brief comments or minimal feedback.

<img width="267" alt="drug distr" src="https://github.com/user-attachments/assets/fe6d83d8-e754-4030-a5a9-211d39be8f04">

 
 The distribution suggests that users tend to give extreme ratings, either very high or very low, with a notable lack of neutral or middle ratings. This could reflect polarized user experiences with the drugs



              

                                     




