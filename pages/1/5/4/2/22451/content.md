
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

Let 

* $F$ be a [[p-adic field]] with $\kappa$ denoting its [[residue field]];

* $\Vert\sigma\Vert$ denotes the [[valuation]] of the corresponding element of $F^{\times}$ under the isomorphism of local [[class field theory]].


\begin{definition}\label{WeilDeligneRepresentation}
**(Weil-Deligne representation)**\linebreak
A *Weil-Deligne representation* is a [[pair]] $(\rho_{0},N)$ where 

* $\rho_{0} \colon W_{F} \to GL_{n}(\mathbb{C})$ is a [[linear representation]] of the [[Weil group]] of $F$ 

and 

* $N$ is a nilpotent _monodromy operator_ 

satisfying 

$$
  \rho_{0}(\sigma)N\rho_{0}(\sigma)^{-1}
   \;=\;
  \left\Vert \sigma \right\Vert N
$$ 

for all $\sigma\in W_{F}$.


\end{definition}


## Related entries

* [[local Langlands correspondence]]


## References

* {#Tate77} [[John Tate]], Section 4 in: *Number theoretic background*, in: *Automorphic forms, representations and L-functions*, Proc. Sympos. Pure Math., Oregon State Univ., Corvallis, Ore. (1977), Part 2, Proc. Sympos. Pure Math., XXXIII, pages 3–26. Amer. Math. Soc., Providence, RI ([ISBN:978-0-8218-3371-1](https://bookstore.ams.org/pspum-33-2), [pdf](http://www.math.ucsd.edu/~csorense/teaching/math205/Tate_Weil.pdf), [[TateNumberTheory.pdf:file]])

* [[Robin Zhang]], *Weil-Deligne Representations I -- Local Langlands seminar* ([pdf](http://math.columbia.edu/~rzhang/files/Weil-Deligne%20Representations%20I.pdf), [[ZhangWeilDeligneRepresentations.pdf:file]])


[[!redirects Weil-Deligne representations]]

