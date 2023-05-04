
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

The *Schouten bracket* on [[multivector fields]] is &lbrack;[Michor (1987)](#Michor87)&rbrack; the unique (up to a multiplication by a constant) [[natural operation]] on [[multivector fields]]
$$
  \Gamma(\Lambda^k T M)
    \otimes
  \Gamma(\Lambda^l T M)
  \longrightarrow
  \Gamma(\Lambda^{k+l-1} T M)
  \,.
$$

Concretely, it is given in terms of the [[Lie bracket of vector fields]] by:
$$
  [X_1\wedge\cdots\wedge X_k,Y_1\wedge\cdots\wedge Y_l]
  \;=\;
  \sum_{i,j}(-1)^{i+j}
  [X_i, Y_j] \wedge X_1\wedge\cdots\hat X_i\cdots\wedge X_k\wedge Y_1\wedge\cdots \hat Y_j\cdots \wedge Y_l
  .
$$

For [[multivector fields]] regarded as “[[antifields]]” in [[BV-BRST formalism]], the Schouten bracket is called the _[[antibracket]]_.


## Applications

Suppose $P\in\Gamma(\Lambda^2 TM)$.
The the bracket $\{f,g\}=\langle d f\wedge d g,P\rangle$ satisfies the [[Jacobi identity]] (and hence is a [[Poisson bracket]]) if and only if $[P,P]=0$.

## Related concepts

* [[Lie bracket of vector fields]]

* [[Frölicher–Nijenhuis bracket]]

* [[Nijenhuis–Richardson bracket]]

## References

The notion is due to:

* [[Jan Schouten]], _Über Differentialkonkomitanten zweier kontravarianten Grössen_, Indagationes Mathematicae **2** (1940) 449–452

* [[Jan Schouten]], _On the differential operators of the first order in tensor calculus_, In: Convegno Int. Geom. Diff. Italia. (1953) 1–7

* [[Albert Nijenhuis]], _Jacobi-type identities for bilinear differential concomitants of certain tensor fields I_, Indagationes Mathematicae **17** (1955) 390–403 &lbrack;[doi:10.1016/S1385-7258(55)50054-0](https://doi.org/10.1016/S1385-7258(55)50054-0)&rbrack;

A coordinate-free treatment is given in

* W. M. Tulczyjew, _The Graded Lie Algebra of Multivector Fields and the Generalized Lie Derivative of Forms_. Bulletin de l'Académie Polonaise des Sciences. Série des Sciences Mathématiques, Astronomiques et Physiques 22:9 (1974), 937–942.  [PDF](https://dmitripavlov.org/scans/tulczyjew-the-graded-lie-algebra-of-multivector-fields-and-the-generalized-lie-derivative-of-forms.pdf).

Characterization as a [[natural operation]] is due to:

* {#Michor87} [[Peter W. Michor]], *Remarks on the Schouten-Nijenhuis bracket*,  In: Bureš, J. and Souček, V. (eds.): *Proceedings of the Winter School "Geometry and Physics"* Circolo Matematico di Palermo, Palermo (1987) 207-215 &lbrack;[dml:701423](https://dml.cz/handle/10338.dmlcz/701423), [pdf](https://dml.cz/bitstream/handle/10338.dmlcz/701423/WSGP_07-1987-1_21.pdf), [[Michor-SchoutenNijenhuisBracket.pdf:file]]&rbrack;

[[!redirects Schouten-Nijenhuis bracket]]
[[!redirects Schouten–Nijenhuis bracket]]
[[!redirects Schouten-Nijenhuis brackets]]
[[!redirects Schouten–Nijenhuis brackets]]
