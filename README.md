# Blog post: an example on Vintage Sparse PCA

## 1 The background and main question

Semantic Scholar Open Research Corpus contains research papers published in
all fields and is provided as an easy-to-use JSON archive. There are about 220
million papers and over 100Gb meta data. We study the citation network and
term-abstract network on this massive collection of academic publications.

This post is an starting example toward our course project, and we focus
on all papers relate to a good technique "false discovery rate" or "FDA" in
short here. The FDR conceptualize the rate of type I errors in null hypothesis
testing with multiple comparisons. The FDR was first formally introduced by
Benjamini and Hochberg in 1995 [1]. It has been particularly influential and
gain broad acceptance in many scientific fields including life sciences, genetics,
biochemistry, oncology and plant sciences. Thus we can expect a good sample
size and some good clustering result in this example.

We first set all papers that mention "false discovery rate" in their abstract as
our data-set, then we consider the community detection and cluster the data-set
by citations (both in-Citations and out-Citations) using vintage sparse principle component analysis (VSP). Next, we redo the clustering for the Cititation
networks using bag-of-words representation of the abstracts (BFF). Finally, we
do the comparison across the classes, such as the class size, the first published
year and the regression along the time (in the next step toward the project).

```{r}
x = 2 + 3
```