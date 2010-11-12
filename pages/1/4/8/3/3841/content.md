# Contents
* automatic table of contents goes here
{:toc}

## Idea

A regular cardinal is is a [[cardinal number]] that is 'closed under union'.  The [[category]] of [[sets]] bounded by a regular cardinal has several nice properties, making it a [[universe]] that is handy for some purposes but falls short of being a [[Grothendieck universe]].  Unlike Grothendieck universes (which are based on [[inaccessible cardinals]] rather than regular cardinals), it is easy to prove that (even [[uncountable set|uncountable]]) regular cardinals exist.


## Definitions

An [[infinite set|infinite]] [[cardinal]] $\kappa$ is a **regular cardinal** if it satisfies the following equivalent definitions:

* no set (in a [[material set theory]]) of cardinality $\kappa$ is the [[union]] of fewer than $\kappa$ sets of cardinality less than $\kappa$.  

* no set (in a [[structural set theory]]) of cardinality $\kappa$ is the [[disjoint union]] of fewer than $\kappa$ sets of cardinality less than $\kappa$.  

* given a function $P \to X$ (regarded as a [[family of sets]] $\{P_x\}_{x\in X}$) such that ${|X|} \lt \kappa$ and ${|P_x|} \lt \kappa$ for all $x \in X$, then ${|P|} \lt \kappa$.  

* the [[category]] $\Set_{\lt\kappa}$ of sets of cardinality $\lt\kappa$ has all [[colimits]] (or just all [[coproducts]]) of size $\lt\kappa$.  

A cardinal that is not regular is called **singular**.


### Finite regular cardinals?

Traditionally, one requires regular cardinals to be infinite.  This clause may be removed, in which case $0$, $1$, and $2$ are all regular cardinals.  (See the examples below.)  However, we may rule out these examples by listing the definition (in terms of $Set_{\lt\kappa}$) as follows:

1.  $Set_{\lt\kappa}$ is closed under coproducts of size $\lt\kappa$.
2.  $Set_{\lt\kappa}$ is closed under binary coproducts.
3.  $Set_{\lt\kappa}$ is closed under nullary coproducts (taking the [[initial object]]).
4.  $Set_{\lt\kappa}$ has a nullary [[copower]].

These are all variations on the theme of closure under coproducts.

Clauses (2--4) hold of all infinite cardinals, while clauses (2&4) together force $\kappa$ to be greater than any finite cardinal.


### In weak foundations

Thinking of a regular cardinal *as* a cardinal number makes the most sense using the [[axiom of choice]].  Otherwise, we probably want to think of it as a *collection* of cardinals, or equivalently think of it as the category $Set_{\lt\kappa}$.

From this perspective, a regular cardinal is a [[full subcategory]] of $Set$ that is closed under taking [[quotient objects]] and satisfies the condition on $Set_{\lt\kappa}$ above.  We can then recover $\kappa$ as the largest cardinal number greater than every cardinal in $Set_{\lt\kappa}$, if we accept the axiom of choice.


## Examples

### Regular cardinals

* The first (infinite) regular cardinal is $\aleph_0 = {|\mathbb{N}|}$, because a set with cardinality less than $\aleph_0$ is a [[finite set]], and a finite union of finite sets is still a finite set.

* The [[successor]] of any infinite cardinal, such as $\aleph_1$, is a regular cardinal.  (This requires the [[axiom of choice]].)  In the case of $\aleph_1$, this means that a countable union of countable sets is countable.  Note that this implies that there exist arbitarily large regular cardinals: for any cardinal $\lambda$ there is a greater regular cardinal, namely $\lambda^+$.


### Singular cardinals

* $\aleph_\omega = \bigcup_{n\in \mathbb{N}} \aleph_n$ is singular, more or less by definition, since $\aleph_n\lt\aleph_\omega$ and ${|\mathbb{N}|} = \aleph_0 \lt\aleph_\omega$.


[[!redirects regular cardinal]]
[[!redirects regular cardinals]]
[[!redirects singular cardinal]]
[[!redirects singular cardinals]]
