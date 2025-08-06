# Twitter Data Scraping & Word Cloud Analysis

A comprehensive Python project for collecting, analyzing, and visualizing Twitter data from financial/trading accounts using the Twitter API and word cloud generation.

## 🎯 Project Overview

This project demonstrates how to:
- **Collect Twitter data** using the official Twitter API via `tweepy`
- **Process and clean** unstructured social media text data  
- **Generate visualizations** with word clouds to identify trending topics
- **Store and analyze** data in multiple formats (CSV, Excel)

## 📊 Features

- ✅ **Twitter API Integration**: Secure OAuth authentication
- ✅ **Multi-Account Scraping**: Collect tweets from multiple financial accounts
- ✅ **Data Processing**: Handle retweets, timestamps, and user information
- ✅ **Word Cloud Generation**: Visual representation of most common terms
- ✅ **Data Export**: Save results in CSV and Excel formats
- ✅ **Statistical Analysis**: Generate insights about collected data

## 🗂️ Data Structure

The collected data includes:
- **Tweet Text**: Full tweet content (280 characters)
- **Timestamp**: When the tweet was posted
- **Account ID**: Source account handle
- **User Name**: Display name of the account
- **Retweet Flag**: Whether the tweet is original content or a retweet

## 📁 Repository Structure

```
Twitter-Scraping/
├── Twitter Scraping.ipynb    # Main analysis notebook (well-commented)
├── Data/
│   ├── twitters_raw_data.csv # Raw tweet data (CSV format)
│   ├── twitter_raw_data.xlsx # Raw tweet data (Excel format)
│   └── README.md             # Data documentation
├── LICENSE                   # MIT License
└── README.md                # This file
```

## 🚀 Getting Started

### Prerequisites
```bash
pip install tweepy pandas matplotlib wordcloud jupyter
```

### Setup
1. **Get Twitter API credentials** from [Twitter Developer Portal](https://developer.twitter.com/)
2. **Clone this repository**
3. **Open the Jupyter notebook**: `Twitter Scraping.ipynb`
4. **Add your API credentials** (see security note below)
5. **Run the cells** sequentially

### ⚠️ Security Note
**Never commit API credentials to version control!** The notebook includes placeholders for credentials. Use environment variables or a secure config file for production use.

## 📈 Sample Analysis

The current setup analyzes tweets from financial trading accounts:
- `@jimcramer` - Investment advice and market commentary
- `@criticalcharts` - Technical analysis and charts
- `@zipcharlie` - Trading insights
- `@stockstobuy` - Stock recommendations  
- `@StocksToTrade` - Trading education

## 🎨 Word Cloud Example

The generated word clouds highlight the most frequently mentioned terms, with:
- **Larger text** = More frequent terms
- **Custom stopwords** = Filtered out common/irrelevant words
- **Financial focus** = Terms relevant to trading and markets

## 🔮 Future Enhancements

- **Sentiment Analysis**: Score tweet sentiment (positive/negative/neutral)
- **Temporal Trends**: Track how topics change over time
- **Hashtag Analysis**: Extract and analyze hashtag usage patterns
- **Real-time Monitoring**: Automated data collection and alerts
- **Interactive Dashboards**: Web-based visualization interface

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for improvements.

---

*This project is for educational purposes and demonstrates social media data analysis techniques. Please respect Twitter's Terms of Service and API rate limits.*
