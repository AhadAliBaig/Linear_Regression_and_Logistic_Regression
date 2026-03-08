# Logistic Regression Model - SMS Spam Classification

## Data

We use the **SMS Spam Collection** (see `Data/readme` for full details). It is a set of 5,574 English SMS messages labeled as **ham** (legitimate) or **spam**. The file has one message per line: first column is the label (ham/spam), second column is the raw message text, separated by a tab. About 87% of the messages are ham and 13% are spam.

## What We Did

1. **Load the data** -> Read the tab-separated file into a table with columns `label` and `message`.
2. **Binary target** -> Turned labels into numbers: ham = 0, spam = 1.
3. **Split** -> Kept 80% of the data for training and 20% for testing.
4. **Text to numbers** -> Used CountVectorizer to turn each message into word counts so the model can use it.
5. **Train** -> Fit a logistic regression model on the training set.
6. **Evaluate** -> Checked accuracy on the test set and showed a confusion matrix.

## Results

The model reaches high accuracy. The confusion matrix shows all real ham messages were correctly classified (no false alarms), and most spam was caught; a small number of spam messages were missed (predicted as ham).