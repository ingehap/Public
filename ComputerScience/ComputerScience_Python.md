# Code 01, Python - project sceleton
```python=
cookiecutter https://github.com/audreyr/cookiecutter-pypackage.git
```

# Code 02, Python - script template
```python=
#!/usr/bin/env python

"""
One-line description of what the script does.
""" 

import argparse 

def main(args): 
    """Run the program.""" 
    print('Input file:', args.infile) 
    print('Output file:', args.outfile) 

if __name__ == '__main__': 
    parser = argparse.ArgumentParser(description=__doc__) 
    parser.add_argument('infile', type=str, help='Input file name') 
    parser.add_argument('outfile', type=str, help='Output file name') 
    args = parser.parse_args() 
    main(args)
```

# Code 03, Python - reproducibility
```python=
        # reproducibility101.py
	import random
	random.seed(101)
        import numpy as np
        np.random.seed(101)
        import tensorflow as tf
        tf.random.set_seed(101)
        import torch
        torch.manual_seed(101)
```

# Code 04, Python - python-dotenv
```python=
        # pip install python-dotenv
        # .env contains EMAIL='ingehap@gmail.com'
	from dotenv import load_dotenv
        load_dotenv()
        my_email = os.environ['EMAIL']
```

### 04. Appendix B/Templates

#### 04.1 Python - Linear Regression 

Example 1
```python=
import statsmodels.api as sm
from sklearn import datasets
data = datasets.load_boston()
import numpy as np
import pandas as pd

# define the data/predictors as the pre-set feature names  
df = pd.DataFrame(data.data, columns=data.feature_names)

# Put the target (housing value -- MEDV) in another DataFrame
target = pd.DataFrame(data.target, columns=["MEDV"]). 
X = df["RM"] ## X = df[[“RM”, “LSTAT”]] if two variables
y = target["MEDV"]
X = sm.add_constant(X) # if you want a constant in your model
model = sm.OLS(y, X).fit()
predictions = model.predict(X)
model.summary()
```

Example 2
```python=
from sklearn import linear_model
lm = linear_model.LinearRegression()
model = lm.fit(X,y)
predictions = lm.predict(X)
print(predictions)[0:5]
lm.score(X,y) # Rsquared
lm.coef_
lm.intercept_
```

#### 04.2 Python - list of search paths for site packages

```python=
	import site
	site.getsitepackages()
```

#### 04.3 Python - pickle example

```python=
	import pickle
	est = SymbolicRegressor()
	est.fit(X_train, y_train)
	with open('gp_model.pkl', 'wb') as f:
	    pickle.dump(est, f)
	with open('gp_model.pkl', 'rb') as f:
	    est = pickle.load(f)
```

#### 04.4 Python - pydotplus

```python=
	from IPython.display import Image
	import pydotplus
	graph = est_gp._program.export_graphviz()
	graph = pydotplus.graphviz.graph_from_dot_data(graph)
	Image(graph.create_png())
```
