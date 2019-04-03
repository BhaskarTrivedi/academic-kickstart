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
<br/>
Project specific. <br/>
Naïve Based classification<br/><br/>
Naïve Based classification assume each feature (in many literatures also refer as dimension are independent of each other). It is simple probability-based classifier. It uses Bayes probability theorem to solve classification problem.<br/><br/>
Mathematical representation of Bayes Theorem <br/><br/>
P(A|B) = P(B|A) * P(A) / P(B)<br/><br/>
If we consider movie data set the formula will become <br/>
P(y|X) = P(X|y) * P(Y) / P(X)<br/><br/>
According to naïve bayes each feature is independent of each other <br/>
P(y|x1,x2,…..xn ) = P(x1|y)P(x2|y)..P(xn|y) P(y) /(P(x1)P(x2)…..P(xn) <br/><br/>
Visit https://nlp.stanford.edu/IR-book/pdf/13bayes.pdf for detailed clarification.<br/><br/>
Implementation Details.<br/>
Class CNaiveBayes.py<br/>
Responsible to perform Naïve classification and return probability-based class<br/><br/>
Variable description<br/>
ClassF : store classfrequency/ Probablity<br/>
queryClassPrabablity : store  Probablity of class given term<br/>
ClassTermCount : to store each class has how may total term<br/>
TermClassFrequency : to store count of term in each class<br/>

Method Description <br/><br/>
Tokenize : create token from the string description and remove stop word(common word)<br/>

    def tokenize(self, description):
        if pd.isnull(description):
            return []
        else:
            terms = description.lower().split()
            # remove stop word
            filtered = [word for word in terms if not word in stopwords.words('english')]
            return filtered


Initialize : Perform Basic Initialization Operation Reading data, create token and initialize each class variable.<br/>

          for term in u_term:
                #updating count of each term 
                self.ClassTermCount[current_class].add(term)
                self.TermClassFrequency[term][current_class] = self.TermClassFrequency[term].get(current_class,0) + u_count[term_index]
                term_index += 1

CalculateClassProbability : Calculate probability of each class based on data.<br/>

          for key in self.ClassF:
            self.ClassF[key] = self.ClassF[key] / self.totalDocument
            
CalculateTermProbablity : Predict probability of term based on naïve bayes <br/>

        for key in self.ClassF:
            #print((self.ClassTermCount[key]))
            currentProb = self.ClassF[key]
            #with each term loop will expand to P(x1|y)P(x2|y)..P(xn|y) P(y)
            for term in terms:
                currentProb = currentProb * (( self.TermClassFrequency[term].get(key,0)+1) /( len(self.ClassTermCount[key]) + len( self.unique_terms)))

            self.queryClassPrabablity[key] = currentProb
            print(currentProb)
            if currentProb > probablity:
                probablity = currentProb
                className = key

<br/>
For Code and Implementation detail visit [Git hub](https://github.com/BhaskarTrivedi/QuerySearch_Recommentation_Classification)<br/><br/>

Dataset <br/>
Dataset primary refer as a collection of similar type of index data which can be used for special purposes. With time and technology data set are becoming huge and tradition approach (normal SQL queries) is not sufficient to store and retrieve data from data set. To tackle this situation big data come into picture. It helps with fast data retrieval with proper indexing. The first step towards developing any recommender system is to finalize data set. According to data set we can plan our approach and decide which feature is important to create our recommender system. Click here to visit [movielens](https://grouplens.org/datasets/movielens/).
To explore more dataset [click here](https://www.kdnuggets.com/2016/02/nine-datasets-investigating-recommender-systems.html).
More [movie dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset#movies_metadata.csv).



