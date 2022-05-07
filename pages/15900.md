#Contents#
* table of contents
{:toc}

This page is supposed to be a review of the seminal article

* [[Alexander Beilinson]], 

  _Higher regulators and values of L-functions_, 

  Journal of Soviet Mathematics 30 (1985), 2036-2070, 

  ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861))

introducing [[Beilinson-Deligne cohomology]], [[Beilinson regulators]], [[higher regulators]], and the [[Beilinson conjectures]].

Please note that it is currently in a very preliminary state, having been prepared quickly as notes for a seminar talk on the first section of the paper.
It follows the paper very closely, and an interested reader might like to rewrite from the [[nPOV]].

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
Let $V = V_\mathbf{R}$ denote the category of [[smooth variety|smooth]] [[quasi-projective variety|quasi-projective]] [[schemes]] over $\mathbf{R}$.
By the [[GAGA]] principle, we have a functor $\sigma : \Pi' \to V$ which sends a pair $(X, \overline{X})$ to $X$.
Conversely given $X \in V$, by [[Hironaka]] there exists a pair $(X, \overline{X}) \in \Pi'$ (a compactification).

+-- {: .num_defn}
###### Definition
Let $X \in V$ be a smooth quasi-projective algebraic variety over $\mathbf{R}$.
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
for each $X \in V$.
This induces a canonical homomorphism
  $$ Pic(X) = H^1(X, \mathcal{O}^*) \longrightarrow H^2(X, A(1)) $$
from the [[Picard group]] of [[invertible sheaves]].

+-- {: .num_defn}
###### Definition
For an [[invertible sheaf]] $\mathcal{L}$ on $X$, its **first Chern class** is defined to be the image of the class of $\mathcal{L}$ under the above homomorphism.
=--

One can show that for $A = \mathbf{Z}$, this homomorphism is injective, and further surjective if $X$ is [[compact]].

Next Beilinson shows the [[projective bundle formula]] for Beilinson-Deligne cohomology.

+-- {: .num_prop}
###### Proposition
**(Projective bundle formula)**.
Let $E$ be an [[vector bundle]] of rank $r$ on $X$, let $\pi : \mathbf{P}(E) \to X$ be the associated [[projective bundle]], and $\mathcal{O}(1)$ the [[tautological sheaf]] on $\mathbf{P}(E)$.
The homomorphism
  $$ \oplus c_1(\mathcal{O}(1))^j \cup \pi^*
       : \bigoplus_{j=0}^{r-1} H_D(X, A(i-j))[2j]
       \longrightarrow H_D(\mathbf{P}(E), A(i)) $$
is invertible.
=--

+-- {: .proof}
###### Proof
By definition we have the distinguished triangle
  $$ H_B(X)[-1] \to R\Gamma(X, A(i))_D) \to R\Gamma(X, F^i) \oplus R\Gamma(X, A(i)) \to. $$
One checks that it is compatible with the cup product.
Since the morphism $A(i)_D \to A(i)$ sends first [[Chern classes]] in Deligne cohomology to first Chern classes in [[Betti cohomology]], the [[projective bundle formula]]s for [[Betti cohomology]] and [[de Rham cohomology]] show that the map in question induces an isomorphism on the leftmost and rightmost members of the triangle.
Hence the result follows.
=--

After the projective bundle theorem, one can define [[Chern classes]] of [[vector bundles]] following [[Grothendieck]].
In particular one gets the [[Chern character]]
  $$ ch : K_0(X) \longrightarrow \bigoplus_i H^{2i}(X, A \otimes \mathbf{Q}(i)). $$

+-- {: .num_lemma}
###### Lemma
For each $i$, there exists a unique assignment to a [[vector bundle]] $E$ over $X \in \mathcal{V}$ a class
  $$ c_i(E) \in H^{2i}_D(X, A(i)) $$
that is [[functorial]] with respect to [[inverse images]] and for which $A(i)_D \to A(i)$ sends $c_i(E)$ to the usual Chern class in [[Betti cohomology]].
=--

+-- {: .proof}
###### Proof
We omit the proof and just recall the construction due to Grothendieck of the Chern classes.
Let $r = rk(E)$ and write $P = \mathbf{P}(E)$.
By the projective bundle formula one has
  $$ H_D^{2r}(P, \mathbf{Z}(r)) = \bigoplus_{i=0}^{r-1} H^{2j+2r}_D(X, \mathbf{Z}(r-j)) $$
There exist $\gamma_i$ such that
  $$ \Sigma_{i=0}^r \pi^* \gamma_i \cup c_1(\mathcal{O}_P(1))^{r-i} = 0 $$
with $\gamma_i \in H_D^{2i}(X, \mathbf{Z}(i))$ and $\gamma_0 = 1$.
We define $c_i(E) = \gamma_i$.
=--

#### Homologies

In this paragraph, our goal is to define the [[homology theory]] dual to Deligne cohomology, for schemes over $\mathbf{R}$.
To do this, we first define functorial complexes on $\Pi_*$.
Then they extend, more or less formally, to the category of finite type schemes over $\mathbf{R}$ and [[proper maps]].
Then we establish [[Poincare duality]].

##### for smooth analytic spaces

+-- {: .num_defn}
###### Definition
Let $X \in An$ be smooth.
Let
  $$ \mathcal{A}^\bullet_X \qquad \text{(resp.} \quad \mathcal{D}^\bullet_X \text{)} $$
denote the complex of $C^\infty$ [[differential forms|forms]] (resp. with [[distribution]] coefficients on $\mathcal{A}^{-p,-q}_{X}$).
This is the [[totalization]] of the [[double complex]] $\mathcal{A}^{*,*}_X$ (resp. $\mathcal{D}^{*,*}_X$) formed by sheaves of $(p,q)$-forms (resp. with [[distribution]] coefficients).
Let $\mathcal{A}^{\ge *}_{X}$ and $\mathcal{D}^{\ge *}_{X}$ denote the respective induced [[filtrations]].

Let
  $$ C'^\bullet(X, A(p)) $$
denote the complex of $C^\infty$ [[singular chains]] with coefficents in the [[constant sheaf]] $A(p)$.

Let
  $$ \mathcal{D}^\bullet_X = \Gamma_c(X, \mathcal{D}_X) $$
denote the complex of [[global sections]] with [[compact support]].
(Here we view $\mathcal{D}_X$ as a sheaf on $X$.)
=--

##### for pairs (logarithmic singularity)

Let $\Pi_* \subset \Pi$ denote the subcategory with the same objects and only morphisms $f : (X, \overline{X}) \to (Y, \overline{Y})$ which satisfy $f(\overline{X} - X) \subset \overline{Y} - Y$.

+-- {: .num_defn}
###### Definition
Let $(X, \overline{X}) \in \Pi_*$.
Define the complexes
  $$ \mathcal{A}^\bullet_{(X, \overline{X})} = \mathcal{A}^\bullet_{\overline{X}} \otimes_{\Omega^\bullet_{\overline{X}}} \Omega^\bullet_{(X, \overline{X})} $$
and
  $$ \mathcal{D}^\bullet_{(X, \overline{X})} = \mathcal{D}^\bullet_{\overline{X}} \otimes_{\Omega^\bullet_{\overline{X}}} \Omega^\bullet_{(X, \overline{X})} $$
with the induced filtrations $\mathcal{A}^{\ge *}_{(X, \overline{X})}$ and $\mathcal{D}^{\ge *}_{(X, \overline{X})}$.

Define the complex of relative $C^\infty$ singular chains on $(X, \overline{X})$ as the [[quotient chain complex]]
  $$ C'^\bullet(X, \overline{X}, A(i)) := C'^\bullet(\overline{X}, A(i))/C'^\bullet(\overline{X}-X, A(i)). $$

Let
  $$ \mathcal{D}^\bullet(X, \overline{X}) = \Gamma_c(\overline{X}, \mathcal{D}^\bullet_{(X, \overline{X})}) $$
denote the complex of sections with [[compact support]], with the induced filtration $\mathcal{D}^{\ge *}(X, \overline{X})$.
=--

Finally, define the complex $C'_D(X, \overline{X}, A(p))$ (this is the complex that will give us the Deligne homology groups $H'_D^*(X, \overline{X}, A(p))$).

+-- {: .num_defn}
###### Definition
For $(X, \overline{X}) \in \Pi_*$, define the complex
  $$ C'_D(X, \overline{X}, A(p)) = Cone(\mathcal{D}^{\ge p}(X, \overline{X}) \oplus C'^\bullet(X, \overline{X}, A(i)) \longrightarrow \mathcal{D}^\bullet(X, \overline{X})). $$
=--

This is functorial on $\Pi_*$.

##### for schemes

Let $Sch_*$ denote the category of [[finite type]] schemes over $\mathbf{R}$ and [[proper maps]].
Let $V_* \subset Sch_*$ denote the subcategory of smooth quasi-projective schemes.
Let $\Pi'_* = \Pi' \cap \Pi_*$ denote the category of pairs $(X, \overline{X})$ with $\overline{X}$ smooth projective, $X \subset \overline{X}$ open with $\overline{X} - X$ a normal crossing divisor, and with morphisms $f : (X, \overline{X}) \to (Y, \overline{Y})$ such that $f(\overline{X} - X) \subset \overline{Y} - Y$.

+-- {: .num_lemma}
###### Lemma
The functor $C'^\bullet_D(-, A(p))$ on the category $\Pi'_*$ extends uniquely to a functor on $Sch_*$.
In particular one gets has a [[distinguished triangle]] in $D^+(A-mod)$
  $$ \longrightarrow H'_{dR}(X) \longrightarrow H'_D(X, A(p)) \longrightarrow F^i H'_{dR}(X) \oplus H'_B(X, A(p)) \longrightarrow, $$
where $H'_{dR}$ is [[de Rham homology]], $F^i$ is the [[Hodge filtration]], $H'_B$ is the [[Borel-Moore homology]] with coefficients in the [[constant sheaf]] $A(p)$, and $H'_D(X, A(p))$ is the [[Deligne homology]], defined by the complex $C'_D(X, A(p))$.
=--

+-- {: .num_lemma}
###### Lemma
**(Poincare duality).**
Let $X$ be a smooth scheme of dimension $n$.
There is a canonical isomorphism
  $$ H'_D(X, A(p)) = H_D(X, A(p+n))[2n]. $$
=--

+-- {: .proof}
###### Proof
Let $(X, \overline{X}) \in \Pi'_*$ be a compactification of $X$.
Consider the presheaf on $\overline{X}$ of complexes of abelian groups, defined by
  $$ U \mapsto C'(\overline{X}, A(p))/C'(\overline{X} - (X \cap U), A(p)). $$
Take its associated sheaf, and consider it as a complex of abelian sheaves, $\overline{C}'_{X, \overline{X}}(A(p))$.
First of all note that
  $$ \overline{C}'_{X, \overline{X}}(A(p)) = j_*j^* \overline{C}'_{X, \overline{X}}(A(p)) $$
where $j : X \hookrightarrow \overline{X}$ is the open immersion.
Note that $j^* \overline{C}'_{X, \overline{X}}(A(p))$ is a [[flasque resolution]] of the sheaf $A(p+n)[2n]$ on $X$.
Since the embedding
  $$ \Omega_{X, \overline{X}} \hookrightarrow \mathcal{D}_{X, \overline{X}}[-2n] $$
is a [[filtered quasi-isomorphism]], and the [[associated graded objects]] $gr^p \mathcal{D}_{X, \overline{X}}$ are [[soft sheaves]], one gets
  $$ R\Gamma(\Omega_{X, \overline{X}}, \Omega^{\ge p}_{X, \overline{X}}) = \Gamma(\overline{X}, (\mathcal{D}_{X, \overline{X}}, \mathcal{D}^{\ge p+n}_{X, \overline{X}}))[-2n] $$

=--


#### Cycles

Let $X$ be a scheme and $Y \in Z_n(X)$ an [[irreducible topological space|irreducible]] subscheme of dimension $n$.
Note that the canonical homomorphism
  $$ H'_D^{-2n}(Y, A(-n)) \longrightarrow H'_B^{-2n}(Y, A(-n)) = A $$
is invertible.
Let $cl_D(Y)$ denote the element of $H'_D^{-2n}(Y, A(-n))$ corresponding to the unit $1 \in A$.
Hence one gets a homomorphism
  $$ cl_D : Z_n(X) \longrightarrow H'_D^{-2n}(X, A(-n)) $$
given by $cl_D[Y] = i_*(\cl_D(Y))$.
If $X$ is smooth, by Poincare duality this corresponds to a homomorphism
  $$ cl_D : Z^n(X) \longrightarrow H_D^{2n}(X, A(n)) $$
on the group of [[algebraic cyles]] of [[codimension]] $n$.

+-- {: .num_lemma}
###### Lemma
If $X$ is smooth and compact, then for each $Y \in Z_n(X)$, if $cl_B(Y) \in H'_B^{-2n}(X, \mathbf{Z}(-n))$ is equal to 0, then $cl_D(Y)$ coincides with the Abel-Jacobi-Griffiths periods of the cycle $Y$.
=--

+-- {: .proof}
###### Proof
The distinguished triangle defining $\mathbf{Z}(n)_D$ induces, after passing to the associated [[long exact sequence]], a [[short exact sequence]]
  $$ 0 \to \mathcal{I}^n(X) \to H_D^{2n}(X, \mathbf{Z}(n)) \to Hdg^n(X) \to 0 $$
where $\mathcal{I}^n$ is the $n$th [[intermediate Jacobian]] of [[Griffiths]], defined as
  $$ \mathcal{I}^n = H^{2n-1}_B(X, \mathbf{C})/(H^{2n-1}_B(X, \mathbf{Z}(n)) \oplus F^n H^{2n-1}_B(X, \mathbf{C})) $$
and $\Hdn^n(X)$ is the group of integral [[Hodge cycles]] of type $(n, n)$.

Using the usual explicit model for the [[mapping cone]], $cl_D(Y)$ is the homology class of the cycle
  $$ (cl_F(Y), i_* cl_B(Y), 0) \in C'_D^{-2n}(X, \mathbf{Z}(-n)) $$
where $i : Y \hookrightarrow X$ denotes the closed immersion, and $cl_F(Y) \in F^{-n}\mathcal{D}^{-2n}(X)$ is a distribution defined by integration over $Y$.
Since $cl_B(Y) = 0$, we can choose $s \in C'^{-2n-1}(X, \mathbf{Z}(-n))$ such that $d(s) = i_*(cl_B(Y))$.
By subtracting from $cl_D(Y)$ the boundary $(0, s, 0)$, we see that $cl_D(Y) = (cl_F(Y), 0, s)$.
But the latter is precisely the definition of the periods of the cycle $Y$.
=--

#### Hodge conjecture for Deligne cohomology

### Regulators

+-- {: .num_lemma}
###### Lemma

=--
+-- {: .num_lemma}
###### Lemma

=--
...

## References

* {#Beilinson85} [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861)) (reviewed in [Esnault-Viehweg 88](#EsnaultViehweg88))

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))

* {#HopkinsQuick} [[Michael Hopkins]], [[Gereon Quick]], _Hodge filtered complex bordism_, [arXiv](http://arxiv.org/abs/1212.2173v3).