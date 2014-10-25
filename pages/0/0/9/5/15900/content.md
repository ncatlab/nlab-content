This page is a review of the seminal article

* [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861))

introducing [[Beilinson-Deligne cohomology]], [[Beilinson regulators]], [[higher regulators]], and the [[Beilinson conjectures]].

## Review

### Notation

By [[analytic space]] we will mean [[real analytic space]].  Let $An$ denote the real [[analytic site]].  Let $D^+(An)$ denote the [[derived category]] of bounded above [[cochain complexes]] of [[sheaves]] on $An$.  Let $\Omega^\bullet$ denote the [[de Rham complex]] of [[holomorphic forms]].  Let $F^i = \Omega^{\ge i}$ denote the "stupid" [[filtration]].

Fix a subring $A \subset \mathbf{R}$ and let $A(p) = A \cdot (2\pi i)^p \subset \mathbf{C}$ for $p \in \mathbf{Z}$.  We will abuse notation and write $\mathbf{C}$ for the complex concentrated in degree zero by the constant sheaf associated to $\mathbf{C}$.  Similarly we will view $A(p)$ as an object of $D^+(An)$.

We will write $H^*_B(X, \mathbf{C})$ for the [[Betti cohomology]] of $X \in An$.

### Main constructions and conjectures

#### Beilinson-Deligne cohomology

For each $p \in \mathbf{Z}$, the inclusions $F^p \hookrightarrow \Omega^\bullet$ and $A(p) \hookrightarrow \mathbf{C} \hookrightarrow \Omega^\bullet$ induce a canonical morphism
  $$ F^p \oplus A(p) \longrightarrow \Omega^\bullet $$
(given by the difference of the two inclusions).

+-- {: .num_defn}
###### Definition
For $p \in \mathbf{Z}$, the **Beilinson-Deligne complex of weight $p$**, denoted $A(p)_\D$, is defined as the [[mapping cone]] of the above morphism shifted by -1, hence fitting in the [[distinguished triangle]]
  $$ (F^p \oplus A(p))[-1] \longrightarrow \Omega^\bullet[-1] \longrightarrow A(p)_\D \longrightarrow F^p \oplus A(p). $$
=--

The complex $A(p)_D \in D^+(An)$ defines a functor $R\Gamma(-, A(p)_D)$ on $An$ with values in $D^+(A-mod)$.
This is just the [[right derived functor]] of the functor of [[global sections]]: given $X \in An$, take an [[injective resolution]] of $A(p)_D$ and evaluate each component at $X$, to get a complex of $A$-modules.

+-- {: .num_defn}
###### Definition
The **Beilinson-Deligne cohomology** of $X \in An$ of weight $p$ and degree $q$ with coefficients in $A$ is
  $$ H_D^q(X, A(p)) = H^q R\Gamma(X, A(p)_D), $$
i.e. the [[sheaf cohomology]] or [[hypercohomology]].
=--

+-- {: .num_prop}
###### Proposition
There is a canonical [[long exact sequence]]
  $$ \cdots \to H^{q-1}_B(X, \mathbf{C}) \to H^q_D(X, A(p)) \to F^p H^q_B(X, \mathbf{C}) \oplus H^q(X, A(p)) \to \cdots $$
=--

This follows by applying the [[cohomological functor]] $R\Gamma(X, -)$ to the above [[distinguished triangle]].

+-- {: .num_lemma}
###### Lemma
There are canonical [[quasi-isomorphisms]]
  $$ \begin{aligned}
    A(p)_D &\stackrel{\sim}{\longrightarrow} (A(p) \to \mathcal{O} \to \Omega^1 \to \cdots \to \Omega^{p-1}) \\
    &\stackrel{\sim}{\longrightarrow} (0 \to \mathcal{O}/A(p) \to \Omega^1 \to \cdots \to \Omega^{p-1})
  \end{aligned} $$
=--

#### Cup product

+-- {: .num_prop}
###### Proposition
There exists a canonical morphism in $D^+(An)$
  $$ - \cup - : A(i)_D \otimes^L A(j)_D \longrightarrow A(i+j)_D $$
defining an [[associative]] [[commutative]] multiplication.
=--

In fact, one gets a product on $A(*)_D$ immediately by noting that it is identified with the underlying [[cochain complex]] of the [[homotopy pullback]] of $A(*) \to \Omega \gets F^*$ (as [[dg-algebras]]).

+-- {: .num_defn}
###### Definition
=--

+-- {: .num_defn}
###### Definition
=--

## References

* {#Beilinson85} [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861)) (reviewed in [Esnault-Viehweg 88](#EsnaultViehweg88))

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))
