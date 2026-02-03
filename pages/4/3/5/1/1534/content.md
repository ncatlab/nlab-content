
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

In Euclidean ([[Wick rotation|Wick rotated]]) [[field theory]] factorization algebras serve to axiomatize the [[operator product expansion]].

## Definition

### Prefactorization algebra

+-- {: .num_defn}
###### Definition


For $X$ a [[topological space]] write $Fact_X$ be the colored [[operad]] in [[Set]] whose

* [[object]]s are the [[connected]] [[open subset]]s of $X$;

* the [[hom-set]] $Fact_X(\{U_i\}_i, V)$ is the singleton precisely if the
  $U_i$ are all in $V$ and are pairwise disjoint and is the [[empty set]] otherwise.

This specifies composition uniquely. 

=--

+-- {: .num_defn #PrefactorizationAlgebra}
###### Definition


For $(C, \otimes)$ a [[symmetric monoidal category|symmetric monoidal]] [[abelian category]] and $A \in C$ an [[object]], let $End(A)$ be its [[endomorphism operad]]. A **prefactorization algebra** on $X$ with values in $A$ is an [[algebra over an operad]] over $Fact_X$ in $C$, hence a morphism of operads

$$
  \mathcal{F} \colon Fact_X \to End(A)
  \,.
$$

=--

These definitions appear in [Costello & Gwilliam](#CostelloGwilliam).


### Factorization algebras

+-- {: .num_defn #FactorizingCover}
###### Definition

For $X$ a [[topological space]] and $U \subset X$ an [[open subset]], a [[open cover]] $\{U_i \hookrightarrow U\}_{i \in I}$ is called a **factorizing cover** if for every [[finite set]] of points $\{x_1, \cdots, x_k\} \subset U$ there is a finite subset $\{U_{i_j}\}_{j \in J \subset I} $ of pairwise disjoint open subsets such that each point is contained in their union.

=-- 


+-- {: .num_remark}
###### Remark


Every [[Hausdorff space]] admits a factorizing cover.

=--

+-- {: .num_defn}
###### Notation


For a factorizing cover $\{U_i \to U\}_{i \in I}$ write $P I$ for the set of finite subsets $\alpha \subset I$ such that for $j,j' \in \alpha$ we have $U_j \cap U_{j'} = \emptyset$. 

Given a [prefactorization algebra](#PrefactorizationAlgebra) $\mathcal{F}$ and $\alpha \in P I$ write 

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

+-- {: .num_defn}
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

These definitions appear [here](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.382.8322&rep=rep1&type=pdf).

See also at _[[cosheaf]]_.

### Homotopy factorization algebras

Let now $(C,\otimes)$ specifically be a [[category of chain complexes]].

+-- {: .num_defn}
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

+-- {: .num_remark}
###### Remark

This is the analogue of a [[descent]] condition for [[simplicial presheaves]].

=--

These definitions appear [here](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.382.8322&rep=rep1&type=pdf).

## Examples

* [[beta-gamma system]]

## Related concepts

Factorization algebras have some similarity with 

* [[Hochschild homology]];

* [[blob homology]], [[factorization homology]], [[topological chiral homology]];

* [[local net]]s in [[AQFT]].

* [[chiral algebra]], [[vertex operator algebra]]

* [[nonabelian Poincaré duality]]
  

[[!include Isbell duality - table]]


## References

* {#CostelloGwilliam} [[Kevin Costello]], [[Owen Gwilliam]]: *Factorization algebras in quantum field theory* &lbrack;[[CostelloGwilliam-FactorizationAlgebras.pdf:file]]&rbrack;

The notion of factorization algebra may be regarded as a slight variation on the concept _[[chiral algebra]]_ originally introduced in

* [[Alexander Beilinson]], [[Vladimir Drinfeld]]:  _[[Chiral Algebras]]_.

A definition formulated genuinely in  [[Higher Algebra]] appears in section 4.1 _Topological Chiral Homology_ of

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

This discusses how locally constant factorization algebras obtained from [[En-algebras]] induce [[extended quantum field theory|extended]] [[FQFTs]].

A fairly comprehensive account of factorization algebras as a formalization of [[perturbation theory|perturbative]] [[quantum field theory]] (see at _[[factorization algebra of observables]]_) is in 

* [[Kevin Costello]], [[Owen Gwilliam]], _[[Factorization algebras in perturbative quantum field theory]]_ 

* [[Owen Gwilliam]], _Factorization algebras and free field theories_ PhD thesis ([[GwilliamThesis.pdf:file]])

* [[Owen Gwilliam]], [[Kasia Rejzner]], _Comparing nets and factorization algebras of observables: the free scalar field_, [arxiv:1711.06674](https://arxiv.org/abs/1711.06674)


and the beginnings of

* {#Costello11} [[Kevin Costello]], *Notes on supersymmetric and holomorphic field theories in dimension 2 and 4*, talk at *[Geometric and Algebraic Structures in Mathematics](https://www.math.stonybrook.edu/dennisfest/)*, Stony Brook (2011) &lbrack;[arXiv:1111.4234](https://arxiv.org/abs/1111.4234)&rbrack;

* [[Kevin Costello]], [[Claudia Scheimbauer]], _Lectures on mathematical aspects of (twisted) supersymmetric gauge theories_, pp. 57-88 in: Mathematical aspects of QFTs, D. Calaque, T. Strobl editors, Springer 2015

Lecture notes:

* [[Kevin Costello]] (with [[Owen Gwilliam]]), _Factorization algebras in perturbative quantum field theory_ in [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Strings, Field, Topology]], Oberwolfach report No 28, 2009 ([pdf](http://www.mfo.de/programme/schedule/2009/24/OWR_2009_28.pdf#page=12))

  This can also be found mentioned in the talk notes of the [[Northwestern TFT Conference 2009]], see in particular

  * notes by  [[Christoph Wockel]], [[costello.pdf:file]]

  * notes by Evan Jenkins on the same talk: [Factorization algebras in perturbative quantum gravity](http://www.math.uchicago.edu/~ejenkins/notes/nwtft/25may-kc.pdf)

* [[Araminta Amabel]], *Notes on Factorization Algebras and TQFTs* &lbrack;[arXiv:2307.01306](https://arxiv.org/abs/2307.01306)&rbrack;

  > (with relation to [[functorial field theory]])

Further review:

* [[Kevin Costello]], [[Owen Gwilliam]], *Factorization algebra*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2310.06137](https://arxiv.org/abs/2310.06137)&rbrack;


There seems to be a close relation between the description of [[quantum field theory]] by factorization algebras and the proposal presented in 

* [[Stefan Hollands]], ([arXiv:0802.2198](http://arxiv.org/abs/0802.2198))

The relation of locally constant factorization algebras to higher order [[Hochschild homology]] is in 

* [[Gregory Ginot]], [[Thomas Tradler]], [[Mahmoud Zeinalian]], _Derived higher Hochschild homology, topological chiral homology and factorization algebras_, [arxiv/1011.6483](http://arxiv.org/abs/1011.6483)

* [[Gregory Ginot]], _Notes on factorization algebras, factorization homology and applications_, [arxiv/1307.5213](https://arxiv.org/abs/1307.5213)

A comparison with FQFT for TFTs is presented in

* C. Scheimbauer, _A factorization view on states/observables in topological field theories_ [youtube](https://www.youtube.com/watch?v=nN-qtnbtpW4) 19 min, string-math 2017, Hamburg

An [[(infinity,1)-category theory|(infinity,1)-category theoretic ]] treatment of higher factorization algebras is in 

* [[Dennis Gaitsgory]], [[John Francis]] _Chiral Koszul duality_ ([arXiv:1103.5803](http://arxiv.org/abs/1103.5803))
 {#GaitsgoryFrancis}

A construction of [[chiral differential operator]]s via quantization of $\beta\gamma$ system in [[BV formalism]] with an intermediate step using factorization algebras:

* Vassily Gorbounov, Owen Gwilliami, Brian Williams, _Chiral differential operators via Batalin-Vilkovisky quantization_, [pdf](http://people.mpim-bonn.mpg.de/gwilliam/cdo.pdf)
* Brian Williams, _The Virasoro vertex algebra and factorization algebras on Riemann surfaces_, Lett. Math. Phys. __107__:12, 2189–2237 (2017) [doi](https://dx.doi.org/10.1007/s11005-017-0982-7)

A version of bosonic string theory related to factorization algebras is presented in

* Owen Gwilliam, Brian Williams, _The holomorphic bosonic string?, [arxiv/1711.05823](https://arxiv.org/abs/1711.05823)


A higher-dimensional generalization of vertex algebras is suggested in the framework of factorization algebras in
 
* Emily Cliff, _Universal factorization spaces and algebras_, [arxiv/1608.08122](http://arxiv.org/abs/1608.08122)

>  We introduce categories of weak factorization algebras and factorization spaces, and prove that they are equivalent to the categories of ordinary factorization algebras and spaces, respectively. This allows us to define the pullback of a factorization algebra or space by an \'etale morphism of schemes, and hence to define the notion of a universal factorization space or algebra. This provides a generalization to higher dimensions and to non-linear settings of the notion of a vertex algebra. 

Relation to [[homotopical algebraic quantum field theory]]:

* [[Donald Yau]], _Homotopical quantum field theory_ &lbrack;[arxiv/1802.08101](https://arxiv.org/abs/1802.08101)&rbrack;

* [[Marco Benini]], Giorgio Musante, [[Alexander Schenkel]], *Quantization of Lorentzian free BV theories: factorization algebra vs algebraic quantum field theory* &lbrack;[arXiv:2212.02546](https://arxiv.org/abs/2212.02546)&rbrack;

* [[Marco Benini]]: *A stacky approach to the comparison of axiomatizations of quantum field theory*, [talk at](CQTS#BeniniNov2024) [[CQTS]], NYU Abu Dhabi (Nov 2024) &lbrack;slides:[[Benini-CQTS-Nov2024.pdf:file]]&rbrack;

* [[Marco Benini]], [[Victor Carmona]], [[Alastair Grant-Stuart]], [[Alexander Schenkel]]: *On the equivalence of AQFTs and prefactorization algebras* &lbrack;[arXiv:2412.07318](https://arxiv.org/abs/2412.07318)&rbrack;



[[conformal net|Conformal nets]] exhibit factorization algebras

* [[Andre Henriques]], _Conformal nets are factorization algebras_, [arXiv:1611.05529](https://arxiv.org/abs/1611.05529)

Relation with [[vertex algebras]]

* Yusuke Nishinaka, _An algebraic construction of functors between vertex algebras and Costello--Gwilliam factorization algebras_, [arXiv:2408.00412](https://arxiv.org/abs/2408.00412)

> We construct functors between the category of vertex algebras and that of Costello-Gwilliam factorization algebras on the complex plane ℂ, without analytic structures such as differentiable vector spaces, nuclear spaces, and bornological vector spaces. We prove that this pair of functors is an adjoint pair and that the functor from vertex algebras to factorization algebras is fully faithful. Also, we identify the class of factorization algebras that are categorically equivalent to vertex algebras. To illustrate, we check the compatibility with the commutative structures and the factorization algebras constructed as factorization envelopes, including the Kac-Moody factorization algebra, the quantum observables of the βγ system, and the Virasoro factorization algebra. 

A generalized treatment:

* [[Clark Barwick]], _Factorization algebras in quite a lot of generality_ &lbrack; [arXiv:2602.01292](https://arxiv.org/abs/2602.01292),  [pdf](https://webhomes.maths.ed.ac.uk/~cbarwick/papers/facts.pdf)&rbrack;




[[!redirects factorization algebras]]