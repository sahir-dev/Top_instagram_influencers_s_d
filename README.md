# Instagram Influencers Analysis

Analysis of Top 200 Instagram Influencers - exploring engagement patterns, predicting influence scores, and classifying engagement levels.

## Overview

This project analyzes Instagram influencer data to understand what drives engagement and influence on the platform. Key questions explored:

- Do more followers mean better engagement?
- Which countries produce the most top influencers?
- Can we predict an influencer's impact from their metrics?

## Dataset

- **Source**: Top Instagram Influencers Data (Cleaned)
- **Records**: 200 influencers
- **Features**: rank, username, influence_score, posts, followers, avg_likes, engagement_rate, total_likes, country

## Key Findings

### The Engagement Paradox
Interestingly, influencers with fewer followers tend to have higher engagement rates:
- Accounts with >100M followers: **0.91%** avg engagement
- Accounts with <50M followers: **2.01%** avg engagement

This suggests micro-influencers might offer better ROI for brand partnerships.

### Top Performers
| Category | Influencer | Value |
|----------|------------|-------|
| Most Followers | cristiano | 475.8M |
| Highest Engagement | j.m | 26.4% |
| Top Influence Score | selenagomez | 93 |

### Geographic Distribution
- USA leads with 66 influencers (33%)
- 26 countries represented
- Emerging markets: Brazil (13), India (12), Indonesia (7)

## Project Structure

```
├── analysis.py              # Main analysis script
├── top_insta_influencers_data.csv
├── data/
│   ├── cleaned_data.csv
│   └── featured_data.csv
├── visualizations/
│   ├── 01_top15_followers.png
│   ├── 02_country_distribution.png
│   ├── 03_followers_vs_engagement.png
│   ├── 04_influence_score_dist.png
│   ├── 05_correlation_matrix.png
│   ├── 06_top_engagement.png
│   ├── 07_engagement_by_tier.png
│   ├── 08_posts_vs_likes.png
│   ├── 09_regression_results.png
│   ├── 10_feature_importance.png
│   ├── 11_confusion_matrix.png
│   └── 12_dashboard.png
└── README.md
```

## Methods

### Data Cleaning
- Converted string values (e.g., "475.8m") to numeric
- Handled 62 missing country values
- Filled missing engagement rates with median

### Feature Engineering
- `likes_per_follower`: Total engagement efficiency
- `likes_per_post`: Average content performance
- `avg_likes_pct`: Engagement as % of followers
- `eng_category`: Low/Medium/High classification

### Machine Learning
**Regression** (predicting influence score):
- Linear Regression
- Random Forest Regressor

**Classification** (predicting engagement level):
- Random Forest Classifier
- Achieved **75% accuracy**

## Visualizations

### Dashboard
![Dashboard](visualizations/12_dashboard.png)

### Top 15 by Followers
![Top Followers](visualizations/01_top15_followers.png)

### Engagement by Follower Tier
![Engagement Tiers](visualizations/07_engagement_by_tier.png)

### Correlation Matrix
![Correlations](visualizations/05_correlation_matrix.png)

## Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
```

## Usage

```bash
python analysis.py
```

This will:
1. Clean and process the data
2. Generate all visualizations
3. Train ML models
4. Output results to console
5. Save processed data and plots

## Insights for Brands

1. **Don't chase followers** - Higher follower counts don't guarantee better engagement
2. **Consider micro-influencers** - They often have more engaged audiences
3. **Look beyond USA** - Emerging markets offer untapped potential
4. **Check engagement rates** - More reliable metric than raw follower count

## Author

[Your Name]

## License

MIT
