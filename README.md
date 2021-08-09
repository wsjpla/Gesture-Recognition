
## Requirements

- Python 3.8
- Numpy
- Pandas
- Scikit-learn
- Seaborn

## Usage

Train:

```bash
./gestureRecognition.py train
```

Evaluating:

```bash
./gestureRecognition.py test
```

You can choose the ML model by editing the follow codes:
```python
#model = RandomForestClassifier(n_estimators=100)
#model = KNeighborsClassifier(n_neighbors=10)
#model = Pipeline([("scaler", StandardScaler()), ("svm_clf", SVC(kernel="rbf", gamma=1, C=1))])
model = Pipeline([("scaler", StandardScaler()), ("svm_clf", SVC(kernel="poly", degree=3, coef0=1, C=3))])
```
