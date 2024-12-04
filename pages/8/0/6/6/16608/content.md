#Contents#
* table of contents
{:toc}

## Idea

**Tambara functors** are algebraic structures similar to [[Mackey functors]], but with multiplicative norm maps as well as additive transfer maps, and a rule governing their interaction. They were introduced by Tambara, as TNR-functors, to encode the relationship between Trace (additive transfer), Norm (multiplicative transfer) and Restriction maps in the representation theory and cohomology theory of finite groups ([Tam93](#Tam93)).

>In the $G$-equivariant context for a finite group $G$, the role of abelian groups in non-equivariant algebra is played by Mackey functors. The category of Mackey functors is a closed symmetric monoidal category with symmetric monoidal product, the box product. In addition to the expected generalization of commutative rings to simply commutative monoids for the box product, there is a poset of generalizations of the notion of commutative rings to the $G$-equivariant context: the incomplete Tambara functors. These interpolate between [[Green functors]], the ordinary commutative monoids for the box product, and Tambara functors. The distinguishing feature for [incomplete] Tambara functors is the presence of certain multiplicative transfer maps, called norm maps. For a [[Green functor]], we have no norm maps; for a Tambara functor, we have norm maps for any pair of subgroups $H \subset K$ of $G$. ([Hill 17](#Hill17))

>A Mackey functor is represented by a "$G$-equivariant Eilenberg&#8211;MacLane spectrum", ... a Tambara functor is represented by a commutative "$G$-equivariant Eilenberg-MacLane ring spectrum" ([AB15](#AB15))


## Examples

Burnside rings, representation rings, zeroth stable homotopy group of a genuine equivariant $E_{\infty}$-ring.

>the homotopy category of Eilenberg MacLane commutative ring spectra is equivalent to the category of Tambara functors. ([Ull13](#Ull13))

Some other examples are related to [[Witt-Burnside functors]], Witt rings in the sense of Dress and Siebeneicher.

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

## Related concepts

* [[Mackey functor]]
* [[polynomial functor]]
* [[Witt vectors]]
* [[N-∞ operad]]

##References

* {#Tam93} [[Daisuke Tambara]], _On multiplicative transfer_, Comm. Algebra 21 (1993), no. 4, 1393&#8211;1420 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/tambara.pdf)).

* [[Neil Strickland]], _Tambara Functors_, [arXiv:1205.2516](http://arxiv.org/abs/1205.2516)
* [[Morten Brun]], _Witt vectors and Tambara functors_, [arXiv:math/0304495](http://arxiv.org/abs/math/0304495)

* {#AB15} [[Vigleik Angeltveit]] and [[Anna Marie Bohmann]], _Graded Tambara Functors_, ([arXiv:1504.00668](http://arxiv.org/abs/1504.00668))
[[!redirects Tambara functors]]
* {#Ull13} [[John Ullman]], _Tambara Functors and Commutative Ring Spectra_, ([arXiv:1304.4912](http://arxiv.org/abs/1304.4912))
* [[Michael Hill]], _Derived Equivariant Algebraic Geometry_, ([lecture and notes](https://www.msri.org/workshops/689/schedules/18236))
* Kristen Mazur, _On the Structure of Mackey Functors and Tambara Functors_, ([thesis](http://sites.lafayette.edu/mazurk/files/2013/07/Mazur-Thesis-4292013.pdf))
* {#Hill17} [[Michael Hill]], _On the Andre-Quillen homology of Tambara functors_, ([arXiv:1701.06219](https://arxiv.org/abs/1701.06219))
* [[Andrew Blumberg]], [[Michael Hill]], _Incomplete Tambara functors_, ([arXiv:1603.03292](https://arxiv.org/abs/1603.03292))

* [[Elden Elmanto]], [[Rune Haugseng]], _On distributivity in higher algebra I: The universal property of bispans_, ([arXiv:2010.15722](https://arxiv.org/abs/2010.15722))

* [[Bastiaan Cnossen]], [[Rune Haugseng]], [[Tobias Lenz]], [[Sil Linskens]], _Normed equivariant ring spectra and higher Tambara functors_, ([arXiv:2407.08399](https://arxiv.org/abs/2407.08399))

[[!redirects Tambara functors]]