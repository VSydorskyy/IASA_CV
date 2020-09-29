# IASA_CV
Codebase for IASA CV course

# Heart task

## Pipeline

1. Put `heart.csv` into `data` folder

2. Go to `notebooks` folder

3. Run `data_observation.ipynb` and take a look at data distributions

4. Run `make_stratification.ipynb` and make KFolds Stratified by `target`

5. Run `neural_net_approach.ipynb` and train and evaluate your model

## TODO

- Add explanations
- Add `requirements.txt`
- Try XGB, LGB, Catboost, Random Forest, LogRegression, SVM
- Tweak NN model hyperparams 

If you liked it, follow me on Kaggle - https://www.kaggle.com/vladimirsydor

# Experiments

## NN baseline
```python
model = MultiLayerPerceptron(
        embedding_sizes_list=[(4,8),(3,6),(3,6),(2,4),(2,4),(2,4)],
        n_cont_features=len(ordinal_features),
        linear_config_list=[
            (64, 0.2, "MISH"),
            (128, 0.2, "MISH"),
            (64, 0.2, "MISH"),
            (1, 0.0, "IDENTITY")
        ]
    )
```
```
roc_auc
OOF : 0.8829903978052127
Fold scores: fold_n
0    0.960718
1    0.931538
2    0.973380
3    0.835648
4    0.887731
dtype: float64
Fold mean: 0.9178030303030302
Fold std: 0.05650849343497842



accuracy
OOF : 0.8215488215488216
Fold scores: fold_n
0    0.850000
1    0.900000
2    0.796610
3    0.728814
4    0.830508
dtype: float64
Fold mean: 0.8211864406779661
Fold std: 0.06376801895393938
```

# NN baseline_3layers
```python
model = MultiLayerPerceptron(
        embedding_sizes_list=[(4,8),(3,6),(3,6),(2,4),(2,4),(2,4)],
        n_cont_features=len(ordinal_features),
        linear_config_list=[
            #(64, 0.2, "MISH"),
            (128, 0.2, "MISH"),
            (64, 0.2, "MISH"),
            (1, 0.0, "IDENTITY")
        ]
    )
```
```
roc_auc
OOF : 0.9102423411065387
Fold scores: fold_n
0    0.956229
1    0.941639
2    0.938657
3    0.821759
4    0.890046
dtype: float64
Fold mean: 0.9096661054994388
Fold std: 0.05509851658418262



accuracy
OOF : 0.8181818181818182
Fold scores: fold_n
0    0.850000
1    0.900000
2    0.847458
3    0.694915
4    0.796610
dtype: float64
Fold mean: 0.8177966101694916
Fold std: 0.0778185781915186
```