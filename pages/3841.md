
# Contents
* automatic table of contents goes here
{: toc}

## Idea

A regular cardinal is is a [[cardinal number]] that is 'closed under union'.  The [[category]] of [[sets]] bounded by a regular cardinal has several nice properties, making it a [[universe]] that is handy for some purposes but falls short of being a [[Grothendieck universe]].  Unlike Grothendieck universes (which are based on [[inaccessible cardinals]] rather than regular cardinals), it is easy to prove that (even [[uncountable set|uncountable]]) regular cardinals exist.


## Definitions

An [[infinite set|infinite]] [[cardinal]] $\kappa$ is a **regular cardinal** if it satisfies the following equivalent properties:

* no set (in a [[material set theory]]) of cardinality $\kappa$ is the [[union]] of fewer than $\kappa$ sets of cardinality less than $\kappa$.  

* no set (in a [[structural set theory]]) of cardinality $\kappa$ is the [[disjoint union]] of fewer than $\kappa$ sets of cardinality less than $\kappa$.  

* given a function $P \to X$ (regarded as a [[family of sets]] $\{P_x\}_{x\in X}$) such that ${|X|} \lt \kappa$ and ${|P_x|} \lt \kappa$ for all $x \in X$, then ${|P|} \lt \kappa$.  

* the [[category]] $\Set_{\lt\kappa}$ of sets of cardinality $\lt\kappa$ has all [[colimits]] (or just all [[coproducts]]) of size $\lt\kappa$. 

* the [[cofinality]] of $\kappa$ is equal to $\kappa$. 

A cardinal that is not regular is called **singular**.


### Finite regular cardinals?
{#finite}

Traditionally, one requires regular cardinals to be infinite.  This clause may be removed, in which case $0$, $1$, and $2$ are all regular cardinals.

Other modifications of the definition which are equivalent for infinite cardinals may include some of $0$, $1$, and $2$ but not all.  For instance, if we regard an indexed [[disjoint union]] $\sum_{i\in\lambda} \alpha_i$ as a binary operation taking as input $\lambda$ and a $\lambda$-indexed family $\alpha$, then closure under this binary operation as in the above definition also entails closure under the ternary version $\sum_{i\in\lambda} \sum_{j\in \mu_i} \alpha_{i,j}$, and so on.  The unary version is simply the identity operation, whereas the nullary version will always output the [[singleton set]] $1$.  (This can be seen by thinking in terms of trees of uniform finite height, or remembering that a [[dependent sum]] includes a binary [[cartesian product]] as a special case, so a nullary dependent sum should at least include a nullary product.)  Thus, from this perspective, $2$ is a regular cardinal, but $0$ and $1$ are not.  In applications for which this perspective is the relevant one, such as [[familial regularity and exactness]], one may more precisely be interested in an [[arity class]] rather than a regular cardinal.

We may rule out all three finite regular cardinals by additionally generalising from indexed disjoint unions to finitary disjoint unions.

Then in terms of $Set_{\lt\kappa}$, the (potential) conditions on a (possibly finite) regular cardinal are as follows:

1.  $Set_{\lt\kappa}$ is closed under iterated disjoint unions ($\biguplus_i A_i$).
2.  $Set_{\lt\kappa}$ is closed under the nullary iterated disjoint union (the [[singleton]]).
3.  $Set_{\lt\kappa}$ is closed under binary disjoint unions ($A \uplus B$).
4.  $Set_{\lt\kappa}$ is closed under the nullary disjoint union (the [[empty set]]).

These are all variations on the theme of closure under disjoint unions.

Clauses (2--4) hold of all infinite cardinals, while clauses (2&3) together force $\kappa$ to be greater than any finite cardinal.  However, if we require only clauses (1&2), then $2$ is a regular cardinal.


### In weak foundations

Thinking of a regular cardinal *as* a cardinal number makes the most sense using the [[axiom of choice]].  Otherwise, we probably want to think of it as a *collection* of cardinals, or equivalently think of it as the category $Set_{\lt\kappa}$.

From this perspective, a regular cardinal is a [[full subcategory]] of $Set$ that is closed under taking [[quotient objects]] and satisfies the condition on $Set_{\lt\kappa}$ above.  We can then recover $\kappa$ as the smallest cardinal number greater than every cardinal in $Set_{\lt\kappa}$, if we accept the axiom of choice.

Note that if we require only conditions (1&2) on $Set_{\lt\kappa}$, then (even classically), $\{1\}$ is an acceptable (and finite) regular collection of cardinals, even though it is not actually of the form $Set_{\lt\kappa}$ for any cardinal number $\kappa$.

In the absence of the axiom of choice, it is not clear that there exist arbitrarily large regular cardinals.  Thus in weaker foundations, regular cardinals (or "regular sets of cardinals") can be regarded as a [[large cardinal]] property.

At least if "regular cardinal" has its classical meaning of a particular ordinal, then the statement that *there exist arbitrarily large regular cardinals* is independent of [[ZF]]; in fact it is consistent with ZF that all uncountable cardinals are singular.  A foundational axiom which is related to the existence of regular cardinals (but considers them as sets with various closure properties, rather than cardinal numbers) is the [[regular extension axiom]].


## Examples

### Regular cardinals

* The first (infinite) regular cardinal is $\aleph_0 = {|\mathbb{N}|}$, because a set with cardinality less than $\aleph_0$ is a [[finite set]], and a finite union of finite sets is still a finite set.

\begin{theorem} Assuming the [[axiom of choice]], the [[successor]] of any infinite cardinal, such as $\aleph_0$, is a regular cardinal. 
\end{theorem} 

In the case of $\aleph_0$, this means that a countable union of countable sets is countable.  Note that this implies that there exist arbitarily large regular cardinals: for any cardinal $\lambda$ there is a greater regular cardinal, namely $\lambda^+$. 

\begin{proof} 
Under the axiom of choice, the successor of a cardinal number is the [[Hartogs number]] (see there): if $\lambda$ is the cardinality of $X$, then $\lambda^+$ is the order type of the well-ordered set $\aleph(X)$. If $(\lambda_\alpha) = (0 = \lambda_0 \lt \lambda_1 \lt \ldots)$ is a set of ordinals with least upper bound $\lambda^+$, and supposing, working toward a contradiction, that this set has cardinality $\leq \lambda$, then the corresponding initial segments $X_\alpha$ of $\aleph(X)$ provide a partition 
$$\aleph(X) = \bigcup_\alpha X_{\alpha+1} \setminus X_\alpha$$ 
and by construction of $\aleph(X)$, each $X_{\alpha+1} \setminus X_\alpha$ has cardinality $\leq \lambda$. Thus the union would have at most $\lambda \cdot \lambda = \lambda$ elements, which is less than the cardinality $\lambda^+$ of $\aleph(X)$, contradiction. 
\end{proof} 


### Singular cardinals

* $\aleph_\omega = \bigcup_{n\in \mathbb{N}} \aleph_n$ is singular, more or less by definition, since $\aleph_n\lt\aleph_\omega$ and ${|\mathbb{N}|} = \aleph_0 \lt\aleph_\omega$.

* More generally, any limit cardinal that can be "written down by hand" should be singular, since if it were regular then it would be [[weakly inaccessible cardinal|weakly inaccessible]], and the existence of weakly inaccessible cardinals cannot be proven in [[ZFC]] (if $ZFC$ is consistent).  We say 'should' rather than 'must', since there are exceptions, but they are sort of cheating: one (definable with Choice) is 'the smallest limit cardinal that is regular if and only if some weakly innaccessible cardinal exists'.

* Assuming the consistency (with [[ZFC]]) of 'there is a [[proper class]] of [[strongly compact cardinal|strongly compact cardinals]]', it is consistent with $ZF$ that every uncountable cardinal is singular (and in fact every infinite well-orderable cardinal has [[cofinality]] $\aleph_0$), a result due to [[Moti Gitik]].  (Of course this conclusion is inconsistent with $ZFC$, in which many uncountable cardinals, starting with $\aleph_1$, are regular.)


[[!redirects regular cardinal]]
[[!redirects regular cardinals]]
[[!redirects regular cardinal number]]
[[!redirects regular cardinal numbers]]
[[!redirects regular collection of cardinal numbers]]
[[!redirects regular collections of cardinal numbers]]
[[!redirects regular set of cardinal numbers]]
[[!redirects regular sets of cardinal numbers]]
[[!redirects regular class of cardinal numbers]]
[[!redirects regular classes of cardinal numbers]]

[[!redirects singular cardinal]]
[[!redirects singular cardinals]]
[[!redirects singular cardinal number]]
[[!redirects singular cardinal numbers]]
[[!redirects singular collection of cardinal numbers]]
[[!redirects singular collections of cardinal numbers]]
[[!redirects singular set of cardinal numbers]]
[[!redirects singular sets of cardinal numbers]]
[[!redirects singular class of cardinal numbers]]
[[!redirects singular classes of cardinal numbers]]
