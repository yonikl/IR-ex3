# Information Retrieval Assignment 3 - Sentiment Analysis Report—README

## Students Information
- Names: Moshe Shahar, Yonatan Klein
- IDs: 211692165, 322961764

## Project Overview
This project involves performing sentiment analysis in the context of pro-Israeli or pro-Palestinian, on articles from various newspapers. Using multiple pre-trained sentiment analysis models, we analyzed the content to classify articles into categories (e.g., Positive, Negative, Neutral). The goal was to extract meaningful insights about the sentiment distribution across different newspapers and assess the behavior of reporters and their writing styles.

## Methodology
### Steps Taken:
1. **Data Loading**: 
   - Loaded articles from multiple newspapers into Pandas DataFrames.
   - Merged content from titles, subtitles, and body text for comprehensive analysis.

2. **Preprocessing**:
   - Split text into sentences.
   - Filtered sentences containing Israel-related (`i_word`) or Palestine-related (`p_word`) keywords.

3. **Sentiment Analysis**:
   - Utilized multiple pre-trained models such as `cardiffnlp/twitter-roberta-base-sentiment-latest`.
   - Normalized labels to `Positive`, `Negative`, and `Neutral` for consistency.

4. **Aggregation and Scoring**:
   - Determined the dominant sentiment (`majority`) for each article.
   - Calculated average scores for the most frequent sentiment in each newspaper.

5. **Visualization**:
   - Generated pie charts for sentiment distribution per newspaper.
   - Created histograms and bar plots for additional statistical insights.

## Challenges
### Sentiment Identification:
- **Difficulty**: Certain sentences contained ambiguous or mixed sentiments, making it challenging for models to classify them.
- **Insights**: Articles with factual reporting or balanced arguments often resulted in Neutral classifications.

### Model Limitations:
- **Pre-trained Bias**: Sentiment models trained on specific datasets (e.g., Twitter) occasionally struggled with formal newspaper language.
- **Chunk Splitting**: Long sentences required truncation, potentially losing critical information.

### Anomalies:
- **Strange Behaviors**: Certain newspapers exhibited unexpected sentiment patterns, such as predominantly positive sentiments in critical contexts. This might reflect editorial bias or audience targeting.

## Results
### Pie Chart: Sentiment Distribution Per Newspaper
For each newspaper, we plotted the percentage of articles classified into Positive, Negative, and Neutral categories.

\![Pie Chart Placeholder](charts/sentiment_distribution_pie_chart.png)

### Histogram: Average Sentiment Scores
Displayed the distribution of sentiment scores across all articles.

\![Histogram Placeholder](charts/sentiment_score_histogram.png)

## Insights and Conclusions
1. **Newspaper Analysis**:
   - Newspaper A: Majority of articles were Neutral, reflecting balanced reporting.
   - Newspaper B: High proportion of Positive articles, indicating potential editorial bias.
   - Newspaper C: Dominantly Negative sentiments, possibly due to focus on critical or controversial topics.

2. **Reporter Recommendations**:
   - Encourage balanced reporting to reduce bias.
   - Diversify the vocabulary used to describe contentious topics to avoid skewing sentiments.

3. **Model Performance**:
   - Models performed well on simple sentences but struggled with context-heavy and ambiguous sentences.

## Error Analysis
### Common Errors:
- **Misclassification**: Ambiguous sentences were often misclassified.
- **Keyword Filtering**: Over-reliance on specific keywords led to missing nuanced sentiments.