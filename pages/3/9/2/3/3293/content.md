

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

\tableofcontents


## Idea

The concept of _Fr&#233;chet manifold_ is a special case of that of _[[infinite-dimensional manifold]]_:
In analogy to how a finite-dimensional [[smooth manifold]] is a [[manifold]] modeled on a [[Cartesian space]] $\mathbb{R}^n$ in [[CartSp]], a _Fr&#233;chet manifold_ is a [[manifold]] modeled on a [[Fréchet space]], such as notably $\mathbb{R}^\infty$ ([exmpl.](Fr&#233;chet+space#ProjRInfinity)).

The [[category]] of Fr&#233;chet manifolds is a [[full subcategory]] of that of [[diffeological spaces]] (prop. \ref{FFEmbeddingOfFrechetInDiffeological} below) hence of [[smooth sets]] (see [here](diffeological+space#EmbeddingOfDiffeologicalSpacesIntoTheSheafTopos)).

## Definition

### Fr&#233;chet manifolds

It is possible to define, analogous to the finite dimensional case, the notion of [[smooth functions]] between [[Fréchet spaces]], see at _[Fr&#233;chet space -- Differentiable and smooth functions](Fr&#233;chet+space#DifferentiableAndSmoothFunctions)_. Therefore, the usual definition of _[[smooth manifold]]_ carries over word by word:

+-- {: .num_defn}
###### Definition
A **Fr&#233;chet manifold** is a [[Hausdorff topological space]] with an [[atlas]] of [[coordinate charts]] taking their value in [[Fréchet spaces]], such that the coordinate transition functions are all smooth functions between Fr&#233;chet spaces.
=--

It is possible to generalize some concepts of differential geometry from the finite case to the Fr&#233;chet case, one has to be careful, however:

1. The [[dual vector space|dual]] of a Fr&#233;chet space that is not a [[Banach space]] is never a Fr&#233;chet space, therefore one cannot e.g. define both the tangent and the cotangent bundle as Fr&#233;chet manifolds. More serious is however

2. The existence and uniqueness theorems for ordinary differential equations fail in infinite dimensions, so that theorems depending on that from finite dimensional differential geometry cannot be transcribed to the infinite situation in general. It is possible to do this on a case by case basis however.

### Tangent Vectors

There are several definitions of tangent vectors that are equivalent in the finite dimensional setting, but may be different in infinite dimensions. Tangent vectors can be defined to be derivations on germs of functions (algebraic definition), or as equivalence classes of smooth curves (kinematic definition). For the time being we settle with the kinematic definition:

+-- {: .num_defn}
###### Definition
**kinematic tangent vector**

The kinematic tangent vector space of a Fr&#233;chet manifold $M$ at a point $p$ consists of all pairs $(p, c'(0))$ where $c$ is a smooth curve
$$
c: \mathbb{R} \to M \; \text{with} \; c(0) = p
$$
As usual, the set of pairs $(p, c'(0)), p \in M$ forms a Fr&#233;chet manifold, the tangent bundle $TM$.
=--

The last sentence makes use of the notion of vector bundle, which can be defined exactly as in the finite dimensional setting:

### Vector bundles

+-- {: .num_defn}
###### Definition
**vector bundle**

A Fr&#233;chet manifold $V$ is a Fr&#233;chet vector bundle over $M$ with projection $\pi$, if for every point $p \in M$ there are charts of $M$ and $V$ such that $V$ is mapped locally to $U \subset F \times G$ for Fr&#233;chet spaces $F, G$, the projection $\pi$ corresponds to the projection of $U \times G$ to $U$, and the vector space structure on each fibre is induced by the vector space structure on $G$.
=--

Since, as mentioned before, the dual space of a Fr&#233;chet space that is not a Banach space is itself not a Fr&#233;chet space, we cannot define the cotangent space canonically as the dual space of the tangent space. Instead we define it directly:

### Differential forms

+-- {: .num_defn}
###### Definition
**differential form**

A differential form (a one form) $\alpha$ is a smooth map
$$
\alpha: T M \to \mathbb{R}
$$
where $TM$ is the tangent bundle.
=--

## Properties

### Relation to diffeological spaces  {#RelationBetweenDeffeologicalAndFrechetStructure}

We discuss how Fr&#233;chet manifolds form a [[full subcategory]] of that of [[diffeological spaces]].

+-- {: .num_defn }
###### Definition

Define a [[functor]]

$$
  \iota \;\colon\; FrechetManifolds \longrightarrow DiffeologicalSpaces
$$

from Fr&#233;chet manifolds to [[diffeological spaces]] (and hence to [[smooth spaces]] and  [[smooth stacks]])
in the evident way by taking for $X$ a [[Fréchet manifold]] for any $U \in $ [[CartSp]] the set of $U$-plots of $\iota(X)$ to be the set of smooth functions $U \to X$.

=--

+-- {: .num_prop #FFEmbeddingOfFrechetInDiffeological}
###### Proposition

The functor $\iota \colon FrechetManifolds \hookrightarrow DiffeologicalSpaces$ is a [[full and faithful functor]].

=--

This appears as ([Losik, theorem 3.1.1](#Losik94)).

+-- {: .num_prop #CompatibilityWithDiffeologicalMappingSpaces}
###### Proposition

Let $X, Y \in SMoothManifold$ with $X$ a [[compact manifold]]. 

Then under this embedding, the diffeological [[mapping space]] structure $C^\infty(X,Y)_{diff}$ on the mapping space coincides with the Fr&#233;chet manifold structure $C^\infty(X,Y)_{Fr}$:

$$
  \iota(C^\infty(X,Y)_{Fr})
  \simeq
  C^\infty(X,Y)_{diff}
  \,.
$$

=--

This appears as ([Waldorf, lemma A.1.7](#Waldorf)).

## Examples

### Smooth mapping spaces

+-- {: .num_example }
###### Example

For $X,Y$ two [[smooth manifolds]], such that in addition $X$ is [[compact topological space|compact]], then the [[mapping space]], i.e. the set of [[smooth functions]] $C^\infty(X,Y)$ is naturally a Fr&#233;chet manifold. Under the [[full subcategory]] inclusion of Fr&#233;chet manifolds into [[diffeological spaces]] and [[smooth sets]] (prop. \ref{FFEmbeddingOfFrechetInDiffeological}) this coincides with the canonical [[mapping space]] formed there.

For example [[smooth loop space]] (i.e. for $X = S^1$ the [[circle]]) are Fr&#233;chet manifolds.

For details on this see at _[[manifold structure of mapping spaces]]_.

=--

### Projective limits of smooth finite-dimensional manifolds
 {#ProjectiveLimitsOfSmoothFiniteDimensionalManifolds}

(see also [Dodson-Galanis-Vassiliou 15](#DodsonGalanisVassiliou15))

Fréchet manifolds may be thought of as [[projective limits]] of [[Banach manifolds]] (see the "added remark" at the end of [this MO comment](http://math.stackexchange.com/a/53020/58526))

+-- {: .num_example #RInfinity}
###### Example

The infinite product [[Fréchet space]] $\mathbb{R}^\infty$ ([exmpl.](Fr&#233;chet+space#ProjRInfinity)) is of course a Fr&#233;chet manifold.

=--

+-- {: .num_prop}
###### Proposition


As a Fr&#233;chet manifold, $\mathbb{R}^\infty$ (example \ref{RInfinity}) should be the [[projective limit]]

$$
  \mathbb{R}^\infty \simeq \underset{\longleftarrow}{\lim}_n \mathbb{R}^n
$$

formed in the category of Fr&#233;chet manifolds.

=--

+-- {: .proof}
###### Proof 

The point that needs checking is that for $X$ any Fr&#233;chet manifold, then a [[continuous function]] 

$$
  f \colon X \longrightarrow \mathbb{R}^\infty
$$ 

is smooth as soon as all its components 

$$
  f_n \colon X \overset{f}{\longrightarrow} \mathbb{R}^\infty
  \overset{p_n}{\longrightarrow} \mathbb{R}
$$ 

are smooth. This is checked for instance in ([Saunders 89, lemma 7.1.8](#Saunders89)).

=--


Conversely: 

+-- {: .num_prop #DifferentiableFunctionOutOfRInfinity}
###### Proposition

A function 

$$
  \mathbb{R}^\infty
    \longrightarrow
  \mathbb{R}
$$

_out_ of $\mathbb{R}^\infty$ (example \ref{RInfinity}) is differentiable precisely if at each point only a [[finite number]] of its partial derivative are non-vanishing.

=--


([Saunders 89, example 7.1.6](#Saunders89))


+-- {: .num_example #JetBundlesAsFrechetManifolds}
###### Example

As a global generalization of the pro-finite dimensional Fr&#233;chet manifold $\mathbb{R}^\infty$ of example \ref{RInfinity}, every infinite [[jet bundle]] $J^\infty E = \underset{\longleftarrow}{\lim}_k J^k E$ is a Fr&#233;chet manifold, modeled on $\mathbb{R}^\infty$ ([Saunders 89, chapter 7](#Saunders89)). 

=--

+-- {: .num_remark #DifferenceBetweenProManifoldAndFrecherManifoldStructure}
###### Remark

Beware, that infinite [[jet bundles]] are also naturally thought of as [[pro-manifolds]]. This differs from the Frechet manifold structure of example \ref{JetBundlesAsFrechetManifolds}:

A morphism of [[pro-manifolds]]

$$
  f \colon J^\infty E \longrightarrow \mathbb{R}
$$

is equivalently a function that is "globally of finite order", in that there exists $k \in \mathbb{N}$ and an ordinary smooth function $f_k \colon J^k E \to \mathbb{R}$ such that $f = f_k \circ p_k$.

But by prop. \ref{DifferentiableFunctionOutOfRInfinity} a morphisms of Fr&#233;chet manifolds 

$$
  f \colon J^\infty E \longrightarrow \mathbb{R}
$$

is only restricted to have finite order of partial derivatives at every point.

This is a weaker condition. In fact it seems to be also weaker than the condition of being "locally of finite order" considered in [Takens 79](jet+bundle#Takens79). (The function $f$ is _locally of finite order_ if for every point in $J^\infty E$ there exists a $k \in \mathbb{N}$ and an open neighbourhood $U_k$ of its image in $J^k E$ and a smooth function $f^U_k \colon U_k \to \mathbb{R}$ such that restricted to the pre-image of $U_k$ in $J^\infty E$ the function $f$ given by $f_k \circ p_k $).

Hence it makes sense to speak of _[[locally pro-manifolds]]_.

=--



## Related concepts

* [[Banach manifold]]

* [[Hilbert manifold]], [[ILH manifold]]

* [[convenient manifold]]

* [[F-star-algebra]]

* [[geometry of physics -- smooth sets]]


## References

Accounts include:

* [[Richard S. Hamilton]], Section I.4 in: *The inverse function theorem of Nash and Moser*, Bull. Amer. Math. Soc. **7** (1982) 65-222 &lbrack;[doi:1982-07-01/S0273-0979-1982-15004-2](https://doi.org/10.1090/S0273-0979-1982-15004-2), [euclid:bams/1183549049](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society-new-series/volume-7/issue-1/The-inverse-function-theorem-of-Nash-and-Moser/bams/1183549049.full)&rbrack;



* {#Michor80} [[Peter Michor]], _Manifolds of differentiable mappings_, Shiva Publishing (1980) [pdf](http://www.mat.univie.ac.at/~michor/manifolds_of_differentiable_mappings.pdf)

* {#KM} [[Andreas Kriegl]], [[Peter Michor]]: *[[The convenient setting of global analysis]]*, Mathematical Surveys and Monographs **53** AMS (1997) &lbrack;ISBN:978-0-8218-0780-4, [ams:surv-53](https://bookstore.ams.org/surv-53), [pdf](http://www.mat.univie.ac.at/~michor/apbookh-ams.pdf)&rbrack;
 
* V. I. Arnold,  B. A. Khesin, _Topological methods in hydrodynamics._ (Springer 1998, [ZMATH](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0902.76001&format=complete))

* Boris Khesin, Robert Wendt, _The geometry of infinite-dimensional groups._ (Springer 2009, [ZMATH](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1153.22001&format=complete))

* Armen Sergeev, Part I of: *Kähler Geometry of Loop Spaces*, MSJ Memoirs (2010) 1-76 &lbrack;[euclid:10.2969/msjmemoirs/02301C010](https://projecteuclid.org/ebooks/mathematical-society-of-japan-memoirs/K%C3%A4hler-Geometry-of-Loop-Spaces/Chapter/Part-I-Preliminary-concepts/10.2969/msjmemoirs/02301C010)&rbrack;

See also:

* Wikipedia: *[Fréchet manifold](https://en.wikipedia.org/wiki/Fr%C3%A9chet_manifold)*

The embedding into [[diffeological spaces]] is due to

* {#Losik92} [[Mark Losik]], _Fréchet manifolds as diffeologic spaces_, Russian Mathematics 36:5 (1992), 36–42.  English translation: [PDF](https://dmitripavlov.org/scans/losik-frechet-manifolds-as-diffeologic-spaces.pdf).  Russian original: М. В. Лосик, _О многообразиях Фреше как диффеологических пространствах_, Изв. вузов. Матем. (Izv. Vyssh. Uchebn. Zaved. Mat.), 1992, issue 5, 36–42, ([mathnet:ivm4812](http://mi.mathnet.ru/eng/ivm4812))

and reviewed in 

* {#Losik94} [[Mark Losik]], Section 3 of: _Categorical Differential Geometry_. Cah. Topol. G&#233;om. Diff&#233;r. Cat&#233;g., 35(4):274&#8211;290, 1994 ([numdam:CTGDC_1994__35_4_274_0](http://www.numdam.org/item/CTGDC_1994__35_4_274_0))

The preservation of [[mapping spaces]] under this embedding is due to

* {#Waldorf} [[Konrad Waldorf]], _Transgression to Loop Spaces and its Inverse I_ ([arXiv:0911.3212](http://arxiv.org/abs/0911.3212)) 
 

Fr&#233;chet manifold structure on [[jet bundles]] is discussed in

* {#Saunders89} [[David Saunders]], chapter 7 of _The geometry of jet bundles_, London Mathematical Society Lecture Note Series __142__, Cambridge Univ. Press 1989.

* {#DodsonGalanisVassiliou15} C. T. J. Dodson, George Galanis, Efstathios Vassiliou,, p. 109 and section 6.3 of _Geometry in a Fr&#233;chet Context: A Projective Limit Approach_, Cambridge University Press (2015)


[[!redirects Fréchet manifolds]]


[[!redirects Frechet manifold]]
[[!redirects Frechet manifolds]]