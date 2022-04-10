# Capsular Contracture

### Logistic Regression Model Starter Code
To load the model, run the following in the command line:
```
python
import pickle
import pandas as pd
import sklearn
loaded_model = pickle.load(open('capsule_model_LR.sav', 'rb'))
```

After loading the model, run the following to generate a probability prediction:
```
test=pd.DataFrame({'Age at surgery':[#],
                   'BMI at surgery':[#],
                   'Post-op radiation':[0,1],
                   'NF':[#],
                   'te2implant_time':[#]})
                   
loaded_model.predict_proba(test)
```
where "num" is an integer or a float, and [0,1] represents a categorical variable, where 0 = no, and 1 = yes

### Output Format
>**[% No Contracture, % Capsular Contracture]**

### Neural Network Model Starter Code
To load the model, run the following in the command line:
```
pip install pyyaml h5py
new_model = tf.keras.models.load_model('my_model.h5')
```
where "num" is an integer or a float, and [0,1] represents a categorical variable, where 0 = no, and 1 = yes

After loading the model, run the following to generate a probability prediction:
```
new_model.predict(dict(test))

### Output Format
>** value <= 0: No Contracture, otherwise: Capsular Contracture**


### Python Version
>3.7.4

