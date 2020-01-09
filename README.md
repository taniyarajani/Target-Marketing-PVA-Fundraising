# Target-Marketing-PVA-Fundraising
Developed data mining models to improve the cost effectiveness of PVA's direct marketing campaign. According to their recent mailing records, the overall response rate is 5.1%. Out of those who responded (donated), the average donation is $13.00. Each mailing, which includes a gift of personalized address labels and assortments of cards and envelopes, costs $0.68 to produce and send. Using these facts, we take a sample of this dataset to develop a classification model that can effectively capture donors so that the expected net profit is maximized. Weighted sampling is used, under-representing the non-responders so that the sample has a more balanced numbers of donors and non-donors.

Data The modeling dataset is in the file kdd98LRN.txt. The data has around 95K rows and 480 attributes. The target variable, on response, is in the TARGET_B column. The data set has 5.1% responders.

**Part 1 - Target variable is TARGET_B (to predict donors).** 
Steps included in the part 1- 
1. Data cleaning and exploration
  -Missing value imputation
  -Variable selection is done using Random Forest and Decision Trees
  -Derived new variables
  -Variable transformation
  -Data reduction is done using Principle Component Analysis (PCA)
2. Resampling 
  -Models are evaluated using higher proportion of response (40%-50%), lower proportion (20%-30%) and balanced proportion
3. Modelling
  -Logistic Regression, using Ridge and Lasso, Random forest, Boosted trees and SVM
4. A comparative evaluation of performance of best models from each technique is done considering confusion matrix, lift and ROC.
(Target_D which is amount of donation is not included in part 1)

**Part 2 - Target variable is TARGET_D (to amount of donation)
Here, I have develop a model to predict donation amount (TARGET_D) directly, and examined how to combine the response and donation amount models to identify the most profitable individuals to target.**
Steps included in the part 2-
1. Identified the most profitable individuals to target using the response model with average donation & mailing costs information
2. Develop a second model on TARGET_D, and combine this with the response model to identify the most profitable individuals to target
3. Well-calibrated probability scores before ‘combining’ the response and donation amount models

