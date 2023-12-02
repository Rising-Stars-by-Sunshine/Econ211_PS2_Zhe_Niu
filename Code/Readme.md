# Data Query and Analysis Process
This Readme outlines the process employed in data_query.ipynb and data_analysis.ipynb files for querying and analyzing a credit card fraud dataset. The process involves setting up a Kaggle API for data download, preprocessing the data, including scaling and handling missing values, and applying balancing techniques like SMOTE and RandomUnderSampler. Key steps include scaling the 'Amount' feature, removing certain columns, and examining the data for insights through visualizations like KDE plots, box plots, and correlation matrices. The goal is to prepare the dataset adequately for effective fraud detection analysis.

# Pseudo-Code for Data Query Process
The following pseudo-code in LaTeX format encapsulates the general steps in the data query and preprocessing process, applicable across major programming languages such as Python:

\begin{table}[H]
\centering
\begin{tabular}{|l|}
\hline
\textbf{Pseudo-Code: Data Query and Preprocessing} \ \hline
Set API credentials and configure Kaggle API environment. \
Download dataset from Kaggle competition. \
Unzip the downloaded dataset. \
Read training and testing datasets into dataframes. \
Define a preprocessing function: \
\ \ \ \ - Scale 'Amount' feature using RobustScaler. \
\ \ \ \ - Drop 'Time', 'id', and 'Amount' columns. \
Apply preprocessing to training and testing datasets. \
Check for missing values in the dataset. \
Generate visualizations (KDE plots, box plots, heatmaps) for analysis. \
Apply SMOTE for oversampling and balance the dataset. \
Apply RandomUnderSampler for undersampling and balance the dataset. \
Visualize the balanced dataset and its correlation matrix. \ \hline
\end{tabular}
\caption{Pseudo-code for data query and preprocessing steps}
\end{table}
