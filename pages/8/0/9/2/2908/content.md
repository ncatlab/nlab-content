
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Algebraic categories
* table of contents
{: toc}


## Idea

An algebraic category is a [[concrete category]] which behaves very much like the categories familiar from [[algebra]], such as [[Grp]], [[Ring]], and [[Vect]], but characterised in category-theoretic terms.  But many other categories are also algebraic, most famously [[compact Hausdorff space|CompHausTop]]; one can describe these in purely algebraic terms, but only using infinitary (perhaps even largely many) operations.

There are several definitions of 'algebraic' in the literature.  Here, we will follow AHS (see references) in using a generous interpretation, but other authors follow Johnstone in using 'algebraic' to mean monadic (a stricter requirement), while some authors add finiteness conditions that remove examples such as $Comp Haus Top$.  However, all of these notions are related, and we will discuss them here.

The definitions in AHS also includes a requirement violating the [[principle of equivalence]], which we omit: that of unique strict lifts of isomorphisms, which serves to fix algebraic categories up to [[isomorphism of categories|isomorphism]] (instead of mere [[equivalence of categories|equivalence]]).


## Definitions

Let $A$ be a [[concrete category]]; that is, $A$ is equipped with a [[forgetful functor]] $U\colon A \to Set$ to the [[Set|category of sets]].  For some authors, such a category is called 'concrete' only if $U$ is [[representable functor|representable]], but that follows in all the cases considered below; in particular, if $A$ has free objects (that is, if $U$ has a [[left adjoint]] $F$), then $U$ is representable by $F(1)$, where $1$ is a [[singleton]].

+-- {: .un_defn}
###### Definition (based on AHS 23.38)

The concrete category $A$ is __algebraic__ if the following conditions hold:

*  $A$ has [[free objects]].
*  The category $A$ has all binary [[coequalizers]].
*  The forgetful functor $U$ preserves and reflects [[extremal epimorphisms]].
=--

+-- {: .un_defn}
###### Definition (based on AHS ...)

The concrete category $A$ is __monadic__ if the following conditions hold:

*  $A$ has [[free objects]].
*  The [[adjunction]] $F \dashv U$ is [[monadic adjunction|monadic]].
=--

+-- {: .un_defn}
###### Definition (based on AHS 24.11)

An algebraic (or monadic) category is __bounded__ if the following condition holds:

*  For some [[cardinal number]] $\kappa$ and every $\kappa$-[[directed colimit]] in $A$, the universal [[cocone]] is jointly [[surjection|surjective]] in $Set$.
=--

+-- {: .un_defn}
###### Definition (based on AHS 24.4)

An algebraic (or monadic) category is __finitary__ if the following condition holds:

*  For every finitely [[directed colimit]] in $A$, the universal [[cocone]] is jointly [[surjection|surjective]] in $Set$.
=--

Note that this is a weakening of the condition that the forgetful functor $U$ is [[finitary functor|finitary]] (that is, that $U$ preserves directed colimits); every universal cocone in $Set$ is jointly surjective, but not conversely.


## Properties

Every monadic category is algebraic; an algebraic category is monadic if and only if the forgetful functor $U$ preserves [[congruences]].  (AHS 23.41)

A category is algebraic if and only if it is a [[reflective subcategory]] of a monadic category with [[regular epimorphism|regular epic]] reflector; given an algebraic category, this monadic category is the [[Eilenberg–Moore category]] of the monad $U \circ F$.  (AHS 24.3)

Every monadic category is the category of algebras for some [[variety of algebras]], although we must allow potentially a [[proper class]] of infinitary axioms; that is, every monadic category is [[equationally presentable category|equationally presentable]].  Similarly, every algebraic category is the category of algebras for some [[quasivariety of algebras]]; that is, we allow [[conditional statements]] of equations among the axioms.  (AHS 24.11)

As special cases of the last item:

*  A concrete category is bounded monadic if and only if it is equationally presentable (presented by a variety) with a small set of operations (and hence equations).
*  A concrete category is bounded algebraic if and only if it is presented by a quasivariety with a small set of operations.
*  A concrete category is finitary monadic if and only if it is the category of algebras for some finitary variety; that is, we have only a small set of finitary operations.
*  A concrete category is finitary algebraic if and only if it is the category of algebras for some finitary quasivariety.

Also, every algebraic category whose [[forgetful functor]] preserves [[filtered colimits]] is the category of [[models]] for some [[first-order theory]]. The converse is false.

## Examples

The typical categories studied in [[algebra]], such as [[Grp]], [[Ring]], [[Vect]], etc, are all finitary monadic categories.  The [[monad]] $U \circ F$ may be thought of as mapping a set $x$ to the set of words with alphabet taken from $x$ and the connections between letters taken from the appropriate algebraic operations, with two words identified if they can be proved equal by the appropriate algebraic axioms.

The category of cancellative [[monoids]] is finitary algebraic but not monadic. The category [[Field]] of [[fields]] is not even algebraic.

Assuming the [[ultrafilter principle]], the category of [[compact Hausdorff spaces]] is monadic, but not bounded algebraic.  The monad in question takes a set $x$ to the set of [[ultrafilters]] on $x$.  (Without the ultrafilter principle, this monad still exists, but it may be quite small, possibly even the [[identity monad]]; passing to [[locales]] does not help.)

Similarly, the category of [[Stone space]]s is algebraic, but not monadic or bounded algebraic.


## References

The original definitions can be found in

* [[F. William Lawvere]], _Algebraic theories, algebraic categories, and algebraic functors_. 1965 Theory of Models (Proc. 1963 Internat. Sympos. Berkeley), 413–418. North-Holland, Amsterdam.

Our definitions are taken from

*  **AHS**: [[Jiri Adamek|Jiří Adámek]], [[Horst Herrlich]], [[George Strecker]]; _Abstract and Concrete Categories: [[The Joy of Cats]]_, Sections 23 &amp; 24; [web](http://katmat.math.uni-bremen.de/acc).

Actually, AHS discusses the more general concept of algebraic (etc) *functors*, generalising from $U\colon A \to Set$ to arbitrary functors (not necessarily faithful, not necessarily to $Set$).  We actually take our definitions from AHS\'s characterisation theorems in the case of faithful functors to $Set$.  We probably should discuss the more general concept, perhaps at [[algebraic functor]]; we already have [[monadic functor]].

*  [[Peter Johnstone]]; _[[Stone Spaces]]_, Section 3.8

For Johnstone, a concrete category is 'algebraic' if and only if it is monadic.  However, Johnstone also discusses [[equationally presentable category|equationally presentable categories]].

Another modern reference is

* [[Jiří Adámek]], [[Jiří Rosický]], [[Enrico M. Vitale]],
_Algebraic theories_,
Cambridge Tracts in Mathematics 184 (2011), Cambridge University Press.
doi:10.1017/cbo9780511760754.


[[!redirects algebraic category]]
[[!redirects algebraic categories]]
[[!redirects bounded algebraic category]]
[[!redirects bounded algebraic categories]]
[[!redirects finitary algebraic category]]
[[!redirects finitary algebraic categories]]

[[!redirects monadic category]]
[[!redirects monadic categories]]
[[!redirects bounded monadic category]]
[[!redirects bounded monadic categories]]
[[!redirects finitary monadic category]]
[[!redirects finitary monadic categories]]