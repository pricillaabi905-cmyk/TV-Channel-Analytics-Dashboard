# TV Channel Analytics Dashboard

An interactive Business Intelligence dashboard developed using Microsoft Power BI to analyze television channel performance, audience reach, viewer engagement, subscription trends, and digital presence.

## Project Overview

The TV Channel Analytics Dashboard transforms raw TV channel data into meaningful and interactive visual insights.

The project focuses on analyzing channel performance across different categories, languages, show categories, audience metrics, subscription fees, and digital platforms.

The dashboard provides an interactive environment where users can explore channel performance, compare different segments, and identify important patterns in the dataset.

## Objectives

- Analyze overall TV channel performance
- Compare channels across different categories and languages
- Analyze audience reach and viewer engagement
- Study social media and YouTube performance
- Analyze subscription fees and viewer performance
- Examine HD availability across channel categories
- Identify patterns in ratings, viewership, and digital engagement
- Develop an interactive and user-friendly Power BI dashboard
- Present complex data through clear and meaningful visualizations

## Tools and Technologies

| Technology | Purpose |
|---|---|
| Microsoft Power BI | Dashboard development and data visualization |
| Power Query | Data cleaning and transformation |
| DAX | Measures and analytical calculations |
| Python | Data preprocessing and analysis |
| Pandas | Data manipulation |
| Jupyter Notebook | Exploratory data analysis |
| CSV | Dataset storage |
| GitHub | Version control and project documentation |

## Dataset

The project uses a TV Channel Analytics dataset containing information about television channels, shows, audience metrics, ratings, subscriptions, and digital engagement.

### Dataset Attributes

- Channel ID
- Channel Name
- Channel Category
- Show Category
- Language
- Number of Shows
- Average Viewers
- Average Rating
- Total Likes
- Social Media Followers
- YouTube Views
- HD Availability
- Subscription Fee
- Monthly Reach
- Years Active

## Data Preparation

The dataset was prepared before dashboard development using the following process:

1. Imported the raw dataset
2. Inspected the dataset structure
3. Checked for missing values
4. Identified duplicate records
5. Standardized data formats
6. Cleaned categorical fields
7. Validated numerical columns
8. Checked data consistency
9. Created the cleaned dataset
10. Performed exploratory data analysis
11. Loaded the processed dataset into Power BI
12. Created DAX measures
13. Developed interactive visualizations

## Dashboard Structure

### Overview

The Overview page provides a high-level summary of the TV channel dataset.

#### Key Performance Indicators

- Total Channels
- Total Shows
- Average Viewers
- Average Rating
- Total Monthly Reach

#### Visualizations

- Top 10 Channels by Average Viewers
- Audience Reach by Language
- Subscription Fee vs Average Viewers
- YouTube Views by Show Category
- Average Viewers by Years Active
- HD Availability by Channel Category
- Social Media Followers by Show Category

### Category and Channel

This page focuses on channel categories, channel performance, subscription information, and audience reach.

#### Key Performance Indicators

- Total Categories
- Top Channel Rating
- Average Subscription Fee
- Average Years Active
- HD Channel Percentage

#### Visualizations

- Monthly Reach Breakdown
- Category Ranking by Average Rating
- Monthly Reach Contribution by Channel Category

### Audience and Digital

This page focuses on audience engagement and digital performance.

#### Key Performance Indicators

- Total Social Media Followers
- Total YouTube Views
- Total Likes
- Monthly Reach
- Average Subscription Fee

#### Analysis

- Social Media Followers vs YouTube Views
- Digital Performance by Channel Category
- YouTube Views by Language
- Channel-Level Digital Performance

## Interactive Filters

The dashboard includes interactive filters that allow users to explore different segments of the dataset.

- Language
- Channel Category
- Show Category
- HD Availability

These filters dynamically update the dashboard visualizations based on the selected values.

## Key DAX Measures

### Total Channels

```DAX
Total Channels =
DISTINCTCOUNT('cleaned_tv_channel_dataset'[Channel_ID])
```

### Total Shows

```DAX
Total Shows =
SUM('cleaned_tv_channel_dataset'[No_of_Shows])
```

### Average Viewers

```DAX
Average Viewers =
AVERAGE('cleaned_tv_channel_dataset'[Avg_Viewers])
```

### Average Rating

```DAX
Average Rating =
AVERAGE('cleaned_tv_channel_dataset'[Avg_Rating])
```

### Total Likes

```DAX
Total Likes =
SUM('cleaned_tv_channel_dataset'[Total_Likes])
```

### Total YouTube Views

```DAX
Total YouTube Views =
SUM('cleaned_tv_channel_dataset'[YouTube_Views])
```

### Total Monthly Reach

```DAX
Total Monthly Reach =
SUM('cleaned_tv_channel_dataset'[Monthly_Reach])
```

### Total Social Media Followers

```DAX
Total Social Followers =
SUM('cleaned_tv_channel_dataset'[Social_Media_Followers])
```

### Average Subscription Fee

```DAX
Average Subscription Fee =
AVERAGE('cleaned_tv_channel_dataset'[Subscription_Fee])
```

### Average Years Active

```DAX
Average Years Active =
AVERAGE('cleaned_tv_channel_dataset'[Years_Active])
```

### Total Categories

```DAX
Total Categories =
DISTINCTCOUNT('cleaned_tv_channel_dataset'[Channel_Category])
```

### Top Channel Rating

```DAX
Top Channel Rating =
MAX('cleaned_tv_channel_dataset'[Avg_Rating])
```

### HD Channel Percentage

```DAX
HD Channel % =
DIVIDE(
    CALCULATE(
        DISTINCTCOUNT('cleaned_tv_channel_dataset'[Channel_ID]),
        'cleaned_tv_channel_dataset'[HD_Available] = "Yes"
    ),
    DISTINCTCOUNT('cleaned_tv_channel_dataset'[Channel_ID])
)
```

## Dashboard Design

The dashboard follows a clean and professional visual design with a consistent teal and green color palette.

### Design Features

- Interactive page navigation
- KPI cards
- Interactive slicers
- Cross-filtering
- Category-level analysis
- Channel-level analysis
- Audience analytics
- Digital performance analytics
- Consistent typography and formatting
- User-friendly layout

## Key Analysis Areas

The dashboard enables analysis of relationships between:

- Channel categories and audience reach
- Languages and monthly reach
- Subscription fees and average viewers
- Show categories and YouTube views
- Years active and viewer performance
- Channel categories and HD availability
- Social media followers and digital engagement
- Channel ratings and category performance

## Repository Contents

The repository contains the following project files:

- Power BI dashboard file
- TV Channel Analytics Jupyter Notebook
- Original TV channel dataset
- Cleaned TV channel dataset
- Project documentation

## How to Use

1. Clone or download this repository.
2. Open the Power BI dashboard file using Microsoft Power BI Desktop.
3. If required, update the dataset file path.
4. Refresh the data.
5. Navigate between the dashboard pages.
6. Apply the available filters.
7. Interact with the visualizations to explore channel, audience, and digital performance.

## Skills Demonstrated

- Data Cleaning
- Data Preprocessing
- Exploratory Data Analysis
- Data Visualization
- Business Intelligence
- Microsoft Power BI
- Power Query
- DAX
- Python
- Pandas
- Dashboard Development
- Dashboard Design
- Data Analysis
- Interactive Reporting
- Git and GitHub

## Project Type

Data Analytics | Business Intelligence | Data Visualization | Power BI

## Author

**Pricilla G**

B.Tech in Artificial Intelligence and Data Science

## Conclusion

The TV Channel Analytics Dashboard demonstrates how raw television channel data can be transformed into an interactive Business Intelligence solution.

By combining data preparation, exploratory analysis, DAX calculations, and Power BI visualizations, the project provides a structured approach to analyzing channel performance, audience reach, viewer engagement, and digital presence.

The project can be further enhanced by integrating real-time data sources, additional audience metrics, predictive analytics, and machine learning techniques.
