
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

and so in which case the shear map, seen as a morphism in $\mathcal{C}$, reads as follows:

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

Early explicit appearance of the shear map, alongside discussion of its [[isomorphism|isomorphy]] ([[pseudo-torsor]]-condition):

* {#Grothendieck60} [[Alexander Grothendieck]], p. 312 (15 of 30) in: *Technique de descente et théorèmes d’existence engéométrie algébrique. I. Généralités. Descente parmorphismes fidèlement plats*, Séminaire N. Bourbaki, 1960, exp. no190, p. 299-327 ([numdam:SB_1958-1960__5__299_0](http://www.numdam.org/item/?id=SB_1958-1960__5__299_0))

* {#Grothendieck67} [[Alexander Grothendieck]], 16.5.15 in: *[[Éléments de géométrie algébrique]]* : IV. *Étude locale des schémas et des morphismes de schémas (Quatrième partie)*, Publications mathématiques de l’I.H.É.S., tome  32 (1967), p. 5-361 ([numdam:PMIHES_1967__32__5_0](http://www.numdam.org/item/PMIHES_1967__32__5_0))

* {#Grothendieck71} [[Alexander Grothendieck]], p. 9 of _Exemples et Complements_ ([doi:10.1007/BFb0058666](https://link.springer.com/chapter/10.1007/BFb0058666), [pdf](https://link.springer.com/content/pdf/10.1007%2FBFb0058666.pdf)), which is p. 293 in:

  [[Alexander Grothendieck]], [[Michèle Raynaud]], *Revêtements étales et groupe fondamental* ([[SGA 1]]),  Lecture Notes in Mathematics **224**, Springer 1971 ([arXiv:math/0206203](https://arxiv.org/abs/math/0206203), [doi:10.1007/BFb0058656](https://link.springer.com/book/10.1007/BFb0058656))


[[!redirects shear maps]]




