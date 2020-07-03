# Street Fighting Data Science 


## Competition Post Mortems

TODO

## Tips & Tricks

### [Interview with a Kaggle Grandmaster - Giba](https://datasciblog.github.io/2015/11/09/profiling-top-kagglers-gilberto-titericz-new-1-in-the-world/)

As of May-2015.

Iteration cycle:
1. First of all it is very important understand the problem, the features, and the evaluation metric. 
1. After that I look for a good cross validation strategy. Those are the very basic and essential steps. 
1. Only after that you can start thinking about feature engineering and training algorithms that match the problem.
1. Then I choose a training algorithm and optimize hyperparameters based on a cross validation score. 
1. If a model is good and stable I save the train set and test set predictions. 
1. Then I start all over again using another training algorithm or model. 
1. When I have a handful of good model predictions, I start ensembling at the second level of training.

Favorite machine learning algorithms: GBM, NNs.

Tools: XGBoost, Vowpal Wabbit, LibFM, scikit-learn.

CV: compromise between local CV score vs leaderboard results: 

```python
((LocalCVscore*number_rows_trainset) + (LBscore*number_of_rows_used_to_calculate_LB)) / (sum_of_number_of_rows_in_CV_and_LB )
```

Secret sauce: models and features, CV, teaming up, ensembles, hard work and luck :)


### [Interview with a Kaggle Grandmaster - bestfitting](https://medium.com/kaggle-blog/profiling-top-kagglers-bestfitting-currently-1-in-the-world-58cc0e187b)

As of May-2018.

Iteration cycle:
1. Create a solution document, follow and update as the competition continues on.
1. Read the overview and data description of the competition carefully
1. Find similar Kaggle competitions. As a relatively new comer, I have collected and done a basic analysis of all Kaggle competitions.
1. Read solutions of similar competitions.
1. Read papers to make sure I don’t miss any progress in the field.
1. Analyze the data and build a stable CV.
1. Data pre-processing, feature engineering, model training.
1. Result analysis such as prediction distribution, error analysis, hard examples.
1. Elaborate models or design a new model based on the analysis.
1. Based on data analysis and result analysis, design models to add diversities or solve hard samples.
1. Return to a former step if necessary.

Favorite machine learning algorithms: ridge regression when ensemble, resnet-50 for DL.

Tools: PyTorch, seaborn, XGBoost.

CV: check and make sure the validation set has similar distribution to the training set and test set.

Secret sauce: CV, learning from other competitions, papers, hard work, "solution doc".

On solution doc: "I force myself to make a list that includes the challenges we faced, 
the solutions and papers I should read, possible risks, possible CV 
strategies, possible data augmentations, and the way to add model diversities. 
And I keep updating the document."



### [Interview with a Kaggle Grandmaster - KazAnova](https://medium.com/kaggle-blog/profiling-top-kagglers-kazanova-currently-2-in-the-world-f3fa9f936810)

TODO

### [Andrew Ng - Career Advice & Reading Research Papers](https://youtu.be/733m6qBH-jI)

Tips on reading papers:
- compile a list of papers & other resources, read them simultaneously, mark progress 
- reading one paper:
	- multiple passes
		1. title / abstract / figures
		1. intro / conclusions / figures / skim rest / skip related work
		1. read full, skip math
	- what did authors try to accomplish?
	- what are the key elements?
	- what can you use?
	- references
- sources of papers
	- twitter
	- NIPS / ICML / ICLR
- dealing with math
	- rederive from scratch
- dealing with code
	- run source
	- reimplement from scratch
- read steady, learn steady
