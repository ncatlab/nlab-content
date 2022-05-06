
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[mathematics]] typically by default the term "configuration space" of a [[topological space]] $X$ refers to the topological space of pairwise distinct points in $X$, also called _[[Fadell's configuration space]]_, for emphasis.

In principle many other kinds of configurations and the spaces these form may be referred to by "configuration space", notably in [[physics]] the usage is in a broader sense, see at _[[configuration space (physics)]]_.

## Definition

+-- {: .num_defn #ConfigurationSpaceOfParticleswithLabels}
###### Definition
**(configuration space of particles with labels)**

Let $(X, \infty)$ and $(A, 0)$ be [[pointed topological spaces]].

Then the _configuration space of points in $X$ with labels in $A$_

$$
  Conf(X, A)
  \;\coloneqq\;
  \left(
    \underset{ n \in \mathbb{N} }{\coprod} 
    \left( 
      X^n \setminus \mathbf{\Delta}^n_X
    \right)
    \times A^n
  \right)/\sim
$$

is the [[quotient space]] of the [[disjoint union]] of the [[Cartesian products]] of the space of configurations of distinguishable but unlabeled [[n-tuples]] of points, hence the [[complement]] in $X^n$ of the [[fat diagonal]] $\mathbf{\Delta}_X^n$, with the products of label spaces, by the following [[equivalence relations]]:

1. [[action]] of the [[symmetric group]]:

   $$
     \big((x_1, \cdots, x_n), (a_1, \cdots, a_n)\big) 
     \sim 
     \big((x_{\sigma(1)}, \cdots, x_{\sigma(n)}), (a_{\sigma(1)}, \cdots, a_{\sigma(n)})\big) 
   $$

   for any [[permutation]] $\sigma \in S_n$


1. vanishing of particles of "zero charge":

   $$     
     \big((x_1, \cdots, x_{n-1}, x_n), (a_1, \cdots, a_{n-1}, 0)\big) 
     \;\sim\;
     \big((x_1, \cdots, x_{n-1}), (a_1, \cdots, a_{n-1})\big) 
   $$

1. vanishing of particles of "[[vanishing at infinity|at infinity]]":

   $$     
     \big((x_1, \cdots, x_{n-1}, \infty), (a_1, \cdots, a_{n-1}, a_n)\big) 
     \;\sim\;
     \big((x_1, \cdots, x_{n-1}), (a_1, \cdots, a_{n-1})\big) 
   $$


=--

(e.g. [Bödigheimer 87, 1](#Boedigheimer87))


+-- {: .num_example #UnlabeledConfigurationSpace}
###### Example
**(configuration space of unlabeled points)**

For $A = S^0 = \{1\}_+$ the [[0-sphere]] all points in Def. \ref{ConfigurationSpaceOfParticleswithLabels} carry the same label "1", which means that they are actually unlabeled, and we will write just

\[
  \label{ConfigurationSpaceOfUnlabeledPoints}
  Conf(X)
  \;\coloneqq\;
  Conf(X,S^0)
\]

in this case.

=--

A slight variation of the definition is sometimes useful:

+-- {: .num_defn #ConfigurationSpaceOfDisks}
###### Definition
**(configuration space of $dim(X)$-disks)**

In the situation of Def. \ref{ConfigurationSpaceOfParticleswithLabels}, with $X$ a [[manifold]] of [[dimension]] $dim(X) \in \mathbb{N}$

$$
  DiskConf(X,A)
  \longrightarrow
  Conf(X,A)
$$

be, on the left, the labeled configuration space of joint [[embedding of smooth manifolds|embeddings]] of [[tuples]]

$$
  \left(
    D^{dim(X)} 
      \overset{ \iota_i }{\hookrightarrow}
    X
  \right)
$$

of $dim(X)$-dimensional disks/[[closed balls]] into $X$, with identifications as in Def. \ref{ConfigurationSpaceOfParticleswithLabels} (in particular the disks centered at the basepoint are quotiented out) and with the comparison map sending each disk to its center.

This map is evidently a [[deformation retraction]] hence in particular a [[homotopy equivalence]].

=--


## Properties

### Cocycle spaces and the Scanning map
 {#CocycleSpacesAndScanningMap}


(...)


### Classifying space of the symmetric group

Let $X= \mathbb{R}^\infty$. Then 

* the _unordered_ configuration space of $n$ points in $\mathbb{R}^\infty$ is a model for the [[classifying space]] $B \Sigma(n)$ of the [[symmetric group]] $\Sigma(n)$;

  (e.g. [Bödigheimer 87, Example 10](#Boedigheimer87))


* the _ordered_ configuration space of $n$ points, equipped with the canonical $\Sigma(n)$-[[action]], is a model for the $\Sigma(n)$-[[universal principal bundle]].



### James construction

The [[James construction]] of $X$ is [[homotopy equivalence|homotopy equivalent]] to the [[configuration space (mathematics)|configuration space]] $C(\mathbb{R}^1, X)$ of points in the [[real line]] with "[[charges]]" taking values in $X$.

(e.g. [Bödigheimer 87, Example 9](#Boedigheimer87))


## References

### General 

General survey includes

* [[Craig Westerland]], _Configuration spaces in geometry and topology_, 2011 ([pdf](https://www.austms.org.au/Publ/Gazette/2011/Nov11/TechPaperWesterland.pdf))

* [[Ben Knudsen]], _Configuration spaces in algebraic topology_ ([arXiv:1803.11165](https://arxiv.org/abs/1803.11165))

See also

* Edward Fadell, Lee Neuwirth, _Configuration spaces_
Math. Scand. __10__ (1962) 111-118, [MR141126](http://www.ams.org/mathscinet-getitem?mr=141126), [pdf](http://www.mscand.dk/article.php?id=1623)


* Edward R. Fadell, Sufian Y. Husseini, _Geometry and topology of configuration spaces_, Springer Monographs in Mathematics (2001), [MR2002k:55038](http://www.ams.org/mathscinet-getitem?mr=2002k:55038), xvi+313 pp.

* F. R. Cohen, [[Sam Gitler|S. Gitler]], _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013)


* [[Sadok Kallel]], Ines Saihi, _Homotopy Groups of Diagonal Complements_, Algebr. Geom. Topol. 16 (2016) 2949-2980 ([arXiv:1306.6272](https://arxiv.org/abs/1306.6272))





### Scanning map and cohomotopy

The [[scanning map]] and hence the relation of configuration spaces to [[cohomotopy]] goes back to 

* {#May72} [[Peter May]], _The geometry of iterated loop spaces_, Springer 1972

* {#Segal73} [[Graeme Segal]], _Configuration-spaces and iterated loop-spaces_, Invent. Math. __21__ (1973), 213&#8211;221. MR 0331377 ([pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf))

Generalization of these constructions and results is due to

* {#McDuff75} [[Dusa McDuff]], _Configuration spaces of positive and negative particles_, Topology Volume 14, Issue 1, March 1975, Pages 91-107 (<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>)

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf))

and generalization to [[equivariant cohomology]] is discussed in

* Colin Rourke, Brian Sanderson, _Equivariant Configuration Spaces_, 62(2), October 2000, pp. 544-552 ([pdf](http://wrap.warwick.ac.uk/828/1/WRAP_Rourke_Equivariant_configuration.pdf))


Reviews include


* {#FrancisLect17} [[John Francis]], _The H-Principle Lecture 17: The sheaf of configuration spaces and the scanning map_ ([pdf](http://math.northwestern.edu/~jnkf/classes/hprin/17configmapping.pdf))

* {#FrancisLect18} [[John Francis]], _The H-Principle Lecture 18: The proof of McDuff's theorem First part_ ([pdf](http://math.northwestern.edu/~jnkf/classes/hprin/18mcduff1.pdf))




See also

* [[Sadok Kallel]], _Particle Spaces on Manifolds and Generalized Poincaré Dualities_ ([arXiv:math/9810067](https://arxiv.org/abs/math/9810067)) 

* [[Shingo Okuyama]], [[Kazuhisa Shimakawa]], _Interactions of strings and equivariant homology theories_, ([arXiv:0903.4667](https://arxiv.org/abs/0903.4667))


### In Goodwillie-calculus
 {#ReferencesInGoodwillieCalculus}

The configuration spaces of a space $X$ appear as the [[Goodwillie derivatives]] of its [[mapping space]]/[[nonabelian cohomology]]-[[functor]] $Maps(X,-)$:


* {#Arone99} [[Greg Arone]], _A generalization of Snaith-type filtration_, Transactions of the American Mathematical Society 351.3 (1999): 1123-1150. ([pdf](https://www.ams.org/journals/tran/1999-351-03/S0002-9947-99-02405-8/S0002-9947-99-02405-8.pdf))

* {#Ching05} [[Michael Ching]], _Calculus of Functors and Configuration Spaces_, Conference on Pure and Applied Topology Isle of Skye, Scotland, 21-25 June, 2005 ([pdf](https://www3.amherst.edu/~mching/Work/skye.pdf))

### Relation to graph complexes

Models for the [[ordinary cohomology]] of configuration in terms of [[graph complexes]] are discussed in

* {#CamposWillwacher16} [[Ricardo Campos]], [[Thomas Willwacher]], _A model for configuration spaces of points_ ([arXiv:1604.02043](https://arxiv.org/abs/1604.02043))


[[!redirects scanning map]]
[[!redirects scanning maps]]

[[!redirects scanning map equivalence]]
[[!redirects scanning map equivalences]]

