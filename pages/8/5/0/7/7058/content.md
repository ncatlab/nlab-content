
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $C$ a [[cartesian closed category]] and $L,R : C \to C$ two [[endomorphism|endo]][[functors]], they are called **strong adjoints** to each other if there is a [[natural isomorphism]]

$$
  [L X, A] \simeq [X, R A]
$$

for all [[objects]] $X,A \in C$ and for $[-,-]$ the [[internal hom]].

## Properties

Notice that for $* $ the [[terminal object]] of $C$ we have that the [[global points]] of the internal hom give the external [[hom set]]

$$
  \Gamma [X,A] := C(*, [X, A]) \simeq C(X,A)
  \,.
$$

Therefore strongly adjoint functors are in particular [[adjoint functors]] in the ordinary sense.

## References

For instance appendix 6 of 

* [[Bill Lawvere]], _Outline of synthetic differential geometry_ ([pdf](https://ncatlab.org/nlab/files/LawvereSDGOutline.pdf))


[[!redirects strong adjoint functors]]

[[!redirects strong adjunction]]
[[!redirects strong adjunctions]]


