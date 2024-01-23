# Dog-Adoption-Classification
A step-by-step process of classification modeling to predict whether a dog will be adopted or not, as well as the significant features that affect this outcome.

# Step 1: Importing Data
Using Deepnote, I first imported the datasets found on Kaggle (https://www.kaggle.com/datasets/whenamancodes/dog-adoption?select=dogTravel.csv and https://www.kaggle.com/datasets/umairnsr87/petadoption-mod/data) for further analysis and cleaning.

# Step 2: Data Cleaning
Once these datasets were merged, we performed data cleaning by removing duplicate IDs and faulty data while also handling null values by replacing them with 'unknown' or 'False' depending on individual column requirements. The data was also generally filtered by removing irrelevant/duplicate columns (EX: column dog.x only having one value: dog), columns that demonstrated inconsistencies (EX: breed_mixed not being a consistent boolean when breed_primary and breed_secondary existed), and columns with too many unique values (such as address).

# Step 3: Modeling
The four modeling strategies implemented include a baseline model, logistic regression, CART/Decision Tree, and a Decision Tree with Cross-Validation, all of which were utilized to determine important features that can predict whether a dog will be adopted or not. The baseline model simply only predicts that a dog will not be adopted, resulting in 76.57% accuracy without any predictive features. 

The logistic regression (utilizing all chosen features after data cleaning) had only a slightly higher accuracy at 76.93%, however, we were able to understand the reasoning behind this through a confusion matrix that demonstrated a low true positive rate and a high true negative rate (similar to the baseline model). 

The most valuable insights gained from this modeling came from the decision trees, where the version without cross-validation demonstrated a few of our important deciding features of whether a dog is likely to be adopted such as whether a dog is up to date with shots (giving us an accuracy of 77.16%). However, without cross-validation, all of the features were included in the decision tree, which did not narrow down our important features enough and led us to include cross-validation to determine the most important features relating to dog adoption (like primary breed, house_trained, child_friendly, etc) in a more abbreviated and efficient decision tree with an accuracy of 78.11%.

# Conclusion
In the end, this project was able to conclude important features in predicting whether a dog will be adopted, which gives some actionable responses for dog shelters to increase the likelihood a dog will be adopted (keeping up to date on vaccinations, for example). In the future, improving this modeling could involve implementing sentimentality scores according to each dog's description, improved decision tree parameters, and of course more data.

Further details about this project are available in the slides attached.
