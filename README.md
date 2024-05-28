# sentiment_analysis_BERT
Sentiment Analysis of Wessex Water using Pre-trained BERT Model

This summary outlines the steps taken to perform sentiment analysis on customer reviews of Wessex Water using a pre-trained BERT model. The analysis categorizes sentiments into five classes: very negative, negative, neutral, positive, and very positive.

**Objectives**:
Extract customer reviews from the Wessex Water Trustpilot page.
Use a pre-trained BERT model to determine the sentiment of each review.
Categorize and analyze the sentiment scores.

**Methodology**:
Review Extraction:

Reviews were collected from the first 10 pages of Wessex Water's Trustpilot review section using web scraping techniques with BeautifulSoup.

Sentiment Analysis:
The nlptown/bert-base-multilingual-uncased-sentiment BERT model and its corresponding tokenizer were used to analyze the sentiment of each review.
Each review was tokenized into a format suitable for the BERT model and fed into the model to obtain prediction logits.
The logits were processed to determine the sentiment score, ranging from 1 to 5 (1 being very negative and 5 being very positive).

Data Processing:
The sentiment scores were computed and added to a DataFrame containing the reviews.
Reviews were categorized based on their sentiment scores.
Bad reviews (sentiment scores of 1 or 2) were identified and extracted for further analysis.

Findings:
The sentiment analysis provided a detailed view of customer opinions, highlighting areas of satisfaction and dissatisfaction.
The processed reviews were categorized as follows:
1 = Very Negative
2 = Negative
3 = Neutral
4 = Positive
5 = Very Positive
Bad reviews were isolated to identify common issues and areas needing improvement.
