Week 11 Assignment

# Data-Collection-Challenge

In the Data-Collection-Challenge, you will utilize your web-scraping and data analysis skills to gather information and analyze Mars news articles and weather data. You will use Splinter and Beautiful Soup to identify HTML elements to extract information. 


## Prerequisites

Before working on the Data-Collection-Challenge, ensure you complete the following requirements:

- Install VS Code, Python, and Splinter on your machine (can use Jupyter Notebook)
- Import Pandas, matplotlib, BeautifulSoup, and Browser
- Create a new repository called 'data-collection-challenge' in GitHub with README and .gitignore files.


## Repository Setup

Repository Setup:
  - Create a new repository called 'data-collection-challenge' in GitHub with a README file
  - Copy the SSH key in GitHub
  - Navigate into the working directory 
  - Clone SSH key in directory
    - Import both starter codes, part_1_mars_news and part_2_mars_weather into the directory
  - Git add, commit, and push changes into the repository

```
Navigate into the working directory. 
git clone (add you ssh key)
cd 'data-collection-challenge''
git add .
git commit -m "Pushing challenge work"
git push 
```


## Instructions

Ensure you have downloaded the starter code files to start the challenge.

The challenge is separated into two parts:

    - Part 1: Scrape Titles and Preview Text from Mars News 

    - Part 2: Scrape and Analyze Mars Weather



PART 1: Scrape Titles and Preview Text from Mars News 

Open the ```part_1_mars_news.ipynb``` starter code in VS Code or Jupyter Notebook and complete the following steps to scrape the Mars News website.  

1. Use Splinter to automate browser actions to visit the Mars news website.
2. Create a Beautiful Soup Object.
3. Extract Titles and Preview Text.
4. Store the results in a Python list. 
5. Exist the Browser.


PART 2: Scrape and Analyze Mars Weather

Open the ```part_2_mars_weather.ipynb``` starter code in VS Code or Jupyter Notebook and complete the following steps to scrape the Mars weather data. 

1. Use Splinter to automate browser actions to visit the Mars weather data.
2. Create a Beautiful Soup Object.
3. Extract the rows of data. 
4. Store the data in a Python list and convert it into a Pandas dataframe. 
5. Prepare and Analyze Weather Data:  
    - How many months exist on Mars?
    - How many Martian day's worth of data exist in the scraped dataset?
    - Calculate which month, on average, has the lowest temperature and create a bar chart.
    - Calculate which month, on average, has the lowest atmospheric pressure and create a bar chart.
    - How many terrestrial (Earth) days exist in a Martian year?
    - How many days elapse on Earth when Mars circles the Sun once?
    - Plot the daily minimum temperature.
6. Save dataframe to a CSV file.
7. Exist the Browser.


## Mars News Example 

```VS Code
# Loop through the text elements
# Extract the title and preview text from the elements
# Store each title and preview pair in a dictionary

for article in articles:
    title = article.find('div', class_='content_title').get_text()
    preview = article.find('div', class_='article_teaser_body').get_text()
    mars_news_articles.append({'title': title, 'preview': preview})
```


## Mars Weather Example

```VS Code
# Create an empty list
temp_data = []

# Loop through the scraped data to create a list of rows
for row in rows:
    column_values = row.find_all("td")
    list = []
    for value in column_values:
        list.append(value.text)
    temp_data.append(list)
temp_data
```


## Acknowledgements

I want to mention the following individuals and resources for their assistance and support throughout this assignment: 
- Study group members
    - Omid Khan - omidk414@gmail.com - omidk414
    - Evan Wall - - ewall@escoffier.edu - Ewall24
- Class instructor Elias and Class TA Brian and Karen
- Xpert Learning Assistant and ChatGPT
- HTML Cheat Sheet (https://web.stanford.edu/group/csp/cs21/htmlcheatsheet.pdf)
