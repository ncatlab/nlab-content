
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}


## Definition

+-- {: .num_defn #FredholmOperator}
###### Definition 

A [[continuous function|continuous]] [[linear operator]] $F \colon B_1\to B_2$ between [[Banach spaces]] is **Fredholm** if it has [[finite set|finite]] [[dimension|dimensional]] [[kernel]] and finite dimensional [[cokernel]]. 

=--

+-- {: .num_defn }
###### Definition 

The difference between the dimensions of the kernel and the cokernel of a Fredholm operator $F$ is called its **index** 

$$
  ind F \coloneqq dim ker F - dim coker F = dim ker F - codim im F
  \,.
$$

=--

A standard equivalent characterization of Fredholm operators is the following:

+-- {: .num_defn #Parametrix}
###### Definition 

A **parametrix** of a [[bounded operator|bounded]] [[linear operator]] $F \colon \mathcal{H}_1 \to \mathcal{H}_2$ is a reverse operator $P \colon \mathcal{H}_2 \to \mathcal{H}_1$ which is an "[[inverse]] up to [[compact operators]]", i.e. such that $F \circ P - id_{\mathcal{H}_2}$ and $P \circ F - id_{\mathcal{H}_1}$ are both [[compact operators]].

=--


+-- {: .num_prop }
###### Proposition

A [[bounded operator|bounded]] [[linear operator]] $ F \colon B_1\to B_2$ between [[Banach spaces]] is Fredholm, def. \ref{FredholmOperator} precisely it is has a parametrix, def. \ref{Parametrix}.

=--

## Examples

* [[elliptic operator|Elliptic operators]] on [[compact topological space|compact]] [[manifolds]] are naturally Fredholm, when understood between the appropriate [[Sobolev spaces]].


## Properties

+-- {: .num_prop }
###### Proposition

The [[image]] (range) of a Fredholm operator is closed. 

=--

+-- {: .num_prop }
###### Proposition

The subspace $Fred(B_1,B_2)\subset B(B_1,B_2)$ of Fredholm operators in the space of bounded linear operators with the norm topology is open. 

=--

  In other words, given a Fredholm operator $F$, there exists $\epsilon\gt 0$ such that every bounded linear operator $G$ satisfying $\| G-F\|\lt \epsilon$ is Fredholm. Fredholm operators on a fixed separable Hilbert space $H = B_1 = B_2$ form a [[semigroup]] with respect to the composition and the index is a morphism of semigroups: $ind F G = ind F + ind G$. 

+-- {: .num_prop }
###### Proposition

The space $Fred$ of all Fredholm operators on an (infinite dimensional) [[separable Hilbert space]] is a model for the [[classifying space]] of degree-0 [[topological K-theory]].

=--

(...)

## Generalizations

Fredholm operators generalize to Fredholm complexes. A finite [[chain complex]]

$$
0 \to C_0 \stackrel{d_0}\to C_1\stackrel{d_1}\to C_2 \ldots C_n\to 0
$$

of [[Banach space]]s and bounded operators is said to be a **Fredholm complex** if the images $d_i$ are closed and the [[chain homology]] of the complex is finite dimensional. The [[Euler characteristic]] (the alternative sum of the dimensions of the homology groups) is then called the __index__ of the Fredholm complex. Each Fredholm operator can be considered as a Fredholm complex concentrated at zero. Each Fredholm complex produces a Fredholm operator from the sum of the even- to the sum of the odd-numbered spaces in the complex. 

One can consider *Fredholm almost complexes*, where $d_i \circ d_{i-1}$ is not zero but the image of that operator is compact. Out of every Fredholm almost complex one can make a complex by correcting the differentials by compact perturbation terms. [[elliptic complex|Elliptic complexes]] give examples of Fredholm complexes. 

## Related concepts



* [[Fredholm module]], 

* [[Fredholm determinant]], 

* [[Dirac operator]], 

* [[Toeplitz operator]]

* [[K-theory]], [[KK-theory]]

* [[index theory]] 


## References


* [wikipedia:Fredholm operator](http://en.wikipedia.org/wiki/Fredholm_operator)

* A. S. Mishchenko, &#1042;&#1077;&#1082;&#1090;&#1086;&#1088;&#1085;&#1099;&#1077; &#1088;&#1072;&#1089;&#1089;&#1083;&#1086;&#1077;&#1085;&#1080;&#1103; &#1080; &#1080;&#1093; &#1087;&#1088;&#1080;&#1084;&#1077;&#1085;&#1077;&#1085;&#1080;&#1103; (Vector bundles and their applications), Nauka, Moscow, 1984. 208 pp. MR87f:55010  

* S. Rempel, B-W. Schulze, _Index theory of elliptic boundary problems_, Akademie--Verlag, Berlin, 1982.

* [[Lars Hörmander]], _The analysis of linear partial differential operators. III. Pseudo-differential operators_, 1994, reprinted 2007. 

* Pietro Aiena, _Fredholm and local spectral theory, with applications to multipliers_, [book page](http://www.springer.com/mathematics/analysis/book/978-1-4020-1830-5)

* [[Otgonbayar Uuye]], _A simple proof of the Fredholm Alternative_, [arxiv/1011.2933](http://arxiv.org/abs/1011.2933)

* [[Alexander Grothendieck]], _La th&#233;orie de Fredholm_, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __84__ (1956), p. 319-384, [numdam](http://www.numdam.org/item?id=BSMF_1956__84__319_0) 

category: analysis
[[!redirects Fredholm complex]]
[[!redirects Fredholm operators]]

[[!redirects parametrix]]

