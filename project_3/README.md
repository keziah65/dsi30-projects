# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

### Problem Statement


As a member of the Netflix data scientist team, I am assigned to research the general customer opinions toward Netflix and one of its competitors, Disney+, on Reddit.

The goals of this project are:

-   to categorize postings on the r/netflix and r/DisneyPlus subreddits
-   to investigate the reasons behind Netflix's declining subscriber count
-   to suggest potential solutions to increase Netflix's subscriptions


#### Background


Netflix is one of the world's most popular streaming service. In 2022, Netflix lost over 1.2 million customers.

Based on the  [source](https://www.makeuseof.com/why-netflix-is-losing-subscribers/), here are the following reasons why Neflix is losing subscribers:

-   1.  Netflix Pulled Its Service From Russia
-   2.  Netflix Hiked Up Prices
-   3.  Netflix Account Sharing Slows Down Growth
-   4.  Netflix Keeps Losing Content From Media Companies
-   5.  Quality of Content
-   6.  There Are Too Many Streaming Services

This project would like to dive deeper into studying and comparing Netflix with one of its biggest competitor, Disney Plus.

### Model Summary
**![](https://lh3.googleusercontent.com/LxnPaH95TxJPVn5z5SGdciZxHvuqtdQENTn38RyxTtwWNIx7cTa6AMVLYXlTp7segkbEgeiAE76maBRbzb3Vd9_vHxwlz35Xw7uKr2Tp4U_k6buJyUkl0rfimfVtjbKX8WNv7Lh2jHMJcyL6c2e1RqgB_A)**

### Conclusion

All the models outperformed the baseline accuracy score of 0.5. As the focus is on getting as many correct predictions as possible with lesser overfitting, the Random Forest classifier with TFI-DF Vectorizer has the best predictive performance on the classification problem. The Random Forest model can classify the subreddit's post with 73.5% accuracy by first vectorizing the text using TFI-DF Vectorizer.

However, there is quite a high overfitting in our overall model indicating that the 2 subreddits' posts might have quite a number of similar words. We might want to fine-tune our stop words or collect more data points to have a better prediction.

---

### Business Recommendations

Based on the importance of the features, the shows available on each streaming platform are dominating the top features for predictions. There are stranger things, marvel, resident evil, mena, obi wan kenobi, star wars, and so on. We can see that customers subscribe to a streaming service based on the type of content that it can provide. Disney Plus provides such a good bargain at $8 a month for anyone who loves Disney, Marvel, Pixar, and National Geographic. Disney Plus is also the only place where you can watch Obi-Wan Kenobi. On the other hand, Netflix has content that is suitable for all ages. However, the quality of movies that Netflix produces could vary. Therefore, Netflix should continue to try to increase the quality of movies that it produces so that it can attract more people of all ages.

### Further Improvements

- Collect more data points
- Add ensemble model to reduce overfitting
- Include more relevant or similar subreddits
- Explore additional features
- Add more specific stop words


---




