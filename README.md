# Sentiment Analysis with NLP on Tweets

### Overview
This project dives into the world of Natural Language Processing (NLP) to classify tweet sentiments about Apple and Google products. Using a dataset of over 9,000 tweets, we explore, model, and tune machine learning algorithms to accurately predict whether a tweet has a **positive**, **neutral**, or **negative** sentiment.

### Dataset
The data, sourced from CrowdFlower, consists of tweets labeled by human raters on sentiments related to Apple and Google products. Each tweet is categorized as either positive, negative, or neutral, providing an excellent foundation for training supervised NLP models.

### Project Goal
Our goal is to build an effective model that can rate the sentiment of a tweet based on its content, allowing companies like Apple and Google to gauge public opinion in real time.

### Models Used
To capture the best-performing sentiment classifier, we experimented with and fine-tuned several models, optimizing them using hyperparameters and adjusting for class imbalances. Here’s a breakdown of the models tested:

1. **Logistic Regression with Count Vectorizer**  
   - **Standard Logistic Regression**: Our baseline model using `C = 1.0`.
   - **Class-Balanced Logistic Regression**: We set `class_weight='balanced'` to improve performance on minority classes, specifically Negative and Positive sentiments.
   - **Tuned Logistic Regression**: We tested varying regularization strengths with `C = 0.5`, finding this value offered the best balance of recall for Neutral tweets without sacrificing accuracy.

2. **Multinomial Naive Bayes**  
   - **Count Vectorizer and TF-IDF**: Using both vectorization techniques, we evaluated how Naive Bayes could handle the term frequencies and document frequency weights effectively for sentiment classification.

3. **K-Nearest Neighbors (KNN)**  
   - Although less commonly used for NLP, we included KNN with both Count Vectorizer and TF-IDF to evaluate how proximity-based models perform on tweet data.

### Key Findings
Our best model is the **Logistic Regression model with `C = 0.5`**. This model excels in identifying neutral tweets (93% recall).

### Next Steps
To further improve the model’s performance, additional data sources or pre-trained language models (e.g., BERT) could be explored. Additionally, handling class imbalance with advanced techniques, such as SMOTE or ensemble methods, might yield even better results.

---

Happy Modeling! 🎉
