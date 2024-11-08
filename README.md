# AI-POWERED BEAUTY PRODUCT RECOMMENDATION SYSTEM
![product](https://github.com/user-attachments/assets/d370cd58-a84b-472c-afa3-ea13a3424085)


## Project Overview
This project focuses on building an AI-powered recommendation system for a variety of beauty products. While traditional recommendation systems tend to specialize in a single category, this project is designed to suggest a broad spectrum of products including skincare, haircare, supplements, perfumes, makeup, and more. This system aims to deliver personalized beauty recommendations that cater to users’ unique needs and preferences using advanced AI techniques.

### Key Features
- **Comprehensive Recommendations**: Combining content-based filtering (ingredient-based similarity), collaborative filtering (SVD), and sentiment analysis (LSTM and Sentiment Intensity Analyzer) to suggest products across various beauty categories.
- **User-Friendly Interface**: Deployed on Streamlit, where users can input their beauty needs to receive tailored product recommendations across multiple product types.
- **Diverse Target Audience**: Intended for a wide range of users with varied beauty needs and preferences, enabling personalized product suggestions across skin types, hair textures, fragrance preferences, and more.

---

## Problem Statement
The beauty industry offers an overwhelming selection of products, often leaving users unsure of which ones suit them best. This project aims to bridge this gap by developing an inclusive recommendation system that leverages advanced AI to provide targeted suggestions across a variety of beauty categories.

## Objectives
- **Develop** a recommendation system that covers multiple beauty product categories using AI and ML techniques.
- **Incorporate** content-based and collaborative filtering, as well as sentiment analysis, for comprehensive recommendations.
- **Deploy** an accessible Streamlit interface for easy-to-use, personalized beauty suggestions.

---

## Stakeholders
- **End Users**: Individuals seeking tailored recommendations across skincare, haircare, makeup, and other beauty products.
- **Beauty Brands**: Companies interested in reaching consumers with personalized product suggestions.
- **Retailers and Professionals**: Beauty experts and retailers looking to provide customized product advice.

---

## Data Description
The dataset used in this project was gathered via a Python-based web scraper, including a wide array of beauty products and user reviews.

1. **Product Data**:
   - **Beauty Products**: Data covering various beauty products from brands, with details on type, ingredients, ratings, and price.
   - **Main Features**: `product_id`, `product_name`, `category` (skincare, haircare, makeup, etc.), `brand_name`, `ingredients`, `rating`, `price`, `stock_status`.

2. **User Reviews**:
   - **Customer Feedback**: Reviews with insights into product effectiveness for various skin types, hair textures, and personal preferences.
   - **Main Features**: `author_id`, `rating`, `review_text`, `skin_type`, `hair_type`, `review_preferences`, `helpfulness`.

---

### Exploratory Data Analysis

#### 1. Count of Products by Skin Type
![Count of Products by Skin Type](https://github.com/ECCHERUIYOT/AI-Powered-Skincare-Recommendations-For-Melanin-Skin/blob/Echeruiyot/images/image1.png)

* The distribution shows that products labeled for combination skin are the most common, followed by those for dry, normal, and then oily skin. This insight can guide product selection based on prevalent skin types and consumer demand within the Black women demographic.

#### 2. Top 20 Recommended Products for Melanin Skin
![Top 20 Recommended Products for Melanin Skin](https://github.com/ECCHERUIYOT/AI-Powered-Skincare-Recommendations-For-Melanin-Skin/blob/Echeruiyot/images/image2.png)
* For melanated skin tones, there's a strong emphasis on gentle yet effective skincare products, with the top three recommendations focusing on hydration and sun protection.
* The Dew Dream Cleansing Balm leads the pack with about 55 recommendations, suggesting that gentle makeup removal is a priority for this skin type. The second most recommended product being the Signature Moisturizer, followed by the NA°39 Facial Sunscreen Mist with SPF 39, indicates that maintaining skin hydration and sun protection are crucial concerns for melanated skin. The prevalence of brightening, revitalizing, and gentle products in the top 10 (such as Absolue Soft Cream and Evercalm Gentle Cleansing Gel) suggests that users with melanated skin often seek products that address hyperpigmentation and sensitivity while maintaining skin barrier health.

* The list also includes several treatment-focused products like glycolic serums and exfoliators in the middle to lower rankings, indicating that while these are important, they're secondary to basic skin protection and hydration needs.

#### 3. Out of stock Products and Recommendations based on skin tone
![Out of stock Products and Recommendations based on skin tone](https://github.com/ECCHERUIYOT/AI-Powered-Skincare-Recommendations-For-Melanin-Skin/blob/Echeruiyot/images/image3.png)
* The Recommended pie chart illustrates the percentage of products recommended versus those that are not. A significant portion (85%) of products are not marked as recommended, indicating a possible quality or suitability gap. This could help identify where product performance might fall short or suggest a need for more tailored product options.

* The Products pie chart shows the balance between new and existing products. The larger percentage of existing products (91%) suggests that the platform maintains a consistent range of products, with newer items being introduced selectively. This distribution can provide insights into the inventory management and refresh rates of the catalog over time.

#### 4. Skin Tone Distribution by Price Tier
![skintone](https://github.com/user-attachments/assets/6e1279f0-3247-479c-adef-3549870ebdab)
* There is a noticeable price difference across skin tones. Products for melanated skin tend to have lower average prices, than non-melanated skin tones, highlighting more affordable options specifically formulated or suited for melanated skin. 

#### 5. Heatmap of Product Count by Skin Tone Category and Skin Type
![Heatmap of Product Count by Skin Tone Category and Skin Type](https://github.com/ECCHERUIYOT/AI-Powered-Skincare-Recommendations-For-Melanin-Skin/blob/Echeruiyot/images/image5.png)
* The heatmap analysis of skin_type and skin_tone_category highlights important insights that align closely with our objective of providing tailored skincare recommendations for women of color. Our data reveals a concentration of products available for combination and dry skin types, particularly within lighter skin tones. However, there is a notable scarcity of options for deeper skin tones, suggesting that women of color may have fewer product options specifically suited to their needs. This gap underscores the limited market focus on skincare for melanin-rich skin concerns, such as hyperpigmentation, dryness, and sensitivity, which are often more pronounced in deeper skin tones.

* These findings directly support our business problem: many existing recommendation systems fail to provide targeted solutions for melanated women. The evident lack of specialized options for drier skin in deeper tones emphasizes an opportunity to develop and recommend products that address this unique need. By prioritizing these underserved areas, our recommendation system can significantly enhance satisfaction and efficacy for women of color seeking products that work for their melanin-rich skin.

---

## Modeling Approach
We implemented a hybrid recommendation system that combines multiple techniques:

1. **Content-Based Filtering**: Calculates product similarity based on features and ingredients.
2. **Collaborative Filtering**: Uses Singular Value Decomposition (SVD) for insights into user-product interaction.
3. **Sentiment Analysis**: Employs LSTM and Sentiment Intensity Analyzer for scoring reviews, prioritizing highly-rated products across categories.
4. **Hybrid Model**: Merges all techniques to generate comprehensive and personalized recommendations.

### Evaluation
- **Precision**: Measures relevance of recommended products.
- **Recall**: Assesses how well recommendations align with user preferences.
- **F1-Score**: Balances precision and recall to improve recommendation accuracy.

---

## System Interface
The Streamlit application provides personalized product recommendations across a variety of beauty categories.

- *User Interface*: An intuitive interface where users can select options based on preferences (e.g., skincare, makeup, fragrance).
- *Recommendation Options*: Users receive product recommendations tailored to specific beauty needs or similar to products they already enjoy.
- *Modeling*: Content-based and collaborative filtering techniques (TF-IDF vectorization, SVD) power the recommendations.

![Home Page 1](https://github.com/user-attachments/assets/395f3d3f-a4fd-4b30-af33-3ad5a2865914)
![Home Page 2](https://github.com/user-attachments/assets/0937d7c3-367a-43ee-a93f-60c591faa849)
![Highlights](https://github.com/user-attachments/assets/66557dd3-55d7-4a59-a8a4-3f8445554fe6)
![Content-Based](https://github.com/user-attachments/assets/0e8ca50d-1371-48f9-9b0e-109d9245be16)

---

## Challenges and Solutions
- **Data Variety**: Diversity across beauty categories; addressed by expanding data sources.
- **Model Optimization**: Balancing performance required iterative fine-tuning.
- **Sentiment Analysis**: Ensuring accuracy by refining LSTM models for cross-category sentiment.

---

## Future Improvements
- **User Feedback Mechanism**: Integrate feedback loops for more refined recommendations.
- **Dataset Expansion**: Broaden product and review data across additional beauty brands.
- **Partnerships**: Collaborate with beauty professionals for validated recommendations.

