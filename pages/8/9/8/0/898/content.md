
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Filtered categories
* table of contents
{: toc}


## Idea

A filtered category is a [[categorification]] of the concept of [[directed set]].  In addition to having an upper bound (but not necessarily a [[coproduct]]) for every pair of objects, there must also be an upper bound (but not necessarily a [[coequaliser]]) for every pair of parallel morphisms.

A [[diagram]] $F:D\to C$ where $D$ is a filtered category is called a **filtered diagram**.  A colimit of a filtered diagram is called a **[[filtered colimit]]**.

A category whose opposite is filtered is called **cofiltered**.


## Definitions

### Ordinary filteredness

+-- {: .num_defn}
###### Definition

A **(finitely) filtered category**  is a [[category]] $C$ in which every finite [[diagram]] has a [[cocone]].  

=--

That is, for any finite category $D$ and any [[functor]] $F:D\to C$, there exists an object $c\in C$ and a [[natural transformation]] $F\to \Delta c$ where $\Delta c:D\to C$ is the constant diagram at $c$. If $D^+$ is the result of freely adjoining a terminal object to a category $D$, then the condition is the same as that any functor $F: D \to C$ with finite domain admits an extension $\tilde{F}: D^+ \to C$. 

Equivalently, filtered categories can be characterized as those categories where, for every finite diagram $J$, the diagonal functor $\Delta : C \to C^J$ is [[final functor|final]]. This point of view can be generalized to other kinds of categories whose colimits are well-behaved with respect to a type of limit, such as [[sifted colimit|sifted]] categories.

This can be rephrased in more elementary terms by saying that:

* There exists an object of $C$  (the case when $D=\emptyset$)
* For any two objects $c_1,c_2\in C$, there exists an object $c_3\in C$ and morphisms $c_1\to c_3$ and $c_2\to c_3$.
* For any two [[parallel morphisms]] $f,g:c_1\to c_2$ in $C$, there exists a morphism $h:c_2\to c_3$ such that $h f = h g$.

Just as all finite [[colimit|colimits]] can be constructed from initial objects, binary coproducts, and coequalizers, so a cocone on any finite diagram can be constructed from these three.

In [[constructive mathematics]], the elementary rephrasing above is equivalent to every [[Bishop-finite]] diagram admitting a cocone.

### Higher filteredness

More generally, if $\kappa$ is an infinite [[regular cardinal]] (or an [[arity class]]), then a **$\kappa$-filtered category** is one such that any diagram $D\to C$ has a cocone where $D$ has $\lt \kappa$ arrows, or equivalently that any functor $F: D \to C$ whose domain has fewer than $\kappa$ morphisms admits an extension $\tilde{F}: D^+ \to C$. The usual filtered categories are then the case $\kappa = \omega$, i.e., where the $D$ have fewer than $\omega$ morphisms (in other words are finite).  (We could also say in this case "$\aleph_0$-filtered", but $\omega$-filtered is more usual in the literature.) 

Note that a [[preorder]] is $\kappa$-filtered as a category just when it is $\kappa$-[[direction|directed]] as a preorder. 

### Generalized filteredness

Even more generally, if $\mathcal{J}$ is a class of small categories, a category $C$ is called **$\mathcal{J}$-filtered** if $C$-colimits commute with $\mathcal{J}$-limits in [[Set]].  When $\mathcal{J}$ is the class of all $\kappa$-small categories for an infinite regular cardinal $\kappa$, then $\mathcal{J}$-filteredness is the same as $\kappa$-filteredness as defined above.  See [ABLR](#ABLR).

If $\mathcal{J}$ is the class consisting of the [[terminal category]] and the [[empty category]] --- which is to say, the class of $\kappa$-small categories when $\kappa$ is the finite regular cardinal $2$ --- then being $\mathcal{J}$-filtered in this sense is equivalent to being [[connected category|connected]].  Note that this is not what the explicit definition given above for infinite regular cardinals would specialize to by simply setting $\kappa=2$ (that would be simply [[inhabited set|inhabitation]]).

## Examples

* A filtered [[preorder]] is the same as a [[direction|directed]] one: a **filtered [[(0,1)-category]]**.

* Every category with a [[terminal object]] is filtered.

* Every category which has finite [[colimit]]s is filtered.

* A [[product]] of filtered categories is filtered.


## Related concepts

* [[sifted category]], [[sifted (∞,1)-category]]

* [[directed set]], **filtered category**, [[filtered (∞,1)-category]]

* [[direct category]]

* [[filtered colimit]]

## References

* {#ABLR} [[Ji?í Adámek]], [[Francis Borceux]], [[Stephen Lack]], and [[Ji?í Rosický]], _A classification of accessible categories_, Journal of Pure and Applied Algebra 175:7-30, 2002, ([web page with PS fulltext](http://maths.mq.edu.au/~slack/papers/acc.html)).



[[!redirects filtered categories]]
[[!redirects cofiltered category]]
[[!redirects cofiltered categories]]
[[!redirects filtrant category]]
[[!redirects filtrant categories]]
[[!redirects filtered diagram]]