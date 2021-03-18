![Goodreads](https://s2982.pcdn.co/wp-content/uploads/2020/10/goodreads-logo-700x373.jpg.optimal.jpg)
### Goodreads Web Scraping 
The purpose of this project to build a web scraping script to obtain 200 pages of books related to Computer Science, and do statistical tests to see does factors, the number of pages leads to a higher average rating.

### Dataset
The dataset is obtained from [Goodreads](https://www.goodreads.com/) under the [search bar page](https://www.goodreads.com/search?page=1&q=Computer+Science&qid=iHFbTUVsHL&search_type=books&tab=books&utf8=%E2%9C%93). We will be using the search bar to search books for **Computer Science**. The search pages only extended to **100 pages**, which contains **2000 books** of information (1 search page contains 20 books). Each book has a personalized web link that allows users to click in to check for book information. Each book must have a title, and may or may not have the following information:

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

#### Search Bar Page
![searchbar](https://raw.githubusercontent.com/HailinDu/Goodreads-Web-Scraping/main/Images/Search_Bar.PNG?token=AMMQHZKQ366DH5ZDOMGMITLAKMBAA)
#### Book Info from Sublink
![sublink](https://raw.githubusercontent.com/HailinDu/Goodreads-Web-Scraping/main/Images/Book_Sublink_Info.PNG?token=AMMQHZPGB3H7LFUKKLIJLTLAKMA7A)

### Install & Quickstart
We will be using [MongoDB](https://www.mongodb.com/) to store our data during the Web Scraping process. That allows us to do Exploratory Data Analysis simultaneously without the Web Scraping process is complete. 

As a result, you will need to install [Docker](https://docs.docker.com/get-docker/), [Docker Compose](https://docs.docker.com/compose/install/), and register a [Docker Hub](https://hub.docker.com/) account. Then, we will pull the [MongoDB image](https://hub.docker.com/_/mongo) using Docker. Inside your terminal, you should already able to run Docker [Hello World](https://hub.docker.com/_/hello-world), then you should run the following command to pull MongoDB:
1. Using Mongo:

```$ docker run --name mongoserver -p 27017:27017 -v "$PWD":/Your-Working-Directory -d mongo```

2. Starting Mongo

```$ docker start mongoserver```

![workflow](https://raw.githubusercontent.com/HailinDu/Goodreads-Web-Scraping/main/Images/WorkFlow.PNG?token=AMMQHZIDAF6YPKFHG4HYRC3AKL7V4)

### Part1: Web Scraping
We will have two seperate juypter notebook, one for web scraping purpose call ```Goodreads Web Scraping Notebook.ipynb```, and another is for EDA purpose call```Goodreads  Exploratory Data Analysis & Statistical Tests.ipynb```.

### Part2: Exploratory Data Analysis & Statistical Tests
We can do simple EDA while the web scraping is still spinning and understand our dataset in advance. After all data (books) are being collected and stored in our MongoDB, then we can do statistical tests to answer our question. 

### Findings
* Average Rating (No signifcant difference between Books with longer number of pages of short number of number of pages)
* Review Count (No significant difference)
* Number of Book Editions (No significant difference)
* **Rating Count** (sigificant difference acorrding to the test!)

![Findings](https://raw.githubusercontent.com/HailinDu/Goodreads-Web-Scraping/main/Images/Findings.PNG?token=AMMQHZMC7GR5BV7KOSHJ3TDAKMBBI)
1. A book with more pages **DOES tend** to be rated more often according to the Statistical T-Tests.
2. A Book has long number of pages **DOES NOT** lead to a higher Average Rating, Reviews Count, and Editions according to the Statistical T-Tests.

## Tableau (Data Visualization)
![Dashboard](https://raw.githubusercontent.com/HailinDu/Goodreads-Web-Scraping/main/Images/Tableau_Dashboard.png?token=AMMQHZOI5O63TANDNFQVMNDAKMA4K)
