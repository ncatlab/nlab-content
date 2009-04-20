# Idea #

Given an extensional relation $\prec$ on a set, two elements are equal if they cannot be distinguished by the structure of the set of elements that they are related to, that those elements are related to, and so on forever in one direction.  We generally think of the statement $x\prec y$ as saying that $x$ is an 'element' of $y$, so that $\prec$ is extensional when "$x$ is determined by its elements."

# Definitions #

## Definition for well-founded relations ##

A relation $\prec$ on a set $S$ is __weakly extensional__ if, given any elements $x$ and $y$ of $S$, $x = y$ whenever (for all $t$) $t \prec x$ if and only if $t \prec y$.

Interpreting $\prec$ as membership $\in$, this corresponds to the [[axiom of extensionality]] as usually stated for [[pure set]]s. However, it is really only appropriate when $\prec$ is [[well-founded relation|well-founded]], just as the usual axiom of extensionality must be strengthened in the absence of the [[axiom of foundation]]. For example, consider the set $\{a,b\}$ where $a\prec b$ and $b\prec a$; then $a$ and $b$ cannot really be distinguished by their $\prec$-elements, but this set does satisfy the above criterion.

However, when $\prec$ is well-founded, weak extensionality is equivalent to all the stronger notions below; thus in that case it is usually called just **extensionality**.


## Definition using isomorphisms ##

One tempting way to deal with non-well-founded relations is as follows.  Let $\prec^*$ be the reflexive-[[transitive closure]] of the relation $\prec$ on $S$ (so $\prec^*$ is a [[preorder]]).  Given an element $x$ of $S$, let $S_x$ be the [[downset]] of $x$ under $\prec^*$, equipped with the restriction of $\prec$.  Then say that the relation $\prec$ is extensional if, given any elements $x$ and $y$ of $S$, $x = y$ whenever $S_x$ and $S_y$ are isomorphic as sets equipped with a relation $\prec$.

Unfortunately, as pointed out by Aczel in Chapter 4 of [Non-Well-Founded Sets](http://standish.stanford.edu/pdf/00000056.pdf), this definition does not even imply weak extensionality.  Consider the set $S=\{a,b\}$ where $b\prec a$ and $b\prec b$.  Then $S_a = S$ but $S_b = \{b\}$, so they are not isomorphic and this criterion does not require $a=b$; however it is true that $t\prec a$ if and only if $t\prec b$, so weak extensionality _would_ require $a=b$.

This can easily be resolved as follows, however: instead of $S_x$, consider the 'strict downset' $(S\downarrow x)$, which is defined to consist of all $y$ for which there exists a chain
$$y\prec y_1\prec \dots\prec y_n \prec x$$
where $n\ge 0$.  Following Aczel, we say that $\prec$ is **Finsler-extensional** if for any $x,y\in S$, if $(S\downarrow x)\cong (S\downarrow y)$ then $x=y$.  It is easy to show that Finsler-extensional implies weakly-extensional, and (using [[induction]]) that the converse is true for well-founded relations.


## Definition using bisimulations ##

Finsler-extensionality is often also not strong enough, however.  Consider the set $\{a,b_0,b_1,b_2,\dots\}$ where $a\prec a$ and $b_{n+1}\prec b_n$ for all $n$.  Then both $a$ and $b_0$ (and, in fact, every $b_n$) are characterized by a single infinite descending chain of $\prec$-elements, namely $\dots \prec a \prec a \prec a$ and $\dots \prec b_2\prec b_1\prec b_0$.  But $a\neq b_0$ and yet this set is Finsler-extensional.

To remedy this, we give the following definition.  Let $S$ be equipped with a binary relation $\prec$.  A **bisimulation** on $S$ is a binary relation $\sim$ such that whenever $x\sim y$, for any $a\prec x$ there is a $b\prec y$ with $a\sim b$, and for every $b\prec y$ there is an $a\prec x$ with $a\sim b$.  We then say that $\prec$ is **(strongly) extensional** if every bisimulation is contained in the identity relation; i.e. if $\sim$ is a bisimulation then $x\sim y$ implies $x=y$.  Again, it is easy to show that extensionality in this sense implies Finsler-extensionality, hence also weak extensionality, and is equivalent to weak extensionality for well-founded relations.

# Extensional quotients #

Weak extensionality is a kind of [[antisymmetric relation|antisymmetry]] condition: Let $x \leq y$ mean that $t \prec y$ whenever $t \prec x$.  Then $\leq$ is clearly a [[preorder]], which is antisymmetric (so a [[partial order]]) if and only if $\prec$ is weakly extensional.

Now suppose that if $t \prec x$ if and only if $t \prec y$ for all $t$, then $x \prec z$ if and only if $y \prec z$ for all $z$.  Then if we define $x\sim y$ to mean $x\leq y$ and $y\leq x$, $\sim$ is an equivalence relation such that $\prec$ descends to a weakly extensional relation on the [[quotient set]] $S/{\sim}$.

Strongly extensional quotients are even easier to construct.  It is easy to see that the union of any family of bisimulations is a bisimulation, and therefore there is a largest bisimulation $\approx$ for any binary relation $\prec$ on $S$.  Moreover, $\approx$ is an equivalence relation (though not every bisimulation need be so), and $\prec$ descends to a (strongly) extensional relation on the quotient $S/\approx$.


## Morphisms ##

+--{: .query}
[[Mike Shulman|Mike]]: I don't think this is the right notion of morphism.  It's not really clear to me that there is a notion that deserves to be called a "morphism of extensional relations," but if I had to pick one it would be a simulation (see my comment at [[well-founded relation]]).  For instance, strong extensionality for $S$ is equivalent to saying that any two simulations $T \;\rightrightarrows\; S$ are equal, and also to saying that any simulation $S\to T$ is an injection.

_Toby_:  I think that we can just say that my definitions (both of 'extensional' in the general context and of 'morphism' here) are simply wrong.  Unless you think that they have pedagogical value, we can even delete them.
=--

Let $S$ and $T$ be sets, each equipped with an extensional relation $\prec$.  Then a [[function]] $f: S \to T$ is a __morphism__ of sets so equipped if it always induces [[isomorphism]]s (of sets equipped with an arbitrary binary [[relation]] on each) from $S_x$ to $S_{f(x)}$.

The interesting thing about extensional relations is that any such morphism must be unique.  That is, we have a (large) [[poset]] of sets equipped with extensional relations.


## Applications ##

Well-founded relations are often used to represent [[axiom of foundation|well-founded]] [[pure set]]s.  In this case, where $\prec$ represents the 'membership' relation $\in$, a restriction to (weakly) extensional such relations corresponds to imposing the [[axiom of extensionality]] (that two sets are equal if they have the same elements).  For non-well-founded sets, one usually wants to impose one of the stronger versions of extensionality.

A well-founded relation that is both extensional and [[transitive relation|transitive]] is precisely a [[well-order]].
