# Social Media Sentiment & Engagement Analysis using Spark SQL and DataFrames

## 📘 Overview
This project analyzes a fictional social media dataset using Apache Spark. The goal is to extract meaningful insights from posts and user information by leveraging Spark SQL and DataFrames.

You’ll explore:
- Trending hashtags
- User engagement by age group
- Sentiment-driven behavior
- Influencer reach based on engagement

---

## 📂 Dataset

### 1. `posts.csv`
Contains user-generated post data.
| Column | Type | Description |
|--------|------|-------------|
| PostID | Integer | Unique post identifier |
| UserID | Integer | ID of the user who made the post |
| Content | String | Text content of the post |
| Timestamp | String | Date and time of posting |
| Likes | Integer | Number of likes |
| Retweets | Integer | Number of retweets |
| Hashtags | String | Comma-separated hashtags |
| SentimentScore | Float | Sentiment score from -1 to 1 |

### 2. `users.csv`
Contains user profile information.
| Column | Type | Description |
|--------|------|-------------|
| UserID | Integer | Unique user ID |
| Username | String | User’s handle |
| AgeGroup | String | Age category (Teen, Adult, Senior) |
| Country | String | Country of residence |
| Verified | Boolean | True if the account is verified |

---



---

## Tasks & Logic

###  Task 1: Hashtag Trends
- Extract and split hashtags
- Count frequency of each hashtag
- Output: Top 10 most-used hashtags

###  Task 2: Engagement by Age Group
- Join posts with user info
- Group by `AgeGroup` and calculate average `Likes` and `Retweets`

###  Task 3: Sentiment vs Engagement
- Categorize sentiment as Positive (>0.3), Neutral (-0.3 to 0.3), or Negative (<-0.3)
- Aggregate average likes and retweets per sentiment type

### ✅Task 4: Top Verified Users by Reach
- Filter for `Verified` users
- Calculate total reach (Likes + Retweets)
- Output: Top 5 most influential users by reach

---

##  Requirements
- Python 3.8+
- Apache Spark 3.x
- PySpark

Install dependencies:
```bash
pip install pyspark
```

###How to Run

spark-submit src/task1_hashtag_trends.py
spark-submit src/task2_engagement_by_age.py
spark-submit src/task3_sentiment_vs_engagement.py
spark-submit src/task4_top_verified_users.py

Output CSVs will be saved in the outputs/ folder.
