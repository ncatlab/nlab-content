> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

***

## Idea

In the context of [[holography]]/[[AdS-CFT duality]] and [[holographic entanglement entropy]], by an *entanglement wedge* $W(A)$ one refers (since [HHLR 2014](#HHLR2014)) to a subspace of the [[bulk]] [[spacetime]] which is the holographic dual of a given subspace $A$ of the [[asymptotic boundary]].

Concretely, the entanglement wedge of $A$ is the causal hull of  the *homology surface* of $A$, hence the maximal [[globally hyperbolic spacetime]] whose [[Cauchy surface]] is the homology surface of $A$. (Here, the *homology surface* of $A$ is the minimal area bulk region whose [[boundary of a manifold|boundary]] is the [[union]] of $A$ with its [Ryu-Takayanagi surface](holographic+entanglement+entropy#RyuTakayanagiFormula).)

Closely related to but crucially different from the entanglement wedge is the *causal wedge* of $A$, which is the [[intersection]] of the [[causal structure|causal]] [[future]] and [[past]] of $A$ inside the bulk. In contrast to the entanglement wedge, the causal wedge is generally not [[globally hyperbolic spacetime|globally hyperbolic]] (cf. [Rangamani & Takayanagi 2017 §9.2.2](#RangamaniTakayanagi2017)).

## References

The notion was introduced in:

* [[Bartlomiej Czech]], Joanna L. Karczmarek, Fernando Nogueira, [[Mark Van Raamsdonk]]: *The Gravity Dual of a Density Matrix*, Classical and Quantum Gravity **29** (2012) 155009 &lbrack;[arXiv:1204.1330](https://arxiv.org/abs/1204.1330), [doi:10.1088/0264-9381/29/15/155009](https://doi.org/10.1088/0264-9381/29/15/155009)&rbrack;

and the term "entanglement wedge" was coined in:

* {#HHLR2014} [[Matthew Headrick]], [[Veronika E. Hubeny]], Albion Lawrence, [[Mukund Rangamani]]: *Causality & holographic entanglement entropy*,  J. High Energ. Phys. **2014** 162 (2014) &lbrack;<a href="https://doi.org/10.1007/JHEP12(2014)162">doi:10.1007/JHEP12(2014)162</a>, <a href="https://arxiv.org/abs/1408.6300">arXiv:1408.6300 hep-th</a>&rbrack;

The entanglement wedge reconstruction property was more comprehensively argued in:

* Xi Dong, [[Daniel Harlow]], [[Aron C. Wall]]: *Reconstruction of Bulk Operators within the Entanglement Wedge in Gauge-Gravity Duality*, Phys. Rev. Lett. **117** 021601 (2016) &lbrack;[doi:10.1103/PhysRevLett.117.021601](https://doi.org/10.1103/PhysRevLett.117.021601), [arXiv:1601.05416](https://arxiv.org/abs/1601.05416)&rbrack;

* [[Daniel L. Jafferis]], Aitor Lewkowycz, [[Juan Maldacena]], S. Josephine Suh: *Relative entropy equals bulk relative entropy*, J. High Energ. Phys. **2016** 4 (2016) &lbrack;<a href="https://doi.org/10.1007/JHEP06(2016)004">doi:10.1007/JHEP06(2016)004</a>, [arXiv:1512.06431](https://arxiv.org/abs/1512.06431)&rbrack;



Review:

* {#RangamaniTakayanagi2017} [[Mukund Rangamani]], [[Tadashi Takayanagi]]; §9.2.2 in: *Holographic Entanglement Entropy*, Lecture Notes in Physics **931**, Springer (2017) &lbrack;[doi:10.1007/978-3-319-52573-0](https://doi.org/10.1007/978-3-319-52573-0), [arXiv:1609.01287](https://arxiv.org/abs/1609.01287)&rbrack;



This is how you place two tikzcd diagrams side by side:
<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
  A
  \arrow[r,  "{B(1, f)}", ""{name=U, below}]
  \arrow[d, "f"']
  & B
  \arrow[d, "id"]
  \\
  B
  \arrow[r, "U_B"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
<td style="border: none;">
\begin{tikzcd}
  B
  \arrow[r,  "{B(f, 1)}", ""{name=U, below}]
  \arrow[d, "id"']
  & A
  \arrow[d, "f"]
  \\
  B
  \arrow[r, "U_B"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
</tr>
</table>

\linebreak

***

\begin{tikzcd}
  T'
  \ar[
    dd, shift left=5pt, "{ n }"
  ] 
  \ar[
    dd, shift right=5pt, "{ n' }"{swap}
  ] 
  \ar[
    ddr, "{ m'_i }"
  ]
  && & 
  U(T')
  \ar[
    dd, shift left=5pt, "{ U(n) }"
  ] 
  \ar[
    dd, shift right=5pt, "{ U(n') }"{swap}
  ] 
  \ar[
    ddr, "{ U(m'_i) }"
  ]
  \\
  && \mapsto
  \\
  T
  \ar[
    r, "{ m_i }"{swap}
  ]
  &
  S_i
  &&
  \mathllap{X = \;}
  U(T)
  \ar[r, "{ f_i }"]
  &
  U(S_i)
\end{tikzcd}



***


+-- {: .num_prop#SiftedIffFinalDiag}
###### Proposition

An [[inhabited set|inhabited]] [[small category]] $D$ is sifted precisely if the [[diagonal]] functor 
  
$$
  D \to D \times D
$$

is a [[final functor]].

=--

This is due to ([GabrielUlmer](#GabrielUlmer))

+-- {: .num_prop #SiftedIffFinalDiag}
###### Proposition

Let $D$ be a small category. The following are equivalent:

1. $D$ is sifted.

2. $D$ is non-empty and for every pair of objects $d_1,d_2\in D$, the category $Cospan_D(d_1,d_2)$ of [[cospans]] from $d_1$ to $d_2$ is [[connected category|connected]].

3. The diagonal functor $D\to D^S$ is final, where $S$ is a finite set.

4. For every finite family of objects $d_1,\dots,d_n\in D$, the category $Sink_D(d_1,\dots,d_n)$ of sinks in $D$ with sources $d_1,\dots,d_n$ is connected.

=--

+-- {: .proof}
###### Proof

The equivalence between 1 and 2 is just the restatement of \ref{SiftedIffFinalDiag}. The equivalence between 3 and 4 is obvious. Trivially, 2 implies 4. We see the converse.

Assume 4. In particular we have that the category of sinks $Sink_D(\emptyset)$ over the empty family of objects in $D$ is connected and thus inhabited, so $D$ is non-empty.

Now let's see that $Sink_D(d_1,\dots,d_n)$ is non-empty. If $n=0$, this is because $D$ is non-empty. If $n=1$, we always have the identity sink $d_1\to d_1$. We show $Sink_D(d_1,\dots,d_n)$ is non-empty for $n\geq 2$ by induction on $n$. The base case $n=2$ is our assumption. For each $1\leq i\lt n$, pick a cospan $d_1\to c_i\leftarrow d_{i+1}$. By induction, there is a sink $\{c_i\to e\}_{1\leq i\lt n}$. Thus $\{d_1\to c_1\to e\}\cup\{d_{i+1}\to c_i\to e\}_{1\leq i\lt n}$ is a sink with sources $d_1,\dots,d_n$. Now we show there is a zig-zag of morphisms between any two objects of $Sink_D(d_1,\dots,d_n)$. In the case $n=0$, this is our assumption. Let $n\geq 1$. Given two sinks $\{d_i\to c\}_{1\leq i \leq n}$, $\{d_i\to e\}_{1\leq i \leq n}$, the assumption gives a cospan $c\to a\leftarrow e$, 

=--

\tableofcontents




## Idea

The *Floreanini-Jackiw Lagrangian* (FL, due to [Floreanini & Jackiw 1987](#FloreaniniJackiw1987)) is a [[Lagrangian density]] for a [[scalar field]] in 2-dimensions whose [[equations of motion]] single out (essentially) just the "right moving" ("chiral") half of solutions of the usual [[relativistic field theory|relativistic]] [[wave equation]]. As such, the FJ-Lagrangian density is an approach, in low dimension, to the notoriously subtle problem of finding [[Lagrangian densities]] for [[self-dual higher gauge fields]].

The FL-Lagrangian arises also as the [[effective field theory|effective]] [[boundary field theory]] of [[abelian Chern-Simons theory]] ([Wen 1992 §2.5](#Wen1992), [1995 §3.3](#Wen1995), cf. [Tong 2016 §6.1.2](#Tong2016)). This realizes the FL theory as the abelian case of [[Wess-Zumino-Witten theory]] (cf. [[CS/WZW correspondence]]) and witnesses it as the [[effective field theory]] of [[edge modes]] in [[fractional quantum Hall systems]].

## From abelian Chern-Simons theory

The [[Lagrangian density]] of [[abelian Chern-Simons theory]] with [[gauge field]] [[differential 1-form|1-form]] $a$ is 

\[
  \propto \tfrac{1}{2} a \wedge \mathrm{d}a
  \mathrlap{\,.}
\]

Setting

\[
  a = \mathrm{d}\phi
\]

and on the 3D [[spacetime]] [[manifold with boundary|with boundary]] $\mathbb{R}^{0,1} \times \mathbb{R}^2_{y \leq 0}$ gives, by [[Stokes' theorem]], the [[boundary field theory|boundary]] Lagrangian density for $\phi$ ([Wen 1992 (2.62)](#Wen1992))

\[
  L(\phi) 
    = 
  \tfrac{1}{2} (\partial_x \phi) (\partial_{t'}\phi) 
\]

for $t'$ and $x$ two [[coordinate functions]] on the 2D [[spacetime]] $\mathbb{R}^2$. Understanding ([Wen '92 (2.64)](#Wen1992))

\[
  t' \coloneqq t - c x
\]

as a [[lightcone gauge]] coordinate, this is

\[
  L(\phi) 
    = 
  \tfrac{1}{2} (\partial_x \phi) 
  \big(
    \partial_{t} - c \partial_x\phi 
  \big) 
  \mathrlap{\,.}
\]

This is the FL-Lagrangian density:

## Lagrangian and Equations of motion

For $\phi$ a [[scalar field]] on $\mathbb{R}^2$ (the latter equipped with its canonical [[coordinate functions]], here denoted $t$ for *[[time]]* and $x$ for *[[space]]*), the FL [[Lagrangian density]] is ([FL '87 (20)](#FloreaniniJackiw1987)):

\[
  L(\phi)
  \;\coloneqq\;
  \tfrac{1}{2}
  (\partial_x\phi) 
  \big(
    \partial_t \phi
      - 
    c
    \partial_x \phi
  \big)
  \mathrlap{\,,}
\]

where $c \in \mathbb{R} \setminus \{0\}$ is a constant which sets the [[velocity]] (the [[speed of light]], often set to $c = 1$).

The corresponding [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] is 

\[
  \big(
    \partial_t - c \partial_x
  \big)
  \partial_x
  \phi
  = 0
  \mathrlap{\,.}
\]

The general solutions to this equation are of the form

\[
  \label{TheEquationOfMotion}
  \phi(t,x)
  = 
  \phi_c(x + c t)
  + 
  g(t)
\]

where $g$ is an arbitrary ([[smooth function|smooth]]) function of just the temporal coordinate $t$ (hence is a "spatial zero mode"), while $\phi_c$ is a solution of the *chiral/right-moving wave equation*

\[
  \big(
    \partial_t - c \partial_x
  \big)
  \phi_c
  = 0
  \mathrlap{\,.}
\]

## As effective theory of FQH edge modes

When the the FL theory is understood as an [[effective field theory]] for [[edge modes]] of [[fractional quantum Hall liquids]] ([Wen 1992 §2.5](#Wen1992), review in  [Tong 2016](#Tong2016) [p. 207](https://ncatlab.org/nlab/files/Tong-QuantumHallEffect.pdf#page=209)), it is the spatial derivative

\[
  \rho \coloneqq \partial_x \phi
\]

which represents the [[current density]] on the edge, and by (eq:TheEquationOfMotion) this again satisfies the chiral wave equation

\[
  \big(
    \partial_t - c \partial x
  \big)
  \rho
  = 0
  \mathrlap{\,.}
\]



## References

### General

The original article:

* {#FloreaniniJackiw1987} [[Roberto Floreanini]], [[Roman Jackiw]]: *Self-dual fields as charge-density solitons*, Phys. Rev. Lett. **59** (1987) 1873 &lbrack;[doi:10.1103/PhysRevLett.59.1873](https://doi.org/10.1103/PhysRevLett.59.1873)&rbrack;
  > (the FR-Lagrangian appears in equation (20))

A manifestly [[Lorentz group]]-[[invariant]] re-formulation:

* {#Townsend202} [[Paul K. Townsend]]: *Manifestly Lorentz invariant chiral boson action*, Phys. Rev. Lett. **124** (2020) 101604 \[<a href="https://doi.org/10.1103/PhysRevLett.124.101604">doi:10.1103/PhysRevLett.124.101604</a>, [arXiv:1912.04773](https://arxiv.org/abs/1912.04773)\]

### As EFT for FQH edge modes

Review as the [[boundary field theory]] of [[abelian Chern-Simons theory]], in the context of [[effective field theory]] for [[edge modes]] of [[fractional quantum Hall systems]]:

* {#Wen1992} [[Xiao-Gang Wen]]; §2.5 in: *Theory of Edge States in Fractional Quantum Hall Effects*, International Journal of Modern Physics B **06** 10 (1992) 1711-1762 &lbrack;[doi:10.1142/S0217979292000840](https://doi.org/10.1142/S0217979292000840), [[Wen-EdgeStatesEffective.pdf:file]]&rbrack;

* {#Wen1995} [[Xiao-Gang Wen]]; §3.3 in: *Topological order in rigid states and edge excitations in fractional quantum Hall states*, Advances in Physics **44** 5 (1995) 405-437 &lbrack;[arXiv:cond-mat/9506066](https://arxiv.org/abs/cond-mat/9506066), [doi;10.1080/00018739500101566](https://doi.org/10.1080/00018739500101566)&rbrack;

reviewed in:

* {#Tong2016} [[David Tong]]; §6.1.2 in: *The Quantum Hall Effect*, lecture notes (2016) &lbrack;[arXiv:1606.06687](https://arxiv.org/abs/1606.06687), [course webpage](https://www.damtp.cam.ac.uk/user/tong/qhe.html), [pdf](http://www.damtp.cam.ac.uk/user/tong/qhe/qhe.pdf), [[Tong-QuantumHallEffect.pdf:file]]&rbrack;




\linebreak


## Nonconservative mathematical adjectives

In the practice of the naming of concepts in [[mathematics]], it happens that an adjective added to a term not just qualifies that term but actually contradicts it. 

For instance "[[partial functions]]" are not special kinds of functions but are, generally, not functions at all. (More examples are listed below.) This is in contrast to cases like "[[abelian groups]]", which are indeed special kinds of [[groups]].

Hence such *nonconservative adjectives* are modifiers in mathematical terminology that fundamentally alter, negate, or expand the defining axioms of a base term, rather than simply restricting them.

In linguistics one speaks in such cases of *[privative adjectives](https://en.wikipedia.org/wiki/Privative_adjective)*. For example a "fake X" is not an "X", hence "fake" is a privative adjective in the English language.

While strict logic may suggest to avoid nonconservative/privative adjectives, their use in mathematics is pragmatic and the meaning is typically suggestive and readily grasped, instead of misleading. For instance the intended meaning of "[[manifolds with boundary]]" is clear, and yet (if the boundary is non-empty) these are not strictly speaking "[[manifolds]]", whence "with boundary" is a nonconservative qualifier.

Accordingly, an earlier suggestion in this entry to refer to nonconservatively qualified terminology as "red herrings" is (while it may have gained some popularity, though maybe for the wrong reason) not really appropriate, as "red herrings" in the figurative sense are deliberately misleading.



### FQH Excitation modes



On multiple modes resolving the would-be single GMP mode for [FQH excitations](quantum+Hall+effect#CollectiveExcitations) 

near filling fraction $\nu = 1/4$:

* Dung Xuan Nguyen, [[F. D. M. Haldane]], [[Edward H. Rezayi]], [[Dam Thanh Son]], Kun Yang: *Multiple Magnetorotons and Spectral Sum Rules in Fractional Quantum Hall Systems*, Phys. Rev. Lett. **128** (2022) 246402 \[<a href="https://doi.org/10.1103/PhysRevLett.128.246402">doi:10.1103/PhysRevLett.128.246402</a>, [arXiv:2111.10593](https://arxiv.org/abs/2111.10593), suppl:[pdf](https://journals.aps.org/prl/supplemental/10.1103/PhysRevLett.128.246402/Supp.pdf)\]

at [Jain filling fractions](quantum+Hall+effect#CompositeParticlePicture) $n/(2 p n \pm 1)$ with ${\vert n \vert}\geq 2$ (e.g. $\nu = 2/5, 3/7, 2/9, 2/7$):

* [[Ajit C. Balram]], Zhao Liu, [[Andrey Gromov]], [[Zlatko Papić]]: *Very-High-Energy Collective States of Partons in Fractional Quantum Hall Liquids*, Phys. Rev. X **12** (2022) 021008 \[<a href="https://doi.org/10.1103/PhysRevX.12.021008">doi:10.1103/PhysRevX.12.021008</a>, [arXiv:2111.10395](https://arxiv.org/abs/2111.10395)\]

at filling fractions $\nu  = n/(4 n \pm 1)$:

* [[Ajit C. Balram]], G. J. Sreejith, [[Jainendra K. Jain]]: *Splitting of Girvin-MacDonald-Platzman density wave and the nature of chiral gravitons in fractional quantum Hall effect*, Phys. Rev. Lett. **133** (2024) 246605 \[<a href="https://doi.org/10.1103/PhysRevLett.133.246605">doi:10.1103/PhysRevLett.133.246605</a>, [arXiv:2406.02730](https://arxiv.org/abs/2406.02730)\]

in FQH liquids that are not fully spin-polarized:

* Rakesh K. Dora, [[Ajit C. Balram]]: *Dispersion of collective modes in spinful fractional quantum Hall states on the sphere* \[<a href="https://arxiv.org/abs/2509.13100">arXiv:2509.13100</a>\] 

\linebreak

\begin{example}
In the category of [[schemes]] the subcategory of [[affine schemes]] is dense, see [[affine scheme#AffineSchemesFullSubcategoryOfOppositeOfRings|here]].
\end{example}

\begin{example}
In the category of [[smooth manifolds]], the full subcategory whose objects are given by $\mathbb{R}^n$ for $n\geq 1$ with the standard smooth structure, is dense.
\end{example}

Proof: The restricted Yoneda to the full subcategory spanned by ${\{R\}}$ is faithful, hence so is when restricted to the subcat spanned by $\{R,R^2\}$. To see fullness when restricted to the subcat spanned by $\{R,R^2\}$, suppose we are given a morphism $\operatorname{Hom}(-,M)\Rightarrow\operatorname{Hom}(-,N)$ of presheaves on $\mod_{\{R,R^2\}}$. Given $x\in M$, write $z_x\in N$ for the image of $1\in R$ of the induced map $R\to N$ from $R\to M,1\mapsto x$. Write $[x,y]:R^2\to M$ for the map sending $(1,0)$ and $(0,1)$ to $x$ and $y$, respectively, and write $z_{[x,y]}:R^2\to N$ for the induced map. Then $z_{[x,y]}=[z_x,z_y]$ by compatibility with the $i$-th component map $c_i:R\to R^2$, $i=1,2$. Thus, compatibility with the diagonal map $\Delta:R\to R^2$ gives $z_{x+y}=\Delta^*z_{[x,y]}=\Delta^*[z_x,z_y]=z_x+z_y$. On the other hand, given $r\in R$, compatibility with $r: k\to k$ gives $z_{r x}=rz_x$. Thus $x\mapsto z_x$ defines a map $f:M\to N$ of $R$-modules such that $f^*:\operatorname{Hom}(-,M)\Rightarrow\operatorname{Hom}(-,N)$ is the morphism we began with.



## Definition

A complex (or real) [[extended C*-algebra]] whose bounded part is a [[von Neumann algebra]].

Equivalently (by a theorem due to Dixon and Zakirov–Chilin), a complex (or real) [[*-algebra]] $A$ of closed densely defined unbounded operators on a [[Hilbert space]] closed under the operations of strong sum, strong multiplication, passing to adjoints, contains all scalar multiples of the identity operator, for every $x\in A$ we have $(1+x^*x)^{-1}\in A$ (equivalently, $x$ is affiliated with $A_b$), and the [[*-subalgebra]] $A_b$ of bounded operators in $A$ is a [[von Neumann algebra]].

## Properties

For any [[von Neumann algebra]] there is a unique (up to a unique isomorphism) maximal extended von Neumann algebra that has $A$ as its bounded part, namely, the extended von Neumann algebra of locally measurable operators affiliated with $A$.

The [[reduction theory]] for [[von Neumann algebras]] can be extended to the case of extended von Neumann algebras.

## References

* P. G. Dixon, _Generalized B*-algebras_, Proceedings of the London Mathematical Society s3-21:4 (1970), 693-715.  [DOI](https://doi.org/10.1112/plms/s3-21.4.693).

  **  establishes functional calculus for commutative extended C*-algebras and Gelfand-Neumark theorem for noncommutative extended C*-algebras
  ** defines “concrete” C*-algebras in Definition 7.1
  ** shows that “abstract” and “concrete” extended C*-algebras are the same notion, see Theorem 7.13

* P. G. Dixon, _Unbounded operator algebras_, Proceedings of the London Mathematical Society s3-23:1 (1971), 53-69.  [DOI](https://doi.org/10.1112/plms/s3-23.1.53).

  **  defines “concrete” extended von Neumann algebras (called EW*-algebras there) in Definition 1.2
  ** develops reduction theory in Section 3
  ** studies measurable operators in Section 4 and 5
  ** studies locally measurable operators in Section 6 and 7

* B. S. Zakirov, V. I. Chilin, _Abstract characterization of EW*-algebras_, Functional Analysis and Its Applications 25:1 (1991), 63-64.  [DOI](https://doi.org/10.1007/bf01090683).

  *  shows that “abstract” and “concrete” extended von Neumann algebras are the same

  *  proves that extended von Neumann algebras are precisely those [[extended C*-algebras]] whose bounded part is a [[von Neumann algebra]]

\[ A \].

