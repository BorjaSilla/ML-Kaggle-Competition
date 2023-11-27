# Predicting Airbnb Rental Prices with Machine Learning
![HEADER](https://i.imgur.com/eAembvm.png)


## Project Overview 🏡

The primary objective of this project is to predict the price of Airbnb listings based on various attributes. This predictive model serves as a valuable tool for hosts to set competitive prices, aiding in better decision-making. Additionally, guests can benefit from the analysis and predictions, aligning their expectations with actual pricing. The target variable for this project is the 'price' of the Airbnb rental.

## Data Overview 🔍

### The Data
The project utilizes several CSV files, with a focus on the 'train_data.csv.' Key features include:

- `first_review`: Date of the first review.
- `host_has_profile_pic`: Host profile picture availability (True/False).
- `host_identity_verified`: Host identity verification status (True/False).
- `host_response_rate`: Host response rate.
- `host_since`: Date the host joined Airbnb.
- `instant_bookable`: Property instant booking availability (T/F).
- `last_review`: Date of the last review.
- `latitude` and `longitude`: Geographical coordinates of the property.
- `name`: Property name.
- `neighborhood`: Neighborhood where the property is located.
- `number_of_reviews`: Total number of reviews.
- `review_scores_rating`: Overall score of reviews.
- `thumbnail_url`: URL of the thumbnail.
- `id`: Unique property identifier.
- `log_price`: Rental price in log format (Target Variable).
- `property_type`: Property type (e.g., apartment, house, etc.).
- `room_type`: Type of room (e.g., private room, entire apartment, etc.).
- `amenities`: Amenities offered at the property.
- `accommodates`: Maximum number of guests.
- `bathrooms`: Number of bathrooms.
- `bed_type`: Type of bed (e.g., double bed, sofa bed, etc.).
- `cancellation_policy`: Reservation cancellation policy.
- `cleaning_fee`: Cleaning fee charged (True/False).
- `city`: City where the property is located.
- `description`: Description of the property.

## Data Preprocessing ⚙️

### Handling Missing Values:
- Identified and addressed missing values, applying appropriate strategies for filling or handling them.

### Dropping Irrelevant Columns:
- Removed columns with a high number of missing values or those deemed irrelevant.
  - Example: Dropped columns such as 'first_review,' 'host_response_rate,' etc.

### Creating a New Column:
- Introduced a new feature, 'num_amenities,' counting the number of amenities an Airbnb has based on the existing 'amenities' column.

### Categorical and Numeric Features:
- Numeric Features: Standard scaling using StandardScaler().
- Categorical Features: One-hot encoding using OneHotEncoder.
- Utilized ColumnTransformer to streamline the preprocessing process.

### Train-Test Split:
- Split the data into a training set (80%) and a test set (20%).

### Random Forest Regression:
![GIF](https://img.genial.ly/6563719825d6360011948cf3/03175a3a-6083-4607-81cf-0f4fa8ef67bc.gif)
- Chose Random Forest Regression for its robustness, suitability for regression tasks, and effectiveness in capturing non-linear patterns.
- Achieved a RMSE of 0.4195 with this model.

## Test Data Preprocessing 🧹

- Filled missing values in 'bathrooms,' 'bedrooms,' and 'beds' columns with their respective medians.
- Transformed 'host_response_rate' to a float, removing the percentage symbol, and filled null values with the mean.
- Handled date data by filling missing values in 'first_review' and 'last_review' with a placeholder date of '1900-01-01.'
- Dropped irrelevant columns ('neighborhood,' 'thumbnail_url,' 'zipcode').
- Imputed missing values in categorical columns ('host_has_profile_pic' and 'host_identity_verified') with their respective modes.
- Filled missing values in 'review_scores_rating' and 'host_since' with the mean and mode, respectively.

### Model Evaluation 📊

- Applied the trained model to the clean test_data dataframe.
- Created a submission.csv for Kaggle evaluation.
- Achieved a Kaggle score of 0.4179, ranking #5 in the competition.
  
## Future Steps 🚀

- Explore different models and hyperparameters to further improve predictive accuracy.
- Continue refining the model for even more accurate pricing predictions.

Feel free to reach out for collaboration or any questions related to the project! 📧

[<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/480px-LinkedIn_logo_initials.png" width="30" height="30">](https://www.linkedin.com/in/borjasg)


