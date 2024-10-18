# Day 5: Implementing More-Advanced Models

### Overview

Today, I focused on implementing more advanced models, starting with Random Forest using GloVe embeddings and then moving on to BERT. My initial baseline was Logistic Regression, so I wanted to see how these more sophisticated approaches would perform. After each implementation, I visualized the results to gain insight into how each model handled sentiment classification. These visualizations revealed important strengths and weaknesses across the models.

### Model Implementation and Fine-Tuning

The first step was setting up Random Forest with GloVe embeddings. I averaged the pre-trained vectors for each review and ran the model. Right after, I visualized the confusion matrix, which showed issues with neutral sentiments being misclassified as positive. GloVe’s static nature was a clear limitation. Moving on to BERT, I utilized PyTorch and my old 1080 Ti GPU, utilizing its CUDA cores to speed up the training process. Once BERT was implemented, I fine-tuned it by adjusting the learning rate and running extra epochs. After that, I visualized the results again—this time, BERT showed much better performance, especially with neutral and negative sentiment differentiation.


### Insights Through Visualization

The visualizations gave me crucial insights after each model was implemented. Random Forest, paired with GloVe, struggled to classify neutral sentiments correctly. It leaned toward predicting positive, which wasn’t surprising given GloVe’s lack of context awareness. In contrast, BERT’s confusion matrix told a different story—its dynamic embeddings captured the nuance of context, leading to far fewer misclassifications. Comparing the two models visually made it clear that BERT’s ability to adapt based on sentence structure was a game changer.

### Challenges Faced

BERT, while powerful, presented its own challenges in terms of setup and understanding the training process. Implementing PyTorch and utilizing the CUDA cores was the toughest part of today, as configuring everything correctly to leverage the GPU for faster training was new territory for me. My old 1080 Ti came in handy, but getting comfortable with the workflow of these more advanced models required some time. Random Forest, by comparison, was simpler to implement and didn’t demand as much computational effort, but it still struggled with imbalanced data, often over-predicting positive sentiments.

### Key Insights

Today’s work showcased the differences between static and dynamic embeddings. Random Forest with GloVe, although quick to train, couldn’t capture the subtleties needed for accurate sentiment prediction. BERT, on the other hand, thrived in this area due to its dynamic embeddings, which adapted to context. Visualizing the confusion matrices for each model made these differences even more apparent, highlighting BERT’s significant advantage in understanding complex sentiment relationships.

### Next Steps

To push BERT’s performance further, I’m considering implementing a grid search to fine-tune its hyperparameters. Adding an early stopping mechanism is also on the table to prevent overfitting during long training sessions. Additionally, I want to explore interactive visualization tools like Plotly to get a deeper analysis of how each model handles sentiment categories.

### Conclusion

Day five was all about experimenting with and refining advanced models. The visualizations after each implementation were key to understanding how Random Forest with GloVe compared to BERT. While Random Forest struggled with the static nature of GloVe embeddings, BERT’s dynamic approach led to more accurate sentiment classification. These insights have given me a clear direction moving forward, and I’m excited to keep on learning.