Python and R package download comparison
---

### Data source
#### R package download data
- CRAN package download logs
  - http://cran-logs.rstudio.com/
  - e.g., https://www.r-bloggers.com/finally-tracking-cran-packages-downloads/
- Download stats API in R: 
  - https://cranlogs.r-pkg.org/
  - JSON API: https://github.com/r-hub/cranlogs.app
  - e.g., https://cranlogs.r-pkg.org/downloads/total/2014-01-01:2014-12-31/ggplot2
  - access through R package `canlogs`: https://github.com/r-hub/cranlogs
- Python package `cranlogs`
  - `pip install cranlogs`
  - https://cranlogs.readthedocs.io/en/latest/cran_downloads.html
#### Python package download data
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
| |pandas | loc, sort_values, aggregate, groupby, merge | dplyr, data.table|filter, arrange, select, mutate, summarise, groupby, join |
| |pandas | pivot, melt, stack, unstack, groupby| tidyr|gather, spead |
| |pandas | .| magrittr|%>% |
| |pandas, matplotlib | | tidyverse|a set of packages that include ggplot2, dplyr, tidyr, readr, purrr, tibble, stringr, and forcats|
|| datetime| | lubridate, hms| |
|**Models** || |||
|Linear models|sklearn.linear_model, statsmodels| |stats | lm()|
|Generalised linear models  |statsmodels| GLM|stats |glm() |
|Generalised additive models |pyGAM, stasmodels.gam||mgcv |gam() |
|Penalised linear models |sklearn.linear_model|Lasso, ElasticNet |glmnet |glmnet() |
|Penalised linear models |glmnet| |glmnet |glmnet() |
|Robust linear models |statsmodels|RLM |MASS |rlm() |
|Linear Mixed-Effects Models |stasmodels|mixedlm|lme4, lmerTest | |
|Structural eqation modeling |semopy||lavaan | |
|k-means |sklearn.cluster|KMeans |stats|kmeans |
|PCA |sklearn.decomposition|PCA |stats|prcomp |
|t-SNE|sklearn.manifold|TSNE|Rtsne|Rtsne|
|KNN|sklearn.neighbors|KNeighborsClassifier|class,FNN|KNN|
|Decision Trees |sklearn|tree |rpart |rpart() |
|Random forest |sklearn.ensemble|RandomForestClassifier |randomForest |randomForest() |
|Gradient boosting |xgboost| |xgboost| |
|other|scipy, numpy, sklearn| |e1071|collection of models (Functions for latent class analysis, short time Fourier transform, fuzzy clustering, support vector machines, shortest path computation, bagged clustering, naive Bayes classifier,...)|
|other|sklearn| |caret|caret is a set of functions that attempt to streamline the process for creating predictive models|
|network analysis|networkx| |igraph| |
|**Deep learning**|keras, tensorflow| |keras, tensorflow| |
|**Visualization** |matplotlib, bokeh| | ggplot2, graphics| |
|**Dashboard**  |panel, voila| | shiny| |

### Data
I retrieved package download data from Conda, PyPI, and Cran from Janurary 2018 to July 2019. Then I combined Conda and PyPI downloads to represent total downloads of Python packages. 

### Results 
Pandas was downloaded a lot more than dplyr, tidyverse and data.table. And the growth of pandas is substantial over time. 

![](https://github.com/sophiamyang/PythonRcomparison/blob/master/figures/pandas.png)

scikit-learn is downloaded a lot more than statsmodels in Python, caret in R, and e1071 in R.  

![](https://github.com/sophiamyang/PythonRcomparison/blob/master/figures/sklearn.png)

Most people use Keras and Tensorflow in Python, few use them in R. 

![](https://github.com/sophiamyang/PythonRcomparison/blob/master/figures/keras.png)

People use matplotlib a lot. ggplot2 is as popular as Bokeh. 

![](https://github.com/sophiamyang/PythonRcomparison/blob/master/figures/plot.png)

For creating dashboard, most people use Shiny. Few use Panel and Voila. 

![](https://github.com/sophiamyang/PythonRcomparison/blob/master/figures/dashboard.png)

### Conclusion
Except for creating dashboard, people seem to download a lot more Python packages than R packages for data manipulation, visualization, machine learning, and deep learning. 

### Note! 
Python package download numbers can be inflated for the following reasons:
- CI systems: A lot of the downloads could be coming from CI systems. And R might have a lot less downloads from CI systems. 
- Environments: Python users might be more likely to manage multiple environment and install packages in various environment. However, R users might just use one environment. 
- Packaging updates: R users might not update packages as often as Python users. 

### References
https://r4ds.had.co.nz/ <br />
https://lgatto.github.io/IntroMachineLearningWithR/<br />
https://topepo.github.io/caret/index.html <br />
https://daviddalpiaz.github.io/r4sl/ <br />
https://www.tidyverse.org/ <br />

