# IASA_CV
Codebase for IASA CV course

# Heart task

## Pipeline

1. Put `heart.csv` into `data` folder

2. Go to `notebooks` folder

3. Run `data_observation.ipynb` and take a look at data distributions

4. Run `make_stratification.ipynb` and make KFolds Stratified by `target`

5. Run `neural_net_approach.ipynb` and train and evaluate your model

6. Run `ml_approach.ipynb` and train and evaluate your model

7. Run `Blend.ipynb` and blend predictions

If you liked it, follow me on Kaggle - https://www.kaggle.com/vladimirsydor

# Experiments

Metric - ROC-AUC (5 folds)

## NN 

OOF : 0.9108824874256972

Fold mean: 0.9101220538720538

Fold std: 0.05358644090975845

## SVC 

OOF : 0.8790123456790123

Fold mean: 0.8900252525252526

Fold std: 0.036693204775323

## Random Forest 

OOF : 0.9168724279835391

Fold mean: 0.9183291245791245

Fold std: 0.03999131461434162

## Log Reg 

OOF : 0.9047553726566072

Fold mean: 0.9058291245791248

Fold std: 0.037308402973721295

## Random Forest 

OOF : 0.9001828989483311

Fold mean: 0.9019570707070708

Fold std: 0.0504083494837172

## Blend 

OOF : 0.9188385916780978