
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


\tableofcontents

## Definition

Let $k$ denote the [[ground field]] and $k^\times$ its [[group of units]].


\begin{definition}
Given a [[symplectic vector space]] $(C,\omega)$, its *conformal symplectic group* $CSp(V,\omega)$ is the [[group]] of [[linear isomorphisms]] $f \colon V \to V$ which preserve the [[symplectic form]] up to a scalar $\lambda(f) \in k^\times$:
$$
  \omega\big(
    f(-)
    ,\,
    f(-)
  \big)
  \;=\;
  \lambda(f) 
  \cdot
  \omega(-,-)
  \,.
$$
\end{definition}

(e.g. [Guillemin & Sternberg 1977 p 115](#GuilleminSternberg77), [Malle & Testerman 2012 p. 7](#MalleTesterman12), [Taylor 2021 §1](#Taylor21)).

\begin{remark}
Remembering just this *conformal scale* $\lambda$ evidently constitutes a [[group homomorphism]] from $CSp(V,\omega)$ to $k^\times$, whose [[kernel]] is the ordinary [[symplectic group]]:
$$
  0
  \to
  Sp(V,\omega)
  \longrightarrow
  OSp(V,\omega)
  \xrightarrow{\phantom{-} \lambda \phantom{-}}
  k^\times
  \to 0
  \,.
$$
\end{remark}

\begin{remark}
  In contrast to [[symmetric bilinear forms]], where the [[conformal group]] is typically assumed to rescale only by [[positive numbers]], for [[symplectic forms]] it more generally makes sense to rescale by any non-vanishing number. But beware that some authors constrain elements of a conformal symplectic group to have positive multiplier (e.g. [Jensen & Kruglikov 2020 §7](#JensenKruglikov20)).
\end{remark}


## Related concepts

* [[conformal group]], [[symplectic group]]

* [[conformal invariance and scale invariance]]


## References

* {#GuilleminSternberg77} [[Victor Guillemin]], [[Shlomo Sternberg]], p. 115 of: *Geometric asymptotics*, Mathematical Surveys and Monographs **14**, AMS (1977) &lbrack;[ams:surv-14](https://bookstore.ams.org/surv-14)&rbrack;

* Rudolf Scharlau, Pham Huu Tiep: *Symplectic group lattices*, Trans. Amer. Math. Soc. **351** (1999) 2101-2139 &lbrack;[doi:10.1090/S0002-9947-99-02469-1](https://doi.org/10.1090/S0002-9947-99-02469-1)&rbrack;

* {#MalleTesterman12} Gunter Malle, Donna Testerman, p. 7 of: *Linear Algebraic Groups and Finite Groups of Lie Type*, Cambridge University Press (2012) &lbrack;[doi:10.1017/CBO9780511994777](https://doi.org/10.1017/CBO9780511994777)&rbrack;




* {#Taylor21} D. E. Taylor: *Conjugacy Classes in Finite Conformal Symplectic Groups* (2021) &lbrack;[pdf](https://www.maths.usyd.edu.au/u/don/code/Magma/CSpConjugacy.pdf)&rbrack;

See also:

* {#JensenKruglikov20} Jørn Olav Jensen, Boris Kruglikov: *Differential Invariants of Linear Symplectic Actions* &lbrack;[arXiv:2010.08024](https://arxiv.org/abs/2010.08024)&rbrack;


[[!redirects conformal symplectic groups]]
