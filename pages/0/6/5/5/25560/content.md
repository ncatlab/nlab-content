
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Stable Homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### In stable $\infty$-categories

#### Definition

In broad generality, given a [[stable (infinity,1)-category|stable $\infty$-category]] $\mathcal{A}$ equipped with a [[t-structure]] $\mathcal{A}_{\geq n}, \mathcal{A}_{\leq n} \hookrightarrow \mathcal{A}$, the objects in the [[full sub-(infinity,1)-category|full sub-$\infty$-category]] $\mathcal{A}_{\geq n}$ are the *$n$-connective objects*, for any $n \in \mathbb{Z}$.

Here typically one understands that a plain "connective" is short for "0-connective."

Accordingly, the [[coreflective subcategory|coreflections]] $\mathcal{A} \to \mathcal{A}_{\geq n}$ are called the *[[connective cover]]*-constructions.

Dually, the objects of $\mathcal{A}_{\leq n}$ may be called the "$n$-*co*connective objects". For non-negative $k \in \mathbb{N}$ the [[intersection]] $\mathcal{A}_{\geq 0} \cap \mathcal{A}_{\leq k}$ of [[sub-(infinity,1)-categories]] of objects which are both connective and $k$-coconnective  are equivalently the [[n-truncated object in an (infinity,1)-category|$k$-truncted]] connective object:

$$
 \tau_{\leq k} \mathcal{A}_{\geq 0} 
 \;\simeq\; 
 \mathcal{A}_{\geq 0} \cap \mathcal{A}_{\leq k}
  \,.
$$

([Lurie, Warning 1.2.1.9](#LurieHA))


#### Examples

* For the standard [[t-structure]] on an [[(infinity,1)-category of chain complexes|$\infty$-category of chain complexes]], the $n$-connective objects are the $n$-[[connective chain complexes]], namely those which are concentrated in degrees $\geq n$.

* For the standard [[t-structure]] on an [[(infinity,1)-category of spectra|$\infty$-category of spectra]], the $n$-connective objects are the $n$-[[connective spectra]], namely those whose [[stable homotopy groups]] are concentrated in degree $\geq n$.

### In $\infty$-toposes

In an [[(infinity,1)-topos|$\infty$-topos]] one would ---  following traditional in [[algebraic topology]] --- instead speak of the *[[n-connected object in an (infinity,1)-topos|$k$-connected]]* for $k \in \mathbb{N}$. If one insists on saying "connective" also in this case (as is the convention in [[Jacob Lurie|Lurie]]'s *[[Higher Topos Theory]]*) then there is a shift in degree: $n$-connected corresponds to $n+1$ connective. (See [there](n-connected+object+of+an+infinity1-topos#Connectedness) for more.)

## Related concepts

* [[t-structure]]

* [[connective chain complex]]

* [[connective spectrum]]

* [[connective spectrum object]]

## References

For general discussion in the context of [[stable (infinity,1)-categories|stable $\infty$-categories]] see the references at *[[t-structure]]*, such as 

* {#LurieHA} [[Jacob Lurie]], Section 1.2.1 in: *[[Higher Algebra]]*

For the terminology "connective"/"coconnective" in this context, see for instance:

* Harry Smith, Def. 2.1 in: *Bounded t-structures on the category of perfect complexes over a Noetherian ring of finite Krull dimension*, Advances in Mathematics **399** (2022) 108241 &lbrack;[doi:10.1016/j.aim.2022.108241](https://doi.org/10.1016/j.aim.2022.108241), [pdf](http://homepages.math.uic.edu/~hsmith36/Bounded%20t-structures%20on%20perfect%20complexes.pdf)&rbrack;

* Emanuele Pavia, p. 4 of: *t-structures on ∞-categories* (2021) &lbrack;[pdf](https://genoa-logic-group.github.io/itaca-workshop-2021/assets/slides/PaviaE.pdf)&rbrack;

[[!redirects n-connective objects]]

[[!redirects connective object]]
[[!redirects connective objects]]


[[!redirects n-connective]]
[[!redirects n-connective object]]
[[!redirects n-connective objects]]
[[!redirects 0-connective]]
[[!redirects 1-connective]]
[[!redirects 2-connective]]
[[!redirects 3-connective]]
[[!redirects ∞-connective]]
