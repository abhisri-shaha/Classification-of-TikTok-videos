
# Classification of Tiktok videos

Machine learning models developed to predict whether Tiktok videos present claims or opinions. This project is aimed at streamlining the process of video review by flagging content for human evaluation.


## Background
TikTok users have the ability to submit reports that identify videos and comments that contain user claims. These reports identify content that needs to be reviewed by moderators. The process generates a large number of user reports that are challenging to consider in a timely manner. 

TikTok is working on the development of a predictive model that can determine whether a video contains a claim or offers an opinion. With a successful prediction model, TikTok can reduce the backlog of user reports and prioritize them more efficiently.


## EDA (Exploratory Data Analysis)
### Data exploration
- **Dataset**: The dataset includes video metadata such as video ID, duration (in seconds), transcription text, view count, like count, download count, comment count and claim status as well as author information such as verified status and ban status.
- **Shape**: There are 19382 rows and 12 columns in the dataset.
- **Basic information**: Number of non-null entries in each column and their respective datatypes.
- **Descriptive statistics**: Key metrics such as mean, standard deviation, minimum, maximum, etc.

### Data visualization
- **Box Plots**: Examine the spread of values in various columns
- **Histograms**: Explore the distribution of variables
- **Pie graph**: Depict the proportion of total views for claim videos and total views for opinion videos
- **Scatter Plots**: Explore correlations between different features

### Data cleaning 
- **Outlier Removal**: Identify and remove outliers from count variables (e.g., view count, like count) to ensure robust statistical analysis.
## Hypothesis Testing
- **Objective**: Determine if there is a statistically significant difference between the view count of videos posted by verified accounts and those posted by unverified accounts on TikTok.
- **Method**: Conduct a two-sample t-test.
- **p-Value**: The p-value is 2.6×10⁻¹²⁰, which is extremely small and far below the significance threshold of 0.05.
- **Result**: The difference in the view count between videos posted by verified accounts and those posted by unverified accounts on TikTok is of statistical significance. The cause of this difference requires further investigation. Possible causes could include unverified accounts posting more clickbait-y videos or they might be associated with spam bots that help inflate views.


## Models and Evaluation Metrics

### Logistic Regression
- **Objective**: Predicts verified user status, as initial observations indicated a link between verification and posting opinions. It was observed that if a user is verified, they are much more likely to post opinions. This analysis aims to inform a final model for predicting whether a video presents a claim or an opinion.
- **Results**:
  - **Accuracy**: 65%
  - **Precision**: 67% (weighted average)
  - **Recall**: 65% (weighted average)
  - **F1 score**: 64% (weighted average)
- **Interpretation**: Indicates moderate performance; further tuning needed.

### Random Forest
- **Objective**: Predict claim status
- **Results**:
  - **Accuracy**: 100%
  - **Precision**: 100% (weighted average)
  - **Recall**: 100% (weighted average)
  - **F1 score**: 100% (weighted average)
- **Interpretation**: Excellent performance; may indicate overfitting.

### XGBoost
- **Objective**: Predict claim status
- **Results**:
  - **Accuracy**: 99%
  - **Precision**: 99% (weighted average)
  - **Recall**: 99% (weighted average)
  - **F1 score**: 99% (weighted average)
- **Interpretation**: High performance with slight potential for overfitting; robust model choice.

## Future Work
- Enhance model generalization to avoid overfitting.
- Integrate more diverse data sources to improve prediction accuracy.
- Implement real-time video analysis for faster moderation.
## Conclusion
This project demonstrates the potential for machine learning models to assist in moderating TikTok content. The developed models show promise in distinguishing between claims and opinions, which can significantly streamline the moderation process and enhance content review efficiency.
