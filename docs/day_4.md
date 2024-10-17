# Day 4: Establishing a Baseline with Logistic Regression

### Overview

Today, I finally moved into model creation. With my datasets cleaned and organized, it was time to see how well the data could predict sentiment categories. I started by loading the cleaned `.csv` files and took a quick look at the dataset to refresh myself on the column names and features. From there, I applied TF-IDF to score the tweet content and tested the results with a logistic regression model. While there were a few issues, I made solid progress.

### Preparing Training and Test Data

I started by loading the cleaned datasets. I always find it helpful to take a quick glance at the columns before diving into anything else. After this, I assigned the training and validation datasets into their respective training and testing variables to ensure I had a good foundation for evaluating the model's performance.

### Defining Features and Utilizing TF-IDF

I used TF-IDF (Term Frequency-Inverse Document Frequency) to convert the tweet content into numerical data. TF-IDF assigns higher importance to unique words while filtering out common ones. This transformation is key for text-based data. However, I encountered a small issue. The columns I was working with were objects, and TF-IDF requires Unicode. To fix this, I converted the data to Unicode using `.astype('U')`. Once that was sorted, I moved on to model fitting.

### Logistic Regression

I chose logistic regression as my first model. It’s simple but effective when dealing with categorical data like sentiment analysis (Positive, Neutral, Negative). Logistic regression provides a solid baseline to check whether the preprocessing was effective. After fitting the model, I stored the predicted values in `y_pred` and began evaluating the results.

### Scikit-learn Metrics

Next, I evaluated the model using metrics from `sklearn.metrics`. I calculated accuracy, precision, recall, and F1 score. Additionally, I generated a classification report to better understand how well the model predicted each sentiment category. Each of these metrics is valuable for evaluating a model's performance:

- **Accuracy** is the ratio of correct predictions to total attempted predictions. It gives a general sense of how often the model is right, but doesn’t account for imbalances between classes.
- **Precision** measures how many of the predicted positive labels were actually correct (true positives vs. false positives). High precision means fewer false positives, which is crucial when false alarms are costly.
- **Recall** measures how many actual positives the model was able to identify. It's essentially about how well the model catches the true positive cases, and a lower recall means more positives were missed.
- **F1 Score** provides a balanced mean between precision and recall, which is useful when you need a single metric to assess the overall performance, especially when the class distribution is imbalanced.

The classification report provides a per-class breakdown of these metrics, making it easy to see how well the model performed for each sentiment category (Positive, Neutral, Negative). It also gives us two more metrics for the model:

- **Macro Average** summarizes the average performance across all classes equally, without considering the class sizes. It’s helpful to understand how the model treats each class in isolation.
- **Weighted Average** takes into account the relative sizes of each class when calculating the average, which is useful when one class is much larger than others (as in this project, where positive sentiment was overrepresented).

### Saving the Model

After running the evaluation, I saved the logistic regression model using `joblib`. Having a saved model is always useful, especially for future testing or if I need to make adjustments without retraining from scratch. Plus, it was a good way for me to practice saving my work.

### Creating a Visualization

To make sense of the results, I created a simple dataframe utilizing the data from the generated classification report. It’s always nice to see the metrics laid out like this, as it makes it easier to spot the differences in results.

### Analyzing Results

Now for the results. The logistic regression model performed fairly well when predicting positive sentiment but struggled more with neutral and negative categories. Not too surprising, though, as the dataset had about 1,000 extra positive samples, which likely biased the model. While this wasn’t ideal, it gave me a strong starting point for future improvements.

### Challenges Faced

One challenge was the type error I encountered with TF-IDF. Since TF-IDF requires Unicode, I had to adjust the data type. It was a quick fix, but it’s a good reminder to keep an eye on data types throughout the preprocessing phase. It was also a fun challenge to understand the reasoning behind different things, such as how TF-IDF works and why it’s important for sentiment analysis. Additionally, utilizing logistic regression as a baseline model gave me a solid foundation to build on. A lot of the challenges I faced on Day 4 were more about the thought process—understanding which approaches would work best and why—rather than just technical hurdles.

### Key Learnings

As a key learning, I learned the importance of balancing datasets for better accuracy. The extra positive samples skewed the results, but logistic regression still provided a solid baseline. I also gained more practice in visualizing model performance, which is becoming an essential skill.

### Next Steps

Next, I plan to implement an embedding model like GloVe to get more accurate, static vector representations for the tweet content. From there, I’ll dive into BERT, a transformer model that uses context for dynamic word representations. These models should help address the imbalance in the dataset and improve the model's overall performance. Additionally, I plan to re-balance the data to minimize any bias toward Positive sentiment values. This will help ensure a more-even distribution across all sentiment categories. Addressing this imbalance is crucial to prevent skewed results and improve the overall performance of the analysis.

### Conclusion

In conclusion, today marked a key step in my sentiment analysis project. Logistic regression served as a good baseline, but now it's time to move forward with more advanced techniques. I’m excited about the improvements that more sophisticated models can bring, and I’m eager to continue experimenting and learning.