Toolkit
- Data Manipulation Tools for modifying CSVs: PERL, regular expressions.  Cool book - Data Munging in PERL
- Interactive Analysis start with Excel.  If data is too big, sample.
- You need a general purpose programming tool to complement R.  
- Free viz tool - ggobi
- Version Control tool

Decision Tree
- 1st part of algorithm is split-search
 - When splitting is done with the chi-squared criteria, split to maximize the log worth (- log chi-squared p-value)
  - criteria is usually somewhat more complicated - for example, you cannot have fewer than a specified number of observations in a branch
  - bonferroni correction used to adjust p-values since many statistical tests are being done in parallel
  - in addition, each level of the tree depends on the p-values of prior splits.  There is an additional depth adjustment to the p-values. 
 - algorithm tries putting missing values on both left and right side of split
- 2nd Part: Pruning
 - Remove a specified number of branches from the tree.  Various combinations will produce different subtrees.  
 - Assess each with validation data and choose the best performing simplest model.
 - statistic used to assess tree will depend on whether you want a ranking, decision, or estimate.
  - Decision
   - can be evaluated by accuracy / misclassification rate
  - ranking
   - evaluated by concordance
  - estimate
   - evaluated by squared error
  - The pruning stage is different depending on whether we want ranking, decision, or estimate.  This doesn't make a difference on the first stage.
