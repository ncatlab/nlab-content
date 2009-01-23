## Definition in ordinary category theory ##

A **limit** of some [[diagram]] $F$ is a [[universal construction|universal]] [[cone]] to $F$. In more detail, it is a cone $\theta$ from an object denoted $lim F$ to $F$, such that given any cone $\gamma: \Delta c \to F$, there exists a unique morphism $f: c \to lim F$ such that 
$$\gamma = (\Delta c \stackrel{\Delta f}{\to} \Delta lim F \stackrel{\theta}{\to} F$$ 
(Given $f: c \to d$, $\Delta f: \Delta c \to \Delta d$ is the evident natural transformation whose component at each object $j$ of $J$ is $f: c \to d$.) 

[To be continued...]

Here are some important examples of limits:

* A limit of the [[diagram|empty diagram]] is a [[terminal object]].
* A limit of a diagram consisting of two (or more) objects is their [[product]].
* A limit of a [[cospan]] is a [[pullback]].
* A limit of a pair (or more) of [[parallel morphisms]] is an [[equalizer]].

#Remarks#

* The meaning of the notion of limit is possibly best appreciated by regarding them in the context of [[representable functor]]s (as explained there).