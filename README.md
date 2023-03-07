# CS 539 Final Project Overview

## Classification, Prediction and Analysis of Tungsten-based Alloy Densities from Trace Element Properties, Powder Characteristics, and Processing Parameters Data Using EDA, Random Forest, SVM and Decision Tree Models

### Project: Motivation, Description and Overview: 

The refractory metals industry, and many like it, are plagued with high cost and time-intensive testing. Some industries, such as the aluminum or iron metals industry, are less burdened by these restraints. The refractory metal I'll be observing cost nearly 150x more than aluminum per kilo and takes nearly 16x longer to process overall, from powder/raw to final machined product. This puts a heavy constraint on reseach and development overall. This also means that any scrap produced due to lack of quality checks or failed experiments take a much larger toll on the companies. Overall this leads to less data points, higher costs, and longer times between testing, while also keeping the high dimensionality of the complex processing environment.

The aim of this project was to predict the density of a tungsten-based alloy using regression and classification models, while also characterizing trends and gaining insights into the influence of the chosen features. The challenge to predict ingot density, with a 70% accuracy based on chemical properties, powder characteristics and basic processing parameters was seemingly successful using KNN, SVM, Random Forest and Decision Tree models. Among the successful models other insights derived included the influence of the time of year, trace elements outside primary elements and dataset complications. As a result, the project concluded with insightful and shocking results.

The dataset used is a collection of datasets from multiple departments that were merged together, they did not share a similar key format, so most of the merging was done manually. The dataset consisted of multiple float values and some string columns. The dataset is 6105 records and 28 features for one material called WK. The data was collected for the dates of June 2021, to June 2022. Features chosen are listed below.

- LotNumber: The lot number associated per bar
- PanelNumber: Furnace panel used
- BottleNumber: Bottle in furnace line used
- DateStamp: Date of density check
- BarDensity: Discrete bar densities for regression
- BarDensityA: Binned bar densities for classification
- FSSS: Average spherical diameter of powder (um)
- BulkDensity: Loose packing density of powder (g/in^3)
- TapDensity: Tapped packing density of powder (g/cm^3)
- *Trace Elements (ppm)* -> {Al, C, Ca, Co, Cr, Cu, Fe, K, La, Mo, Ni, P, Si, Ti, Zn, Zr}


### Project: Full Analysis (sample)

The project started off with some exploratory data analysis (EDA). The methods used during the EDA of the project included:

- Basic Statistics
- Histogram Plots
- Boxplots
- Scatterplots
- Correlation plots/Matrix
- PCA
- Stripplots
- Distribution plots

Below are some examples of the visuals generated from the analysis. The first is the correlation plot, which compares all features with each other and displays their correlation scores. This plot provides a comprehensive view of the data and can help guide further exploration. While most features do not correlate, a few show some correlation, making this a good starting point for analysis.

<!-- ![Correlation Plot](https://raw.githubusercontent.com/GitMooreHub/Moore_CS539_Final_Project/main/images/Correlation-Plot.png) -->
<img src="https://raw.githubusercontent.com/GitMooreHub/Moore_CS539_Final_Project/main/images/Correlation-Plot.png" alt="Correlation Plot" width="75%" height ="75%">

PCA was done in order to derive important features. Most PCA plots tested looked like the one below which was clustered and scattered randomly between PCs. The first two components only explained ~22% of the variance in the data. This means that the data on a whole is either unrepresentative of the target or is random.

<!-- ![PCA Plot 1](https://raw.githubusercontent.com/GitMooreHub/Moore_CS539_Final_Project/main/images/PCA1.png) -->
<img src="https://raw.githubusercontent.com/GitMooreHub/Moore_CS539_Final_Project/main/images/PCA1.png" alt="PCA Plot 1" width="75%" height ="75%">

Lastly, optimization was done through pipelines and gridsearches in order to find the best parameter pairs. Below is an example of the optimal K found for a KNN model. The optimization produced much better classification and prediction accuracy from the model. 

![KNN 'K' Evaluation](https://raw.githubusercontent.com/GitMooreHub/Moore_CS539_Final_Project/main/images/KNN-K-Eval.png)

Overall, models produced just above 80% accuracy, with SVM being highest out of all the models at ~83% accuracy in predictions which is hopeful for physical testing.

See Full Analysis Document for more information.

[VIEW WEBSITE](https://gitmoorehub.github.io/Moore_CS539_Final_Project/)

[VIEW FULL ANALYSIS DOCUMENT](https://github.com/GitMooreHub/Moore_CS539_Final_Project/blob/main/process_notebook.ipynb)
