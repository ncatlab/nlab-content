This page is a review of the seminal article

* [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861))

introducing [[Beilinson-Deligne cohomology]], [[Beilinson regulators]], [[higher regulators]], and the [[Beilinson conjectures]].

## Review

### Notation

By [[analytic space]] we will mean [[real analytic space]].  Let $An$ denote the real [[analytic site]].  Let $D^+(An)$ denote the [[derived category]] of bounded above [[cochain complexes]] of [[sheaves]] on $An$.  Let $\Omega^\bullet$ denote the [[de Rham complex]] of [[holomorphic forms]].  Let $F^i = \Omega^{\ge i}$ denote the "stupid" [[filtration]].

Fix a subring $A \subset \mathbf{R}$ and let $A(p) = A \cdot (2\pi i)^p \subset \mathbf{C}$ for $p \in \mathbf{Z}$.  We will abuse notation and write $\mathbf{C}$ for the complex concentrated in degree zero by the constant sheaf associated to $\mathbf{C}$.  Similarly we will view $A(p)$ as an object of $D^+(An)$.

### Main constructions and conjectures

For each $p \in \mathbf{Z}$, the inclusions $F^p \hookrightarrow \Omega^\bullet$ and $A(p) \hookrightarrow \mathbf{C} \hookrightarrow \Omega^\bullet$ induce a canonical morphism
  $$ F^p \oplus A(p) \longrightarrow \Omega^\bullet $$
(given by the difference of the two inclusions).

+-- {: .num_defn}
###### Definition
For $p \in \mathbf{Z}$, the **Beilinson-Deligne complex of weight $p$**, denoted $A(p)_\D$, is defined as the [[mapping cone]] of the above morphism shifted by -1, hence fitting in the [[distinguished triangle]]
  $$ (F^p \oplus A(p))[-1] \longrightarrow \Omega^\bullet[-1] \longrightarrow A(p)_\D \longrightarrow F^p \oplus A(p). $$
=--

The complex $A(p)_D \in D^+(An)$ defines a [[cohomological functor]] $R\Gamma(-, A(p)_D)$ with values in $D^+(A-mod)$.
This is just the [[right derived functor]] of the functor of [[global sections]].

+-- {: .num_defn}
###### Definition
The **Beilinson-Deligne cohomology** of $X \in An$ of weight $p$ and degree $q$ with coefficients in $A$ is
  $$ H_D^q(X, A(p)) = H^q R\Gamma(X, A(p)_D), $$
i.e. the [[sheaf cohomology]].
=--

+-- {: .num_defn}
###### Definition
=--

+-- {: .num_defn}
###### Definition
=--

+-- {: .num_defn}
###### Definition
=--

## References

* {#Beilinson85} [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861)) (reviewed in [Esnault-Viehweg 88](#EsnaultViehweg88))

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))
