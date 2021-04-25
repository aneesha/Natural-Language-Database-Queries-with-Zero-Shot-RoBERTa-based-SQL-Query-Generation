# Natural-Language-Database-Queries-with-Zero-Shot-RoBERTa-based-SQL-Query-Generation

Based on the Google Colab Notebook (https://colab.research.google.com/drive/1qYJTbbEXYFVdY6xae9Zmt96hkeW8ZFrn) provided for the paper "[Data Agnostic RoBERTa-based Natural Language to SQL Query Generation](https://arxiv.org/abs/2010.05243)". Only a list of fields and their types are needed for the model to convert Natural Language to an SQL query.

This notebook shows how to implement the model to make a Natural Language to SQL converter for any uploaded tabular dataset.

Key Funtionality

* Allows csv file upload
* Loads the csv into an in-memory SQLite database
* Determines the type schema automatially
* Loads the pre-trained models
* Converts Natural Language to SQL
* Executes the SQL against the in-memory SQLite database
* Display the results in a filterable table

Note:
You will need to download the model files from [here](https://drive.google.com/drive/folders/13f2MrdpieC9QGXM_DJnj2f1Hs6ZBh2ZT?usp=sharing.) and upload to your own Google Drive. You will need to update the path to the location within your Google Drive. The 2 required files are model_roberta_best.pt and model_best.pt.

The orignal github repo is https://github.com/DebadityaPal/RoBERTa-NL2SQL
https://github.com/aneesha/RoBERTa-NL2SQL is a fork with code changes to return SQL (rather than printing it out) and add quotes around string/text fields. Some postprocessing is also added to display all fields in the dataset and support SQL with distinct.
