
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

_Adjoint functor theorems_ are theorems stating that under certain conditions a [[functor]] that preserves [[limit]]s is a [[right adjoint]], and that a functor that preserves [[colimit]]s is a [[left adjoint]].


A basic result of [[category theory]] is that right [[adjoint functors]] [[preserved limit|preserve]] all [[limits]] that exist in their [[domain]], and, dually, left adjoints preserve all [[colimits]].  An _adjoint functor theorem_ is a statement that (under certain conditions) the converse holds: a functor which preserves limits is a right adjoint.


The basic idea of an adjoint functor theorem is that _if_ we could assume that a [[large category]] $D$ had all [[limits]] over [[small category|small]] and [[large category|large]] [[diagrams]], then for $R : D \to C$ a [[functor]] that [[preserved limit|preserves]] all these limits we might define its would-be left adjoint $L$ by  taking  $L c$ to be the limit
$$
  L c \coloneqq \lim_{c\to R d} d
$$
This notation stands for a limit over the [[comma category]] $c/R$ (whose [[objects]] are [[pairs]] $(d,f:c\to R d)$ and whose [[morphisms]] are arrows $d\to d'$ in $D$ making the obvious triangle [[commuting diagram|commute]] in $C$) of the projection functor $\pi: c/R \to D$ that forgets the morphism $f$: 
$$
  L c = \lim_{c\to R d} \pi
  \,.
$$

Because with this definition there would be, for every $d$, an obvious morphism
$$
  L R d \stackrel{=}{\to} \lim_{R d \to R d'} d' \to d
$$
(the component map over $d$ of the limiting [[cone]]). Moreover, because $R$ preserves limits, we would have an [[isomorphism]]
$$
  R L c \simeq \lim_{c\to R d} R d
$$ 
(the limit of the functor $R \pi$), and hence an obvious morphism of [[cone]] tips
$$
 c \to R L c
 \,.
$$  

It is easy to check that these would be the [[unit of an adjunction|unit]] and [[counit of an adjunction|counit]] of an [[adjunction]] $L\dashv R$. See _[[adjoint functor]]_ for more.

The problem with this would-be argument is that in general the comma category $(c/G)$ may not be [[small category]]. But one can generally not expect a large category to have all large limits: even if we pass to a [[universe]] in which $(c/G)$ is considered small, a [classical theorem of Freyd](complete+small+category#CompleteSmallCategoriesArePosets) says that any [[complete small category]] is a [[preorder]] (see [[complete small category]] for the proof, which is valid in [[classical logic]] and also holds classically in any [[Grothendieck topos]]).  Thus, the argument we gave above is necessarily only an **adjoint functor theorem for preorders**: 

+-- {: .num_theorem #ForPosets}
###### Theorem

If $G:D\to C$ is any functor between (small) preorders such that $D$ has, and $G$ preserves, all small [[meets]], then $G$ has a left adjoint.

=--

(This theorem holds in [[constructive mathematics]], although not in [[predicative mathematics]]; the classical reasoning before this explains why the theorem is not more general, but the proof itself is already constructive.)

To obtain adjoint functor theorems for categories that are not preorders, one must therefore impose various additional "size conditions" on the category $D$ and/or the functor $G$.  


## Statement


+-- {: .num_theorem #StandardAdjointFunctorTheorem}
###### Theorem

Sufficient conditions for a limit-preserving functor $R : C \to D$ to be a [[right adjoint]] include:

* $C$ is [[complete category|complete]] and [[locally small category|locally small]], and $R$ satisfies the [[solution set condition]].  

  This is Freyd's original version, sometimes called the "**General Adjoint Functor Theorem**".

* $C$ is complete, locally small [[well-powered category|well-powered]], and has a [[small set|small]] [[cogenerating set]], and $D$ is [[locally small category|locally small]].  

  This is sometimes called the "**Special Adjoint Functor Theorem**", and abbreviated to SAFT.

* $C$ is locally small and [[total category|cototal]], and $D$ is locally small.

=--

In the first two cases, which work by replacing large limits by small ones, it suffices to assume that $R$ preserves small limits (that it preserves all limits will follow).  The third case works by assuming that $C$ has, while not all large limits, enough so that the theorem goes through; thus is this case $R$ must be already known to preserve [[large category|large]] limits as well.


+-- {: .proof}
###### Proof

Here is a proof of the General Adjoint Functor Theorem: that a functor $R : C \to D$ out of a [[locally small category]] $C$ with all small limits has a left adjoint if it preserves these [[limit]]s and satisfies the [[solution set condition]]. 

From the discussion at <a href="http://ncatlab.org/nlab/show/adjoint%20functor#UniversalArrows">adjoint functors -- In terms of universal arrows</a> we have that the existence of the adjoint is equivalent to the existence for each $d \in D$ of an [[initial object]] $i_d : d \to R L d$ in the [[comma category]] $(d \downarrow R)$: an object such that for each $f : d \to R d'$ there is a unique $\tilde f$ such that 

$$
  \array{
    && d 
    \\
    & {}^{\mathllap{i_d}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R L d &&\underset{R \tilde f}{\to}&& R d'
    \\
    \\
    L d &&\underset{\tilde f}{\to}&& d'
  }
$$

commutes. Now an initial object is the limit of the identity functor, but this is generally a large limit; we replace this with some small limit conditions that guarantee existence of an initial object. 

1. Let $Y$ be a category. Call a small family of objects $F$ _weakly initial_ if for every object $y$ of $Y$ there exists $x \in F$ and a morphism $f: x \to y$. 

1. Suppose $Y$ has small products. If $F$ is a weakly initial family, then $\prod_{x \in F} x$ is a [[weak multilimit|weakly initial]] object. 

1. **Claim:** Suppose $Y$ is locally small and small complete. If $x$ is a weakly initial object, then the domain $e$ of the joint equalizer $i: e \to x$ of all arrows $x \to x$ is an initial object. **Proof:** clearly $e$ is weakly initial. Suppose given an object $y$ and arrows $f, g: e \to y$; we must show $f = g$. Let $j: d \to e$ be the equalizer of $f$ and $g$. There exists an arrow $k: x \to d$. The arrow $i: e \to x$ equalizes $1_x$ and $i j k: x \to x$, so $i j k i = i$. Since $i$ is monic, $j (k i) = 1_e$. Thus $j$ is an epi, and $f = g$ follows. 

If $C$ is locally small and small-complete and $R: C \to D$ preserves limits, then $d \downarrow R$ is locally small and small-complete for every object $d$ of $D$. 

If in addition each $d \downarrow R$ has a weakly initial family (solution set condition), then by 2. and 3. each $d \downarrow R$ has an initial object. This restates the condition that $R$ has a left adjoint.

=--

+-- {: .proof} 
###### Proof of SAFT 
As before, the proof proceeds by constructing initial objects of comma categories. We assume that $C$ is locally small, small-complete, well-powered, has a cogenerating set $\{c_\alpha: \alpha \in A\}$, and that $R: C \to D$ is a small-continuous functor into a locally small category $D$. 

As before, for each object $d$ of $D$, the comma category $d \downarrow R$ is locally small and small-complete. Moreover, it is easy to check that it is well-powered, and that the set of all objects of the form $d \to R c_\alpha$ is a cogenerating set for $d \downarrow R$. 

It then remains to prove that any locally small, small-complete, well-powered category $X$ with a cogenerating set $\{k_s: s \in S\}$ has an initial object. The initial object $0$ is constructed as the intersection = pullback of all subobjects of $\prod_s k_s$, i.e., the minimal subobject. Then, given $f, g: 0 \to x$, the equalizer $Eq(f, g)$ is isomorphic to $0$ because $0$ is minimal, and so $f = g$: there is at most one arrow $0 \to x$ for each $x$. 

On the other hand, for each $x$ the canonical map 

$$i: x \to \prod_{s \in S} k_{s}^{\hom(x, k_s)}$$ 

is monic since the $k_s$ cogenerate. The following pullback of $i$, 

$$\array{
k & \to & x \\ 
\downarrow & & \downarrow \mathrlap{i} \\
\prod_s k_{s}^1 & \stackrel{\prod_s k_{s}^!}{\to} & \prod_s k_{s}^{\hom(x, k_s)}
},$$ 
gives a subobject $k$ of $\prod_s k_s$ that maps to $x$, and into which $0$ embeds. Thus there exists a map $0 \to x$, and we conclude $0$ is initial. 
=--

In practice an important special case is that of functors between
[[locally presentable categories]]. For these there is the following 
version of an adjoint functor theorem.

+-- {: .num_theorem #AdjFuncTheoremForLocallyPresentableCats}
###### Theorem

Let $F : C \to D$ be a functor between [[locally presentable categories]]. Then

* $F$ has a [[right adjoint]] if and only if it preserves all small [[colimits]].

* $F$ has a [[left adjoint]] if and only if it is an [[accessible functor]] and preserves all small [[limits]].

=--

The second statement, characterizing when $F$ has a left adjoint, is  ([AdamekRosicky, theorem 1.66](#AdamekRosicky)). In the "if" direction, this is an application of the general adjoint functor theorem: any accessible functor satisfies the solution set condition. The "only if", particularly that having a left adjoint forces accessibility, takes a little work. But in any case there are easy examples that show that continuity alone is insufficient, i.e., examples of continuous functors between locally presentable categories that do not have left adjoints. See below in the section [In locally presentable categories](#InLocallyPresentableCategories). 

The first statement, characterizing when $F$ has a right adjoint, can be proven using the special adjoint functor theorem: by a non-trivial theorem ([AdamekRosicky, theorem 1.58](#AdamekRosicky)), any locally presentable category is co-wellpowered. 

Thus, the first statement can be strengthened by removing the assumption that $D$ is locally presentable: it is enough that $D$ be locally small. For example, if $C$ is locally presentable, then every continuous functor 

$$C^{op} \to Set$$ 

has a left adjoint (is representable), because its opposite $C \to Set^{op}$ is cocontinuous and therefore has a right adjoint, even though $Set^{op}$ is not locally presentable. 

A right adjoint to any cocontinuous functor $F \colon C \to D$ between locally presentable categories can also be constructed directly. If $C$ is locally $\lambda$-presentable and $P_\lambda$ is the subcategory of $\lambda$-small objects, then $C$ is equivalent to the full subcategory of $[P_\lambda^{op},Set]$ of presheaves that preserve $\lambda$-small limits ([AdamekRosicky, theorem 1.46](#AdamekRosicky)). The presheaves in the image of the functor $D \to [P_\lambda^{op},Set]$ defined by $d \mapsto \hom(F-,d)$ preserve $\lambda$-small limits because $F$ is cocontinuous. So this functor factors through the subcategory $C$. The functor $D \to C$ so-constructed is a right adjoint to $F$.


## Examples {#Examples}

### In locally presentable categories
 {#InLocallyPresentableCategories}

The following is a counter-example, indicating the need for something more than just continuity to force a functor between locally presentable categories to be a right adjoint; as stated in theorem \ref{AdjFuncTheoremForLocallyPresentableCats}, the missing extra condition is precisely accessibility.

+-- {: .num_example}
###### Example

For every infinite [[cardinal number]] $\kappa$, let 
$G_\kappa$ be a [[simple group]] of [[cardinality]] $\kappa$. 
Define the functor $ML:$ [[Group]] $\to$ [[Set]] to be the 
[[product]] of all the [[representable functors]] 
$Hom(G_\kappa,-)$. 
Since no group can admit a nontrivial 
[[homomorphism]] from proper-[[class]]-many of the $G_\kappa$, 
this functor does indeed land (or can be redefined to land) in [[Set]]. 
Since it is a product of representables, it is 
[[continuous functor|continuous]] 
(and of course [[Group]] and [[Set]] are 
[[locally presentable categories]]), 
but it is not itself representable (hence has no [[left adjoint]]).

=--

[[André Joyal]] has been attributing this example to [[Saunders MacLane]],
it appears in print for instance right at the beginning of ([Ad&#225;mekKoubekTrnkov&#225;01](#AdamekKoubekTrnkova)).

### In cocomplete categories

Suppose $C$ and $D$ are categories that admit [[small colimits]]
(i.e., are [[cocomplete]])
and $F\colon C\to D$ is a functor that preserves [[small colimits]]
(i.e., is cocontinuous).
The $F$ has a [[right adjoint functor]]
if and only if for any object $d\in D$
the functor
$$C^{op} \to Set$$
that sends
$$c\mapsto D(F(c),d)$$
is a [[small presheaf]] on $C$.

See the [MathOverflow answer](https://mathoverflow.net/questions/346153/surmounting-set-theoretical-difficulties-in-algebraic-geometry/346162#346162) by [[Ivan Di Liberti]].


### In toposes

+-- {: .num_prop}
###### Proposition

Every [[sheaf topos]] is a [[total category]] and a [[cototal category]].

=--

See the discussion at _[[Grothendieck topos]]_. 


It follows that

+-- {: .num_cor}
###### Corollary

Let $F : C \to D$ be a [[functor]] between [[sheaf toposes]]. Then

* $F$ has a [[right adjoint]] precisely if it preserves all small [[colimits]];

* $F$ has a [[left adjoint]] precisely if it preserves all small [[limits]].

=--


### In presheaf categories 
 {#InPresheafCategories}

It is instructive to spell out the construction of the [[right adjoint]] from a colimit preserving functor $L$ in the simple case where all categories are [[categories of presheaves]]. This is a particularly simple case, but is useful in itself and serves as a template for the general case.

So let now $C$ and $D$ be [[small categories]] and $L$ a [[colimit]]-[[preserved colimit|preserving]] functor between their [[categories of presheaves]] (which we abbreviate $\widehat C \;\coloneqq\; [C^{op}, Set]$, etc):

$$
  L \;\colon\; \widehat{C} \longrightarrow \widehat{D}
$$

Then its [[right adjoint]] $ R \;\colon\; \widehat{D} \longrightarrow \widehat{C}$ is given (with $y_c \coloneqq C(-, c)$ denoting the [[Yoneda embedding]]) by

\[
  \label{RightAdjointOfColimitPreservingFunctorOfPresheaves}
  R 
    \;\colon\; 
  A 
    \;\mapsto\;  
  R(A)  
   \;\coloneqq\; 
   \widehat{D}
   \left(
     L(y_{(-)}),
     A
   \right)
   \,,
\]

as we shall check in a moment. But first notice that using the [[co-Yoneda lemma]] this may be rewritten as

$$
  \cdots 
    \;\simeq\;  
   \int^{c \in C} 
   \widehat{D}
   \left(
     L(y_c), A
   \right) 
     \cdot y_c
   \,,
$$

where the [[coend]] is equivalently given by the [[colimit]]

$$
  \cdots \;=\; \lim_{\underset{L c \to A}{\to}} c
  \,.
$$

This is the formula for the would-be right adjoint from the general discussion above, only that here the colimit is only over the representables, hence over a small category.

Now we check that the functor $R$ thus obtained is indeed right adjoint to $L$, by explicitly checking the hom-isomorphism ([here](adjoint+functor#InTermsOfHomIsomorphism)) of the pair of [[adjoint functors]]:

We compute $\widehat{D}(L(X),A)$. In the first step

$$
  \widehat{D}(L(X), A)
  \simeq
  \widehat{D}
  \left(
     L 
     \left(
        \int^{c \in C} X(c) \cdot y_c
     \right), 
     A
   \right)
$$

we use the [[co-Yoneda lemma]] for $X$. Then, because $L$ [[preserved limit|preserves]] colimits, this is

$$
  \cdots 
    \simeq 
   \widehat{D}
   \left(
     \int^c X(c) \cdot L(y_c), A
   \right)
  \,.
$$

Since the [[hom-functor]] preserves limits in both arguments, we can take the [[coend]] out to get an [[end]]

$$
  \cdots 
    \simeq 
   \int_{c \in C} 
     \widehat{D}(X(c) \cdot L(y_c), A)
  \,.
$$

Then we use the standard [[copower|tensoring]] of our categories over [[Set]] to get

$$
  \cdots 
    \simeq 
   \int_{c \in C} 
   Set\left(  
     X(c), 
     \widehat{D}(L(y_c),A)
   \right)
  \,.
$$

And finally this is recognized as the formula for the [[hom-set]] of presheaves (see the discussion at _[[functor category]]_):

$$
  \cdots 
    \simeq 
   \widehat{C}
   \left(
     X, 
     \widehat{D}(L(y_{(-)}),A)
    \right) 
     \;=\; 
    \widehat{C}(X, R A)
  \,,
$$

where on the right we identified (eq:RightAdjointOfColimitPreservingFunctorOfPresheaves).

The [[composition]] of this sequence of [[natural isomorphisms]] is hence the desired hom-isomorphism:

$$
  \widehat{D}(L(X), A) \simeq \widehat{C}(X, R(A))
  \,.
$$

## Related concepts

* **adjoint functor theorem**

* [[indexed adjoint functor theorem]]

* [[adjoint (∞,1)-functor theorem]]

* [[adjoint triangle theorem]]

## References

The classical adjoint functor theorems originate in the exercise section of ch.3 (pp.84ff) in

* [[Peter Freyd]], *Abelian Categories*, Harper & Row New York 1964. (Reprinted with author's comment as [TAC reprints no. 3 (2003)](http://www.tac.mta.ca/tac/reprints/articles/3/tr3abs.html))

A more recent exposition is in

* [[Peter Freyd]], Andre Scedrov, *Categories, Allegories*, North-Holland, 1990. (Also Dover reprint New York 2014, pp.144-148)

Careful discussions can be found in

* [[Francis Borceux]], *Handbook of Categorical Algebra I*, Cambridge UP, 1994. (sections 3.3, 6.6)

* [[Saunders Mac Lane]], *Categories for the Working Mathematician*, Springer Heidelberg, 1998&#178;. (sections V.6, V.8)

A brief introductory discussion is around [theorem 5.4](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf#page=54) of

* [[Jaap van Oosten]], *Basic category theory*, ms. ([pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf))

A detailed expository survey is

* Oliver Kullmann, *The adjoint functor theorem*, ms. ([pdf slides](http://www.cs.swan.ac.uk/~csoliver/Hauptseminar/Quellen/200702Swansea_b.pdf))

The adjoint functor theorem in context with [[Yoneda embedding]] is discussed in 

* Friedrich Ulmer, *The adjoint functor theorem and the Yoneda embedding*, Illinois J. Math. **15**  no.3 (1971), pp. 355-361. ([euclid](http://projecteuclid.org/euclid.ijm/1256052605))

The connection between the solution set condition and the Čech homology construction is discussed in

* Renato Betti, _Čech methods and the adjoint functor theorem_ , Cah. Top. Géom. Diff. Cat. **XXVI** no.3 (1985) pp.245-257. ([numdam](http://www.numdam.org/item/?id=CTGDC_1985__26_3_245_0))

The parallels between the adjoint functor theorem for categories and the computation of colimits from limits in a lattice as well as similar parallels between co/completeness for Boolean algebras and Paré's theorem for finite completeness of toposes is studied from a type-theoretical perspective in

* [[Dusko Pavlovic|Duško Pavlović]], _On completeness and cocompleteness in and around small categories_ , APAL **74** (1995) pp.121-152.

The case for [[locally presentable categories]] is discussed in

* [[Jiří Adámek]], [[Jiri Rosicky]], *[[Locally presentable and accessible categories]]*, Cambridge UP, 1994.
  {#AdamekRosicky}

* [[Jiří Adámek]], V. Koubek and V. Trnkov&#225;, *How large are left exact functors?*, Theory and Applications of Categories **8** (2001), pp. 377-390. ([abstract](http://www.emis.de/journals/TAC/volumes/8/n13/8-13abs.html))
 {#AdamekKoubekTrnkova}

A relative version of Freyd's classical results is in

* [[Brian Day]], *An adjoint-functor theorem over topoi*, Bull. Austral. Math. Soc. **15** (1976), pp. 381-394.

[[indexed adjoint functor theorem|Adjoint functor theorems for indexed categories]] are discussed in

* [[Robert Paré]], Dietmar Schumacher, _Abstract Families and the Adjoint Functor Theorems_ , pp.1-125 in LNM **661** Springer Heidelberg 1978.

[[!redirects adjoint functor theorems]]