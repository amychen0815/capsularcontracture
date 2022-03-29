# Capsular Contracture

### Model Starter Code
To load the model, run the following in the command line:
```
python
import pickle
import pandas as pd
loaded_model = pickle.load(open('capsule_model.sav', 'rb'))
```

After loading the model, run the following to generate a probability prediction:
```
test=pd.DataFrame({'Age at surgery':[#],
                   'BMI at surgery':[#],
                   'Retropec':[0,1],
                   'Phasix':[0,1],
                   'Necrosis?':[0,1],
                   'Treatment?\nYes (1)\nNo (0)':[0,1],
                   'Post-op radiation':[0,1],
                   'NF':[#],
                   'Height^2\nNF^2 - (0.5BW)^2':[#]})
loaded_model.predict_proba(test)
```
where "num" is an integer or a float, and [0,1] represents a categorical variable, where 0 = no, and 1 = yes

### Output Format
>**[% No Contracture, % Capsular Contracture]**

### Python Version
>3.7.4
