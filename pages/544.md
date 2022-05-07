
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

An _$A_\infty$-algebra_ is a [[monoid]] internal to a [[homotopical category]] such that the [[associativity]] law holds not as an equation, but only up to higher [[coherent]] [[homotopy]].

## Definition


+-- {: .num_defn}
###### Definition

An **$A_\infty$-algebra** is an [[algebra over an operad]] over an [[A-∞ operad]].

=--

## Realizations


### In chain complexes

Let here $\mathcal{E}$ be the [[category of chain complexes]] 
$\mathcal{Ch}_\bullet$. Notice that often in the literature this choice of $\mathcal{E}$ is regarded as default and silently assumed.

An $A_\infty$-algebra in chain complexes is concretely the following data. 

A chain $A_\infty$-algebra is the structure of a degree 1 [[coderivation]] 

$$
  D : T^c V \to T^c V
$$

on the reduced tensor coalgebra $T^c V = \oplus_{n\geq 1} V^{\otimes n}$ (with the standard noncocommutative coproduct, see [[differential graded Hopf algebra]]) over a [[graded vector space]] $V$ such that 
$$
  D^2 = 0
  \,.
$$

Coderivations on free coalgebras are entirely determined by their "value on cogenerators", which allows one to decompose $D$ as a sum:

$$
  D = D_1 + D_2 + D_3 + \cdots
$$

with each $D_k$ specified entirely by its action

$$
  D_k : V^{\otimes k} \to V
  \,.
$$
which is a map of degree $2-k$ (or can be alternatively understood as a map $D_k : (V[1])^{\otimes k}\to V[1]$ of degree $1$). 

Then:

* $D_1 : V\to V$ is the _differential_ with $D_1^2 = 0$;

* $D_2 : V^{\otimes 2} \to V$ is the _product_ in the algebra;

* $D_3 : V^{\otimes 3} \to V$ is the _associator_ which measures the failure of $D_2$ to be associative;

* $D_4 : V^{\otimes 4} \to V$ is the _pentagonator_ (or so) which measures the failure of $D_3$ to satisfy the pentagon identity;

* and so on.

One can also allow $D_0$, in which case one talks about weak $A_\infty$-algebras, which are less understood.

There is a resolution of the operad $\mathrm{Ass}$ of associative algebras (as operad on the category of chain complexes) which is called the $A_\infty$-operad; the algebras over the $A_\infty$-[[A-infinity operad|operad]] are precisely the $A_\infty$-algebras. 

A **morphism of $A_\infty$-algebras** $f : A\to B$ is a collection $\lbrace f_n\rbrace_{n\geq 1}$ of maps 
$$
f_n : (A[1])^{\otimes n}\to B[1]
$$
of degree $0$ satisfying
$$
\sum_{0\leq i+j\leq n} f_{i+j+1}\circ(1^{\otimes i}\otimes D_{n-i-j}\otimes 1^{\otimes j})
= \sum_{i_1+\ldots+i_r=n} D_r\circ (f_{i_1}\otimes\ldots f_{i_r}).
$$
For example, $f_1\circ D_1 = D_1\circ f_1$.



#### Rectification

+-- {: .num_theorem }
###### Theorem
**(Kadeishvili (1980), Merkulov (1999))**

If $A$ is a [[dg-algebra]], regarded as a strictly associative $A_\infty$-algebra, its [[chain homology and cohomology|chain cohomology]] $H^\bullet(A)$, regarded as a [[chain complex]] with trivial differentials, naturally carries the structure of an $A_\infty$-algebra, unique up to isomorphism, and is weakly equivalent to $A$ as an $A_\infty$-algebra.

=--

More details are at _[[Kadeishvili's theorem]]_.
  


+-- {: .num_remark }
###### Remark

This theorem provides a large supply of examples of $A_\infty$-algebras: there is a natural $A_\infty$-algebra structure on all cohomologies such as

* [[de Rham cohomology]]

* [[Hochschild cohomology]]

etc.

=--

### In Topological space

An $A_\infty$-algebra in [[Top]] is also called an _[[A-∞ space]]_ .

#### Examples

Every [[loop space]] is canonically an [[A-∞ space]]. (See there for details.)

#### Rectification

+-- {: .num_theorem }
###### Theorem

Every $A_\infty$-space is [[weak homotopy equivalence|weakly homotopy equivalent]] to a topological [[monoid]].

=--

This is a classical result by ([Stasheff 1963](#Stasheff63), [BoardmanVogt](#BoardmanVogt)). It follows also as a special case of the more general result on rectification in a [[model structure on algebras over an operad]] (see there). 

### In spectra

See [[ring spectrum]] and [[algebra spectrum]].


## Related concepts

* **$A_\infty$-algebra**, [[A-∞-category]]

  * [[augmented A-∞ algebra]]

  * [[curved A-∞ algebra]]

* [[A-n algebra]]

* [[E-∞ algebra]]

* [[L-∞ algebra]], .

[[!include k-monoidal table]]

[[!include deformation quantization - table]]


## References

A survey of $A_\infty$-algebras in chain complexes is in

* [[Bernhard Keller]], _A brief introduction to $A_\infty$-algebras_ ([pdf](http://people.math.jussieu.fr/~keller/publ/IntroAinfEdinb.pdf))

Classical articles on $A_\infty$-algebra in topological spaces are 

* {#Stasheff63} [[Jim Stasheff]], *Homotopy associativity of H-spaces I*, Trans. Amer. Math. Soc. 108 (1963), p. 275-292 ([doi:10.1090/S0002-9947-1963-0158400-5](https://doi.org/10.1090/S0002-9947-1963-0158400-5))

* [[Michael Boardman]] and [[Rainer Vogt]], _Homotopy invariant algebraic structures on topological spaces_ , Lect. Notes Math. 347 (1973).
{#BoardmanVogt}

A brief survey is in section 1.8 of

* [[Martin Markl]], Steve Shnider, [[Jim Stasheff|James D. Stasheff]], _Operads in algebra, topology and physics_, Math. Surveys and Monographs __96__, Amer. Math. Soc. 2002.


The 1986 thesis of [[Alain Prouté]] explores the possibility of obtaining analogues of [[minimal model]]s for $A_\infty$ algebras. It was published in TAC much later.

* [[Alain Prouté]], _Alg&#232;bres diff&#233;rentielles fortement homotopiquement associatives ($A_\infty$-alg&#232;bres)_, thesis, available as [Reprints in Theory and Applications of Categories, No. 21, 2011, pp. 1&#8211;99](http://www.logique.jussieu.fr/~alp/these_A_Proute-TAC.pdf)

[[!redirects A-infinity-algebras]]
[[!redirects A-infinity algebra]]
[[!redirects A-infinity algebras]]
[[!redirects A-∞ algebra]]
[[!redirects A-∞ algebras]]
[[!redirects A? algebra]]
[[!redirects A? algebras]]
[[!redirects A-∞-algebra]]

[[!redirects A-∞-algebras]]


