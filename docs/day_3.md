# Day 3: Diving into Exploratory Data Analysis

### Overview
Today, I took a step further into my project by focusing on exploratory data analysis (EDA). My goal was to visualize key aspects of the dataset, including sentiment distribution, tweet length, and the most commonly used words. Along the way, I cleaned up some lingering issues in the data and created visualizations to uncover patterns. It was a productive day of discovery, and I’m excited to share the results and the insights gained.

### Sentiment Label Distribution
The first task was to understand the sentiment label distribution. Initially, the dataset had four labels: positive, neutral, negative, and irrelevant. I quickly realized that the "irrelevant" label was more noise than value, so I decided to remove it from the analysis to maintain focus on the actual sentiments. Once I cleaned that up, I visualized the remaining labels. As expected, positive sentiments far outnumbered neutral and negative ones. This imbalance is something I’ll need to account for when building my model later.

### Word Cloud: Visualizing Common Words
Next, I created a word cloud to visualize the most frequently used words across all the tweets, which is always an enjoyable step since it provides a colorful and immediate sense of the conversation topics. Initially, the word cloud contained positive sentiments such as "love" and "good," but I also noticed non-sentiment words like "game" and "xbox series" dominating the cloud. To address this, I utilized the word cloud to identify and filter out irrelevant words, such as "games," "borderlands," and "xbox." This was done with the goal of optimizing the data going into training. I implemented a stop word filter function to remove any words from the `cleaned_tweet_content` that matched those in my specified stopword list. I made sure to continuously check the word cloud after adding new stopwords, refining the list until I was satisfied with the results.

### Tweet Length Distribution
Another interesting aspect of the dataset was the length of the tweets. I generated a bar graph to explore how long or short the tweets were. It turned out most tweets were pretty brief—typically under 10 words. This isn’t all that surprising given Twitter’s character limits, but it’s a useful insight as I start thinking about feature engineering for the model. Short tweets might not carry much information, so handling them effectively will be important.

### Cleaning Up Further
After visualizing the data, I went back for a final round of cleaning. While I had already removed URLs and some special characters, there were still a few random strings and short noise like ".com" and "co" scattered throughout the text. Using regular expressions, I filtered out these remaining bits of noise to ensure that the dataset was as clean as possible. This should improve the model’s performance by removing irrelevant content that could throw off the predictions.

### Challenges Faced
One of the ongoing challenges was dealing with the imbalanced sentiment distribution. The higher number of positive tweets means the model could end up biased toward positive predictions, which I’ll have to address during training. Another challenge was cleaning up the text data. While regular expressions helped, I had to tweak my approach a few times to ensure I wasn’t accidentally removing useful content. It’s a reminder that even small cleaning tasks can take time but are worth the effort.

### Key Learnings
Today’s work reinforced a few key lessons. First, thorough exploration before modeling can save a lot of headaches later. Spotting the imbalance and cleaning up the noise now will make for better results down the line. Second, visualizing the data helped guide my approach to cleaning and prepping for the next steps. And finally, taking the time to experiment with cleaning methods, like using regex for URL and string removal, paid off with a much cleaner dataset.

### Next Steps
With the data cleaned and visualized, the next logical step is feature engineering. I’ll need to think carefully about how to handle the label imbalance, possibly by using resampling techniques or weighting. Then, I’ll start training the model and testing a few different algorithms to see which performs best on this dataset. I also plan to document this process on GitHub and reflect on it in future blog entries.

### Conclusion
Today’s exploratory data analysis was a valuable deep dive into the dataset. I gained new insights through visualization, cleaned up remaining noise, and prepared myself for the modeling phase. I’m feeling more confident as I move forward, knowing I’ve laid a solid foundation for the next steps.