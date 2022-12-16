![image1](https://github.com/NBYHO/Microsoft-project-1/blob/main/images/RT_300EssentialMovies_700X250.jpeg)
# Microsoft Movies data analysis project

**Authors**: Ngoc Ho

## Overview
This project analyses the movies market using data from IBDM database, Box office Mojo and The Numbers. Descriptive data analysis of title rating and domestic/worldwide gross showed the most popular and top gross movie genre are Action, Adventure and Sci-Fi with median runtime between 80-100 minutes. This data analysis showed the profit varies seasonally and the most profitable season is Summer. The budget required to make a movie around 30 millions. Results from this data analyis can guide Microsoft's decision on genre of movies, production budget and release timeline. 

## Business Problem
Microsoft is interested in bulding a movie studio. 

To successfully set up a new movie studio, we have to consider:
- Properties of a popular and profitable such as genre, runtime 
- Business aspects such as budget, profit margin
- Strategy aspects such as best time to release, marketing strategies, etc,.

Data analytic questions that might help explores the these points:
- Which movie genres has highest rating/most popular/most gross
- What is a typical runtime of top rating movies?
- Which season best to release a movie?
- What is the average budget for a movies?
- Does higher budget correlates to higher profit?

## Data
In this project we use data from:
IMBd

IMDb database consists of multiple tables on various information about movies. The two dataset we will be using are : title.basics and title.ratings.
The title.basics table includes movie titles, release year, and genres with 146144 titles and 6 columns. The title.ratings table includes average movie rating and number of votes with 73856 rows x 3 columns. The primary key for both tables is tconst.

Box office Mojo 

Box office Mojo dataset contains information on 3387 movies entries and 5 columns of data points of their domestic, foreign gross, studio and production year. 
Target variables : domestic and foreign gross and studio.
Target data include genres, runtime minutes, average rating and number of votes. 

The Numbers 

The Numbers dataset contains records of 5782 movies entries with 6 columns containing data points on the movie's production budget, domestic gross, worldwide gross and release date from 1915 to 2020.
Target variables: production budget, domestic, worldwide gross and release date.

## Methods
We will be utilising pandas functions to find means, median, count correllation and trends to establish relationship between variables. Seaborn and matplotlib will helps us transform our analysed results into visualisation to help aid understanding results and draw conclusions.  

For each dataset we apply the following process:
1. Data exploration:*** 
    1.1 import data csv using pd.read_csv()***
    2.1 Display and inspect dataframe using .head() and .info()***
2. Data preparation 
    2.1. Data cleaning 
        a. check for null values and replace them appropriately 
        b. check for duplicates and deal with them accordingling 
        c. renaming columns and drop irrelevant columns 
    2.2. Merging dataframes to group target variables together in order to perform functions and study their relationship
 3. Data modelling 
    3.1 To find which genre is the most popular with high rating, we merged title.basics and title.rating and limit only genres with rating >= 8 then find the genre with the highest number of votes. 
    3.2 To find the typical runtime of high performing movies we find the median runtime of all movies with rating >=8 and also use histogram to visualise which timeframe most movies concentrate. 
    3.3 We then merge title.basics, title.rating and bom.movie_gross to investigate which movie genre has highest gross with high rating and number of votes 
    3.4 Lastly we investigate which season of the year is the most profitable to release a movie base on domestic and worlwide gross variables in The Numbers dataframe. We use return on investment (ROI) formula to measure a movie's performance. We also find a typical budget for a high rated movies and explore the correlation between production budget and profit using regression plot.  

## Results
1. The top 5 most common genres of movies are, Documentary, Drama, Comedy, Horror, Comedy/Drama however Action,Adventure,Sci-Fi is the genre with the highest votes in movies with average rating >=8. It also has the highest gross domestically and globally.

### Visual 1: Top 5 genres with highest votes and average rating>=8
![graph1](https://github.com/NBYHO/Microsoft-project-1/blob/main/images/fig_1.png)

### Visual 2: Top 10 genres with highest gross domestically and globally
![graph2](https://github.com/NBYHO/Microsoft-project-1/blob/main/images/fig_2.png)

2. The typical runtime for movies with average rating >=8 is 87 minutes. Histogram of runtime of all movies with average rating >=8 showed most movies concentrate around 80-100 minutes. 

### Visual 3: Typical runtime for movies with average rating >=8
![graph3](https://github.com/NBYHO/Microsoft-project-1/blob/main/images/hist.png)

3. Summer has the highest median ROI (103% globally and 7% domestically while all other season's ROI are negative domestically)

### Visual 4: Return on Investment by season
![graph4](https://github.com/NBYHO/Microsoft-project-1/blob/main/images/bar.png)

4. On average, production budget of movies is between 15-20 millions USD however top 20% profitable movies domestically and globally has median budget about 30 millions and 57.75 millions respectively.

5. Investigation into the relationship of budget and net profit showed a weak correlation ( r= 0.01) between production budget and domestic profit yet there is a  mild- moderately positive correlation (r=0.61) between production budget and worldwide profit.

### Visual 5: Correlation between budget and profit
![graph5](https://github.com/NBYHO/Microsoft-project-1/blob/main/images/fig_10.png)


## Conclusions

This analysis leads to 3 recommendations for Microsoft new movie studio:
- **Focus on Drama, Documentary, Action/Adventure/Sci-fi movies with runtime around 80-100 minutes in Summer and Action, Animation, Adventure in Winter.** These movies tend be the highest gross domestically and internationally. They tend to have higher number of votes by audience and has decent average rating. The median runtime for movies with average rating >=8. 
- **Plan release date of movies around June - August during summer break OR winter between December-Feb (Holidays season)** Movies released in summer tends to have higher return on investment (ROI) overall (103% globally and 7% domestically while all other seasons have negative ROI domestically). However data is more variable so projection might not be as accurate. Winter on the otherhand has narrower range which is less variable and boxplot showed distribution is postively skewed meaning higher frequency of higher profit. 
- **Production budget around 30 millions domestically and upto 60 millions internationally** For the top 20% highest profit movies, the median production budget is 30 millions while the median production budget for all movies is around 15-20 millions.  Higher budget does not equate to higher profit as correlation between production budget is weak domestically and somewhat mildly correlated internationally. 

### Limitation:¶
**Runtime:** significant nulls values. We also did not taken movies with average rating less than 8. Unclear if runtime has any effect on average rating
**Data currency:** IMBd Data stops at 2018 and The numbers data stops at 2020 - having access to more recent data can help us visualise the movie industry/market in recovery period post COVID. This will help us predict future trends more accurately
**Missing data:** Box office Moji bom.movie_gross has large amount of missing data in foreign gross - reduced credibility of analysis.

 ### Future Considerations:

- Analyse other performance metrics such as critic, reviews and investigate other databases. This will help predicting a movie performance/profitablity and budget more accurately 
- Analysing runtime, average rating and profit. This will help establish whether runtime would affect user rating or generate more profit. 
- Analysing data on directors, writers, actors and crews. This would allow more efficiency to for staff recruitment, recruiting the right person  
- Research in competitors business model. This would allow us to have insights into their competitor business model to help build our business.

## For More Information

Please review our full analysis in [our Jupyter Notebook](dsc-phase1-project-template.final.ipynb) or our [presentation](DS_Project_Presentation.pdf).

For any additional questions, please contact **Ngoc Ho, yen.ho993@gmail.com**

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── dsc-phase1-project-template.ipynb   <- Narrative documentation of analysis in Jupyter notebook
├── DS_Project_Presentation.pdf         <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
```
