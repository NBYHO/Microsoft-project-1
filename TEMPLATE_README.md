# Microsoft Movies data analysis project

**Authors**: Ngoc Ho

## Overview
This project analyses the movies market using data from IBDM database, Box office Mojo and The Numbers. Descriptive data analysis of title rating and domestic/worldwide gross income showed the most popular and top gross movie genre are Action, Adventure and Sci-Fi with median runtime between 80-100 minutes. This data analysis showed the profit varies seasonally and the most profitable season is Summer. The budget required to make a movie around 30 millions. Results from this data analyis can guide Microsoft's decision on genre of movies, production budget and release timeline. 

## Business Problem
Microsoft is interested in starting up a movie studio however they lack knowledge about the movie market. They would like to know which movie is doing well to help them decide which movie to create. By finding out which genre has the highest rating and has the most gross income domestically and internationally which give Microsoft insights to decide which genre of film to make, set budget and release date for maximum profit. 

To successfully set up a new movie studio, we have to consider:
- Components of the film such as genre, runtime, casts, crews 
- Business aspects such as budget, profit margin
- Strategy aspects such as best time to release, marketing strategies, etc,.

Data analytic questions that might help explores the these points:
- Which movie genres has highest rating/most popular?
- Which movie genres has high grossing? Which current studio is making top grossing movies?
- What is a typical runtime of top rating movies?
- Which season best to release a movie?
- What is the average budget for a movies?
- Does higher budget correlates to higher profit?

## Data

The internet movie database (IMDb) is an online database of information related to films, televison series, home videos, video games and streaming content online. This database includes title, genre, ratings and number of votes. the IMDb database is updated daily. We also used data from IMDb subsidiary Box Office Mojo and The number database for movie financial details such as release date, budgets, domestic and worldside box office gross. Our target variable are genre, average rating and number of votes to determine which genre is most popular and has high rating. We also target variables such as domestic, worldwide box office gross and budget to identify most profitable genre and which release season optimise profit. We will be utilising pandas functions to find means, median, count correllation and trends to establish relationship between variables. Seaborn and matplotlib will helps us transform our analysed results into visualisation to help aid understanding of our dataset and decision making. 


## Methods

Describe the process for analyzing or modeling the data. For Phase 1, this will be descriptive analysis.

***
Questions to consider:
* How did you prepare, analyze or model the data?
* Why is this approach appropriate given the data and the business problem?
***

## Results

Present your key results. For Phase 1, this will be findings from your descriptive analysis.

***
Questions to consider:
* How do you interpret the results?
* How confident are you that your results would generalize beyond the data you have?
***

Here is an example of how to embed images from your sub-folder:

### Visual 1
![graph1](./images/viz1.png)

## Conclusions

Provide your conclusions about the work you've done, including any limitations or next steps.

***
Questions to consider:
* What would you recommend the business do as a result of this work?
* What are some reasons why your analysis might not fully solve the business problem?
* What else could you do in the future to improve this project?
***

## For More Information

Please review our full analysis in [our Jupyter Notebook](./dsc-phase1-project-template.ipynb) or our [presentation](./DS_Project_Presentation.pdf).

For any additional questions, please contact **name & email, name & email**

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── dsc-phase1-project-template.ipynb   <- Narrative documentation of analysis in Jupyter notebook
├── DS_Project_Presentation.pdf         <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
```
