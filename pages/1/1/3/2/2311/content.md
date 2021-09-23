
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[multiplicative cohomology theory|multiplicative]] [[cohomology theory]] $E$ is called _even_ if its [[cohomology ring]] is trivial in all odd degrees:

$$
  E^{2k+1}(X) = 0
  \,.
$$

## Properties

For an even cohomology theory $E$:

* There is an isomorphism of rings 

$$ E^{\ast}(\mathbb{C}P^n) \cong E^{\ast}(S^0)[x]/\langle x^{n+1} \rangle,$$ 

where $|x|=2$.

* $E^{\ast}(\mathbb{C}P^{\infty} \times \ldots \times \mathbb{C}P^{\infty}) \cong E^{\ast}(S^0)[[x_1, \ldots, x_k]]$.

* Any even cohomology theory is [[complex oriented cohomology theory|complex orientable]]; a choice of complex orientation gives an isomorphism

$$E^{\ast}(\mathbb{C}P^{\infty}) \cong E^{\ast}(S^0)[[x]].$$

([Mehrle 18, 1.1](#Mehrle18))



## Related entries

* [[even periodic ring spectrum]]

* [[A Survey of Elliptic Cohomology - cohomology theories]]

## References

* {#Mehrle18} David Mehrle, _Chromatic homotopy theory: Journey to the frontier_, Graduate workshop notes, Boulder 16-17 May 2018, ([pdf](http://pi.math.cornell.edu/~dmehrle/notes/conferences/cht/cht-notes.pdf))


[[!redirects even cohomology theories]]
