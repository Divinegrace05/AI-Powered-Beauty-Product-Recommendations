# AI POWERED BEAUTY PRODUCTS RECOMMENDATION SYSTEM

![product](https://github.com/user-attachments/assets/ac674706-9096-4118-884b-4edd476499c8)

## Project Overview
This project focuses on creating an AI-powered recommendation system to address a key gap in the skincare industry: the lack of personalized product recommendations for women of color. This demographic often has unique skincare needs—like managing hyperpigmentation, sensitivity, and hydration—yet current solutions frequently offer generalized recommendations that fail to consider these specific concerns. Our solution aims to fill this gap by providing tailored skincare recommendations using AI models optimized for melanin-rich skin.

### Key Features
- **Personalized Recommendations**: Utilizing a combination of content-based filtering (ingredient-based similarity), collaborative filtering (SVD), and sentiment analysis (LSTM and Sentiment Intensity Analyzer).
- **User-Friendly Interface**: Deployed on Streamlit, enabling users to enter their skincare needs and receive personalized product suggestions.
- **Targeted for Melanin-Rich Skin**: Specifically focused on concerns like hyperpigmentation, dryness, and sensitivity that are more prevalent among women of color.

---

## Problem Statement
Despite the growing demand for skincare products among women of color, most recommendation systems lack specificity in addressing concerns unique to melanin-rich skin. This project aims to bridge this gap by developing an inclusive recommendation system that leverages advanced AI techniques to provide targeted skincare solutions.

## Objectives
- **Develop** a recommendation system for melanin-rich skin using AI and ML techniques.
- **Incorporate** content-based and collaborative filtering, as well as sentiment analysis, for accurate recommendations.
- **Deploy** an accessible Streamlit interface for easy-to-use, personalized skincare suggestions.

---

## Stakeholders
- **End Users**: Women of color seeking skincare products tailored to their specific needs.
- **Skincare Brands**: Companies interested in reaching this demographic more effectively.
- **Healthcare Professionals**: Dermatologists who may use the system as a tool for recommending products suited to melanin-rich skin.

---

## Data Description
The dataset used was collected via a Python-based web scraper and includes the following key elements:

1. **Product Data**: 
   - Over 8,000 skincare products from the Sephora online store, including details on brand, ingredients, rating, price, and stock availability.
   - Main Features: `product_id`, `product_name`, `brand_name`, `ingredients`, `rating`, `price_ksh`, `new`, `out_of_stock`, `highlights`.

2. **User Reviews**:
   - About 1 million reviews covering over 2,000 products in the skincare category, with details on user skin type, skin tone, and review ratings.
   - Main Features: `author_id`, `rating`, `review_text`, `skin_type`, `skin_tone`, `helpfulness`.

---

## Exploratory Data Analysis (EDA)
### Product Distribution by Skin Type
![download](https://github.com/user-attachments/assets/afdbd9db-19a8-44db-803a-5741efe0c067)
- The majority of products are labeled for combination skin, with fewer options for other types, guiding our recommendations for underserved demographics.

### Top Recommended Products for Melanin-Rich Skin
![download](https://github.com/user-attachments/assets/8946f8fa-8448-4107-a84e-03e661bd4b6c)
- Highlights top products for hyperpigmentation and hydration, addressing unique needs of women with melanin-rich skin.

### Heatmap of Product Count by Skin Tone and Skin Type
![download](https://github.com/user-attachments/assets/85e65e5a-60de-4f85-8d36-bbc1aa258743)
- Reveals a shortage of options for deeper skin tones, underlining the need for tailored skincare products.

---

## Modeling Approach
We used a hybrid recommendation system combining the following techniques:

1. **Content-Based Filtering**: Calculates product similarity based on ingredients using cosine similarity.
2. **Collaborative Filtering**: Utilizes Singular Value Decomposition (SVD) for user-product interaction patterns.
3. **Sentiment Analysis**: Employs an LSTM model and Sentiment Intensity Analyzer to score reviews, prioritizing highly-rated products.
4. **Hybrid Model**: Merges all techniques to deliver robust, personalized recommendations.

### Evaluation
- **Precision**: Measures the relevance of the recommended products.
- **Recall**: Evaluates how well the recommendations capture the user’s preferences.
- **F1-Score**: Balances precision and recall to optimize recommendation accuracy.

---

## System Interface
The Streamlit app provides a simple, intuitive way for users to receive tailored skincare suggestions. Users input a product name or skin concern, and the app generates a list of recommended products based on their profile.
![Home Page 1](https://github.com/user-attachments/assets/8f989d6e-5e7f-4f97-b2a1-51e21c5642c3)
![Home Page 2](https://github.com/user-attachments/assets/5ab64f1a-9dd4-43cc-a055-3bf57ba4d170)
![Highlights](https://github.com/user-attachments/assets/d07323a0-4f0d-4ffe-9c60-46bad479b709)
![Content-Based](https://github.com/user-attachments/assets/62827675-c0e2-4fe1-86a5-96012e91e61a)


---

## Challenges and Solutions
- **Data Limitations**: The dataset has limited diversity across brands, which we addressed by augmenting product features and expanding review sources.
- **Model Optimization**: Balancing model performance in the hybrid approach required iterative fine-tuning.
- **Sentiment Analysis**: Ensuring accurate sentiment classification was critical; challenges in NLP were addressed by refining the LSTM model.

---

## Future Improvements
- **User Feedback Mechanism**: Incorporate feedback loops to allow users to rate recommendations, improving system accuracy.
- **Dataset Expansion**: Increase the range of brands and product types to enhance recommendation quality.
- **Partnerships**: Collaborate with skincare experts and dermatologists for validation and expanded reach.

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
2. Install required packages:
    ```bash
    pip install -r requirements.txt

### Usage
To start the Streamlit application:
    ```bash
    streamlit run skincareApp.py


## Repository Navigation

This repository is structured to facilitate easy navigation and organization of files, datasets, scripts, and notebooks related to the AI-Powered Beauty Products Recommendation System project.

### Directory Structure

- **`data/`**: Contains the datasets used in this project. This includes both raw and processed data files that support the recommendation system and model training.
- **`notebooks/`**: Jupyter notebooks for exploratory data analysis (EDA) and model training. Each notebook is organized to showcase various stages of analysis and model development.
- **`models/`**: Contains saved machine learning models used in this project. These are ready-to-use models trained on the provided dataset.
- **`scripts/`**: Python scripts that handle data preprocessing, feature engineering, and model evaluation. The scripts are modular to allow for easy adjustments and scaling.
- **`app.py`**: The main Streamlit application file. This file runs the application, providing users with an interface to receive skincare product recommendations based on their inputs.
- **`requirements.txt`**: Contains a list of all packages and dependencies required for the project. This file can be used to set up a virtual environment with the necessary libraries.

---

### Files and Scripts

- **`app.py`**: This is the primary file to run the Streamlit application. Launch this file using `streamlit run app.py` to access the recommendation system interface.
- **`requirements.txt`**: Lists all dependencies required to run the project, ensuring that the environment is correctly set up. Install dependencies with `pip install -r requirements.txt`.
- **`EDA_notebook.ipynb`**: This Jupyter notebook contains the exploratory data analysis (EDA), where we explore patterns, relationships, and insights within the dataset.
- **`Modeling_notebook.ipynb`**: This notebook covers machine learning model training and evaluation, detailing the models used in the recommendation system and their respective performance metrics.

---

Thank you for exploring the AI-Powered Beauty Products Recommendation System! This project is dedicated to inclusivity in the beauty industry by providing skincare recommendations specifically designed for melanin-rich skin.
