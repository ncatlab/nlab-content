
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

**Tambara functors** are algebraic structures similar to [[Mackey functors]], but with multiplicative norm maps as well as additive transfer maps, and a rule governing their interaction. They were introduced by Tambara, as TNR-functors, to encode the relationship between Trace (additive transfer), Norm (multiplicative transfer) and Restriction maps in the representation theory and cohomology theory of finite groups ([Tam93](#Tam93)).

>In the $G$-equivariant context for a finite group $G$, the role of abelian groups in non-equivariant algebra is played by Mackey functors. The category of Mackey functors is a closed symmetric monoidal category with symmetric monoidal product, the box product. In addition to the expected generalization of commutative rings to simply commutative monoids for the box product, there is a poset of generalizations of the notion of commutative rings to the $G$-equivariant context: the incomplete Tambara functors. These interpolate between [[Green functors]], the ordinary commutative monoids for the box product, and Tambara functors. The distinguishing feature for [incomplete] Tambara functors is the presence of certain multiplicative transfer maps, called norm maps. For a [[Green functor]], we have no norm maps; for a Tambara functor, we have norm maps for any pair of subgroups $H \subset K$ of $G$. ([Hill 17](#Hill17))

>A Mackey functor is represented by a "$G$-equivariant Eilenberg&#8211;MacLane spectrum", ... a Tambara functor is represented by a commutative "$G$-equivariant Eilenberg-MacLane ring spectrum" ([AB15](#AB15))


## Definition
### In parts
Given a sequence of maps of finite $G$-sets $X \xrightarrow{g} Y \xrightarrow{h} Z$, we define **distributor** diagram
\[
  \Delta(g,h) = \left( X \xleftarrow{p} A \xrightarrow{q} B \xrightarrow{r} Z \right)
\]
by setting 
\[
  B \coloneqq \left\{ (z,s) \mid z \in Z, s\colon h^{-1}(z) \rightarrow X, \text{ s.t. } gs = \mathrm{id}_{h^{-1}(z)} \right\}
\]
\[
  A \coloneqq Y \times_Z B
\]
and setting $p(y,s) = s(y)$, $q(y,s) = (h(y),s)$, and $r(z,s) = z$.

\begin{definition}
  A **semi-Tambara functor** for the group $G$ is the data of 
  
* a $G$-coefficient system of sets $R$ and

* two $G$-semi-Mackey functors $(R,T)$ and $(R,N)$ with coefficient system $R$,

subject to the distributivity condition that, for all distributors $\Delta(f,g) = (X \xleftarrow{p} A \xrightarrow{q} A \xrightarrow{r} Z)$, we have
\[
  N_g T_f = T_r N_q R_p.
\]
A semi-Tambara functor is a **Tambara functor** if $(R,T)$ is a [[Mackey functor]].
\end{definition}
We often refer to the maps $R_f$ as *restrictions*, $T_f$ as *transfers*, and $N_f$ as *norms*.

### Categorically
We define a 2-category to have

* objects: finite $G$ sets

* morphisms: _bispan_ diagrams $I \xleftarrow{p} X \xrightarrow{f} Y \xrightarrow{q} J$ in finite $G$-sets

* 2-cells: isomorphisms of bispan diagrams
\begin{tikzcd}[ampersand replacement=\&]
	\& X \& Y \\
	I \&\&\& J \\
	\& {X'} \& {Y'}
	\arrow[from=1-2, to=1-3]
	\arrow[from=1-2, to=2-1]
	\arrow["\sim"{description}, from=1-2, to=3-2]
	\arrow[from=1-3, to=2-4]
	\arrow["\sim"{description}, from=1-3, to=3-3]
	\arrow[from=3-2, to=2-1]
	\arrow[from=3-2, to=3-3]
	\arrow[from=3-3, to=2-4]
\end{tikzcd}

The identity morphisms and 2-cells are as one would expect, and composition is defined by the outer bispan diagram
\begin{tikzcd}[ampersand replacement=\&]
	\&\&\& \textcolor{rgb,255:red,199;green,3;blue,0}{W \times_{X \times_J Y}Y \times_Z B} \& \textcolor{rgb,255:red,0;green,23;blue,235}{Y \times_Z B} \& \textcolor{rgb,255:red,199;green,3;blue,0}{B} \\
	\&\& {W \times_J Y} \& \textcolor{rgb,255:red,0;green,23;blue,235}{X \times_J Y} \\
	\& W \& X \&\& \textcolor{rgb,255:red,0;green,23;blue,235}{Y} \& \textcolor{rgb,255:red,0;green,23;blue,235}{Z} \\
	\textcolor{rgb,255:red,199;green,3;blue,0}{I} \&\&\& J \&\&\& \textcolor{rgb,255:red,199;green,3;blue,0}{K}
	\arrow[from=1-4, to=1-5]
	\arrow["\psi", color={rgb,255:red,199;green,3;blue,0}, bend left, from=1-4, to=1-6]
	\arrow[from=1-4, to=2-3]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=-45}, draw=none, from=1-4, to=2-4]
	\arrow["\varphi"', color={rgb,255:red,199;green,3;blue,0}, bend right, from=1-4, to=4-1]
	\arrow["q"{description}, color={rgb,255:red,0;green,23;blue,235}, from=1-5, to=1-6]
	\arrow["p"{description}, color={rgb,255:red,0;green,23;blue,235}, from=1-5, to=2-4]
	\arrow[color={rgb,255:red,0;green,23;blue,235}, from=1-5, to=3-5]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=1-5, to=3-6]
	\arrow["r"{description}, color={rgb,255:red,0;green,23;blue,235}, from=1-6, to=3-6]
	\arrow["\rho", color={rgb,255:red,199;green,3;blue,0}, from=1-6, to=4-7]
	\arrow[from=2-3, to=2-4]
	\arrow[from=2-3, to=3-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=-45}, draw=none, from=2-3, to=3-3]
	\arrow[from=2-4, to=3-3]
	\arrow["g", color={rgb,255:red,0;green,23;blue,235}, from=2-4, to=3-5]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=-45}, draw=none, from=2-4, to=4-4]
	\arrow[from=3-2, to=3-3]
	\arrow[from=3-2, to=4-1]
	\arrow[from=3-3, to=4-4]
	\arrow["f", color={rgb,255:red,0;green,23;blue,235}, from=3-5, to=3-6]
	\arrow[from=3-5, to=4-4]
	\arrow[from=3-6, to=4-7]
\end{tikzcd}

whose blue inner diagram is defined by the distributor 
\[
  \Delta(g,f) = \left( X \times_J Y \xleftarrow{p} Y \times_Z B \xrightarrow{q} B \xrightarrow{r} Z \right).
\]

\begin{definition}
  Let $\mathcal{C}$ by an [[∞-category]] admitting finite products.
  Then, a **$G$-semi-Tambara functor** valued in $\mathcal{C}$ is a product preserving functor $\mathrm{Bispan}(\mathbb{F}_G) \rightarrow \mathcal{C}$.
  A $G$-semi-Tambara functor is a **Tambara functor** if its underlying additive semi-Mackey functor is a Mackey functor.
\end{definition}

In this formalism, given a semi-Tambara functor $X$, restriction $R_K^H\colon X(H) \rightarrow X(K)$ is implemented by functoriality under the bispan 
\[
  G/H \leftarrow G/K = G/K = G/K,
\]
norms by 
\[
  G/K = G/K \rightarrow G/H = G/H,
\]
and transfers by
\[
  G/K = G/K = G/K \rightarrow G/H.
\]

## Examples

(under construction...)

Burnside rings, representation rings, zeroth stable homotopy group of a genuine equivariant $E_{\infty}$-ring.

>the homotopy category of Eilenberg MacLane commutative ring spectra is equivalent to the category of Tambara functors. ([Ull13](#Ull13))

Some other examples are related to [[Witt-Burnside functors]], Witt rings in the sense of Dress and Siebeneicher.

### Additive completion of semi-Tambara functors

The following is Proposition 13.23 of [Strickland 12](Strickland12).

\begin{proposition}
  The [additive completion of semi-Mackey functors](https://ncatlab.org/nlab/show/Mackey+functor#AdditiveCompletion) underlies a left adjoint $\mathrm{sTamb}(\mathcal{C}) \rightarrow \mathrm{Tamb}(\mathcal{C})$ to the forgetful functor.
\end{proposition} 

### The Borel construction
Given $S$ a [[semiring]] with $G$-action through homomorphisms, we have a coefficient system $S^{\bullet}$ whose $[G/H]$-value is the invariants $S^H$.
We give this the additional structure of a _semi-mackey functor_ by first using the semiring isomorphism
\[
  S^H \simeq \mathrm{Hom}^G(G/H,S)
\]
under the pointwise semiring structure, then given a map of transitive $G$-sets $r\colon G/K \rightarrow G/H$, writing
\[
  T_K^H(f)(x) = \sum_{r(y) = x}  f(y).
\]
We then give this the structure of a _Tambara functor_ along $q\colon G/K \rightarrow G/H$ by the formula
\[
  N_K^H(f)(x) = \prod_{q(y) = x}  f(y)
\]
In particular, we may view $T_K^H$ as being defined by a "left Kan extension" formula and $N_K^H$ via "right Kan extension."

Note that restricting to the value on $G/e$ yields a functor $U\colon \mathrm{sTamb}_{G}(\mathcal{C}) \rightarrow \mathrm{sRing}_{G}(\mathcal{C})$.
The following is Example 6.3 of [Strickland 12]{#Strickland12}

\begin{proposition}
  The Borel construction is right adjoint to $U\colon \mathrm{sTamb}_{G}(\mathcal{C}) \rightarrow \mathrm{sRing}_{G}(\mathcal{C})$.
\end{proposition}

### Representation Tambara functors
Given $H \subset G$ a subgroup, note that (isomorphism classes of) $H$-representations correspond with $G$-equivariant vector bundles over $[G/H]$:
\[
  \mathrm{Vect}_k^{G}([G/H]) \simeq \mathrm{Rep}^H.
\]
Restriction gives these the structure of a coefficient system;
we may give these a semiring structure under $(\oplus,\otimes)$.
Moreover, we lift this to a semi-Tambara structure
with transfers given by induction
\[ 
  T_K^H(V)_x \simeq \bigoplus_{r(y) = x} V_y 
\]
and norms given by tensor-induction
\[ 
  N_K^H(V)_x \simeq \bigotimes_{q(y) = x} V_y. 
\]
The **Representation Tambara functor** is the additive completion of this.

### Burnside Tambara functors
Let $\mathcal{A}(S)$ be the [[Grothendieck group]] 
\[
  \mathcal{A}(S) \coloneqq K_0 \left((\mathbb{F}_G)_{/S} \right).
\]
This becomes a [[coefficient system]] under precomposition.
Moreover, colimits in $\mathbb{F}_G$ are universal, so precomposition along a map of finite $G$-sets $S \rightarrow T$ possesses a both a left and right adjoint;
the left adjoint to $[G/K] \rightarrow [G/H]$ is called *induction* and the right adjoint is called *coinduction*.
The **Burnside Tambara functor** has coefficient system $\mathcal{A}(-)$, transfers given by induction, and norms given by coinduction.

### An explicit example 
Let $G = C_2 = \{ e, \sigma \}$.
Then, a *C_2*-Mackey functor consists of the data

* an Abelian group $X$ with $C_2$-action,
* an Abelian group $Y$,
* a $C_2$-equivariant restriction homomorphism $R\colon Y \rightarrow X$ (under trivial action on $Y$), and 
* a $C_2$-equivariant transfer homomorphism $T\colon X \rightarrow Y$,

subject to the *double coset formula*

\[
  RT(a) = a + \sigma a.
\]

Thus, a $C_2$-Tambara functor consists of 
* a semiring $X$ with $C_2$-action,
* a semiring  $Y$,
* a $C_2$-equivariant semiring homomorphism $R\colon Y \rightarrow X$ (under trivial action on $Y$), 
* a $C_2$-equivariant additive map $T\colon X \rightarrow Y$, and
* a $C_2$-equivariant multiplicative map $N\colon X \rightarrow Y$,

subject to the double coset formulas

* $RT(a) = a + \sigma a$
 
* $RN(a) = a \cdot \sigma a$

and the distributivity formula

* $T(a R(b)) = T(a) b.$

We may explicitly define a $C_2$-Tambara funcgtor by underlying coefficient system semiring $X = \mathbb{Z}[\alpha] / \alpha^2$, $Y = \mathbb{Z}[\beta, \gamma] / (\beta^2, \beta \gamma, \gamma^2, 2\gamma)$, under trivial $C_2$-action and restriction map
\[
  R(i  + j\beta + k\gamma) = i + 2j\alpha.
\]
We may give this a Tambara structure by transfer
\[
  T(i + j\alpha) = 2i + j\beta
\]
and norm
\[
  N(i + j\alpha) = i^2 + ij\beta + j^2 \gamma.
\]

## Related concepts

* [[Mackey functor]]
* [[polynomial functor]]
* [[Witt vectors]]
* [[N-∞ operad]]

##References

Originally,

* {#Tam93} [[Daisuke Tambara]], _On multiplicative transfer_, Comm. Algebra 21 (1993), no. 4, 1393&#8211;1420 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/tambara.pdf)).

Other references in homotopy theory,

* {#Strickland12} [[Neil Strickland]], _Tambara Functors_, [arXiv:1205.2516](http://arxiv.org/abs/1205.2516)

* [[Michael Hill]], _Derived Equivariant Algebraic Geometry_, ([lecture and notes](https://www.msri.org/workshops/689/schedules/18236))
* Kristen Mazur, _On the Structure of Mackey Functors and Tambara Functors_, ([thesis](http://sites.lafayette.edu/mazurk/files/2013/07/Mazur-Thesis-4292013.pdf))

* {#Ull13} [[John Ullman]], _Tambara Functors and Commutative Ring Spectra_, ([arXiv:1304.4912](http://arxiv.org/abs/1304.4912))

* {#Hill17} [[Michael Hill]], _On the Andre-Quillen homology of Tambara functors_, ([arXiv:1701.06219](https://arxiv.org/abs/1701.06219))

On variations of Tambara functors,

* {#AB15} [[Vigleik Angeltveit]] and [[Anna Marie Bohmann]], _Graded Tambara Functors_, ([arXiv:1504.00668](http://arxiv.org/abs/1504.00668))

* [[Michael Hill]], [[Andrew Blumberg]], _Incomplete Tambara functors_, ([arXiv:1603.03292](https://arxiv.org/abs/1603.03292))

* [[Michael Hill]], [[Andrew Blumberg]], _The right adjoint to the equivariant operadic forgetful functor on incomplete Tambara functors_, ([arXiv:1711.11246](https://arxiv.org/abs/1711.11246))

* [[Michael Hill]], [[Andrew Blumberg]], _Bi-incomplete Tambara functors_, ([arXiv:2104.10521](https://arxiv.org/abs/2104.10521))

* [[Michael Hill]], [[David Mehrle]], [[J.D. Quigley]]: *Free incomplete Tambara functors are almost never flat*, International Mathematics Research Notices **2023** 5 (2023)  &lbrack;[arXiv:2105.11513](https://arxiv.org/abs/2105.11513), [doi:10.1093/imrn/rnab361](https://doi.org/10.1093/imrn/rnab361)&rbrack;

* [[David Chan]], _Bi-incomplete Tambara functors as O-commutative monoids_, ([arXiv:2208.05555](https://arxiv.org/abs/2208.05555))

* [[Ben Spitz]], _Norms of Generalized Mackey and Tambara Functors_, ([arXiv:2409.13131](https://arxiv.org/abs/2409.13131))

* [[Ross Street]], _Objective Mackey and Tambara functors via parametrized categories_ &lbrack;[arXiv:2503.02260](https://arxiv.org/abs/2503.02260)&rbrack;


[[!redirects Tambara functors]]


Relationship with [[Witt vectors]],

* [[Morten Brun]], _Witt vectors and Tambara functors_, ([arXiv:math/0304495](http://arxiv.org/abs/math/0304495)),

* [[Hiroyuki Nakaoka]], _Tambarization of a Mackey functor and its application to the Witt-Burnside construction_, ([arXiv:1010.0812](https://arxiv.org/abs/1010.0812))

In algebra,

* [[Hiroyuki Nakaoka]], _A generalization of The Dress construction for a Tambara functor, and polynomial Tambara functors_, ([arXiv:1012.1911](https://arxiv.org/abs/1012.1911))

* [[Hiroyuki Nakaoka]], _Ideals of Tambara functors_ ([arXiv:1101.5982](https://arxiv.org/abs/1101.5982)),

* [[Hiroyuki Nakaoka]], _On the fractions of semi-Mackey and Tambara functors_ ([arXiv:1103.3991](https://arxiv.org/abs/1103.3991)),

* [[Hiroyuki Nakaoka]], _Biset transformations of Tambara functors_ ([arXiv:1105.0714](https://arxiv.org/abs/1105.0714)),

* [[Hiroyuki Nakaoka]], _Spectrum of the Burnside Tambara functor on a cyclic $p$-group_ ([arXiv:1301.1453](https://arxiv.org/abs/1301.1453)).

* Maxine Calle, Sam Ginnett, _The Spectrum of the Burnside Tambara Functor of a Cyclic Group_, ([arXiv:2011.04729](https://arxiv.org/abs/2011.04729))

* Noah Wisdom, _A classification of $C_{p^n}$-Tambara fields_, ([arXiv:2409.02966](https://arxiv.org/abs/2409.02966))

* [[David Chan]], [[David Mehrle]], [[J.D. Quigley]], [[Ben Spitz]], [[Danika Van Niel]], _On the Tambara Affine Line_ ([arXiv:2410.23052](https://arxiv.org/abs/2410.23052))

In derived algebra,

* [[David Mehrle]], [[J.D. Quigley]], [[Michael Stahlhauer]]: _Koszul Resolutions over Free Incomplete Tambara Functors for Cyclic $p$-Groups_ &lbrack;[arXiv:2407.18382](https://arxiv.org/abs/2407.18382)&rbrack;

* [[David Mehrle]], [[J.D. Quigley]], [[Michael Stahlhauer]], _Pathological Computations of Mackey Functor-valued $Tor$ over Cyclic Groups_ &lbrack;[arXiv:2410.11974](https://arxiv.org/abs/2410.11974)&rbrack;

In [[higher algebra]],

* [[Elden Elmanto]], [[Rune Haugseng]], _On distributivity in higher algebra I: The universal property of bispans_, ([arXiv:2010.15722](https://arxiv.org/abs/2010.15722))

* [[Bastiaan Cnossen]], [[Rune Haugseng]], [[Tobias Lenz]], [[Sil Linskens]], _Normed equivariant ring spectra and higher Tambara functors_, ([arXiv:2407.08399](https://arxiv.org/abs/2407.08399))

[[!redirects Tambara functors]]