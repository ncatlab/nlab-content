
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Just as an ordinary [[elementary topos]] comes with its [[internal logic]] formalized by [[type theory]], an [[elementary (∞,1)-topos]] should come with its _internal "$(\infty,1)$-logic"_ formalized by [[homotopy type theory]].


## Type theory versus logic
 {#TypeTheoryVersusLogic}

As remarked at [[type theory]], it is useful to distinguish between the internal type theory of a category and the internal logic which sits on top of that type theory.  The type theory is about constructing objects, while the logic is about constructing [[subobjects]].  For instance, [[limits]] and [[colimits]], [[exponential object|exponentials]], and [[object classifiers]] belong to the type theory, while [[images]], [[dual image|dual images]], [[intersections]], [[unions]], and [[subobject classifiers]] belong to the logic.  Thus, the semantics of (extensional) type theory naturally lies in a category with appropriate structure, while the semantics of logic over that type theory naturally lies in some indexed [[poset]] over that category.  However, we commonly take this indexed poset to consist of the [[subobjects]] in the category in question, in which case additional "logical" structure on the category is required, for instance that it be a [[Heyting category]].

In an elementary 1-topos, all of the "logical" structure is not usually included in the definition, because it comes for free once you have [[power objects]].  But object classifiers may not be as powerful as power objects in this respect, so for purposes of studying the internal logic (and not just the internal type theory) of an $(\infty,1)$-topos, it's good to keep in mind both the type-theoretic structure and the logical structure, and in particular both the object classifier and the subobject classifier.

## The type theory of an $(\infty,1)$-category

Amazingly, a variant of type theory that seems appropriate for interpretation in an $(\infty,1)$-category already exists, namely *intensional type theory* with [[identity type]]s.

### Intensional identity types in $(\infty,1)$-categories

The usual sort of type theory that one interprets in a 1-category is *extensional type theory*.  To explain what this means, consider how the categorical structure of finite limits is represented in the type theory.  On the one hand, we have product types $A\times B$, which of course represent categorical [[products]]; thus to obtain finite limits it suffices to have [[equalizers]].  We can obtain these from *identity types*, which supply for each type $A$ and each pair of terms $x,y:A$, a dependent type $Id_A(x,y)$, whose intended interpretation is that it is inhabited precisely when $x=y$.  In terms of 1-categorical semantics, it is natural to require that any two elements of $Id_A(x,y)$ be equal, i.e. that $Id_A(x,y)$ be essentially a [[truth value]]/[[subsingleton]].  Then if we have two terms $x:A\vdash f(x):B$ and $x:A\vdash g(x):B$ representing morphisms $f,g\colon A\to B$, their equalizer is represented by the type $\Sigma_{x:A} Id_B(f(x),g(x))$.

However, for semantics in an $(\infty,1)$-category, it makes sense to use the same identity types, but now interpreted as a [[path space]].  Now it will no longer be true that $Id_A(x,y)$ is a subsingleton, since two points can be connected by more than one path, so we must drop that axiom.  This *intensional type theory* has been widely studied by type-theorists, although from a different point of view: assuming the [[propositions as types]] approach, $Id_A(x,y)$ should be the type of *proofs* or *reasons* why $x=y$, which can also of course have many different elements.

Thus we suspect that intensional type theory may be a natural sort of type theory to have semantics in an $(\infty,1)$-category.  According to the general framework of syntax/semantics, we would hope that

1. From any intensional type theory, we can construct a syntactic $(\infty,1)$-category, and
1. In any $(\infty,1)$-category, we can model an intensional type theory.

Some work in both of these directions has been done.  On the one hand, it is known that in any intensional type theory with identity types, for any type $A$ the [[globular set]] (or more accurately globular [[context]]) given by

$$ A \leftleftarrows Id_A \leftleftarrows Id_{Id_A} \leftleftarrows \dots $$

has the structure of a [[Batanin ∞-groupoid]].  This can be found in:

* [[Peter Lumsdaine]], *Weak omega-categories from intensional type theory*, [arXiv:0812.0409](http://arxiv.org/abs/0812.0409), and independently
* [[Richard Garner]] and [[Benno van den Berg]], *Types are weak omega-groupoids*, [arXiv:0812.0298](http://arxiv.org/abs/0812.0298)).

Moreover, the syntactic category of such a theory carries a natural [[weak factorization system]], the [[identity type weak factorization system]].  However, there seems as yet to be no published work constructing a full syntactic $(\infty,1)$-category.

On the other hand, it is known that in any nice enough [[model category]] (and in fact, in any category with a nice enough [[weak factorization system]]), one can model intensional type theory.  This is studied in

* [[Steve Awodey]] and [[Michael Warren]], *Homotopy theoretic models of identity types*, [arXiv:0709.0248](http://arxiv.org/abs/0709.0248)
* [[Michael Warren]], *Homotopy theoretic aspects of constructive type theory*, [Ph.D. thesis](http://aix1.uottawa.ca/~mwarren/Papers/phd.pdf).

[[Vladimir Voevodsky]] has also studied the particular model of intensional type theory in simplicial sets, which he calls the *univalent model*; see his [website](http://www.math.ias.edu/~vladimir/Site3/home.html).

### Additional axioms

Although intensional type theory has semantics in $(\infty,1)$-categories, one can naturally expect that these models will all satisfy additional axioms.  This is especially true if we want to add additional structure to our $(\infty,1)$-categories.

* Exponential (and dependent product) types can probably be modeled by (locally) cartesian closed $(\infty,1)$-categories.  However, although exponentials in an $(\infty,1)$-category are not strictly extensional the way they are in a 1-category, they are still extensional "up to coherent higher homotopies," which (unlike the case for identity types) is seemingly not guaranteed by the type-theoretic structure.  Thus, there may be an $\infty$-extensionality axiom to be added.

* Disjoint sum types may be expected to correspond to coproducts in an $(\infty,1)$-category.

* The usual notions of *quotient type* make little sense without extensional identity types.  In the 1-categorical world, quotient types correspond to [[exact categories]], while the appropriate notion of "exactness" for an $(\infty,1)$-category deals with [[groupoid objects in an (∞,1)-category]].  It remains to be seen how to phrase a corresponding axiom in the type theory.

* The [[object classifier]] in an $(\infty,1)$-topos does in fact correspond to a well-known concept in type theory, namely that of a *universe* such as the type $Type$.  However, as a universe, the object classifier in an $(\infty,1)$-topos has the special property that the *paths* between two types $A$ and $B$ as elements of $Type$ (that is, the path space $Id_{Type}(A,B)$) is equivalent to the space of equivalences between $A$ and $B$ as types (an appropriate subspace of the exponential $B^A$).  A type-theoretic axiom asserting this equivalence was introduced by [[Vladimir Voevodsky|Voevodsky]] under the name of the *equivalence axiom*.

## Logic over type theory in an $(\infty,1)$-category

Now when we go to add *logic* to the type theory of an $(\infty,1)$-category, it seems natural by analogy that it will deal with *subobjects*, i.e. with [[monomorphisms in an (∞,1)-category]].  That is, a proposition $\varphi(x)$ with a variable $x:A$ will be interpreted by a monomorphism $[\varphi] \rightarrowtail [A]$.  Just as in the [[internal logic]] of a 1-category and of a [[michaelshulman:2-categorical logic|2-category]], in order to interpret the logical connectives and quantifiers we will then need suitable structure on the posets of subobjects in our $(\infty,1)$-category.  It is naturally to be expected that any $(\infty,1)$-topos will have this necessary structure.

Again, the requisite type theory more or less exists, namely intensional type theory together with a sort of propositions that can depend on types.  In fact, this type theory is very closely related to the [[calculus of constructions]] used in the proof assistant [Coq](http://coq.inria.fr/), making Coq a very convenient place to play around with the type theory that ought to be valid in an $(\infty,1)$-topos.  In particular, Voevodsky has written out a Coq script up to the statement of his equivalence axiom, to be found on his [website](http://www.math.ias.edu/~vladimir/Site3/home.html).

## The problem of finiteness

In describing the internal type theory and logic of an $(\infty,1)$-category we encounter the problem that many structures in an $(\infty,1)$-category require a (countably) infinite amount of data to describe.  For instance, when looking for a way to state the "exactness" property one has to say what is meant by a groupoid object, but since this really means a "coherent" or "$A_\infty$" groupoid object, it involves an infinite amount of data.  By contrast, the most common type theories are purely finitary systems.

There is the one amazing fact that the entire complicated infinitary structure of a Batanin $\omega$-groupoid can be recovered from the simple finitary rules of identity types.  It is not clear, however, whether we can expect this happy occurrence to continue.  We might have to bite the bullet and work with an infinitary type theory, i.e. one allowing derivation rules taking as input an infinite list of hypotheses.  In fact, this is almost certainly what we will need if we want a good notion of a [[geometric theory]] in the $(\infty,1)$-case, since that involves infinitary logic even in the 1-categorical case.

However, such a type theory would obviously no longer have "computational content" and couldn't be modeled in a proof assistant such as Coq, and also wouldn't provide a fully "elementary," i.e. finitary first-order, theory such as [[ETCS]] provides in the 1-categorical case.  It might be helpful to note that infinitary structures can at least sometimes be finitarily described using [[inductive type]]s and/or [[coinductive type]]s, but it is not clear yet whether this is useful in the $(\infty,1)$-categorical context.


## Examples

### Internal logic in $\infty Grpd$ {#OfInfGrpd}

The archetypical [[(∞,1)-topos]] is [[∞Grpd]]. This is to be thought of as the [[vertical categorification|(∞,1)-categorification]] of the archetypical 1-[[topos]] [[Set]].

At [internal logic - in Set](http://ncatlab.org/nlab/show/internal+logic#LogicOfSet) is a step-by-step discussion of how ordinary logic is recovered from the point of view of the [[internal logic]] of a topos $\mathcal{T}$ when  choosing $\mathcal{T} := Set$.

Here we look at the $(\infty,1)$-categorical analog of that discussion,  step-by-step, now everything internal to [[∞Grpd]].


* The [[terminal object]] of $\infty Grpd$ is [[generalized the|the]] [[contractible]] $\infty$-groupoid $*$.

  This _generates_ $\infty Grpd$ under [[colimit]]s: every small $\infty$-groupoid is a colimit over a small diagram consisting only of copies of the terminal $\infty$-groupoid.

* The _subobject classifier_ of $\infty Grpd$ is 

  $\Omega = \{\top, \bottom\}$

  The _object_ classifier should be the [[core]] of the
  [[universal fibration of (infinity,1)-categories|universal left fibration]].

  See [[(sub)object classifier in an (∞,1)-topos]].

Now...

...

## Related concepts

* [[internal logic]], [[type theory]]

* **internal logic in an $(\infty,1)$-topos**, [[homotopy type theory]]

## References

* [[Chris Kapulkin]], _Internal Languages of Higher Categories_, [blog post](https://golem.ph.utexas.edu/category/2015/07/internal_languages_of_higher_c.html)

* [[Chris Kapulkin]], _Internal Languages of Higher Categories II_, [blog post](https://golem.ph.utexas.edu/category/2017/11/internal_languages_of_higher_c_1.html)
[[!redirects internal logic of an (∞,1)-topos]]
