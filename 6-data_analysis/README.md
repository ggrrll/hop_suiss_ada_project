# Data analysis


In this folder we present our data analysis on the full dataset,
 as well as on the Lausanne Marathon 2016.


* [`lausanne_marathon_analysis:`]() exploratory statistics on the Lausanen Marathon 2016. After a brief descriptive analysis, we assess differences on age and performance, across sex and race distance.

* [`exploratory_full_sport_dataset:`](https://nbviewer.jupyter.org/github/ggrrll/hop_suisse_ada_project_public/blob/master/6-data_analysis/exploratory_full_sport_dataset.ipynb)
exploratory statistics on the full dataset. We first study how participation to sport events evolves in time. 
After, we study how age and weather conditions might influence runner's performance.

* [`complementary_lausanne:`](https://nbviewer.jupyter.org/github/ggrrll/hop_suisse_ada_project_public/blob/master/6-data_analysis/complementary_lausanne.ipynb) A short notebook where non-parametric tests for age/sex distribution of the Lausanne Marathon 2016 are implemented.

* [`geoanalysis:`](https://nbviewer.jupyter.org/github/ggrrll/hop_suisse_ada_project_public/blob/master/6-data_analysis/geoanalysis.ipynb) In this notebook we explore the possible links between statistical and geographical patterns in the time distribution for marathon runners. Requires the .pickle dataset to be run, as well as [swisscities.xlsx](../datasets/swisscities.xlsx) and canton_population.xlsx.

* [`network_of_runners:`](https://nbviewer.jupyter.org/github/ggrrll/hop_suisse_ada_project_public/blob/master/6-data_analysis/network_of_runners.ipynb) in this notebook we tried a complex network approach on runners.
We define a network of runners (nodes), linked according to the number of races they run together (edge weight).
