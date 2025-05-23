
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

__$Loc$__ or **$Locale$** is the [[category]] whose [[objects]] are [[locales]] and whose [[morphisms]] are [[continuous maps]] between locales.  By definition, this means that $Loc$ is the [[opposite category]] of [[Frm]], the category of [[frames]].

$Loc$ is used as a substitute for [[Top]] if one wishes to do [[topology]] with locales instead of standard [[topological spaces]].

$Loc$ is naturally a [[(1,2)-category]]; its [[2-morphisms]] are the pointwise ordering of [[frame]] homomorphisms. 

+-- {: .num_defn}
###### Definition

The [[2-category]] [[Locale]] has

* as [[object|objects]] $X$ [[frame|frames]] $Op(X)$;

* as [[morphisms]] $f : X \to Y$ frame homomorphisms $f^* : Op(Y) \to Op(X)$;

* a unique [[2-morphism]] $f \Rightarrow g$ whenever for all $U \in Op(Y)$ we have a (then necessarily unique) morphism $f^* U \to g^* U$.

=--

(For instance [Johnstone, C1.4, p. 514](#Johnstone).)


## Properties

For any [[base topos]] $S$ the [[2-category]] $Loc(S)$ of [[internal locales]] in $S$ is [[equivalence of categories|equivalent]] to the [[subcategory]] of the [[over topos|slice]] of [[Topos]] over $S$ on the [[localic geometric morphism|localic geometric morphisms]]. See there for more details.

See [[locale]] for more properties.


The [[2-functor]] that forms [[category of sheaves|categories of sheaves]]

$$
  Sh : Locale \to Topos
$$

exhibits $Locale$ as a [[full sub-2-category]] of [[Topos]]. See _[[localic reflection]]_ for more on this.

## Related concepts

* [[category of coherent locales]]

## References

For instance Section C1 of 

*  [[Peter Johnstone]], _[[Elephant|Sketches of an elephant: a topos theory compendium]]_.
 {#Johnstone}


[[!redirects Loc]]
[[!redirects Locale]]
[[!redirects category of locales]]
[[!redirects the category of locales]]

category: category
