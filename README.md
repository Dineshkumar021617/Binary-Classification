# BINARY CLASSIFICATION
## Aim:
To write a python program to perform binary classification.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## Related Theory Concept:
Binary classification is a form of classification — the process of predicting categorical variables — where the output is restricted to two classes. It is used in many different data science applications, such as Medical Diagnosis, Email analysis, Marketing, etc. For example, in medical diagnosis, a binary classifier for a specific disease could take in symptoms of a patient and predict whether the patient is healthy or has a disease. The possible outcomes of the diagnosis are positive and negative.

## Algorithm
1. Import the necessary modules.
2. Create the Dataset using make_blob function.
3. Assign the counter value using the Counter Function and with the help of a for loop iterate over the values.
4. Plot the row values in the graph.

## Program:
```
/*
Program to implement binary classification.
Developed by: Dineshkumar.S
RegisterNumber:  212220230012
*/
from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot
x,y=make_blobs(n_samples=10,centers=2,random_state=1)
print(x.shape,y.shape)
counter=Counter(y)
print(counter)
for i in range(5):
    print(x[i],y[i])
for label,_ in counter.items():
    row_ix=where(y==label)[0]
    pyplot.scatter(x[row_ix,0],x[row_ix,1],label=str(label))
    pyplot.legend()
```

## Output:
![Screenshot (39)](https://user-images.githubusercontent.com/75234807/165560360-00c5ffca-7116-4d7e-b258-45d6362804f5.png)

## Result:
Thus the python program performed binary classification successfully.
