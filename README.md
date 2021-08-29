# AAAI HCOMP 2021 - Conjoint Analysis of Human Preferences
This repository contains code to support the analysis of the paper: "[Modeling Simultaneous Preferences for Age, Gender, Race, and Professional Profiles in Government-Expense Spending: a Conjoint Analysis]()" published in the 2021 Proceedings of [AAAI Conference on Human Computation and Crowdsourcing](https://www.humancomputation.com/).

This repository and associated work may be cited as follows:
```
@inproceedings{ibrahim2021modeling,
  title={Modeling Simultaneous Preferences for Age, Gender, Race, and Professional 
    Profiles in Government-Expense Spending: a Conjoint Analysis},
  author={Ibrahim, Lujain and Ghassemi, Mohammad M. and Alhanai, Tuka},
  booktitle={Proceedings of the AAAI Conference on Human Computation and Crowdsourcing},
  year={2021}
}

```

## Directory Structure
* `datasets`: contains three csv files:
  * `suggestedadvisor-expense-pairs.csv`: the file that is sampled to show advisor profiles and expenses during the experiment
  * `results.csv`: the file with all the data collected from the experiments
  * `users.csv`: the file with information on each of the experiment respondents
* `ip-map-datasets`: contains files used to create heatmap of geographical locations of respondents
* `requirements.txt`: required python libraries for analysis
* `demographic-analysis.ipynb`: jupyter notebook to perform demographic analysis of respondents
* `global-conjoint-analysis.ipynb`: jupyter notebook to perform conjoint analysis on responses from all respondents
* `global-plots.ipynb`: jupyter notebook to generate sankey plots and bubble plots on respondents' choices for age, gender, race, and profession
* `political-party-conjoint-analysis.ipynb`: jupyter notebook to perform conjoint analysis on responses from (a) democrats and (b) republicans
* `political-party-plots.ipynb`: jupyter notebook to generate sankey plots and bubble plots on (a) democratic respondents' and (b) repiublican respondents' choices for gender and race

## Running Analysis
### System Requirements

* To install Python 3, follow these [instructions](https://realpython.com/installing-python/). 
* To install Pip, follow these [instructions](https://pip.pypa.io/en/stable/installing/).
* To install Jupyter Lab/Notebook, follow these [instructions](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html). To run Jupyter Lab/Notebook, follow these [instructions](https://jupyter.readthedocs.io/en/latest/running.html). 
* To set up a virtual environment and use it in Jupyter Lab/Notebook, follow these [instructions](https://janakiev.com/blog/jupyter-virtual-envs/).


### To install requirements:

1. Clone this github repository 
```
git clone <url-to-this-repo>
cd <cloned-repo>
cd public-repo
```
2. Get Python requirements needed
```
pip3 install -r requirements.txt
```
### Understanding Datasets
There are two datasets used in the analysis: 
1. `datasets/results.csv`:
    * `session_id`: unique id of the each respondent's session
    * `response_id`: unique id of each task response in a respondent's session
    * `expense_category`: category of the expense presented in task
    * `expense`: specific expense presented in task
    * `age_suggested`: age of suggested advisor
    * `age_selected`: age of customized advisor
    * `age_changed`: 0 if age_selected=age_suggested, 1 otherwise
    * `gender_suggested`: gender of suggested advisor
    * `gender_selected`: gender of customized advisor
    * `gender_changed`: 0 if gender_selected=gender_suggested, 1 otherwise 
    * `race_suggested`: race of suggested advisor
    * `race_selected`: race of customized advisor
    * `race_changed`: 0 if race_selected=race_suggested, 1 otherwise
    * `profession_suggested`: profession of suggested advisor
    * `profession_selected`: profession of customized advisor
    * `profession_changed`: 0 if profession_selected=profession_suggested, 1 otherwise
    * `profession_option1`: 1st profession option in the customized advisor profession drop down menu 
    * `profession_option2`: 2nd profession option in the customized advisor profession drop down menu 
    * `profession_option3`: 3rd profession option in the customized advisor profession drop down menu 
    * `profession_option4`: 4th profession option in the customized advisor profession drop down menu 
    * `task_submit_time`: task submission time
3. `datasets/users.csv`:
    * `session_id`: unique id of the each respondent's session
    * `user_state`: state the respondent completed the experiment from 
    * `user_gender`: self-reported gender of respondent (survey response)
    * `user_age`: self-reported age of respondent (survey response)
    * `user_degree`: self-reported educational level of respondent (survey response)
    * `user_politics`: self-reported political party affiliation of respondent (survey response)
    * `user_vote`: self-reported voting behavior (yes/no/not sure) in 2020 national elections of respondent (survey response)
    * `user_religion`: self-reported religion of respondent (survey response)
    * `user_ethnicity`: self-reported ethnicity of respondent (survey response)
    * `user_income`: self-reported annual income of respondent (survey response)
    * `session_submit_time`: session submission time (survey response)

### Running Jupyter Notebooks
All the analysis notebooks used to generate the figures and results used in the publication can be found in this folder:
* [Datasets](datasets)
* [Subjects Demographic Analysis](demographic-analysis.ipynb)
* [Global Conjoint Analysis](global-conjoint-analysis.ipynb)
* [Political Party Conjoint Analysis](political-party-conjoint-analysis.ipynb)
* [Global Sankey & Bubble Plots](global-plots.ipynb)
* [Political Party Sankey & Bubble Plots](political-party-plots.ipynb)

