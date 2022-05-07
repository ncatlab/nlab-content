
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given a [[group]] $G$ (generally: a [[group object]] in some ambient [[category]] $\mathcal{C}$) and a [[group action]] (generally an [[action object]] in $\mathcal{C}$)

\[
  \label{ActionMorphism}
  G \times A \overset{\rho}{\longrightarrow} X
\]

the *shear map* is the [[morphism]]

$$
  \array{
    G \times A
    &\overset{ (\rho,pr_2) }{\longrightarrow}&
    A \times A
    \\
    (g,a) &\mapsto& \big( \rho(g)(a), a \big)
    \,.
  }
$$

form the [[Cartesian product]] of (the [[objects]] underlying) $G$ and $A$ to that of $A$ with itself, whose first component is the [[action]] morphism (eq:ActionMorphism) and whose second component is the [[projection]] onto the second factor (or the other way around, equivalently).

The action $(A,\rho)$ is called:

* a *[[free action]]* if the shear map is a [[monomorphism]],

* a *[[transitive action]]* if the shear map is an [[epimorphism]],

* a *[[regular action]]* or *$G$-[[torsor]]* if the shear map is an [[isomorphism]] (or rather a *[[pseudo-torsor]]* if $A$ is not required to be [[inhabited]]).

Often this is considered in the case that:

1. $\mathcal{C}$ is a [[slice category]] over an object $X$, 

1. $G$ is a [[trivial bundle]] of groups over $X$, then still denoted $G$

in which case 

1. $A = (P \overset{p}{\longrightarrow} X)$ is a [[bundle]] over $X$,

1. $A \times A \,=\, P \times_X P$ is the [[fiber product]] over $X$,

1. $\rho$ is a [[fiber]]-wise [[action]],

in which case the shear map, seen as a morphism in $\mathcal{C}$, reads:

\[
  \label{ShearMapForBundles}
  \array{
    G \times P
    &\overset{ (\rho, pr_2) }{\longrightarrow}&
    P \times_X P
    \\
    (g,p) &\mapsto& \big( \rho(g)(p), p \big)
    \,.
  }
\]

Here $P$ with this action is called a *$G$-[[principal bundle]]* (not necessarily [[locally trivial]]) if the shear map is an [[isomorphism]], or rather a *[[formally principal bundle]]* if $P$ is allowed to be an [[empty bundle]].

Notice that this condition (eq:ShearMapForBundles) is equivalent to the condition that we have a [[pullback square]] as follows:

$$
  \array{
     G \times P
     &\overset{\rho}{\longrightarrow}&
     P
     \\
     {}^{\mathllap{pr_2}}
     \big\downarrow
     &{}^{{}_{(pb)}}&
     \big\downarrow {}^{\mathrlap{p}}
     \\
     P
     &\underset{p}{\longrightarrow}&
     X
     \mathrlap{\,,}
  }
$$

because the shear map (eq:ShearMapForBundles) is the universal comparison morphism induced from the [[commuting square|commutativity]] of this square to the manifest [[fiber product]] pullback.

## Related concepts

* [[group action]]

* [[torsor]], [[pseudo torsor]]

* [[principal bundle]]


## References

Early explicit appearance of the shear map:

* {#Grothendieck60} [[Alexander Grothendieck]], p. 312 (15 of 30) in: *Technique de descente et théorèmes d’existence engéométrie algébrique. I. Généralités. Descente parmorphismes fidèlement plats*, Séminaire N. Bourbaki, 1960, exp. no190, p. 299-327 ([numdam:SB_1958-1960__5__299_0](http://www.numdam.org/item/?id=SB_1958-1960__5__299_0))



[[!redirects shear maps]]




