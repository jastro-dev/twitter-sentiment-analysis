# Day 2: Preprocessing and Cleaning the Dataset

### Overview
Day two was all about data preparation, focusing on cleaning and preprocessing the dataset to get it ready for analysis. I made significant progress with data cleansing, tackling missing values as well as handling messy text data. Below, I’ll share the key steps taken, challenges faced, and important lessons learned.

### Data Cleaning and Preprocessing
The first order of business was getting the data in shape. I started by dealing with missing values by dropping them. Next, I took care of duplicate entries to keep things consistent. However, the real work came with cleaning up the tweet content data. Since the text is derived from tweets, I decided to clean the content by stripping away URLs, hashtags, mentions, and special characters. I also removed stop words and converted the text to lowercase to standardize the format, utilizing the Regular Expression as well as the Natural Language Toolkit modules for efficient text processing.

### Saving the Cleaned Data
Once everything with the dataset was looking good, I exported the new dataframes to `cleaned_twitter_training.csv` and `cleaned_twitter_validation.csv`. I kept the file names simple, just to keep things organized and easy to find later.

### Version Control Practice
I was also able to practice using GitHub by working with branches to manage changes, which allowed me to roll back updates if needed. Sooner or later these git commands are going to get burned into my memory.

### Challenges Faced
For challenges faced today, the process of cleaning the text wasn’t as straightforward as I’d hoped. Since tweets often include hashtags and URLs, I had to take care to remove these elements to optimize the data for modeling. Seeing the results after the cleanup highlighted the importance of proper data preparation in my analysis.

### Key Learnings
If today taught me anything, it’s that data quality is everything. Spending time cleaning the dataset now is going to pay off big time during the analysis phase. Also, sticking to good version control practices, like branching and regular commits, made the whole process feel more manageable.

### Next Steps
Now that the data is clean, I plan to dig into some exploratory data analysis (EDA) to help uncover patterns and discover new insights. I also plan to utilize different visualizations in order to further explain my findings and reasonings.

### Conclusion
Day two was a productive step forward in getting the dataset ready for analysis. There were some bumps along the way, but I’m learning a lot and building momentum. I'm very excited to get to the next steps of this journey.