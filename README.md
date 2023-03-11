## MULTICLASS TEXT CLASSIFIER TO DETECT AN ONLINE POST IS HARMFUL TO CHILDREN

This project is done as a part of Omdena local chapter challenge to identify the grooming behavior.
https://omdena.com/projects/stop-online-violence-against-children-using-nlp/

The text is classified into 5 different classes to be more specific.
- Sexism
- Racism
- Homophobia
- Hate speech
- Bullying

Although the main focus of the project was to identify the grooming behaviour(talking to children online to exploit them sexually), based on the data collected from the twitter the team decided to go with more broader topics. The data collected was annotated manually by a team of 8 people.

## Data Preprocessing:
- Removed all the urls
- Removed all the numbers
- Removed Extra white spaces
- Removed hashtags
To deal with the class imbalance the data is divieded into train, validation and test set by using stratified split(7:2:1).

## Modelling:
Used camemBERT model from transformers library and fined tuned it to our dataset. The model was trained on 138 GB French text. The learning rate =1e-5, epochs = 10, batch size = 16.

## Evaluation:
Precision: 0.8499
Recall:0.8421
F1_score:0.8445

Inference on test set: Accuracy=0.8421

## Model Deployment:
The best model was saved in pickle format so that it can be used for inference. A simple streamlit app was created to demonstrate the classification.






