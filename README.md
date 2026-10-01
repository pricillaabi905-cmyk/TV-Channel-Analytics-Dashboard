# TV Channel Analytics Dashboard

An interactive Business Intelligence dashboard developed using Microsoft Power BI to analyze television channel performance, audience reach, viewer engagement, channel categories, and digital presence.

## Project Overview

The TV Channel Analytics Dashboard transforms television channel data into an interactive analytical solution using Microsoft Power BI.

The dashboard provides insights into channel performance, audience reach, ratings, subscription-related metrics, social media engagement, YouTube performance, and channel categories.

The project consists of three analytical dashboard pages:

- Overview
- Category & Channel
- Audience & Digital

Interactive slicers and cross-filtering allow users to explore the data dynamically.

## Objectives

- Analyze television channel performance
- Compare channel performance across categories
- Understand audience reach across languages
- Analyze viewer ratings and average viewership
- Examine subscription fee and viewer relationships
- Analyze social media and YouTube performance
- Study channel distribution by category
- Understand digital reach across different channel characteristics
- Present analytical findings through an interactive Power BI dashboard

## Tools and Technologies

| Technology | Purpose |
|---|---|
| Microsoft Power BI | Dashboard development and data visualization |
| Power Query | Data preparation and transformation |
| DAX | Measures and analytical calculations |
| Python | Data preprocessing and analysis |
| Pandas | Data manipulation |
| Jupyter Notebook | Exploratory data analysis |
| CSV | Dataset storage |
| GitHub | Version control and project documentation |

## Dataset

The project uses a TV Channel Analytics dataset containing information about television channels, categories, audience metrics, ratings, digital engagement, subscriptions, and channel characteristics.

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

The dataset was prepared before dashboard development through data cleaning, transformation, and validation.

The preparation process included:

1. Importing the raw dataset
2. Inspecting the dataset structure
3. Checking data types
4. Identifying missing values
5. Checking duplicate records
6. Standardizing data formats
7. Cleaning categorical fields
8. Validating numerical fields
9. Creating the cleaned dataset
10. Performing exploratory analysis
11. Loading the processed data into Power BI
12. Creating DAX measures
13. Developing interactive visualizations

## Dashboard Pages

### 1. Overview

The Overview page provides a high-level view of the television channel dataset.

#### Key Performance Indicators

- Total Channels
- Total Shows
- Average Viewers
- Average Rating
- Total Monthly Reach

#### Visualizations

- Top Channels by Average Viewers
- Audience Reach by Language
- Subscription Fee vs Average Viewers
- Average Viewers by Years Active
- Social Media Followers by Show Category

The page provides an overall understanding of audience performance, channel viewership, and digital engagement.

### 2. Category & Channel

The Category & Channel page focuses on channel distribution, category performance, audience reach, and ratings.

#### Key Performance Indicators

- Total Categories
- Top Channel Rating
- Average Subscription Fee
- Average Years Active
- HD Channel Percentage

#### Visualizations

- Channel Distribution by Category
- Average Rating by Channel Category
- Monthly Reach Breakdown
- Category Ranking by Average Rating
- Monthly Reach Contribution by Channel Category

This page enables comparison between channel categories and provides a detailed view of category-level performance.

### 3. Audience & Digital

The Audience & Digital page focuses on digital engagement and audience-related performance.

#### Key Performance Indicators

- Total Social Media Followers
- Total YouTube Views
- Total Likes
- Monthly Reach
- Average Subscription Fee

#### Visualizations

- Digital Engagement by Channel Category
- Channel-Level Digital Performance
- Digital Reach by Years Active

The page combines social media, YouTube, likes, ratings, and channel characteristics to provide a digital performance perspective.

## Interactive Filters

The dashboard provides interactive slicers for filtering and exploring the data.

Available filtering dimensions include:

- Language
- Channel Category
- Show Category
- Channel Name
- HD Availability

The slicers dynamically affect the relevant dashboard visuals and allow users to analyze specific channel segments.

## Key DAX Measures

### Total Channels

```DAX
Total Channels =
DISTINCTCOUNT('cleaned_tv_channel_dataset'[Channel_ID])
Total Shows
Total Shows =
SUM('cleaned_tv_channel_dataset'[No_of_Shows])

Average Viewers
Average Viewers =
AVERAGE('cleaned_tv_channel_dataset'[Avg_Viewers])

Average Rating
Average Rating =
AVERAGE('cleaned_tv_channel_dataset'[Avg_Rating])

Total Likes
Total Likes =
SUM('cleaned_tv_channel_dataset'[Total_Likes])

Total YouTube Views
Total YouTube Views =
SUM('cleaned_tv_channel_dataset'[YouTube_Views])

Total Monthly Reach
Total Monthly Reach =
SUM('cleaned_tv_channel_dataset'[Monthly_Reach])

Total Social Media Followers
Total Social Followers =
SUM('cleaned_tv_channel_dataset'[Social_Media_Followers])

Average Subscription Fee
Average Subscription Fee =
AVERAGE('cleaned_tv_channel_dataset'[Subscription_Fee])

Average Years Active
Average Years Active =
AVERAGE('cleaned_tv_channel_dataset'[Years_Active])

Total Categories
Total Categories =
DISTINCTCOUNT('cleaned_tv_channel_dataset'[Channel_Category])

Top Channel Rating
Top Channel Rating =
MAX('cleaned_tv_channel_dataset'[Avg_Rating])

HD Channel Percentage
HD Channel % =
DIVIDE(
    CALCULATE(
        DISTINCTCOUNT('cleaned_tv_channel_dataset'[Channel_ID]),
        'cleaned_tv_channel_dataset'[HD_Available] = "Yes"
    ),
    DISTINCTCOUNT('cleaned_tv_channel_dataset'[Channel_ID])
)

Dashboard Features
- Interactive dashboard navigation
- KPI cards
- Interactive slicers
- Cross-filtering
- Channel-level analysis
- Category-level analysis
- Audience analysis
- Digital performance analysis
- Rating analysis
- Subscription analysis
- Professional dashboard layout
- Consistent visual formatting
Analytical Areas
The dashboard allows users to explore relationships between:
- Channel categories and audience reach
- Languages and audience reach
- Subscription fees and average viewers
- Channel categories and ratings
- Years active and digital reach
- Show categories and social media followers
- Channel categories and digital engagement
- Individual channels and their digital performance
Repository Structure
TV-Channel-Analytics-Dashboard/
│
├── TV-Channel-Analytics-Dashboard.pbix
├── TV_Channel_Analytics.ipynb
├── TV_channel_dataset.csv
├── cleaned_tv_channel_dataset.csv
└── README.md

How to Use
1. Clone or download the repository.
2. Open TV-Channel-Analytics-Dashboard.pbix using Microsoft Power BI Desktop.
3. Ensure the dataset path is correctly configured if required.
4. Refresh the data.
5. Navigate between the dashboard pages.
6. Use the available slicers to filter the data.
7. Interact with the visualizations to explore channel, audience, and digital performance.
Skills Demonstrated
- Data Cleaning
- Data Transformation
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
Project Type
Data Analytics | Business Intelligence | Data Visualization | Power BI
Author
Pricilla G
B.Tech in Artificial Intelligence and Data Science
Conclusion
The TV Channel Analytics Dashboard demonstrates the application of Business Intelligence techniques to television channel data.
The project combines data preparation, exploratory analysis, DAX calculations, and interactive Power BI visualizations to provide insights into channel performance, audience reach, ratings, subscriptions, and digital engagement.
The dashboard provides a structured and interactive approach to exploring television channel analytics and can be further extended with real-time data integration, predictive analytics, and advanced machine learning techniques.

This version is based on the **actual visuals, pages, KPIs, and slicers inside your uploaded PBIX**, so it avoids claiming dashboard elements that you haven't actually built.
