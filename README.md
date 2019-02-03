# Instagram-Image-Analysis

****************************************************************************
I have been leaning on how to do Text Analytics and Natural Language Processing on wide platform of social media like Public Forums (Edmunds, Yelp etc.), Instagram, Twitter etc.

This is the first Project of the Series #User-Generated-Content-Analysis. Since this is a learning process, you will see a gradual improvement in the techniques used and also reduction in the number of assumption. 

As for this project: 

Things Learned:
* Lift Calculation
* Word-Frequency count
* Natural Language Processing
* Stemming & Lemitization
* Importance of word replacement
* Sentiment Analysis
* Cosine Similarity
* Engagement score
****************************************************************************

# Project 4 of Series #User-Generated-Content-Analysis

The aim of this project is to analyze the NatGeo page on Instagram to analyze the engagement of the image with the users. To explain this further the aim of this project is to find that does the post captions create more engagement among the users or if image labels (obtained from Google Vision API - in our case) were used they would have created more engagement or finally if the combination of these two were used then the engagement would have been high.

The flow of this project goes as follows:

* On Instagram, choose the National Geographic (natgeo) page (do not use hashtags). Write a scraper or use the Web Scraper to extract (i) image URLs (do not extract video URLs, it may end up costing you a lot of money to run analytics on video), (ii) post caption (the text description of a post), (iii) # likes and (iv) # comments. We don’t need actual comments for this assignment. Scrape 250-500 image posts. 

* Using the image URLs, obtain image labels from Google Vision cloud. For Google Vision API, look here: https://cloud.google.com/vision/docs/quickstart

* Create a metric for engagement by using a weighted sum of # likes and # comments. However, first normalize # likes and # comments such that they both have values between 0 and 1. We can scale the # likes by dividing by the maximum # likes (for a post) in the data and do the same for # comments, so that # likes and comments will be in the range [0,1]. Now create an engagement score = .4*# likes (normalized) + .6*# comments (normalized). Define High (1) and Low (0) engagement based on whether the engagement score is above or below the median value.  

* Run a logistic regression with Engagement (binary) as the dependent variable, and the image labels as independent variables. What is the accuracy (show the confusion matrix)? The objective is to find: What accuracy do we get by using the post caption words as the independent variables instead of image labels? Finally, what accuracy do we get by combining the image labels and post captions and using them as independent variables? What can we conclude from our analysis?

Note: Doing a word frequency analysis and word replacement on the image labels as well as captions will increase the accuracy of prediction. For better results, TF-IDF scores should be used. 

* Perform topic modeling (LDA) on the image labels. Choose an appropriate number of topics. It can be started with 5, but adjust the number up or down depending on the word distributions that we get. 

* Based on the above analysis, What advice would can we give National Geographic if it wants to increase engagement on its Instagram page.   


