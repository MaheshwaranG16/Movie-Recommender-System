# Movie Recommender System
 
**Overview**:

Welcome to the Movie Recommender System repository, where we explore and develop personalized movie recommendation algorithms using various machine learning techniques. A movie recommender system is a type of information filtering tool that helps users discover movies that match their tastes and preferences. These systems analyze various types of data to provide personalized recommendations.

**Business Problem**:

The entertainment industry thrives on engaging audiences with content that matches their preferences. A robust movie recommender system enhances user experience by providing personalized movie suggestions, which increases user satisfaction and engagement. By analysing user behaviour and movie attributes, we can uncover patterns and develop algorithms to predict user preferences, ultimately driving higher viewership and retention rates.

**Imported Libraries**:

The data wrangling process is documented in the Movie_Recommender_Analysis.ipynb Python script. The provided code imports essential libraries and modules for developing a movie recommender system. It includes Pandas and NumPy for data manipulation and analysis, Matplotlib and Seaborn for data visualization, and SciPy for statistical operations. The ast module's literal_eval is used for safely evaluating expressions. Scikit-learn is employed for feature extraction and similarity calculations, particularly using TfidfVectorizer, CountVectorizer, linear_kernel, and cosine_similarity. NLTK is utilized for text processing with tools like SnowballStemmer and WordNetLemmatizer. Finally, the Surprise library facilitates building and evaluating recommender systems with functionalities such as Reader, Dataset, SVD, and accuracy measurement, alongside cross-validation and dataset splitting tools. This comprehensive setup enables efficient data preprocessing, feature extraction, model building, and performance evaluation for a movie recommendation system.

**Datasets:**

In this notebook, I will attempt at implementing a few recommendation algorithms (content based, popularity based and collaborative filtering) and try to build an ensemble of these models to come up with our final recommendation system. With us, we have two MovieLens datasets.

1. The Full Dataset: Consists of 26,000,000 ratings and 750,000 tag applications applied to 45,000 movies by 270,000 users. Includes tag genome data with 12 million relevance scores across 1,100 tags.
2. The Small Dataset: Comprises of 100,000 ratings and 1,300 tag applications applied to 9,000 movies by 700 users.

Dataset Source: [The Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)

**Visualizations:**

[Movie Analysis Dashboard](https://public.tableau.com/shared/FW96MF497?:display_count=n&:origin=viz_share_link)
1. [Top 10 Popular Movies](https://public.tableau.com/shared/PD2G2SQ49?:display_count=n&:origin=viz_share_link)
2. [Top 10 Grossing Movies](https://public.tableau.com/shared/6TWKRSD79?:display_count=n&:origin=viz_share_link)
3. [Revenue Over Years](https://public.tableau.com/shared/NMPNR8B96?:display_count=n&:origin=viz_share_link)
4. [Budget Over Years](https://public.tableau.com/shared/582PXXNH8?:display_count=n&:origin=viz_share_link)
5. [Top 10 Highest Paying Directors](https://public.tableau.com/shared/Y6QX9TWTW?:display_count=n&:origin=viz_share_link)

**Conclusion**:

In this notebook, I have built 4 different recommendation engines based on different ideas and algorithms. They are as follows:
1.	Simple Recommender: This system used overall TMDB Vote Count and Vote Averages to build Top Movies Charts, in general and for a specific genre. The IMDB Weighted Rating System was used to calculate ratings on which the sorting was finally performed.
2.	Content Based Recommender: We built two content based engines; one that took movie overview and taglines as input and the other which took metadata such as cast, crew, genre and keywords to come up with predictions. We also devised a simple filter to give greater preference to movies with more votes and higher ratings.
3.	Collaborative Filtering: We used the powerful Surprise Library to build a collaborative filter based on single value decomposition. The RMSE obtained was less than 1 and the engine gave estimated ratings for a given user and movie.
4.	Hybrid Engine: We brought together ideas from content and collaborative filterting to build an engine that gave movie suggestions to a particular user based on the estimated ratings that it had internally calculated for that user.
