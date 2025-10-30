![[scikit_learn_ml_ai.png]]

Data > Algorithm > Fit > Evaluate > Improve > Save

## Get data ready
```python
df = pd.read_csv('quiz_data.csv')

features = ['Age', 'Weight (kg)', 'Height (m)', 'Session_Duration (hours)', 'Avg_BPM', 'Resting_BPM']
target = 'Calories_Burned'

X = df[features]
y = df[target]

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```
## Choose the right estimator/algorithm for problem

```python
model = LinearRegression()

```

## Fit the model/algorithm and use it to make predictions on data
```python
model.fit(X_train, y_train)
```

## Evaluate a model
```python

sample = pd.DataFrame([{
    'Age': 25,
    'Weight (kg)': 68,
    'Height (m)': 1.75,
    'Session_Duration (hours)': 1.2,
    'Avg_BPM': 140,
    'Resting_BPM': 72
}])

predicted_calories = model.predict(sample)
print(f"პროგნოზირებული კალორიების რაოდენობა: {predicted_calories[0]:.2f}")

###########################################################################

model.score(x_test, y_test)
# 1 max
# 0 min
from sklearn.metrices import classification_report, confusion_matrix, accuracy_score

classification_report(y_test, y_pred)
```

## Improve a model

## Save and load a trained model

