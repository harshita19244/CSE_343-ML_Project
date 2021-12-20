# E-commerce product classification
With the growing popularity of e-commerce websites like Amazon, Flipkart, and Myntra, number of products available on these platforms have significantly increased. Owing to this, the product classification problem has gained practical significance in the industry. The project aims to address the product classification problem by deeply taking into account natural language processing techniques. It focuses on applying natural language processing to obtain a clean dataset consisting of product descriptions. This has been achieved by eliminating common words, stop words and generic product categories. Additionally, count vectorizers are implemented to convert text data into its appropriate vector representation. Various modern machine learning algorithms are applied to achieve accurate product classification for catalogues consisting of lakhs of products on the obtained vectorized data. In retrospect, this project finds intensive application in the currently booming E-commerce industry.

## Literature Surveyed
In order to understand the previous approaches towards solving this problem we went through the following literature:
* [Goldenbullet: Automated classification of product data in e-commerce](https://www.researchgate.net/publication/335420427_Atlas_A_Dataset_and_Benchmark_for_E-commerce_Clothing_Product_Categorization)
* [Machine Learning Based Product Classification for eCommerce](https://www.tandfonline.com/doi/abs/10.1080/08874417.2021.191088)
* [Don't Classify, Translate: Multi-Level E-Commerce Product Categorization Via Machine Translation.](https://arxiv.org/abs/1812.05774)
* [Amazon ML Challenge](https://www.hackerearth.com/challenges/competitive/amazon-ml-challeng/)

## Dataset
The dataset for the product classification task was taken from the Amazon product classification challenge on Kaggle. The dataset can be found [here](https://drive.google.com/file/d/1cMo_cczClT4UPw3eEjlKxnmbzheqX516/view?usp=sharing).

## Data-Preprocessing
In the inital stages of the project we perfomed data pre-processing. We used an NLP based approach. 
* Firstly, null valued columns were eliminated from the data. Then, each data point was converted into an independent document, a tuple containing the product title, description and bullet points together. 
* Tokenization was performed on the text document which enabled us to perform POS tagging and lemmatization on the dataset based on the category. We appropriately classified the 
words present in each category description as appropriate parts of speech for further evaluation. 
* We employed the WordNet lemmatizer to lemmatize categorical data and perform appropriate preprocessing. Every document tuple was cleaned, and stop words and punctuations were eliminated.  
* In the dataset, products with no defined categories were labeled as 'Generic' products. Hence 'Generic' category products were eliminated. 
* Words that appear in about 95% of the data points were eliminated from the dataset to improve model performance. 

## Models employed
* Logistic Regression
* SGD classifier
* Bernoulli Naive Bayes
* Multinomial Naive Bayes
* Decision Tree
* Random Forest
* SVM
* MLP
* K-NN Classifier

## Running the model

* To demonstrate the working, clone the repository.
* Load the model
<br/>The models trained are saved in the models directory. Uncompress the model if compressed and load using the following command.
```
model = joblib.load(model)
```
* Testing the model
<br/>Predict the output on the testing data using the following code:
```
y_pred = model.predict(x_test)

```
* Getting the accuracy
<br/>Get the accuracy of the model used using the following code:
```
score = model.score(x_test)

```
* If you want to execute the whole model including all algorithms and pre-processing tasks, navigate to the ```final code``` directory and execute [final_code.ipynb](https://github.com/HardikDudeja/CSE_343-ML_Project/tree/main/final%20code)
### Team Members
* [Hardik Dudeja](https://github.com/HardikDudeja)
* [Harshita Srinivas](https://github.com/harshita19244)
* [Mohit Bhar](https://github.com/MohitBhar)
* [Saksham Mehla](https://github.com/Saksham-Mehla)

