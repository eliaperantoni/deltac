# $\Delta$ Counter

An Apache Spark pipeline for counting the number of triangles in a large
undirected graph.

---

[Link to Jupyter Notebook](./project.ipynb)

[Link to PDF report](./report.pdf)

---

The problem of counting triangles in a graph inherits great importance from
several interesting metrics on graphs that build upon it. The clustering
coefficient, for instance, is a measure of the degree to which nodes in a graph
tend to cluster together. Evidence suggests that real world graphs, social
networks in particular, tend to create tightly knit groups characterized by a
relatively high density of ties. This metric, arguably a very insightful one,
requires the number of triangles to be known, in order to compute it. Hence, its
relevance.

In recent years, internal and external memory algorithms have been developed to
solve the problem of triangle counting; but some of the graphs that we wish to
analyze have become so large that they can no longer fit inside a single
machine.

One possible solution, is distributing the computation across multiple machines
using the Map-Reduce technique. This project, provides an implementation for the
_Triangle Type Partition (TTP)_ Map-Reduce algorithm, introduced in _Park,
Ha-Myung, and Chin-Wan Chung. "An efficient mapreduce algorithm for counting
triangles in a very large graph." Proceedings of the 22nd ACM international
conference on Information & Knowledge Management. 2013_.
