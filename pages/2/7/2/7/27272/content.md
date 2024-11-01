
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

A [[Grothendieck topology]] $J$ on a small [[Cauchy complete]] category $\mathcal{C}$ is **rigid** when the corresponding sheaf topos $Sh(\mathcal{C},J)$ is of the form $Set^{\mathcal{D}^{op}}$ for some full subcategory $\mathcal{D}\hookrightarrow \mathcal{C}$. In particular, $Sh(\mathcal{C},J)$ is an [[essential subtopos]] of $Set^{\mathcal{C}^{op}}$.


## Definition

Let $\mathcal{C}$ be a small [[Cauchy complete]] category and $J$ a [[Grothendieck topology ]] on $\mathcal{C}$, an object 
$U\in\mathcal{C}$ is called **$J$-irreducible** if the only covering [[sieve]] is the maximal sieve.

$J$ is called **rigid** when every object $X\in \mathcal{C}$ admits a $J$-[[cover|covering]] by  $J$-irreducible objects.


## Properties

+-- {: .num_prop #rigidsubtopos}
###### Proposition
Let $J$ be a rigid topology on the small Cauchy complete category $\mathcal{C}$ and $J|_{\mathcal{D}}$ the induced [[Grothendieck topology]] on the full subcategory $\mathcal{D}$ of $J$-irreducible objects. Then 
 
$$Sh(\mathcal{C},J)\simeq Sh(\mathcal{D},J|_{\mathcal{D}})\simeq Set^{\mathcal{D}^{op}}\qquad .$$

=--

The first equivalence follows from the [[comparison lemma]] and the second equivalence from the fact that $J|_{\mathcal{D}}$ is the minimal topology on $\mathcal{D}$ whence every presheaf is a sheaf (cf. [Johnstone](#Johnstone02), B2.2.18).
Since $Set^{\mathcal{D}^{op}}\hookrightarrow Set^{\mathcal{C}^{op}}$ arises by [[Kan extension]] of the (full) subcategory inclusion $\mathcal{D}\hookrightarrow \mathcal{C}$ the subtopos inclusion is in fact [[essential subtopos|essential]].


## Related entries

* [[level of a topos]]

* [[Aufhebung]]

## References

* {#Johnstone02} [[Peter Johnstone]], _[[Sketches of an Elephant]] II_, Oxford UP 2002. (C2.2.18, pp.560-563)

* {#Marques24}Jérémie Marquès, _A Criterion for Categories on which every Grothendieck Topology is Rigid_, arXiv:2407.1847 (2024). ([abstract](https://arxiv.org/abs/2407.18417v1))


[[!redirects rigid topologies]]
[[!redirects rigid Grothendieck topology]]
