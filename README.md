# RLF
R code implementation of RLF. The general backbone follows the R implementation of Randomforest (Leo Breiman [aut] (Fortran original), Adele Cutler [aut] (Fortran original), Andy Liaw [aut, cre] (R port), Matthew Wiener [aut] (R port))

Paper link: https://openreview.net/pdf?id=Gx8ujJTnG9
## How to use RLF:

### (1)Open RiemannLebesgueForest project with R studio
### (2)Click "build" to install RLF locally
### (3)Open a new R console/ markdown file
### (4)library(RiemannLebesgueForest)
### (5)Check the file "Experiments_datadrivenP.rmd" or other rmd files in the file named "R" to see examples in  setting parameters in RLF.
### (6)Play around with datasets in the file named "R".
### Mainly used parameters: 
### ntree: Number of RiemannLebesgue Tree used. Default value:100
### ntreesub: Number of subtrees used in local randomforest. Default value: 10.  ntreesub=1 in running time experiments,i.e local decision tree
### replace: For subagging step, whether we sample with replacement or not. Default value:FALSE
### data_driven: How control probability tilde_p is determined. Default value: FALSE, i.e we set the value of tilde_p be fixed value.
### L_p: Control probability tilde_p. Default value: 0.8. This parameter is only useful when we set data_driven=FALSE.


Explanations for some csv and rmd files in file named "R":

(1)
CSV files with name such as "rlf_datasetname" include experiment results of RLF with datadriven control probability tilde_p and the results of RF

CSV files with name such as "rlf_datasetnametune" include experiment results of RLF with tuned parameters ( i.e datadriven=FALSE and control probability tilde_p=tuned value) and the results of tuned RF

CSV files with name such as "rlf_datasetname_time" include experiment running time of RLF and RF (All parameters are set as default values )

(2)
"Experiments_datadrivenP.rmd" includes code performing experiments of RLF with datadriven control probability tilde_p and ordinary RF

"Experiments_runningtime.rmd" includes code calculating running time for RLF and RF

"Experiments_TunedP.rmd" includes code performing experiments of RLF and ordinary RF with parameter tuning process.

"Experiments_missing value.rmd" includes code performing extra experiments of RLF on real datasets with missing values.

"Experiments_feature_selection.rmd" includes code performing experiments of RLF and ordinary RF with feature selection strategies on real datasets.

"Simulation_feature_selection.rmd" includes code performing experiments of RLF and ordinary RF with feature selection strategies on simulated datasets.

"Simulation_scality.rmd" includes code performing running time scality experiments of RLF and ordinary RF on simulated datasets.

"test_extra.rmd" includes code  comparing performance of RLF, RF, Gradient Boost and Xgboost on real datasets.
