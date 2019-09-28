# Python for Data Science Essential Training

## Overview Notes

### 1. Data Munging Basics
#### 1.1 Filter and select data 
* data indexing
  * label index `df.loc[]`  
  * integer index `df.iloc[]`  
* data slicing  
* comparing with scalars  
* filtering with scalars  
* setting values with scalars  
#### 1.2 Treat missing values 
* discover what is missing  
  * `np.nan` is a missing value  
  * find missing values with `Series.isnull()`  
* fill in missing values  
  * in dataframe, use `df.fillna()`  
    * fill with 0's `df.fillna(0)`  
    * fill with a dictionary `df.fillna({})`  
    * fill forward down the col `df.fillna(method='ffill')`  
* count missing values  
  * in dataframe, `df.isnull().sum()`  
* filter out missing values  
  * `df.dropna()`  
#### 1.3 Remove duplicates
* test for duplicates 
  * in dataframe, `df.duplicated()`  
* drop duplicate rows  
  * `df.drop_duplicates()`  
* drop duplicate columns  
  * `df.drop_duplicates([col name])`
#### 1.4 Concatenate and transform data
**concatenate** - combine data from different sources  
**transform** - change the data to suit your needs  
* concatenate data on rows  
  * `pd.concat([df1, df2], axis=1)`  
* concatenate data on columns  
  * `pd.concat([df1, df2])
* drop data  
  * *rows:* `df.drop([])`  
  * *cols:* `df.drop([], axis=1)`  
* join columns  
  * `df1.join(df2)`  
##### append data tables  
```
df1.append(df2, ignore_index=False)
```  
* use `ignore_index=False` if don't want the index to update  
##### sort the data  
```
df.sort_values(by=[cols], ascending=[bool])
``` 
#### 1.5 Group and aggregate data  
* `df.groupby([cols]).agg(ftn)`  


### 2. Data Visualization Basics
#### 2.1 Create standard line, bar, and pie plots  
* need to run the line `%matplotlib inline` if want jupyter to print the plots inline  
* use `matplotlib.rcParams` (dictonary) to update asthetic things  

##### line chart:
 * create a line chart from a list obj - `plt.plot(x,y)`  
 * create a line chart from pandas - `df.col_name.plot()`  
 * line chart from dataframe comparing different columns - `df[[col1, col2, col3]].plot()`  
  
##### bar chart: 
 * create bar chart from a list - `plt.bar(x,y)`  
 * create bar chart from pandas - `df.col_name.plot(kind='bar')`
 * create horizontal bar chart - `df.col_name.plot(kind='barh')`  
  
##### pie chart:
 ```
 plt.pie(x)  
 plt.show()
 ```  
##### save a plot:
 ```
 plt.savefig('pie_chart.jpg')
 plt.show()
 ```
 
#### 2.2 Define plot elements

##### Two methods for plot building:
1. *functional method* - call plotting functions on set of variables  
2. *object-oriented method*  
 i. create blank figure object  
 ii. add axes to the figure  
 iii. generate plot(s) within the figure object  
 iv. specify plotting and layout parameters for the plots  

*subplot* - a plotting figure that contains more than one plot (or subplots)  

##### basic syntax:  
 ```
 fig = plt.figure()  
 ax = fig.add_axes([.1, .1, 1, 1])  
 ax.plot(x,y)
 ```  
 * need to define `plt.figure()` and `fig.add_axes([])` each time  
##### set axis limits and tick marks  
 ```
 ax.set_xlim([start, end])
 ax.set_ylim([start, end])
 ax.set_xticks([...])
 ax.set_yticks([...])
 ```
#### 2.3 Format plots
#### 2.4 Create labels and annotations
#### 2.5 Create visualizations from time series data
#### 2.6 Construct histograms, box plots, and scatter plots

### 3. Basic Math and Statistics
#### 3.1 Use NumPy arithmetic
#### 3.2 Generate summary statistics
#### 3.3 Summarize categorical data
#### 3.4 Parametric methods
#### 3.5 Non-parametric methods
#### 3.6 Transform dataset distributions

### 4. Dimensionality Reduction
#### 4.1 Introduction to machine learning
#### 4.2 Explanatory factor analysis
#### 4.3 Principal component analysis (PCA) 

### 5. Outlier Analysis
#### 5.1 Extreme value analysis using univariate methods
#### 5.2 Mulitvariate analysis for outlier detection
#### 5.3 A linear projection method for multivariate data

### 6. Cluster Analysis
#### 6.1 $k$-means method
#### 6.2 Hierarchical methods
#### 6.3 Instance-based learning with $k$-nearest neighbor

### 7. Network Analysis with NetworkX
#### 7.1 Intro to network analysis 
#### 7.2 Work with graph objects
#### 7.3 Simulate a social network
#### 7.4 Generate stats on nodes and inspect graphs

### 8. Basic Algorithmic Learning
#### 8.1 Linear regression model
#### 8.2 Logistic regression model
#### 8.3 Naive Bayes classifiers

### 9. Web-Based Data Visualizations with Plotly
#### 9.1 Create basic charts
#### 9.2 Create statistical charts
#### 9.3 Create Plotly choropleth maps
#### 9.4 Create Plotly point maps

### 10. Web Scraping with Beautiful Soup
#### 10.1 Introduction to Beautiful Soup
#### 10.2 Explore `NavigatableString` objects
#### 10.3 Parse data
#### 10.4 Web scrape in practice

### Conclusion:  Next Steps 
