
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **Sullivan model** of a [[rational space]] $X$ is a particularly well-behaved commutative [[dg-algebra]] [[quasi-isomorphism|quasi-isomorphic]] to the dg-algebra of Sullivan forms on $X$.
These _Sullivan algebras_ are precisely the cofibrant objects in the standard [[model structure on dg-algebras]].

Sullivan models are a central tool in [[rational homotopy theory]].


## Definition


Sullivan models are particularly well-behaved [[differential graded-commutative algebras]] that are equivalent to the dg-algebras of [piecewise polynomial differential forms on topological spaces](differential+forms+on+simplices#PiecewisePolynomialDifferentialForms). Conversely, every rational space can be obtained from a dg-algebra and the _minimal_ Sullivan algebras provide convenient representatives that correspond bijectively to rational homotopy types under this correspondence.

Abstractly, (relative) Sullivan models are the (relative) [[cell complexes]] in the standard [[model structure on dg-algebras]].

We now describe this in detail. First some notation and preliminaries:

+-- {: .num_defn #FiniteType}
###### Definition
**([[of finite type]])**

* A [[graded vector space]] $V$ is _[[of finite type]]_ if in each degree it is finite dimensional. In this case we write $V^*$ for its degreewise dual.

* A [[Grassmann algebra]] is *[[of finite type]]* if it is the Grassmann algebra $\wedge^\bullet V^*$ on a graded vector space of finite type 

  (the dualization here is just convention, that will help make some of the following constructions come out nicely).

* A [[CW-complex]] is of finite type if it is built out of finitely many cells in each degree.

=--



For $V$ a $\mathbb{N}$-[[graded vector space]] write 
$\wedge^\bullet V$ for the [[Grassmann algebra]] over it. Equipped with the trivial differential $d = 0$ this is a [[semifree dgc-algebra]] $(\wedge^\bullet V, d=0)$.

With $k$ our ground [[field]] we write $(k,0)$ for the corresponding [[dg-algebra]], the tensor unit for the standard [[monoidal category|monoidal structure]] on $dgAlg$. This is the [[Grassmann algebra]] on the 0-vector space
$(k,0) = (\wedge^\bullet 0, 0)$.


+-- {: .num_defn #SullivanAlgebra}
###### Definition
**(Sullivan algebras)**

A **relatived Sullivan algebra** is a [[homomorphism]] of [[differential graded-commutative algebras]] that is an inclusion of the form

$$
  (A,d) \hookrightarrow (A \otimes_k \wedge^\bullet V, d')
$$

for $(A,d)$ any [[dgc-algebra]] and for $V$ some [[graded vector space]], such that 

1. there is a [[well ordered set]] $J$ indexing a [[linear basis]] $\{v_\alpha \in V| \alpha \in J\}$ of $V$;

1. writing $V_{\lt \beta} \coloneqq span(v_\alpha | \alpha \lt \beta)$ then for all basis elements $v_\beta$ we have that 

  $$
    d' v_\beta \in A \otimes \wedge^\bullet V_{\lt \beta}
    \,.
  $$

This is called a **minimal** relative Sullivan algebra if in addition the condition

$$
  (\alpha \lt \beta) \Rightarrow (deg v_\alpha  \leq deg v_\beta)
$$

holds. For a Sullivan algebra $(k,0) \to (\wedge^\bullet V, d)$ relative to the tensor unit we call the [[semifree dgc-algebra]] $(\wedge^\bullet V,d)$ simply a **Sullivan algebra**, and we call it a **minimal Sullivan algebra** if $(k,0) \to (\wedge^\bullet V, d)$ is a minimal relative Sullivan algebra.

=--

(e.g. [Hess 06, def. 1.10, remark 1.11](#Hess06))

See also the section [Sullivan algebras](model+structure+on+dg-algebras#SullivanAlgebras) at [[model structure on dg-algebras]].


+-- {: .num_remark }
###### Remark

The special condition on the ordering in the relative Sullivan algebra says that these morphisms are composites of [[pushouts]] of the [[cofibrantly generated model category|generating cofibrations]] for the [[model structure on dg-algebras]], which are the inclusions

$$
  S(n) \hookrightarrow D(n)
  \,,
$$

where 

$$
  S(n) = (\wedge^\bullet \langle c \rangle, d = 0)
$$ 

is the dg-algebra on a single generator in degree $n$ with vanishing differential, and where

$$
  D(n) = (\wedge^\bullet (\langle b \rangle \oplus \langle c \rangle), d b = c, d c = 0)
$$ 

with $b$ an additional generator in degree $n-1$.

Therefore for $A \in dgcAlg$, a pushout

$$
  \array{
     S(n) &\stackrel{\phi}{\to}& A
     \\
     \downarrow && \downarrow
     \\
     D(n) &\to& (A \otimes \wedge^ \bullet \langle b \rangle, d b = \phi) 
  }
$$ 

is precisely a choice $\phi \in A$ of a $d_A$-closed element in degree $n$
and results in adjoining to $A$ the element $b$ whose differential is
$d b = \phi$. This gives the condition in the above definition: the differential of any new element has to be a sum of wedge products of the old elements.

Notice that it follows in particular that the cofibrations in $dgAlg_{proj}$ are precisely all the [[retracts]] of relative Sullivan algebra inclusions.

=--

+-- {: .num_remark }
###### Remark
**($L_\infty$-algebras)**

Because they are [[semifree dga]]s, Sullivan dg-algebras $(\wedge^\bullet V,d)$ are (at least for degreewise finite dimensional $V$) [[Chevalley-Eilenberg algebra]]s of [[L-∞-algebra]]s.

The co-commutative differential co-algebra encoding the corresponding [[L-∞-algebra]] is the free cocommutative algebra $\vee^\bullet V^*$ on the degreewise dual of $V$ with differential $D = d^*$, i.e. the one given by the formula

$$
  \omega(D(v_1 \vee v_2 \vee \cdots v_n)) =
  - (d \omega) (v_1, v_2, \cdots,  v_n)
$$

for all $\omega \in V$ and all $v_i \in V^*$.

=--



+-- {: .num_defn }
###### Definition
**(Sullivan models)**

For $X$ a [[simply connected]] [[topological space]] $X$, a **Sullivan (minimal) model** for $X$ is a Sullivan (minimal) algebra $(\wedge^\bullet V^\ast, d_V)$ equipped with a [[quasi-isomorphism]]

  $$
    (\wedge^\bullet V^*, d_V) 
      \stackrel{\simeq}{\longrightarrow}
    \Omega^\bullet_{pwpoly}(X)
  $$

  to the dg-algebra of [[piecewise polynomial differential forms]].

=--



## Properties

### As cofibrations


+-- {: .num_prop }
###### Proposition
**(cofibrations are relative Sullivan algebras)**

The cofibrations in the [[projective model structure on differential graded-commutative algebras]] $(dgcAlg_{\mathbb{N}})_{proj}$ are precisely the [[retracts]] of relative  Sullivan algebra inclusions (def. \ref{SullivanAlgebra}).

Accordingly, the cofibrant objects in $(dgcAlg_{\mathbb{N}})_proj{}$ are precisely the [[retracts]] of Sullivan algebras.

=--

+-- {: .num_prop }
###### Proposition

Minimal Sullivan models are unique up to [[isomorphism]]. 

=--

e.g [Hess 06, prop 1.18](#Hess06).


### Rationalization


+-- {: .num_theorem #SullivanRationalizationEquivalence}
###### Theorem

Consider the [[adjunction]] of [[derived functors]]

$$
  Ho(Top)
   \simeq
  Ho(sSet)
   \underoverset
     {\underset{\mathbb{R} \Omega^\bullet_{poly}}{\longrightarrow}}
     {\overset{\mathbb{L} K_{poly} }{\longleftarrow}}
     {\bot}
  Ho( (dgcAlg_{\mathbb{Q}, \geq 0})^{op} )
$$

induced from the [[Quillen adjunction]] 

$$
  (dgcAlg_{\mathbb{Q}, \geq 0}_{proj})^{op}
    \underoverset
      {\underset{K_{poly}}{\longrightarrow}}
      {\overset{\Omega^\bullet_{poly}}{\longleftarrow}}
      {\bot}
  sSet_{Quillen}
$$

([this theorem](rational+homotopy+theory#SullivanRationalizationAdjunction)).


Then: On the [[full subcategory]] $Ho(Top_{\mathbb{Q}, \geq 1}^{fin})$ of [[simply connected topological space|simply connected]] [[rational topological spaces]] of [[finite type]] this adjunction restricts to an [[equivalence of categories]]

$$
  Ho(Top_{\mathbb{Q}, \gt 1}^{fin})
   \underoverset
     {\underset{\mathbb{R} \Omega^\bullet_{poly}}{\longrightarrow}}
     {\overset{\mathbb{L} K_{poly} }{\longleftarrow}}
     {\simeq}
  Ho( (dgcAlg_{\mathbb{Q}, \gt 1}^{fin})^{op} )  
  \,.
$$

In particular the [[adjunction unit]]

$$
  X \longrightarrow K_{poly}(\Omega^\bullet_{pwpoly}(X))
$$

exhibits the [[rationalization]] of $X$.

=--


This is a central theorem of [[rational homotopy theory]], see for instance  [Hess 06, corollary 1.26](#Hess06).

It follows that the [[cochain cohomology]] of the cochain complex of [[piecewise polynomial differential forms]] on any topological, hence equivalently that of any of its [[Sullivan models]], coincides with its [[ordinary cohomology]] with coefficients in the [[rational numbers]]:



+-- {: .num_theorem }
###### Theorem

Let $(\wedge^\bullet V^*, d_V)$ be a minimal Sullivan model of a simply connected rational topological space $X$. Then there is an [[isomorphism]]

$$
  \pi_\bullet(X)
    \simeq
  V
$$

between the [[homotopy groups]] of $X$ and the generators of the minimal Sullivan model.

=--


e.g. [Hess 06, theorem 1.24](#Hess06).





### Relation to Whitehead products

See at _[[the co-binary Sullivan differential is the dual Whitehead product]]_.




\linebreak




## Examples 

[[!include Sullivan models -- examples]]






## Related concepts

* [[formal dg-algebra]]

* [[minimal dg-module]]

* [[minimal fibration]]

* [[equivariant Sullivan model]]

## References

Original articles:

* {#Sullivan77} [[Dennis Sullivan]], _Infinitesimal computations in topology_, Publications Math&#233;matiques de l'IH&#201;S, 47 (1977), p. 269-331 ([numdam:PMIHES_1977__47__269_0](http://www.numdam.org/item/PMIHES_1977__47__269_0/))

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))

* {#GriffithMorgan13} [[Phillip Griffiths]], [[John Morgan]], _Rational Homotopy Theory and Differential Forms_,  Progress in Mathematics Volume 16, Birkhauser (2013) ([doi:10.1007/978-1-4614-8468-4](https://doi.org/10.1007/978-1-4614-8468-4))


Review and application:

* {#Halperin83} [[Steve Halperin]], _Lectures on minimal models_, Mem. Soc. Math. Franc. no 9/10 (1983) ([doi:10.24033/msmf.294](https://doi.org/10.24033/msmf.294))

* {#FelixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]], Chapter II of: _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000 ([doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9))

* {#Hess06} [[Kathryn Hess]], around def 1.10  of _Rational homotopy theory: a brief introduction_ ([arXiv:math.AT/0604626](http://arxiv.org/abs/math.AT/0604626))

* {#Menichi13} [[Luc Menichi]], _Rational homotopy -- Sullivan models_, IRMA Lect. Math. Theor. Phys., EMS ([arXiv:1308.6685](https://arxiv.org/abs/1308.6685))

* {#FelixHalperin17} [[Yves Félix]], [[Steve Halperin]], _Rational homotopy theory via Sullivan models: a survey_,  Notices of the International Congress of Chinese Mathematicians Volume 5 (2017) Number 2 ([arXiv:1708.05245](https://arxiv.org/abs/1708.05245), [doi:10.4310/ICCM.2017.v5.n2.a3](https://dx.doi.org/10.4310/ICCM.2017.v5.n2.a3))


[[!redirects Sullivan models]]
[[!redirects Sullivan algebra]]
[[!redirects Sullivan algebras]]
[[!redirects Sullivan minimal algebra]]
[[!redirects Sullivan minimal algebras]]

[[!redirects relative Sullivan model]]
[[!redirects relative Sullivan models]]


[[!redirects relative Sullivan algebra]]
[[!redirects relative Sullivan algebras]]

[[!redirects minimal Sullivan algebra]]
[[!redirects minimal Sullivan algebras]]

[[!redirects minimal Sullivan model]]
[[!redirects minimal Sullivan models]]

[[!redirects Sullivan minimal model]]
[[!redirects Sullivan minimal models]]

