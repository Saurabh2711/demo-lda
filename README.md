## Topic modelling, cancer and air pollution

This repo is a "live" demo of how to perform topic modelling on a corpus of 3000 abstracts taken from scientific article metada. The articles are part of the [PubMed](http://www.ncbi.nlm.nih.gov/pubmed) database, and the [metadata provided by Epidemium](http://epidemium.3do2.fr/files/pubmed/) was pre-processed to :

	1. isolate the articles related to cancer and air pollution
	2. only keep the 3000 most relevant articles to the "cancer + air pollution" subject

### Result

Check a working version of the notebook [here on NbViewer](http://nbviewer.jupyter.org/github/hrjn/demo-lda/blob/master/notebook.ipynb).


### Content

Many things have been pre-computed: 

* `dictionary_abstracts_timespace.dict` is the dictionary of the text corpus
* `abstract_3000_bow.mm ` is the bag-of-words transformation of the corpus, stored into a *market-matrix* file (kinda like a Python dict, optimized for storing sparse matrices)
* `lda_50_topics_3000_abstracts.model` is the pre-trained LDA model that you can reuse if you don't want to train the model yourself. If you want to, feel free, all you need is here :smiley:
* `ldavis_3000_abstracts.html` is a "human-readable" and interactive format of the output of our LDA model. Go directly there if you don't want to see any code. 
* `notebook.ipynb` is where the magic happens (well, not all of it, we kept the gory details of pre-processing for a later episode).
* `abstracts_timespace.txt` is the raw corpus of the abstracts (not used in the notebook, but still necessary for reproducibility). One abstract per line. 
* `requirements.txt` is the list of required Python libraries. To install them, open a shell/Terminal, make sure you have `pip` installed, and run `pip install -r requirements.txt`. And that's it!
