# Idea

An [[object]] of a [[category]] is often called *compact* if it is "finite" in some precise sense.

# Compactness in additive categories

When $C$ is an [[additive category]] (often a [[triangulated category]]), an object $x$ in $C$ is called __compact__ if for every set $S$ of objects of $C$ such that the coproduct $\coprod_{s\in S} s$ exists, the canonical map
$$
\coprod_{s\in S} C(x,s)\to C(x,\coprod_{s\in S}s)
$$
is an isomorphism of sets.

A triangulated category is __compactly generated__ if it is generated (see [[generator]]) by a _set_ of compact objects.

The notion can be modified for categories [[enriched category|enriched]] over a [[closed monoidal category]] (compare to the notions of finite and/or rigid objects in various contexts).

Compact objects in the derived categories of quasicoherent sheaves over a scheme are called perfect complexes. Any compact object in the category of modules over a perfect ring is finitely generated as a module.  Lurie uses $\kappa$-compact objects in the setup of $(\infty,1)$-categories.

# Compactness in non-additive categories

In non-additive contexts, the above definition is not right.  For instance, with this definition a [[topological space]] would be compact iff it is [[connected space|connected]].

Instead, in the category [[Top]] of [[topological space]]s one has the following equivalent definitions of when a [[topological space]] $X$ is _compact_ in that every open cover of it has a finite subcover:

$X$ is compact precisely if the [[hom-functor]] $Top(X,-) : Top \to Top$ commutes with [[filtered category|filtered]] [[colimit]]s.

Conversely, for $C$ any category and $X \in C$, the condition that $C(X,-) : C \to C$ preserves [[filtered category|filtered]] [[colimit]]s imposes  some kind of finiteness condition on $X$. For instance 

* in $C = $ [[Set]] this is the case if the set $X$ is [[finite set|finite]];
* in $C$ a [[topos]] this is the case if the object $X$ is $K$-[[finite object|finite]];
* in $C =$ [[Grp]] this is the case if the group $X$ is [[finitely presented object|finitely presented]] as a group.

## Definition ##

An object $x$ is __compact__ if for every [[filtered category|filtered]] or [[direction|directed]] colimit $\colim_{d\in D} S_d$ in $C$, the canonical map
$$
\colim_{d\in D} C(x,S_d)\to C(x,\colim_{d\in D}S_d)
$$
is an isomorphism.  Sometimes, especially in categories like [[Top]], one may want to restrict to directed "unions," meaning directed colimits whose transition morphisms are (possibly [[strong monomorphism|strong]]) [[monomorphism]]s.