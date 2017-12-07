## Week 4

### Problem definition:


Your task in this week’s assignment is to identify an interesting set of network data that is available on the web (either through web scraping or web APIs) that could be used for analyzing and comparing centrality measures across nodes.  As an additional constraint, there should be at least one categorical variable available for each node (such as "Male" or "Female"; "Republican", "Democrat," or "Undecided", etc.)


In addition to identifying your data source, you should create a high level plan that describes how you would load the data for analysis, and describe a hypothetical outcome that could be predicted from comparing degree centrality across categorical groups. 

### Identify Data

Sonya and Joy identified the network data available on the [ProPublica Congress API](https://projects.propublica.org/api-docs/congress-api/) as a good source of network data that could provide both categorical data for nodes as well as centrality metrics that make sense.

#### Nodes

Nodes could consist of:

- Lawmakers (Representatives and/or Senators), which have a number of attributes including categorical variables such as party affiliation and state represented
- Bills, which have a number of attributes including categorial variables such as party of sponsorship, active status, and enacted stats
- Committees (groups of lawmakers with special privileges relating to bills and nominations in their purview)

#### Edges

Edges could consist of:

- Sponsorship
- Votes
- Committee membership (lawmakers)
- Committee assignment (bills)

#### Centrality Measures

We could consider centrality in terms of the number of co-sponsorships of bills per lawmaker, the total number of votes cast (lawmaker engagement), or influential committee membership (e.g. membership in a committee that has a large number of active or enacted bills).

Interesting outcomes could include lawmaker engagement by party or relative importance / influence by committee.

### Constraints

In order to have a more tractable dataset, we will limit the time frame for both lawmakers and bills, to keep the total number of nodes and relationships reasonable.

### Methods

We have obtained an API key and conducted initial testing to download some sample data.  Our rough plan is:

- Obtain pilot data
- Sketch out a graph diagram to understand the problem
- Choose centrality measures of interest
- Choose categorical variables of interest
- Choose which attributes to keep and which to discard
- Obtain fuller dataset
- Clean data as required
- Transform data to network / graph 
- Check data transformation using visualization and querying
- Conduct initial exploration of data
- Calculate the chosen centrality measure(s) for the categories chosen
- Create and submit literate statistical code for the project

 
