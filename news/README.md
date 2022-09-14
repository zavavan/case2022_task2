# Data

## Description

The news corpus used in this Task is a collection of articles in English language spanning the time range July 27, 2020 through October 26,2020 from a large set of news sources in the U.S.
We used public APIs when available and scraped the newspaper web pages otherwise. For example, we used the New York Times Archive API. 
To get the data from this API, run the below code, changing "your_api_key" with your NYTimes api key. You can get a key from https://developer.nytimes.com/get-started

`python get_data.py your_api_key`

After you run this, a file named "out.json" will be created. Each line of this file will be JSON object containing information about an article. The keys are as follows:
* pub_date -> Publication date of the article
* abstract -> Abstract of the article
* snippet -> A snippet from the article text
* lead_paragraph -> The lead paragraph from the article
* url -> The URL of the article

The articles are filtered by checking the occurrence of keywords ["covid","coronavirus"] in the top two sentences of the articles. Overall the collection contains around 122k articles.
Data are released in a single tab separated file, whose format is:

[id	date	title	abstract]

Please contact ali.hurriyetoglu@gmail.com or hristo.tanev@ec.europa.eu for further details on this dataset.
