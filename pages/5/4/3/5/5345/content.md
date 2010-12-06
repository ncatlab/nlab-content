

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A _simplicial groupoid_ is a [[simplicial object]] in the [[category]] [[Grpd]] of [[groupoids]] whose [[simplicial set]] of objects is simplicially constant. Write $s Grpd$ for the category of simplicial groupoids.

There is a [[model category]] structure on $sGrpd$ whose

* fibrations are the morphisms $f : H \to K$ such that 

  1. for every [[object]] $x$ of $H$ and every morphism $\omega : g(x) \to y$ in $K_0$ there is a morphism $\hat \omega : x \to z$ of $H_0$ such that $f(\hat \omega) = \omega$;

  1. for every object $x$ in $H$ the induced morphism $f : H(x,x) \to K(f(x), f(x))$ is a [[Kan fibration]].

* weak equivalences are morphisms $f : H \to K$ such that

  1. $f$ induces in [[isomorphism]] on connected components $\pi_0 f : \pi_0 H \to \pi_0 K$;

  1. for each object $x$ of $H$ the induced morphism $H(x,x) \to K(f(x), f(x))$ is a weak equivalence in the [[model structure on simplicial groups]] or equivalently in the [[model structure on simplicial sets]].

## References

After corollary 7.3 in chapter V of

* [[Paul Goerss]] and J. F. Jardine, 1999, _Simplicial Homotopy Theory_, number 174 in Progress in Mathematics, Birkhauser. ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))
