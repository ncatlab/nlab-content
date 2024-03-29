[[!redirects separated (∞,1)-presheaf]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .un_defn}
###### Definition


A  **separated** [[(∞,1)-presheaf]] over an [[(∞,1)-site]] $C$ is a [[(∞,1)-presheaf]] $X : C^{op} \to $ [[∞Grpd]] such that [[covering]] families $\{U_i \to U\}$ in $C$ the [[descent]] comparison morphism

$$
  X(U) \to PSh_{(\infty,1)}(S(\{U_i\}), X)
$$ 

is a [[full and faithful (∞,1)-functor]] and hence exhibits a full 
[[sub-(∞,1)-category]].

(Here $S(\{U_i\})$ denotes the [[sieve]] associated to the cover).

More generally, $X$ is **$k$-separated** for $k \in \mathbb{N}$ if the  descent morphism is a $(k-2)$-[[n-truncated|truncated morphism]].

=--

Notice that this means that a _0-separated $(\infty,1)$-presheaf_ is one whose descent morphisms are [[equivalence in an (∞,1)-category|equivalences]], hence those which are [[(∞,1)-sheaves]].


## Related concepts

* [[separated presheaf]]

* [[separated (2,1)-presheaf]]

* **separated (∞,1)-presheaf**


[[!redirects separated (∞,1)-presheaves]]

