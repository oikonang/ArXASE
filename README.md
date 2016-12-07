# ArXASE 
### ArXiv.org Abstract Similarity Engine

## What is arXiv?

The arXiv (pronounced *archive*) is a repository of electronic preprints, known as e-prints, of scientific papers in the field of **mathematics**, **physics**, **astronomy**, **computer science**, **quantitative biology**, **statistics**, and **quantitative finance**, which can be accessed online

## What we will do with it
### Part 1
In this project, we will extract prepints of the API of arXiv, collect the abstract of each article, clean the text (tokenize, lowercase, extract stopwords, lemmatize) and then extract the most important words with **TF-IDF**, and remove the rest. Then we will start building a network graph(directed), using the papers and the words of each paper as nodes. In order for the nodes to be distinguised between each other(nodes and words), we will assume that **paper-nodes** will always have *non-zero out-degrees* and **word-nodes** the opposite.

### Part 2
This graph will then be the basis for a new undirected graph, where all word-nodes will turn into edges. Since we can't have multiple edges between the two same nodes, we will instead set the weight of the edge. The more common words, the higher the **weight**.

### Part 3
Furthermore we will also do **community detection** on the undirected graph, useful for finding papers in different, and potentially unexpected fields of study.

### Part 4
We will create a **wordcloud** per community and analyse the frequency of each field of study per community