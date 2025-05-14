# NFL Play Type Prediction Model
Overview
This project builds a machine learning model to predict whether a football play will be a run or pass based on pre-snap information. Using supervised learning techniques, the model analyzes various game situations and team tendencies to make its predictions.
Project Description
The goal is to build a K-Nearest Neighbors (KNN) classifier that can predict whether a team is going to run or pass the ball based on pre-snap information available in NFL gameplay data. This has practical applications for defensive coordinators and analysts who need to anticipate offensive play calls.
Data:

The data comes from the NFL Big Data Bowl 2025 competition and includes information such as:

Down and distance
Field position
Score differential
Quarter
Time remaining
Team passing tendencies
Receiver alignment
And more

Features Used:

After feature engineering and selection, the best model uses six key features:

yardsToGo - Distance needed for a first down

scoreDifferential - Point difference between teams

gameClock - Time remaining in the quarter

receivers - Number of receivers in the formation

passRate - Team's historical passing tendency

offenseFormation - Offensive formation being used

Model Performance
The final KNN model (k=10) achieves:

77.9% accuracy on the test set
71.7% accuracy on the larger validation set

The model performs better at predicting run plays (81% accuracy) compared to pass plays (57% accuracy).
Installation and Usage
python# Clone the repository
git clone https://github.com/yourusername/nfl-play-prediction.git
cd nfl-play-prediction

# Install required packages
pip install pandas numpy scikit-learn matplotlib seaborn

# Run the notebook
jupyter notebook AE3.ipynb
Methodology

Data Preprocessing

Clean and prepare play data
Handle missing values
Normalize features
Create additional derived features


Feature Selection

Test all possible feature subsets to find optimal combinations
Analyze feature importance
Select the six most predictive features


Model Training

Split data into training (1000 rows) and testing sets
Train K-Nearest Neighbors classifier
Optimize k value using cross-validation
Evaluate model performance


Model Evaluation

Confusion matrix analysis
Performance metrics assessment
Testing on large validation set



Future Improvements

Include more advanced features such as defensive alignments
Test ensemble methods to improve prediction accuracy
Add player-specific data to enhance model performance
Balance the model's performance between run and pass predictions

Author:

Everett Meehan - everettpmeehan@gmail.com


Data provided by the NFL Big Data Bowl 2025
Team tendency data from nfeloapp.com
