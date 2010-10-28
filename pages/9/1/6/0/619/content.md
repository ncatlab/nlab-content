#Contents#
* automatic table of contents goes here
{:toc}


## Definition

A [[full subcategory]] $i : C \hookrightarrow D $ is **reflective** if the inclusion [[functor]] $i$ has a [[adjoint functor|left adjoint]] $T$:

$$
  (T \dashv i) :  C \stackrel{\stackrel{T}{\leftarrow}}{\hookrightarrow}
  D
  \,.
$$

The left adjoint is sometimes called the __reflector__, and a functor which is a reflector (or has a fully faithful right adjoint, which is the same up to equivalence) is called a __reflection__.  Of course, there are dual notions of __coreflective__, __coreflector__, and __coreflection__.

The components of the unit 

$$
  \array{
    & \nearrow &\Downarrow^{\eta}& \searrow^{Id}
    \\
    D &\stackrel{T}{\to}& C &\hookrightarrow & D
  }
$$

of this [[adjunction]] "reflect" each object $d \in D$ into its image $T d$ in the reflective subcategory

$$
  \eta_d : d \to T  d
  \,.
$$

This reflection is sometimes called a [[localization]], although sometimes this term is reserved for the case when the functor $T$ is [[exact functor|left exact]].

If the reflector $T$ is [[faithful functor|faithful]], the reflection is called a [[completion]].


## Characterizations

Given any pair of [[adjoint functor]]s 

$$
  Q^*\dashv Q_* : 
  B
  \stackrel{\overset{Q^*}{\leftarrow}}{\underset{Q_*}{\to}} A
$$ 

the following are equivalent ([[Gabriel-Zisman]]):

1. The [[right adjoint]] $Q_*$ is [[full and faithful functor|fully faithful]]. (In this case $B$ is equivalent to its essential image in $A$ under $Q_*$, a reflective full subcategory of $A$.) 

2. The counit $\varepsilon : Q_* Q^*\to 1_A$ of the [[adjunction]] is a [[natural isomorphism]] of functors.

3. The [[monad]] $(Q^* Q_*,Q^*\varepsilon Q_*,\eta)$ associated to the adjunction is [[idempotent monad|idempotent]].

4. If $S$ is the set of morphisms $s$ in $A$ such that $Q^*(s)$ is invertible in $B$, then $Q^*: A \to B$ realizes $B$ as the [[localization]] of $A$ with respect to the class $S$. 

This is a well-known set of equivalences concerning idempotent monads. The essential point is that a reflective subcategory $i: B \to A$ is [[monadic functor|monadic]], i.e., realizes $B$ as the category of algebras for the monad $i r$ on $A$, where $r: A \to B$ is the reflector. 

See also the related discussion at [[reflective sub-(infinity,1)-category]].

## Special cases

### Exact reflective subcategories

If the reflector (which as a [[left adjoint]] always preserves all [[colimit]]s) in addition preserves finite [[product]]s, the embedding is called _exact_ . If the categories are [[topos]]es then such embeddings are called [[geometric embedding]]s.

In particular, every [[sheaf topos]] is an exact reflective subcategory of a [[category of presheaves]]

$$
  Sh(C) \stackrel{\overset{sheafify}{\leftarrow}}{\hookrightarrow}
  PSh(C)
  \,.
$$

The reflector in that case is the [[sheafification]] functor.


### Complete reflective subcategories

When the unit of the reflector is a [[monomorphism]], a reflective category is often thought of as a full subcategory of *complete* objects in some sense; the reflector takes each object in the ambient category to its completion.  Such reflective subcategories are sometimes called _mono-reflective_.  One similarly has _epi-reflective_ (when the unit is an [[epimorphism]]) and _bi-reflective_ (when the unit is a [[bimorphism]]).


In the last case, note that if the unit is an *iso*morphism, then the inclusion functor is an [[equivalence of categories]], so nontrivial bireflective subcategories can occur only in non-[[balanced categories]].  Also note that 'bireflective' does *not* mean reflective and [[coreflective subcategory|coreflective]].  One sees this term often in discussions of [[concrete categories]] (such as [[topological categories]]) where really something stronger holds: that the reflector lies over the [[identity functor]] on [[Set]].  In this case, one can say that we have a subcategory that is __reflective over $Set$__.



## Properties

A reflective subcategory is always closed under [[limit|limits]] (because the full inclusion is monadic, as noted above), and inherits [[colimit|colimits]] from the larger category by application of the reflector.

+-- {: .un_theorem}
###### Theorem

The weak [[Vop?nka's principle]] is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[limit]]s is a reflective subcategory.

=--

This is [AdamekRosicky, theorem 6.28](#AdamekRosicky)



### Reflective subcategories of cartesian closed categories

In showing that a given category is [[cartesian closed category|cartesian closed]], the following theorem is often useful (cf. A4.3.1 in the [[Elephant]]):

+-- {: .un_theorem}
###### Theorem
If $C$ is cartesian closed, and $D\subseteq C$ is a [[reflective subcategory]], then the reflector $L\colon C\to D$ preserves finite [[products]] if and only if $D$ is an [[exponential ideal]] (i.e. $Y\in D$ implies $Y^X\in D$ for any $X\in C$).  In particular, if $L$ preserves finite products, then $D$ is cartesian closed.
=--


## Examples 

* Complete [[metric space]]s are mono-reflective in metric spaces; the reflector is called _completion_.

* The unital [[ring]]s form a mono-reflective subcategory of possibly nonunital rings; the reflector formally adjoins an [[identity element]].

* The [[category of sheaves]] on a [[site]] $S$ is a reflective subcategory of the category of presheaves on $S$; the reflector is called _[[sheafification]]_. In fact, categories of sheaves are precisely those reflective subcategories of presheaf categories for which the reflector is left [[exact functor|exact]]. This makes the inclusion functor precisely a [[geometric morphism]] of [[topos|topoi]].

* A category of [[concrete presheaves]] inside a [[category of presheaves]] on a [[concrete site]] is a reflective subcategory.

## Property vs structure

Whenever $C$ is a full subcategory of $D$, we can say that objects of $C$ are objects of $D$ with some extra [[property, structure, stuff|property]].  But if $C$ is reflective in $D$, then we can turn this around and (by thinking of the left adjoint as a [[forgetful functor]]) think of objects of $D$ as objects of $C$ with (if we\'re lucky) some [[extra structure]] or (in any case) some [[extra stuff]].

This can always be made to work by brute force, but sometimes there is something insightful about it.  For example, a metric space is a complete metric space equipped with a dense subset.  Or, a possibly nonunital ring is a unital ring equipped with a unital homomorphism to the ring of integers.


## Related concepts

* **reflective subcategory** / [[reflective sub-(∞,1)-category]]

* [[coreflective subcategory]]

## References

* [[Jiri Adamek]], [[Ji?í Rosický]], _Locally presentable and accessible categories_ London Mathematical Society Lecture Note Series 189
{#AdamekRosicky}

[[!redirects reflector]]
[[!redirects reflectors]]
[[!redirects reflection]]
[[!redirects reflections]]
[[!redirects reflective subcategories]]
[[!redirects coreflector]]
[[!redirects coreflectors]]
[[!redirects coreflection]]
[[!redirects coreflections]]
[[!redirects coreflective subcategory]]
[[!redirects coreflective subcategories]]
