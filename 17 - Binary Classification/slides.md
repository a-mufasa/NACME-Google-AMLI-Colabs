---

marp: true

---

<style>
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
</style>

# Binary Classification

<!--
Our exploration of classification will start with the simplest case: binary classification. 
-->

---

# Binary Classification

![center](res/yes_or_no.png)

<!--
Binary means there are only two values to predict. Binary classification is used to predict one of two values.

These can be true/false, hotdog/not hotdog, yes/no, benign/malignant, or any other possible this-or-that options. For simplicity, these options are usually encoded as 1 and 0.

* Image name: res/yes_or_no.png
  * Repo link: https://github.com/google/applied-machine-learning-intensive/tree/master/content/04_classification/01_binary_classification/res/yes_or_no.png
  * Source https://pixabay.com/vectors/button-yes-no-red-green-icon-32259/ by Author Clker-Free-Vector-Images https://pixabay.com/users/clker-free-vector-images-3736/ under License https://pixabay.com/service/license/.
-->

---

# Binary Classification: Models

* Logistic Regression
* Decision Trees and Random Forests
* Support Vector Machines (SVM)
* Bayesian Networks
* Neural Networks
* *... and more*

<!--
There are many models capable of performing binary classification. Some of the more common ones are listed on this slide. Each model has its strengths and weaknesses. We'll study each of these model-types in this course.
-->

---

# Binary Classification: Logistic Regression

![center](res/classification.gif)

<!--
In the lab for this unit, we will build a logistic regression. A logistic regression finds a logistic function and uses it to divide two classes of data. A logistic function is a function in the shape depicted in this slide. It can range in values from zero to one.

This model is relatively easy to interpret and train, but it doesn't perform well unless an actual logistic boundary can be found. To create a logistically divisible set of classes, you sometimes have to perform some very heavy data manipulation.

* Image name: res/classification.gif
  * Repo link: https://github.com/google/applied-machine-learning-intensive/tree/master/content/04_classification/01_binary_classification/res/classification.gif
  * Source https://github.com/google/applied-machine-learning-intensive/tree/master/content/04_classification/01_binary_classification/res/classification.gif by Author Google LLC under License Copyright [2020] Google LLC.
-->

---

# The Lab

![center](res/oranges_and_grapefruit.jpg)

<!--
In our binary classification lab we will try to differentiate between oranges and grapefruit. We have a dataset with weight, size, and color information. We will build a logistic regression model to try to accomplish this task.

* Image name: res/oranges_and_grapefruit.jpg
  * Repo link: https://github.com/google/applied-machine-learning-intensive/tree/master/content/04_classification/01_binary_classification/res/oranges_and_grapefruit.jpg
  * Source https://pixabay.com/photos/oranges-orange-grapefruit-3004200/ by Author Samueles / Samuele Schir?? https://pixabay.com/users/samueles-1246195/  under License https://pixabay.com/service/license/.
-->

---

# The Lab: Grid Search

```python
search = GridSearchCV(model, {
  'learning_rate': [1e-3, 1e-4],
  'max_iter': [10000, 15000],
  'C': 1,
})
```

<!--
In this lab, we'll use a few new machine learning techniques. One of these is grid search. Grid search is a way to test different hyperparameters for a model. The search accepts a dictionary containing keys that map to model parameters. The values are lists for hyperparameters that you want to experiment with or single values for parameters that you want to keep constant.

Grid search tries every combination of parameters and finds which performs the best. This can be really useful for testing hyperparameters, but remember that combinations increase at a factorial rate, so running grid search can take quite a while.
-->

---

# The Lab: Confusion Matrix

![center](res/Classification1.png)

<!--
We will also create our first confusion matrix in this lab. Remember that a confusion matrix shows true and false positives and negatives.

* Image name: res/Classification1.png
  * Repo link: https://github.com/google/applied-machine-learning-intensive/tree/master/content/04_classification/01_binary_classification/res/Classification1.png
  * Source https://github.com/google/applied-machine-learning-intensive/tree/master/content/04_classification/01_binary_classification/res/Classification1.png by Author Google LLC under License Copyright [2020] Google LLC.
-->

---

# Your Turn

<!--
Now let's explore the binary classification lab.
-->
