##Idea

The most usual method of [[subdivision]] for a [[simplicial complex]] as used in
elementary algebraic and geometric topology is the barycentric [[subdivision]].
There is however another very well structured subdivision construction
encountered which can be useful.  The basic geometric construction involves
chopping up a geometric $n$-simplex by $n$-planes parallel to a  face and halfway
between that face and the opposite vertex.  

##Categorical descriptions

We first define the ordinal subdivision on the simplices, $\Delta[n]$.  (Here $\oplus$ denotes the [[ordinal sum]]

The *ordinal subdivision* of $\Delta[n]$, the
standard $n$-simplex in simplicial sets, is denoted by
$Sd(\Delta[n])$, and is defined as follows:- 

$ Sd(\Delta[n]) := \int^{p,q} \Delta([p]\oplus[q],[n]) \cdot (\Delta[p] \times \Delta[q]). $

For a general simplicial set we can then define:

the _ordinal subdivision_ of a simplicial set, $X$, is
denoted by $Sd(X)$ and is defined by 

$$Sd(X) := \int^{n} X_n \cdot Sd(\Delta [n]). $$
This expands to 

$$ Sd(X) := \int^{n} X_n \cdot \left(\int^{p,q} \Delta([p]\oplus[q],[n])
\cdot (\Delta[p] \times \Delta[q]) \right).$$

This is related to the [total d&#233;calage](http://ncatlab.org/nlab/show/bisimplicial+set#TotalSimplicialSets) of $X$ by

$$ Sd(X) = 
 \cong \int^{p,q} DEC(X)_{p,q} \cdot (\Delta[p] \times
\Delta[q]).$$

##References

* [[Phil Ehlers|P. J. Ehlers]] and [[Tim Porter]], _Ordinal subdivision and special pasting in quasicategories_, Advances in Math. 217 (2007), No 2. pp 489-518.Delta