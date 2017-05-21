Prosper Loan Analytics
========================
Xiaxi Li



### Summary ###
This visualization attempts to illustrate various factors that determine the quality of a loan, specifically, its probability to default. The data to derive this infograph is the loan information from Prosper Loan company, with 110k+ data entries, each containing 81 variables. Key variables include descriptor of the loan, such as loan APR and listing-creation-date, and descriptors of the borrower, such as the income, the credit score, and debt-to-income ratio. Besides confirming some commonly known key descriptor such as credit score, this visualization allows the viewers to see impacts of other factors, and reveal some subtlety in the operation of Propser Loan company.


### Design ###

**The initial concept**

The infograph needs to have bar chart to show readers the general status of all loans issued, and the loan status needs to be broken down as function of different categories such as credit score. As shown in the following picture.



 
**The MVP1**

This minimum viable product shows the following functions
	1. Horizontal bar chart showing the ratio of loan status, also served as the legend for the colors used in the stacked bar chart.
	2. Stacked bar chart using different factors (list creation date, loan APR, etc.) as X, count/percentage as Y, and grouped by loan status by different colors.
	3. Buttons on the lower left corner, which can be clicked to switch the indicator (X) on the right panel.


### Feedback ###

Feedbacks are collected on MVP 1.

**Viewer 1:**
	
* I think the legend should reflect the colors used in the visualization and therefore have maybe some icons to show what is what
* Some of the text is missing some spacing, such as "DebtToIncomeRatio"
* Add a story/narrative to explain the data
* Maybe fix the margins a bit so that the left side of the graph fits the page better

**Viewer 2:**

* The y labels of the two right axis need to be fixed. They are both "count"
* The ListingCreationDate does show some trend, but it is misleading. The quality of the loan is not the only factor that impact the data. For example, there must be more loans to be current, if the creation date is closer to current date; and the default rate must be lower since there is not enough time for a loan to go to default status. 
* The correlation with credit score is very clear.
* What type of loan has more default rate? Curious to know.
* Highlight selected panel, otherwise the reader get confused what they are looking at.
* The NA should be removed from BorrowerAPR.

**Viewer 3:**

* Why use bar plot? It looks monotonous.
* Looks like all shown here can be simply done by Excel, maybe show some strength of d3?


### Final Design ###
**Changes made for MVP2:**
	
1. Adding narrative structure
	* Narrative structure added: first to introduce the loan status percentage, then describe the break-out
	* Explain the purpose below the title, using d3plus to wrap text
	* Add comments for each category
	* Change the category "IncomeRange" to "Stated monthly income" for better visualization of the trend.
<br><br>
             
2. Fixing aesthetic issues
	* Redesign the layout
	* Add smooth animation to the barchart
	* Fix axis labels
	* Remove NA from data
	* Highlight selected category


 
**Project repository**

[GIST: ](https://gist.github.com/xiaxili2004/6e7ad2a48f4ddc61ecd1e57c04013899)
MVP1 and MVP2 are both included

[bl.ocks.org: ](http://bl.ocks.org/xiaxili2004/raw/6e7ad2a48f4ddc61ecd1e57c04013899/) Final visualization


### Resources ###

Special thanks to Udacity forum mentor @Myles

How to pass argument to callback function:
	[link](http://stackoverflow.com/questions/3458553/javascript-passing-parameters-to-a-callback-function)

How to order stacked bar chart series
	[link](http://stackoverflow.com/questions/25015266/ordering-columns-in-a-stacked-bar-chart-dimple)

Design of color theme
	[link](http://paletton.com/)
