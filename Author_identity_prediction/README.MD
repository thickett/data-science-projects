# Author Identity Prediction
## Project overview

Using web-scraped, un-labeled text data to try and identity an authors identity, and by extension, how their personaility is captured within their written work.

## Project Breakdown
### 1) Gathering data
* Combined the *Selinium* and *Scrapy* python packages to create an *asynchronous* web scraper capable of searching through dynamic websites.
* used the above mentioned web scraper to gather data on all authors who have published work to the BBC 
  * Note: The BBC was chosen for three reason:
    * Web scraping article data falls within their terms and conditions.
    * Significant amount of varied text data.
    * Significant number of different authors.


### 2) EDA, Data Cleaning, and  pre-processing.
* Basic checks on the quality of our data:
  * Has the data we have scraped come through in a reasonable format? Is anything missing?
  * Checking for missing values, outliers, and the most important data.
  * Check the distribution of articles across our authors to ensure we take the right approaches when we reach the modelling stage.
  
* Created several custom functions to:
  * Remove unwanted text data using regular expressions.
  * Fixing inconsistent data.
  * Tokenized text and removed un-wanted stop words.
    * *Note:* We *do not* lemmatize the tokens, and we take care with which stop words we remove. Remember, we are trying to understand the *differences* between authors. normalization of the text will limit our ability to do this.
 
 
 
 ### 3) Feature Engineering 
* modify text fields to account for common collocations
* Create TF-IDF vectors
* Latent Dirichlet Allocation (LDA) for generating likelihood-probabilities for generated topics.

 ### 4) Model building
 
* Compared three models;
  * Multinominal Naieve Bayes, sklearn'S GBM implementation, XGBoost
  * HyperOpt was used for hyper-parameter optimisation. 
  * f1-scores, time-to-fit, and epoch vs performance curves were used to compare models.
  
  ![image](https://user-images.githubusercontent.com/82325813/204159876-510a5fda-21f4-4131-8932-81b465609638.png)

