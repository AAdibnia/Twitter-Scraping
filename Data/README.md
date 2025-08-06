# Data Directory

This folder contains the raw Twitter data collected from financial/trading accounts for word cloud analysis.

## 📊 Data Files

### `twitters_raw_data.csv`
- **Format**: Comma-separated values
- **Size**: ~93KB
- **Usage**: Primary data file for analysis
- **Encoding**: UTF-8

### `twitter_raw_data.xlsx` 
- **Format**: Microsoft Excel
- **Size**: ~52KB  
- **Usage**: Excel-compatible version for spreadsheet analysis
- **Features**: Formatted for easy viewing

## 🗂️ Data Structure

Each row represents a single tweet with the following columns:

| Column | Description | Data Type | Example |
|--------|-------------|-----------|---------|
| `Text` | Full tweet content (up to 280 chars) | String | "Market is looking bullish today..." |
| `Date` | Timestamp when tweet was posted | DateTime | "2021-07-02 01:21:21" |
| `id` | Twitter handle of the account | String | "jimcramer" |
| `Name` | Display name of the account | String | "Jim Cramer" |
| `Retweet` | Whether this is a retweet | Boolean | True/False |

## 📈 Data Collection Details

- **Source Accounts**: 5 financial Twitter accounts
- **Collection Method**: Twitter API v1.1 via `tweepy`
- **Tweet Mode**: Extended (full 280 characters)
- **Rate Limiting**: Automatic handling via API
- **Time Period**: Varies by account activity

## 🔍 Data Quality Notes

- **Retweets**: Original tweet text is preserved for retweets
- **Encoding**: Special characters and emojis are preserved
- **Timestamps**: All times are in UTC
- **Duplicates**: May contain duplicate tweets across accounts
- **Language**: Primarily English content

## 🛠️ Usage Examples

### Load with pandas:
```python
import pandas as pd
df = pd.read_csv('Data/twitters_raw_data.csv', index_col=0)
print(f"Loaded {len(df)} tweets")
```

### Basic analysis:
```python
# Count tweets per account
print(df['id'].value_counts())

# Check retweet ratio
retweet_ratio = df['Retweet'].mean()
print(f"Retweet ratio: {retweet_ratio:.2%}")
```

## ⚠️ Privacy & Ethics

- Data collected from **public** Twitter accounts only
- Respects Twitter's Terms of Service and API limits  
- Used for **educational/research purposes**
- Personal information anonymized where possible

---
*This data is unstructured social media content collected for text analysis and visualization purposes.*
