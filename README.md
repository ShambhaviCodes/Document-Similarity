# Document Similarity
This repository contains final submission of assignment on document similarity.

## An Overview of the Dataset
 1. 162 Queries and 1 Base Document
 2. Queries given in (.CSV) format and Base Document in (.pdf)
 3. Base Document has multiple tables and mathematical formulae.
 4. Queries did not have tabular entries but a few had linear formulas with special symbols like gamma, alpha etc.


## Formulation of Approach 
   Representing features in the form of vectors for both; queries and base document.
   Calculating the distance between features for each query with the base document.


## Modelling
There are two type of similarities possible in case of matching the texts,
 1. Lexical Similarity : This measures the closeness of occurrence of words. 
           Jaccard Similarity calculates the similarity (Jaccard index) as size of intersection divided 
           by size of the union of two sets.
 2. Semantic Similarity : This measures the texts similarity based on the ‘meanings’ of the sentences. Word embedding is used to create the feature vector and    
    then cosine similarity is used to calculate the matching score. While the match percentage might be different from the ground truth due to methodology or size 
    of dataset, the comparative ratio of most similar and dissimilar queries should be the same.

For example for P161 query, both the above methods give a high matching score.
 

## Contents & Instructions 
 1. Semantic_Similarity.ipynb - Ipython Notebook trained on Google Colab,
    To reproduce the results, select ‘Runtime’ and ‘Run all’ the cells. You will need the ‘cc.en.300.bin’ file. Please download it using a bash terminal (run
    ./download_model.py en),upload on Google Drive and set the paths to the file accordingly. 
 2. Semantic_Similarity.csv - (.CSV) file with results in a separate column.
 3. Lexical_Similarity.ipynb - Python Notebook trained on Jupyter Notebook 
            Open using Jupyter Notebook and ‘Kernel - Restart and Run All’
 4. Lexical_Similarity.csv - (.CSV) file with results in a separate column.
