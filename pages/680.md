#Idea#

The _Dold-Kan correspondence_ asserts that certain [[infinity-category|infinity-categories]] are equivalently encoded as [[chain complex]]es. 

This allows 

* on the one hand to understand the true conceptual home of many constructions with [[chain complex]]es in [[homological algebra]];

* on the other to efficiently compute with certain higher categorical structures.

The classical Dold-Kan correspondence states the equivalence of

$$
  simplicial abelian groups
  \;\;
  \simeq
  \;\;
  non-negatively graded chain complexes of abelian groups
  \,.
$$

Since every simplicial abelian group is a [[Kan complex]], one can equivalently read this more suggestively as 

$$
  \infty-groupoids internal to abelian groups
  \;\;
  \simeq
  \;\;
   chain complexes_+ internal to abelian groups
  \,.
$$

The fact that this involves _abelian_ groups is essential for the correspondence. However, a similar correspondence
still holds in a slightly more nonabelian context:

in a series of articles by Brown and Higgins, based on old work by Whitehead, the above was generalized to

$$
  strict \infty-groupoids
  \;\;
  \simeq
  \;\;
  crossed complexes
$$

See [[strict omega-groupoid]] and [[crossed complex]].
 
Perhaps the 'ultimate' form of a 'classical' Dold-Kan result is by Pilar Carrasco, who identified the extra structure on chain complexes of groups in order that they be [[Moore complex|Moore complexes]] of simplicial groups.  Dominique Bourn has a general form of this result for his [[semi-abelian category|semi-abelian categories]]. His results provide a neat categorical gloss on the theorem.

#Details#

The _Dold-Kan correspondence_ is the name of the [[equivalence of categories|equivalence]] of 

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

This gives a pattern for constructing simplicial structures, often called the _simplicial [[nerve]]_,  from algebraic structures. 

For example the nerve of a groupoid $G$ may be defined as the simplicial set which is $Ob(G)$ in dimension 0 and is given in dimension $n\gt 0$ by 

$$Nerve(G)_n= Gpd(\pi_1(\Delta^n,\Delta^n_0) , G).$$

where $\Delta^n_0$ denotes the set of vertices of $\Delta^n$. 

A [[filtered space]] $X_*$ has a fundamental crossed complex $\Pi X_*$, and a geometric simplex $\Delta^n$ has a filtration $\Delta^n_*$ by skeleta. The nerve of a [[crossed complex]] $C$ is then the simplicial set given in dimension $n$ by 

$$Nerve(C)_n= Crs(\Pi(\Delta^n_*, C).$$

This includes the case when $C$ is a [[crossed module]] (of groupoids) regarded as a crossed complex of length 2. The geometric realisation of this simplicial set gives the [[classifying space]] $BC$ of the crossed complex $C$. This space is filtered by the length of truncations of $C$ to give a filtered space $(BC)_*$ and it is a theorem that $\Pi(BC)_* \cong C$. 


An obvious analogue gives cubical or globular nerves. 

#Remarks#

* There is a whole list of generalizations of this by Brown and Higgins, showing equivalences of various strict infinity-categories [[internal category|internal to]] $Ab$ with $Ch_+(Ab)$. 

*  There is a discussion of some of these and extensions to them to the non-Abelian case, in the entry on [[Moore complex]]
...