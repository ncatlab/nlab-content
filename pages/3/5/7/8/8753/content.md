
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

For $\mathcal{C}$ an [[(∞,1)-category]], a [[simplicial object]] in $\mathcal{C}$ is an [[(∞,1)-functor]]

$$
  X \colon \Delta^{op} \to \mathcal{C}
$$

from the [[opposite category]] of the [[simplex category]] into $\mathcal{C}$.


The $(\infty,1)$-category of simplicial objects in $\mathcal{C}$ and morphisms between them is the [[(∞,1)-category of (∞,1)-functors]]

$$
  \mathcal{C}^{\Delta^{op}}
  = 
  Func_\infty(\Delta^{op}, \mathcal{C})
  \,.
$$

=--

For instance ([Lurie, def. 6.1.2.2](#Lurie)).

+-- {: .num_remark}
###### Remark

For $\mathcal{C}$ a [[1-category]] a simplicial object in $\mathcal{C}$ is a [[simplicial object]] in the traditional sense of [[category theory]].

=--


+-- {: .num_defn}
###### Definition

A _cosimplicial object_ in $\mathcal{C}$ is a simplicial object in the [[opposite category]] $\mathcal{C}^{op}$.

=--

## Properties

### Powering over simplicial sets
 {#Powering}

Assume that $\mathcal{C}$ has all [[(∞,1)-limits]]. 
The following is a model for the [[powering]] of simplicial objects in $\mathcal{C}$ by simplicial sets.

+-- {: .num_defn #PoweringByLimitOverCategoryOfSimplices}
###### Definition

Let $\mathcal{C} \in QCat \hookrightarrow sSet$ be an [[(∞,1)-category]] incarnated as a [[quasi-category]], and let $X \colon \Delta^{op} \to \mathcal{C}$ be a simplicial object. Then for $K \in sSet$ any [[simplicial set]], write

$$
  X[K] \colon \Delta_{/K}^{op} \to \Delta^{op} \stackrel{X}{\to} \mathcal{C}
$$

for the the composite [[(∞,1)-functor]] of $X_\bullet$ with the projection from (the [[opposite category]] of) the [[category of simplices]] of $K$, and write

$$
  X(K) 
    \colon 
  \underset{\leftarrow}{\lim}
  \left(
    \Delta_{/K}^{op} \to \Delta^{op} \stackrel{X}{\to} \mathcal{C}
  \right)
$$

for the [[(∞,1)-limit]] over it (if it exists).

=--

This is discussed in ([Lurie HTT 4.2.3, notation 6.1.2.5](#Lurie)). See also around ([Lurie 2, notation 1.1.7](#LurieGood)).

+-- {: .num_remark}
###### Remark

The inclusion $\Delta_{/K}^{nd} \hookrightarrow \Delta_{K}$ of the [[full subcategory]] on non-degenerate simplicies is a [[homotopy cofinal functor]] (as discussed there). Therefore the $(\infty,1)$-limit in def. \ref{PoweringByLimitOverCategoryOfSimplices} may equivalently be taken over this category of non-degenerate simplices.

=--

+-- {: .num_example}
###### Example

For $K = \Delta^1 \coprod_{\Delta^0} \Delta^1$ the simplicial set consisting of two consecutive edges, we have for $X_\bullet \in \mathcal{C}^{\Delta^\bullet}$ that

$$
  X(K) \simeq X_1 \underset{X_0}{\times} X_1
$$

is the [[homotopy fiber product]] in

$$
  \array{
    && X(K)
    \\
    & \swarrow && \searrow
    \\
    X_1 &&&& X_1
    \\
    & {}_{\mathllap{\partial_1}}\searrow && \swarrow_{\mathrlap{\partial_0}}
    \\
    && X_0
  }
  \,.
$$

=--

+-- {: .num_example}
###### Example

For $K = \Delta^n$ itself an $n$-[[simplex]], for some $n \in \mathbb{N}$ the powering reduces to evaluation on that simplex:

$$
  X(\Delta^n) \simeq X_n
  \,.
$$

This is because the [[category of non-degenerate simplices]] of an $n$-simplex has a [[terminal object]] (namely that $n$-simplex itself), and so its [[opposite category]] has an [[initial object]] and the $(\infty,1)$-limit over a [[diagram]] with initial object is given by evaluation at that initial object. 

=--

+-- {: .num_remark #EquivalenceOfConeCategoriesAndLimits}
###### Remark

For $X_\bullet \in \mathcal{C}^{\Delta^{op}}$ and $K \to K'$ the following are equivalent

1. the induced morphism of cone $(\infty,1)$-categoris $\mathcal{C}_{X[K]} \to \mathcal{C}_{X[K']}$ is an [[equivalence of (∞,1)-categories]];

1. the induced morphism of [[(∞,1)-limits]] $X(K) \to X(K')$ is an [[equivalence in an (∞,1)-category|equivalence]].

=--

(The first perspective is used in ([Lurie](#Lurie)), the second in ([Lurie2](#Lurie2)).)

+-- {: .proof}
###### Proof

In one direction: the limit is the [[terminal object in an (∞,1)-category|terminal object]] in the cone category, and so is preserved by equivalences of cone categories. (This direction appears as ([Lurie, prop. 4.1.1.8](#Lurie))).  Conversely, the limits is the object representing cones, and hence an equivalence of limits induces an equivalence of cone categories.

=--


+-- {: .num_prop #SlicingOverPoweringOfSimplicialObjects}
###### Proposition

Let $X \colon \Delta^{op} \to \mathcal{C}$ be a simplicial object which is a [[groupoid object in an (∞,1)-category]].

If $K \to K'$ is a morphism in [[sSet]] which is a [[weak homotopy equivalence]] and a [[bijection]] on [[vertices]], then the induced morphism on [[slice-(∞,1)-categories]]

$$
  \mathcal{C}_{/X[K]}
  \to 
  \mathcal{C}_{/X[K']}
$$

is an [[equivalence of (∞,1)-categories]] (a [[weak equivalence]] in the [[model structure for quasi-categories]]).

Equivalently, by remark \ref{SlicingOverPoweringOfSimplicialObjects}, we have an equivalence

$$
  X(K) \to X(K')
  \,.
$$

=--

This is ([Lurie, prop. 6.1.2.6](#Lurie)).

### Cohesion

If $\mathcal{C} = \mathbf{H}$ is an [[(∞,1)-topos]] then $\mathcal{C}^{\Delta^{op}}$ is a [[cohesive (∞,1)-topos]] over $\mathbf{H}$. For more see at _[cohesive (∞,1)-topos - Examples - Simplicial objects](cohesive+%28infinity%2C1%29-topos#SimplicialObjctsInACohesiveTopos)_.

### Internal language

If $\mathcal{C}$ is a [[locally cartesian closed (∞,1)-category]] whose [[internal language]] is [[homotopy type theory]], then the internal language of $\mathcal{C}^{\Delta^{op}}$ is that homotopy type theory equipped with the axioms for a [[linear interval]] object. (...)

### Geometric realization and filtering

The _[[geometric realization]]_ ${\vert X_\bullet \vert}$ of a simplicial object $X_\bullet$  is, if it exists, the [[(∞,1)-colimit]] over the corresponding [[(∞,1)-functor]] $X_\bullet \;\colon\; \Delta^{op} \to \mathcal{C}$. 

$$
  {\vert X_\bullet \vert}
  \coloneqq
  \underset{\longrightarrow}{\lim}_n X_n
  \,.
$$

Hence the geometric realization of a cosimplicial object $\Delta^{op} \to \mathcal{C}^{op}$ -- called its [[totalization]] -- is the [[(∞,1)-limit]] over $\Delta \to \mathcal{C}$.

The [[geometric realization]] of the [[simplicial skeleta]] of $X_\bullet$

$$
  {\vert sk_0 X_\bullet \vert} \to {\vert sk_1 X_\bullet \vert} \to {\vert sk_2 X_\bullet \vert} \to \cdots
  \,.
$$

constitutes a [[filtered object in an (infinity,1)-category|filtering]] on the [[geometric realization]] of $X_\bullet$ itself

$$
  {\vert X_\bullet \vert}
  \simeq
  \underset{\longrightarrow}{\lim}_n {\vert sk_n X_\bullet \vert}
  \,.
$$

If $\mathcal{C}$ is a [[stable (∞,1)-category]], then the 
the corresponding [[spectral sequence of a filtered stable homotopy type]] is the [[spectral sequence of a simplicial stable homotopy type]].

### $\infty$-Dold-Kan correspondence

The following statement is the _[[infinity-Dold-Kan correspondence]]_.

+-- {: .num_prop }
###### Proposition

Let $\mathcal{C}$ be a [[stable (∞,1)-category]]. Then the [[(∞,1)-categories]] of non-negatively graded [[sequential diagram|sequences]] in $C$ is [[equivalence of (∞,1)-categories|equivalent]] to the [[(∞,1)-category]] of [[simplicial objects in an (∞,1)-category]] in $\mathcal{C}$

$$
  Fun(N(\mathbb{Z}_{\geq 0}), C)
  \simeq
  Fun(N(\Delta)^{op}, C)  
  \,.
$$

Under this equivalence, a [[simplicial object]] $X_\bullet$ is sent to the [[sequential diagram|sequence]] of [[geometric realizations]] ([[(∞,1)-colimits]]) of its [[simplicial skeleta]]

$$
  {\vert sk_0 X_\bullet \vert} \to {\vert sk_1 X_\bullet \vert} \to {\vert sk_2 X_\bullet \vert} \to \cdots
  \,.
$$

This constitutes a [[filtered object in an (infinity,1)-category|filtering]] on the [[geometric realization]] of $X_\bullet$ itself

$$
  {\vert X_\bullet \vert}
  \simeq
  \underset{\longrightarrow}{\lim}_n {\vert sk_n X_\bullet \vert}
  \,.
$$

=--

([[Higher Algebra|Higher Algebra, theorem 1.2.4.1]])


## Examples

### Internal category objects

* A [[pre-category object in an (∞,1)-category]] $\mathcal{C}$ is a simplicial object which satisfies the [[Segal conditions]];

* a [[category object in an (∞,1)-category]] is a pre-category object which also satisfies the [[univalence axiom]];

* a [[groupoid object in an (∞,1)-category]] is a category object all of whose [[morphisms]] are [[equivalences]] under composition.


## Related concepts

* [[simplicial object]]

  * [[simplicial set]]

* [[semi-simplicial object]]

  * [[semisimplicial set]]

* [[simplicial homotopy theory]]

* [[homotopy Kan fibration]]


## Reference

Simplicial objects in general [[(∞,1)-categories]] are discussed in 

* [[Jacob Lurie]], section 6.1.2 of _[[Higher Topos Theory]]_
 {#Lurie}

Related discussion is also in

* [[Jacob Lurie]], _[[(∞,2)-Categories and the Goodwillie Calculus]]_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 {#LurieGood}

Simplicial obects in [[stable (∞,1)-categories]] are discussed in

* [[Jacob Lurie]], section 1.2.4 of _[[Higher Algebra]]_


[[!redirects simplicial objects in an (∞,1)-category]]
[[!redirects simplicial objects in an (infinity,1)-category]]

[[!redirects simplicial object in an (∞,1)-category]]

[[!redirects cosimplicial object in an (∞,1)-category]]
[[!redirects cosimplicial objects in an (∞,1)-category]]

[[!redirects cosimplicial object in an (infinity,1)-category]]
[[!redirects cosimplicial objects in an (infinity,1)-category]]

