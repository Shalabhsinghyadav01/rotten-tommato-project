
# Movie Review Classification Project


## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model](#model)
- [Evaluation](#evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## overview
This project involves building a high-performing classification algorithm to predict whether a particular movie on Rotten Tomatoes is labeled as ‘Rotten’, ‘Fresh’, or ‘Certified-Fresh’. The dataset used in this project is sourced from Rotten Tomatoes, a popular online review aggregator for film and television.
## Dataset
There are 2 datasets

1. rotten_tomatoes_movies.csv - contains basic information about each movie listed on Rotten Tomatoes; each row represents one movie;
2. rotten_tomatoes_critic_reviews_50k.tsv - contains 50.000 individual reviews by Rotten Tomatoes critics; each row represents one review corresponding to a movie;
**`rotten_tomatoes_movies`** dataset contains the following columns:
- **`rotten_tomatoes_link`** - movie ID
- **`movie_title`** - title of the movie as displayed on the Rotten Tomatoes website
- **`movie_info`** - brief description of the movie
- **`critics_consensus`** - comment from Rotten Tomatoes
- **`content_rating`** - category based on the movie suitability for audience
- **`genres`** - movie genres separated by commas, if multiple
- **`directors`** - name of director(s)
- **`authors`** - name of author(s)
- **`actors`** - name of actors
- **`original_release_date`** - date in which the movie has been released in theatres, in YYYY-MM-DD format
- **`streaming_release_date`** - date in which the movie has been released on streaming platforms, in YYYY-MM-DD format
- **`runtime`** - duration of the movie in minutes
- **`production_company`** - name of a studio/company that produced the movie
- **`tomatometer_status`** - a label assigned by Rotten Tomatoes: "Fresh", "Certified-Fresh" or "Rotten"; **this is the target variable in this challenge**
- **`tomatometer_rating`** - percentage of positive critic ratings
- **`tomatometer_count`** - critic ratings counted for the calculation of the tomatometer status
- **`audience_status`** - a label assigned based on user ratings: "Spilled" or "Upright"
- **`audience_rating`** - percentage of positive user ratings
- **`audience_count`** - user ratings counted for the calculation of the audience status
- **`tomatometer_top_critics_count`** - number of ratings by top critics
- **`tomatometer_fresh_critics_count`** - number of critic ratings labeled "Fresh"
- **`tomatometer_rotten_critics_count`** - number of critic ratings labeled "Rotten"
`rotten_tomatoes_critic_reviews_50k` dataset contains the following columns:

- **`rotten_tomatoes_link`** - movie ID
- **`critic_name`** - name of critic who rated the movie
- **`top_critic`** - boolean value that clarifies whether the critic is a top critic or not
- **`publisher_name`** - name of the publisher for which the critic works
- **`review_type`** - was the review labeled "Fresh" or "Rotten"?
- **`review_score`** - review score provided by the critic
- **`review_date`** - date of the review in YYYY-MM-DD format
- **`review_content`** - text of the review
## Features

- Text Vectorization using CountVectorizer and TfidfVectorizer
- Model Training using Random Forest Classifier
- Handling class imbalance with class weights
- Model evaluation with accuracy score, classification report, and confusion matrix


## Installation

To run this project, you need to have Python installed along with the following libraries:
libraries:

- pandas
- scikit-learn
- seaborn
- matplotlib
You can install the required libraries using:

```bash
 pip install pandas scikit-learn seaborn matplotlib
```
    
## Usage

1.	Clone the repository:
```bash
https://github.com/Shalabhsinghyadav01/rotten-tommato-project.git
cd movie-review-classification
```

2.	Load the dataset:
- Ensure your dataset file is named rotten_tomatoes.csv,rotten_tomatoes_critic_reviews_50k.csv and placed in the project directory.
3.	Run the classification script:
- Modify the script to point to your dataset file if needed.
- execute the script 
```bash
python classify_reviews.py
```
## Model
The core of the project is a Random Forest Classifier that has been fine-tuned to handle imbalanced classes effectively. Text data is vectorized using CountVectorizer and TfidfVectorizer before being fed into the model.

Key Steps:
1.	Data Preprocessing: Handling missing values, encoding categorical variables, and extracting relevant components from date fields.
2.	Text Vectorization: Converting textual data into numerical vectors.
3.	Model Training: Training a Random Forest model with balanced class weights.
4.	Evaluation: Assessing model performance using accuracy score, classification report, and confusion matrix.

## evaluation
Model performance is evaluated using:
- **Accuracy Score**: Measures the overall accuracy of the model.
- **Classification Report**: Provides detailed metrics such as precision, recall, and F1-score for each class.
- **Confusion Matrix**: Visual representation of the model’s performance in distinguishing between different classes.

## result
The model achieves high accuracy in predicting the ‘Rotten’, ‘Fresh’, and ‘Certified-Fresh’ labels. The detailed classification report and confusion matrix help in understanding the strengths and weaknesses of the model.

0.9929494712103408
        
         precision    recall  f1-score   support

         0.0       1.00      1.00      1.00      1488
         1.0       0.99      0.99      0.99      1286
         2.0       0.98      0.98      0.98       630

    accuracy                           0.99      3404
    macro avg       0.99      0.99      0.99      3404
    weighted avg       0.99      0.99      0.99      3404
## Contributing

Contributions are always welcome!
Contributions are welcome! If you have suggestions or improvements, please create a pull request or open an issue.


## License

This project is licensed under the MIT License. See the [license](https://github.com/Shalabhsinghyadav01/rotten-tommato-project/blob/main/LICENSE) file for more details.


## contact
If you have any questions or want to discuss the project, feel free to reach out:
- **Name**: Shalabh Singh Yadav
- **Email**: [shalabhsinghyadav@gmail.com](mailto:shalabhsinghyadav@gmail.com)
- **LinkedIn**: [LinkedIn Profile](https://www.linkedin.com/in/shalabh-singh-yadav-66b607204/)