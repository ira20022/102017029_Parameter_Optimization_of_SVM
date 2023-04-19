# SVM
What is a Support Vector Machine(SVM)?
A Support Vector Machine is a supervised machine learning algorithm which can be used for both classification and regression problems. It follows a technique called the kernel trick to transform the data and based on these transformations, it finds an optimal boundary between the possible outputs.

In simple words, it does some extremely complex data transformations to figure out how to separate the data based on the labels or outputs defined.We will be looking only at the SVM classification algorithm in this article.

# PARAMETER OPTIMIZATION
A fancy name for training: the selection of parameter values, which are optimal in some desired sense (eg. minimize an objective function you choose over a dataset you choose). The parameters are the weights and biases of the network.

# DATASET

Data have been normalized by using the Z-normalization method and divided into two data sets: a training set containing 10437 samples, and a test set containing the 10437 samples.


CLASS DISTRIBUTION (training set)
**A: 4286**<br>
**B: 5**<br>
**C: 103**<br>
**D: 352**<br>
**E: 1095**<br>
**F: 1961**<br>
**G: 446**<br>
**H: 519**<br>
**I: 831**<br>
**W: 44**<br>
**X: 522**<br>
**Y: 266**<br>

Attribute Information:

**F1: intercolumnar distance**<br>
**F2: upper margin**<br>
**F3: lower margin**<br>
**F4: exploitation**<br>
**F5: row number**<br>
**F6: modular ratio**<br>
**F7: interlinear spacing**<br>
**F8: weight**<br>
**F9: peak number**<br>
**F10: modular ratio/ interlinear spacing**<br>
**Class: A, B, C, D, E, F, G, H, I, W, X, Y**<br>

# Methodlogy

The dataset is split into training and testing set for 10 times and the following SVC classifier hyperparameter are selected for best accuracy:

**Kernel** -  Different kernel functions to model non-linear relationships between the input variables and the output variableSelected from RBF, Polynomial, Linear and Sigmoid<br>
**C** (Regularisation parameter) - It is used to set the tolerance of the model to allow the misclassification of data points in order to achieve lower generalization error. Higher the value of C, lesser is the tolerance and what is trained is a maximum-margin classifier. Smaller the value of C, larger is the tolerance of misclassificationRandom integer values from 1 to 6<br>
**Gamma** (Kernel coefficient) - The gamma parameter defines how far the influence of a single training example reaches, with low values meaning ‘far’ and high values meaning ‘close’. The lower values of gamma result in models with lower accuracy and the same as the higher values of gamma. It is the intermediate values of gamma which gives a model with good decision boundaries.Random integer values from -1 to 6. If the value is less than 1, then gamma is randomly set as auto or scale. It is used only by rbf, poly and sigmoid kernel.<br>
**Degree** - Random integer from 1 to 7. It is only used by poly kernel and represent the degree of polynomial kernel function.<br>


# OBSERVATIONS

|Sample| Kernel   |   c | gamma   |   degree |   Accuracy |
|-----:|:---------|----:|:--------|---------:|-----------:|
0      |rbf       |6    |auto     | 5        |0.725791
1      |rbf       |2    | 4       |4         |0.708853
2      |rbf       |4    | 1       |6         |0.770214
3      |rbf       |5    | 1       |1         |0.771492
4      |rbf       |3    |scale    |4         |0.709492
5      |rbf       |3    | 3       |5         |0.706296
6      |rbf       |1    | 4       |7         |0.639182
7      |rbf       |4    |scale    |1         |0.736977
8      |rbf       |5    | 2       |6         |0.735059
9      |rbf       |4    |2        |3         |0.744966

# GRAPH

<img width="431" alt="image" src="https://user-images.githubusercontent.com/102228647/233161977-12cbe2ac-fb6e-486c-8995-ce28a31f17ff.png">


# RESULT

**KERNAL: RBF**<br>
**C:5**<br>
**GAMMA:1**<br>
**DEGREE :1** <br>
**Accuracy : 0.771492**<br>
