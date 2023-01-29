<h1 align="center" style="border-botom: none">
  <b>
    🐍 Hull White One-Factor model 🐍     
  </b>
</h1>


## Problem

## Solution


### Input

### Output


## Getting started

```python
import numpy as np
import pandas as pd
from Hull_White_one_factor import simulate_Hull_White_One_Factor

time = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
forwards = np.array([0.03, 0.03, 0.03, 0.03, 0.03, 0.03, 0.03, 0.03, 0.03, 0.03])
sigma = 0.2
alpha = 0.04
r0 = 0.02

out = simulate_Hull_White_One_Factor(r0, alpha, sigma, time, forwards)

index_evolution = np.insert(np.exp(np.cumsum(out["Interest Rate"].values)),0,1)
print(index_evolution)
```
