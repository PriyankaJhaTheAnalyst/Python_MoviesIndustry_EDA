# Project Overview
Our hypothetical Company  has announced that they would like to get into the movie industry. They will be creating a studio, however they have no knowledge of the movie industry. Our goal is to collect, clean, and analyze movie data from a variety of sources so that we can provide recommendations to our company that will allow them to be successful in the movie industry.

# Data and Exploration
**Web-scrapping** <br />
The web-scraped data used in this project was collected from the following sources:

1. https://www.the-numbers.com/movie/budgets/all/1
2. https://www.imdb.com/search/title/?title_type=feature&num_votes=5000,&languages=en&sort=boxoffice_gross_us,desc&start=1&explore=genres&ref_=adv_nx
3. https://www.boxofficemojo.com/chart/most_theaters/?by_studio_type=major
4. https://www.moviefone.com/movies/2019/?page=1
5. https://en.wikipedia.org/wiki/List_of_Academy_Award-winning_films

**Exploration Questions** <br />
In our analysis we explore and answer the following questions:
1. What are the most profitable movies and how much should you spend?
2. Which movie genres are most commonly produced and does quantity equate to higher net profits?
3. What is the best time of the year to release a movie?
4. Which actors and directors tend to add the most value?
5. How much money should you spend to win an Oscar?
6. What impact, if any, does runtime and movie rating have on Net Profit, Profit Margin and IMDb rating?
7. Sticking to our analysis of Net Profit and Profit Margin, what should Microsoft determine to be the baseline for sustainable success?
8. Based on the success of current competitors, which should we look to for best practices?


## Question 1: What are the most profitable movies and how much should you spend?
To answer this question and provide a recommendation we'll make use of a budgets dataframe called `imdb_budgets_df`. Our analysis will require that we use the data to calculate profit and profit margin.

```
imdb_budgets_df['Profit'] = imdb_budgets_df['Worldwide Gross'] - imdb_budgets_df['Production Budget']

imdb_budgets_df['Profit_Margin'] = (imdb_budgets_df['Worldwide Gross'] - 
                                    imdb_budgets_df['Production Budget'])/imdb_budgets_df['Worldwide Gross']
```

We will also create two columns called `Adjusted_Budget` and `Adjusted_Profit` where we recalculate a movie's budget and profit to account for inflation and allow us to perform analysis based on the value of the 2020 dollar.

We examine the overall trend of budget versus profit to see if there's any correlation.





