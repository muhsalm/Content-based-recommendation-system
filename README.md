# Movie Recommendation System

## Capstone Project by Muhammad Saad Salman

### Table of Contents
- [Introduction](#introduction)
- [Business Problem](#business-problem)
- [Stakeholders](#stakeholders)
- [Datasets](#datasets)
- [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Modeling and Evaluation](#modeling-and-evaluation)
- [Deployment](#deployment)
- [Conclusions](#conclusions)
- [Future Work](#future-work)

## Introduction
With the rapid growth of the streaming industry, users are faced with an overwhelming amount of content to choose from. This project aims to build a **Content-Based Movie Recommendation System** to help users find movies that match their tastes, thereby improving user satisfaction and retention.

## Business Problem
- **Decision Fatigue:** Users are overwhelmed by the sheer volume of available content.
- **Poor Engagement:** Difficulty in finding relevant content leads to user frustration and reduced engagement.
- **Retention Issues:** Users may leave the platform due to poor content discovery, necessitating the need for an effective recommendation system.

## Stakeholders
- **Users:** Seek personalized movie recommendations.
- **Platform Owners:** Aim to increase user engagement and retention.
- **Content Creators:** Want their content recommended to relevant audiences.
- **Advertisers:** Interested in targeting specific user segments.
- **Data Analysts:** Responsible for optimizing the recommendation system's accuracy.

## Datasets
The data was sourced from the **Kaggle TMDb Movie Metadata dataset**, containing information on approximately 5000 to 10000 movies. Key attributes include:
- `id`
- `original_title`
- `genres`
- `keywords`
- `tagline`
- `cast`
- `crew`

## Data Cleaning and Preprocessing
- **Missing Values:** Rows with missing values were dropped to ensure a clean dataset.
- **String Conversion:** Columns such as `genres`, `keywords`, `cast`, and `crew` were converted to string format for compatibility with the recommendation system.
- **Column Selection:** Only the top 3 actors from the `cast` column and the director from the `crew` column were selected.

## Feature Engineering
- **Feature Combination:** The `genres`, `overview`, `keywords`, `cast`, and `crew` columns were combined into a new column `combined_features`.
- **Text Vectorization:** The `combined_features` column was transformed into numerical vectors using TF-IDF Vectorization.

## Modeling and Evaluation
- **Model Used:** Nearest Neighbors model using cosine similarity was employed to recommend movies.
- **Outcome:** The system was able to provide accurate movie recommendations based on different search criteria such as genre, title, keyword, and production company.

## Deployment
The recommendation system was deployed locally using **Streamlit**. Initially, it displayed only the names of recommended movies. The system was later enhanced by integrating the **TMDB API** to fetch and display movie posters alongside titles, improving visual appeal and user engagement.

## Conclusions
This content-based movie recommendation system effectively helps users navigate through the vast amount of available content, thereby enhancing user satisfaction and platform engagement.

## Future Work
- **Hybrid Approach:** Implementing a hybrid system that combines collaborative filtering with content-based methods to further improve recommendation accuracy.
- **User Feedback Integration:** Enhancing the model by incorporating user feedback to refine recommendations.

