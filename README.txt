1. Datasets included:
	unaltered10000reviews.csv - Dataset downloaded from link https://www.kaggle.com/omkarsabnis/yelp-reviews-dataset.
	expanded10000reviews.csv. - Same as unaltered10000reviews.csv except run through YelpExpandContractions.ipynb to expand contractions
	unaltered1000reviews.csv  - Data collected with code in YelpDataCollection.ipynb. Does not produce usable results with YelpDataAnalysis.ipynb because of its small size, but included as it was used in the process of this project
	 
2. General Instructions:
	All the code was written and tested in Google Colab (https://colab.research.google.com), a virtual environment.It does require a login with a Google account. Code should work with any program that can run .ipynb file. You may just need to install "nltk" and "imblearn" with pip install.  Also the pycontractions library used in YelpExpandContractions.ipynb requires openjdk8 install which I believe downgrades Java version, which is why a virtual notebook may be preferred and why expandedreviews10000.csv was included with the project to bypass the use of the pycontractions library . For those reason I would strongly recommend just running the code on Google Colab.

	If using Google Colab, upload notebook file using File->Upload, and then drag and drop required csv files into starting directory in files tab on left side of screen. Then follow Instructions below
	If not using Google Colab, drag and drop csv files into directory with .ipynb files

	IF ALL ELSE FAILS: 
	You can use this link to run copy from my google account: https://colab.research.google.com/drive/1bCANnEks005UUpHIRuL3q_4KjvPuTzoV?usp=sharing&pli=1#scrollTo=rb_RMfDF1G
	Revision history can be viewed to verify that the code was not modified since the due date if this link is used at File->Revision History
 
2. Instructions/Notes for Files Included:
	
YelpExpandContractions.ipynb - Python Notebook containing code to expand contractions of csv files

INSTRUCTIONS:
Add csv file to folder, and change string at line 2 to different filename if needed (set up to process unaltered1000reviews by default for demo purposes as processing 10000 reviews takes time). Run setup cell, and then cells labeled 1 and 2
	
YelpDataAnalysis.ipynb       - Python Notebook containing code to preprocess, vectorize and fit data to machine learning model to make predictions

INSTRUCTIONS: 
After adding included csv files to folder, run cells in numbered order. Optional cells are cells we used in determining best techniques/models for project, but are not required to be run as notebook is set up with our most optimized setup to produce our best results by default. If you want to run your own dataset, change the filename read into the pandas data frame at line 1 of code block 2 in the cell labeled "1) Read in Reviews"

YelpDataCollection.ipynb.    - Python Notebook containing data collection code.  Does not currently collect review texts and ratings correctly at the moment because of Yelp website change, but included as it was used in the process of this project

INSTRUCTIONS: 
Paste your own user agent into user_agent variable at line 16 and run cell.

(Readme written by Daniel Simpson)