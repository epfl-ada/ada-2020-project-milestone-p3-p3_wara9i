## Title : 

Signed networks intercommunities

## Abstract : 

Signed Networks in Social Media presents a study on how well can the theories of balance and the theory of status predict the relationships between INDIVIDUAL users on social networks.

We propose to study how these theories can explain the relationships between COMMUNITIES, and the "online social networks" they represent.

To do this we will investigate the Reddit Hyperlink Network dataset.

In Reddit, a sub-reddit can be seen as a community, where individual users "subscribe" to a subreddit and become "affiliated" to it, by being active and posting.

And sometimes, some posts in a sub-reddit can contain hyperlinks to other an sub-reddit, either to "neutrally" evoque it, "praise" it or "insult" it.

We say a hyperlink originates from a post in the source community and links to a post in the target community.

We will study how well can the analyses made for individual users can be made on communities.


## Research questions :

How effective are the two theories (balance and status) in explaining/predicting the relationship (i.e sign of edges)
between communities ?

What are the differences and similarities between communities and
individual relationships ?

Are there some assumptions that can be made to transform the individuals datasets (i.e Epinions, Slashdot, Wikipedia) into communities dataset (by clustering and viewing clusters as communities) that gives us similar results as the community one we already have (i.e Reddit) ?

How effective are our methods in modeling relationships between
communities and where are the biases and limitations of this
method ?

## Proposed dataset :

We will use the Reddit Hyperlink Network (link : https://snap.stanford.edu/data/soc-RedditHyperlinks.html).

It is a list of posts, whith attributes relating the source subreddit from which the post originates, the target subreddit, and the sentiment of the post.

Thus it represents a **directed, signed, temporal** subreddit-to-subreddit hyperlink network.

- It is extracted from publicly available Reddit data of 2.5 years from Jan 2014 to April 2017.

- The most important columns we will make us of : 

	- SOURCE_SUBREDDIT: the subreddit where the link originates.

	- TARGET_SUBREDDIT: the subreddit where the link ends.

	- TIMESTAMP: time of the post.

	- POST_LABEL : label indicating if the source post is explicitly negative towards the target post. The value is -1 if the source is negative towards the target, and 1 if it is neutral or positive. The label is created using crowd-sourcing and training a text based classifier, and is better than simple sentiment analysis of the posts.

## Methods :

To build the networks we will use the Python NetworkX package.

First, we will load the data, and make some data sanitizing by removing the columns we do not need, transforming subreddit names by unique node IDs.

Then, because we will have duplicates in (SOURCE, TARGET) pairs (because the same source subreddit can contain multiple posts that convey a similar/different sentiment to the same target subreddit), we will average the POST_LABEL signs of all the duplicates to have a unique "weight" that is between -1 and 1.

We will have enough information to make a **weighted, directed, signed** network.

We will look in the literature, or/and think of feasible methods that embodies the theory of status and theory of balance for **weighted** networks.

The most naive method that comes to mind is to simply take the sign of the weight, to have an ordinary **signed network**, as the one investigated in the original paper, and that is our first track to follow.

We will try to reproduce key results found in the paper but for the Reddit-Community dataset, such as results of different tables and make analyses of these results, comparing them with the individuals datasets.

If it turned out that the results for this naive method are inconclusive, we will try to find a better method of analysing the Reddit-Community **weighted** network under the scopes of Balance and Status theories.

And if time permits, we will try to transform our individuals networks (i.e Epinions, Slashdot, Wikipedia) into a network representing communities, by clustering, computing "averages" over the signs in/out-going edges between clusters, giving us weights, with which we will deal similarly as how we dealt with the Reddit-Community dataset, to try to see if there is meaning in viewing such clusters of people as Communities.

## Proposed timeline :

## Organization within the team :

## Questions for TAs :
