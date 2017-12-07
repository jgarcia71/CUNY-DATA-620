# Final Project, IS 620

## Overview and Hypotheses

For our final project, Sonya and Joy will build upon the network analysis of senators in the current (115th) Senate session and do textual analysis of the communication of senators who demonstrate high centrality as well as textual analysis of the bills that demonstrate high centrality.

Our hypothesis is that senators who demonstrate high levels of influence as demonstrated by high centrality metrics will have communication styles, quantity, or content that will distinguish them from senators with low centrality.  We also hypothesize that Senate bills that demonstrate high levels of centrality will also have distinctive textual traits.  

Additional questions of interest that we would like to address if time permits include textual traits that are party-based.  Do bills supported principally or entirely by Democrats have markedly different vocabulary, sentiment, or semantic content than bills supported by Republicans?  Do bills that have bipartisan support demonstrate a combination of the Democratic and Republican traits, or instead show a new style that does not strongly represent either?  The same sort of party-specific analysis could also be applied to senator communication.

## Sources

We will use:

* Information about senators as provided by the ProPublica Congress API
* The text of bills as provided by the ProPublica Congress API
* Information about bill sponsorship as provided by the ProPublica Congress API
* Facebook account IDs and Twitter account IDs of senators as provided by the ProPublica Congress API
* Facebook and Twitter postings on senator accounts as provided by the respective social media APIs

## Plan

We will build upon the centrality measures we calculated for both senators and bills and rank the centrality of both groups.  We will build our comparisons by identifying the 10-20% most and least central senators and bills. 

Once we have our groups (most and least central senators and most and least central bills), we will obtain texts related to these groups.

Texts for senators includes the content of their Facebook and Twitter posts.  We will use APIs or where necessary web scraping to obtain the texts for analysis.  Texts for bills can be obtained via the ProPublica Congress API.

Textual analyis will consist of an analysis of metadata (social media use in frequency and post length, bill length) as well as sentiment and semantic analysis of the texts themselves.

## If Time Permits

If we have more time to do a bit of a stretch, Sonya and Joy will also find senator centrality within party (e.g. which Republican is most highly connected to other Republicans) and partisan strength of bills (which bills are most exclusively supported by a single party).  This will allow us to compare strongly partisan bills and senators across party.  We will compare the social media communications of strongly partisan Republican and strongly partisan Democratic senators as well as compare the bill texts of partisan bills.  We suspect that we will find textual features that will distinguish Democratic and Republican thought by comparing across party, using strongly partisan samples.

## Presentation of Findings

In order to simplify the presentation of findings, it makes sense to divide our work into smaller scripts, each of which is a well-structured example of literate statistical programming.  Creating well planned scripts and interfaces will also allow us to split up work in an agile approach, without waiting for each segment to be completed before beginning work on another.  Tentatively, we will have the following scripts and interfaces:

* A script to rank the centrality of senators and bills (this will be combined as we determine centrality in terms of the interrelationship of senators sponsoring and cosponsoring bills).  The output from this will be csvs listing the most and least central senators and most and least central bills.
* A script to gather and analyze Twitter and Facebook texts from our most and least central senators.  This script will take a csv as input, will query the ProPublica API to get Facebook and Twitter account names, and obtain corpora, which will then be analyzed.  The output will be some statistical features of the the text production of highly and minimally central senators.
* A script to obtain and analyze text from highly and minimally central bills.  This script will use a csv as input, obtain texts from ProPublica's Congress API, and conduct textual analysis.  The output will be statistical features of the bill text of the two types of bills.
* A markdown file that will describe the methods and findings of the study as well as reproducibility tips for those who would like to adapt the scripts for other uses (e.g. studying a different Senate session, studying the House of Representatives, etc.)