
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



\tableofcontents


## Definition

A [[point]] of a [[topological space]] is called **focal** ([Freyd & Scedrov 1990](#FreydScedrov1990)) if its only [[open neighbourhood]] is the entire space.

Equivalently, a point is focal if it is a [[bottom]] element in the [[specialization preorder]] of the space.

## Examples 

* The closed point $\bot$ of [[Sierpinski space]] $\mathbf{2}$ is a focal point. 

* The vertex $v$ of a Sierpinski cone (or [[scone]]) $s(X)$ on a space $X$, given by a pushout in $Top$ 
$$\array{
1 \times X & \to & 1 \\
\mathllap{\bot \times 1_X} \downarrow & & \downarrow \mathrlap{v} \\
\mathbf{2} \times X & \to & s(X),
}$$
is a focal point. This construction is in fact the same as generically adding a focal point to $X$.

* The [[prime spectrum]] of a ring $A$ has a focal point iff $A$ is a [[local ring]]. In this case, the focal point is given by the unique maximal ideal of $A$.

## Properties

The [[category of sheaves]] over (the [[site of open subsets]]) of a topological space with focal point is a [[local topos]].

Every [[topos]] has a [[free construction|free]] "completion" to a "focal space", given by its [[Freyd cover]].

## In locale theory

A [[locale]] $X$ is called **local** if in any covering of $X$ by opens $U_i$, at least one $U_i$ is $X$.

The locale associated to an [[sober space]] is local in this sense if and only if the space possesses a focal point (see [Johnstone, discussion preceding lemma C1.5.6](#Johnstone)). Locale theoretically, this point is then given by the [[frame|frame homomorphism]]
$$ \mathcal{O}(X) \to \Omega, \quad U \mapsto \{ \star | U = X \}, $$
where $\Omega$ is the [[frame of opens]] of the [[point]].

## References

* {#FreydSkedrov1990} [[Peter Freyd]], [[Andre Scedrov]]: *[[Categories, Allegories]]*, Mathematical Library **39** North-Holland (1990) &lbrack;[ISBN 978-0-444-70368-2](https://www.elsevier.com/books/categories-allegories/freyd/978-0-444-70368-2)&rbrack; 

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant|Sketches of an Elephant – A Topos Theory Compendium]]_ (2002)

[[!redirects focal points]]

