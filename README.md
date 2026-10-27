\# Adult Census Income Analysis



\## Project Overview



This project explores the Adult Census Income dataset to analyze demographic and socioeconomic factors associated with income levels and develop machine learning models for income classification.



The project covers data cleaning, exploratory data preparation, feature encoding, clustering, and supervised machine learning. It demonstrates a data analysis workflow from raw data preparation to model evaluation.



\## Project Objectives



\* Clean and prepare the Adult Census dataset for analysis.

\* Explore the distribution of income classes.

\* Transform categorical features into a machine-learning-ready format.

\* Apply K-means clustering to explore patterns within the dataset.

\* Build and evaluate a machine learning model to predict income categories.

\* Assess model performance using relevant classification metrics.



\## Tools and Technologies



\* \*\*Python\*\* — data processing and machine learning.

\* \*\*Jupyter Notebook\*\* — interactive analysis and experimentation.

\* \*\*SQLite\*\* — working with structured data.

\* \*\*Pandas and NumPy\*\* — data manipulation and numerical operations.

\* \*\*Scikit-learn\*\* — preprocessing, clustering, model training, and evaluation.



\*Note: The libraries listed above should be confirmed against the actual notebook before publication.\*



\## Dataset



The Adult Census dataset contains demographic and socioeconomic attributes used to classify individuals into two income categories: `<=50K` and `>50K`.



The original dataset contained \*\*32,561 records and 15 columns\*\*.



\### Income Distribution



| Income category | Number of records | Percentage |

| --------------- | ----------------: | ---------: |

| <=50K           |            24,720 |     75.92% |

| >50K            |             7,841 |     24.08% |

| \*\*Total\*\*       |        \*\*32,561\*\* |   \*\*100%\*\* |



The distribution shows that the `<=50K` category represents the majority of records, making class imbalance an important consideration during model evaluation.



\## Methodology



\### 1. Data Cleaning



The dataset was inspected and duplicate records were removed.



\* Initial dataset: 32,561 rows and 15 columns.

\* Dataset after duplicate removal: 32,537 rows and 15 columns.



This step helped reduce duplication before further analysis.



\### 2. Data Preprocessing



The data was prepared for machine learning, including encoding categorical variables into numerical representations.



\* Encoded dataset: 32,537 rows and 109 columns.

\* Training set: 26,029 records.

\* Testing set: 6,508 records.



\### 3. K-Means Clustering



K-means clustering was used to investigate potential groupings in the dataset.



The best silhouette score recorded was \*\*0.050 at k = 3\*\*.



This low silhouette score suggests that the resulting clusters were not clearly separated. Therefore, the clustering results should be interpreted cautiously rather than treated as strong evidence of distinct natural groups.



\### 4. Supervised Machine Learning



A HistGradientBoosting classifier was evaluated for income prediction. The classification threshold was tuned to improve the balance between precision and recall for the target class.



The selected threshold was \*\*0.332\*\*.



\### 5. Model Evaluation



The tuned model achieved the following recorded results:



| Metric                            | Result |

| --------------------------------- | -----: |

| ROC AUC                           | 0.9209 |

| F1-score                          | 0.7234 |

| Selected classification threshold |  0.332 |



The ROC AUC of 0.9209 indicates strong discrimination between the two income categories on the evaluated data, while the F1-score summarizes the balance between precision and recall at the selected threshold.



These results should be interpreted alongside the model's confusion matrix, precision, recall, and validation procedure. The threshold should be selected using validation data rather than the final test set to avoid optimistic performance estimates.



\## Key Findings



\* The `<=50K` income category accounted for approximately 75.92% of the original dataset.

\* Duplicate removal reduced the dataset from 32,561 to 32,537 records.

\* Categorical encoding expanded the feature set from 15 to 109 columns.

\* K-means clustering achieved a silhouette score of 0.050 at three clusters, suggesting weak cluster separation.

\* The tuned HistGradientBoosting model recorded an ROC AUC of 0.9209 and an F1-score of 0.7234.



\## Limitations



\* The dataset has an imbalanced income distribution.

\* Clustering performance was limited, as indicated by the low silhouette score.

\* Predictive performance depends on the preprocessing pipeline, data split, feature selection, and evaluation methodology.

\* Income prediction from demographic data requires careful consideration of privacy, fairness, and potential socioeconomic bias.



The model identifies statistical patterns in the dataset; it does not establish causation or determine an individual's actual earning potential.



\## Conclusion



This project provided practical experience in data cleaning, feature preprocessing, unsupervised learning, supervised classification, and model evaluation.



The results demonstrate the value of a structured data science workflow while highlighting the importance of critical evaluation, especially when working with imbalanced datasets and demographic information.



\## Project Structure



The repository contains the Jupyter Notebook used for analysis and any supporting scripts included in the project.



```text

adult-census-analysis/

├── README.md

├── adult\_census\_analysis.ipynb

└── scripts/                 # If applicable

```



Update the notebook and folder names above to match the actual files in your repository.



\## Reproducibility



To reproduce the analysis:



1\. Clone or download this repository.

2\. Install the Python libraries required by the notebook.

3\. Open the Jupyter Notebook.

4\. Ensure the dataset is available at the path expected by the notebook.

5\. Run the notebook cells in order.



The exact dependency versions and dataset setup should be documented after verifying the notebook.



\## Acknowledgements



This project was completed as a capstone project. Dataset attribution and team contributions should be added here where applicable.



