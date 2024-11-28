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


<img width="309" alt="NEGATIVE FFEDBACK" src="https://github.com/user-attachments/assets/2ae34fb7-a1f7-4a30-951d-776b77e27cdc">

The word cloud highlights the most frequent words in negative reviews. Words like "pain," "worst," "horrible," and "bad" dominate, indicating common negative experiences, including dissatisfaction with effectiveness or severe side effects.



<img width="314" alt="POSITIVE FEEDBAK" src="https://github.com/user-attachments/assets/a6cb6d10-5518-4c31-9474-406f6ea63cb3">

The word cloud for positive reviews shows words like "great," "best," "love," and "happy," suggesting high satisfaction and positive outcomes, such as improved health, happiness, or effectiveness of the medication.



<img width="466" alt="review length" src="https://github.com/user-attachments/assets/852e96b5-27ba-435d-b4f5-a67d433dcf3a">


 The distribution is heavily skewed to the left, with the vast majority of reviews having relatively short lengths. Most of the reviews fall within a small range of lengths 
 on the lower end.The majority of reviews have lengths below 2,000, as shown by the high concentration of bars in that range.There are a few reviews with significantly higher lengths (extending up to 10,000 or more), though these are relatively rare. These could indicates that a significant portion of the reviews are quite short, with many of them likely being brief comments or minimal feedback.

<img width="267" alt="drug distr" src="https://github.com/user-attachments/assets/fe6d83d8-e754-4030-a5a9-211d39be8f04">

 
 The distribution suggests that users tend to give extreme ratings, either very high or very low, with a notable lack of neutral or middle ratings. This could reflect polarized user experiences with the drugs


<img width="574" alt="most conditions" src="https://github.com/user-attachments/assets/2ee1f48c-d370-4948-9592-eedeb441a607">

This bar chart shows the ten most frequently mentioned conditions. Depression, Pain, and Anxiety are the top conditions, reflecting prevalent health concerns 

<img width="659" alt="mostcommon drug" src="https://github.com/user-attachments/assets/34169554-f5c2-4fdc-a328-54080cedb2e4">

This horizontal bar chart identifies the ten most frequently reviewed drugs. Drugs like Levonorgestrel and Escitalopram have the highest counts, suggesting their popularity or wide usage ,likely reflecting their effectiveness or widespread prescription.



<img width="443" alt="top 5 top 3 drugs adminsitered" src="https://github.com/user-attachments/assets/3578b428-2a27-4b40-81b9-27b7f5e9c8f0">

This grouped bar chart links the top five conditions to the top 10 drugs administered for those conditions. It highlights which drugs are commonly used for specific health issues like Depression and Anxiety.Relationship between conditions and drugs reveals patterns in pharmaceutical treatment, with some drugs serving multiple conditions effectively.

<img width="480" alt="year ratings dugs" src="https://github.com/user-attachments/assets/cc598486-998b-4c52-8316-91c61e1c3773">

This line chart tracks the average ratings for the top five drugs over a period of time. The trends vary, with some drugs experiencing a decline or fluctuation in their average ratings, indicating changing user satisfaction or evolving efficacy perceptions.The fluctuating average ratings for drugs over time suggest changing user experiences, possibly due to shifts in drug formulations, side effects, or treatment expectations.


<img width="465" alt="USEFULL COUNT" src="https://github.com/user-attachments/assets/e07b4b8e-e6be-48fe-9b63-1315494d503a">

This box plot illustrates how many users found the reviews helpful (useful count). Most reviews have a low useful count, with a few outliers receiving significantly higher counts, indicating that some reviews are particularly valuable to readers.


#### SUMMARY

This EDA provides a clear picture of how patients interact with medications and their experiences over time. Depression, anxiety, and pain emerge as the most common health challenges, reflecting key areas of focus for healthcare providers. Many drugs receive high ratings, suggesting overall satisfaction, but fluctuations in ratings over time highlight the importance of monitoring long-term effectiveness and patient perceptions.

A small group of medications dominates in usage and reviews, often addressing multiple conditions. This points to their widespread reliability but also emphasizes the need for personalized treatment options. The link between conditions and the drugs used for treatment offers valuable insights into current healthcare practices.

Overall, these findings show the value of listening to patient experiences to improve drug development, refine treatment strategies, and better meet the needs of those seeking care.








 



 


 


 



 




              

                                     




