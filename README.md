# Predicting-Movie-Genres-from-Plot-Summaries

## Overview:
This goal of this project was to train a model to guess movie genres based on their plot summaries. 

## Data:
This ![data](https://www.cs.cmu.edu/~ark/personas/) was collected by the Language Technologies Institute and Machine Learrning Department at Carnegie Mellon University. It consists of 42,306 movie plot summaries, genres, tv tropes, titles, and character names. I chose to focus on the summaries and the genres. Each movie had between 1 and 7 assigned genres, and there were 363 genres in total. 
![Example of the data-summaries]<img width="760" alt="metadata" src="https://user-images.githubusercontent.com/79812486/126675435-eb17ac6e-ca2b-4bfa-8b28-89269cedda70.png">
![Example of the data-details]<img width="763" alt="Screen Shot 2021-07-21 at 11 39 16 PM" src="https://user-images.githubusercontent.com/79812486/126675520-9d448d9b-f6b8-4fb7-bc98-1c23eccfe577.png">


## Exploratory Data Analysis:
For EDA, I combined the multiple datasets, checked for missing values, labeled and separated the information intoo columns, and tried some plotting. 
![Top Genres](https://user-images.githubusercontent.com/79812486/126675707-a81519d1-9d04-4f4c-b657-b1a0570a0a94.png)

The top 5 genres were:
1. Drama
2. Comedy
3. Romannce
4. Thriller
5. Action

Some of the less popular genres included:
* Silhouette animation
* Neorealism
* Children's Issues


## Natural Language Processing
I went through a variety of steps to transform the data for modeling
* Removed punctuation
* Only used English summaries
* Removed whitespaces
* Converted to lowercase
* Removed stop words

![Top_15_Words](https://user-images.githubusercontent.com/79812486/126676272-21a112d3-b6c7-42ea-b87e-7664716564d6.png)


## Prediction Modeling
I used a logistic regression to predict genres based on move summaries. Below are the steps that I took:
1. Multilabel Binarizer
* TF-IDF for feature extraction
* Train-Test split(test_size = .2)
* Logistic Regression


### Performance
I tried different threshold numbers to try to optimize the f1 score. Given more time, I would like to do a k-fold cross validation to find the best threshold. 
![Threshold and f1 Score Table](https://user-images.githubusercontent.com/79812486/126676797-ece14f3e-8d78-43f0-b21a-e54f505f8968.png)


## Technologies Used
* Numpy
* Matplotlib
* Pandas


## Next Steps
* Improve model
* Load more recent movie data
* Use Flask to create a web page where users can input their own summaries and test the model


## Use
This model could be used to improve movie descriptions for streaming platforms or movie theaters so customers can make better decisions about what to watch. 
