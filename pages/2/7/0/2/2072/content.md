
# Idea #

Let $p : E \to X$ be an [[(∞,1)-functor]] of [[(infinity,1)-category|(∞,1)-categories]]. A _cartesian section_ of $p$ is a [[section]] $\sigma : X \to E$ that sends all 1-morphisms in $X$ to [[Cartesian morphism]]s in $E$.

#Definition#

...

#Remarks#

If $p : E \to X$ is a [[Cartesian fibration]] classified by an [[(∞,1)-functor]] $F : X \to (\infty,1)Cat^{op}$ then $\Gamma_X^{cart}(E)$ is equivalent to the [[limit in a quasi-category|limit]] of $F$

$$
  \Gamma_X^{cart}(E) \simeq lim F 
  \,.
$$

See the discussion at [[limit in a quasi-category]] for details.

#References#

In corollary 3.3.3.2 of 

* [[Jacob Lurie]], [[Higher Topos Theory]] 

the collection of cartesian sections of $p : E \to X$ appears as $Maps_X^\flat(X^#, E^{cart})$.

Here 

* the [[simplicial set]] $Maps_X^\flat(\cdots)$ is the simplicial set underlying the [[internal hom]] of [[marked simplicial set]]s over $X$ (beginning of section 3.1.3);

* $X^#$ is the [[simplicial set]] $X$ with _all_ cells marked (beginning of section 3.1)

* and  $E^{cart}$ is $E$ with precisely all [[Cartesian morphism]]s marked (def. 3.1.1.9).


[[!redirects (∞,1)-category of cartesian sections]]
[[!redirects (infinity,1)-category of cartesian section]]
