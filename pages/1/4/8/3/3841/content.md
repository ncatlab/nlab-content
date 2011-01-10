
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

Traditionally, one requires regular cardinals to be infinite.  This clause may be removed, in which case $0$, $1$, and $2$ are all regular cardinals.

Other modifications of the definition which are equivalent for infinite cardinals may include some of $0$, $1$, and $2$ but not all.  For instance, if we regard an indexed [[disjoint union]] $\sum_{i\in\lambda} \alpha_i$ as a binary operation taking as input $\lambda$ and a $\lambda$-indexed family $\alpha$, then closure under this binary operation as in the above definition also entails closure under the ternary version $\sum_{i\in\lambda} \sum_{j\in \mu_i} \alpha_{i,j}$, and so on.  The unary version is simply the identity operation, whereas the nullary version will always output the [[singleton set]] $1$.  (This can be seen by thinking in terms of trees of uniform finite height, or remembering that a [[dependent sum]] includes a binary [[product]] as a special case, so a nullary dependent sum should at least include a nullary product.)  Thus, from this perspective (which is the relevant one for some applications, such as [[familial regularity and exactness]]), $2$ is a regular cardinal, but $0$ and $1$ are not.

We may rule out all three finite regular cardinals by additionally generalising from indexed disjoint unions to binary and nullary disjoint unions.

Then in terms of $Set_{\lt\kappa}$, the (potential) conditions on a (possibly finite) regular cardinal are as follows:

1.  $Set_{\lt\kappa}$ is closed under coproducts of size $\lt\kappa$.
2.  $Set_{\lt\kappa}$ is closed under binary coproducts.
3.  $Set_{\lt\kappa}$ is closed under nullary coproducts (taking the [[initial object]]).
4.  $Set_{\lt\kappa}$ has a nullary [[copower]] (or something like that).

These are all variations on the theme of closure under coproducts.

Clauses (2--4) hold of all infinite cardinals, while clauses (2&4) together force $\kappa$ to be greater than any finite cardinal.  However, if we require only clauses (1&4), then $2$ is a regular cardinal.


### In weak foundations

Thinking of a regular cardinal *as* a cardinal number makes the most sense using the [[axiom of choice]].  Otherwise, we probably want to think of it as a *collection* of cardinals, or equivalently think of it as the category $Set_{\lt\kappa}$.

From this perspective, a regular cardinal is a [[full subcategory]] of $Set$ that is closed under taking [[quotient objects]] and satisfies the condition on $Set_{\lt\kappa}$ above.  We can then recover $\kappa$ as the largest cardinal number greater than every cardinal in $Set_{\lt\kappa}$, if we accept the axiom of choice.

Note that if we require only conditions (1&4) on $Set_{\lt\kappa}$, then (even classically), $\{1\}$ is an acceptable (and finite) regular collection of cardinals, even though it is not actually of the form $Set_{\lt\kappa}$ for any cardinal number $\kappa$.

In the absence of the axiom of choice, it is not clear that there exist arbitrarily large regular cardinals.  Thus in weaker foundations, regular cardinals (or "regular sets of cardinals") can be regarded as a [[large cardinal]] property.  The statement that *there exist arbitrarily large regular cardinals* is sometimes called the *Regular Extension Axiom*.


## Examples

### Regular cardinals

* The first (infinite) regular cardinal is $\aleph_0 = {|\mathbb{N}|}$, because a set with cardinality less than $\aleph_0$ is a [[finite set]], and a finite union of finite sets is still a finite set.

* The [[successor]] of any infinite cardinal, such as $\aleph_1$, is a regular cardinal.  (This requires the [[axiom of choice]].)  In the case of $\aleph_1$, this means that a countable union of countable sets is countable.  Note that this implies that there exist arbitarily large regular cardinals: for any cardinal $\lambda$ there is a greater regular cardinal, namely $\lambda^+$.


### Singular cardinals

* $\aleph_\omega = \bigcup_{n\in \mathbb{N}} \aleph_n$ is singular, more or less by definition, since $\aleph_n\lt\aleph_\omega$ and ${|\mathbb{N}|} = \aleph_0 \lt\aleph_\omega$.

* More generally, any limit cardinal that can be "written down by hand" must be singular, since if it were regular then it would be [[weakly inaccessible cardinal|weakly inaccessible]], and the existence of weakly inaccessible cardinals cannot be proven in [[ZFC]] (if ZFC is consistent).


[[!redirects regular cardinal]]
[[!redirects regular cardinals]]
[[!redirects singular cardinal]]
[[!redirects singular cardinals]]
[[!redirects regular extension axiom]]
[[!redirects Regular Extension Axiom]]
[[!redirects REA]]
