
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


\tableofcontents

## Idea

A *quadratic Gauss sum* is a sum of square-powers of primitive [[roots of unity]]:

\[
  \label{BasicQuadraticGaussSum}
  \sum_{s = 0}^{k-1}
  e^{
    \tfrac{2 \pi \mathrm{i}}{k}
    s^2
  }
  \;\;
  \in
  \;
  \mathbb{C}
  \,,
  \;\;\;\;\;\;
  \text{for} \; k \in \mathbb{N}_{> 0}
  \,.
\]

A *generalized Gauss sum* is a variant of this expression, admitting other prefectors or powers of $s$ in the exponent.


## Properties

\begin{proposition}\label{EvaluationOfQuadraticGaussSum}
**(evaluation of the quadratic Gauss sum)**
\linebreak
The basic quadratic Gauss sum (eq:BasicQuadraticGaussSum) evaluates to:
\[
  \label{EvaluationFormulaOfQuadraticGaussSum}
  \sum_{s = 0}^{k-1}
  e^{
    \tfrac{2 \pi \mathrm{i}}{k}
    s^2
  }
  \;\;
  =
  \;\;
  \left\{
  \begin{array}{ccl}
    (1 + \mathrm{i}) \sqrt{k} &\vert& m = 0 \;mod\; 4
    \\
    \sqrt{k} &\vert& m = 1 \;mod\; 4
    \\
    0 &\vert& m = 2 \;mod\; 4
    \\
    \mathrm{i} \sqrt{k} &\vert& m = 3 \;mod\; 4
    \mathrlap{\,.}
  \end{array}
  \right.
\]
\end{proposition}
The original proof is due to [Gauss 1811](#Gauss1811), an early alternative proof is due to [Dirichlet 1835](#Dirichlet35), reviewed in [Dirichlet 1871](#Dirichlet1871). Modern review includes [Doyle 2016  (1.1)](#Doyle16), [Ram Murty & Pathak 2017 Thm. 1.1](#MurtyPathak17), [Taylor 2022 Thm. 1.16](#Taylor22).

\begin{proposition}
\label{EvaluationOfQuadraticGaussSumWithHalfedExponents}
**(evaluation of quadratic Gauss sum with halfed exponents)**
\linebreak
For the variant of (eq:EvaluationFormulaOfQuadraticGaussSum) with half the usual exponents we have
$$
  \sum_{s = 0}^{k-1}
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    s^2
  }
  \;\;
  =
  \;\;
  \left\{
  \begin{array}{ccl}
    \sqrt{k} \, e^{\pi \mathrm{i}/4}
    &\vert&
    k \in 2 \mathbb{N}_{\gt 0}
    \\
    ? &\vert& k \in 2 \mathbb{N} + 1
  \end{array}
  \right.
$$
\end{proposition}
Proofs are given at [MO:a/4232289](https://math.stackexchange.com/a/4232289/58526) and [MO:a/489863](https://mathoverflow.net/a/489863/381).


## Related concepts

* [[quadratic reciprocity]]


## References

The original proof of Prop. \ref{EvaluationOfQuadraticGaussSum} is due to 

* {#Gauss1811} [[Carl F. Gauss]]: *Summatio Quarumdam Serierum Singularium* Societas Regia Scientiarum Gottingensis (1811)

and an early alternative proof, using a variant of [[Poisson summation]], is due to 

* {#Dirichlet35} [[P. G. L. Dirichlet]]: &Uuml;ber eine neue Anwendung bestimmter Integrale auf die Summation endlicher oder unendlicher Reihen. Abhandlungen der K&ouml;niglich Preussischen Akademie der Wissenschaften (1835)

reviewed in:

* {#Dirichlet1871} [[P. G. L. Dirichlet]]: *Vorlesungen über Zahlentheorie*, Vieweg und Sohn (1871) &lbrack;[eudml:204463](https://eudml.org/doc/204463)&rbrack;

Further discussion:

* Kenneth Ireland, Michael Rosen: *Quadratic Gauss Sums*, chapter 6 in: *A Classical Introduction to Modern Number Theory*, Graduate Texts in Mathematics **84**, Springer (1990) &lbrack;[doi:10.1007/978-1-4757-1779-2_6](https://doi.org/10.1007/978-1-4757-1779-2_6)&rbrack;

* [[Lisa Jeffrey]], Props. 2.3 and 4.3 in: *Chern-Simons-Witten invariants of lens spaces and torus bundles, and the semiclassical approximation*, Commun.Math. Phys. **147** (1992) 563–604 &lbrack;[doi:10.1007/BF02097243](https://doi.org/10.1007/BF02097243), [spire:342446](https://inspirehep.net/literature/342446)&rbrack; 
  > (reciprocity formulas in the context of [[Chern-Simons theory]])


* Bruce C. Berndt, Ronald J. Evans, Kenneth S. Williams: *Gauss and Jacobi Sums*, John Wiley & Sons (1998) &lbrack;[ISBN:978-0-471-12807-6](https://www.wiley-vch.de/de/fachgebiete/mathematik-und-statistik/gauss-and-jacobi-sums-978-0-471-12807-6)&rbrack;

* George Danas: *Note on the quadratic Gauss sums*, Int. J. Math and Math. Sciences (2001) &lbrack;[doi:10.1155/S016117120100480X](https://doi.org/10.1155/S016117120100480X)&rbrack;

* Kh. M. Saliba & V. N. Chubarikov: *A generalization of the Gauss sum*, Moscow Univ. Math. Bull. **64** (2009) 92–94 &lbrack;[doi:10.3103/S0027132209020132](https://doi.org/10.3103/S0027132209020132)&rbrack;

* {#Doyle16} Greg Doyle: *Quadratic Form Gauss Sums*, PhD thesis, Ottawa (2016) &lbrack;[doi:10.22215/etd/2016-11457](https://doi.org/10.22215/etd/2016-11457), [[Doyle-QuadraticGaussSum.pdf:file]]&rbrack;

* {#MurtyPathak17} M. Ram Murty, Siddhi Pathak: *Evaluation of the quadratic Gauss sum*, The Mathematics Student **86** 1-2 (2017) 139-150 &lbrack;[pdf](https://mast.queensu.ca/~murty/quadratic2.pdf), [pdf](https://www.cmi.ac.in/~siddhi/Quadratic_Gauss_Sum.pdf)&rbrack;

* {#Taylor22} Laurence R. Taylor: *Gauss Sums in Algebra and Topology* &lbrack;[arXiv:2208.06319](https://arxiv.org/abs/2208.06319)&rbrack;

* Frederik Broucke, Jasson Vindas, section 2 of: *The pointwise behavior of Riemann's function*, J. Fractal Geom. **10** 3/4 (2023) 333-349 &lbrack;[arXiv:2109.08499](https://arxiv.org/abs/2109.08499), [doi:10.4171/jfg/137](https://doi.org/10.4171/jfg/137)&rbrack;

* Nilanjan Bag, Antonio Rojas-León, Zhang Wenpeng: *On some conjectures on generalized quadratic Gauss sums and related problems*, Finite Fields and Their Applications
**86** (2023) 102131 &lbrack;[doi:10.1016/j.ffa.2022.102131](https://doi.org/10.1016/j.ffa.2022.102131)&rbrack;

* Alexander P. Mangerel: *On a rigidity property for quadratic Gauss sums* &lbrack;[arXiv:2502.16014](https://www.arxiv.org/abs/2502.16014)&rbrack;

See also:

* Wikipedia: *[Quadratic Gauss sum](https://en.wikipedia.org/wiki/Quadratic_Gauss_sum)*

* Wikipedia: *[Gauss sum](https://en.wikipedia.org/wiki/Gauss_sum)*

On quadratic Gauss sums with half the usual exponent:

* Gergely Harcos: *The reciprocity of Gauss sums via the residue theorem* &lbrack;[pdf](https://users.renyi.hu/%7Egharcos/gauss_sums.pdf), [[Harcos-ReciprocityOfGaussSums.pdf:file]]&rbrack;

* [MO:q/489862](https://mathoverflow.net/q/489862/381)

[[!redirects Gauss sums]]

[[!redirects quadratic Gauss sum]]
[[!redirects quadratic Gauss sums]]

[[!redirects generalized quadratic Gauss sum]]
[[!redirects generalized quadratic Gauss sums]]

[[!redirects generalized Gauss sum]]
[[!redirects generalized Gauss sums]]


[[!redirects Gauß sum]]
[[!redirects Gauß sums]]

[[!redirects quadratic Gauß sum]]
[[!redirects quadratic Gauß sums]]

[[!redirects generalized quadratic Gauß sum]]
[[!redirects generalized quadratic Gauß sums]]

[[!redirects generalized Gauß sum]]
[[!redirects generalized Gauß sums]]







