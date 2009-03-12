A **(finitely) filtered category** is a [[category]] $C$ in which any finite diagram has a [[cocone]].  That is, for any finite category $D$ and any functor $F:D\to C$, there exists an object $c\in C$ and a natural transformation $F\to \Delta c$ where $\Delta c:D\to C$ is the constant diagram at $c$.

This can be rephrased in more elementary terms by saying that:

* There exists an object of $C$  (the case when $D=\emptyset$)
* For any two objects $c_1,c_2\in C$, there exists an object $c_3\in C$ and morphisms $c_1\to c_3$ and $c_2\to c_3$.
* For any two [[parallel morphisms]] $f,g:c_1\to c_2$ in $C$, there exists a morphism $h:c_2\to c_3$ such that $h f = h g$.

Just as all [[finite limit|finite colimits]] can be constructed from initial objects, binary coproducts, and coequalizers, so a cocone on any finite diagram can be constructed from these three.

More generally, if $\kappa$ is a [[cardinal number]], then a **$\kappa$-filtered category** is one such that any diagram $D\to C$ has a cocone where $D$ has fewer than $\kappa$ arrows.  Note that a [[preorder]] is $\kappa$-filtered as a category just when it is $\kappa$-[[directed set|directed]] as a preorder.

A colimit whose domain is a filtered category is called a **filtered colimit**.  A category whose opposite is filtered is called **cofiltered**, and a limit over a cofiltered category is called a **cofiltered limit** or a **filtered inverse limit**.  Filtered colimits are important in the theory of [[locally presentable category|locally presentable]] and [[accessible category|accessible]] categories.  See also [[pro-object]].
