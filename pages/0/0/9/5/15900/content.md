This page is a review of the seminal article

* [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861))

introducing [[Beilinson-Deligne cohomology]], [[Beilinson regulators]], [[higher regulators]], and the [[Beilinson conjectures]].

## Review

### Notation

By [[analytic space]] we will mean [[real analytic space]].
Let $An$ denote the real [[analytic site]].
Consider the category $Sh(An, Ab)$ of [[abelian sheaves|sheaves]] of [[abelian groups]].
Beilinson denotes by $D^+(An)$ the bounded above [[derived category]], i.e. the category of [[connective]] [[cochain complexes]] up to [[quasi-isomorphism]].

In $D^+(An)$ we have the complex $\Omega^\bullet$, of [[de Rham complex]]es of [[holomorphic forms]].  Let $\Omega^{\ge i}$ denote the "stupid" [[filtration]].

Fix a subring $A \subset \mathbf{R}$ and let $A(p) = A \cdot (2\pi i)^p \subset \mathbf{C}$ for $p \in \mathbf{Z}$.  We will abuse notation and write $\mathbf{C} \in D^+(An)$ also for the constant sheaf valued in the complex concentrated in degree zero.  Similarly we will view $A(p)$ as an object of $D^+(An)$.

We will write $H^*_B(X, \mathbf{C})$ for the [[Betti cohomology]] of $X \in An$.

### Main constructions and conjectures

#### Deligne cohomology

For each $p \in \mathbf{Z}$, the inclusions $\Omega^{\ge p} \hookrightarrow \Omega^\bullet$ and $A(p) \hookrightarrow \mathbf{C} \hookrightarrow \Omega^\bullet$ induce a canonical morphism
  $$ \Omega^{\ge p} \oplus A(p) \longrightarrow \Omega^\bullet $$
(given by the difference of the two inclusions).

+-- {: .num_defn}
###### Definition
For $p \in \mathbf{Z}$, the **Deligne complex of weight $p$**, denoted $A(p)_\D$, is defined as the [[mapping cone]] of the above morphism shifted by -1, hence fitting in the [[distinguished triangle]]
  $$ (\Omega^{\ge p} \oplus A(p))[-1] \longrightarrow \Omega^\bullet[-1] \longrightarrow A(p)_\D \longrightarrow \Omega^{\ge p} \oplus A(p). $$
=--

The Deligne cohomology is just the [[hypercohomology]] of this complex.  That is, consider the [[right derived functor]] $R\Gamma(-, A(p)_D)$ of the functor of [[global sections]] on $An$ with values in $D^+(A-mod)$.

+-- {: .num_defn}
###### Definition
The **Deligne cohomology** of $X \in An$ of weight $p$ and degree $q$ with coefficients in $A$ is
  $$ H_D^q(X, A(p)) = H^q R\Gamma(X, A(p)_D). $$
=--

+-- {: .num_prop}
###### Proposition
There is a canonical [[long exact sequence]]
  $$ \cdots \to H^{q-1}_B(X, \mathbf{C}) \to H^q_D(X, A(p)) \to \Omega^{\ge p} H^q_B(X, \mathbf{C}) \oplus H^q(X, A(p)) \to \cdots $$
=--

This follows by applying the [[cohomological functor]] $R\Gamma(X, -)$ to the above [[distinguished triangle]].

+-- {: .num_lemma}
###### Lemma
For $p \le 0$ there is a canonical [[quasi-isomorphism]]
  $$ A(p)_D \stackrel{\sim}{\longrightarrow} \Omega^{\ge p}. $$
For $p \gt 0$ there are canonical [[quasi-isomorphisms]]
  $$ \begin{aligned}
    A(p)_D &\stackrel{\sim}{\longrightarrow} (A(p) \to \mathcal{O} \to \Omega^1 \to \cdots \to \Omega^{p-1}) & (\ast) \\
    &\stackrel{\sim}{\longrightarrow} (0 \to \mathcal{O}/A(p) \to \Omega^1 \to \cdots \to \Omega^{p-1}) & 
  \end{aligned} $$
=--

#### Multiplicative structure

+-- {: .num_prop}
###### Proposition
There exists a canonical morphism in $D^+(An)$
  $$ - \cup - : A(i)_D \otimes^L A(j)_D \longrightarrow A(i+j)_D $$
inducing the structure of a [[graded commutative ring]] on $H^*_D(X, A(p))$ for all $X \in An$.
=--

+-- {: .proof}
###### Proof
Beilinson gives an explicit formula using the usual explicit model for the [[mapping cone]].
He also remarks shortly that the product can be defined by observing that the obvious multiplicative structures on $\Omega^\bullet$, $\Omega^{\ge *}$, $A(*)$, turn each into a [[monoid object]] in the [[symmetric monoidal category]] of [[cochain complexes]] (of [[abelian sheaves]]), that is, into [[dg-algebras]] (of complexes of sheaves).
Consider then the [[homotopy pullback]] of the diagram $A(*) \to \Omega \leftarrow \Omega^{\ge *}$; Beilinson claims that this is a [[dg-algebra]] whose underlying complex has in degree $p$ the Deligne complex $A(p)_D$ of weight $p$.
This point is expanded on in [Hopkins-Quick](#HopkinsQuick).

Here we will simply give a formula for the quasi-isomorphic complex $(*)$ of Lemma 1, which we will denote for the moment by $A(p)_E$.
For $x \in A(p)_E$, $y \in A(q)_E$, define

  $$ x \cup y = \begin{cases} x \cdot y & \deg(x) = 0 \text{ or } \deg(y) = 0 \\ x \wedge (-dy) & \deg(x) \gt 0 \text{ and } \deg(y) = q \gt 0 \\ 0 & \text{otherwise} \end{cases} $$

We omit the various verifications, that this defines a morphism of complexes, is associative, commutative, etc.  Hence one gets a [[dg-algebra]] in the category of cochain complexes of [[abelian sheaves]].  It only remains to see that $R\Gamma(X, -)$ preserves [[dg-algebras]], so that one gets the structure of a [[graded commutative ring]] on the [[hypercohomology]] groups $H^*_D(X, A(p))$ for each $p \in \mathbf{Z}$.
=--

#### The Bloch regulator

#### Relative cohomology

#### Complexes with logarithmic singularities

#### Deligne cohomology for algebraic varieties

#### Chern classes of vector bundles

#### Homologies

#### Cycles

#### Hodge conjecture for Deligne cohomology

### Regulators

...

+-- {: .num_defn}
###### Definition

=--

+-- {: .num_defn}
###### Definition
=--

## References

* {#Beilinson85} [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861)) (reviewed in [Esnault-Viehweg 88](#EsnaultViehweg88))

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))
