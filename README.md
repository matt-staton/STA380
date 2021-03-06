# STA 380: Predictive Modeling

Welcome to part 2 of STA 380, a course on predictive modeling in the MS program in Business Analytics at UT-Austin.  All course materials can be found through this GitHub page.  Please see the [course syllabus](syllabus.md) for links and descriptions of the readings mentioned below.

## Office hours 

On Friday, July 29th, I will hold office hours from 10am to 12pm (normal class time).  I will start in my office (CBA 6.478), but if a lot of folks show up at once, we'll move to the regular classroom.

On Tuesday (8/2) and Thursday (8/4), I will hold office hours from 9-10 AM in CBA 6.478.


## Scribe notes and exercises

To submit your scribe report, please e-mail me link to a .pdf or .md file on your own GitHub page (james.scott at mccombs.utexas.edu).  Do not send an attachment.

You can find the up-to-date collection of [scribe notes here](scribe/).  

The first set of exercises is [available here](exercises/exercises01.md).

## Topics 

### (0) The data scientist's toolbox

Good data-curation and data-analysis practices; R; Markdown and RMarkdown; the importance of replicable analyses; version control with Git and Github.

Readings:  
- [a few introductory slides](notes/STA380intro.pdf)
- [Jeff Leek's guide to sharing data](https://github.com/jtleek/datasharing)  
- [Introduction to RMarkdown](http://rmarkdown.rstudio.com)  
- [Introduction to GitHub](https://help.github.com/articles/set-up-git/)    

### (1) Foundations of probability  

Basic probability, and some fun examples.  Random variables, probability distributions, expected value.  Joint, marginal, and conditional probability.  Independence. Law of total probability.  Bayes' rule.  

Readings:
- [excerpts](notes/probability_book_excerpt.pdf) from an in-progress book on probability.  
 
Some optional stuff:  
- [Bayes and the search for Air France 447](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.370.2913&rep=rep1&type=pdf).  
- [YouTube video](https://www.youtube.com/watch?v=U9-G-noZrwc) on Bayes and the USS Scorpion.  
- [Pretty-but-wrong visualization](http://www.nytimes.com/interactive/2014/09/14/sunday-review/unplanned-pregnancies.html) by the New York Times on the long-term failure rates of various contraceptive methods, together with [James Trussell's explanation](http://io9.gizmodo.com/what-are-the-real-odds-that-your-birth-control-will-fai-1634707739) of why the 10-year numbers are wrong.  His quote is about halfway down the page.  A great example where assuming independence can lead to trouble!  


### (2) Exploratory analysis

Contingency tables; basic plots (scatterplot, boxplot, histogram); lattice plots; basic measures of association (relative risk, odds ratio, correlation, rank correlation)

Scripts and data: 
- [gdpgrowth.R](R/gdpgrowth.R) and [gdpgrowth.csv](data/gdpgrowth.csv)   
- [titanic.R](R/titanic.R) and [TitanicSurvival](data/TitanicSurvival.csv)  

Readings:  
- [excerpts](notes/DataExploration.pdf) from my course notes on statistical modeling  
- NIST Handbook, Chapter 1.  
- R walkthroughs on basic EDA: [contingency tables](http://jgscott.github.io/teaching/r/titanic/titanic.html), [histograms](http://jgscott.github.io/teaching/r/citytemps/citytemps.html), and [scatterplots/lattice plots](http://jgscott.github.io/teaching/r/sat/sat.html). 
- [Bad graphics ](notes/badgraphics.pdf)
- Good graphics: scan through some of the New York Times' best [data visualizations](http://www.nytimes.com/interactive/2014/12/29/us/year-in-interactive-storytelling.html?_r=0#data-visualization)


### (3) Resampling methods

The bootstrap and the permutation test; joint distributions; using the bootstrap to approximate value at risk (VaR). 

Scripts:  
- [gonefishing.R](R/gonefishing.R) and [gonefishing.csv](data/gonefishing.csv) 
- [montecarlo.R](R/montecarlo.R)  
- [portfolio.R](R/portfolio.R)  

Readings:  
- ISL Section 5.2 for a basic overview.  
- [These notes](notes/QuantifyingUncertainty.pdf) on bootstrapping and the permutation test.  
- [Section 2 of these notes](notes/decisions_supplement.pdf), on bootstrap resampling.  You can ignore the stuff about utility if you want.  
- [This R walkthrough](http://jgscott.github.io/teaching/r/creatinine/creatinine_bootstrap.html) on using the bootstrap to estimate the variability of a sample mean.  
- [Another R walkthrough](http://jgscott.github.io/teaching/r/titanic/titanic_permtest.html) on the permutation test in a simple 2x2 table.  
- Any basic explanation of the concept of value at risk (VaR) for a financial portfolio, e.g. [here](https://en.wikipedia.org/wiki/Value_at_risk), [here](http://www.investopedia.com/articles/04/092904.asp), or [here](http://people.stern.nyu.edu/adamodar/pdfiles/papers/VAR.pdf).

Optionally, Shalizi (Chapter 6) has a much lengthier treatment of the bootstrap, should you wish to consult it.    


### (4) Clustering

Basics of clustering; K-means clustering; hierarchical clustering.

Scripts and data:  
- [protein.R](R/protein.R) and [protein.csv](data/protein.csv) 
- [cars.R](R/cars.R) and [cars.csv](data/cars.csv) 
- [we8there.R](R/we8there.R)  
- [hclust_examples.R](R/hclust_examples.R)   

Readings:  
- ISL Section 10.1 and 10.3  
- Elements Chapter 14.3 (more advanced)    
- [K means examples](notes/kmeans_examples.pdf): a few stylized examples to build your intuition for how k-means behaves.  
- [Hierarchical clustering examples](notes/hclust_examples.pdf): ditto for hierarchical clustering.  
- K-means++ [original paper](http://ilpubs.stanford.edu:8090/778/1/2006-13.pdf) or [simple explanation on Wikipedia](https://en.wikipedia.org/wiki/K-means%2B%2B).  This is a better recipe for initializing cluster centers in k-means than the more typical random initialization.


### (5) Latent features and structure

Principal component analysis (PCA).  If time: canonical correlation analysis; multi-dimensional scaling.

Scripts and data:  
- [pca_2D.R](R/pca_2D.R)  
- [pca_intro.R](R/pca_intro.R)  
- [congress109.R](R/congress109.R), [congress109.csv](data/congress109.csv), and [congress109members.csv](data/congress109members.csv)  
- [gasoline.R](R/gasoline.R) and [gasoline.csv](data/gasoline.csv)  
- [FXmonthly.R](R/FXmonthly.R), [FXmonthly.csv](data/FXmonthly.csv), and [currency_codes.txt](data/currency_codes.txt)  
- [cca_intro.R](R/cca_intro.R), [mmreg.csv](data/mmreg.csv), and [mouse_nutrition.csv](data/mouse_nutrition.csv)  


Readings:  
- ISL Section 10.2 for the basics  
- Shalizi Chapters 18 and 19 (more advanced).  In particular, Chapter 19 has a lot more advanced material on factor analysis, beyond what we covered in class.      
- Elements Chapter 14.5 (more advanced)  


### (6) Text data

Co-occurrence statistics; naive Bayes; TF-IDF; topic models; vector-space models of text (if time allows).

Scripts and data:  
- [textutils.R](R/textutils.R) 
- [nyt_stories.R](R/nyt_stories.R) and [selections from the New York Times](https://github.com/jgscott/STA380/tree/master/data/nyt_corpus).
- [tm_examples.R](R/tm_examples.R) and [selections from the Reuters newswire](https://github.com/jgscott/STA380/tree/master/data/ReutersC50).
- [naive_bayes.R](R/naive_bayes.R)  
- [simple_mixture.R](R/simple_mixture.R)
- [congress109_topics.R](R/congress109_topics.R)

Readings: 
- [Stanford NLP notes](http://nlp.stanford.edu/IR-book/html/htmledition/scoring-term-weighting-and-the-vector-space-model-1.html) on vector-space models of text, TF-IDF weighting, and so forth.  
- (Using the tm package)[http://cran.r-project.org/web/packages/tm/vignettes/tm.pdf] for text mining in R.  
- [Dave Blei's survey of topic models](https://www.cs.princeton.edu/~blei/papers/Blei2012.pdf).  
- [A pretty long blog post on naive-Bayes classification](https://www.bionicspirit.com/blog/2012/02/09/howto-build-naive-bayes-classifier.html).  


### (7) Miscellaneous

Coverage of these topics will depend on the time available.  Possibilities include: anomaly detection; label propagation; learning association rules; graph partitioning; partial least squares.  

Scripts and data: 
- [playlists.R](R/playlists.R) and [playlists.csv](data/playlists.csv)  

Readings: 
- [Pradeep Ravikumar's notes on association rule mining](notes/lec-AssociationRules.pdf)  

