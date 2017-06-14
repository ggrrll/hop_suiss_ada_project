# Hop Suisse - public repo for our [ADA](http://ada.epfl.ch) project          


In this project we performed data scraping, analysis and visualization from the
[Datasport](https://www.datasport.com) website, focusing on records of running races.

A more detailed description of the steps followed can be found
[below](#working-steps) and on the [poster](poster.pdf). 


## Team

The project is run by a new team, obtained by merging two previous ADA teams:

- [Ondine Chanon](https://github.com/ochanon)
- [Maxime Peschard](https://github.com/maximepeschard)
- [Stefano Savarè](https://github.com/deatinor)
- [Gianrocco Lazzari](https://github.com/ggrrll)
- [Antonio Iubatti](https://github.com/antonioiubatti93)


## Workflow

Here is a breif list of the steps we went through in our ourject.

* [project proposal](1-project_proposal/project_proposal_hop_suisse.md) :

> Describes guideline and goals of the project.

* [global parsing](2-global_parsing/global_parsing.ipynb) :

> From the datasport main page, we make requests to extract all names, dates and
> places of every running competition, as well as the urls where to find the
> results.
>
> Results :
> * [`links2runs.csv`](datasets/links2runs.csv)

* [ranking parsing](3-ranking_parsing/parsing_datasport.ipynb) : 

> From every url found in `links2runs.csv`, we get all information about every
>  race, namely the information on each runner: name, age,
> category, ranking, pace, etc. Note that given the way Datasport displays
> his records, the parsing step was quite non trivial.
>
> Results :
> * [`pickle`](https://drive.google.com/file/d/0BypxDaHZHjhfYTBsMGM2WVlFdkU/view) (temporarily hosted on Google Drive)

* [weather](4-weather/weather_utils.py) :

> From `links2runs.csv` we consider every date and place and search for the corresponding
> weather and temperature in order to investigate correlation between the runners' performances and the
> weather/temperature. 
> Due to the API used, such weather information for races older than
> July 2008 is not available.
> 
> Results :
> * [`races-information-weather.csv`](datasets/races-information-weather.csv)

* [gathering information](5-gathering_information/races_information.ipynb) :

> Extra steps to build on top of `links2runs.csv` a more complete table
> containing the scraped information plus the weather information and GPS
> coordinates for each location when available.
> 
> Results :
> * [`races-information.csv`](datasets/races-information.csv)

* [data analysis](6-data_analysis) :

> Data analysis performed both on particular races like Lausanne Marathon and on the
> entire dataset - in order to run the analysis on the full dataset, one should first download the
[`pickle`](https://drive.google.com/file/d/0BypxDaHZHjhfYTBsMGM2WVlFdkU/view) file

* [visualization](7-visualization) :

> Our goal is to display the gathered data and the analysis on a website, in a
> more "user-friendly" way than Datasport. 
> Our [hopsuisse website](https://hopsuisse.github.io) is the result, for which we used GitHub
> Pages, Jekyll, D3.js, Leaflet, and other tools.

* [video](8-video):

> We created a [short video](https://www.youtube.com/watch?v=MyvbnOXHShw) 
> in order to help visualize the large Datasport dataset in a concise way. This video was inpsired by the popular
[Hans Rosling's video](https://www.youtube.com/watch?v=jbkSRLYSojo).

