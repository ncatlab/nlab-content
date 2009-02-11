The _Dold-Kan correspondence_ is the name of the [[equivalence]] of 

* the category [[SimpAb]] of [[simplicial set|simplicial]] abelian groups;

and

* the category $Ch_+(Ab)$ of non-negatively graded chain complexes of abelian groups.

There is an adjoint equivalence

$$
  N : \Simp\Ab \stackrel{\leftarrow}{\to} Ch_+(Ab) : \Xi
$$

where $N$ is the normalized chains functor, also called the [[Moore complex]].

A nice expression of the functor $\Xi$ (this was the light Kan shed on the work of Dold!) is that

 $$\Xi(C)_n= Chn(C_*(\Delta^n), C)$$

 where $C_*(\Delta^n)$ is the normalised chains of the simplicial set $\Delta^n$, and $Chn$ denotes the abelian group of chain mappings. 

This gives a pattern for constructing simplicial structures, often called the _simplicial [[nerve]]_,  from algebraic structures. An obvious analogue gives cubical nerves. 

#Remarks#

* There is a whole list of generalizations of this by Brown and Higgins, showing equivalences of various strict infinity-categories [[internal category|internal to]] $Ab$ with $Ch_+(Ab)$. 

*  There is a discussion of some of these and extensions to them to the non-Abelian case, in the entry on [[Moore complex]]
...