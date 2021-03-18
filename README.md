### Goodreads Web Scraping 

The purpose of this project to build a web scraping script to obtain 200 pages of books related to Computer Science, and do statistical tests to see does factors, the number of pages, rating counts, review counts, and editions leads to a higher average rating.

### Datasets
The dataset is obtained from goodreads.com under the search page. We will be using the search bar to search books for Computer Science. The search pages only extended to 200 pages, which contains 2000 books of information. Each book has a personalized web link that allows users to click in to check for book information. Each book will have a title, and may or may not have the following information as well:

1. Book title ***(Must Have)***
2. Author  
3. Average rating 
4. Rating count
5. Review count
6. Number of Page
7. Format
8. Languages
9. First Publish Year
10. Editions 
11. ISBN
12. Link

### Install & Quickstart
We will be using MongoDB to store our data during the Web Scraping process. That allows us to do Exploratory Data Analysis simultaneously without the Web Scraping process is complete. 

As a result, you will need to install Docker, Docker Compose, and register a Docker Hub account. Then, we will pull the MongoDB image using Docker. Inside your terminal, you should already able to run Docker "Hello World", then you should run the following command to pull MongoDB:
1. Using Mongo:

```$ docker run --name mongoserver -p 27017:27017 -v "$PWD":/Your-Working-Directory -d mongo```

2. Starting Mongo

```$ docker start mongoserver```

### Part1: Web Scraping
We will have two seperate juypter notebook, one for web scraping purpose, and another is for EDA purpose.

### Part2: Exploratory Data Analysis & Statistical Test
We can do simple EDA while the web scraping is still spinning and understand our dataset in advance. After all data (books) are being collected and stored in our MongoDB, then we can do statistical tests to answer our question. 

### Findings

