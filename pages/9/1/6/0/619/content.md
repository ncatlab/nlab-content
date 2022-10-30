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
=--
=--


#Contents#
* table of contents
{:toc}


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

The left adjoint is sometimes called the __reflector__, and a functor which is a reflector (or has a fully faithful right adjoint, which is the same up to equivalence) is called a __reflection__.  Of course, there are dual notions of __coreflective__, __coreflector__, and __coreflection__.


+-- {: .num_remark #NonFullReflections}
###### Remark

A few sources (such as [[Categories Work]]) do not require a reflective subcategory to be full.  However, in light of the fact that non-full subcategories are not [[principle of equivalence|invariant under equivalence]], consideration of non-full reflective subcategories seems of limited usefulness.  The general consensus among category theorists nowadays seems to be that "reflective subcategory" implies fullness.

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

This reflection is sometimes called a [[localization]], although sometimes this term is reserved for the case when the functor $T$ is [[exact functor|left exact]].

+-- {: .num_defn }
###### Definition

If the reflector $T$ is [[faithful functor|faithful]], the reflection is called a **[[completion]]**.

=--


## Characterizations


+-- {: .num_prop #CharacterizationByLocalization}
###### Proposition

Given any pair of [[adjoint functor]]s 

$$
  Q^*\dashv Q_* : 
  B
  \stackrel{\overset{Q^*}{\leftarrow}}{\underset{Q_*}{\to}} A
$$ 

the following are equivalent:

1. The [[right adjoint]] $Q_*$ is [[full and faithful functor|fully faithful]]. (In this case $B$ is equivalent to its essential image in $A$ under $Q_*$, a reflective full subcategory of $A$.) 

2. The [[counit of an adjunction|counit]] $\varepsilon : Q^* Q_*\to 1_A$ of the [[adjunction]] is a [[natural isomorphism]] of functors.

3. The [[monad]] $(Q^* Q_*,Q^*\varepsilon Q_*,\eta)$ associated to the adjunction is [[idempotent monad|idempotent]].

4. If $S$ is the set of morphisms $s$ in $A$ such that $Q^*(s)$ is invertible in $B$, then $Q^*: A \to B$ realizes $B$ as the (nonstrict) [[localization]] of $A$ with respect to the class $S$. 

=--

This is due to [[Gabriel-Zisman]].

This is a well-known set of equivalences concerning idempotent monads. The essential point is that a reflective subcategory $i: B \to A$ is [[monadic functor|monadic]], i.e., realizes $B$ as the category of algebras for the monad $i r$ on $A$, where $r: A \to B$ is the reflector. 

See also the related discussion at [[reflective sub-(infinity,1)-category]].

## Special cases

### Exact reflective subcategories
 {#ExactReflectiveSubcategories}

If the reflector (which as a [[left adjoint]] always preserves all [[colimit]]s) in addition preserves [[finite limits]], then the embedding is called _exact_ . If the categories are [[topos]]es then such embeddings are called [[geometric embedding]]s.

In particular, every [[sheaf topos]] is an exact reflective subcategory of a [[category of presheaves]]

$$
  Sh(C) \stackrel{\overset{sheafify}{\leftarrow}}{\hookrightarrow}
  PSh(C)
  \,.
$$

The reflector in that case is the [[sheafification]] functor. 

+-- {: .num_thm}
######Theorem 

If $X$ is a reflective subcategory of a [[cartesian closed category]], then it is an [[exponential ideal]] if and only if its [[reflector]] $D\to C$ preserves finite [[product]]s.

In particular, $C$ is then also cartesian closed.  

=--

This appears for instance as ([Johnstone, A4.3.1](#Johnstone)).

So in particular if $C$ is an exact reflective subcategory of a cartesian closed category $D$, then $C$ is an [[exponential ideal]] of $D$. 

See [[Day's reflection theorem]] for a more general statement and proof. 




### Complete reflective subcategories

When the unit of the reflector is a [[monomorphism]], a reflective category is often thought of as a full subcategory of *complete* objects in some sense; the reflector takes each object in the ambient category to its completion.  Such reflective subcategories are sometimes called _mono-reflective_.  One similarly has _epi-reflective_ (when the unit is an [[epimorphism]]) and _bi-reflective_ (when the unit is a [[bimorphism]]).


In the last case, note that if the unit is an *iso*morphism, then the inclusion functor is an [[equivalence of categories]], so nontrivial bireflective subcategories can occur only in non-[[balanced categories]].  Also note that 'bireflective' does *not* mean reflective and [[coreflective subcategory|coreflective]].  One sees this term often in discussions of [[concrete categories]] (such as [[topological categories]]) where really something stronger holds: that the reflector lies over the [[identity functor]] on [[Set]].  In this case, one can say that we have a subcategory that is __reflective over $Set$__.

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
From ([Adamek-Rosick&#253;](#AdamekRosicky)) the "only if"-direction follows immediately from 2.53  there (saying that an accessibly embedded subcategory of an accessible category is accessible iff it is cone-reflective), while "if"-direction follows immediately from 2.23 (saying any left or right adjoint between accessible categories is accessible).


## Properties

A reflective subcategory is always closed under [[limit|limits]] which exist in the ambient category (because the full inclusion is monadic, as noted above), and inherits [[colimit|colimits]] from the larger category by application of the reflector.

A morphism in a reflective subcategory is monic iff it is monic in the ambient category. A reflective subcategory of a well-powered category is well-powered. 

### Reflective subcategories of locally presentable categories

Both the weak and strong versions of [[Vop?nka's principle]] are equivalent to fairly simple statements concerning reflective subcategories of locally presentable categories: 

+-- {: .num_theorem}
###### Theorem

The weak [[Vop?nka's principle]] is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[limit]]s is a reflective subcategory.

=--

This is [AdamekRosicky, theorem 6.28](#AdamekRosicky)

+-- {: .num_theorem}
###### Theorem
The strong [[Vop?nka's principle]] is equivalent to:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[limit]]s is a reflective subcategory; further on, $D$ is then also locally presentable
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

This can always be made to work by brute force, but sometimes there is something insightful about it.  For example, a metric space is a complete metric space equipped with a dense subset.  Or, a possibly nonunital ring is a unital ring equipped with a unital homomorphism to the ring of integers.




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

+-- {: .num_example #NonUnitalRings}
###### (Counter)Example

Unital [[rings]] [[Ring]] form a non-full (see remark \ref{NonFullReflections}) mono-reflective subcategory  of possibly nonunital rings (and homomorphisms not respecting any unit) $Ring'$; the reflector $L \colon Ring' \to Ring$ formally adjoins an [[identity element]].

=--

+-- {: .num_remark #RemarkOnNonUnitalRings}
###### Remark

Notice that for $R \in Ring$ a ring with unit, its reflection $L R$ in the above example is not in general isomorphic to $R$, but is much larger. 
But an object in a reflective subcategory is necessarily isomorphic to its image under the reflector only if the reflective subcategory is full.  While the inclusion $\mathbf{Ring} \hookrightarrow \mathbf{Ring}$' does have a [[left adjoint]] (as any [[forgetful functor]] between varieties of algebras, by the [[adjoint lifting theorem]]), this inclusion is not full (an arrow in $\mathbf{Ring}$' need not preserve the identity).  

=--


## Related concepts

* [[localization]], [[locally presentable category]]

* [[reflective sub-(infinity,1)-category]]

## References

* [[Jiri Adamek|Ji?í Adamek]], [[Ji?í Rosický]], _[[Locally presentable and accessible categories]]_ London Mathematical Society Lecture Note Series 189
 {#AdamekRosicky}

* Springer eom: [reflective subcategory](http://eom.springer.de/r/r080550.htm)

* cf. the notion of $Q^\circ$-category in the entry [[Q-category]]

The relation of exponential ideals to [[reflective subcategories]] is discussed in section A4.3.1 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
  {#Johnstone}

Reflective and coreflective subcategories of presheaf categories are discussed in

* R. Bashir, J. Velebil, _Simultaneously reflective and coreflective subcategories of presheaves_, Theory and  Applications of Categories, Vol 10. No. 16. (2002) ([pdf](http://www.emis.de/journals/TAC/volumes/10/16/10-16.pdf)).

Related discussion of [[reflective sub-(∞,1)-categories]] is in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}

[[!redirects reflector]]
[[!redirects reflectors]]
[[!redirects reflection]]
[[!redirects reflections]]
[[!redirects reflective subcategories]]
[[!redirects reflexive subcategory]]
[[!redirects coreflector]]
[[!redirects coreflectors]]
[[!redirects coreflection]]
[[!redirects coreflections]]
[[!redirects coreflective subcategory]]
[[!redirects coreflective subcategories]]
