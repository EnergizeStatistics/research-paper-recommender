# Content-Based Research Paper Recommender #
This repository hosts code for a rudimentary research paper recommender. 

## Description ##
The recommender aims at providing recommendations to researchers by using  their research interests, which are represented by their publications.

The code is for experimentation and demonstration purposes only; the recommender system is currently far from polished. Dataset used for the analysis is provided by [National University of Singapore](http://www.comp.nus.edu.sg/~sugiyama/SchPaperRecData.html). The data provider includes a detailed description on their webpage. Basically the dataset includes each researcher's most recent paper(s) (dataset has only 1 most recent paper for junior researchers but multiple for senior researchers), a few hundreds of candidate papers, and citation/reference relationship between papers. Instead of providing the raw papers, the data provider vectorized both candidate papers to recommend and researchers' papers, which makes it challenging for me to verify recommendations. 

My content-based recommender focuses on the junior researchers. Cosine distance is used to measure article similarity. For now the analysis does not consider network - it is possible that the top recommendations are papers that the researcher of interest did not lead (and therefore is not the first author) but were involved in (s/he participated in the study). Including citation/reference relationship information in the picture could lead to the same it-recommends-my-own-study result. Figuring out which/how researchers are connected with others may provide us a remedy. 

Many possibilities exist for future work. I am most interested in adding the abovementioned network element to the analysis. Other similarity metrics can also be introduced. After experimenting with these techniques I will expand the analysis to the senior researchers. 

## Requirements ## 
`Python` and the usual analytical packages such as `numpy`. 
