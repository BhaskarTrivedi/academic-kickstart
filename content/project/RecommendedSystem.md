+++
title = "Recommender System" 
date = 2019-01-26T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Bhaskar Chandra Trivedi"]

#List format.
#0 = Simple
#1 = Detailed
#2 = Stream
list_format = 2

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Project"]

# Step to follow.

# Links (optional).
url_pdf = "files/RecommendedSystem.pdf"


advancemenuimg=""


#Optional featured image (relative to static/img/ folder).
[header] 
image = "" 
caption = "" 
+++
Recommender System<br/>
Purpose of this project to develop a  recommended system from scratch. Best approch to learn any concept, is to implement it. <br/><br/>
Abstract:<br/>
Recommender System / Machine is developed to suggest end user with the product ( can be anything likes movies, sports, food etc.) based on user interest. There are many ways to predict about end user interest. One of the most popular ways to keep track of user past, interest and suggest him/her according to his/her history(commonly known as content based recommendation). The positive side of this approach , it is simple and easy to develop, but the downside of it, the user may get monotonous suggestion and every time he will get the same kind of suggested product. Other approach can be a collaborative recommendation, where user not only get recommendations based on his/her interest but, also based on other similar user who matches with his/her interest to certain thresholds. It helps user to explore new area which he did not explore, but he may find it interesting once introduce it to them. <br/>

Classification<br/>
Classification problem can be defined as “deciding class for unknown data based on its feature and learning from old known data and its classes”. As an example, lets we have a dataset of spam and regular email. After looking into these data set, we decide some feature specific these data like sender, subject line, external link and domain. These features can act as a dimensionality of dataset.  
<br/>
We have different Machine learning algorithm which help with training and classification problem. Logistic Regression, naïve based classifier, Support Vector Machine (SVM), Decision Tree, Neural Network and many more. Each algorithm has their own specification and they work better for specific data set. We don’t have any general algorithm which work better for all data set. 
<br/>
Support Vector Machine is a supervised machine learning algorithm which can be used for classification. It analyzes n dimensional data and performed binary or multi class classification based on available classes in training data sets. 
<br/>
Linear classification separate n dimension data using hyperplane and maximize the margin to reduce error for any known dataset.
Non linear classification first map n dimensional data set to higher dimension and then separates it using classifier. For non linear classification different type of kernel is available like polynomial and exponential kernel.  
<br/>
Project specific. <br/>
To perform classification problem, I needed dataset which should have dimensionality for classification problem. While planning and developing this project I was not just thinking about writing some line of code but also, I was analyzing data and trying to figure it these data has enough information to perform classification problem. I am working on Kaggle movie data set and I didn’t found feature that can be used for classification. One thought come to mind using user review and use it for classification but reject this idea as user review can be good for recommendation system but can’t be utilize for classification as user tends to give very vague statement which can apply to all class.  To solve this issue an idea came to my mind to add dimensionality and weightage based on tag and finale class. Whole idea behind this any movie which we categories as Action also has its share of romance, fantasy and comedy into it. Every movie has element of some other feature but overall it is categorized to one specific category based on specific feature weightage.  So, I added some feature and created training data set to train my classifier. 
{{< figure src="/img/classification.JPG" title="" >}}<br />
<br/>
For Code and Implementation detail visit Git hub<br/>

Dataset <br/>
Dataset primary refer as a collection of similar type of index data which can be used for special purposes. With time and technology data set are becoming huge and tradition approach (normal SQL queries) is not sufficient to store and retrieve data from data set. To tackle this situation big data come into picture. It helps with fast data retrieval with proper indexing. The first step towards developing any recommender system is to finalize data set. According to data set we can plan our approach and decide which feature is important to create our recommender system. Click here to visit [movielens](https://grouplens.org/datasets/movielens/).
To explore more dataset [click here](https://www.kdnuggets.com/2016/02/nine-datasets-investigating-recommender-systems.html).
More [movie dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset#movies_metadata.csv).



