# postdoc_technical_task
Technical work done for the postdoctoral research position in Advanced Machine Learning and Computational techniques for Industry 4.0



## Notebook explanation

* *0_PreliminarAnalysesOfDataset.ipynb* => Notebook in which the preliminary analyses of the Bosch datasets are performed 
    * Output: Images present in .../images/
    
* *1_Feature_selection_categorical-less_muestras.ipynb* => Transformation and reduction of the space of categorical features (from 2140 to 75 features)
    * Output: encoder_categorical_model_FULL_FINAL_TRUE.pkl (list of the 75 most important categorical features) 

* *2_TotalFeature selection_sample.ipynb* => Transformation and reduction of the space of categorical features (from a total of 2200 (75+968+1157) to 125)
    * Output: Output: .../data/final_selected_features.pkl (list of the 150 most important features) 

* *3_Train_tune_final_model.ipynb* => Tune hyperparameters of a XGBoost classifier with a stratified 3-fold.
    * Output: .../data/final_prediction_model.sav (prediction model) and .../data/encoder_for_testing.sav (Leave One Out Encoder)

* *4_TestData.ipynb* => Load the testing dataset, make the transformation needed, the predictions, and save the results in the submission.csv file.
    * Output: .../data/submission.csv

## Conda environment
Use the terminal or an Anaconda Prompt for installing the conda environment used in this works:

1. Create the environment from the *environment.yml* file:

    ```
    conda env create -f environment.yml
    ```

    The first line of the yml file sets the new environment's name. For details see Creating an environment file manually.

2. Activate the new environment: ```conda activate myenv```

3. Verify that the new environment was installed correctly:
    ```
    conda env list
    ```
    You can also use ```conda info --envs```
    
## Data
You need to download the dataset from the [Kaggle competition](https://www.kaggle.com/c/bosch-production-line-performance/data). Then, you can move the .csv files to the data folder.

## Report

The report can be consulted in the file *LuisGasco_Assignment.pdf*
                                    





