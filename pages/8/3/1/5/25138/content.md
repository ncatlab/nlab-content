
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

\tableofcontents


## Idea

In [[homotopy type theory]], the notion of _reduced suspension type_ is an [[axiom|axiomatization]] of the [[reduced suspension]] in [[pointed topological space|pointed]] [[homotopy theory]].

The [[underlying]] type of a [[pointed type|pointed]] reduced suspension type is [[equivalence in type theory]] to the plain [[suspension type]] of the given underlying type, so that, up to [[equivalence in type theory|equivalence]] one may simply take the reduced suspension to be the plain suspension equipped with any one of its terms as basepoint (e.g, [UFP13, Rem. 8.6.3](#UFP13)).

However, in practice it is sometimes convenient to use a different (even if equivalent) construction of the reduced suspension:

## Definition

### As smash product with the circle type

For a given [[type]] $X$, we follow the conventions of the [[reduced suspension]] article and write $\mathrm{S} X$ for the plain [[suspension type]] of $X$ and $\Sigma X$ for the reduced suspension type of $A$. 

The reduced suspension type of a [[pointed type]] $(X,x)$ with [[basepoint]] [[term]]  $x \colon X$ may be defined as the [[smash product type]] of the [[pointed type|pointed]] [[circle type]] $(S^1, s)$ with $X$:

$$
  \Sigma X 
    \;\coloneqq\; 
  (S^1,s) \wedge (X,x)
  \,.
$$



## Properties

The reduced suspension type of the $n$-sphere type $S^n$ is [[equivalence of types|equivalent to]] the $(n + 1)$-sphere type $S^{n + 1}$

$$\Sigma S^n \simeq S^{n + 1}$$

## See also

* [[suspension object]]

  * [[suspension type]], **reduced suspension type**

  * [[suspension]], [[reduced suspension]]

## References

* {#UFP13} [[Univalent Foundations Project]], Rem. 8.6.3 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;



[[!redirects reduced suspension type]]
[[!redirects reduced suspension types]]