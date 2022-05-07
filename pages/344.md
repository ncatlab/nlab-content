
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Regular and Exact categories
+-- {: .hide}
[[!include regular and exact categories - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


* table of contents
{: toc}

## Idea

A [[category]] is _extensive_ if it has [[coproducts]] that interact well with [[pullbacks]].  Variations (some only terminological) include _lextensive_, _disjunctive_, and _positive_ categories.  All of these come in _finitary_ and _infinitary_ versions (and, more generally, $\kappa$-ary versions for any [[arity class]] $\kappa$).

## Definitions

A __finitely extensive category__ (or __finitary extensive category__) is a category $E$ with finite [[coproduct|coproducts]] such that one, and hence all, of the following equivalent conditions holds:

 1. Pullbacks of finite-coproduct injections along arbitrary morphisms exist and finite coproducts are [[disjoint coproduct|disjoint]] and [[pullback stability|stable under pullback]].
 2. For any objects $a,b$ the coproduct functor $E/a \times E/b \to E/(a+b)$ is an [[equivalence of categories]].
 3. Pullbacks of finite-coproduct injections (and thus all coproduct injections) along arbitrary morphisms exist, and in any commutative diagram
 $$\array{x & \to & z & \leftarrow & y\\
   \downarrow  & &   \downarrow  &  &  \downarrow \\
   a & \to & a+b & \leftarrow & b}$$
 the two squares are pullbacks if and only if the top row is a coproduct diagram.
 4. Finite coproducts are [[van Kampen colimits]].  By definition, this is to say one of the previous two conditions (depending on the definition chosen).

An __infinitary extensive category__ is a category $E$ with all (small) [[coproduct]]s such that the following analogous equivalent conditions hold:

 1. Pullbacks of coproduct injections along arbitrary morphisms exist and small coproducts are [[disjoint coproduct|disjoint]] and stable under pullback.
 2. For any small family $(a_i)$ of objects, the coproduct functor $\prod_i (E/a_i) \to E/_{(\coprod_i a_i)}$ is an equivalence of categories.
 3. Pullbacks of finite-coproduct injections (and thus all coproduct injections) along arbitrary morphisms exist, and for any family of commutative squares
 $$\array{ x_i & \to & z \\\downarrow &&\downarrow^f \\ a_i & \to & \coprod_i a_i } $$
 in which the bottom family of morphisms is the coproduct injections and the right-hand morphism is always the same, the top family are the injections of a coproduct diagram (hence $z = \coprod_i x_i$) if and only if all the squares are pullbacks.
 4. All small coproducts are [[van Kampen colimits]].

In between, a __$\kappa$-ary extensive category__ (for $\kappa$ a [[cardinal number]] or an [[arity class]]) is one with disjoint and stable coproducts of fewer than $\kappa$ objects.  The unqualified term **extensive category** can refer to either the finitary or infinitary version, depending on the author; the more usual meaning is the finitary version.

Extensive categories are also called __positive categories__, especially if they are also [[coherent category|coherent]].  Note that any disjoint coproduct in a coherent category is automatically pullback-stable.  A positive coherent category which is also [[exact category|exact]] is called a [[pretopos]].  Infinitary pretoposes encapsulate all the exactness conditions of Giraud's theorem characterizing [[Grothendieck topos|Grothendieck toposes]] (the remaining condition is the existence of a small [[generating set]]).

If an extensive category also has [[finitely complete category|finite limits]], it is called __lextensive__ or __disjunctive__.  (Note that the more usual default meaning of 'disjunctive', unlike the other terms, is the infinitary case.)


## Remarks

* The alternative definitions of finitary disjunctive refer only to binary coproducts, but they obviously imply analogous statements for $n$-ary coproducts for all finite $n \ge 1$.  Less obviously, they also imply the analogous statement for $0$-ary coproducts (that is, [[initial object]]s).  In this case, the statement is that the initial object 0 is _strict_ (any map $a\to 0$ is an isomorphism).

* Furthermore, if binary coproducts are disjoint, then (at least assuming [[classical logic]]) any infinitary coproducts that exist are also disjoint, since
  $$\bigsqcup_{a\in A} X_a \cong
X_{a_0} \sqcup \bigsqcup_{a\neq a_0} X_a \cong
X_{a_0} \sqcup X_{a_1} \sqcup \bigsqcup_{a\neq a_0,a_1} X_a$$
  for any $a_0, a_1\in A$.  Therefore, if a finitary-extensive category has infinitary pullback-stable coproducts, it is necessarily infinitary-extensive.  In particular, a cocomplete [[locally cartesian closed category]] is finitary extensive if and only if it is infinitary extensive.

* As a further special case of the preceding, since an [[elementary topos]] is finitary extensive, any cocomplete elementary topos is infinitary extensive.  However, in this case, one of the arguments for finitary extensivity applies directly to the infinitary case and does *not* require classical logic; see [[toposes are extensive]].

* See [[familial regularity and exactness]] for a generalization of extensivity and its relationship to [[exact category|exactness]].

* Any extensive category with finite [[products]] is automatically a [[distributive category]].


## Examples

1. An [[elementary topos]] (or, more generally, any [[pretopos]]) is finitary lextensive; a [[Grothendieck topos]] (or, more generally, any [[cocomplete category|cocomplete]] elementary topos) is infinitary lextensive.

1. A [[quasitopos]] with disjoint coproducts, or more generally a [[locally cartesian closed category]] with disjoint coproducts, is extensive. (Of course not all quasitoposes have disjoint coproducts, one example being a [[complete Heyting algebra]].) 

1. The category [[Top]] of [[topological spaces]] is infinitary lextensive.  The category [[Diff]] of [[smooth manifolds]] is infinitary extensive, though it does not have all [[pullbacks]] (only those involving a [[cospan]] of [[transversal maps]]).

1. The category of [[schemes]] is infinitary lextensive. In more detail: the category of functors $CRing \to Set$ is infinitary lextensive (since finite limits and small coproducts are computed pointwise in $Set$), then sheaves with respect to the Zariski topology on $CRing^{op}$ form an infinitary lextensive category (since finite limits and small coproducts are reflected back from $[CRing, Set]$ by applying a left exact reflection to the inclusion of sheaves in presheaves). Finally, the category of schemes, as a full subcategory of the Zariski sheaves, are closed under finite limits and small coproducts. (Some discussion of these points can be found at the [nForum](http://nforum.mathforge.org/discussion/5149/extensive-category/), particularly in comment #18.) 

1. The category of affine schemes (opposite to the category of commutative [[ring]]s with identity) is lextensive, but (perhaps contrary to geometric intuition) _not_ infinitary lextensive. Some details may be found [here](http://ncatlab.org/toddtrimble/published/Dippy+disproof+of+infinitary+extensivity+of+affine+schemes). 

1. The category [[Cat]] is infinitary lextensive.

1. The category [[Vect]] is not even finitely extensive.


## Superextensive sites

Any extensive category admits a [[Grothendieck topology]] whose [[cover|covering families]] are (generated by) the families of inclusions into a [[coproduct]] (finite or small, as appropriate).  We call this the **extensive [[coverage]]** or **extensive topology**.  The [[codomain fibration]] of any extensive category is a [[stack]] for its extensive topology.

In general, we call a [[site]] __superextensive__ if its underlying category is extensive, its covering families are generated by (finite or small) families, and its coverage includes the extensive one.  See [[superextensive site]] for more details.


## Pre-lextensive categories

Extensivity is an "exactness" condition, analogous to being a [[exact category]] or a [[pretopos]] (a pretopos being precisely a category that is exact and finitary-extensive).  The corresponding "regularity" condition analogous to being a [[regular category]] or a [[coherent category]] is not well-known, but is not hard to write down.

Let us say (without making any assertion that this is good or permanent terminology) that a category is **pre-lextensive** if 

1. it has a [[strict initial object]] $0$ (equivalently, its [[subobject]] [[preorders]] have pullback-stable bottom elements), and
1. whenever $A\rightarrowtail X$ and $B\rightarrowtail X$ are disjoint subobjects (i.e. $A\cap B=0$), they have a pullback-stable union (which is then automatically a disjoint and stable coproduct).

This is intended to complete the table of analogies:

|some                       |all                    |
|---------------------------|-----------------------|
|[[regular category]]       |[[exact category]]     |
|[[coherent category]]      |[[pretopos]]           |
|pre-lextensive category    |lextensive category    |

Regular/exact categories have quotients of (some) [[congruences]].  Exact categories have quotients of all congruences, while regular ones have quotients only of congruences that are [[kernel pairs]].  Another way to say that is that in a regular category, you can conclude that the quotient of some congruence exists if you can exhibit another object of which the quotient would be a [[subobject]] if it existed.  Similarly, pre-/lextensive categories have [[disjoint unions]].  Lextensive categories have all disjoint unions (= [[coproducts]]), while in a pre-lextensive category you can conclude that a pair of objects $X,Y$ have a disjoint union if you can exhibit another object in which $X$ and $Y$ can be embedded disjointly.  Finally, coherent categories/pretoposes have both quotients and
disjoint unions, or equivalently quotients and not-necessarily-disjoint unions, with the same sort of relationship between the two.

Evidently a pre-lextensive category is lextensive as soon as any two objects can be embedded disjointly in a third.  Pre-lextensive categories also suffice for the interpretation of [[internal logic|disjunctive logic]].

Being pre-lextensive is also sufficient to define the extensive topology and show that it is subcanonical, since it implies that whatever disjoint coproducts exist must be pullback-stable.  The codomain fibration of a pre-lextensive category is not necessarily a stack for its extensive topology, but this condition is weaker than extensivity.  It is true, however, that if $C$ is a pre-lextensive category whose codomain fibration is a stack for its extensive topology, and in which the disjoint coproduct $1+1$ exists, then $C$ is extensive, for arbitrary disjoint (binary) coproducts can then be obtained by descent along the covering family $(1\to 1+1, 1\to 1+1)$.

## Related concepts

* [[extensive 2-category]]

* [[disjunctive (∞,1)-category]]

* [[intensive or extensive quantity|extensive quantity]]

* [[objective number theory]]

* [[disjunctive logic]]

* [[Gaeta topos]]

## Link

* {#catlistdiscussion}[Freyd, Lack, Lawvere et al: CATLIST discussion on extensive categories 1996](https://www.mta.ca/~cat-dist/catlist/1999/extensive)

## References

* [[Aurelio Carboni]], [[George Janelidze]], _Decidable (= separable) objects and morphisms in lextensive categories_ , JPAA **110** (1996) pp.210-240.

* [[Aurelio Carboni]], [[Stephen Lack]], [[Bob Walters|R. F. C. Walters]], _Introduction to extensive and distributive categories_ , JPAA **84** (1993) pp.145-158.

* [[Stephen Lack]], [[Enrico Vitale|Enrico M. Vitale]], _When do completion processes give rise to extensive categories?_ , JPAA **159** (2001) pp.203-230.


[[!redirects extensive category]]
[[!redirects extensive categories]]

[[!redirects extensive topology]]
[[!redirects extensive topologies]]
[[!redirects extensive coverage]]
[[!redirects extensive coverages]]

[[!redirects lextensive category]]
[[!redirects lextensive categories]]

[[!redirects pre-lextensive category]]
[[!redirects pre-lextensive categories]]
[[!redirects prelextensive category]]
[[!redirects prelextensive categories]]

[[!redirects disjunctive category]]
[[!redirects disjunctive categories]]

[[!redirects infinitary extensive category]]
[[!redirects infinitary extensive categories]]

[[!redirects positive category]]
[[!redirects positive categories]]
[[!redirects positive coherent category]]
[[!redirects positive coherent categories]]
