<link rel="stylesheet" href="http://netdna.bootstrapcdn.com/bootstrap/3.0.3/css/bootstrap.min.css">
<style type="text/css"> body {padding: 10px 30px 10px 30px;} table,th, td {text-align: center;}</style>
<style>
td.tableRow
{
text-align:center;
}
</style>


Customer Segmentation in the Boating Industry
========================================================

**J. Niessing, INSEAD**

**T. Evgeniou, INSEAD**


The Business Issue
---------------------------------------------------------

A boating company had become a victim of the crisis in the boating industry. The business problem of the "Boat" case study, although hypothetical, depicts very well the sort of business problems faced by many real companies in an increasingly data-intensive business environment. The management team was now exploring various growth options. Expanding further in some markets, in particular North America, was no longer something to consider for the distant future. It was becoming an immediate necessity. 

The team believed that in order to develop a strategy for North America, they needed a better understanding of their current and potential customers in that market. They believed that they had to build more targeted boats for their most important segments there. To that purpose, the boating company had been commissioned a segmentation project for that market. Being a data-friendly company, the decision was made to develop a segmentation in a data-driven way - none of that soft hold-hands-and-discuss stuff. 


The Data
--------------------------------------------

With the aid of a market research firm, the boating company gathered various data about the boating market in the US through interviews with almost 3,000 boat owners and intenders. The data consisted, among others, 29 attitudes towards boating, which respondents indicated on a 5-point scale (Q. 1, 1-29 shown in the survey in the appendix).

Other types of information had been collected, such as demographics (Q. 11-15 in the survey). Finally, the boating company had compiled information about the boats, such as the length of the boat they owned, how they used their boats, and the price of the boats (Q. 2-10 in the survey). A segmentation and profile of the market would be done using all this data. 

The Approach
--------------------------------------------

Based on past experience, the decision was made to develop a segmentation that was mostly driven by attitudes that consumer held regarding boating - the attitudinal data from the 29 questions in Q.1.

### Factor Analysis

As a first step, the company decided to simplify the data by grouping the 29 attitudinal statements in Q1 into a few meaningful sets/factors. This could be done using a standard method: factor analysis. The objective is to summarize information (the variation) in correlated raw attributes to a smaller number of manageable factors - which are typically uncorrelated or independent. In the process one decreases the number of raw attributes while keeping most of the information in the data in a statistical sense. This data reduction technique is a very useful step in helping interpreting the data and make better decisions. It also helps to identify the key variables that should be used in the segmentation procedure. 

We first have to read the whole dataset, which is in CSV format.

For the Factor Analysis, we will only use the 29 items of the data that describe the attitudes towards boating of people in the sample. Such 29 items are measured on a Likert scale of 1-5. All the 29 items are integer variables that take values between 1 (=strongly disagree) and 5 (=strongly agree).

Every factor analysis has three basic decision points:  

- Decide the number of factors, 

- Choose an extraction method, 

- Choose a rotation method.  


Sometimes it makes sense to run a quick correlation matrix before the factor analysis. It usually gives a first glance at the inter-relationships between variables and it is often an input for factor analysis (i.e. eigenvalue decomposition of the correlation matrix). In this example the correlaton matrix for the 29 attitudes looks like this: 

<style>
.wrapper{


width: 100%;

overflow-x: scroll;

}
.wrapper1{

height:400px;
overflow-y: scroll;
}
th.wrapper{
display:block;
}

</style>




<div class="wrapper wrapper1 th.display">


```
Error in is.data.frame(x): object 'ProjectDataFactor' not found
```

```
Error in is.data.frame(x): object 'ProjectDataFactor' not found
```

```
Error in rownames(thecor): object 'thecor' not found
```

```
Error in lapply(x, f): object 'thecor' not found
```

</div>
</div>
### Number of Factors

There are three common ways to select the optimal number of factors from a statistical perspective:

1. All factors with eigenvalue larger than 1

2. Based on the cumulative variance we would like to explain (e.g. at least 50% for example)

3. Pick the number of factors corresponding to the "elbow" of the scree plot

The first two approaches to select the number of factors/derived variables can be seen in the following table: 
































