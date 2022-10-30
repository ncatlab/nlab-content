#Idea#

The _Dold-Kan correspondence_ asserts that certain [[infinity-category|infinity-categories]] are equivalently encoded as [[chain complex]]es. 

This allows 

* on the one hand to understand the true conceptual home of many constructions with [[chain complex]]es in [[homological algebra]];

* on the other to efficiently compute with certain higher categorical structures.

Compare this to the role played by [[rational homotopy theory]].

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

Here on the left we have [[strict omega-groupoid]]s
and on the right [[crossed complex]]es, a non-abelian generalization of chain complexes of groups.

$$
  crossed complexes \supset
  chain complexes_+ internal of abelian groups
$$
 
Perhaps the 'ultimate' form of a 'classical' Dold-Kan result is by Pilar Carrasco, who identified the extra structure on chain complexes of groups in order that they be [[Moore complex|Moore complexes]] of simplicial groups.  Dominique Bourn has a general form of this result for his [[semi-abelian category|semi-abelian categories]]. His results provide a neat categorical gloss on the theorem.

Dominique Bourn's formulation is very pretty. The Moore complex functor is monadic when the basic category is semi-Abelian (Th. 1.4. p.113 in _Bourn2007_ below). Of course for simplicial _groups_, the  monad on chain complexes of groups gives the hypercrossed complexes of Carrasco and Cegarra, but here they fall out from the theory.  On the down side there is apparently no 
full analysis as yet of the actual form of this monad.


## parameterized version of the Dold-Kan correspondence ##

The statement of the Dold-Kan correspondence generalizes to
[[sheaf|sheaves]] with values in the respective categories and this way from [[Infinity-Grpd]] to more general [[(infinity,1)-topos|(infinity,1)-topoi]]:

for $X$ be a [[site]] let $Sh(X, sAb)$ be the category of 
_simplicial abelian sheaves_ -- i.e. 
[[simplicial presheaf|simplicial sheaves]] which take values
in simplicial abelian groups -- and let $Sh(X, Ch_+(Ab))$
be the category of [[sheaf|sheaves]] on $S$ with values in
non-negatively graded [[chain complex]]es of abelian groups.
The normalized chain complex extends objectwise to a functor
$$
  Sh(X,sAb) \stackrel{\simeq}{\to} Sh(X, Ch_+(Ab))
$$
which is an [[equivalence]] of categories. Moreover, 
both these categories are naturally 
[[category with weak equivalences|categories with weak equivalences]]:
the weak equivalences in $Sh(X, sAb)$ are the stalkwise
[[model structure on simplicial sets|weak equivalences of simplicial sets]]
and the weak equivalences in $Sh(X, Ch_+(Ab))$ are the
[[quasi-isomorphism]]s. The normalized chain complex functor
preserves these weak equivalences.
This sheaf version of the Dold-Kan correspondence 
allows to understand [[abelian sheaf cohomology]]
as a special case of [[nonabelian cohomology]] and
[[generalized sheaf cohomology]].

See page 9,10 of 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]




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


#References#

The relation between [[strict omega-groupoid]]s and [[crossed complex]]es is in

* R. Brown, P. Higgins, _The equivalence of $\infty$-groupoids and crossed complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 371-386  ([pdf](http://archive.numdam.org/article/CTGDC_1981__22_4_371_0.pdf))

The discussion of Dold-Kan in the generalized context of [[semi-abelian category|semi-abelian categories]] is in

* **Bourn2007** D. Bourn, _Moore normalisation and Dold-Kan theorem for semi-Abelian categories_, in 
Categories in algebra, geometry and mathematical physics , volume 431 of Contemp. Math., 
105 &#8211; 124, Amer. Math. Soc., Providence, RI. (2007)
