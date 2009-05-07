## Idea ##

Given an extensional relation $\prec$ on a set, two elements are equal if they cannot be distinguished by the structure of the set of elements that they are related to, that those elements are related to, and so on forever in one direction.  We generally think of $x \prec y$ as saying that $x$ is an 'element' of $y$, so that $\prec$ is extensional when "$x$ is determined by its elements" as in the [[axiom of extensionality]] for material [[set theory]].

## Definitions ##

We begin with the historically first definition, which is correct for [[well-founded relation]]s.  We then consider ways to extend this to more general relations, where the last version seems to be 'correct'.

### Weak extensionality ###

A relation $\prec$ on a set $S$ is __weakly extensional__ if, given any elements $x$ and $y$ of $S$, $x = y$ whenever (for all $t$) $t \prec x$ if and only if $t \prec y$.

Interpreting $\prec$ as membership $\in$, this corresponds to the [[axiom of extensionality]] as usually stated for [[pure set]]s. However, it is really only appropriate when $\prec$ is [[well-founded relation|well-founded]], just as the usual axiom of extensionality must be strengthened in the absence of the [[axiom of foundation]]. For example, consider the set $\{a,b\}$ where $a\prec b$ and $b\prec a$; then $a$ and $b$ cannot really be distinguished by their $\prec$-elements, but this set does satisfy the above criterion.

However, when $\prec$ is well-founded, weak extensionality is equivalent to all the stronger notions below; thus in that case it is usually called just **extensionality**.


### Finsler extensionality ###

Let $\prec^*$ be the [[transitive closure]] of the relation $\prec$ on $S$ (so $\prec^*$ is a [[preorder]]).  Given an element $y$ of $S$, let $S_y$ be the [[downset]] of $y$ under $\prec^*$:
$$ S_y = \{ x: S \;|\; x = t_0 \prec \cdots \prec t_n = y\} $$
with $n \gt 0$.
Then $\prec$ is __Finsler-extensional__ if, given any elements $x$ and $y$ of $S$, $x = y$ whenever $S_x$ and $S_y$ are isomorphic as sets equipped with a relation $\prec$.

It is important that $\prec^*$ be merely the transitive closure of $\prec$ rather than the reflexive-[[transitive closure]] (so that $n = 0$ is allowed in the definition of $S_y$), even though that is a [[preorder]].  As pointed out by Aczel in Chapter 4 of [Non-Well-Founded Sets](http://standish.stanford.edu/pdf/00000056.pdf), such a definition would not even imply weak extensionality.  Consider the set $S=\{a,b\}$ where $b\prec a$ and $b\prec b$.  Then $S_a$ would be $S$ while $S_b$ would be $\{b\}$, which are not isomorphic so this criterion would not require $a=b$; however it is true that $t\prec a$ if and only if $t\prec b$, so weak extensionality _would_ require $a=b$.  Using the definition above, however, we have $S_a = \{b\}$ and $S_b = \{b\}$, so $a = b$ is again required.

It is easy to show that Finsler extensionality implies weak extensionality, and (using [[induction]]) that the converse is true for well-founded relations.


### Strong extensionality ###

Finsler-extensionality is often also not strong enough, however.  Consider the set $\{a,b_0,b_1,b_2,\dots\}$ where $a\prec a$ and $b_{n+1}\prec b_n$ for all $n$.  Then both $a$ and $b_0$ (and, in fact, every $b_n$) are characterized by a single infinite descending chain of $\prec$-elements, namely $\dots \prec a \prec a \prec a$ and $\dots \prec b_2\prec b_1\prec b_0$.  But $a\neq b_0$ and yet this set is Finsler-extensional.

+-- {: .query}
If this set is Finsler-extensional, then $b_0 = b_1 = \cdots$, so $S_a \cong S_{b_0}$ after all.  So this set is Finsler-extensional if and only if it is strongly extensional (in which case it is a point).  ---Toby

[[Mike Shulman|Mike]]: You're right.  I think that actually the notion here is not quite the same as what Aczel calls 'Finsler-extensional.' he uses isomorphisms of $S_y\cup \{y\}$ rather than $S_y$, and his counterexample is $\{a,b\}$ with $a\prec a$ and $a\prec b$.  So maybe we should call it something else.  But probably we can come up with a counterexample to this version too.
=--

To remedy this, we give the following definition.  Let $S$ be equipped with a binary relation $\prec$.  A **bisimulation** on $S$ is a binary relation $\sim$ such that whenever $x\sim y$, for any $a\prec x$ there is a $b\prec y$ with $a\sim b$, and for every $b\prec y$ there is an $a\prec x$ with $a\sim b$.  We then say that $\prec$ is **strongly extensional** if every bisimulation is contained in the identity relation; i.e. if $\sim$ is a bisimulation then $x\sim y$ implies $x=y$.  Again, it is easy to show that strong extensionality implies Finsler-extensionality, hence also weak extensionality, and is equivalent to weak extensionality for well-founded relations.

## Extensional quotients ##

Weak extensionality is a kind of [[antisymmetric relation|antisymmetry]] condition: Let $x \leq y$ mean that $t \prec y$ whenever $t \prec x$.  Then $\leq$ is clearly a [[preorder]], which is antisymmetric (so a [[partial order]]) if and only if $\prec$ is weakly extensional.

Now suppose that if $t \prec x$ if and only if $t \prec y$ for all $t$, then $x \prec z$ if and only if $y \prec z$ for all $z$.  Then if we define $x\sim y$ to mean $x\leq y$ and $y\leq x$, $\sim$ is an equivalence relation such that $\prec$ descends to a weakly extensional relation on the [[quotient set]] $S/{\sim}$.

Strongly extensional quotients are even easier to construct.  It is easy to see that the union of any family of bisimulations is a bisimulation, and therefore there is a largest bisimulation $\approx$ for any binary relation $\prec$ on $S$.  Moreover, $\approx$ is an equivalence relation (though not every bisimulation need be so), and $\prec$ descends to a (strongly) extensional relation on the quotient $S/\approx$.


## Simulations ##

Given two sets $S$ and $T$, each equipped with an extensional relation $\prec$, a [[function]] $f: S \to T$ is a __simulation__ of $S$ in $T$ if
*  $f(x) \prec f(y)$ whenever $x \prec y$ and
*  given $t \prec f(x)$, there exists $y \prec x$ with $t = f(y)$.

Then sets so equipped form a [[category]] with simulations as [[morphism]]s.

Note that there is at most one simulation from $S$ to $T$; in fact, strong extensionality for $T$ is equivalent to saying that any two simulations $S \rightrightarrows T$ are equal.  Also, any simulation from $S$ to $T$ must be an [[injection]]; in fact, strong extensionality for $S$ is equivalent to saying that any simulation $S \to T$ is injective.

Thus, we have a (large) [[poset]] of sets equipped with extensional relations, and we can consistently interpret the simulations as [[subset]] inclusion.  This leads to the model of sets equipped with extensional relations as [[transitive set]]s.


## Applications ##

Well-founded relations are often used to represent [[axiom of foundation|well-founded]] [[pure set]]s.  In this case, where $\prec$ represents the 'membership' relation $\in$, a restriction to (weakly) extensional such relations corresponds to imposing the [[axiom of extensionality]] (that two sets are equal if they have the same elements).  For non-well-founded sets, one usually wants to impose one of the stronger versions of extensionality.

A well-founded relation that is both extensional and [[transitive relation|transitive]] is precisely a [[well-order]].

## References ##

*  Peter Aczel; [Non-Well-Founded Sets](http://standish.stanford.edu/pdf/00000056.pdf).