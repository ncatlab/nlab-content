
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

__Predicate logic__, also called __first-order logic__ and sometimes abbreviated __FOL__, is the usual sort of [[logic]] used in the [[foundations of mathematics]].  

In contrast to [[0th-order logic]], first-order logic admits [[variables]] in [[predicates]] [[bound variable|bound]] by _[[quantification|quantifiers]]_ ("[[universal quantifier|for all]]" $\forall$ and "[[existential quantifier|there exists]] $\exists$). 

(This means that the [[categorical semantics]] of 1st order logic is given by _[[hyperdoctrines]]_.)

However, in contrast to [[higher-order logic]], first-order logic does not allow variables that stand for predicates themselves.  (This distinction can become somewhat confusing when the first-order theory in question is a [[material set theory]], such as [[ZFC]], in which the variables stand for "sets" which behave very much like predicates.)

A __predicate calculus__ is simply a system for describing and working with predicate logic.  The precise form of such a calculus (and hence of the logic itself) depends on whether one is using [[classical logic]], [[intuitionistic logic]], [[linear logic]], etc; see those articles for details.

[[type theory|Typed]] predicate logic may be called [[type theory#Logic over type theory|first-order logic over type theory]]. Typed predicate [[intuitionistic logic]] is often identified with the [[internal logic]] of a [[Heyting category]], while typed predicate [[classical logic]] is often identified with the [[internal logic]] of a [[Boolean category]]. Any untyped predicate logic could be thought of as a [[simple type theory|simply typed]] predicate logic with only one type $V$, known as the __[[domain of discourse]]__ or the __universe of discourse__. 

For many (perhaps most?) authors, predicate logic is really __predicate logic with [[propositional equality|equality]]__. That means that one predicate symbol with two arguments $=(x,y)$ (also  written $x=y$) is distinguished, and has to satisfy reflexivity, symmetry, transitivity and the rule of substitution: $(x = y \wedge \phi(x))\implies \phi(y)$ for any predicate $\phi$ with one argument. However, some forms of predicate logic do not include an equality primitive, such as [[FOLDS]] (in whose name 'FOL' stands for 'first-order logic').  In some first-order theories, such as [[ZFC]], equality can be defined and so is not needed in the logic itself.

In constructive mathematics, one could also have a __predicate logic with [[apartness]]__, which has one predicate symbol with two arguments $\#(x,y)$ (also  written $x\#y$) is distinguished, and has to satisfy irreflexivity, symmetry, and comparison. By definition of an [[apartness relation]], its negation is an [[equivalence relation]], which we could take to be [[propositional equality]] $x = y \coloneqq \neg(x \# y)$ satisfying the rule of substitution: $(\neg(x \# y) \wedge \phi(x))\implies \phi(y)$ for any predicate $\phi$ with one argument. This makes the domain of discourse into an [[apartness space]]. 

## Properties

[[Lindström's theorems]] give important abstract characterizations of classical untyped first-order logic.


## Related concepts

* [[logic]]

  * [[propositional logic]] (0th order)

  * **predicate logic** (1st order)

  * [[second-order logic]]

  * [[higher-order logic]]

  * [[predicate logic as a dependent type theory]]
 
  * [[rule C]]

* [[first-order set theory]]

* [[type theory]]

* [[Lindström's theorem]]


## References

### General

Textbook accounts:

In view of the [[Curry-Howard correspondence]]:

* Morten Heine Sørensen, Pawel Urzyczyn, §9 of: *Lectures on the Curry-Howard isomorphism*, Studies in Logic **149**, Elsevier (2006) &lbrack;[ISBN:9780444520777](https://www.elsevier.com/books/lectures-on-the-curry-howard-isomorphism/sorensen/978-0-444-52077-7), [pdf](https://disi.unitn.it/~bernardi/RSISE11/Papers/curry-howard.pdf)&rbrack;

The [[syntax - semantics duality]] in first order logic is discussed in 

* [[Steve Awodey]], [[Henrik Forssell]], _First-Order Logical Duality_ .([arXiv:1008.3145](http://arxiv.org/abs/1008.3145))

On the historical development:

* Jos&#233; Ferreir&#243;s, _The Road to Modern Logic - An Interpretation_ , The Bulletin of Symbolic Logic **7** no. 4 (2001) pp.441-484. ([draft](https://idus.us.es/server/api/core/bitstreams/819edc9f-3254-4445-bc4f-6f7635521009/content))

### From type theory
 {#ReferencesFromTypeTheory}

First order logic within [[type theory]]/[[homotopy type theory]] via _[[propositions as types]]_ is discussed in

* [[Univalent Foundations Project]], section 3 of  _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_


[[!redirects Predicate logic]]
[[!redirects predicate logic]]
[[!redirects predicate calculus]]
[[!redirects 1st-order logic]]
[[!redirects 1st order logic]]
[[!redirects first-order logic]]
[[!redirects first order logic]]

[[!redirects first-order language]]
[[!redirects first order language]]
[[!redirects first-order languages]]
[[!redirects first order languages]]

[[!redirects FOL]]

[[!redirects Predicate logic with equality]]
[[!redirects predicate logic with equality]]
[[!redirects 1st-order logic with equality]]
[[!redirects 1st order logic with equality]]
[[!redirects first-order logic with equality]]
[[!redirects first order logic with equality]]

[[!redirects Predicate logic with apartness]]
[[!redirects predicate logic with apartness]]
[[!redirects 1st-order logic with apartness]]
[[!redirects 1st order logic with apartness]]
[[!redirects first-order logic with apartness]]
[[!redirects first order logic with apartness]]
