# Curb

This is a repository containing code for the paper:

> J. kim, B. Tabibian, A. Oh, B. Schölkopf, M. Gomez-Rodriguez. Leveraging the Crowd to Detect and Reduce the Spread of Fake News and Misinformation. In Proceedings of the 11th ACM International Conference on Web Search and Data Mining (WSDM), 2018.

## Pre-requisites

This code is developed under Python 3 and the following packages are required for executing the code: `numpy`, `scipy`, `matplotlib`, `pickle`, `seaborn`

## Code structure

The repository contains the code for the execution of the model (`Curb`) and several baseline methods. Also, it contains Jupyter notebook files for generating the figures in the paper and the user exposure data for the `Twitter` and `Weibo` datasets used in the paper.

 - `code` directory contains the code for executing the model and the baselines.
   - `generate_results.py` : Given the user exposure data in the `Twitter` and `Weibo` directories, it runs the models (`Curb` and the baseline methods) and saves the results in `pkl` files.
   - `curb.py` : API for `Curb` and the `Oracle` baseline.
   - `flagratio.py` : API for the `Flag Ratio` baseline.
   - `baseline.py` : API for the `Exposure` baseline.
- `notebook` contains `Jupyter` notebook files for generating the figures in the paper. These notebooks use the results generated by the scripts in the `code` directory.
- `twitter` and `weibo`
   - `exposure_data` contains user exposure data for each story, where exposures are generated from the user sharing raw files.
   - `results` contains pre-computed results for `Curb`, the `Oracle` baseline, the `Flag Ratio` baseline and the `Exposure` baseline.

## Raw data

We use data from `Twitter` and `Weibo`, which includes users' networks and sharing logs, stories, and labels for the stories (whether the story is fake or genuine). The data was released together with the following paper:

> S. Kwon, M. Cha, and K Jung. 2017. Rumor detection over varying time windows. PLOS ONE 12, 1 (2017), e0168344.

and it can be downloaded from the following link:

> https://sites.google.com/site/iswgao/



