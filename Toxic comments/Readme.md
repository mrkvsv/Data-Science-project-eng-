# Predicting positive and negative comments from online store users.

The online store launches a new service. Now users can edit and supplement product descriptions, just like in wiki communities. That is, clients propose their edits and comment on the changes of others.
The store needs a tool that will look for toxic comments and submit them for moderation.

**Task** - to train the model to classify comments into positive and negative.

**Stack:** `numpy` `sklearn` `spacy` `torch` `BERT`

### Conclusion

Thus, we have prepared data and trained various models.
The best model in terms of the quality of the F1 metric was LogisticRegression, trained on features prepared by BERT (unitary/toxic-bert), with parameters: C = 1, penalty = 'l2', and a classification threshold of 0.489, which showed an F1 value of 0.95 on the test sample.
