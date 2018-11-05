# PersistenceCurves
A python package for computing Persistence Curves

## Brief Introduction
Computational Topology is a field of mathematics concerned with examining and utilizing the shape of a dataset to discern the shape of the underlying space. The main tool of this field is Persistent Homology. Using this tool on a dataset yields a visual summary called a Persistence Diagram, which are multisets of points. We can define a metric on these diagrams called the bottleneck distance. These diagrams are stable with respect to this distance in the sense that a small change in the dataset leads to a small change in the diagrams. The set of all persistence diagrams with this bottleneck distance forms a metric space. However, performing machine learning tasks with this space is difficult. For this reason, much work has been done towards creating useful, clever vectorizations of these diagrams that are compatible with machine learning algorithms. Such vectorizations include the [Euler Characteristic Curve](http://www.cs.huji.ac.il/~werman/Papers/1-s2.0-S0167865514002050-main.pdf) (ECC), [Persistence Landscapes](https://arxiv.org/abs/1207.6437) (PL), [Persistence Codebooks](https://arxiv.org/abs/1802.04852), [Persistence Images](https://arxiv.org/abs/1507.06217), and [Persistence Paths]((https://arxiv.org/abs/1806.00381)). Our vectorization, called Persistence Curves (Pre-print forthcoming), generalize both the ECC and PL.

## The Package

### The Diagram Class
The sole class of this package is Diagram. This package assumes the user has already calculated the persistence diagram(s) of interest. Essentially a diagram is an array or data frame of shape (x,2). Suppose D is a diagram. The code below transforms D to the Diagram class.

```python
import Diagram
Diagram(D)
```

