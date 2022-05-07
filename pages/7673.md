+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Categorical models of dependent types
* table of contents
{: toc}

## Idea

In the [[relation between type theory and category theory]], [[dependent types]] are said to correspond to morphisms regarded as indexed families.  That is, if a [[type]] $A$ corresponds to an [[object]] in some [[category]], then a [[dependent type]]

$$ (x:A) \;\vdash\; (B(x) \;type) $$

corresponds to a [[morphism]] $B\to A$ in that category.  We think of this morphism as a [[bundle]] or [[fibration]], whose [[fiber]] over $x:A$ is the type $B(x)$.  We can then say that [[type former|type forming operations]] such as [[dependent sum type]] and [[dependent product type]] correspond to category-theoretic operations of [[dependent sum]] and [[dependent product]].

However, this correspondence is not quite precise; in the case of dependent types there are extra [[coherence]] issues.  [[substitution|Substitution]] in [[type theory]] should correspond to [[pullback]] in [[category theory]] (but see at _[substitution -- Categorical semantics](substitution#CategoricalSemantics)_ for more); that is, given a term

$$ (y:C) \;\vdash\; (f(y) : A) $$

corresponding to a morphism $f:C\to A$, the substituted dependent type

$$ (y:C) \;\vdash\; (B(f(y)) \;type) $$

should correspond to the pullback of $B\to A$ along $f$.  However, substitution in type theory is strictly [[associativity|associative]].  That is, given also $g:D\to C$, the dependent type

$$ (z:D) \;\vdash\; (B(f(g(z))) \;type)$$

is [[equality|syntactically the same]] regardless of whether we obtain it by substituting $y \coloneqq g(z)$ into $B(f(y))$, or $x \coloneqq f(g(z))$ into $B(x)$.  In category theory, however, pullback is not generally strictly associative, so there is a mismatch.  Similarly, every [[type formation rule|type-forming operation]] must also be strictly preserved by substitition/pullback.

The way this is generally dealt with is to introduce a category-theoretic structure which does have a "substitution" operation which is strictly associative, hence does correspond directly to type theory, and then show that any category can be "strictified" into such a stricter structure.  Unfortunately, there are many different such structures which have been used, differing only slightly.  On this page we define and compare them all.

One of these structures is called "contextual categories" (definition \ref{ContextualCategory} below). 

{#StandInForSyntax} This and other kinds of categories-with-extra-structure may hence be thought of as stand-ins for the [[syntax]] of a [[type theory]]:

> Rather than constructing an interpretation of the syntax directly, we may work via the intermediary notion of contextual categories, a class of algebraic objects abstracting the key structure carried by the syntax. The plain definition of a contextual category corresponds to the structural core of the syntax; further syntactic rules (logical constructors, etc.) correspond to extra algebraic structure that contextual categories may carry. Essentially, contextual categories provide a completely equivalent alternative to the syntactic presentation of type theory. 

> Why is this duplication of notions desirable? The trouble with the syntax is that it is mathematically tricky to handle. Any full presentation must account for (among other things) variable binding, capture-free substitution, and the possibility of multiple derivations of a judgement; and so a direct interpretation must deal with all of these, at the same time as tackling the details of the particular model in question. By passing to contextual categories, one deals with these subtleties and bureaucracy once and for all, and obtains a clear framework for subsequently constructing models. Conversely, why not work only with contextual categories, dispensing with syntax entirely?

> The trouble on this side is that working with higher-order logical structure in contextual categories quickly becomes unreadable. The reader preferring to take contextual categories as primary may regard the syntax as essentially a notation for working within them: a powerful, flexible, and intuitive notation, but one whose validity requires non-trivial work to establish. (The situation is comparable to that of string diagrams, as used in monoidal and more elaborately structured categories.)

> (from [Kapulkin-Lumsdaine 12](#KapulkinLumsdaine12))

## Definitions

In all the definitions, $C$ will be a [[category]].  Generally, we will regard the objects of $C$ as [[contexts]] in a type theory.

So far, we do not assume anything about $C$ as a category.  Usually, one at least wants $C$ to have a [[terminal object]], representing the empty context, although this is not always included in the definitions.  The additional structures we impose on $C$ below will imply in particular that certain [[pullbacks]] exist in $C$.

Sometimes, we want to consider $C$ as a [[strict category]], that is, we consider its objects up to [[equality]] rather than [[isomorphism]].  However, for most of the definitions below (until we get to contextual categories), it is still sensible to treat $C$ in an ordinary category-theoretic way, with the strictness living in the additional structure.

All of this could be made more precise by assembling the structures considered below into [[categories]], [[2-categories]], and/or [[strict 2-categories]].


### Comprehension categories

+-- {: .num_defn #ComprehensionCategory}
###### Definition

A **comprehension category** consists of a strictly [[commuting diagram|commutative triangle]] of [[functors]]
$$ \array{ E && \to && C^I\\ & \searrow && \swarrow {\scriptsize cod} \\ && C } $$
where $C^I$ is the [[arrow category]] of $C$ and $cod \colon C^I \to C$ denotes the codomain projection (which is a [[codomain fibration|fibration]] if $C$ has pullbacks), and such that

1. $E\to C$ is a [[Grothendieck fibration]], 

1. $E\to C^I$ takes [[cartesian morphisms]] in $E$ to cartesian morphisms in $C^I$ (i.e. to [[pullback]] squares in $C$).

=--

+-- {: .num_remark}
###### Remark

In def \ref{ComprehensionCategory} we do not ask that $C^I \to C$ be a [[Grothendieck fibration|fibration]] (that would require $C$ to have all [[pullbacks]]), only that the *particular* morphisms in the image of $E$ are cartesian.

=--

+-- {: .num_defn #FullAndSplitComprehensionCategory}
###### Definition

A comprehension category (def. \ref{ComprehensionCategory}) is called 

* **full** if $E\to C^I$ is a [[fully faithful functor]].  

* **split** if $E\to C$ is a [[split fibration]].  

In the latter case, we must consider $E$ at least to be a [[strict category]] (that is, we consider its objects up to equality rather than isomorphism) for the notion to make sense.

=--

+-- {: .num_remark #MeaningOfComprehensionCategory }
###### Remark

The interpretation of def. \ref{ComprehensionCategory} is as follows:

In a comprehension category, we may regard the objects of $C$ as [[contexts]], and the [[fiber]] $E^\Gamma$ of $E\to C$ over an object $\Gamma$ as the category of [[dependent types]] in context $\Gamma$.  If the comprehension category is split (def. \ref{FullAndSplitComprehensionCategory}), then such dependent types have strictly [[associativity|associative]] [[substitution]].

The functor $E\to C^I$ assigns to each "type $A$ in context $\Gamma$" a new context which we think of as $\Gamma$ *extended* by a fresh [[variable]] of type $A$, and write as $\Gamma.A$.  This new context $\Gamma.A$ comes with a projection $\Gamma.A\to \Gamma$ (which forgets the fresh variable), and all substitutions in $E$ are realized as pullbacks in $C$.

=--

### Display map categories

+-- {: .num_defn #DisplayMapCategory}
###### Definition

A **[[display map category]]** consists of a [[category]] $C$ together with a [[class]] $D$ of [[morphisms]] in $C$, called _[[display maps]]_, such that all [[pullbacks]] of display maps exist and are themselves display maps.

=--

If $C$ is a display map category, then by defining $E$ to be the [[full subcategory]] of $C^I$ whose objects are display maps, we obtain a full comprehension category (def. \ref{FullAndSplitComprehensionCategory}).  Thus, we have:

+-- {: .num_lemma #DMCasCmpC}
###### Lemma

Display map categories (def. \ref{DisplayMapCategory}) may be identified with those comprehension categories, def. \ref{ComprehensionCategory}, for which the functor $E\to C^I$ is the inclusion of a [[full subcategory]].

=--

+-- {: .num_remark}
###### Remark

Working up to [[equivalence of categories]], as is usual in [[category theory]], it is natural to consider display map categories to also be equivalent to *full* comprehension categories, def. \ref{FullAndSplitComprehensionCategory}, (those where $E\to C^I$ is merely fully faithful).

However, this breaks down when we are interested in *split* comprehension categories, def. \ref{FullAndSplitComprehensionCategory}, for modeling substitution with strict associativity, since then $E$ at least must be regarded as a [[strict category]] and considered up to [[isomorphism]] rather than equivalence.  Thus, display map categories may be said to be equivalent to non-split full comprehension categories, but "split display map categories" are not equivalent to split full comprehension categories.  (In fact, split display map categories are not very useful; usually in order to make pullbacks strictly associative we have to introduce extra "names" for the same objects.)

=--

### Categories with attributes

+-- {: .num_defn #CategoryWithAttributes}
###### Definition

A **category with attributes** is a comprehension category, def. \ref{ComprehensionCategory}, for which $E\to C$ is a [[discrete fibration]].

=--

+-- {: .num_remark}
###### Remark

That is, in a category with attributes (def. \ref{CategoryWithAttributes}) we demand only that each context comes with a [[set]] of [[dependent types]] in that context, rather than a category of such.  The intent is that the morphisms between two types in context $\Gamma$ should be determined by the morphisms in $C$ between the extended contexts over $\Gamma$.

Another way to convey this same intent with a comprehension category would be to ask that it be *full*, def. \ref{FullAndSplitComprehensionCategory}, i.e. that the functor $E\to C^I$ be fully faithful.  

=--

In fact, any category with attributes gives rise to a full comprehension category by factoring the functor $E\to C^I$ into a [[bijective on objects functor]] followed by a [[fully faithful functor]].  In this way, we obtain:

+-- {: .num_lemma #CWAasCmpC}
###### Lemma
The category $\mathbf{CwA}$ of categories with attributes (def. \ref{CategoryWithAttributes}) is equivalent to the category of $\mathbf{CompCat}_{\text{full,split}}$ of full split comprehension categories (def. \ref{FullAndSplitComprehensionCategory}).

(These are, however, quite different as subcategories of $\mathbf{CompCat}$.)
=--


### Categories with families

A category with attributes specifies for each "context" only a set of "types" in that context.  A comprehension category, by contrast, specifies a whole *category* of "types" in each context.  If $A,B\in E^\Gamma$, then we may think of a morphism $f:A\to B$ in $E^\Gamma$ as a term

\[ (\vec{x} : \Gamma), (a:A(\vec{x})) \;\vdash\; (f(\vec{x},a) : B(\vec{x})) \label{cmpcterm} \]

in type theory.  
A *category with families* specifies instead, for each context and each type in that context, a set of "terms belonging to that type".  These should be thought of as terms

\[ (\vec{x} : \Gamma) \;\vdash\; (f(\vec{x}) : B(\vec{x})) \label{cwfterm} \]

in type theory.  

+-- {: .num_remark}
###### Remark

A [[term]] of the form (eq:cmpcterm) can equivalently be regarded as a term of the form (eq:cwfterm) by replacing $\Gamma$ by the extended context $\Gamma.A$, and $B$ by its substitution along the projection $\Gamma.A \to \Gamma$.

=--

The additional insight in the following definition is that if we expect all of these terms to be determined by the morphisms in $C$, as in a category with attributes or a full comprehension category, then instead of specifying the functor $E\to C^I$ and then asking either that it be fully faithful or that $E$ be discrete (removing the information about extra morphisms in $E$), if we specify the terms of the form (eq:cwfterm), then the functor $E\to C^I$ is determined by a universal property.

Let $Fam$ denote the category of families of sets.  Its objects are set-indexed families $(A_i)_{i\in I}$, and its morphisms $(A_i)_{i\in I} \to (B_j)_{j\in J}$ consist of a function $f\colon I\to J$ and functions $g_i \colon A_i \to B_{f(i)}$.  We can equivalently, of course, regard this as the arrow category $Set^I$ of [[Set]], where $(B_j)_{j\in J}$ corresponds to the arrow $\coprod B \to J$.

+-- {: .num_defn #CategoryWithFamilies}
###### Definition

A **category with families** is a category $C$ together with

* A functor $F:C^{op} \to Fam$, written $F(\Gamma) = (Tm(A))_{A\in Ty(\Gamma)}$.

* For each $\Gamma\in C$ and $A\in Ty(\Gamma)$, a [[representing object]] for the functor
  $$
  \begin{aligned}
    (C/\Gamma)^{op} & \to Set\\
    (\Delta \xrightarrow{f} \Gamma) & \mapsto Tm(f^*(A))
  \end{aligned}
  $$
=--
Intuitively, $F(\Gamma)$ is the set of terms in the context $\Gamma$ indexed by their type, and the representing object for the map $(C/\Gamma)^{op} \to Set$ is the projection from context $\Gamma; A$ to context $\Gamma$.

We can then prove:

+-- {: .num_lemma #CwAareCwF}
###### Lemma

Categories with attributes, def. \ref{CategoryWithAttributes} are equivalent to categories with families, def. \ref{CategoryWithFamilies}.

=--
+-- {: .proof}
###### Proof
Given a category with families, let $E\to C$ be the [[Grothendieck construction]] of the functor $Ty:C^{op}\to Set$, and let $E\to C^I$ take each $A\in Ty(\Gamma)$ to the above representing object.  This is a category with attributes.

Conversely, given a category with attributes, let $Ty:C^{op}\to Set$ be the functor corresponding to the discrete fibration $E\to C$, and for $A\in Ty(\Gamma)$ let $Tm(A)$ be the set of [[sections]] of the morphism in $C$ that is the image of $A$ in $C^I$.  These constructions are inverses up to isomorphism.
=--


### Natural Models

[[Steve Awodey]] ([Awodey 2018](#Awodey2018)) presented the following "natural model" of type theory as an alternative to categories with families.

+-- {: .num_theorem}
###### Theorem
If we modify Def. \ref{CategoryWithFamilies} by requiring only that the functors $(\Delta \xrightarrow{f} \Gamma) \mapsto Tm(f^*(A))$ be representable (rather than equipped with representing objects), then it is equivalent to giving

1. a category $C$, together with
1. a morphism $Tm \to Ty$ in the category of [[presheaves]] on $C$ which is a [[representable morphism]].
=--

The category $C$ models the category of contexts and substitutions, and the morphism $Tm \to Ty$ models the bundle of (context-dependent) terms over (context-dependent) types. The representability models the extension of a context with a new typed variable.

The condition of being a representable morphism can be reformulated in terms of representable profunctors as follows.
A natural model consists of

1. a category $C$,
2. a presheaf $Ty : \hat C$ of types in context.
3. a presheaf $Tm : \widehat {\int Ty}$ of typed terms in context.
4. a functor $ext : \widehat {\int Ty} \to C$ of context extension with data that represents the profunctor ${\int Ty}(ty-,=) \odot C(-,ctx(ty(=))) : \int Ty &#8696; C$ where $ty : \int Tm \to \int Ty$ and $ctx : \int Ty \to C$ are the projections of the [[Grothendieck construction]].

Writing the profunctor as P, it is equivalent to the following definition:

$$P(\Delta, (\Gamma, A)) = (\gamma : \Delta \to \Gamma) \times (a : Tm(\Delta, A[\gamma]))$$

then the universal property of the context extension is that there is a natural isomorphism $\Delta \to ext(\Gamma, A) \cong P(\Delta,(\Gamma,A))$


### Contextual categories, or C-systems

Recall that 

+-- {: .num_defn #NotationForExtendedContexts}
###### Definition


If $C$ is a [[comprehension category]] (def. \ref{ComprehensionCategory}), $\Gamma\in C$ is a "context" and $A\in E^\Gamma$ is a "type" in context $\Gamma$, then we denote by $\Gamma.A$ the "extended context" in $C$ (remark \ref{MeaningOfComprehensionCategory}).

=--

+-- {: .num_defn #ContextualCategory}
###### Definition

A **contextual category** ([Cartmell 86](#Cartmell86), [Streicher 91](#Streicher91)) or **C-system** ([Voevodsky 15](#Voevodsky15a)) is a category with attributes $C$ (def. \ref{CategoryWithAttributes}) together with a *length function* $\ell : ob(C) \to \mathbb{N}$ such that

1. There is a unique object of length $0$, which is a [[terminal object]].
1. For any $\Gamma\in C$ and $A\in E^\Gamma$, we have $\ell(\Gamma.A) = \ell(\Gamma)+1$.
1. For any $\Delta\in C$ with $\ell(\Delta)\gt 0$, there exists a unique $\Gamma\in C$ and $A\in E^\Gamma$ such that $\Delta = \Gamma.A$ (with notation as in def. \ref{NotationForExtendedContexts}).

=--

+-- {: .num_remark}
###### Remark

Since def. \ref{ContextualCategory} refers to [[equality]] of objects, a contextual category $C$ must be a [[strict category]].  

=--

+-- {: .num_remark}
###### Remark

The idea which distinguishes a contextual category is that "every context must be built out of types" in a unique way.  

=--

This makes for the closest match with type theory; in fact we have:

+-- {: .num_theorem #CxtCareTT}
###### Theorem

The category of contextual categories, def. \ref{ContextualCategory}, and (strictly) structure-preserving functors is [[equivalence of categories|equivalent]] to the [[category of dependent type theories and interpretations]].

=--

+-- {: .num_remark}
###### Remark

Since contextual categories are [[strict categories]], the category of such is really a [[1-category]], or perhaps a [[strict 2-category]].

=--

+-- {: .num_example #ContextualFromAttributes}
###### Example

Given any category with attributes $C$, def. \ref{CategoryWithAttributes},  possessing a [[terminal object]], there is a canonical way to build a contextual category $cxt(C)$, def. \ref{ContextualCategory}, from it.  

1. Choose a [[terminal object]] $1\in C$ (the resulting contextual category does not depend on this choice, up to isomorphism).  

1. The [[objects]] of $cxt(C)$ are the finite [[lists]]

   $$(A_0,A_1,\dots,A_n)$$

   such that $A_0 \in E^1$ and $A_{k+1} \in E^{1.A_0.A_1.\cdots .A_k}$ for all $k$.  

1. The [[morphisms]] $(A_0,\dots,A_n) \to (B_0,\dots,B_m)$ in $cxt(C)$ are the morphisms $1.A_0.A_1.\cdots.A_n \to 1.B_0.B_1.\cdots.B_m$ in $C$.  

All the rest of the structure on $cxt(C)$ is induced in an evident way from $C$.  This construction is in fact right adjoint to the inclusion of contextual categories in categories with attributes; see [Kapulkin-Lumsdaine, Proposition 4.4](#KapulkinLumsdaine16).

=--

## Examples

Comprehension categories and display map categories are easy to come by "in nature", but it is more difficult to find examples of the "split" versions of the above structure (which are what is needed for modeling type theory).  Here we summarize some basic known constructions.

However, first we should mention the examples that come from type theory itself.

### Syntactic categories

+-- {: .num_example}
###### Example

The [[syntactic category]] of any [[dependent type theory]] has all of the above structures.  Its objects are [[contexts]] in the theory, and the types in context $\Gamma$ form the set or category $E^\Gamma$.  The strict associativity of substitution in type theory makes this fibration automatically split.

=--


### Splitting fibrations

There are standard constructions which can replace any [[Grothendieck fibration]] by an equivalent [[split fibration]].  Therefore, 

+-- {: .num_example #FromComprehensionToContextual}
###### Example

Given any comprehension category, def. \ref{ComprehensionCategory}, 

1. we may replace it by a split comprehension category, def. \ref{FullAndSplitComprehensionCategory}, 

1. then consider the underlying category with attributes, def. \ref{CategoryWithAttributes}, 

1. and finally pass to a contextual category by the construction in example \ref{ContextualFromAttributes}.

=--

Of course, comprehension categories are easy to come by; perhaps they arise most commonly as [[display map categories]].  For instance, if $C$ has all [[pullbacks]], then we can take all maps to be [[display maps]].  If $C$ is a [[category of fibrant objects]], we can take the [[fibrations]] to be the display maps.

So, for the record, we have in particular:

+-- {: .num_example #TypeTheoryModelFromLocallyCartesianClosedCategory}
###### Example

For $C$ a [[locally cartesian closed category]] $C$, it becomes a model for [[dependent type theory]]  by regarding its [[codomain fibration]] $C^I \to C$ as a comprehension category, def. \ref{ComprehensionCategory}, and then strictifying that as in example \ref{FromComprehensionToContextual}.

=--

+-- {: .num_remark}
###### Remark

It turns out that for modeling additional [[type-forming operations]], however, not all splitting constructions are created equal.

Given $E\to C$, one construction due to [[Benabou]] (called the "right adjoint splitting"), defines $E'\to C$, where the objects of $E'$ over $\Gamma\in C$ are functors $C/\Gamma \to E$ over $C$ which map every morphism of $C/\Gamma$ to a cartesian arrow.  Type-theoretically, we can think of such an object as a type together with *specified* compatible substitutions along any possible morphism.  That type-formers may be extended in this case was proven by [[Martin Hofmann]] for [[dependent sums]] and [[dependent products]] and the [[identity types]] of [[extensional type theory]].  But this is not generally possible for the identity types of [[intensional type theory]] (particularly not their [[term elimination|eliminator]]), which do not have a 1-categorical universal property and hence are not stable under pullback up to isomorphism.

A different construction (due to [[John Power]], called the "left adjoint splitting") defines an object of $E'$ over $\Gamma\in C$ to consist of a morphism $f:\Gamma \to \Delta$ in $C$ along with an object $A$ of $E$ over $\Delta$.  Type-theoretically, we can regard $(f,A)$ as a type $A$ with a "delayed substitution" $f$.  This produces a split fibration (the chosen cartesian arrows are given by composition of morphisms in $C$), and it was proven by [Lumsdaine and Warren](#LumsdaineWarren13) that essentially all type formers can be extended to it from $E$.

=--


### Universes

Suppose given a particular morphism $p:\widetilde{U} \to U$ in $C$.  We can then define a category with attributes, def. \ref{CategoryWithAttributes}, as follows: the discrete fibration $E\to C$ corresponds to the representable presheaf $C(-,U)$, and the functor $E\to C^I$ is defined by pullback of $p$.  We are thus treating $U$ as a "[[universe]]" of types.  We may then of course pass to a contextual category, via example \ref{FromComprehensionToContextual}.

Type-forming operations may be extended strictly in this case by performing them once in the "universal" case, then acting by composition.  This construction is due to [[Voevodsky]].  It also meshes quite well with type theories that contain internal universes -- a [[type of types]]-- , and in particular for modeling the [[univalence axiom]].

Particular important universes include:

* Any [[Grothendieck universe]] in [[Set]], or more generally a [[universe in a topos]].  The resulting display maps are those with "$U$-small fibers".

* In the category [[Gpd]], the groupoid of small groupoids.  The resulting display maps are the [[split opfibrations]] with small fibers.  Similarly, we can consider the groupoid of small sets, whose display maps are the [[discrete opfibrations]] with small fibers.

* In the category [[sSet]] of [[simplicial sets]], there is a [[universal Kan fibration]] $p:\widetilde{U} \to U$ which classifies all [[Kan fibrations]] with small fibers.


### Simple fibrations

Let $C$ be any category with finite products, and define $E\to C$ to be the [[discrete fibration]] corresponding to the presheaf $C^{op}\to Set$ which is constant at $ob(C)$.  Thus, the objects of $E$ are pairs $(\Gamma,A)$ of objects of $C$, with the only morphisms being of the form $(\Gamma,A) \to (\Delta,A)$ induced by a morphism $\Gamma\to\Delta$ in $C$.

Define the functor $E\to C^I$ to take $(\Gamma,A)$ to the projection $\Gamma\times A \to \Gamma$.  It is straightforward to check that this defines a category with attributes.  The corresponding (split) full comprehension category is called the *simple fibration* of $C$.

The dependent type theory which results from this structure "has no nontrivial dependency".  That is, whenever we have a dependent type $\Gamma \vdash (A \;type)$, it is already the case that $A$ is a type in the empty context (that is, we have $\vdash (A\; type)$), and so it cannot depend nontrivially on $\Gamma$.  In effect, it is not really a dependent type theory, but a *simple* (non-dependent) type theory --- hence the name "simple fibration".


### The big model of locally cartesian closed categories

+-- {: .num_example #BigModelLocallyCartesianClosed}
###### Example

Ignoring coherence issues, the CwF induced by a locally cartesian closed (lcc) category $\mathcal{C}$ (example \ref{TypeTheoryModelFromLocallyCartesianClosedCategory}) is given explicitly by the "Explicit" column of the following table:

|                   | In $\mathcal{C}$: Explicit                                                             | In terms of slices of $\mathcal{C}$                                                                                | Big model                                                                         |
| ----------------- |----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Contexts          | Objects $\Gamma \in \mathcal{C}$                                     | Slice categories $\mathcal{C}_{/ \Gamma}$                                                         | Lcc categories $\Gamma$                                                           |
| Context Morphisms | Morphisms $f : \Gamma \rightarrow \Delta$                            | Lcc functors $f^* : \mathcal{C}_{/ \Delta} \rightarrow \mathcal{C}_{/ \Gamma}$ over $\mathcal{C}$ | Lcc functors $f : \Delta \rightarrow \Gamma$                                      |
| Types             | Morphisms $\sigma : \operatorname{dom} \sigma \rightarrow \Gamma$    | Objects $\sigma \in \mathcal{C}_{/ \Gamma}$                                                       | Objects $\sigma \in \Gamma$                                                       |
| Terms             | Sections $s : \Gamma \leftrightarrows \operatorname{dom} \sigma : \sigma$ | Morphisms $s : \mathrm{id}_\sigma \rightarrow \sigma$ in $\mathcal{C}_{/ \Gamma}$                 | Morphisms $s : 1 \rightarrow \sigma$ in $\Gamma$, where $1$ is a terminal object. |
| Substitution      | Pullback along $f$                                                   | Application of $f^*$                                                                              | Application of $f$

The next column describes the same CwF in the terminology of slice categories:
Every object of $\mathcal{C}$ corresponds to a slice category $\mathcal{C}_{/ \Gamma}$ over $\mathcal{C}$, and $\mathcal{C}_{/ \Gamma}$ is also lcc.
Every morphism $f : \Gamma \rightarrow \Delta$ in $\mathcal{C}$ induces a pullback functor $f^* : \mathcal{C}_{/ \Delta} \rightarrow \mathcal{C}_{/ \Gamma}$.
$f^*$ preserves the finite limits and dependent products of $\mathcal{C}_{/ \Delta}$ (i.e. it is an lcc functor), and the diagram
$$
  \array{
    && \mathcal{C}
    \\
    & {}_{\Delta^*} \swarrow && \searrow_{\Gamma^*}
    \\
    \mathcal{C}_{/ \Delta} && \stackrel{\to}{f^*} && \mathcal{C}_{/ \Gamma}
}
$$
commutes (up to unique isomorphism).
Conversely, every lcc functor $\mathcal{C}_{/ \Delta} \rightarrow \mathcal{C}_{/ \Gamma}$ under $\mathcal{C}$ is uniquely isomorphic to the pullback functor along some morphism $\Gamma \rightarrow \Delta$.

The last column describes the **big model** of type theory in the opposite category of lcc categories and lcc functors.
Since the contexts of this model are itself models of type theory, it can be understood as a "model of models".
The definition of the big model can be arrived at by removing all reference to the fixed lcc category $\mathcal{C}$ in the previous column.
Instead of just the slice categories of $\mathcal{C}$, now all lcc categories are allowed as contexts.
Context morphisms are generalized to general lcc functors instead of just the pullback functors of $\mathcal{C}$.
The identity morphism on an object $\Gamma$ of $\mathcal{C}$ is a terminal object in the slice category $\mathcal{C}_{/ \Gamma}$ and is thus generalized to a terminal object in any lcc category.

The usual model in a fixed lcc category $\mathcal{C}$ can be recovered from the big model by slicing:
The contextual core (example \ref{ContextualFromAttributes}) of the slice of the big model over $\mathcal{C}$ is equivalent to $\mathcal{C}$.

However, the naive definition of the big model above suffers from the same coherence issues as the standard models in individual lcc categories:
Lcc functors preserve lcc structure (i.e. type formers) up to isomorphism, but not necessarily up to equality.
These coherence problems can be resolved by working with a suitable model categorical presentation of the $(2, 1)$-category of lcc categories, lcc functors and natural isomorphisms.
Note that the [[model category]] presenting a higher category is unique up to zig-zag of Quillen equivalences, but that the underlying 1-categories of these model categories can vary non-trivially.
Because coherence issues are ultimately about equations in the underlying 1-category, we can thus hope that some model categories presenting the category of lcc categories will be better behaved than others for our purpose.

One possible way to construct such a well-behaved model category is as follows (see ([Bidlingmaier 2020](#Bidlingmaier20)) for details):

1. First one defines a model category $\mathrm{Lcc}$ of lcc sketches.
   An **lcc sketch** is a category with some diagrams [marked](#Isaev2016) as finite limits cones and evalution maps of dependent products.
   These marked diagrams do not need to satisfy the corresponding universal property, however.
   The model category structure is set up such that every object is cofibrant, and the fibrant objects are precisely the lcc categories with diagrams marked if and only if they satisfy the corresponding universal property.
   Thus the subcategory of fibrant objects of $\mathrm{Lcc}$ corresponds to the usual category of lcc categories.
   Note however, that lcc categories in the sense of fibrant lcc sketches "have" finite limits and dependent products in the sense that these universal objects _merely exist_; there are no distinguished/assigned choices of universal objects.
   Thus preservation of universal objects by functors up to equality (i.e. strictness of substitution) cannot even be stated in $\mathrm{Lcc}$.
2. The model category $\mathrm{sLcc}$ of **strict lcc categories** is defined as the category of [[algebraically fibrant objects]] of $\mathrm{Lcc}$; it is Quillen equivalent to $\mathrm{Lcc}$.
   Assigned lifts against the trivial cofibrations of $\mathrm{Lcc}$ correspond to distinguished choices of universal objects, and these choices are preserved by the morphisms of $\mathrm{sLcc}$, the **strict lcc functors**.
   Thus $\mathrm{sLcc}$ supports substitutions that preserve type formers up to equality.

   However, it does not support some dependent type formers in any obvious way, notably not $\Sigma$ and $\Pi$ types.
   The problem is that the context extension $\Gamma.\sigma$ of some $\Gamma \in \operatorname{Ob} \mathrm{sLcc}$ by a type (i.e. object) $\sigma$ of $\Gamma$ is given by freely (in the 1-categorical sense) adjoining a morphism $1 \rightarrow \sigma$ to $\Gamma$.
   To interpret $\Sigma$ and $\Pi$ types, one has to relate $\Gamma.\sigma$ with the slice category $\Gamma_{/ \sigma}$ in some way, and it appears that this is not generally possible.
   Note that $\Gamma_{/ \sigma}$ has the universal property of a context extension in the higher/bicategorical sense, but that $\Gamma.\sigma$ is defined purely 1-categorically.
3. To reconcile context extensions $\Gamma.\sigma$ with slice categories $\Gamma_{/ \sigma}$, one can work with the [algebraically cofibrant objects](#ChingRiehl2014) of $\mathrm{sLcc}$.
   An algebraically cofibrant object of $\mathrm{sLcc}$ is a coalgebra for a fixed cofibrant replacement comonad.
   The category of such coalgebras has model category structure, and this model category is again Quillen equivalent to $\mathrm{sLcc}$.

   A cofibrant object $\Gamma$ of $\mathrm{sLcc}$ has the property that every non-strict lcc functor (i.e. morphism of underlying lcc sketches) out of $\Gamma$ is isomorphic to a strict lcc functor.
   This property turns out to be sufficient to construct a weak equivalence $\Gamma.\sigma \rightarrow \Gamma_{/ \sigma}$ in $\mathrm{sLcc}$.
   For _algebraically_ cofibrant $\Gamma$, this weak equivalence is structure and hence preserved by coalgebra morphisms up to equality.
   This turns out to be sufficient to endow the category of algebraically cofibrant objects of $\mathrm{sLcc}$ with CwF structure that supports finite limit, $\Sigma$ and $\Pi$ type constructors.

=--

## Related pages

* [[categorical semantics]]

* [[relation between type theory and category theory]]

* [[initiality conjecture]]

* [[Awodey's conjecture]]

## References

Another overview can be found in the [HoTT wiki](https://ncatlab.org/homotopytypetheory/show/semantics).

A general overview may be found in

* [[Martin Hofmann]], *Syntax and semantics of dependent types*, Semantics and logics of computation (Cambridge, 1995), Publ. Newton Inst., vol. 14, Cambridge Univ. Press, Cambridge, 1997, pp. 79--130

Comprehension categories are defined in

* [[Bart Jacobs]], *Comprehension categories and the semantics of type dependency*, Theoret. Comput. Sci. 107 (1993), no. 2, 169--207

A 2-categorical treatment of variant kinds of comprehension category is given in 

* [[Paul-André Melliès]], Nicolas Rolland, _Comprehension and quotient structures in the language of 2-categories_, ([arXiv:2005.10015](https://arxiv.org/abs/2005.10015))

A correspondence with orthogonal factorization systems is discussed in

* Clemens Berger, Ralph M. Kaufmann, *Comprehensive factorisation systems* ([pdf](https://arxiv.org/abs/1710.09438))

Display maps are discussed in

* [[Paul Taylor]], _[[Practical Foundations of Mathematics]]_, section 8.3

Categories with attributes are discussed in

* John Cartmell, *Generalised algebraic theories and contextual categories*, Ph.D. thesis, Oxford, 1978 ([GitHub LaTeXing project](https://github.com/peterlefanulumsdaine/cartmell-thesis), organised by [[Peter LeFanu Lumsdaine]]. Currently only sections 1.0-1.4 are done)


* [[Eugenio Moggi]], *A category-theoretic account of program modules*, Math. Structures Comput. Sci. 1 (1991), no. 1, 103--139

* Andrew M. Pitts, *Categorical logic*, Handbook of logic in computer science, Vol. 5, Handb. Log. Comput. Sci., vol. 5, Oxford Univ. Press, New York, 2000, pp. 39--128

Categories with families are defined in

* [[Peter Dybjer]], *Internal type theory*, Types for proofs and programs (Torino, 1995), Lecture Notes in Comput. Sci., vol. 1158, Springer, Berlin, 1996, pp. 120--134, [PDF](http://www.cse.chalmers.se/~peterd/papers/InternalTT.pdf)

and shown to be equivalent to categories with attributes in

* [[Martin Hofmann]], *Syntax and semantics of dependent types*, [citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.8985).

The formulation in terms of representable natural transformations is in

* [[Steve Awodey]]. (2018). *Natural models of homotopy type theory*, Mathematical Structures in Computer Science, 28(2), 241-286. [PDF](https://arxiv.org/pdf/1406.3219.pdf)

See also

* Clive Newstead, _Algebraic models of dependent type theory_ ([arXiv:2103.06155](https://arxiv.org/abs/2103.06155)) 

A proof of initiality for dependent type theory is claimed in

* Simon Castellan, _Dependent type theory as the initial category with families_, 2014 ([pdf](http://iso.mor.phis.me/archives/2011-2012/stage-2012-goteburg/report.pdf))

This was formalized inside type theory with set quotients of [[higher inductive types]] in:

* {#AltKap2015} [[Thorsten Altenkirch]], Ambrus Kaposi, _Type Theory in Type Theory using Quotient Inductive Types_, (2015) ([pdf](http://www.cs.nott.ac.uk/~txa/publ/tt-in-tt.pdf)), ([formalisation in Agda](https://bitbucket.org/akaposi/tt-in-tt)).


Contextual categories were defined in

* {#Cartmell86} John Cartmell, _Generalised algebraic theories and contextual categories_, Annals of Pure and Applied Logic Volume 32, 1986, Pages 209-243 ([doi:10.1016/0168-0072(86)90053-9](http://dx.doi.org/10.1016/0168-0072%2886%2990053-9))

* {#Streicher91} [[Thomas Streicher]], *Semantics of type theory*, Progress in Theoretical Computer Science, Birkh&#228;user Boston Inc., Boston, MA, 1991, Correctness, completeness and independence results.

Review includes

* {#KapulkinLumsdaine12} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], section 1.2 and appendix B of _The Simplicial Model of Univalent Foundations (after Voevodsky)_ ([arXiv:1211.2851](https://arxiv.org/abs/1211.2851))

Contextual categories as models for [[homotopy type theory]] are discussed in

* {#KapulkinLumsdaine16} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], _The homotopy theory of type theories_ ([arXiv:1610.00037](https://arxiv.org/abs/1610.00037))

* {#Joyal17} [[André Joyal]], _Notes on Clans and Tribes_ ([arXiv:1710.10238](https://arxiv.org/abs/1710.10238))

* See also [[clan]].

Further discussion of contextual categories is in

* {#Voevodsky15a} [[Vladimir Voevodsky]], _A C-system defined by a universe category_, Theory Appl. Categ. 30 (2015), No. 37, 1181&#8211;1215, arXiv:1409.7925 ([arXiv:1409.7925](https://arxiv.org/abs/1409.7925))

* {#Voevodsky15b} [[Vladimir Voevodsky]], _Martin-L&#246;f identity types in the C-systems defined by a universe category_ ([arXiv:1505.06446](https://arxiv.org/abs/1505.06446))

* {#Voevodsky15c} [[Vladimir Voevodsky]], _Products of families of types in the C-systems defined by a universe category_ ([arXiv:1503.07072](https://arxiv.org/abs/1503.07072))

* {#Voevodsky15d} [[Vladimir Voevodsky]], _Subsystems and regular quotients of C-systems_ ([arXiv:1406.7413](https://arxiv.org/abs/1406.7413))


Strictification is discussed in

* [[Martin Hofmann]], *On the interpretation of type theory in locally cartesian closed categories*

* {#CurienGarnerHofmann} [[Pierre-Louis Curien]], [[Richard Garner]], [[Martin Hofmann]], _Revisiting the categorical interpretation of dependent type theory_ ([[CurienGarnerHofmann.pdf:file]])

* {#LumsdaineWarren13} [[Peter LeFanu Lumsdaine]], [[Michael Warren]], _The local universes model: An overlooked coherence construction for dependent type theory_, [arXiv:1411.1736](https://arxiv.org/abs/1411.1736), ACM Transactions on Computational Logic.

* [[Vladimir Voevodsky]], [Notes on type systems](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/expressions_current.pdf)

* {#Awodey2018} [[Steve Awodey]]. (2018). *Natural models of homotopy type theory*, Mathematical Structures in Computer Science, 28(2), 241-286. [PDF](https://arxiv.org/pdf/1406.3219.pdf)

Comparisons of various models can be found in

* [[Benedikt Ahrens]], [[Peter LeFanu Lumsdaine]], [[Vladimir Voevodsky]], *Categorical structures for type theory in univalent foundations*, [arxiv](https://arxiv.org/abs/1705.04310)

* {#KapulkinLumsdaine16} [[Chris Kapulkin]] and [[Peter LeFanu Lumsdaine]], *The homotopy theory of type theories*, [arXiv:1610.00037](https://arxiv.org/abs/1610.00037)

Recent work on abstract definitions of (models of) type theory include:

* Valery Isaev, _Algebraic Presentations of Dependent Type Theories_ [arXiv](https://arxiv.org/abs/1602.08504)

* Taichi Uemura, _A General Framework for the Semantics of Type Theory_ [arXiv](https://arxiv.org/abs/1904.04097)

A category with families structure is constructed on the $(2,1)$-category of all locally cartesian closed categories, which since locally presentable may be treated via model categories, in:

* {#Bidlingmaier20} Martin Bidlingmaier, _An interpretation of dependent type theory in a model category of locally cartesian closed categories_, ([arXiv:2007.02900](https://arxiv.org/abs/2007.02900))

* {#ChingRiehl2014} Michael Ching, Emily Riehl, _Coalgebraic models for combinatorial model categories_ [arXiv:1403.5303](https://arxiv.org/abs/1403.5303) 

* {#Isaev2016} Valery Isaev, _Model category of marked objects_ [arXiv:1610.08459](https://arxiv.org/abs/1610.08459)



[[!redirects categorical model of dependent types]]
[[!redirects categorical models of dependent types]]
[[!redirects category-theoretic model of dependent types]]
[[!redirects category-theoretic models of dependent types]]
[[!redirects split model of type theory]]
[[!redirects split models of type theory]]
[[!redirects categorical semantics of dependent types]]
[[!redirects category-theoretic semantics of dependent types]]

[[!redirects comprehension category]]
[[!redirects comprehension categories]]
[[!redirects display map category]]
[[!redirects display map categories]]
[[!redirects category with attributes]]
[[!redirects categories with attributes]]
[[!redirects category with families]]
[[!redirects categories with families]]
[[!redirects contextual category]]
[[!redirects contextual categories]]
[[!redirects C-system]]
[[!redirects C-systems]]