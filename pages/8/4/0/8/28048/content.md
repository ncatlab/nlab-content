
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


\tableofcontents

## Definition


Denote by 

* $\mathscr{H}$ [[generalized the|the]] countably-infinite-dimensional [[separable Hilbert space|separable]] [[Hilbert space]],

* $\mathcal{B}(\mathscr{H})$ the [[norm topology]]-space of [[bounded operators]],

* $\mathcal{K}(\mathscr{H}) \subset \mathcal{B}(\mathscr{H})$ the [[subset]] of [[compact operators]],

* $GL(\mathscr{H}) \subset \mathcal{B}(\mathscr{H})$ the [[general linear group]],

* $\mathrm{U}(\mathscr{H}) \subset GL(\mathscr{H})$ the [[unitary group]] (cf. at *[[U(ℋ)]]*).

\begin{definition}
  The *Fredholm group* of $\mathscr{H}$ is the [[subgroup]] of the [[general linear group]] of those [[elements]] which differ from the [identity operator](identity+morphism#IdentityOperator) by a [[compact operator]]:

\[
  GL^c(\mathscr{H})
  \coloneqq
  \big\{
    \phi \in GL(\mathscr{H})
    \,\big\vert\,
    \phi - id \in \mathcal{K}(\mathscr{H})
  \big\}
  \,.
\]

(cf. [Atiyah & Singer 1969 pp 10](#AtiyahSinger69), [Swanson 1978 p 191](Swanson1978), [Mukherjea 1970 p. 653](#Mukherjea1970))

Analogously, the *unitary Fredholm group* is the [[subgroup]] of [[U(ℋ)]] of those [[elements]] which differ from the [identity operator](identity+morphism#IdentityOperator) by a [[compact operator]]:

\[
  U^c(\mathscr{H})
  \coloneqq
  \big\{
    U \in \mathrm{U}(\mathscr{H})
    \,\big\vert\,
    U - id \in \mathcal{K}(\mathscr{H})
  \big\}
  \,.
\]

(cf. [Atiyah & Singer 1969 pp 10](#AtiyahSinger69), [Andruchow & Larotonda 2010](#AndruchowLarotonda2010), [DSBW 2023 p. 87, 247](#DSBW2023))

\end{definition}


## References

The Fredholm group is named in variation of *[[Fredholm operators]]* after *[[Ivar Fredholm]]*.


Mentioning of the Fredholm group:

* {#AtiyahSinger69} [[Michael Atiyah]], [[Isadore Singer]], pp 10 of: *Index theory for skew-adjoint Fredholm operators*,  Publications Mathématiques de l’Institut des Hautes Scientifiques **37** 1 (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [pdf](http://www.maths.ed.ac.uk/~aar/papers/askew.pdf)&rbrack;
  > (not calling these groups by any name other than a symbol)

* {#Mukherjea1970} Kalyan K. Mukherjea: *The Homotopy Type of Fredholm Manifolds*, Transactions of the AMS **149** (1970) 653-663 &lbrack;[doi:10.1090/S0002-9947-1970-0259954-4](https://doi.org/10.1090/S0002-9947-1970-0259954-4), [pdf](https://www.ams.org/journals/tran/1970-149-02/S0002-9947-1970-0259954-4/S0002-9947-1970-0259954-4.pdf)&rbrack;

* {#Swanson1978} R. C Swanson: *Fredholm intersection theory and elliptic boundary deformation problems, I*, Journal of Differential Equations **28** 2 (1978) 189-201 \[<a href="https://doi.org/10.1016/0022-0396(78)90066-9">doi:10.1016/0022-0396(78)90066-9</a>\]

Mentioning of the unitary Fredholm group:

* {#AtiyahSinger69} [[Michael Atiyah]], [[Isadore Singer]]: *Index theory for skew-adjoint Fredholm operators*,  Publications Mathématiques de l’Institut des Hautes Scientifiques **37** 1 (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [pdf](http://www.maths.ed.ac.uk/~aar/papers/askew.pdf)&rbrack;

* {#AndruchowLarotonda2010} Esteban Andruchow, Gabriel Larotonda: *The rectifiable distance in the unitary Fredholm group*, Studia Mathematica Volume **196** 2 (2010) 151-178 &lbrack;[arXiv:0812.4475](https://arxiv.org/abs/0812.4475), [eudml:285458](https://eudml.org/doc/285458)&rbrack;


* {#DSBW2023} Nora Doll, [[Hermann Schulz-Baldes]], [[Nils Waterstraat]], Sections 3.7 and 8.1 in: *Spectral Flow --- A Functional Analytic and Index-Theoretic Approach*, Studies in Mathematics **94**, De Gruyter (2023) &lbrack;[doi:10.1515/9783111172477](https://doi.org/10.1515/9783111172477), [hdl:20.500.12657/63798](https://library.oapen.org/handle/20.500.12657/63798), ch8:[[DSBW23-HomotopyFredholmOps.pdf:file]]&rbrack;

[[!redirects Fredholm groups]]

[[!redirects unitary Fredholm group]]
[[!redirects unitary Fredholm groups]]
