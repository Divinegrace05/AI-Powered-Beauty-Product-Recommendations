# AI-POWERED BEAUTY PRODUCTS RECOMMENDATION SYSTEM

![product](https://github.com/user-attachments/assets/ac674706-9096-4118-884b-4edd476499c8)

## Project Overview
This project introduces an AI-powered recommendation system for diverse beauty products tailored to users’ individual preferences and needs. The system spans multiple categories—skincare, haircare, makeup, supplements, perfumes, and more—providing comprehensive and personalized recommendations. By incorporating various recommendation techniques and leveraging user reviews, this project aims to offer a unique, all-encompassing experience for beauty enthusiasts.

### Key Features
- **Comprehensive Beauty Recommendations**: Uses a hybrid approach of content-based filtering, collaborative filtering, and sentiment analysis to generate personalized product suggestions across multiple beauty categories.
- **User-Friendly Interface**: A Streamlit app allows users to easily input their beauty needs and preferences to receive tailored recommendations.
- **Inclusive of Various Beauty Needs**: While initially focused on melanin-rich skincare, this system has evolved to recommend products for a broader range of users and beauty needs.

---

## Problem Statement
Beauty product recommendation systems are often limited to specific categories, failing to address the varied and personalized needs of beauty consumers. This project bridges that gap, enabling an inclusive recommendation system covering a wide range of beauty products based on individual needs, preferences, and reviews.

## Objectives
- **Develop** a recommendation system for multiple beauty product categories using advanced AI and ML techniques.
- **Incorporate** a hybrid model that combines content-based, collaborative filtering, and sentiment analysis for accurate and comprehensive recommendations.
- **Deploy** an accessible Streamlit app that provides easy-to-use, personalized recommendations across diverse beauty needs.

---

## Stakeholders
- **End Users**: Individuals seeking personalized beauty product recommendations.
- **Beauty Brands**: Companies aiming to better target and reach customers with personalized experiences.
- **Healthcare and Beauty Professionals**: Dermatologists, cosmetologists, and wellness experts who may find this tool useful for recommending suitable products.

---

## Data Description
The dataset includes a variety of product categories, sourced via a Python-based web scraper and other datasets covering the following elements:

1. **Product Data**: 
   - A diverse range of beauty products (over 10,000) from multiple categories, including skincare, haircare, supplements, makeup, and fragrances, with details on brand, ingredients, rating, price, and availability.
   - Main Features: `product_id`, `product_name`, `category`, `brand_name`, `ingredients`, `rating`, `price`, `stock_status`, `highlights`.

2. **User Reviews**:
   - Over 1 million reviews covering products across different beauty categories, detailing users’ needs and preferences, such as skin type, hair type, review ratings, and purchase intent.
   - Main Features: `author_id`, `rating`, `review_text`, `beauty_concern`, `helpfulness`.

---

## Exploratory Data Analysis (EDA)
### Product Distribution by Category
- Displays the distribution of products across various beauty categories, such as skincare, haircare, and makeup.

### Top Recommended Products Across Beauty Categories
- Highlights top products for common beauty concerns, addressing the unique needs of users across skincare, haircare, and supplements.

### Heatmap of Product Count by Beauty Concern and Category
- Reveals product availability and variety across different beauty concerns, underscoring the importance of tailored recommendations.

---

## Modeling Approach
The project employs a hybrid recommendation system that includes the following techniques:

1. **Content-Based Filtering**: Calculates product similarity based on ingredients, features, and category using cosine similarity.
2. **Collaborative Filtering**: Utilizes Singular Value Decomposition (SVD) for user-product interaction patterns.
3. **Sentiment Analysis**: Analyzes product reviews using an LSTM model and Sentiment Intensity Analyzer, helping prioritize products with positive feedback.
4. **Hybrid Model**: Combines these methods to deliver well-rounded, personalized recommendations.

### Evaluation
- **Precision**: Measures the relevance of the recommended products.
- **Recall**: Evaluates how well the recommendations align with users' preferences.
- **F1-Score**: Balances precision and recall for optimized recommendation quality.

---

## System Interface
The Streamlit app offers an intuitive interface for users to input their preferences and receive tailored recommendations for a wide variety of beauty products.

---

## Challenges and Solutions
- **Data Diversity**: The dataset initially lacked variety across product types, addressed by expanding product categories and diversifying sources.
- **Model Optimization**: Iterative tuning was necessary to balance performance in the hybrid model.
- **Sentiment Analysis**: Improved sentiment classification accuracy by refining the LSTM model to better interpret user reviews.

---

## Future Improvements
- **User Feedback**: Integrate a feedback mechanism allowing users to rate recommendations, enhancing model accuracy.
- **Dataset Expansion**: Broaden product categories and brands to increase recommendation quality.
- **Collaborations**: Partner with beauty experts to refine recommendations and expand system reach.

---

## Getting Started
To run this project locally, follow these steps:

### Prerequisites
- Python 3.8 or higher
- Libraries: `pandas`, `numpy`, `scikit-learn`, `nltk`, `tensorflow`, `streamlit`, `cosine-similarity`

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Divinegrace05/AI-powered-Beauty-Product-Recommendations.git
   cd AI-powered-Beauty-Product-Recommendations
   ```
2. Install required packages:
    ```bash
    pip install -r requirements.txt
    ```

### Usage
To start the Streamlit application:
   ```bash
   streamlit run app.py
   ```

---

### Repository Structure

- **`data/`**: Contains datasets used in this project for various beauty products.
- **`notebooks/`**: Jupyter notebooks with EDA and model training steps.
- **`models/`**: Stores saved machine learning models for product recommendation.
- **`scripts/`**: Scripts for data preprocessing, feature engineering, and evaluation.
- **`app.py`**: The main Streamlit application file.
- **`requirements.txt`**: Lists dependencies for the project.

---

Thank you for exploring the AI-Powered Beauty Products Recommendation System! This project strives to provide an inclusive, customized beauty recommendation experience across a wide variety of products.

---

For Jupyter Notebook markdowns, here’s a suggested structure for each section:

1. **Introduction**:
   - Briefly introduce the expanded recommendation system and its purpose in providing diverse beauty recommendations.

2. **Exploratory Data Analysis (EDA)**:
   - Describe the analysis of product distributions, review sentiment, and patterns by category (e.g., makeup, haircare).
   - Add visuals that showcase distribution across multiple beauty categories, along with any insights on product availability by need.

3. **Modeling Section**:
   - Explain the use of a hybrid model combining content-based, collaborative filtering, and sentiment analysis.
   - Include subsections for each method with concise explanations.

4. **Results and Evaluation**:
   - Discuss evaluation metrics for the overall model and any category-specific insights.
   - Summarize the performance of each component and highlight the strengths of the hybrid approach in producing relevant beauty recommendations.

This revision will help align the README and notebook content with your project's broader scope and beauty focus. Let me know if there’s any specific markdown content you’d like more detail on!
