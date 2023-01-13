# Junior-DS-Assessment--UM
## Hypothesis:
People who are most eligible for home loans have a credit history, education, a coapplicant, and are not self-employed.

## Top Performing Model:
Random Forest Classifier

## Model stats:
roc auc: 0.7115
accuracy: 0.8261
precision: .8080
recall: .9877
f1: 0.8888

## Written Portion Questions:
### Why did I choose this model?
1. I modeled both Logistic Regression and Random Forest Classifier. I always like to test various models, especially ones that are different in terms of flexibility and interpretability.

2. Advantages to Random Forest models are:  <br>
  2a. implicitly perform feature selection and generate uncorrelation decision trees  <br>
  2b. not influenced by outliers to a fair degree  <br>
  2c. able to handle linear and non-linear relationships well  <br>
  2d. able to generally provide high accuracy and balance the bias-variance trade-off well  <br>
  
3. While the Random Forest model performed better in terms of roc_auc, Logistic Regression was very close behind. If the prompt had requested more information about how the predictors relate to the response, I would have likely only gone with a regression model because they are more interpretable and are able to tell you about the relationship of beta and selected features
### What could I do to improve this model?
1. Tweak hyperparameters even further. Potentially using techniques like GridSearchCV.

2. Leverage boosted trees models like XGBoost.

3. I imputed data for some of our features and I wonder how the model would perform if I had just removed all nulls without imputing. It would be interesting to compare model results with each method of cleaning the data, this would help me understand if my imputations introduced bias.

4. Work with stakeholders to understand the precision/recall tradeoff.
### What next steps would I take? (outside of model improvements)
1. Given my geospatial background, I think it would be really interesting to run this analysis from a geospatial lens. A potential way to break this down could be the ‘Property_Area’ feature in the test and train data.  <br>
  1a. If applicant addresses (even at zip code level) were an optional data field, it would allow for more granular insights.
  
2. Work with relevant business groups to fully implement this automated way of approving home loan applicants into production.  <br>
  2a. Help business groups understand that model results are probabilistic. This means that it is not 100% that applicants fall into their assigned group, it is rather a probability that they are eligible or not for a home loan. This information would help stakeholders decide the best implementation of this process.  <br>
  2b. There are also chances to work with other teams, like marketing. Using the data, analysis, and model results, we now have an idea who the ideal candidates for loans are. We could uncover where these populations are and increase outreach efforts in these areas if it was of interest.
