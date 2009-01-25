## Idea and origins##
Although partially ordered and directed spaces originally arose in Analysis and General Topology, the recent interest in them has resulted from attempts to model state spaces of evolving processes, particularly those that arise in modelling concurrent programming. They also occur in models of space-time and in modelling certain modal logics.

The basic idea is that of a topological space in which points can be compared using a partial order corresponding to 'precedes'. 





##Definitions## 

* A **partially ordered space** or **pospace**, $X$, is a topological space with a (globally defined) closed partial order, $ \leq$, so considering $\leq $ as a subset of $X\times X$, it is a closed subset.

* A **dimap** $f : X \to Y$ between two pospaces, $X$ and $Y$, is a continuous map that respects the partial order,
$$x\leq x^\prime \Rightarrow f(x) \leq f(x^\prime).$$

There are several useful notions of 'homotopy' between dimaps. Choosing between them depends on the  intended use and/or the situation being modelled.

* Suppose $a$ and $b$ are dimaps between $X$ and $Y$. A **directed homotopy** between $a$ and $b$ is a dimap
$$h : X \times I_d \to Y,$$ 
where $X \times I_d$ is given the product partial order. (The pospace $I_d$ is defined below amongst the examples.)




We say $a$ and $b$ are **dihomotopic**, the relation being called **directed homotopy**.

#Examples#

* The _standard directed interval_ is $I_d = ([0,1], \leq)$ is a pospace that gives rise to the d-space of the same name.

* Any [[pospace]] $X$ gives rise to a [[d-space]] by taking the 
directed paths to be,..., directed paths, i.e. dimaps from $I_d$ to $X$. (It can be helpful to use directed paths of variable length based on $\stackrel{\to}{[0,r]}$ the directed version of the interval of length $r$.



