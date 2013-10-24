The reason we teach SPSS - some first just use SPSS and don't have SAS.  Three 1.5 hour sessions.
Designed for people who wanted to avoid code and instead point-and-click, though it does allow you to code.
We are using a just-released version, 22.  Noticed a couple of bugs.
SPSS 21.0 tutorial is available on the moodle

Data Editor interface looks very similar to excel.  Variables in columns, rows with data.  Variable view is essentially your code book.  

Open => New => Syntax opens a code window.  Every dataset has its own syntax window, output window, and scripts window.

### Variable View 
- Missing data shows up as a .  You can code missing values as well, using "Discrete Missing Values"
- Measure options let you set as Nominal, Ordinal, Scale (continuous)
- Role lets you set your target
- You can add and delete variables from the variable view.

### Data View
- You can also add variables here with a right-click menu option

With cluster analysis, wrong variable types can cause problems.

Same menu bar options regardless of which view you are looking at.

### Options
- you can readch this by clicking Edit => Options
- On the output tab, Dr. D likes to switch all the options on the left to "values and labels"

### Transform
- Compute variable option 
 - allows you to create new variables using calculations on existing values.
 - Clicking the "If.." will allow you to subset your data according to a criteria.
- Recode
 - Probably best to use "recode into different..." so that you don't overwrite
 - You can use ranges.  Ranges are inclusive.
- Visual Binning
 - Will show you how it bins a continuous variable.  By default makes 10 bins.
- Replacing Missing Values
 - Multiple ways to handle
 - Reason to replace - some techniques will delete entire case if there is even one missing value.
 - Imputing Categorical Data
  - Using the mean to imputing categorical data is not generally a good idea
  - One option is to regress the missing variable on the other variables.
 - Important to understand the reason the data is missing.
 - Very important to handle missing value analysis correctly.  In previous years, eliminating obs with missing values results in a data set 30% the original size

### Analyze
- Reports => Codebook will create a report of your analysis (I THINK)
- TURF Analysis - Total unduplicated region and frequency.  If you are trying to avoid duplication between two promotions
- Multile Response: You can use this to analyze multiple responses, like a person who said they have a checking account AND an IRA account
- Quality Control - lets you see variability... I think this is mainly for industrial applications
- Chart Builder

### Chart
- Gallery is the easier / quicker way to create charts

### Syntax View
- Use asterisk to comment
- Like SAS, will run code you have highlighted.  If nothing is highlighted, runs all your code.
- Always be careful to save

### Output Window
- Will give you a log with warnings.

### Add-ons
- Correspondence Analysis: dimension reduction for categorical data

### Help
- Topics
- Tutorials
- Cas Studies are very good

#### Next Class - we will work with some real data.



