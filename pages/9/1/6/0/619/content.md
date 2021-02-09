+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

A _reflective subcategory_ is a [[full subcategory]]

$$
  C \hookrightarrow D
$$

such that [[objects]] $d$ and [[morphisms]] $f \colon d \to d'$ in $D$ have "reflections" $T d$ and $T f \colon T d \to T d'$ in $C$. Every object in $D$ looks at its own reflection via a morphism $d \to Td$ and the reflection of an object $c \in C$ is equipped with an [[isomorphism]] $T c \cong c$. 

A canonical example is the inclusion 

$$
  \mathrm{Ab} \hookrightarrow \mathrm{Grp}
$$

of the [[category of abelian groups]] into the [[category of groups]], whose reflector is the operation of _[[abelianization]]_.

A useful property of reflective subcategories is that the inclusion $C \hookrightarrow D$ [[created limit|creates all limits]] of $D$ and $C$ has all [[colimits]] which $D$ admits.



## Definition

+-- {: .num_defn }
###### Definition

A [[full subcategory]] $i : C \hookrightarrow D $ is **reflective** if the inclusion [[functor]] $i$ has a [[left adjoint]] $T$:

$$
  (T \dashv i) :  C \stackrel{\stackrel{T}{\leftarrow}}{\hookrightarrow}
  D
  \,.
$$

=--

The left adjoint is sometimes called the __reflector__, and a functor which is a reflector (or has a fully faithful right adjoint, which is the same up to equivalence) is called a __reflection__.  Of course, there are dual notions of __[[coreflective subcategory]]__, __coreflector__, and __coreflection__.


+-- {: .num_remark #NonFullReflections}
###### Remark

A few sources (such as [[Categories Work]]) do not require a reflective subcategory to be full.  However, in light of the fact that non-full subcategories are not [[principle of equivalence|invariant under equivalence]], consideration of non-full reflective subcategories seems of limited usefulness.  The general consensus among category theorists nowadays seems to be that "reflective subcategory" implies fullness.  Examples for non-full subcategories and their behaviour can be found in a [TAC paper](http://www.tac.mta.ca/tac/volumes/30/41/30-41.pdf) by Ad&#225;mek and Rosick&#253;.

=--


+-- {: .num_remark }
###### Remark

The components of the [[unit of an adjunction|unit]]

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

=--

This reflection is sometimes called a _[[localization]]_ (due to [this Prop.](reflective+localization#ReflectiveSubcategoriesAreLocalizations) at _[[reflective localization]]_), although sometimes this term is reserved for the case when the functor $T$ is [[exact functor|left exact]].

+-- {: .num_defn }
###### Definition

If the reflector $T$ is [[faithful functor|faithful]], the reflection is called a **[[completion]]**.

=--


## Characterizations


+-- {: .num_prop #CharacterizationByLocalization}
###### Proposition
**(equivalent characterizations)**

Given any pair of [[adjoint functors]]

$$
  (Q^*\dashv Q_*)
  \;:\; 
  B
    \underoverset
      {\underset{Q_*}{\longrightarrow}}
      {\overset{Q^*}{\longleftarrow}} 
      {\bot}
  A
$$ 

the following are equivalent:

1. The [[right adjoint]] $Q_*$ is [[full and faithful functor|fully faithful]]. (In this case $B$ is equivalent to its [[essential image]] in $A$ under $Q_*$, a full [[reflective subcategory]] of $A$.) 

2. The [[counit of an adjunction|counit]] $\varepsilon : Q^* Q_*\to 1_B$ of the [[adjunction]] is a [[natural isomorphism]] of functors.

3. The [[monad]] $(Q_* Q^*,Q_*\varepsilon Q^*,\eta)$ associated with the adjunction is [[idempotent monad|idempotent]], the right adjoint $Q_*$ is [[conservative functor|conservative]], and the left adjoint $Q^*$ is [[essentially surjective functor|essentially surjective on objects]].

4. If $S$ is the set of morphisms $s$ in $A$ such that $Q^*(s)$ is an [[isomorphism]] in $B$, then $Q^* \colon A \to B$ realizes $B$ as the (nonstrict) [[localization]] of $A$ with respect to the class $S$. 

=--

This is originally due to ([Gabriel-Zisman 67, prop. 1.3, page 7](#GabrielZisman67)). 

+-- {: .proof}
###### Proof

The equivalence of 1) and 2) is [this prop.](adjoint+functor#FullyFaithfulAndInvertibleAdjoints). The equivalence of 1) and 3) is [this Prop.](idempotent+monad#EquivalentConditions).

For the last item see at _[[reflective localization]]_. 

=--

This is a well-known set of equivalences concerning [[idempotent monads]]. The essential point is that a reflective subcategory $i: B \to A$ is [[monadic functor|monadic]], i.e., realizes $B$ as the category of [[algebra over a monad|algebras for the monad]] $i r$ on $A$, where $r: A \to B$ is the reflector. 

See also the related discussion at [[reflective sub-(infinity,1)-category]].

## Special cases

### Exact reflective subcategories
 {#ExactReflectiveSubcategories}

If the reflector (which as a [[left adjoint]] always preserves all [[colimit]]s) in addition preserves [[finite limits]], then the embedding is called _exact_. If the categories are [[topos]]es then such embeddings are called [[geometric embedding]]s.

In particular, every [[sheaf topos]] is an exact reflective subcategory of a [[category of presheaves]]

$$
  Sh(C) \stackrel{\overset{sheafify}{\leftarrow}}{\hookrightarrow}
  PSh(C)
  \,.
$$

The reflector in that case is the [[sheafification]] functor. 

+-- {: .num_theorem}
######Theorem 

If $X$ is a reflective subcategory of a [[cartesian closed category]], then it is an [[exponential ideal]] if and only if its [[reflector]] $D\to C$ preserves [[finite product]].

In particular, $C$ is then also cartesian closed.  

=--

This appears for instance as ([Johnstone, A4.3.1](#Johnstone)). See also at _[[reflective subuniverse]]_.

So in particular if $C$ is an exact reflective subcategory of a cartesian closed category $D$, then $C$ is an [[exponential ideal]] of $D$. 

See [[Day's reflection theorem]] for a more general statement and proof. 




### Complete reflective subcategories

When the unit of the reflector is a [[monomorphism]], a reflective category is often thought of as a full subcategory of *complete* objects in some sense; the reflector takes each object in the ambient category to its completion.  Such reflective subcategories are sometimes called _mono-reflective_.  One similarly has _epi-reflective_ (when the unit is an [[epimorphism]]) and _bi-reflective_ (when the unit is a [[bimorphism]]).


In the last case, note that if the unit is an *iso*morphism, then the inclusion functor is an [[equivalence of categories]], so nontrivial bireflective subcategories can occur only in non-[[balanced categories]].  Also note that 'bireflective' here does *not* mean reflective and [[coreflective subcategory|coreflective]].  One sees this term often in discussions of [[concrete categories]] (such as [[topological categories]]) where really something stronger holds: that the reflector lies over the [[identity functor]] on [[Set]].  In this case, one can say that we have a subcategory that is __reflective over $Set$__.

### Accessible reflective subcategories
 {#AccessibleReflectiveSubcategories}

+-- {: .num_defn #AccessibleReflection}
###### Definition

A reflection 

$$
  \mathcal{C}
  \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}}
  \mathcal{D}
$$

is called **accessible** if $\mathcal{D}$ is an [[accessible category]] and  the reflector $R\circ L \colon \mathcal{D} \to \mathcal{D}$ is an [[accessible functor]].

=--

+-- {: .num_prop}
###### Proposition

A reflective subcategory $\mathcal{C} \hookrightarrow \mathcal{D}$ of an [[accessible category]] is accessible, def. \ref{AccessibleReflection}, precisely if $\mathcal{C}$ is an [[accessible category]].

=--

In this explicit form this appears as ([Lurie, prop. 5.5.1.2](#Lurie)).
From ([Adamek-Rosick&#253;](#AdamekRosicky)) the "only if"-direction follows immediately from 2.53  there (saying that an accessibly embedded subcategory of an accessible category is accessible iff it is cone-reflective), while the "if"-direction follows immediately from 2.23 (saying any left or right adjoint between accessible categories is accessible).


## Properties

### General

A reflective subcategory is always closed under [[limit|limits]] which exist in the ambient category (because the full inclusion is monadic, hence creates limits, as noted above), and inherits [[colimit|colimits]] from the larger category by application of the reflector [Riehl, Prop 4.5.15](#Riehl). In particular, if the ambient category is complete and cocomplete then so is the reflective subcategory.

A morphism in a reflective subcategory is monic iff it is monic in the ambient category. A reflective subcategory of a well-powered category is well-powered. 

### As Eilenberg-Moore category of the idempotent monad
 {#AsEilenbergMooreCategory}

+-- {: .num_prop}
###### Proposition

Any reflective subcategory is recovered as the [[Eilenberg-Moore category]] of [[algebra over a monad|algebras]] over its associated [[idempotent monad]].

=--

See for instance ([Borceux, vol 2, cor. 4.2.4](#Borceux)) and see at _[idempotent monad -- Properties -- Algebras for an idempotent monad and localization](idempotent+monad#AlgebrasForAnIdempotentMonad)_.

### Reflective subcategories of locally presentable categories

Both the weak and strong versions of [[Vopěnka's principle]] are equivalent to fairly simple statements concerning reflective subcategories of locally presentable categories: 

+-- {: .num_theorem}
###### Theorem

The weak [[Vopěnka's principle]] is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[limit]]s is a reflective subcategory.

=--

This is [AdamekRosicky, theorem 6.28](#AdamekRosicky)

+-- {: .num_theorem}
###### Theorem
The strong [[Vopěnka's principle]] is equivalent to:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[limit]]s is a reflective subcategory; further on, $D$ is then also locally presentable.
=--
(Remark after corollary 6.24 in [Adamek-Rosicky book](#AdamekRosicky)).

### Reflective subcategories of cartesian closed categories
 {#ReflectiveSubcategoriesOfCartesianClosedCategotries}

In showing that a given category is [[cartesian closed category|cartesian closed]], the following theorem is often useful (cf. A4.3.1 in the [[Elephant]]):

+-- {: .num_theorem}
###### Theorem
If $C$ is cartesian closed, and $D\subseteq C$ is a [[reflective subcategory]], then the reflector $L\colon C\to D$ preserves finite [[products]] if and only if $D$ is an [[exponential ideal]] (i.e. $Y\in D$ implies $Y^X\in D$ for any $X\in C$).  In particular, if $L$ preserves finite products, then $D$ is cartesian closed.
=--

### Reflective and coreflective subcategories

+-- {: .num_theorem}
###### Theorem

A subcategory of a [[category of presheaves]] $[A^{op}, Set]$ which is both reflective and coreflective is itself a category of presheaves $[B^{op}, Set]$, and the inclusion is induced by a functor $A \to B$.

=--

This is shown in ([BashirVelebil](#BashirVelebil)).

### Property vs structure

Whenever $C$ is a full subcategory of $D$, we can say that objects of $C$ are objects of $D$ with some extra [[property, structure, stuff|property]].  But if $C$ is reflective in $D$, then we can turn this around and (by thinking of the left adjoint as a [[forgetful functor]]) think of objects of $D$ as objects of $C$ with (if we\'re lucky) some [[extra structure]] or (in any case) some [[extra stuff]].

This can always be made to work by brute force, but sometimes there is something insightful about it.  For example, a metric space is a complete metric space equipped with a dense subset.  Or, an [[integral domain]] is a [[field]] equipped with numerator and denominator functions.




## Examples 
 {#Examples}

+-- {: .num_example }
###### Example

Complete [[metric spaces]] are mono-reflective in metric spaces; the reflector is called _completion_.

=--


+-- {: .num_example }
###### Example

The [[category of sheaves]] on a [[site]] $S$ is a reflective subcategory of the [[category of presheaves]] on $S$; the reflector is called _[[sheafification]]_. In fact, categories of sheaves are precisely those accessible reflective subcategories, def. \ref{AccessibleReflection},  of presheaf categories for which the reflector is left [[exact functor|exact]]. This makes the inclusion functor precisely a [[geometric inclusion]] of [[toposes]].

=--

+-- {: .num_example }
###### Example

A category of [[concrete presheaves]] inside a [[category of presheaves]] on a [[concrete site]] is a reflective subcategory.

=--


+-- {: .num_example }
###### Example

In a [[recollement]] situation, we have several reflectors and coreflectors. We have a reflective and coreflective subcategory $i_*: A' \hookrightarrow A$ with reflector $i^*$ and coreflector $i^!$. The functor $j^*$ is both a reflector for the reflective subcategory $j_*: A'' \hookrightarrow A$, and a coreflector for the coreflective subcategory $j_!: A'' \hookrightarrow A$.

=--

+-- {: .num_example #TheReflectiveSubcategoriesOfSet}
###### Example

Assuming classical logic, the category [[Set]] has exactly three reflective (and [[replete subcategory|replete]]) subcategories: the full subcategory containing all [[singleton set|singleton sets]]; the full subcategory containing all [[subsingletons]]; and $Set$ itself.

In [[constructive mathematics]], there are potentially more reflective subcategories, for instance the subcategory of $j$-sheaves for any [[Lawvere-Tierney topology|Lawvere?Tierney topology]] on $Set$.

=--

+-- {: .num_example #AffineVarieties}
###### Example

The category of [[affine schemes]] is a reflective subcategory of the category of [[schemes]], with the reflector given by $X \mapsto Spec \Gamma(X,\mathcal{O}_X)$.

The generalization of this example to [[homotopy theory]] is discussed at _[[function algebras on infinity-stacks]]_. The analogue in [[noncommutative algebraic geometry]] is in ([Rosenberg 98, prop 4.4.3](#Rosenberg98)). 

=--

+-- {: .num_example #NonUnitalRings}
###### (Counter)Example
The non-full inclusion of unital [[rings]] into non-unital rings has a left adjoint (with monic units), whose reflector formally adjoins an [[identity element]].  However, we do not call it a reflective subcategory, because the "inclusion" is not full; see remark \ref{NonFullReflections}.
=--

+-- {: .num_remark #RemarkOnNonUnitalRings}
###### Remark

Notice that for $R \in Ring$ a ring with unit, its reflection $L R$ in the above example is not in general isomorphic to $R$, but is much larger. 
But an object in a reflective subcategory is necessarily isomorphic to its image under the reflector only if the reflective subcategory is full.  While the inclusion $\mathbf{Ring} \hookrightarrow \mathbf{Ring}$' does have a [[left adjoint]] (as any [[forgetful functor]] between varieties of algebras, by the [[adjoint lifting theorem]]), this inclusion is not full (an arrow in $\mathbf{Ring}$' need not preserve the identity).  

=--

+-- {: .num_example #CategoryOfCategories}
###### Example

The subcategory
$$ Cat \hookrightarrow sSet$$
of the [[category of categories]] into the [[sSet|category of simplical sets]] is a reflective subcategory [Riehl, example 4.5.14 (vi)](#Riehl). The reflection is given by the [[homotopy category|homotopy category functor]]. This implies that [[Cat]] is complete and cocomplete because it inherits all limits and colimits from [[sSet]].
=--

+-- {: .num_example #ModelsOfALawvereTheory}
###### Example

For any [[Lawvere theory]] $T$, its category of models is the category
$$Prod(T, Set)$$
of product preserving functors into $Set$ and natural transformations between them. The inclusion 
$$Prod(T, Set) \hookrightarrow [T, Set]$$
is a reflective subcategory [Buckley, theorem 5.2.1](#Buckley). Therefore, because $[T,Set]$ is complete and cocomplete (limits and colimits are computed pointwise), so is $Prod(T, Set)$. This implies that many familar algebraic categories such as [[Grp]], [[Mon]], [[Ring]], etc. are complete and cocomplete as a special case.
=--

## Related concepts

* [[localization]], [[locally presentable category]]

* [[reflective localization]]

* [[Quillen reflection]], [[left Bousfield localization]]

* [[reflective sub-(infinity,1)-category]]

* [[adjoint cylinder]], describing the situation when the reflector has a further left adjoint

* [[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes]]


## References

* {#GabrielZisman67} [[Pierre Gabriel]], [[Michel Zisman]], _[[Calculus of fractions and homotopy theory]]_, Springer 1967 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf))

* {#Borceux} [[Francis Borceux]], _[[Handbook of Categorical Algebra]]_, vol.1, p. 196.

* {#AdamekRosicky} [[Jiri Adamek|Jiri Adamek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_ London Mathematical Society Lecture Note Series 189
 

* Springer eom: [reflective subcategory](http://eom.springer.de/r/r080550.htm)


* cf. the notion of $Q^\circ$-category in the entry [[Q-category]]

* {#Riehl} [[Emily Riehl]], _[[Category Theory in Context]], p. 142, Courier Dover Publications 2017 ([pdf](http://www.math.jhu.edu/~eriehl/context.pdf))

* {#Buckley} Mitchell Buckley, _Lawvere Theories, 2008 [pdf](http://web.science.mq.edu.au/~street/MitchB.pdf)

The relation of exponential ideals to [[reflective subcategories]] is discussed in section A4.3.1 of 

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]]_
  

Reflective and coreflective subcategories of presheaf categories are discussed in

* {#BashirVelebil}R. Bashir, J. Velebil, _Simultaneously reflective and coreflective subcategories of presheaves_, Theory and  Applications of Categories, Vol 10. No. 16. (2002) ([pdf](http://www.emis.de/journals/TAC/volumes/10/16/10-16.pdf)).

Related discussion of [[reflective sub-(∞,1)-categories]] is in 

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_
 

The example of affine schemes in [[noncommutative algebraic geometry]] is in 

* {#Rosenberg98} [[Alexander Rosenberg]], _Noncommutative schemes_, Comp. Math. 112, 93&#8211;125 (1998)


[[!redirects reflector]]
[[!redirects reflectors]]


[[!redirects reflective subcategories]]
[[!redirects reflexive subcategory]]
