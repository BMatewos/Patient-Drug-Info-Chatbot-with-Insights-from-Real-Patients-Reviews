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

 *Table 1:dataset*








| Column       | Description            | Data Type   |
|--------------|------------------------|-------------|
| ID            | A unique identifier for each entry in the dataset                    | Integer     |
| drugName     | The name of the drug being reviewed     | Categorical |
| condition    | The medical condition for which the drug was used     | Categorical |
| review       | The textual review or feedback provided by the patient about the drug.      | Categorical |
| rating       | The rating given by the patient for the drug, likely on a specific scale (e.g., 1-5 or 1-10).          | Categorical |
| date         | The date when the review was submitted.          | Date        |
| usefulCount  | The count of how many users found the review useful  | Categorical |

*Table 2:data description*

### steps to Achieve this:

<img width="559" alt="FIGURE 00" src="https://github.com/user-attachments/assets/af786207-5045-40ab-8abe-3fbae93bf464">


*Figure 00 :Steps Taken*


## Section 1:Data Collection and Preprocessing
The data collection and preprocessing involved loading the drugs.csv file directly into a pandas DataFrame . Following the import, unnecessary columns were removed, and rows with missing values in critical fields were eliminated. The date column was converted to a datetime format, and duplicate entries were removed. A preprocessing function was then applied to clean the text data by converting it to lowercase, removing special characters and numbers, handling negation phrases, and lemmatizing words while filtering out stopwords. New columns for cleaned reviews, review length, and word count were added, followed by the removal of rows with very short reviews for example 1 or 2 words which did no means anything, thus preparing the dataset for further analysis.

## Step 2 :Exploratory Data Analysis



<img width="405" alt="negative reviews" src="https://github.com/user-attachments/assets/058e2e41-92f2-435f-8220-f1e2ee3451f7">



*Figure 1: Negative Word Cloud*

The word cloud highlights the most frequent words in negative reviews. Words like "pain," "worst," "horrible," and "bad" dominate, indicating common negative experiences, including dissatisfaction with effectiveness or severe side effects.



<img width="383" alt="positive word reviews" src="https://github.com/user-attachments/assets/8bb338ce-def7-4591-8d95-a3c35e502001">

*Figure 2: Positive Word Cloud*

The word cloud for positive reviews shows words like "great," "best," "love," and "happy," suggesting high satisfaction and positive outcomes, such as improved health, happiness, or effectiveness of the medication.



<img width="344" alt="review length" src="https://github.com/user-attachments/assets/c6f9cfec-57a9-4fb1-a20e-3ef71b3d1fef">

*Figure 3: Review length histogram*

The distribution is heavily skewed to the left, with the vast majority of reviews having relatively short lengths. Most of the reviews fall within a small range of lengths 
 on the lower end.The majority of reviews have lengths below 2,000, as shown by the high concentration of bars in that range.There are a few reviews with significantly higher lengths (extending up to 10,000 or more), though these are relatively rare. These could indicates that a significant portion of the reviews are quite short, with many of them likely being brief comments or minimal feedback.

<img width="499" alt="distribution of drug ratings" src="https://github.com/user-attachments/assets/72f7d41c-b19e-4db3-a1ac-f8a228e5f8ec">

*Figure 4: Ratings Histogram*

The distribution suggests that users tend to give extreme ratings, either very high or very low, with a notable lack of neutral or middle ratings. This could reflect polarized user experiences with the drugs


<img width="473" alt="top 10 c0nditions" src="https://github.com/user-attachments/assets/41d0a609-77d7-4c47-9777-31528668d7fa">

*Figure 5: Top 10 Conditions*

This bar chart shows the ten most frequently mentioned conditions. Depression, Pain, and Anxiety are the top conditions, reflecting prevalent health concerns. The overwhelming focus on birth control suggests it is a primary concern among users.Mental health conditions like depression and anxiety are significant themes, indicating a need for support and treatment in these areas.A variety of physical health issues are also discussed, emphasizing the diverse range of conditions that users are addressing.

<img width="479" alt="most common drugs" src="https://github.com/user-attachments/assets/d450149d-5bdb-4874-8b72-68216fe99cf5">

*Figure 6: Most Common Drugs*

This horizontal bar chart identifies the ten most frequently reviewed drugs. Drugs like Levonorgestrel and Escitalopram have the highest counts, suggesting their popularity or wide usage ,likely reflecting their effectiveness or widespread prescription.



<img width="443" alt="top 5 top 3 drugs adminsitered" src="https://github.com/user-attachments/assets/3578b428-2a27-4b40-81b9-27b7f5e9c8f0">

*Figure 7: Top 5 conditions vs drugs*

This grouped bar chart links the top five conditions to the top 10 drugs administered for those conditions. It highlights which drugs are commonly used for specific health issues like Depression and Anxiety.Relationship between conditions and drugs reveals patterns in pharmaceutical treatment, with some drugs serving multiple conditions effectively.

<img width="533" alt="average rating  over time" src="https://github.com/user-attachments/assets/4a158bd0-ec50-4677-937d-68b3fcf5dac2">

*Figure 8: Average rating over time*

This line chart tracks the average ratings for the top five drugs over a period of time. The trends vary, with some drugs experiencing a decline or fluctuation in their average ratings, indicating changing user satisfaction or evolving efficacy perceptions.The fluctuating average ratings for drugs over time suggest changing user experiences, possibly due to shifts in drug formulations, side effects, or treatment expectations.lets look at Nexplanon:
This drug has a clear upward trend, starting at a low average rating near 5.0 in 2008 and gradually increasing to approximately 7.5 by 2016, indicating growing acceptance or satisfaction among users.Users may report fewer side effects and greater convenience compared to other methods, enhancing satisfaction.

<img width="426" alt="top 10 bigrams" src="https://github.com/user-attachments/assets/ade3a1be-a7b8-4f45-8d55-94e2f431318a">

*Figure 9: Top 10 Bigrams*

The prominence of "birth control" reinforces that contraceptive methods are a primary focus of user reviews.Emotional responses and side effects are critical themes, reflecting users' concerns about their experiences.References to age and time indicate that personal context plays a significant role in user feedback.



<img width="467" alt="top 10 trigram" src="https://github.com/user-attachments/assets/6de59a13-401d-44bf-8987-0168b2d1b958">

*Figure 10: Top 10 Trigrams*

"birth control" appears to be the most common trigram, suggesting a strong focus on contraceptive topics in the reviews."im year old" and "mg twice day" are also highly frequent, indicating that users may often mention their age and dosage instructions."high blood pressure" suggests concerns related to medical conditions that may be relevant to the drugs being reviewed.








<img width="283" alt="correlation matrix" src="https://github.com/user-attachments/assets/5d2f128d-b6ec-46a0-b479-cc031cfc8ae7">

*Figure 11:correlation matrix*

The correlation heatmap illustrates the relationship between review length and rating. The correlation coefficient between these two variables is 0.01, indicating a negligible correlation. This suggests that there is no significant relationship between the length of reviews and the ratings given by users, as the values are close to zero.








#### SUMMARY

This EDA provides a clear picture of how patients interact with medications and their experiences over time. Depression, anxiety, and pain emerge as the most common health challenges, reflecting key areas of focus for healthcare providers. Many drugs receive high ratings, suggesting overall satisfaction, but fluctuations in ratings over time highlight the importance of monitoring long-term effectiveness and patient perceptions.

A small group of medications dominates in usage and reviews, often addressing multiple conditions. This points to their widespread reliability but also emphasizes the need for personalized treatment options. The link between conditions and the drugs used for treatment offers valuable insights into current healthcare practices.

Overall, these findings show the value of listening to patient experiences to improve drug development, refine treatment strategies, better meet the needs of those seeking care and addressing the gaps in treatment effectiveness and patient satisfaction.

## STEP 3:Model Fitting
### Naive Bayes Multinomial Model
 The Naive Bayes model used was MultinomialNB.The motive behind this model is because it is well-suited for text data where the features represent the count or frequency of words. This aligns well with how TF-IDF Vectorizer works, which converts text into a matrix of TF-IDF features.We used TFIDF vectoriser instead of count Vectorizer the reason being it helps represent the importance of words in the corpus. Words that are frequently used in a document but rare across the whole dataset get higher weights, improving the differentiation between documents, also TF-IDF Vectorizer can handle a large vocabulary and transform it into a sparse feature matrix, making it suitable for models like MultinomialNB.

 Train -test-Split was done using train-test-split() from sklearn.The data was divided into 80% train data and 20% test data ,to ensure that the model is trained on a sustantial portion of tha data while keeping a separate for validation and testing.

The process for hyperparameter selection involved using GridSearchCV to identify the best parameters for both the TfidfVectorizer and MultinomialNB model. We set up a parameter grid with options for the number of features (max_features), n-gram range (ngram_range), and smoothing parameter (alpha). We applied 5-fold cross-validation to ensure robust evaluation of each parameter combination, with accuracy as the scoring metric.
The grid search process helped pinpoint the most effective configuration: a max_features of 10,000, an ngram_range of (1, 2), and an alpha of 0.1. This approach allowed us to systematically explore different hyperparameter combinations and find the optimal ones to improve model performance. Cross-validation helped us avoid overfitting and ensured that the model's performance was evaluated on different subsets of the training data for better generalization.
The best cross-validation score of 0.411 suggests that the model, while better than random guessing, does not yet achieve high accuracy. This may indicate the need for further fine-tuning or exploration of other model types.
From our results results yperparameters selection imply that the alpha parameter for MultinomialNB at 0.1, a larger max_features (10000), and using both unigrams and bigrams contributed to the best performance.

<img width="238" alt="confusion matrix" src="https://github.com/user-attachments/assets/fd4bb869-cad3-45f9-9733-df27edccc0a1">

*Figure 12:Confusion Matrix*


While accuracy was the initial metric considered, a deeper analysis using precision, recall, and F1-score helped identify specific weaknesses, such as underperformance in identifying certain classes. The confusion matrix confirmed that the model had a biased approach toward more frequent classes and struggled to detect rarer ones effectively



#### Predictions:
The model was tested using our raw data and processed data and the results were these:

<img width="521" alt="testing" src="https://github.com/user-attachments/assets/0ff7209c-d5b6-4cca-9d83-44691fad28e6">

*Figure 13:testing code*

#### Prediction from new data

##### Model Prediction Examples

Below are examples of how the model predicts the rating for new reviews, along with additional details such as the drug name, condition, and actual rating:

| **Review**                                                                                                                               | **Drug Name**              | **Condition**           | **Actual Rating** | **Predicted Rating** |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|-------------------------|-------------------|-----------------------|
| *"Limited improvement month developed bad rash md refused continue medication"*                                                         | Abatacept                  | Rheumatoid Arthritis    | 4                | 1                     |
| *"Suboxone completely turned life around feel healthier im excelling job always money pocket saving account none suboxone spent year abusing oxycontin paycheck already spent time got started resorting scheming stealing fund addiction history youre ready stop there good chance suboxone put path great life found sideeffects minimal compared oxycontin im actually sleeping better slight constipation truly amazing cost pale comparison spent oxycontin"* | Buprenorphine / naloxone   | Opiate Dependence        | 9                 | 10                    |

*Table 3:Predictions*

#### Training and Loss Validation

<img width="329" alt="training validation loss" src="https://github.com/user-attachments/assets/14176c6c-fd5a-4201-82a3-fd104811d408">

The training loss is decreasing, indicating the model is fitting the training data well.However, the validation loss is increasing after a certain fold number, suggesting the model is not generalizing well to the validation data.This is a classic sign of overfitting, where the model has learned the training data too well but fails to perform on unseen data.

### Neural Network

We implemented the Neural network model.The reason behind the choice is :Neural networks  automatically learn relevant features from raw data, reducing the need for extensive feature engineering. This is particularly useful in high-dimensional spaces.Employing a neural network model for this dataset can facilitate a deeper understanding of user sentiments, improve predictive modeling for ratings based on reviews, and adapt to the complexity and variability of natural language, ultimately leading to better insights into drug effectiveness and user experiences.

The architecture used in the code is a Long Short-Term Memory (LSTM) network, which is a type of Recurrent Neural Network (RNN) well-suited for sequence data, such as text.The model has 5 layers listed as follows:
Architecture Components:
##### Embedding Layer:
Input Dimension: 5000 (number of words to consider in the vocabulary).
Output Dimension: 128 (size of the embedding vector for each word).
This layer transforms input sequences into dense vectors of fixed size, capturing semantic relationships between words.

##### LSTM Layer:
Units: 128 (the number of LSTM units).
Return Sequences: False (this means that only the output of the last time step is returned, which is appropriate for regression tasks).
LSTMs are effective in capturing long-range dependencies in sequential data, which is crucial for understanding context in text reviews.

##### Dropout Layer:
Dropout Rate: 0.5 (50% of the neurons are randomly dropped during training).
This helps prevent overfitting by making the model more robust and ensuring it does not rely too heavily on any particular feature.

##### Dense Layer:
Units: 64 (the number of neurons in this fully connected layer).
Activation Function: relu (Rectified Linear Unit), which introduces non-linearity to the model and helps it learn complex patterns.

##### Output Layer:
Units: 1 (for regression output).
Activation Function: linear (suitable for predicting continuous values like ratings).

#### Hyperparametres:

Batch Size (32): Processes 32 reviews at a time, balancing memory usage and stable gradient estimates, which helps the model learn diverse patterns from user-generated content.
Epochs (5): The model trains over the entire dataset five times, refining its understanding of the relationship between review text and ratings. This number may need adjustment if overfitting occurs.
Optimizer (Adam): An adaptive learning rate algorithm that enhances convergence speed and model performance, effectively handling the noisy nature of user reviews.
Loss Function (Mean Squared Error - MSE): Measures the average squared difference between predicted and actual ratings, emphasizing larger errors to ensure significant ratings are accurately predicted.

R² Score was used and it indicates the proportion of variance explained by the model, with a score of approximately 0.67 suggesting a moderate level of predictive accuracy.
But the model exhibited some weakness though accuracy was found out to be o.67.The model exhibits some error, as indicated by the MAE (1.23) and RMSE (1.88). This suggests that while it performs reasonably well, there are instances where predictions deviate significantly from actual ratings.
### Predictions:
#### from Data
A review predicting a rating of 9 might correspond to positive feedback indicating satisfaction with a medication’s effectiveness.

A review predicting a rating of 2 could stem from negative experiences, highlighting side effects or lack of efficacy.
#### From New Data

| *Field*               | *Value*                                                                                      |
|-------------------------|-----------------------------------------------------------------------------------------------|
| * Query*              | What are reviews for drug treating ANXIETY                                                                                              |
| *Answer from Reviews* | medicine ive ever used helped decrease anxiety helped anxiety medicine                        |
| *Average Rating*      | 10.00                                                                                        |
| *Drugs Mentioned*     | Clonazepam, Klonopin, Valium, Diazepam                                                       |
| *Positive Reviews*    | helped anxiety medicine<br>- medicine ive ever used helped decrease anxiety                |
| *Negative Reviews*    | No negative reviews found.                                                                   |


### Multi-Output Model and Chatbot Overview

#### Multi-Output Prediction: Drugs, Rating, and Review
The model predicts multiple outputs (drugs, rating, reviews) using a multi-task learning framework:

1. **Input Preprocessing:** Processes input data with tokenization and embeddings.
2. **Shared Encoder:** Extracts features using CNNs, LSTMs, or transformers.
3. **Task-Specific Heads:**\n
   - **Drug Prediction:** Identifies the prescribed drug (softmax classifier).
   - **Rating Prediction:** Predicts ratings (regression or ordinal classification).
   - **Review Generation:** Generates text reviews (sequence-to-sequence model).
4. **Loss Functions and Optimization:** Combines task-specific losses and optimizes end-to-end.
5. **Output Post-Processing:** Decodes predictions into human-readable formats.

#### Chatbot Functionality
The chatbot integrates with the prediction model and operates as follows:

1. **Natural Language Understanding (NLU):** Extracts intents and entities using models like BERT.
2. **Dialogue Management:** Determines responses based on conversation state.
3. **Response Generation:** Uses templates or neural models for contextual replies.
4. **Multi-Turn Conversations:** Tracks history for coherent interactions.
5. **Integration with Prediction Model:** Queries the model for outputs and combines them into responses.
6. **Safety Mechanisms:** Filters inappropriate content and provides disclaimers.
7. **Continuous Learning:** Improves with user feedback and reinforcement learning.

#### Example Workflow
1. **User Query:** “What’s the best drug for migraines?”
2. **Processing:** Identifies intent and keywords, and the model predicts:
   - Drug: “Sumatriptan”
   - Rating: 4.5
   - Review: “Effective for most users with mild side effects.”
3. **Response:** “For migraines, Sumatriptan is recommended with a 4.5 rating. Users find it effective with mild side effects.”


## Production

To ensure effective deployment of the model, we will continuously monitor performance metrics such as MAE, RMSE, and R², while setting up alerts for any significant drops in performance. Regular updates with new data are essential for maintaining the model's relevance and accuracy. Incorporating a user feedback loop will also help refine predictions based on real-world outcomes. Additionally, leveraging cloud-based solutions will allow for scalable resource allocation according to demand, and seamless integration with existing systems will facilitate easy access for users.

Precautions include emphasizing that the model is a supportive tool and should not replace professional medical advice. It's important to evaluate the model for biases to avoid reinforcing disparities in treatment recommendations, acknowledging that predictions may not always reflect individual experiences. Compliance with data privacy regulations is vital, and robust data protection measures should be implemented. Lastly, establishing a fallback mechanism for reporting issues and providing alternative recommendations if the model fails is essential for responsible use in healthcare settings.

## Going Further
To improve the model, several strategies can be implemented. Increasing the volume of training data would enhance its ability to generalize, especially with a wider variety of user experiences and drug types. Incorporating additional features, such as demographic information (age, gender), specific dosage details, or temporal data (time of review), could provide richer context and improve prediction accuracy. Data augmentation techniques, like paraphrasing reviews or synthesizing new examples, would help diversify the training dataset, making the model more robust to variations in language and sentiment. Exploring different architectures, such as transformers, and fine-tuning hyperparameters like learning rates and dropout rates could further enhance performance. Additionally, employing ensemble methods by combining predictions from multiple models could reduce variance and improve overall accuracy. By implementing these enhancements, the model could become more accurate and reliable in predicting drug ratings based on user reviews.










 



 


 


 



 




              

                                     




