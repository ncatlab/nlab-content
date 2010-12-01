
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

A _factorization algebra_ is an [[algebra over an operad]] where the [[operad]] in question is like the [[little disk operad]], but with each disk embedded into a given [[manifold]] $X$.

This way a factorization algebra is an assignment of a [[chain complex]] $V_D$ to each [[ball]] $D \subset X$ embedded in $X$, and for each collection of non-intersecting embedded balls $D_1 , \cdots, D_n \subset D \subset X$ sitting inside a bigger embedded ball $D$ in $X$ a morphism

$$
  V_{D_1} \otimes V_{D_2} \otimes \cdots \otimes V_{D_n} \to V_{D}
$$

such that composition of such operations is suitably respected.

## Definition

### Prefactorization algebra

+-- {: .un_defn}
###### Definition


For $X$ a [[topological space]] write $Fact_X$ be the colored [[operad]] in [[Set]] whose

* [[object]]s are the [[connected]] [[open subset]]s of $X$;

* the [[hom-set]] $Fact_X(\{U_i\}_i, V)$ is the singleton precisely if the
  $U_i$ are all in $V$ and are pairwise disjoint and is the [[empty set]] otherwise.

This specifies composition uniquely. 

=--

+-- {: .un_defn #PrefactorizationAlgebra}
###### Definition


For $(C, \otimes)$ a [[symmetric monoidal category|symmetric monoidal]] [[abelian category]] let $End(C)$ be its [[endomorphism operad]]. A **prefactroization algebra** on $X$ with values in $C$ is an [[algebra over an operad]] over $Fact_X$ in $C$, hence a morphism of operads

$$
  \mathcal{F} : Fact_X \to End(C)
  \,.
$$

=--

These definitions appear ([here](http://math.northwestern.edu/~costello/factorization_public.html#[[Prefactorization%20algebras]])).

### Factorization algebras

+-- {: .un_defn #FactorizingCover}
###### Definition

For $X$ a [[topological space]] and $U \subset X$ an [[open subset]], a [[open cover]] $\{U_i \hookrightarrow U\}_{i \in I}$ is called a **factorizing cover** if for every [[finite set]] of points $\{x_1, \cdots, x_k\} \subste U$ there is a finite subset $\{U_{i_j}\}_{j \in J \subset I} $ of pairwise disjoint open subsets such that each point is contained in ther union.

=--


+-- {: .un_remark}
###### Remark


Every [[Hausdorff space]] admits a factorizing cover.

=--

+-- {: .un_def}
###### Notation


For a factorizing cover $\{U_i \to U\}_{i \in I}$ write $P I$ for the set of finite subsets $\alpha \subset I$ such that for $j,j' \in \alpha$ we have $U_j \cap U_{j'} = \epmtyset$. 

Given a [prefactorization algebra](#PrefactorizationAlgebra) $\mathcal{F}$ and $\alpga \in P I$ write 

$$
  \mathcal{F}(\alpha) := \otimes_{j \in \alpha} F(U_j)
$$

and for $\alpha_1, \cdots, \alpha_k \in P I$ write

$$
  \mathcal{F}(\alpha_1, \cdots, \alpha_k) = 
    \bigotimes_{(j_1, \cdots, j_k) \in \alpha_1 \times \cdots \times \alpha_k}
    \mathcal{F}(U_{j_1} \cap \cdots \cap U_{j_k})
  \,.
$$

For each $1 \leq i \leq k$ there is a canonical morphism

$$  
  p_i : \mathcal{F}(\alpha_1,\cdots, \alpha_k)
  \to 
   \mathcal{F}(\alpha_1, \cdots, \alpha_{i-1}, \alpha_{i+1}, \cdots, \alpha_k)
  \,.
$$

=--

+-- {: .un_def}
###### Definition

A prefactorization algebra $\mathcal{F} : Fact_X \to End(C)$ is called a **factorization algebra** if for every open subset $U \subset X$ and every [factorizing cover](#FactorizingCover) $\{U_i \to U\}_{i \in I}$ the sequence 


$$
  \bigoplus_{\alpha_1, \alpha_2 \in P I}
   \mathcal{F}(\alpha_1, \alpha_2)
  \stackrel{p_1 - p_2}{\to}
    \bigoplus_{\beta \in P I}
   \mathcal{F}(\beta)
   \to 
   \mathcal{F}(U)
   \to 0
$$

is an [[exact sequence]].

=--

These definitions appear [here](http://math.northwestern.edu/~costello/factorization_public.html#[[Factorization%20algebra]]).

### Homotopy factorization algebras

Let now $(C,\otimes)$ specifically be a [[category of chain complexes]].

+-- {: .un_def}
###### Definition

A  [prefactorization algebra]{#PrefactorizationAlgebra} $\mathcal{F} : Fact_X \to End(X)$ is a **homotopy factorization algebra** if for all factorizing covers $\{U_i \to U \subset X\}_{i \in I}$ the canonical morpshim

$$
  \bigoplus_{k \geq 0} \bigoplus_{\alpha_1, \cdots, \alpha_k \in P I}
   \mathcal{F}(\alpha_1, \cdots, \alpha_k)[k-1]
   \to 
  \mathcal{F}(U)
$$

is a [[quasi-isomorphism]], where the [[differential]] on the left is defined by (...).

=--

+-- {: .un_remark}
###### Remark

This is the analogue of a [[descent]] condition for [[simplicial presheaves]].

=--

These definitions appear [here](http://math.northwestern.edu/~costello/factorization_public.html#[[Factorization%20algebra]]).


## Related concepts

Factorization algebras have some similarity with 

* [[Hochschild homology]];

* [[blob homology]];

* [[local net]]s in [[AQFT]].


## References

This may be regarded as a slight variation on the concept _chiral algebra_ originally introduced by Beilinson and Drinfeld.

A definition appears in section 4.1 _Topological Chiral Homology_ of

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

There it is demonstrated how factorization algebras can be used to construct extended [[FQFT]]s.

Concrete constructions of formal algebras for familiar [[quantum field theory|quantum field theories]] are described in 

* [[Kevin Costello]] (with [[Owen Gwilliam]]), _Factorizaton algebras in perturbative quantum field theory_ in [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Strings, Field, Topology]], Oberwolfach report No 28, 2009 ([pdf](http://www.mfo.de/programme/schedule/2009/24/OWR_2009_28.pdf#page=12))

This can also be found mentioned in the talk notes of the [[Northwestern TFT Conference 2009]], see in particular

* notes by  [[Christoph Wockel]], [[costello.pdf:file]]

* notes by Evan Jenkins on the same talk: [Factorization algebras in perturbative quantum gravity](http://www.math.uchicago.edu/~ejenkins/notes/nwtft/25may-kc.pdf)

More is at

* [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in perturbative quantum field theory_ ([wiki](http://math.northwestern.edu/~costello/factorization_public.html))

There seems to be a close relation between the description of [[quantum field theory]] by factorization algebras and the proposal presented in 

* Stefan Hollands ([arXiv](http://arxiv.org/abs/0802.2198))

[[!redirects factorization algebras]]