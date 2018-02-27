# Tasks
KDD Cup 2009: Customer relationship prediction

Task Description

The task is to estimate the churn, appetency and up-selling probability of customers, hence there are three target values to be predicted. The challenge is staged in phases to test the rapidity with which each team is able to produce results. A large number of variables (15,000) is made available for prediction. However, to engage participants having access to less computing power, a smaller version of the dataset with only 230 variables will be made available in the second part of the challenge.

Churn (wikipedia definition): Churn rate is also sometimes called attrition rate. It is one of two primary factors that determine the steady-state level of customers a business will support. In its broadest sense, churn rate is a measure of the number of individuals or items moving into or out of a collection over a specific period of time. The term is used in many contexts, but is most widely applied in business with respect to a contractual customer base. For instance, it is an important factor for any business with a subscriber-based service model, including mobile telephone networks and pay TV operators. The term is also used to refer to participant turnover in peer-to-peer networks.
Appetency: In our context, the appetency is the propensity to buy a service or a product.
Up-selling (wikipedia definition): Up-selling is a sales technique whereby a salesman attempts to have the customer purchase more expensive items, upgrades, or other add-ons in an attempt to make a more profitable sale. Up-selling usually involves marketing more profitable services or products, but up-selling can also be simply exposing the customer to other options he or she may not have considered previously. Up-selling can imply selling something additional, or selling something that is more profitable or otherwise preferable for the seller instead of the original sale.

# Evaluation

The performances are evaluated according to the arithmetic mean of the AUC for the three tasks (churn, appetency. and up-selling). This is what we call "Score" in the Result page.

# Sensitivity and Specificity

The main objective of the challenge is to make good predictions of the target variables. The prediction of each target variable is thought of as a separate classification problem. The results of classification, obtained by thresholding the prediction score, may be represented in a confusion matrix, where tp (true positive), fn (false negative), tn (true negative) and fp (false positive) represent the number of examples falling into each possible outcome:

|---------|---------|--------------------------------|
|---------|---------|            Prediction          |
|---------|---------|--------------------------------|
|---------|---------|   Class+1       | Class+2      |
|  Truth  |Class +1 |      tp         |    fn        |
|---------|Class +2 |      fp         |    tn        |
|---------|---------|-----------------|--------------|


Any sort of numeric prediction score is allowed, larger numerical values indicating higher confidence in positive class membership.

We define the sensitivity (also called true positive rate or hit rate) and the specificity (true negative rate) as:

Sensitivity = tp/pos
Specificity = tn/neg
where pos = tp+fn is the total number of positive examples and neg=tn+fp the total number of negative examples.

# AUC

The results will be evaluated with the so-called Area Under Curve (AUC). It corresponds to the area under the curve obtained by plotting sensitivity against specificity by varying a threshold on the prediction values to determine the classification result. The AUC is related to the area under the lift curve and the Gini index used in marketing (Gini = 2 AUC -1). The AUC is calculated using the trapezoid method. In the case when binary scores are supplied for the classification instead of discriminant values, the curve is given by {(0,1), (tn/(tn+fp), tp/(tp+fn)), (1,0)} and the AUC is just the Balanced ACcuracy BAC.