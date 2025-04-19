
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


> For disambiguation see at *[[wreath product]]*.


\tableofcontents


## Definition ##

\begin{definition}\label{BasicDefinition}
Given ([[discrete groups|discrete]]) [[groups]] $H, G \in Grp(Set)$ and a [[G-set]] $S$, the *wreath product group*

$$
  H \wr_S G 
  \;\;
  \coloneqq
  \;\;
  H^S \rtimes G
$$

is the [[semidirect product group]] of 

1. the [[direct product group]] $H^S$ of ${\vert S \vert}$ copies of $H$ 

1. with $G$, [[group action|acting]] on $H^S$ by [[permutation]] of factors:

   $$
     g \big((h_s)_{s \in S}\big)
     \;\coloneqq\;
     \big(h_{g^{-1}(s)}\big)_{s \in S}
     \,.
   $$

\end{definition}

(cf. [BMMN 2006, Def. 8.1](#BMMN06), see also [James & Kerber 1984 §4.1](#JamesKerber84))


\begin{remark}\label{Notation}
**(Notation)**
Other notation for "$H \wr_S G$" is "$H Wr_S G$" or "$H wr_S G$". 

Often the choice of $G$-set $S$ is notationally suppressed, writing instead "$H \wr G$", etc.

But beware that conventions differ:

Some authors understand by default the [[regular action]] of $G$ on its [[underlying set]]. 

But when $G = Sym(n)$ is a [[symmetric group]], then often its defining action on $\{1, \cdots, n\}$ is understood (cf. Ex. \ref{FundamentalGroupOfHomotopyQuotientByPermutations} below). In this case [James & Kerber 1984 §4.2](#JamesKerber84) speak of *complete monomial groups over $H$*.
\end{remark}


## Examples ##

\begin{example}
The [[dihedral group]] $Dih(4)$ of [[order of a group|order]] $2\cdot 4=8$ is the wreath product $C_2 \wr C_2$ of [[cyclic group of order 2|$C_2$]] with itself (in this sense of regular representations).
\end{example}

More generally:

\begin{example}
The [[symmetry group]] of the $n$-dimensional [[hypercube]] is $C_2 \wr Sym(n)$.
\end{example}

\begin{example}
The [[Sylow p-subgroup|Sylow-$p$-subgroups]] $P_n$ of the [[symmetric groups]] $Sym(n)$ can be [[recursion|recursively]] described as the wreath product $C_p \wr P_a$ where $C_p$ is the [[cyclic group]] of [[order of a group|order]] $p$ and $n = a p+r$ with $0\leq r \lneq p$.
\end{example}

\begin{example}
The [[Sylow p-subgroup|Sylow-$\ell$-subgroups]] of [[general linear group|$GL_n(q)$]] for [[greatest common divisor|$gcd(q,\ell)=1$]] can [[recursion|recursively]] be described as a wreath product of the Sylow-$\ell$-subgroup of a strictly smaller $GL_{m}(q)$ and a Sylow-$\ell$-subgroups of a suitable [[symmetric group]].
\end{example}

\begin{example}
\label{FundamentalGroupOfHomotopyQuotientByPermutations}
  For a [[connected topological space]] $X$, the [[homotopy quotient]] of its $n$-fold [[product topological space]] by the [[symmetric group]] $Sym(n)$ [[group action|acting]] by [[permutation]] of factors, hence the [[Borel construction]]  
$$
  X^n \sslash Sym(n)
  \;\;
  \simeq
  \;\;
  \big(
    X^n \times E Sym(n)
  \big)
  / Sym(n)
  \,,
$$
has as [[fundamental group]] the wreath product with the [[fundamental group]] of $X$:
$$
  \pi_1\big(
    X^n \sslash Sym(n)
  \big)
  \;\simeq\;
  \pi_1(X) \wr Sym(n)
  \,.
$$
\end{example}
(cf. [MO:a/867292](https://math.stackexchange.com/a/867292/58526))

\begin{example}
  A [[framed braid group]] is the wreath product with the [[integers]] $\mathbb{Z}$ of a plain [[braid group]].
\end{example}



## Properties

### General 

\begin{remark}\label{AsAPermutationGroup}
**(as a permutation group)**
\linebreak
If both $H \subset Sym(X)$ and $G \subset Sym(Y)$ are presented as [[permutation groups]], then the wreath product is itself a permutation group, acting on the [[Cartesian product]] set $X \times Y$ by letting $G$ act trivially on the first and naturally on the second factor and letting $H^Y$ act on $X\times Y$ such that the $y$-th component of $H^Y$ permutes $X\times\{y\}$ naturally and fixes everything else pointwise.
\end{remark}
(e.g. [Holland 1989](#Holland89))


### Irreducible representations
 {#IrreducibleRepresentations}

Let $G$ be a [[finite group]]. Denote by $Irr(G) \simeq \big\{ [\rho_i] \big\}_{i \in I}$ the [[set]] of [[isomorphism classes]] of its [[irreducible representations]].

For $n \in \mathbb{N}$ and  $(n_i \in \mathbb{N})_{i \in I}$ an $I$-[partition](partition#partitions_of_natural_numbers), in that $n = \sum_i n_i$, write

$$
  Sym_{(n)}
  \;\coloneqq\;
  \textstyle{\prod_{i \in I}} Sym_{n_i}
  \;\;
  \subset
  \;\;
  Sym_n
$$

There is an evident [[linear representation]] of 
$$
  \textstyle{\prod_{i \in I}}
  \big(
    G \wr Sym_{n_i}
  \big)
  \;\;
  \simeq
  \;\;
  G \wr Sym_{(n)} 
  \;\;\subset\;\; 
  G \wr Sym_n
$$ 
on 
\[
  \label{PartitionedExternalTensorProduct}
  \rho
  \;\coloneqq\;
  \displaystyle{\underset{i \in I}{\boxtimes}}
  \rho_i^{\boxtimes_{n_i}} 
  \;\;\;
  \in
  \;\;
  Rep(G \wr Sym_{(n)})
  \,,
\]
where the [[subgroup]] $G^n \subset G \wr Sym_{(n)}$ acts according to the [[external tensor product of representations]], and the subgroup $Sym_{(n)}$ acts by [[permutation]] of [[tensor product of vector spaces|tensor factors]].

The irreps $\sigma$ of the [[direct product group]] $Sym_{(n)}$ are (see [there](direct+product+group#IrrepsOfDirectProductsAreExternalTensorProductsOfIrreps)) of the form 
\[
  \label{IrrepsOfPartitionedSymmetricGroup}
  \sigma 
    \;\simeq\; 
  \underset{i \in I}{\boxtimes} \sigma_{j(i)}
  \,,
\] 
for $\sigma_{j(i)}$ an [[representation theory of the symmetric group|irrep of the symmetric group]] $Sym_{n_i}$. We may canonically regard $\sigma$ as a representation of $G \wr Sym_{(n)} \twoheadrightarrow Sym_{(n)}$.

\begin{theorem}
  \label{IrrepsOfWreathProductOfFiniteGroup}
  For $G$ a [[finite group]] and $n \in \mathbb{N}$,
  the [[irreducible representations]] of the [[wreath product group]] $G \wr Sym_n$ are, up to [[isomorphism]], exactly the [[induced representations]] along $G \wr Sym_{(n)} \hookrightarrow G \wr Sym_n$ of the [[tensor product of representations|tensor products]] of representations $\rho$ (eq:PartitionedExternalTensorProduct) for $(n)$ an $I$-partition as above, with irreps $\sigma$ (eq:IrrepsOfPartitionedSymmetricGroup) of $Sym_{(n)}$:
\[
  \label{FormulaForIrrepsOfWreathProductWithFiniteGroup}
  \mathbb{C}\big[
    G \wr Sym_n
  \big]
  \otimes_{
    \mathbb{C}\big[ G \wr Sym_{(n)} \big]
  }
  \bigg(
    \Big(
      \displaystyle{\underset{i \in I}{\boxtimes}}
      \rho_i^{\boxtimes_{n_i}} 
    \Big)
    \otimes
    \sigma
  \bigg)
  \,.
\]
\end{theorem}

This is a digest of [James & Kerber 1984 Thm. 4.3.34](#JamesKerber84), for the special case that their "$H$" is all of $H = Sym_n$. For proper subgroups $H \subset Sym_n$ the analogous statement holds for the irreps of $G \wr H$, with $Sym_{(n)}$ above replaced throughout by $Sym_{(n)} \cap H$.

\begin{example}
\label{IrrepsOfCkWreathSym3}
**(Irreps of $C_k \wr Sym_3$)**

For $k \in \mathbb{N}_{\gt 0}$ denote by $C_k$ the [[cyclic group]] of [[order of a group|order]] $k$. Its [[complex numbers|complex]] [[irreps]] $\mathbf{1}_{p}$ are all 1-dimensional, labeled by $p \in C_k$: The element $[1] \in C_k$ acts on $\mathbf{1}_p$ as multiplication with $e^{2 \pi \mathrm{i} \tfrac{p}{k}}$.

The irreps of $Sym_3$ are the [[trivial representation]] $\mathbf{1}$, the [[sign representation]] $\mathbf{1}_{sgn}$ and the [standard representation](representation+theory+of+the+symmetric+group#TheStandardRepresentation) $\mathbf{2}$.

The irreps of $C_p \wr Sym_3$ according to Thm. \ref{IrrepsOfWreathProductOfFiniteGroup} may be regarded as falling into 3 classes, according to the nature of the corresponding partition:

**Case 1 -- Partition involves a single irrep** $\mathbf{1}_p$. 
In this case $Sym_{(3)} \simeq Sym_3$ and the formula (eq:FormulaForIrrepsOfWreathProductWithFiniteGroup) produces the representations
$$
  \mathbf{1}_{p}^{\boxtimes_3}
  \otimes
  \sigma
  \;\;
  \in
  \;\;
  Rep(C_p \wr Sym_3)
$$
for $p \in C_p$ and $\sigma \in \big\{\mathbf{1}, \mathbf{1}_{sgn}, \mathbf{2}\big\}$.


**Case 2 -- Partition involves two distinct irreps**, $\mathbf{1}_p$ and $\mathbf{1}_{p'}$. 
In this case $Sym_{(3)} = 1 \times Sym_2 \simeq Sym_2$ and the formula (eq:FormulaForIrrepsOfWreathProductWithFiniteGroup) produces
$$
  \mathbb{C}\big[
    C_k \wr Sym_3
  \big]
  \otimes_{
    \mathbb{C}\big[
      C_k \times (C_k \wr Sym_2)
    \big]
  }
  \Big(
    \big(
      \mathbf{1}_{p} 
        \boxtimes
      \mathbf{1}_{p'}^{\boxtimes_2}
    \big)
    \otimes
    \sigma
  \Big)
$$
for $p \neq p' \in C_k$ and $\sigma \in \big\{\mathbf{1}, \mathbf{1}_{sgn}\big\}$.

**Case 3 -- Partition involves three distinct irreps**, $\mathbf{1}_{p_1}, \mathbf{1}_{p_2}, \mathbf{1}_{p_3}$. 
In this case $Sym_{(3)} \simeq 1 \times 1 \times 1 \simeq 1$ and the formula (eq:FormulaForIrrepsOfWreathProductWithFiniteGroup) produces
$$
  \mathbb{C}\big[
    C_k \wr Sym_3
  \big]
  \otimes_{
    \mathbb{C}\big[
      C_k^3
    \big]
  }
  \big(
    \mathbf{1}_{p_1} 
      \boxtimes
    \mathbf{1}_{p_2}
      \boxtimes
    \mathbf{1}_{p_3}
  \big)
$$
for $p_i \in C_k$ pairwise distinct.

\end{example}


\linebreak


## References 

Monographs:

* {#BMMN06} Meenaxi Bhattacharjee, Dugald Macpherson, Rögnvaldur G. Möller, Peter M. Neumann: *Wreath products*, Chapter 8 of: *Notes on Infinite Permutation Groups*, Lecture Notes in Mathematics **1698**, Springer (2006) 67-76 &lbrack;[doi:10.1007/BFb0092558](https://doi.org/10.1007/BFb0092558)&rbrack;

See also:

* {#Holland89} W. Charles Holland: _The characterization of generalized wreath products_, J. Alg. **13** (1989) 152-172 &lbrack;<a href="https://doi.org/10.1016/0021-8693(69)90069-6">doi:10.1016/0021-8693(69)90069-6</a>, [pdf](https://core.ac.uk/download/pdf/82380943.pdf)&rbrack;

In the generality of [[semigroups]]:

* [[Charles Wells]]: _Some applications of the wreath product construction_, Amer. Math. Monthly __83__ 5 (1976) &lbrack;[doi:10.1080/00029890.1976.11994114](https://doi.org/10.1080/00029890.1976.11994114)&rbrack;


Special cases and applications:

* G. Baumslag: _Wreath products and extensions_, Math Z **81** (1963) 286-299 &lbrack;[doi:10.1007/BF01111576](https://doi.org/10.1007/BF01111576)&rbrack;

* [[I. G. Macdonald]]: _Polynomial functors and wreath products_, J. Pure Appl. Alg. __18__ (1980) 173-204 \[<a href="https://doi.org/10.1016/0022-4049(80)90128-0">doi:10.1016/0022-4049(80)90128-0</a>, [pdf](https://core.ac.uk/download/pdf/82423307.pdf)\]

On the [[representation theory]] of wreath products with [[symmetric groups]]:

* {#JamesKerber84} [[Gordon D. James]], Adalbert Kerber: *Representations of Wreath Products*, Chapter 4 of: *The Representation Theory of the Symmetric Group*, Cambridge University Press (1984) &lbrack;[doi:10.1017/CBO9781107340732](https://doi.org/10.1017/CBO9781107340732)&rbrack;

* I. A. Pushkarev: *On the representation theory of wreath products of finite groups and symmetric groups*, Journal of Mathematical Sciences, **96** (1999) 3590–3599 &lbrack;[doi:10.1007/BF02175835](https://doi.org/10.1007/BF02175835)&rbrack;

  originally in: *Representation theory, dynamical systems, combinatorial and algorithmic methods. Part II*, Zap. Nauchn. Sem. POMI **240**, POMI, St. Petersburg (1997) 229–244 &lbrack;[mathnet:znsl475](https://www.mathnet.ru/eng/znsl475)&rbrack;

On [[wreath product of groups|wreath products]] of a [[cyclic groups|cyclic]] with a [[symmetric group]] as analogs of ([[anyon]]) [[braid groups]] in [[dimension of a manifold|dimension]] $\gt 2$:

* [[Michael Freedman]], [[Matthew B. Hastings]], [[Chetan Nayak]], [[Xiao-Liang Qi]], [[Kevin Walker]], [[Zhenghan Wang]]: *Projective Ribbon Permutation Statistics: a Remnant of non-Abelian Braiding in Higher Dimensions*, Phys. Rev. B **83** 115132 (2011) &lbrack;[doi:10.1103/PhysRevB.83.115132](https://doi.org/10.1103/PhysRevB.83.115132), [arXiv:1005.0583](https://arxiv.org/abs/1005.0583)&rbrack;

On wreath products with [[braid groups]] (cf. also *[[framed braid group]]*):

* *Semidirect products with braid groups and type $F_\infty$* &lbrack;[MO:q/179104](https://mathoverflow.net/q/179104/381)&rbrack;


category: algebra

[[!redirects wreath products of groups]]

[[!redirects wreath product group]]
[[!redirects wreath product groups]]
