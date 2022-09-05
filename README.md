# Diagno.AI

Diagno.AI is an integrated end to end Artificial Intelligence application for the people who instantly need preliminary medical diagnosis. The inspiration for my idea comes while solving the problem: There are millions of people in this world without access to proper healthcare and preliminary medical diagnosis. And in effort to solve this problem was born Diagno.AI - An Artificial Intelligence based Preliminary Diagnosis Platform for patients around the world!

Note: Diagno.AI includes a fully functional frontend, don't forget to try it!!

Diagno.AI currently supports preliminary diagnosis of following disease:
- Diabetes
- Heart Disease
- Parkinson's Disease

The Model files are generated through seperated Machine Learning >Data Analysis >Model Building >Model Training >Finetuning pipeline for which the code is here: 

## How to Call

First, we simply load the PyDaisi package:

```python
import pydaisi as pyd
```

Next, we connect to the Daisi:

```python
diagno_ai = pyd.Daisi("amitpatel/Diagno AI")
```

Next, we have three end points for prediction of Diabetes, Heart Disease and Parkinson's Disease respectively:

predict_diabetes
```python
diagno_ai.predict_diabetes(diab_features).value
'''
Parameters: - diab_features (List) : This can be an array/list of features/params as a model inputs Sample Param Order: [Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age] Returns : A probab score which tells scale of diabetes
'''
```

predict_heart_disease
```python
diagno_ai.predict_heart_disease(heart_features).value
'''
Parameters: - heart_features (List) : This can be an array/list of features/params as a model inputs Sample Param Order: [age, sex, cp, trestbps, chol, fbs, restecg,thalach,exang,oldpeak,slope,ca,thal] Returns : A probab score which tells scale of heart disease
'''
```

predict_parkinsons
```python
diagno_ai.predict_parkinsons(parkinsons_features).value
'''
Parameters: - parkinsons_features (List) : This can be an array/list of features/params as a model inputs Sample Param Order: [fo, fhi, flo, Jitter_percent, Jitter_Abs, RAP, PPQ,DDP,Shimmer,Shimmer_dB,APQ3,APQ5,APQ,DDA,NHR,HNR,RPDE,DFA,spread1,spread2,D2,PPE] Returns : A probab score which tells scale of parkinsons
'''
```

Also, Streamlit UI endpoint:

st_ui
```python
diagno_ai.st_ui().value
'''
Streamlit UI
'''
```

Thank-you:))


