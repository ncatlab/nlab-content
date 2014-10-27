#Contents#
* table of contents
{:toc}

This page is a review of the seminal article

* [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861))

introducing [[Beilinson-Deligne cohomology]], [[Beilinson regulators]], [[higher regulators]], and the [[Beilinson conjectures]].

Please note that it is currently in a very preliminary state.

## Overview

### Notation

By [[analytic space]] we will mean [[real analytic space]].
Let $An$ denote the real [[analytic site]].
Consider the category $Ab(Sh(An))$ of [[abelian sheaves]] on $An$.
Beilinson denotes by $D^+(An)$ its bounded above [[derived category]], i.e. the category of [[connective]] [[cochain complexes]] up to [[quasi-isomorphism]].
Given an analytic space $X \in An$, we will also consider its [[petit topos]] $X^\sim$ of sheaves on the site $Ouv(X)$ of open subsets.

In $D^+(An)$ we have the complex $\Omega^\bullet$, of [[de Rham complex]]es of [[holomorphic forms]].  Let $\Omega^{\ge i}$ denote the "stupid" [[filtration]].

Fix a subring $A \subset \mathbf{R}$ and let $A(p) = A \cdot (2\pi i)^p \subset \mathbf{C}$ for $p \in \mathbf{Z}$.  We will abuse notation and write $\mathbf{C} \in D^+(An)$ also for the constant sheaf valued in the complex concentrated in degree zero.  Similarly we will view $A(p)$ as an object of $D^+(An)$.

We will write $H^*_B(X, \mathbf{C})$ for the [[Betti cohomology]] of $X \in An$.

### Main constructions and conjectures

#### Deligne cohomology of analytic spaces

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
inducing the structure of a [[graded commutative ring]] on
  $$ H^*_D(X, A(*)) = \bigoplus_{p,q} H^p_D(X, A(p)) $$
for all $X \in An$.
=--

+-- {: .proof}
###### Proof
Beilinson gives an explicit formula using the usual explicit model for the [[mapping cone]].
He also remarks shortly that the product can be defined by observing that the obvious multiplicative structures on $\Omega^\bullet$, $\Omega^{\ge *}$, $A(*)$, turn each into a [[monoid object]] in the [[symmetric monoidal category]] of [[cochain complexes]] (of [[abelian sheaves]]), that is, into [[dg-algebras]] (of complexes of sheaves).
Consider then the [[homotopy pullback]] of the diagram $A(*) \to \Omega \leftarrow \Omega^{\ge *}$; Beilinson claims that the underlying complex of this [[dg-algebra]] has in each degree $p$ the Deligne complex $A(p)_D$ of weight $p$.
This point is expanded on in [Hopkins-Quick](#HopkinsQuick).

Here we will simply give a formula for the quasi-isomorphic complex $(*)$ of Lemma 1 (assuming $i,j \gt 0$), which we will denote for the moment by $A(i)_E$.
For $X \in An$, take $x \in \Gamma(X, A(i)_E)$, $y \in \Gamma(X, A(j)_E)$, and define

  $$ x \cup y = \begin{cases}
    x \cdot y & \deg(x) = 0\quad\text{or}\quad\deg(y) = 0 \\
    x \wedge dy & \deg(x) \gt 0\quad\text{and}\quad\deg(y) = j \gt 0 \\
    0 & \text{otherwise}
  \end{cases} $$

We omit the various verifications, that this defines a morphism of complexes, is associative, commutative, etc.
One gets a [[monoid object]] in the category of cochain complexes of [[abelian sheaves]].  It only remains to see that $R\Gamma(X, -)$ preserves monoids, so that one gets the structure of a graded commutative ring on the [[hypercohomology]] groups $H^*_D(X, A(*))$.
=--

#### The Bloch regulator

Beilinson uses this cup product for $i=j=1$ to recover the [[Bloch regulator]].

+-- {: .num_theorem}
###### Theorem
**(Bloch)**.  For each [[algebraic curve]] $X$ over $\mathbf{R}$, there is a canonical functorial homomorphism
  $$ r_X : K_2(X) \to H^1_B(X, \mathbf{C}^*) $$
from the second [[algebraic K-theory]] group to the first [[Betti cohomology]] group with coefficients in $\mathbf{C}^*$.
=--

+-- {: .proof}
###### Sketch of proof
By Lemma 1, there are quasi-isomorphisms
  $$ \mathbf{Z}(1)_D \stackrel{\sim}{\to} \mathcal{O}^*[-1] $$
induced by the [[exponential map]], and
  $$ \mathbf{Z}(2)_D \stackrel{\sim}{\to} (\mathcal{O}^* \stackrel{d \log}{\to} \Omega^1)[-1] $$
induced by $x \mapsto \exp(x/2\pi i)$.
It follows that the cup product
  $$ \cup : H^1_D(X, \mathbf{Z}(1)) \otimes H^1_D(X, \mathbf{Z}(1)) \longrightarrow H^2_D(X, \mathbf{Z}(2)) $$
corresponds to a canonical homomorphism
  $$ \mathcal{O}^*(X) \otimes \mathcal{O}^*(X) \to H^1(X, \mathcal{O}^* \to \Omega^1). $$
According to Deligne, the RHS classifies isomorphism classes of [[line bundles]] with [[holomorphic connection]].
Since $\dim(X) = 1$, all [[connections]] are [[integrable connection|integrable]] and this group is identified with $H^1_B(X, \mathbf{C}^*)$.

Now by Matsumoto's theorem, giving a presentation of the $K_2$ group of a [[field]] by two generators and certain relations, one has
  $$ K_2(\mathcal{O}(X)) = (\mathcal{O}(X)^* \otimes \mathcal{O}(X)^*)/\lt t \otimes (1-t) \gt_{t \ne 0,1}. $$
On the other hand, one has the Steinberg identity $t \cup (1-t) = 0$ for $t \in \mathcal{O}^*(X)$.
It follows that the homomorphism above factors through $K_2(\mathcal{O}(X)) = K_2(\eta)$ for $\eta$ a generic point.
To extend it to all of $X$, one uses the commutative diagram of localization [[exact sequences]]
  $$ \begin{array}{ccccc}
    K_2(X) & \longrightarrow & K_2(\eta) & \longrightarrow & \oplus_{x \in X(\mathbf{C})} \mathbf{C}^* \\
    \downarrow & & \downarrow & & \downarrow \\
    H^1_B(X, \mathbf{C}) & \longrightarrow & H^1(\eta, \mathbf{C}^*) & \longrightarrow & \oplus_{x \in X(\mathbf{C})} \mathbf{C}^*
  \end{array} $$
The first row comes from the [[Gersten-Quillen resolution]] for K-theory.
=--

#### Relative cohomology

If $S$ and $T$ are [[toposes]] and $u^* : S \rightleftarrows T : u_*$ is a [[geometric morphism]], consider the [[Artin gluing]], i.e. the [[topos]] $(id_S/u_*) = (u^*/id_T)$ whose objects are morphisms $u^*(F) \to G$ for $F \in S$, $G \in T$, and morphisms are commutative diagrams.
Write $(S, T)$ for this topos.

+-- {: .num_defn}
###### Definition
The functor of [[global sections]] on $(S, T)$ is the [[left exact functor]]
  $$ \Gamma(S, T, -) : Ch^+(Ab(S, T)) \longrightarrow Ch^+(Ab) $$
defined by
  $$ \Gamma(S, T, F) = Cone(\Gamma(T, F_T) \to \Gamma(S, F_S))[-1] $$
for each sheaf $F \in (S, T)$ given by $u^*(F_S) \to F_T$ with $F_S \in S$ and $F_T \in T$.
Let $R\Gamma(S, T, -) : D^+(Ab(S, T)) \to D^+(Ab)$ denote its [[right derived functor]].
=--

The rest of this section is just defining a [[monoidal product]] on $Ch^+(Ab((S, T)))$, and explaining that a [[monoid]] in $D^+(Ab((S,T)))$ will induce a [[monoid]] in $D^+(Ab)$, i.e. a [[dg-algebra]], after taking [[cohomology]].

#### Complexes with logarithmic singularities

Let $\Pi$ denote the category of pairs $(X, \overline{X})$ with $\overline{X} \in An$ [[smooth manifold|smooth]] and $j : X \hookrightarrow \overline{X}$ an [[open subspace]] such that the complement $\overline{X} - X$ is a [[normal crossing divisor]].
The [[open immersion]] $j$ induces a functor $\Ouv(X) \to \Ouv(\overline{X})$ on the [[petit sites]] by mapping an open subspace $U \subset X$ to $U \subset X \subset \overline{X}$.
This induces a [[geometric morphism]] $j^* : \overline{X}^{\sim} \rightleftarrows X^{\sim} : j_*$ on the [[petit toposes]].
Following the discussion of the previous section, we make the

+-- {: .num_defn}
###### Definition
The **topos of the pair** $(X, \overline{X})$ is defined to be the [[Artin gluing]] $(j^*/id)$, and will be denoted $(X, \overline{X})^{\sim}$.
Hence a **sheaf on the pair** $(X, \overline{X})$ is a sheaf $F$ on $X$, a sheaf $G$ on $\overline{X}$, and a connecting morphism $j^*(G) \to F$.
=--

Let $\Omega^\bullet_{X,\overline{X}} \in \Ch^+(Ab((X, \overline{X})^{\sim}))$ denote the [[de Rham complex]] of [[holomorphic forms]] on $C$ with [[logarithmic singularities]] along $\overline{X} - X$.
That is, $\Omega^\bullet_{X,\overline{X}}$ is an object of $Ch^+(Ab(\overline{X}^\sim))$ and we view it as a complex on $(X, \overline{X})^\sim$ by taking the part on $X^\sim$ to be trivial.
Let $\Omega^{\ge p}_{X, \overline{X}}$ denote the stupid [[filtration]].

Now we define a complex of abelian sheaves $A(p)_D$ in $Ch^+(Ab((X, \overline{X})^{\sim}))$ as follows.

+-- {: .num_defn}
###### Definition
The **Beilinson-Deligne complex with logarithmic singularities** of weight $p$ of the pair $(X, \overline{X})$ is a complex of abelian sheaves on $(X, \overline{X})^\sim$, denoted $A(p)_D \in Ch^+(Ab((X, \overline{X})^\sim))$ and defined as follows.
In degree $n \in \mathbf{Z}$, take the sheaf
  $$ A(p)_{D,X} = Cone^n(A(p) \to \Omega^\bullet_X) $$
in $X^\sim$ (where the [[mapping cone]] is taken in $Ch^+(Ab(X^\sim))$), and the sheaf
  $$ A(p)_{D,\overline{X}} = \Omega^{\ge p}_{X, \overline{X}} $$
in $\overline{X}^\sim$, together with the connecting morphism induced by the inclusion $j^*(\Omega^{\ge p}) \hookrightarrow \Omega^\bullet_X$.
=--

+-- {: .num_defn}
###### Definition
The **Beilinson-Deligne cohomology with logarithmic singularities** of the pair $(X, \overline{X})$ in weight $p$ and degree $q$ and with coefficients in $A$, is the [[hypercohomology]]
  $$ H^q_D(X, \overline{X}, A(p)) = H^q R\Gamma((X, \overline{X})^\sim, A(p)_D). $$
=--

One defines a cup product on these complexes in the same way as above, and gets a graded commutative ring structure on Beilinson-Deligne cohomology with logarithmic singularities.

+-- {: .num_defn}
###### Definition

=--

#### Deligne cohomology for algebraic varieties

Let $\Pi' \subset \Pi$ denote the full subcategory spanned by pairs $(X, \overline{X})$ for which $\overline{X}$ is a [[smooth variety|smooth]] [[projective variety|projective]] [[algebraic variety]].
Let $Sch = Sch_\mathbf{R}$ denote the category of [[smooth variety|smooth]] [[quasi-projective variety|quasi-projective]] [[schemes]] over $\mathbf{R}$.
By the [[GAGA]] principle, we have a functor $\sigma : \Pi' \to Sch$ which sends a pair $(X, \overline{X})$ to $X$.
Conversely given $X \in Sch$, by [[Hironaka]] there exists a pair $(X, \overline{X}) \in \Pi'$ (a compactification).

+-- {: .num_defn}
###### Definition
Let $X \in Sch$ be a smooth quasi-projective algebraic variety over $\mathbf{R}$.
Let $(X, \overline{X}) \in \Pi'$ be a compactification and define the **Beilinson-Deligne cohomology** of $X$ as
  $$ H_D^q(X, A(p)) = H^q R\Gamma(\overline{X}, X, A(p)_D) $$
and
  $$ H_B^q(X, A(p)) = H^q R\Gamma(X, A(p)). $$
=--

One shows that these definitions are independent of the chosen compactification.
By the above, one gets a [[cup product]] also on these cohomology groups.

Next Beilinson shows that $H_D$ can be defined as cohomologies of certain complexes of [[Zariski topology|Zariski sheaves]].
He notes that this is not necessary for the remainder of the paper, so we omit this here.

#### Chern classes of vector bundles

There is a canonical morphism
  $$ c_1 : R\Gamma(X, \mathcal{O}^*)[-1] \longrightarrow H_D(X, A(1)) $$
for each $X \in \Sch$.
This induces a canonical homomorphism
  $$ Pic(X) = H^1(X, \mathcal{O}^*) \longrightarrow H^2(X, A(1)) $$
from the [[Picard group]] of [[invertible sheaves]].

+-- {: .num_defn}
###### Definition
For an [[invertible sheaf]] $\mathcal{L}$ on $X$, its **first Chern class** is defined to be the image of the class of $\mathcal{L}$ under the above homomorphism.
=--

One can show that for $A = \mathbf{Z}$, this homomorphism is injective, and further surjective if $X$ is [[compact]].

Next Beilinson shows the [[projective bundle theorem]] for Beilinson-Deligne cohomology.

+-- {: .num_prop}
###### Proposition
**(Projective bundle theorem)**.
Let $E$ be an $n$-dimensional [[vector bundle]] on $X$, let $\pi : \mathbf{P}(E) \to X$ be the associated [[projective bundle]], and $\mathcal{O}(1)$ the [[tautological sheaf]] on $\mathbf{P}(E)$.
The homomorphism
  $$ \oplus c_1(\mathcal{O}(1))^j \cup \pi^*
       : \bigoplus_{0 \le j \le n-1} H_D(X, A(i-j))[2j]
       \longrightarrow H_D(\mathbf{P}(E), A(i)) $$
is invertible.
=--

+-- {: .proof}
###### Proof

=--

After the projective bundle theorem, one can define [[Chern classes]] of [[vector bundles]] following [[Grothendieck]].
In particular one gets the [[Chern character]]
  $$ ch : K_0(X) \longrightarrow \bigoplus_i H^{2i}(X, A \otimes \mathbf{Q}(i)). $$

#### Homologies

In this paragraph, Beilinson considers the [[homology theory]] dual to Deligne cohomology.
For a smooth [[analytic space]] $X$ let $\Omega^{p,q}_{X^\infty}$ denote the sheaf of $C^\infty$ $(p,q)$-forms, and let $\Omega'^{p,q}_{X^\infty}$ denote the sheaf of $(p,q)$-forms with [[distribution]] coefficients on $\Omega^{-p,-q}_{X^\infty}$.
These defines [[bicomplexes]] of [[abelian groups]], and we write $\Omega^\bullet_{X^\infty}$ and $\Omega'^\bullet_{X^\infty}$ for their [[totalizations]], respectively.
Let $\Omega^{\ge *}_{X^\infty}$ and $\Omega'^{\ge *}_{X^\infty}$ denote the respective "stupid" [[filtrations]] on each.
Of course, one has the structure of a [[monoid]] on $\Omega^\bullet_{X^\infty}$, making it a [[dg-algebra]].

+-- {: .num_lemma}
###### Lemma
In the [[filtered derived category]] of [[abelian groups]] one has inclusions
  $$ (\Omega^\bullet_X, \Omega_X^{\ge *})
     \hookrightarrow (\Omega^\bullet_{X^\infty}, \Omega_{X^\infty}^{\ge *})
     \hookrightarrow (\Omega'^\bullet_{X^\infty}[-2\dim(X)], \Omega'_{X^\infty}^{\ge (*+\dim(X))}) $$
which compose to a [[filtered quasi-isomorphism]].
=--

We pass to the logarithmic singularity versions as follows.

+-- {: .num_defn}
###### Definition
Let $(X, \overline{X}) \in \Pi$ be a pair as above.
Define the complexes
  $$ \Omega^\bullet_{(X, \overline{X})^\infty} = \Omega^\bullet_{\overline{X}^\infty} \otimes_{\Omega^\bullet_{\overline{X}}} \Omega^\bullet_{(X, \overline{X})} $$
and
  $$ \Omega'^\bullet_{(X, \overline{X})^\infty} = \Omega'^\bullet_{\overline{X}^\infty} \otimes_{\Omega^\bullet_{\overline{X}}} \Omega^\bullet_{(X, \overline{X})} $$
with filtrations
  $$ \Omega_{X^\infty}^{\ge *} = \Omega^{\ge *}_{\overline{X}^\infty} \otimes_{\Omega_{\overline{X}}} \Omega^\bullet_{(X, \overline{X})} $$
and
  $$ \Omega'_{X^\infty}^{\ge *} = \Omega'^{\ge *}_{\overline{X}^\infty} \otimes_{\Omega_{\overline{X}}} \Omega^\bullet_{(X, \overline{X})} $$
respectively.
=--


+-- {: .num_defn}
###### Definition
The complex of **relative singular chains** on $(X, \overline{X})$ is defined as the [[quotient chain complex]]
  $$ C'^\bullet(X, \overline{X}, A(i)) := C'^\bullet(\overline{X}, A(i))/C'^\bullet(\overline{X}-X, A(i)). $$
Define the complex
  $$ \Omega'^\bullet(X, \overline{X}) = \Gamma_c(\overline{X}, \Omega'^\bullet_{(X, \overline{X})^\infty}) $$
the complex of sections with [[compact support]], with the filtration
  $$ \Omega'^{\ge *}(X, \overline{X}) = \Gamma_c(\overline{X}, \Omega'^{\ge *}_{(X, \overline{X})^\infty}) $$
=--

+-- {: .num_defn}
###### Definition
=--

#### Cycles

#### Hodge conjecture for Deligne cohomology

### Regulators

...

## References

* {#Beilinson85} [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861)) (reviewed in [Esnault-Viehweg 88](#EsnaultViehweg88))

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))

* {#HopkinsQuick} [[Michael Hopkins]], [[Gereon Quick]], _Hodge filtered complex bordism_, [arXiv](http://arxiv.org/abs/1212.2173v3).