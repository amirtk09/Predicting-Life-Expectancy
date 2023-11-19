# Predicting-Life-Expectancy
_Predicting Life Expectancy using Pycaret and IBM SPSS Modeler_


| Title                 | Description                                      |
|-----------------------|------------------------------------------------  |                                                                   
| Description 📝        | Project Overview                                |
| Dataset 🗒️            | Explanations about the Data                     |
| Installation 🖥️       | Software and Libraries Required for the Project |
| Data Preprocessing 🔍 | Details of Data Preprocessing                   |
| Model Building 🎯     | Explanations Regarding Modeling                 |
| Conclusion 📖          | Final conclusion                                |

<hr>

## 📝 Description
Developed a predictive machine learning model to predict life expectancy for each country in 2022, using data from the United Nations' World Population Report. Preprocessing of the data was done using IBM SPSS Modeler, followed by regression prediction using the PyCaret machine learning library.

<hr>

## 🗒️Dataset
- For our project, we will be utilizing data from the United Nations World Population Prospects. This report provides invaluable insights into global demographic trends, including population growth rates, age distribution, and population density.
- https://github.com/amirtk09/Predicting-Life-Expectancy/blob/main/data/WPP2022.xlsx

<hr>

## 🖥️ Installation
- ### IBM SPSS Modeler <br/>
  You can download IBM SPSS Modeler from the IBM website. Once downloaded, follow the installation instructions to install the software on your system.
  
- ### Pycaret  <br/>
  In order to avoid potential conflicts with other packages, it is strongly recommended to use a virtual environment, e.g. python3 virtualenv or conda environments. Using an isolated environment makes it possible to install a specific version of pycaret and its dependencies independently of any previously installed Python packages. <br/>
  
  ````
  # create a conda environment
  conda create --name yourenvname python=3.8

  # activate conda environment
  conda activate yourenvname

  # install pycaret
  pip install pycaret

  # create notebook kernel
  python -m ipykernel install --user --name yourenvname --display-name "display-name"
  ````
  
<hr>
  
## 🔍 Data Preprocessing
The data for this project was obtained from Kaggle. The data was in xlsx format and was imported into IBM SPSS Modeler for preprocessing.

The following steps were performed in IBM SPSS Modeler to preprocess the data:
- Two approaches were used to manage outlier data:
  1. Features with a normal distribution were handled using standard deviation.
  2. Features with a non-normal distribution were managed using interquartile range (IQR).
- Missing values were handled using a combination of the mean method and a C&RT machine learning model.
- Feature selection was performed.
- Data normalization was carried out using Min-max transformation.

<hr>

## 🎯 Model Building
In the modeling section, regression machine learning models were compared. The bagged Extra Trees model was then finalized by training it on the entire dataset, and the life expectancy for all countries was predicted for the year 2022.
The obtained R2 value of 0.9526 suggests that the model can explain 95.26% of the variance in the dependent variable based on the independent variables, indicating good performance on the new dataset. However, it is important to note that the model's performance on the new dataset should be evaluated using multiple evaluation metrics, not just R2, to ensure accurate predictions.

<hr>

### 📖 Conclusion
This project demonstrates how to use Pycaret and IBM SPSS Modeler to preprocess and model data for life expectancy prediction. The project can be further improved by trying out different models, tuning hyperparameters, and adding new features to the dataset.
