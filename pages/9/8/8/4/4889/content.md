
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### Externally

Let $\mathcal{C}$ be an [[(∞,1)-category]]. Let $X \in \mathcal{C}$ be an [[object]].

As a [[discrete ∞-groupoid|discrete]] [[∞-group]] the **automorphism $\infty$-group** of $X$ is the [[monomorphism in an (∞,1)-category|sub-]][[∞-groupoid]]

$$
  Aut(X) \hookrightarrow \mathcal{C}(X,X)
$$

of the [[derived hom space]] of [[morphisms]] in $\mathcal{C}$ from $X$ to itself, on those that are [[equivalence in an (∞,1)-category|equivalences]].

This is an [[∞-group]] in [[∞Grpd]], 

$$
 Aut(X)\in Grp(\infty Grpd)
  \,.
$$


### Internally

Let $\mathcal{C}$ be a [[cartesian closed (∞,1)-category]] (for instance an [[(∞,1)-topos]]). Write

$$
  [-,-] : \mathcal{C}^{op} \times \mathcal{C} \to \mathcal{C}
$$

for the [[internal hom]]. Then for $X \in \mathcal{C}$ an object, the _internal automorphism $\infty$-group_ is the [[subobject]]

$$
  \mathbf{Aut}(X) \hookrightarrow [X,X]
$$

of the [[internal hom]] on those morphism that are [[equivalence in an (infinity,1)-category|equivalences]].

In the special case that $\mathcal{C}$ is an [[∞-topos]], the [[delooping]] $\mathbf{B}\mathbf{Aut}(X)$ of the internal automorphism $\infty$-group is equivalently the [[∞-image]]

$$
  * \to \mathbf{B}\mathbf{Aut}(X) \hookrightarrow Obj
$$

of the morphism

$$
  * \stackrel{\vdash X}{\to} Obj
$$

to [[generalized the|the]] [[object classifier]], that modulates $X$ (the "name" of $X$).


### In the syntax of homotopy type theory

Let $\mathcal{C}$ be an [[(∞,1)-topos]]. Then its [[internal language]] is [[homotopy type theory]]. In terms of this the object $X \in \mathcal{C}$ is a [[type]] ([[homotopy type]]). In the type theory syntax the internal automorphism $\infty$-group $\mathbf{Aut}(X)$ then is (as a type, without yet the group structure)

$$
  \vdash (X \stackrel{\simeq}{\to} X) : Type
  \,,
$$

the [[subtype]] of the [[function type]] on the [[equivalence in homotopy type theory|equivalences]]. Its [[delooping]] $\mathbf{B}\mathbf{Aut}(X)$ is

$$
  \vdash \; \left(\sum_{Y : Type} [Y = X]\right) \colon Type
  \,,
$$

where on the right we have [[dependent sum]] over one argument of the [[bracket type]]/[[inhabited type|(-1)-truncation]] $[X = Y] = isInhab(X = Y)$ of the [[identity type]] $(X = Y)$.

The equivalence of this definition to the previous one is essentially equivalent to the [[univalence axiom]].


## Examples

### In a 1-category

If $\mathcal{C}$ happens to be a [[1-category]] then the external automorphism $\infty$-group of an object is the ordinary [[automorphism group]] of that object.

If $\mathcal{C}$ happens to be a 1-[[topos]], then the internal automorphism $\infty$-group is the traditional automorphism [[group object]] in the topos. Etc.

### Of $\infty$-groups

For $G \in \infty Grp(\mathcal{X})$ an [[∞-group]] there is the direct automorphism $\infty$-group $Aut(G)$. But there is also the [[delooping]] $\mathbf{B}G \in \mathcal{X}$ and _its_ automorphism $\infty$-group.

Sometimes (for instance in the discussion of [[∞-gerbes]]) one considers

$$
  AUT(G) := Aut(\mathbf{B}G)
$$

and calls this the automorphism $\infty$-group of $G$.

For instance when $G$ is an ordinary [[group]], $AUT(G)$ is the [[2-group]] discussed at [[automorphism 2-group]].

## Related concepts

There may be the [[stuff, structure, property|structure]] of an [[∞-Lie group]] on $Aut(F)$. The corresponding [[∞-Lie algebra]] is an [[automorphism ∞-Lie algebra]].


* [[group]], [[∞-group]],

* [[automorphism group]], [[automorphism 2-group]], **automorphism $\infty$-group,

* [[center]], [[center of an ∞-group]]

* [[outer automorphism group]], [[automorphism 2-group]], [[outer automorphism ∞-group]]

* [[rigidification of a stack]]

[[!redirects outer automorphism group]]
[[!redirects outer automorphism groups]]

[[!redirects outer automorphisms]]
[[!redirects automorphism ∞-group]]
[[!redirects automorphism ∞-groups]]

[[!redirects automorphism infinity-groups]]

[[!redirects automorphism n-group]]
[[!redirects automorphism n-groups]]
