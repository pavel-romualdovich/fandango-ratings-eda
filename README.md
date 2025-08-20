# Student EDA based on Fandango movie ratings
**EDA goal**: to perform an analysis inspired by the article [Be Suspicious Of Online Movie Ratings, Especially Fandango’s](http://fivethirtyeight.com/features/fandango-movies-ratings/) and compare the results with the conclusions presented in the article 

## Project structure
```
fandango-ratings-eda/
├── data/                               # All data, used in the project
│   ├── fandango_score_comparison.csv
│   └── fandango_scrape.csv
└──  notebook.ipynb                     # Jupyter notebook with all the EDA
```

## EDA structure
- [Part 1. Fandango ratings analysis](notebook.ipynb#part-1-fandango-ratings-analysis)
  - [Uploading data](notebook.ipynb#uploading-data)
  - [Exploring the relationship between data](notebook.ipynb#exploring-the-relationship-between-data)
- [Part 2. Analysis of Fandango ratings in comparison with ratings of other companies](notebook.ipynb#part-2-analysis-of-fandango-ratings-in-comparison-with-ratings-of-other-companies)
  - [Uploading data](notebook.ipynb#uploading-data-1)
  - [A short analysis of ratings from other companies](notebook.ipynb#a-short-analysis-of-ratings-from-other-companies)
  - [Comparison of Fandango ratings with ratings of other companies](notebook.ipynb#comparison-of-fandango-ratings-with-ratings-of-other-companies)

## Used data
The original data used in this project is [publicly available](https://github.com/fivethirtyeight/data/tree/master/fandango) and consists of two CSV files:
- [fandango_score_comparison.csv](data/fandango_score_comparison.csv);
- [fandango_scrape.csv](data/fandango_scrape.csv).

### fandango_score_comparison.csv
It contains all films for which there are ratings on Rotten Tomatoes, Metacritic, and IMDb. The data was uploaded on August 24, 2015.
Feature | Defenition
--- | -----------
FILM | The name of the film
RottenTomatoes | "Rotten Tomatoes" critics' ratings for this film
RottenTomatoes_User | "Rotten Tomatoes" user's ratings for this film
Metacritic | "Metacritic" critics' ratings for this film
Metacritic_User | "Metacritic" user's ratings for this film
IMDB | "IMDb" user's ratings for this film

### fandango_srcape.csv
It contains information about films that the authors of the article uploaded from Fandango.
Feature | Defenition
--- | ---------
FILM | The name of the film
STARS | The number of stars on Fandango.com
RATING | Value read from the HTML page. This is the average rating of the film
VOTES | The number of votes of users who wrote a review about the film

## Conclusion
Based on the plots and statistical hypothesis testing, the following conclusions can be confirmed:
- The number of stars shown for movies on Fandango was, on average, inflated compared to their actual ratings on the website;
- Fandango's ratings were statistically significantly higher than those of other rating platforms.

Additionally, data analysis and visualization skills were improved, in line with the stated goal.
## Installation
1. Clone the repository:
```shell
git clone https://github.com/pavel-romualdovich/fandango-ratings-eda.git
cd fandango-ratings-eda
```
2. Create and activate a virtual environment:
```shell
python3 -m venv venv
source venv/bin/activate
```
3. Install the required packages:
```shell
pip install -r requirements.txt
```
4. Set Jupyter venv kernel:
```shell
python -m ipykernel install --user --name=venv --display-name "Python (venv)"
```
5. Launch the notebook and chose "Python (venv)" kernel:
```shell
jupyter notebook notebook.ipynb
```
