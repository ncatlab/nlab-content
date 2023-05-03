
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

The Schouten bracket on [[multivector fields]] is the unique (up to a multiplication by a constant) [[natural operation]]
$$\Gamma(\Lambda^k TM)\otimes\Gamma(\Lambda^l TM)\to\Gamma(\Lambda^{k+l-1} TM).$$

Concretely,
$$[X_1\wedge\cdots\wedge X_k,Y_1\wedge\cdots\wedge Y_l]=\sum_{i,j}(-1)^{i+j}[X_i,Y_j]\wedge X_1\wedge\cdots\hat X_i\cdots\wedge X_k\wedge Y_1\wedge\cdots \hat Y_j\cdots \wedge Y_l.$$

For multivector fields regarded as “[[antifields]]” in [[BV-BRST formalism]], the Schouten bracket is called the _[[antibracket]]_.


## Related concepts

* [[Frölicher–Nijenhuis bracket]]

* [[Nijenhuis–Richardson bracket]]

## References

* [[Jan Schouten]], _Über Differentialkonkomitanten zweier kontravarianten Grössen_, Indagationes Mathematicae 2 (1940), 449–452.

* [[Jan Schouten]], _On the differential operators of the first order in tensor calculus_, In: Convegno Int. Geom. Diff. Italia. (1953), 1–7.

* [[Albert Nijenhuis]], _Jacobi-type identities for bilinear differential concomitants of certain tensor fields I_, Indagationes Mathematicae **17** (1955) 390–403 &lbrack;[doi:10.1016/S1385-7258(55)50054-0](https://doi.org/10.1016/S1385-7258(55)50054-0)&rbrack;

[[!redirects Schouten-Nijenhuis bracket]]
[[!redirects Schouten–Nijenhuis bracket]]
[[!redirects Schouten-Nijenhuis brackets]]
[[!redirects Schouten–Nijenhuis brackets]]
