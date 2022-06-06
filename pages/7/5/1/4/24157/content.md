+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition ##

In [[homotopy type theory]], an __identity system__ on a type $A$ is a dependent type $a:A \vdash R(a,a)$ indexed by the product type $A \times A$ with a dependent function 
$$r_0: \prod_{a:A} R(a, a)$$ 
such that for any dependent type 
$$a:A, b:B, r: R(a, b) \vdash D(a, b, r)$$
and dependent function 
$$d: \prod_{a:A} D(a, a, r(a))$$ 
there exists a dependent function 
$$f: \prod_{a:A} \prod_{b:B} \prod_{r:R(a, b)} D(a, b, r)$$
and a dependent function
$$e: \prod_{a:A} f(a, a, r(a)) = d(a)$$

## See also ##

* [[dependent type theory]]
* [[identity type]]
* [[homotopy type theory]]

## References ##

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)