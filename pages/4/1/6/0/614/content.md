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

#Discussion#

_[[Eric Forgy|Eric]]_: I can imagine that "directed" stuff might begin to garner more attention here, so could we settle on a notation? For example, I've used $\uparr$ to indicate that a space is directed so that the directed interval is denoted $\uparr I$. Above, it is given as $I_d$. I am slightly partial (but not firmly set) to using $\uparr$ to denote that a space is directed or partially ordered (or even preordered).

Second, I have a "continuum" allergy and never like to see a definition that explicitly evokes the continuum to define important objects. Is there a more combinatoric or abstract way to define pospaces, [[directed space|directed spaces]], and [[directed homotopy theory|directed homotopy]] that does not evoke the continuum immediately?

How/if is the standard directed interval related to [[interval object]]?

 _[[Tim Porter|Tim]]_:  I am also alergic to too much 'continuum' use.  The problem is to get a substitute that allows  and controls subdivision.  Ideas anyone?  Gabriel Minian (paper in _K-theory_ used a variant of Baues's cofibration category notion to handle various categories including that of simplicial complexes.  He used an Ind-object instead of an interval object. His theory is not a directed one, of course.  Marco Grandis also looked at the problem of subdivision in some papers and going right back there were notes by George Hoff and Marcel Evrard trying to do the homotopy theory of categories using concatentated intervals.  I can try to find references if it should proved useful.

As to combinatorial definitions, pospace is not infected with 'continuumitis', but the directed interval is. Perhaps what you want is that the directed interval is both a directed object and an interval object, but that may lead to a clash of definitions, so better an amalgam of the two definitions should be sought.

One can try to use a domain theoretic definition of things a bit like the papers such as
_A Domain of spacetime intervals for General relativity_ by Keye Martin and Prakash Panangaden. (see on Prakash's page
http://www.cs.mcgill.ca/~prakash/accepted.html). 
