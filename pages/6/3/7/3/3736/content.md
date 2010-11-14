

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

An object in a [[model category]] is fibrant if all morphisms into it have extensions along acyclic cofibrations. An **algebraic fibrant object** is a fibrant object equipped with a _choice_ of such extensions.

Under mild conditions, the category $Alg C$ of algebraic fibrant objects in a model category $C$ forms itself naturally a model category which is [[Quillen equivalence|Quillen equivalent]] to $C$, and in which all objects are fibrant.  Notably, $Alg C$ is always a [[category of fibrant objects]].


## Definition

+-- {: .un_defn}
###### Definition

Let $C$ be a [[cofibrantly generated model category]] such that 
all acyclic cofibrations are [[monomorphism]]s. 

Choose a set $\{A_j \to B_j\}_{j \in J}$ of acyclic cofibrations such that an object $X \in C$ is fibrant precisely if it has the [[right lifting property]] against these morphisms.

An **algebraic fibrant object** in $C$ is a fibrant object of $C$ together with a choice of lifts ("fillers") $\sigma_j : B_j \to X$ in

$$
  \array{
    A_j &\to& X
    \\
    \downarrow & \nearrow_{\mathrlap{\sigma_j}}
    \\
    B_j
  }
$$

for each morphism $A_j \to X$, $j \in J$. 

Write $ALg C$ for the category whose objects are algebraic fibrant objects in $C$ and whose morphisms are morphisms in $C$ that respect the chosen lifts.

=--

+-- {: .un_remark}
###### Remark

The set $J$ can always be taken to be that of all generating acyclic cofibrations. But often there are smaller subsets that still characterize all fibrant objects.

=--

+-- {: .un_theorem}
###### Theorem

The [[forgetful functor]] [[adjunction]]

$$
  (F \dashv U) : Alg C \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C 
$$

induces the [[transferred model structure]] on $Alg C$: the fibrations
and weak equivalences in $Alg C$ are those of the underlying morphisms in $C$.

In particular, every object in $Alg C$ is fibrant.

The [[Quillen adjunction]] $(F \dashv U)$ is a [[Quillen equivalence]].


=--

+-- {: .proof}
###### Proof

This is theorem 2.18

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))


=--

Note that since fibrations in $Alg C$ are created in $C$, and any algebraically fibrant object is, in particular, fibrant, every object in the model category $Alg C$ is fibrant.  Thus almost any model category is equivalent to one in which all objects are fibrant.  However, in general not all objects in $Alg C$ will be cofibrant, even if this was true in $C$ itself.

## Examples

### Algebraic $\infty$-groupoids {#AlgebaicHigherCategories}

The standard [[model structure on simplicial sets]] $sSet_{Quillen}$ models the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoid]]s: its fibrant objects are precisely the [[Kan complex]]es. But a Kan complex is a model for an $\infty$-groupoid in which composites and inverses of [[k-morphism]]s are only guaranteed to exist, but are not specifically _chosen_ .

An algebraic fibrant object in $sSet_{Quillen}$ is a [[Kan complex]] with a chosen filler for each [[horn]]: an **[[algebraic Kan complex]]** (see [[simplicial T-complex]] for a related but much stricter notion). This means precisely that all possible composites and all possible inverses are chosen. So the Quillen equivalence

$$
  sSet_{Quillen} \stackrel{\leftarrow}{\to} Alg sSet_{Quillen} 
$$

induces an equivalence from an [[algebraic definition of higher category|algebraic definition of ∞-groupoids]] to a [[geometric definition of higher categories|geometric definition]].

### Algebraic $(\infty,1)$-categories

Similarly, the [[model structure for quasi-categories]] $sSet_{Joyal}$ models [[(∞,1)-categories]]: its fibrant objects are precisely the [[quasi-categories]]: an **[[algebraic quasi-category]]**. Again, these form a model for $(\infty,1)$-categories in which composition is only a relation, not an operation.

But equipping a quasi-category with the structure of an algebraic fibrant object precisely means choosing such composites. Accordingly, the [[Quillen equivalence]]

$$
  sSet_{Joyal} \stackrel{\leftarrow}{\to} Alg sSet_{Joyal} 
$$

establishes an equivalence of an algebraic with the standard geometric model for $(\infty,1)$-categories.

## References

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))

* [[Thomas Nikolaus]] Talk on _Algebraic models for higher categories_ ([here](http://www.math.uni-hamburg.de/home/nikolaus/AlgMod.pdf))

