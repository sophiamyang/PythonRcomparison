Python and R package download comparison
---

### R package download data
- CRAN package download logs
  - http://cran-logs.rstudio.com/
  - e.g., https://www.r-bloggers.com/finally-tracking-cran-packages-downloads/
- Download stats API: 
  - https://cranlogs.r-pkg.org/
  - JSON API: https://github.com/r-hub/cranlogs.app
  - e.g., https://cranlogs.r-pkg.org/downloads/total/2014-01-01:2014-12-31/ggplot2
  - access through `canlogs`: https://github.com/r-hub/cranlogs

### Python package download data
- Pypi data:
    - https://packaging.python.org/guides/analyzing-pypi-package-downloads/
    - https://github.com/ofek/pypinfo#installation
- Conda data:
    - https://github.com/ContinuumIO/anaconda-package-data

### Python & R package comparison

| Purpose  | Python package  | Python function  | R package  |R function|
| -------- | -------- | -------- | -------- | -------- |
| **Data import and export** | pandas |read_csv, to_csv   | readr| read.csv, write.csv|
| |pandas | read_excel  | readxl| .xls and .xlsx|
| |pandas |  read_json | jsonlite| json|
| |json |  json.loads | jsonlite| json|
| |xml | xml.etree.ElementTree.parse  | XML| xmlparse|
|**Data processing** |pandas | apply, map| purrr| map|
||pandas | apply, map| plyr| apply functions, e.g., aaply|
| |pandas | loc, sort_values, aggregate, groupby | dplyr|filter,arrange,select, mutate, summarise,groupby |
| |pandas | pivot, melt, stack, unstack, groupby| tidyr|gather, spead |
| |pandas | merge| dplyr|join |
| |pandas | .| magrittr|%>% |
| |pandas | | tidyverse|combined packages|
|| datetime| | lubridate, hms| |
|**Models** || |||
|Linear models|sklearn.linear_model, statsmodels| |stats | lm()|
|Generalised linear models  |statsmodels| GLM|stats |glm() |
|Generalised additive models |pyGAM, stasmodels.gam||mgcv |gam() |
|Penalised linear models |sklearn.linear_model|Lasso, ElasticNet |glmnet |glmnet() |
|Penalised linear models |glmnet| |glmnet |glmnet() |
|Robust linear models |statsmodels|RLM |MASS |rlm() |
|Linear Mixed-Effects Models |stasmodels|mixedlm|lme4, lmerTest | |
|k-means |sklearn.cluster|KMeans |stats|kmeans |
|PCA |sklearn.decomposition|PCA |stats|prcomp |
|t-SNE|sklearn.manifold|TSNE|Rtsne|Rtsne|
|KNN|sklearn.neighbors|KNeighborsClassifier|class,FNN|KNN|
|Decision Trees |sklearn|tree |rpart |rpart() |
|Random forest |sklearn.ensemble|RandomForestClassifier |randomForest |randomForest() |
|Gradient boosting |xgboost| |xgboost| |
|a collection of models (Functions for latent class analysis, short time Fourier transform, fuzzy clustering, support vector machines, shortest path computation, bagged clustering, naive Bayes classifier,...) |scipy, numpy, sklearn| |e1071||
|a set of functions that attempt to streamline the process for creating predictive models|sklearn| |caret| |
|network analysis|networkx| |igraph| |
|**Deep learning**|keras, tensorflow| |keras, tensorflow| |
|**Visualization** |matplotlib, bokeh| | ggplot2, graphics| |
|**Dashboard**  |panel, voila| | shiny| |


#### References
https://r4ds.had.co.nz/ <br />
https://lgatto.github.io/IntroMachineLearningWithR/<br />
https://topepo.github.io/caret/index.html <br />
https://daviddalpiaz.github.io/r4sl/ <br />
https://www.tidyverse.org/ <br />

