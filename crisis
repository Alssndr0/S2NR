import pandas as pd
import numpy as np 
import matplotlib.pyplot as plt
import seaborn as sns
import operator
plt.style.use('seaborn')

def crisis_called(values, operator, threshold):
    
    '''
    Returns the number of crisis for a values/threshold model. 
    
    Values = insert your values, the data you want to study 
    Operator = operator.lt sets the model to signal for values under the treshold | operator.gt sets the model to signal for values above the treshold
    Threshold = your critical value, on a plot this is a straight line 
    '''
    
    array_values = np.asanyarray(values)
    signals = values[operator(array_values, threshold)]
    return len(signals)  
    
---
  
  
def crisis_called_plot(values, operator, threshold):
    
    '''
    Plots the number of crisis for a values/threshold model. 
    
    Values = insert your values, the data you want to study 
    Operator = operator.lt sets the model to signal for values under the treshold | operator.gt sets the model to signal for values above the treshold
    Threshold = your critical value, on a plot this is a straight line 
    
    '''
    
    
    array_values = np.asanyarray(values)
    signals = values[operator(array_values, threshold)]
    fig, axes = plt.subplots(1)
    sns.lineplot(x = np.linspace(1, len(values), num = len(values)), y = values, ax = axes).set(title='Number of crisis: {} '.format(str(len(signals))))
    sns.lineplot(x = np.linspace(1, len(values), num = len(values)), y = threshold, ax = axes)  
    
  
