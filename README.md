# CS 539 Final Project Overview

## Classification, Prediction and Analysis of Tungsten-based Alloy Densities from Trace Element Properties, Powder Characteristics, and Processing Parameters Data Using EDA, Random Forest, SVM and Decision Tree Models

### Project: Motivation, Description and Overview: 

The refractory metals industry, and many like it, are plagued with high cost and time-intensive testing. Some industries, such as the aluminum or iron metals industry, are less burdened by these restraints. The refractory metal I'll be observing cost nearly 150x more than aluminum per kilo and takes nearly 16x longer to process overall, from powder/raw to final machined product. This puts a heavy constraint on reseach and development overall. This also means that any scrap produced due to lack of quality checks or failed experiments take a much larger toll on the companies. Overall this leads to less data points, higher costs, and longer times between testing, while also keeping the high dimensionality of the complex processing environment.

This project was to predict density of a tungsten based alloy using both regression type and classification based models as well as characterize trends and gather insight on fluence of the chosen features. The challenge to predict ingot density, with a 70% accuracy based on chemical properties, powder characteristics and basic processing parameters was seemingly successful using KNN, SVM, Random Forest and Decision Tree models. Among the successful models other insights derived included the influence of the time of year, trace elements outside primary elements and dataset complications. Needless to say, the project concluded with insightful and shocking results.

The dataset used is a collection of datasets from multiple departments that were merged together, they did not share a similar key format, so most of the merging was done manually. The dataset consisted of multiple float values as well as some all string columns. The dataset is 6105 records, not including the header, and 28 featuresfor one material called WK. The data was collected for the dates of June 2021, to June 2022. Features chosen are listed below.

LotNumber: The lot number associated per bar

PanelNumber: Furnace panel used

BottleNumber: Bottle in furnace line used

DateStamp: Date of density check

BarDensity: Discrete bar densities for regression

BarDensityA: Binned bar densities for classification

FSSS: Average spherical diameter of powder (um)

BulkDensity: Loose packing density of powder (g/in^3)

TapDensity: Tapped packing density of powder (g/cm^3)

*Trace Elements (ppm)* -> {Al, C, Ca, Co, Cr, Cu, Fe, K, La, Mo, Ni, P, Si, Ti, Zn, Zr}


### Project: Full Analysis (sample)

The project started off with some exploratory data analysis (EDA). The methods used during the EDA of the project included:

Basic Statistics

Histogram Plots

Boxplots

Scatterplots

Correlation plots/Matrix

PCA

Stripplots

Distribution plots

Below is examples of some of the visuals taken from the analysis:

First is the correlation plot which cross matches all features with one another and shows their correlation score. This is a very good representation of the data in all as this shows where some exploration may start. Overall most features don't correlate but a couple do and this is a good basis to start on.

![](https://github.com/GitMooreHub/Moore_CS539_Final_Project/blob/main/images/Correlation-Plot.png)

PCA was done in order to derive important features. Most PCA plots tested looked like the one below which was clustered and scattered randomly between PCs. The first two components only explained ~22% of the variance in the data. This means that the data on a whole is either unrepresentative of the target or is random.

![](https://github.com/GitMooreHub/Moore_CS539_Final_Project/blob/main/images/PCA1.png)

Lastly, optimization was done through pipelines and gridsearches in order to find the best parameter pairs. Below is an example of the optimal K found for a KNN model. The optimization produced much better classification and prediction accuracy from the model. 

![](https://github.com/GitMooreHub/Moore_CS539_Final_Project/blob/main/images/KNN-K-Eval.png)

Overall, models produced just above 80% accuracy, with SVM being highest out of all the models at ~83% accuracy in predictions which is hopeful for physical testing.

See Full Analysis Document for more information.

[RETURN TO PORTFOLIOS PAGE](https://gitmoorehub.github.io/Portfolio_Profiles/posts/2022/12/data-science-portfolio/)
