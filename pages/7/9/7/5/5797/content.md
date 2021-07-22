
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Supergeometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _super $L_\infty$-algebra_ is an [[L-∞ algebra]] in the context of [[superalgebra]]: the [[higher category theory|higher category theoretical]]/[[homotopy theory|homotopy theoretical]] version of a [[super Lie algebra]]. For more background see at _[[geometry of physics -- superalgebra]]_.


In the [[supergravity]] literature the [[formal duality|formal dual]] of super $L_\infty$-algebras of [[finite type]] came to be known as "[[FDA]]"s (see remark \ref{SuperLInfintiyAsFDA} below), a decade before plain [[L-∞ algebras]] were discussed in the mathematical literature. The key example in this context are [[extended super Minkowski spacetimes]], which are [[super L-∞ algebras]] obtained by iterated [[universal higher central extension]] from the [[super Minkowski spacetime]] [[super Lie algebra]]. The super-[[L-∞ algebra cohomology]] of these (called "[[tau-cohomology]]" in the physics literature) turns out to classify [[super p-branes]] and serves as a tool for the construction of [[supergravity]] theories in the [[D'Auria-Fré formulation of supergravity]]. For more background on this see at _[[geometry of physics -- fundamental super p-branes]]_.


## Definition
 {#Definition}

Abstractly, the definition is immediate:

+-- {: .num_defn #SuperLInfinityAlgebra}
###### Definition

A **super $L_\infty$-algebra** is an [[L-∞ algebra]] [[internalization|internal to]] the [[symmetric monoidal category]] of [[super vector spaces]] (i.e. in [[chain complexes of super vector spaces]]).

=-- 

Explicitly this equivalently comes down to the following definition in components:

+-- {: .num_defn #SuperGradedSignatureOfPermutation}
###### Definition
**(super graded signature of a permutation)**

Let $V$ be a $\mathbb{Z}$-[[graded object|graded]] [[super vector space]], hence a $\mathbb{Z} \times (\mathbb{Z}/2)$-bigraded vector space. 

For $n \in \mathbb{N}$ let 

$$
  \mathbf{v} = (v_1, v_2, \cdots, v_n)
$$ 

be an [[n-tuple]] of elements of $V$ of homogeneous degree $(n_i, s_i) \in \mathbb{Z} \times \mathbb{Z}/2$, i.e. such that $v_i \in V_{(n_i,s_i)}$. 

For $\sigma$ a [[permutation]] of $n$ elements, write $(-1)^{\vert \sigma \vert}$ for the [[signature of a permutation|signature of the permutation]], which is by definition equal to $(-1)^k$ if $\sigma$ is the composite of $k \in \mathbb{N}$ permutations that each exchange precisely one pair of neighboring elements.

We say that the _super $\mathbf{v}$-graded signature of $\sigma$_

$$
  \chi(\sigma, v_1, \cdots, v_n) \;\in\; \{-1,+1\}
$$ 

is the product of the [[signature of a permutation|signature of the permutation]] $(-1)^{\vert \sigma \vert}$ with a factor of 

$$
  (-1)^{n_i n_j}(-1)^{s_i s_j}
$$ 

for each interchange of neighbours $(\cdots v_i,v_j, \cdots )$ to $(\cdots v_j,v_i, \cdots )$ involved in the decomposition of the permuation as a sequence of swapping neighbour pairs (see at _[[signs in supergeometry]]_ for discussion of this combination of super-grading and homological grading).

=--

Now def. \ref{SuperLInfinityAlgebra} is equivalent to the following def. \ref{sLInfinityDefinitionViaGeneralizedJacobiIdentity}. This is just the definiton for [L-infinity algebras](#L-infinity-algebra#DefinitionViaHigherBrackets), with the pertinent sign $\chi$ now given by def. \ref{SuperGradedSignatureOfPermutation}.


+-- {: .num_defn #sLInfinityDefinitionViaGeneralizedJacobiIdentity}
###### Definition

An _super $L_\infty$-algebra_ is 

1. a $\mathbb{Z} \times (\mathbb{Z}/2)$-[[graded object|graded]] [[vector space]] $\mathfrak{g}$;

1. for each $n \in \mathbb{N}$ a [[multilinear map]], called the _$n$-ary bracket_, of the form

   $$
     l_n(\cdots) 
       \;\coloneqq\; 
     [-,-, \cdots, -]_n 
     \;\colon\; 
       \underset{n \; \text{copies}}{\underbrace{\mathfrak{g} \otimes \cdots \otimes \mathfrak{g}}}
       \longrightarrow
       \mathfrak{g}
   $$
  
   and of degree $n-2$
  
such that the following conditions hold:

1. (**super graded skew symmetry**) each $l_n$ is graded antisymmetric, in that for every [[permutation]] $\sigma$ of $n$ elements and for every [[n-tuple]] $(v_1, \cdots, v_n)$ of  homogeneously graded elements $v_i \in \mathfrak{g}_{\vert v_i \vert}$ then

   $$
     l_n(v_{\sigma(1)}, v_{\sigma(2)},\cdots ,v_{\sigma(n)}) 
     = 
     \chi(\sigma,v_1,\cdots, v_n) \cdot l_n(v_1, v_2, \cdots v_n)
   $$

   where $\chi(\sigma,v_1,\cdots, v_n)$ is the super $(v_1,\cdots,v_n)$-graded signature of the permuation $\sigma$, according to def. \ref{SuperGradedSignatureOfPermutation};

1. (**strong homotopy [[Jacobi identity]]**) for all $n \in \mathbb{N}$, and for all [[n-tuple|(n+1)-tuples]] $(v_1, \cdots, v_{n+1})$ of homogeneously graded elements $v_i \in \mathfrak{g}_{\vert v_i \vert}$ the followig [[equation]] holds

   \[
     \label{LInfinityJacobiIdentity}
     \sum_{{i,j \in \mathbb{N}} \atop {i+j = n+1}} 
     \sum_{\sigma \in UnShuff(i,j)}
     \chi(\sigma,v_1, \cdots, v_{n})
     (-1)^{i(j-1)}
      l_{j} \left(
        l_i \left( v_{\sigma(1)}, \cdots, v_{\sigma(i)} \right),
        v_{\sigma(i+1)} , \cdots , v_{\sigma(n)}
      \right)
     = 0
     \,,
   \]

   where the inner sum runs over all $(i,j)$-[[unshuffles]] $\sigma$ and where $\chi$ is the super graded signature sign from def. \ref{SuperGradedSignatureOfPermutation}.


A _strict [[homomorphism]]_ of super $L_\infty$-algebras

$$is
  \mathfrak{g}_1 \longrightarrow \mathfrak{g}_2
$$

is a [[linear map]] that preserves the bidegree and all the brackets, in an evident sens.

A _[[homomorphism of L-infinity algebras|strong homotopy homomorphism]]_ ("[[sh map]]") of super $L_\infty$-algebras is something weaker than that, best defined in [[formal duality|formal duals]], below in def. \ref{SuperLInfinityCEAlgebra}.

=--

In order to define the correct homomorphisms between super $L_\infty$-algebras ("sh-maps") as well as their super-[[L-∞ algebra cohomology]], consider the following dualization of the above definition:

+-- {: .num_defn #SuperLInfinityCEAlgebra}
###### Definition

A super $L_\infty$ algebra $\mathfrak{g}$ is of _[[finite type]]_ if the underlying $\mathbb{Z} \times (\mathbb{Z}/2)$-[[graded vector space]] is degreewise of [[finite number|finite]] [[dimension]].

If $\mathfrak{g}$ is of finite type, then its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ is the [[differential graded-commutative superalgebra]] whose underlying [[graded algebra]] is the super-Grassmann algebra

$$
  \wedge^\bullet \mathfrak{g}^{\ast}
$$

of the graded degreewise [[dual vector space]] $\mathfrak{g}^\ast$, equipped with the [[differential]] which on generators is the sum of the [[dual linear maps]] of the $n$-ary brackets:

$$
  d_{\mathfrak{g}}
   \coloneqq
  [-]^\ast + [-,-]^\ast + [-,-,-]^\ast + \cdots
  \;\colon\;
  \wedge^1 \mathfrak{g}^\ast
    \longrightarrow
  \wedge^\bullet \mathfrak{g}^\ast
$$

and extended to all of $\wedge^\bullet \mathfrak{g}^\ast$ as a super-graded [[derivation]] of degree $(1,even)$.

Notice that here the [[signs in supergeometry]] are such that for $\alpha_i \in \mathfrak{g}^\ast_{(n_i,s_i)}$ elements of homogenous bidegree, then 

$$
  \alpha_1 \wedge \alpha_2
  \;=\;
  -(-1)^{n_1 n_2} (-)^{s_1 s_2}
$$

and

$$
  d_{\mathfrak{g}}
  (\alpha_1 \wedge \alpha_2)
  \;=\;
  (d_{\mathfrak{g}} \alpha_1) \wedge \alpha_2
  + 
  (-1)^{n_1} \alpha_1 \wedge (d_{\mathfrak{g}} \alpha_2)
  \,.
$$

(see at _[[signs in supergeometry]]_ for more on this).

A _strong homotopy homomorphism_ ("sh-map") between super $L_\infty$-algbras of [[finite type]]

$$
 f \;\colon\; \mathfrak{g}_1 \longrightarrow \mathfrak{g}_2
$$

is defined to be a homomorphism of [[dg-algebras]] between their [[Chevalley-Eilenberg algebras]] going the other way:


$$
  CE(\mathfrak{g}_1) \longleftarrow CE(\mathfrak{g}_2)
    \;\colon\;
  f^\ast
$$

(here $f^\ast$ is the primitive concept, and $f$ is defined as the [[formal duality|formal dual]] of $f$). Hence the [[category]] of super $L_\infty$-algebras of [[finite type]] is the [[full subcategory]]

$$
  s L_\infty Alg \hookrightarrow dgcsAlg^{op}
$$

of the [[opposite category]] of [[differential graded-commutative superalgebras]] on those that are CE-algebras as above.

Finally, the [[cochain cohomology]] of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ of a super $L_\infty$ algebra of [[finite type]] is its _[[L-∞ algebra cohomology]]_ with [[coefficients]] in $\mathbb{R}$:

$$
  H^\bullet(\mathfrak{g}, \mathbb{R})
   \;=\;
  H^\bullet(CE(\mathfrak{g}))
  \,.
$$

=--

+-- {: .num_remark #LInfinityTerminology}
###### Remark

Special cases of the general concept of [[super L-∞ algebras]] def. \ref{sLInfinityDefinitionViaGeneralizedJacobiIdentity} go by special names:

Let $\mathfrak{g}$ be a [[super L-∞ algebra]].

If $\mathfrak{g}$ is concentrated in even $\mathbb{Z}/2$-degree, it is called an _[[L-∞ algebra]]_.

If the only possibly non-vanishing brackets of $\mathfrak{g}$ are the unary one $[-]$ (which induces the structure of a [[chain complex]] on $\mathfrak{g}$) and the binary one, then $\mathfrak{g}$ is equivalently a (super-)[[dg-Lie algebra]].

If $\mathfrak{g}$ is concentrated in $\mathbb{Z}$-degrees 0 to $n-1$ then it is called a _[[super Lie n-algebra]]_.

In particular if $\mathfrak{g}$ is concentrated in degree 0, then it is equivalently a [[super Lie algebra]].

Combining this, if $\mathfrak{g}$ is concentrated in even $\mathbb{Z}/2$-degree and in $\mathbb{Z}$-degree 0 through $n-1$, then it is called a _[[Lie n-algebra]]_.

In particular if $\mathfrak{g}$ is concentrated in $\mathbb{Z}$-degree 0 and in even $\mathbb{Z}/2$-degree, then it is
equivalently a plain [[Lie algebra]].

=--


## History

+-- {: .num_remark #SuperLInfintiyAsFDA}
###### Remark
**(history of the concept of (super-)$L_\infty$ algebras)**

The identification of the concept of (super-)$L_\infty$-algebras has a non-linear history:

[[L-∞ algebras]] in the incarnation of higher brackets satisfying a higher Jacobi identity, 
def. \ref{sLInfinityDefinitionViaGeneralizedJacobiIdentity}
and remark \ref{LInfinityTerminology}, were introduced in
[Lada-Stasheff 92](https://ncatlab.org/nlab/show/L-infinity-algebra#LadaStasheff92), based on the 
example of such a structure on the [[BRST complex]] of the [[bosonic string]] that 
was found in the construction of [[closed string field theory]] in [Zwiebach 92](string+field+theory#Zwiebach93).
Some of this history is recalled in [Stasheff 16](#L-infinity-algebra#Stasheff16).

The observation that these systems of higher brackets are fully characterized by their Chevalley-Eilenberg dg-(co-)algebras
(def. \ref{SuperLInfinityCEAlgebra})
is due to [Lada-Markl 94](https://ncatlab.org/nlab/show/L-infinity-algebra#LadaMarkl94).
See [Sati-Schreiber-Stasheff 08, around def. 13](#SatiSchreiberStasheff08).

But in this dual incarnation, [[L-∞ algebras]] and more generally [[super L-∞ algebras]] (of [[finite type]]) 
had secretly been introduced within the [[supergravity]] literature already in [D'Auria-Fr&#233;-Regge 80](#DAuriaFreRegge80) and explicitly in [van Nieuwenhuizen 82](#Nieuwenhuizen82).
The concept was picked up in the [[D'Auria-Fré formulation of supergravity]] ([D'Auria-Fr&#233; 82](#DAuriaFre82)) and eventually came to be referred to as "FDA"s (short for "free differential algebra") in the [[supergravity]] literature (but beware that these dg-algebras 
are in general [[free construction|free]] only as graded-[[supercommutative superalgebras]], not as differential algebras)
The relation between super $L_\infty$-algebras and the "FDA"s of the [[supergravity]] literature is made explicit in ([FSS 13](#FSS13)).

| [[nLab:higher Lie theory]] | [[nLab:supergravity]] |
|----------------------------|-----------------------|
| $\,$ [[nLab:super Lie n-algebra]] $\mathfrak{g}$ $\,$ | $\,$ "FDA" $CE(\mathfrak{g})$ $\,$ |

The construction in [van Nieuwenhuizen 82](#Nieuwenhuizen82) in turn was motivated by the [[Sullivan algebras]]
in [[rational homotopy theory]] ([Sullivan 77](#rational+homotopy+theory#Sullivan77)). Indeed, their
dual incarnations in rational homotopy theory are [[dg-Lie algebras]] ([Quillen 69](#rational+homotopy+theory#Quillen69)),
hence a special case of $L_\infty$-algebras (remark \ref{LInfinityTerminology})

This close relation between [[rational homotopy theory]] and [[higher Lie theory]] might have remained less of a
secret had it not been for the focus of [[Sullivan minimal models]] on the non-[[simply connected topological space|simply connected]]
case, which excludes the ordinary [[Lie algebras]] from the picture. But the Quillen model of
[[rational homotopy theory]] effectively says that for $X$ a [[rational topological space]] then its [[loop space]]
[[∞-group]] $\Omega X$ is reflected, infinitesimally, by an [[L-∞ algebra]]. This perspective began to 
receive more attention when the [[Sullivan construction]] in [[rational homotopy theory]] was
concretely identified as higher [[Lie integration]] in [Henriques 08](#Lie+integration#Henriques).
A modern review that makes this [[L-∞ algebra]]-theoretic nature of [[rational homotopy theory]] manifest is in 
[Buijs-F&#233;lix-Murillo 12, section 2](rational+homotopy+theory#BuijsFelixMurillo12).

=--




## Properties

* Every super $L_\infty$-Lie algebra has a [[Lie integration]] to a [[super ∞-groupoid]] and a [[smooth super ∞-groupoid]]. See at _[[Lie integration]]_ for more on this.

## Examples

In the context of [[supergravity]]/[[string theory]] the

* [[super Poincaré Lie algebra]]

and its super-$L_\infty$-extensions to the 

* [[supergravity Lie 3-algebra]] ([[m2brane]])

* [[supergravity Lie 6-algebra]]

* [[type II supergravity Lie 2-algebra]]

play a central role. Their exceptional [[infinity-Lie algebra cohomology]] governs the consistent [[Green-Schwarz action functionals]] for super-$p$-[[brane|branes]]. (See the discusson of the _[brane scan](Green-Schwarz+action+functional#BraneScan)_) there.

See at _[[geometry of physics -- fundamental super p-branes]]_ for more on this.

$\,$

The [[BRST complex]] of the [[superstring]] might form a super $L_\infty$-algebra whose brackets give the [[n-point function]] of the string, in analogy to what happens for the bosonic string in Zwiebach's [[string field theory]]. (...)

## Related concepts

* [[model structure on chain complexes of super vector spaces]]

* [[model structure on differential graded-commutative superalgebras]]

## References

In their [[formal duality|formal dual]] incarnations as super-graded commutative [[dg-algebras]] (super [[Chevalley-Eilenberg algebras|Chevalley-Eilenberg algebras]]), super $L_\infty$-algebras of [[finite type]] had secretly been introduced in 

* {#DAuriaFreRegge80} [[Riccardo D'Auria]], [[Pietro Fré]] [[Tullio Regge]], _Graded Lie algebra, cohomology and supergravity_, Riv. Nuov. Cim. 3, fasc. 12 (1980) ([spire](http://inspirehep.net/record/156191))

* {#Nieuwenhuizen82} [[Peter van Nieuwenhuizen]], _Free Graded Differential Superalgebras_, in *Istanbul 1982, Proceedings, Group Theoretical Methods In Physics*, 228-247 and CERN Geneva - TH. 3499 ([spire](http://inspirehep.net/record/182644/))

and hence a whole decade before the explicit appearance of plain (non-super) [[L-∞ algebras]] in [Lada-Stasheff 92](L-infinity-algebra#LadaStasheff92).

The concept was picked up in the [[D'Auria-Fré formulation of supergravity]]

* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]], _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 ([[GeometricSupergravityErrata.pdf:file]]) 

and eventually came to be referred to as "FDA"s (short for "free differential algebra") in the [[supergravity]] literature (where in [[rational homotopy theory]] one says "[[semifree dga]]", since these dg-algebras are crucially not required to be free as _differential_ algebras).

The relation between super $L_\infty$-algebras and the "FDA"s of the [[supergravity]] literature is made explicit in

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ ([arXiv:1308.5264](https://arxiv.org/abs/1308.5264))


[[!redirects super L-∞ algebra]]
[[!redirects super L-∞ algebras]]

[[!redirects super L-infinity algebras]]

[[!redirects super Lie n-algebra]]
[[!redirects super Lie n-algebras]]

[[!redirects super Lie-infinity algebra]]

[[!redirects super Lie-∞ algebra]]
[[!redirects super Lie-∞ algebras]]

[[!redirects FDA]]
[[!redirects FDAs]]

