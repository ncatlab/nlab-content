
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Categorical models of dependent types
* table of contents
{: toc}

## Idea

In the [[relation between type theory and category theory]], [[dependent types]] are said to correspond to morphisms regarded as indexed families.  That is, if a [[type]] $A$ corresponds to an [[object]], then a dependent type

$$ (x:A) \;\vdash\; (B(x) \;type) $$

corresponds to a morphism $B\to A$.  We think of this morphism as a [[bundle]] or [[fibration]], whose [[fiber]] over $x:A$ is the type $B(x)$.  We can then say that [[type former|type forming operations]] such as [[dependent sum type]] and [[dependent product type]] correspond to category-theoretic operations of [[dependent sum]] and [[dependent product]].

However, this correspondence is not quite precise; in the case of dependent types there are extra coherence issues.  [[substitution|Substitution]] in type theory should correspond to [[pullback]] in category theory; that is, given a term

$$ (y:C) \;\vdash\; (f(y) : A) $$

corresponding to a morphism $f:C\to A$, the substituted dependent type

$$ (y:C) \;\vdash\; (B(f(y)) \;type) $$

should correspond to the pullback of $B\to A$ along $f$.  However, substitution in type theory is strictly associative.  That is, given also $g:D\to C$, the dependent type

$$ (z:C) \;\vdash\; (B(f(g(z))) \;type)$$

is syntactically the same regardless of whether we obtain it by substituting $y \coloneqq g(z)$ into $B(f(y))$, or $x \coloneqq f(g(z))$ into $B(x)$.  In category theory, however, pullback is not generally strictly associative, so there is a mismatch.  Similarly, every type-forming operation must also be strictly preserved by substitition/pullback.

The way this is generally dealt with is to introduce a category-theoretic structure which does have a "substitution" operation which is strictly associative, hence does correspond directly to type theory, and then show that any category can be "strictified" into such a stricter structure.  Unfortunately, there are many different such structures which have been used, differing only slightly.  On this page we define and compare them all.

## Definitions

In all the definitions, $C$ will be a [[category]].  Generally, we will regard the objects of $C$ as [[contexts]] in a type theory.

So far, we do not assume anything about $C$ as a category.  Usually, one at least wants $C$ to have a [[terminal object]], representing the empty context, although this is not always included in the definitions.  The additional structures we impose on $C$ below will imply in particular that certain [[pullbacks]] exist in $C$.

Sometimes, we want to consider $C$ as a [[strict category]], that is, we consider its objects up to equality rather than isomorphism.  However, for most of the definitions below (until we get to contextual categories), it is still sensible to treat $C$ in an ordinary category-theoretic way, with the strictness living in the additional structure.


### Comprehension categories

+-- {: .num_defn #ComprehensionCategory}
###### Definition
A **comprehension category** consists of a commutative triangle
$$ \array{ E && \to && C^I\\ & \searrow && \swarrow\\ && C } $$
where $C^I$ is the [[arrow category]] of $C$, and such that

1. $E\to C$ is a [[Grothendieck fibration]], and 
1. $E\to C^I$ takes [[cartesian morphisms]] in $E$ to cartesian morphisms in $C^I$ (i.e. to [[pullback]] squares in $C$).
=--

Note that we do not ask that $C^I\to C$ be a fibration (that would require $C$ to have all pullbacks), only that the *particular* morphisms in the image of $E$ are cartesian.

A comprehension category is called **full** if $E\to C^I$ is a [[fully faithful functor]].  It is called **split** if $E\to C$ is a [[split fibration]].  Note that in the latter case, we must consider $E$ at least to be a [[strict category]] (that is, we consider its objects up to equality rather than isomorphism) for the notion to make sense.

In a comprehension category, we may regard the objects of $C$ as contexts, and the fiber $E^\Gamma$ of $E\to C$ over an object $\Gamma$ as the category of dependent types in context $\Gamma$.  If the comprehension category is split, then such dependent types have strictly associative substition.

The functor $E\to C^I$ assigns to each "type $A$ in context $\Gamma$" a new context which we think of as $\Gamma$ *extended* by a fresh [[variable]] of type $A$, and write as $\Gamma.A$.  This new context $\Gamma.A$ comes with a projection $\Gamma.A\to \Gamma$ (which forgets the fresh variable), and all substitutions in $E$ are realized as pullbacks in $C$.


### Display map categories

+-- {: .num_defn #DisplayMapCategory}
###### Definition
A **display map category** consists of a category $C$ together with a class $D$ of morphisms in $C$ called [[display maps]], such that all pullbacks of display maps exist and are display maps.
=--

If $C$ is a display map category, then by defining $E$ to be the [[full subcategory]] of $C^I$ whose objects are display maps, we obtain a full comprehension category.  Thus, we have:

+-- {: .num_lemma #DMCasCmpC}
###### Lemma
Display map categories may be identified with comprehension categories for which the functor $E\to C^I$ is the inclusion of a full subcategory.
=--

Working up to [[equivalence of categories]], as is usual in category theory, it is natural to consider display map categories to also be equivalent to *full* comprehension categories (those where $E\to C^I$ is merely fully faithful).

However, this breaks down when we are interested in *split* comprehension categories for modeling substitution with strict associativity, since then $E$ at least must be regarded as a [[strict category]] and considered up to [[isomorphism]] rather than equivalence.  Thus, display map categories may be said to be equivalent to non-split full comprehension categories, but "split display map categories" are not equivalent to split full comprehension categories.  (In fact, split display map categories are not very useful; usually in order to make pullbacks strictly associative we have to introduce extra "names" for the same objects.)


### Categories with attributes

+-- {: .num_defn #CategoryWithAttributes}
###### Definition
A **category with attributes** is a comprehension category for which $E\to C$ is a [[discrete fibration]].
=--

That is, in a category with attributes we demand only that each context come with a [[set]] of dependent types in that context, rather than a category of such.  The intent is that the morphisms between two types in context $\Gamma$ should be determined by the morphisms in $C$ between the extended contexts over $\Gamma$.

Another way to convey this same intent with a comprehension category would be to ask that it be *full*, i.e. that the functor $E\to C^I$ be fully faithful.  In fact, any category with attributes gives rise to a full comprehension category by factoring the functor $E\to C^I$ into a [[bijective on objects functor]] followed by a fully faithful one.  In this way, we obtain:

+-- {: .num_lemma #CWAasCmpC}
###### Lemma
Categories with attributes are equivalent to full split comprehension categories.
=--


### Categories with families

A category with attributes specifies only for each "context", a set of "types" in that context.  A comprehension category, by contrast, specifies a whole *category* of "types" in each context.  If $A,B\in E^\Gamma$, then we can think of a morphism $f:A\to B$ in $E^\Gamma$ as a term

\[ (\vec{x} : \Gamma), (a:A(\vec{x})) \;\vdash\; (f(\vec{x},a) : B(\vec{x})) \label{cmpcterm} \]

in type theory.  A *category with families* specifies instead, for each context and each type in that context, a set of "terms belonging to that type".  These should be thought of as terms

\[ (\vec{x} : \Gamma) \;\vdash\; (f(\vec{x}) : B(\vec{x})) \label{cwfterm} \]

in type theory.  Note that a term of the form (eq:cmpcterm) can equivalently be regarded as a term of the form (eq:cwfterm) by replacing $\Gamma$ by the extended context $\Gamma.A$, and $B$ by its substitution along the projection $\Gamma.A \to \Gamma$.

The additional insight in the following definition is that if we expect all of these terms to be determined by the morphisms in $C$, as in a category with attributes or a full comprehension category, then instead of specifying the functor $E\to C^I$ and then asking either that it be fully faithful or that $E$ be discrete (removing the information about extra morphisms in $E$), if we specify the terms of the form (eq:cwfterm), then the functor $E\to C^I$ is determined by a universal property.

Let $Fam$ denote the category of families of sets.  Its morphisms are set-indexed families $(A_i)_{i\in I}$, and its morphisms $(A_i)_{i\in I} \to (B_j)_{j\in J}$ consist of a function $f\colon I\to J$ and functions $g_j \colon A_i \to B_{f(i)}$.  We can equivalently, of course, regard this as the arrow category $Set^I$ of [[Set]], where $(A_i)_{i\in I}$ corresponds to the arrow $\coprod A \to I$.

+-- {: .num_defn #CategoryWithFamilies}
###### Definition
A **category with families** is a category $C$ together with

* A functor $F:C^{op} \to Fam$, written $F(\Gamma) = (Tm(A))_{A\in Ty(\Gamma)}$.

* For each $\Gamma\in C$ and $A\in Ty(\Gamma)$, a [[representing object]] for the functor
  $$
  \begin{aligned}
    (C/Gamma)^{op} & \to Set\\
    (\Delta \xrightarrow{f} \Gamma) & \to Tm(f^*(A))
  \end{aligned}
  $$
=--

+-- {: .query}
It seems to me that categories with families are actually equivalent to categories with attributes.  But I haven't seen this stated anywhere in the literature, so I feel like there must be some subtlety I'm not getting.
=--


### Contextual categories

Recall that if $C$ is a comprehension category, $\Gamma\in C$ is a "context" and $A\in E^\Gamma$ is a "type" in context $\Gamma$, we denote by $\Gamma.A$ the "extended context" in $C$.

+-- {: .num_defn #ContextualCategory}
###### Definition
A **contextual category** is a category with attributes $C$, together with a *length function* $\ell : ob(C) \to \mathbb{N}$ such that

1. There is a unique object of length $0$, which is a [[terminal object]].
1. For any $\Gamma\in C$ and $A\in E^\Gamma$, we have $\ell(\Gamma.A) = \ell(\Gamma)+1$.
1. For any $\Delta\in C$ with $\ell(\Delta)\gt 0$, there exists a unique $\Gamma\in C$ and $A\in E^\Gamma$ such that $\Delta = \Gamma.A$.
=--

Since the definition refers to equality of objects, a contextual category $C$ must be a [[strict category]].  The idea which distinguishes a contextual category is that "every context must be built out of types" in a unique way.  This makes for the closest match with type theory; in fact we have

+-- {: .num_theorem #CxtCareTT}
###### Theorem
The category of contextual categories and (strictly) structure-preserving functors is [[equivalence of categories|equivalent]] to the category of dependent type theories and interpretations.
=--

Note that since contextual categories are strict categories, the category of such is really a 1-category, or perhaps a [[strict 2-category]].

Given any category with attributes $C$ possessing a terminal object, there is a canonical way to build a contextual category from it.  Choose a terminal object $1\in C$ (the resulting contextual category does not depend on this choice, up to isomorphism).  Define the objects of $cxt(C)$ to be the finite lists

$$(A_0,A_1,\dots,A_n)$$

such that $A_0 \in E^1$ and $A_{k+1} \in E^{1.A_0.A_1.\cdots .A_k}$ for all $k$.  Define the morphisms $(A_0,\dots,A_n) \to (B_0,\dots,B_m)$ in $cxt(C)$ to be the morphisms $1.A_0.A_1.\cdots.A_n \to 1.B_0.B_1.\cdots.B_m$ in $C$.  All the rest of the structure is induced in an evident way from $C$.

## Examples

There are several ways to construct categories with the above structure out of categories that occur "in nature".  But first we should mention the examples that come from type theory itself.

### Syntactic categories

The [[syntactic category]] of any dependent type theory has all of the above structures.  Its objects are [[contexts]] in the theory, and the types in context $\Gamma$ form the set or category $E^\Gamma$.  The strict associativity of substitution in type theory makes this fibration automatically split.


### Splitting fibrations

There are standard constructions which can replace any fibration by an equivalent split fibration.  Therefore, given any comprehension category, we may replace it by a split one, then consider the underlying category with attributes, and finally pass to a contextual category as described above.

Of course, comprehension categories are easy to come by; perhaps they arise most commonly as display map categories.  For instance, if $C$ has all pullbacks, then we can take all maps to be display.  If $C$ is a [[category of fibrant objects]], we can take the fibrations to be the display maps.

It turns out that for modeling additional type-forming operations, however, not all splitting constructions are created equal.  Given $E\to C$, one classical construction (due to Power) defines $E'\to C$, where an object of $E'$ over $\Gamma\in C$ consists of a morphism $f:\Gamma \to \Delta$ in $C$ along with an object $A$ of $E$ over $\Delta$.  Type-theoretically, we can regard $(f,A)$ as a type $A$ with a "delayed substitution" $f$.  This produces a split fibration (the chosen cartesian arrows are given by composition of morphisms in $C$), but it seems impossible to define dependent sums and products on it in a strict way.

A better choice is a construction due to Benabou, which defines the objects of $E'$ over $\Gamma\in C$ to be functors $C/\Gamma \to E$ over $C$ which map every morphism of $C/\Gamma$ to a cartesian arrow.  Type-theoretically, we can think of such an object as a type together with *specified* compatible substitutions along any possible morphism.  That type-formers can be extended in this case was proven by Martin Hofmann for dependent sums and products and extensional identity types, and by Michael Warren in the case of intensional identity types.


### Universes

Suppose given a particular morphism $p:\widetilde{U} \to U$ in $C$.  We can then define a category with attributes as follows: the discrete fibration $E\to C$ corresponds to the representable presheaf $C(-,U)$, and the functor $E\to C^I$ is defined by pullback of $p$.  We are thus treating $U$ as a "universe" of types.  We can then of course pass to a contextual category, as described above.

Type-forming operations can be extended strictly in this case by performing them once in the "universal" case, then acting by composition.  This construction is due to Voevodsky.  It also meshes quite well with type theories that contain internal universes, and in particular for modeling the [[univalence axiom]].


## References

A general overview can be found in

* Martin Hofmann, *Syntax and semantics of dependent types*, Semantics and logics of computation (Cambridge, 1995), Publ. Newton Inst., vol. 14, Cambridge Univ. Press, Cambridge, 1997, pp. 79--130

Comprehension categories are defined in

* [[Bart Jacobs]], *Comprehension categories and the semantics of type dependency*, Theoret. Comput. Sci. 107 (1993), no. 2, 169--207

Display maps are discussed in

* [[Paul Taylor]], _[[Practical Foundations of Mathematics]]_, section 8.3

Categories with attributes are discussed in

* John Cartmell, *Generalised algebraic theories and contextual categories*, Ph.D. thesis, Oxford, 1978

* Eugenio Moggi, *A category-theoretic account of program modules*, Math. Structures Comput. Sci. 1 (1991), no. 1, 103--139

* Andrew M. Pitts, *Categorical logic*, Handbook of logic in computer science, Vol. 5, Handb. Log. Comput. Sci., vol. 5, Oxford Univ. Press, New York, 2000, pp. 39--128

Categories with families are defined in

* Peter Dybjer, *Internal type theory*, Types for proofs and programs (Torino, 1995), Lecture Notes in Comput. Sci., vol. 1158, Springer, Berlin, 1996, pp. 120--134

Contextual categories are defined in

* John Cartmell, *Generalised algebraic theories and contextual categories*, Ann. Pure Appl. Logic 32 (1986), no. 3, 209--243

* [[Thomas Streicher]], *Semantics of type theory*, Progress in Theoretical Computer Science, Birkh&#228;user Boston Inc., Boston, MA, 1991, Correctness, completeness and independence results.

Strictification is discussed in

* [[Martin Hofmann]], *On the interpretation of type theory in locally cartesian closed categories*

* [[Vladimir Voevodsky]], [Notes on type systems](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/expressions_current.pdf)


[[!redirects categorical model of dependent types]]
[[!redirects categorical models of dependent types]]
[[!redirects category-theoretic model of dependent types]]
[[!redirects category-theoretic models of dependent types]]
[[!redirects split model of type theory]]
[[!redirects split models of type theory]]

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
