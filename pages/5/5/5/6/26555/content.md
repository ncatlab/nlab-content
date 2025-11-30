
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Quantum sets are a generalization of [[sets]] to the context of  [[noncommutative geometry]]. They have many equivalent definitions.

* A quantum set is a [[C-star algebra|$C^\ast$-algebra]] $\mathcal{A}$ that is the $c_0$-[[direct sum]] of full [[matrix algebras]]:
$$
  \mathcal{A} 
    \cong 
  \bigoplus_{i \in I}^{c_0} 
  M_{n_i}(\mathbb{C})
  \,.
$$

* A quantum set is a [[von Neumann algebra]] $\mathcal{M}$ that is an $l^\infty$-[[direct sum]] of full [[matrix algebras]].
$$
  \mathcal{M} 
  \cong 
  \bigoplus_{i \in I}^{l^\infty} 
  M_{n_i}(\mathbb{C})
  \,.
$$

* A quantum set $X$ is an [[indexed set|indexed family]] of nonzero [[finite-dimensional Hilbert spaces]]:
$$
  X 
  = 
  \{\mathcal{H}_i\}_{i \in I}
  \,.
$$

These definitions do not define equal classes of objects, but they can be extended to define [[equivalence of categories|equivalent categories]] in two natural ways. Using the second definition of quantum sets, we can take the [[morphisms]] to be [[quantum relations]] or, inequivalently, to be unital normal $*$-homomorphisms. In the former case, we obtain the [[category]] $qRel$, and in the latter case, we obtain the [[opposite category|opposite]] of the category $qSet$. Note that $qRel$ is equivalent to its own opposite. Quantum sets can be further generalized to "nontracial" quantum sets. This article will use the third definition of quantum sets because this definition avoids operator topologies, making it more accessible to a wider audience.

## Basic definitions

\begin{definition}
\label{QuantumSet}
A quantum set $X$ is a family of nonzero [[finite-dimensional Hilbert spaces]] over $\mathbb{C}$ that is [[indexed set|indexed]] by a set $\mathrm{At}(X)$, which may be empty, finite, or infinite.
$$
X = \{X_\alpha\}_{\alpha \in \mathrm{At}(X)}
  \,.
$$
\end{definition}

Very little changes if we allow zero-dimensional Hilbert spaces in this definition; doing so is mathematically more natural but less intuitive. The elements of $\mathrm{At}(X)$ are called the atoms of $X$.

Quantum sets are viewed as a generalization of sets by identifying each set $A$ with the quantum set $\mathrm{Inc}(A)$.

\begin{definition}
\label{Identification}
For each set A, we define the quantum set $\mathrm{Inc}(A)$ by
$\mathrm{At}(\mathrm{Inc}(A)) = A$ and $\mathrm{Inc}(A)_\alpha = \mathbb{C}$ for all $\alpha \in A$.
\end{definition}

The following basic operations generalize the familiar basic operations on sets.

\begin{definition}
\label{BasicOperations}
Consider quantum sets $X$ and $Y$ according to Def. \ref{QuantumSet}. Then:

* The *disjoint union* $X + Y$ is defined by $\mathrm{At}(X + Y) \coloneqq \mathrm{At}(X) + \mathrm{At}(Y)$ and
$$
(X + Y)_\alpha \coloneqq \begin{cases} 
  X_\alpha & \text{if }\;\alpha \in \mathrm{At}(X), 
  \\ 
  Y_\alpha & \text{if }\;\alpha \in \mathrm{At}(Y).
\end{cases}
$$

* The *Cartesian product* $X \times Y$ is defined by $\mathrm{At}(X \times Y) \coloneqq \mathrm{At}(X) \times \mathrm{At}(Y)$ and
$$
(X \times Y)_{(\alpha, \beta)} \coloneqq X_\alpha \otimes Y_\beta,
$$
where $\mathcal{H} \otimes \mathcal{K}$ denotes the Hilbert-space [[tensor product]].

\end{definition}

We have that $\mathrm{Inc}(A + B) = \mathrm{Inc}(A) + \mathrm{Inc}(B)$ and that $\mathrm{Inc}(A \times B) = \mathrm{Inc}(A) \times \mathrm{Inc}(B)$.

The Cartesian product of quantum sets is so named because it generalizes the Cartesian product of sets. However, in contrast to how the Cartesian product of ordinary sets is their [[cartesian product|categorical product]] in [[Set|$Set$]] in the usual sense of [[universal properties]], be warned that the Cartesian product of quantum sets is not their categorical product in either of the categories $qSet$ or $qRel$ defined below. 

\begin{remark} 
A similar nomenclatural clash occurs for [[Rel|$Rel$]], consisting of sets and relations: there the cartesian product of sets as familiarly understood yields a monoidal product but not a categorical product. 
\end{remark}

In both of the [[symmetric monoidal category|symmetric monoidal categories]] $qRel$ and $qSet$, $X + Y$ is the [[coproduct]] of $X$ and $Y$, and $X \times Y$ is the designated [[monoidal category|monoidal product]]. In $qRel$, $X+Y$ is also the [[cartesian product|product]] of $X$ and $Y$. In $qSet$, the [[cartesian product|product]] of $X$ and $Y$ is not easily definable and may be notated $X \ast Y$.

## The category $qRel$

\begin{definition}
\label{qRel}
We define the [[dagger-compact category]] $qRel$.

1. An object $X$ is a quantum set (see Def. \ref{QuantumSet}).

1. A morphism $R \colon X \to Y$ is a choice of subspaces
$$
R_{\alpha,\beta} \subseteq L(X_\alpha, Y_\beta),
$$
where $L(\mathcal{H},\mathcal{K})$ is the space of all linear maps from $\mathcal{H}$ to $\mathcal{K}$. These morphisms are called relations.

1. The composition $S \circ R \colon X \to Z$ of morphisms $R \colon X \to Y$ and $S \colon Y \to Z$ is given by
$$
(S \circ R)_{\alpha,\gamma} \coloneqq \mathrm{span}
\{s r \mid r \in R_{\alpha, \beta},\; s \in S_{\beta, \gamma}\;\text{for some}\; \beta \in \At(Y)\}.
$$

1. The identity morphism $\mathrm{id}_X\colon X \to X$ is defined by
$$
(\mathrm{id}_{X})_{\alpha, \beta} \coloneqq \begin{cases} \mathrm{span}\{1\} & \text{if}\;\alpha = \beta,\\
\{0\} & \text{if}\; \alpha \neq \beta.\end{cases}
$$

1. The [[dagger category|dagger]] of a morphism $R\colon X \to Y$ is defined by
$$
(R^\dagger)_{\beta, \alpha} \coloneqq \{r^\dagger \mid r \in R_{\alpha, \beta}\},
$$
where $r^\dagger$ is the [[hermitian matrix|Hermitian adjoint]].

1. The [[monoidal category|monoidal product]] of objects $X$ and $X'$ is the Cartesian product $X \times X'$ (see Def. \ref{BasicOperations}).

1. The monoidal product of morphisms $R\colon X \to Y$ and $R'\colon X' \to Y'$ is defined by
$$
(R \times R')_{(\alpha, \alpha'),(\beta, \beta')} \coloneqq \mathrm{span}\{r \otimes r' \mid r \in R_{\alpha, \beta},\; r' \in R'_{\alpha', \beta'}\}.
$$

1. The monoidal unit $1$ is defined by $\mathrm{At}(1) \coloneqq \{\bullet\}$ and $1_\bullet \coloneqq \mathbb{C}$.

1. The [[symmetric monoidal category|braiding]] $\sigma_{X,Y}\colon X \times Y \to Y \times X$ is defined by
$$
(\sigma_{X,Y})_{(\alpha,\beta),(\beta', \alpha')} \coloneqq \begin{cases} \mathrm{span}\{\sigma_{X_\alpha, Y_\beta}\} & \text{if}\; (\alpha, \beta) = (\alpha', \beta'),\\
\{0\} & \text{if}\;(\alpha, \beta) \neq (\alpha', \beta'),
\end{cases}
$$
where $\sigma_{X_\alpha, Y_\beta}$ denotes the braiding in [[Hilb|$Hilb$]]. The associator and unitors are defined similarly.

1. The [[dualizable object|dual]] of an object $X$ is the dual quantum set $X^*$, which is defined by $\mathrm{At}(X^*) \coloneqq \mathrm{At}(X)$ and
$$
(X^*)_\alpha \coloneqq X_\alpha^*,
$$
where $\mathcal{H}^*$ is the [[dual vector space|dual Hilbert space]].

\end{definition}

Furthermore, $qRel$ has all [[coproduct|coproducts]]. It is a [[semiadditive dagger category]] with infinitary dagger biproducts and an infinitary [[distributive monoidal category]] with a [[unitary]] distributor. The dagger biproduct of $X$ and $Y$ is their disjoint union $X + Y$ (see Def. \ref{BasicOperations}). The zero object $0$ is defined by $\mathrm{At}(0) = \emptyset$.

\begin{proposition}
The dagger-compact category $qRel$ is [[enriched category|enriched]] over [[suplattice|suplattices]] with 
$$
R \leq S \qquad \Longleftrightarrow \qquad R_{\alpha, \beta} \subseteq S_{\alpha, \beta}
$$
for all $\alpha \in \mathrm{At}(X)$ and $\beta \in \mathrm{At}(Y)$, where $R, S \colon X \to Y$. In other words, $qRel$ is a [[quantaloid]].
\end{proposition}

The dagger-compact category [[Rel|$Rel$]] is enriched over suplattices too. It is an [[allegory]], while $qRel$ fails to be an allegory because the relevant modular law fails. Nevertheless, $qRel(X,Y)$ is always a [[modular lattice]].

In effect, $Rel$ is an enriched dagger-compact subcategory of $qRel$.

\begin{definition}
We define the "inclusion" [[functor]] $\mathrm{Inc}\colon Rel \to qRel$:

* For each set $A$, we define $\mathrm{Inc}(A)$ as in Def. \ref{Identification}.

* For each relation $R\colon A \to B$, we define
$$
\mathrm{Inc}(R) =
\begin{cases}
\mathbb{C}  & \text{if}\;(\alpha, \beta) \in R, \\
0 & \text{if}\;(\alpha, \beta) \notin R,
\end{cases}
$$
where we identify $L(\mathbb{C}, \mathbb{C})$ with $\mathbb{C}$ in the obvious way.

\end{definition}

\begin{proposition}
The "inclusion" functor $\mathrm{Inc}\colon Rel \to qRel$ is an [[enriched functor|enriched]] [[monoidal functor|strong monoidal]] [[dagger functor]] that is [[full and faithful functor|full and faithful]].
\end{proposition}

The material in this section is mostly from [Kornell 2020](#Kornell20). The morphisms were first defined in [Kuperberg & Weaver 2012](#KuperbergWeaver12) and investigated in [Weaver 2012](#Weaver12); see the article on [[quantum relations]].

## The category $qSet$

\begin{definition}
We define the [[symmetric monoidal category]] $qSet$ to be the [[wide subcategory]] of $qRel$ whose morphisms are maps. A [[allegory|map]] is a morphism $f\colon X \to Y$ such that $f^\dagger \circ f \geq \mathrm{id}_X$ and $f \circ f^\dagger \leq \mathrm{id}_Y$.
\end{definition}

In the terminology of [[allegory|allegories]], $\qSet \coloneqq Map(qRel)$.
The maps in $qRel$, i.e., the morphisms in $qSet$, are sometimes called functions.

\begin{theorem}
\label{Cosmos}
The symmetric monoidal category $qSet$ is [[complete category|complete]], [[cocomplete category|cocomplete]], and [[closed monoidal category|closed]]. In other words, it is a [[Bénabou cosmos]]. It also has an [[(epi, mono) factorization system|epi-mono factorization system]].
\end{theorem}

The closure of $qSet$ can be deduced from general principles (see Theorem 6.16 of [Jenča & Lindenhovius 2025](#JencaLindenhovius25)).

\begin{proposition}
The "inclusion" functor $\mathrm{Inc}\colon Rel \to qRel$ restricts to a functor $\mathrm{Inc}\colon Set \to qSet$, which has a [[right adjoint]] $\mathrm{Elm}\colon qSet \to Set$.
\end{proposition}

\begin{definition}
We define the "elements" functor $\mathrm{Elm}\colon qSet \to Set$:

* For each quantum set $X$, we define $\mathrm{Elm}(X) = \{\alpha \in \mathrm{At}(X) \mid \mathrm{dim} (X_\alpha) = 1\}$.

* For each morphism $f \colon X \to Y$, we define $\mathrm{Elm}(f) = \{(\alpha, \beta) \in \mathrm{Elm}(X) \times \mathrm{Elm}(Y) \mid \mathrm{dim} (f_{\alpha, \beta}) = 1\}$.

\end{definition}

We have that $\mathrm{Elm}(X + Y) = \mathrm{Elm}(X) + \mathrm{Elm}(Y)$, that $\mathrm{Elm}(X \times Y) = \mathrm{Elm}(X) \times \mathrm{Elm}(Y)$, and that $\mathrm{Elm}(\mathrm{Inc}(A)) = A$. We also have a [[natural isomorphism]] $\mathrm{Elm}(X) \cong qSet(1,X)$. The monoidal unit $1$ is [[terminal object|terminal]] in $qSet$, so $\mathrm{Elm}(X)$ is essentially the set of [[global element|global elements]] of $X$.

\begin{theorem}
\label{qPow}
The inclusion functor $qSet \hookrightarrow qRel$ has a [[right adjoint]] $\mathrm{qPow}\colon qRel \to qSet$ with $\mathrm{qPow}(X) = [X^*, 1 + 1]$ for each quantum set $X$.
\end{theorem}

The notation $X^*$ refers to the dual of $X$, as in Def. \ref{qRel}. The notation $[X,Y]$ refers to the [[internal hom]] of $X$ and $Y$, as in Thm. \ref{Cosmos}. Thm. \ref{qPow} expresses that $qRel$ behaves somewhat like a [[allegory|power allegory]]. The quantum power set $qPow(X)$ is canonically a quantum poset in the sense of Example \ref{QuantumPoset}.
In general, $\mathrm{qPow}(\mathrm{Inc}(A)) \ncong \mathrm{Inc}(\mathrm{Pow}(A))$, where $\mathrm{Pow}(A)$ is the [[power set]] of $A$. However, we do have that $\mathrm{Elm}(\mathrm{qPow}(\mathrm{Inc}(A)) \cong \mathrm{Pow}(A)$. 

Overall, $qSet$ is unlike an [[topos|elementary topos]] in two respects. First, its monoidal product is not its categorical product, so it is not a [[cartesian monoidal category]]. However, its monoidal unit $1$ is terminal, so it is a [[semicartesian monoidal category]]. Furthermore, its monoidal product $X \times Y$ satisfies the uniqueness condition of the universal property that defines the [[cartesian product|categorical product]].

Second, $qSet$ does not have a [[subobject classifier]]. However, every subobject of a quantum set $X$ has a unique [[characteristic function|characteristic morphism]] $\chi\colon X \to 1 + 1$ such that $\chi = (! + !) \circ f$ for some $f \colon X \to X + X$ with $\nabla \circ f = \mathrm{id}_X$. Here, $!\colon X \to 1$ is the [[terminal object|unique]] morphism from $X$ to $1$ and $\nabla \colon X \to X + X $ is the [[codiagonal morphism|codiagonal]].

\begin{proposition}
Let $X$ be a quantum set. There is a [[one-to-one correspondence]] between the subsets of $At(X)$ and the [[subobjects]] of $X$ in $qSet$. Each subset $A \subseteq X$ corresponds to a subobject $j \colon W \to X$ with $At(W) = A$ and $W_\alpha = X_\alpha$.
\end{proposition}

The material in this section is mostly from [Kornell 2020](#Kornell20), [Kornell, Lindenhovius & Mislove 2022] (#KornellLindenhoviusMislove22), and [Jenča & Lindenhovius 2025](#JencaLindenhovius25).

## Internalization

Many classes of discrete quantum structures can be defined via [[internalization]] in the [[dagger-compact category|dagger-compact]] [[quantaloid]] $qRel$. In this context, the term "quantum" refers to [[noncommutative geometry]], and the term "discrete" refers to $C^*$-algebras that are $c_0$-direct sums of full matrix algebras, as in section 1.

We highlight two aspects of this internalization. First, for many classes of discrete quantum structures, the original definition in noncommutative geometry is motivated by sophisticated considerations that are specific to that class. In contrast, the definition via internalization in $qRel$ is simply a reinterpretation of a straightforward definition in $Rel$.

Second, in many cases, a comparable definition via internalization in $qSet$ is not available because the [[monoidal category|monoidal product]] in $qSet$ is not its [[cartesian product|categorical product]]. Thus, this section refers to "allegorical internalization" rather than "categorical internalization." In other words, the given definitions are meant to be interpreted in $qRel$, as well as [[Rel|$Rel$]] and other [[allegory|allegories]].

\begin{example}
\label{QuantumPoset}
A discrete quantum [[partial order|poset]] is a quantum set $X$ together with a relation $R\colon X \to X$ such that

1. $\id_X \leq R$,

1. $R \circ R \leq R$,

1. $R^\dagger \wedge R = id_X$,

where $R \wedge S$ is the [[meet]] of $R$ and $S$.
\end{example}

\begin{example}
A discrete quantum [[graph]] is a quantum set $X$ together with a relation $R\colon X \to X$ such that

1. $R^\dagger = R$,

1. $\id_X \leq R$.

These axioms internalize simple graphs with the convention that every vertex is adjacent to itself. This convention is standard in [[quantum information|quantum information theory]].
\end{example}


\begin{example}
A discrete quantum [[metric space]] is a quantum set $X$ together with a map $d\colon X \times X^* \to \mathrm{Inc}([0, \infty))$ such that

1. $\mathrm{Inc}(0)^\dagger \circ d = \varepsilon_X$,

1. $\mathrm{Inc}(+) \circ (d \times d) \circ (\id_X \times \varepsilon_X \times \id_X) \leq \mathrm{Inc}(\leq) \circ d$,

1. $d \circ \sigma_{X^*,X} = (d^*)^\dagger$,

where $\varepsilon_X$ is the [[dualizable object|counit]] and $\sigma_{X,Y}$ is the [[symmetric monoidal category|braiding]]. In axiom 1, the map $0: \{\bullet\} \to [0, \infty)$ has the value $0 \in [0, \infty)$.
\end{example}

\begin{example}
A discrete quantum [[monoid]] is a quantum set $X$ together with maps $m\colon X \times X \to X$ and $e\colon 1 \to X$ such that

1. $m \circ (m \times \id_X)= m \circ (\id_X \circ m)$,

1. $m \circ (e \times \id_X) = \id_X = m \circ (\id_X \times e)$.

\end{example}

\begin{example}
A discrete quantum [[group]] is a quantum monoid $(X,m,e)$ such that

1. $e^\dagger \circ m \circ (\!\top_X\! \times \id_X) = \!\top_X^\dagger$,

1. $e^\dagger \circ m \circ (\id_X \times \!\top_X\!) = \!\top_X^\dagger$,

where $\top_X$ is the [[top|maximum]] relation $1 \to X$. Note that a discrete quantum group is not a [[group object]] in $qSet$.
\end{example}

\begin{example}
A Kac-type discrete quantum group is a quantum monoid $(X,m,e)$ together with a map $i \colon X^* \to X$ such that

1. $m \circ (\id_X \times i) \circ \varepsilon_{X} = e$,

1. $m \circ (i \times \id_X) \circ \varepsilon_{X^*} = e$.

\end{example}

These examples are all discrete in the sense that the underlying quantum space is discrete and not in the sense that the structure on that quantum space is discrete. This qualification is necessary because the underlying space of a quantum structure is often assumed to be from a larger class. For example, the underlying quantum space of a quantum graph may be a quantum [[localizable measurable space|measurable space]], and the underlying space of a quantum group may be a quantum [[locally compact topological space|topological space]].

The material in this section is mostly from [Weaver 2012](#Weaver12), [Kornell 2024](#Kornell24), and [Chirvasitu & Kornell 2025](#ChirvasituKornell25).

## Duality

Quantum sets first appeared implicitly as a class of [[C-star-algebra|$C^\ast$-algebras]] in [Podleś & Woronowicz 1990](#PodlesWoronowicz90). However, these $C^\ast$-algebras are not [[identity element|unital]], and this makes the relevant category complicated to define. It is easier to work with an equivalent category of [[von Neumann algebra|von Neumann algebras]]. This category is [[duality|dual]] to $qSet$, and this section describes this duality.

\begin{definition}
\label{l-infinity}
For each quantum set $X$, define the von Neumann algebra
$$
l^\infty(X) \coloneqq \bigoplus_{i \in I}^{l^\infty} L(X_\alpha),
$$
where the notation refers to the $l^\infty$-[[direct sum]] of von Neumann algebras.
\end{definition}

This definition generalizes $l^\infty$ [[sequence space|sequence spaces]] in the sense that $l^\infty(\mathrm{Inc}(A)) = l^\infty(A, \mathbb{C})$ for every set $A$.

\begin{proposition}
For each quantum set $X$, there is a [[one-to-one correspondence]] between projection operators in $l^\infty(X)$ and relations $1 \to X$. Each projection operator $p$ corresponds to the relation $Supp(p)$, which is defined by
$$
Supp(p)_{\bullet, \alpha} \coloneqq \{r \in L(\mathbb{C}, X_\alpha) \mid p_\alpha r = r\}.
$$
\end{proposition}

In this context, a [[projector|projection operator]] $p \in l^\infty(X)$ is an element that satisfies $p^2 = p$ and $p^\dagger = p$, where $a^\dagger$ denotes the canonical [[star-algebra|anti-involution]] of the von Neumann algebra. For $a \in l^\infty(X)$, we define $(a^\dagger)_\alpha = a_\alpha^\dagger$.

\begin{definition}
We define $\mathrm{W}^\ast$ to be the [[symmetric monoidal category]] of [[von Neumann algebra|von Neumann algebras]] and unital ultraweakly continuous $\dagger$-homomorphisms with the spatial tensor product.
\end{definition}

\begin{theorem}
There is a [[full and faithful]] [[monoidal functor|strong monoidal]] [[contravariant functor]] $l^\infty \colon qSet \to \mathrm{W}^\ast :$

* For each quantum set $X$, we define $l^\infty(X)$ as in Def. \ref{l-infinity}.

* For each morphism $f\colon X \to Y$, we define $l^\infty(f)\colon l^\infty(Y) \to l^\infty(X)$ by $Supp(l^\infty(f)(p)) = f^\dagger \circ Supp(p) $.

\end{theorem}
(Any ultraweakly continuous $\dagger$-homomorphism is completely determined by its values on projection operators.)

This functor also maps coproducts in $qSet$ to products in $\mathrm{W}^*$. Thus, we have that
$$
l^\infty(X + Y) \cong l^\infty(X) \oplus l^\infty(Y), \qquad \qquad l^\infty(X \times Y) \cong l^\infty(X) \otimes l^\infty(Y).
$$

We also have a one-to-one correspondence between maps $X \to \mathrm{Inc}(\mathbb{R})$ and [[self-adjoint operator|self-adjoint operators]] [[affiliated operator|affiliated]] with $l^\infty(X)$.

\begin{theorem}
Let $\mathcal{M} \subseteq \mathcal{B}(\mathcal{H})$ be a von Neumann algebra. The following are equivalent:

1. $\mathcal{M}$ is in the [[essential image]] of the contravariant functor $l^\infty\colon qSet \to \mathrm{W}^*$,

1. $\mathcal{M} \cong \bigoplus^{l^\infty}_{i \in I} M_{n_i}(\mathbb{C})$ for some [[indexed family]] of positive integers $\{n_i\}_{i \in I}$,

1. every von Neumann subalgebra of $\mathcal{M}$ is atomic,

1. every [[self-adjoint operator]] in $\mathcal{M}$ has an [[Hilbert space|orthonormal basis]] of [[eigenvector|eigenvectors]] in $\mathcal{H}$,

1. the group of [[unitary operator|unitaries]] in $\mathcal{M}$ is compact in the [[von Neumann algebra|ultraweak topology]].

\end{theorem}

Von Neumann algebras of this kind are sometimes called hereditarily atomic, referring to condition 3.

Overall, we have an [[equivalence of categories|equivalence]] of [[symmetric monoidal category|symmetric monoidal categories]] between the [[opposite category]] $qSet^{op}$ and the [[full subcategory]] of hereditarily atomic von Neumann algebras. In effect, this generalizes the familiar equivalence between $Set^{op}$ and the category of [[complete Boolean algebra|complete atomic Boolean algebras]]. The projection operators in a von Neumann algebra form a [[complete lattice|complete]] [[orthomodular lattice]], which is a Boolean algebra iff the von Neumann algebra is commutative.

The material in this section is mostly from [Kornell 2020](#Kornell20) and [Chirvasitu 2025](#Chirvasitu25).

## Quantum sets as bundles

In mild paraphrase (following the discussion at *[[dependent linear type]]* and *[[quantum circuits via dependent linear types]]*):

* **quantum sets** are  [[indexed sets]] of [[finite-dimensional Hilbert spaces]] --- hence finite-[[rank of a vector bundle|rank]] [[Hilbert bundle|Hilbert]]-[[vector bundles]] over [[discrete topological spaces]] regarded as a [[sets]] --- and regarded as equipped with the [[external tensor product]] $\boxtimes$ [of vector bundles](VectBund#TensorMonoidalStructure);

* a **[[quantum relation]]** between quantum sets $(x \colon X) \times \mathscr{H}_x$ and $(x' \colon X') \times \mathscr{H}'_x$ is a [[monomorphism]] from a quantum set $\big((x,x') \colon X \times X'\big) \times \mathscr{R}_{(x,x')}$ to $\mathscr{H}^\ast_\bullet \boxtimes \mathscr{H}'_\bullet$:

  $$
    (x,x') \colon X \times X'
    \;\;\;
    \vdash
    \;\;\;
    \mathscr{R}_{(x,y)}
    \hookrightarrow
    \mathscr{H}^\ast_{(x,y)} 
      \otimes
    \mathscr{H}^'_{(x,y)} 
  $$

With [[composition]] the evident [[matrix multiplication]] ([Kornell 2020 (5)](#Kornell20)), quantum relations between quantum sets form a [[category]] $qRel$, which is a [[dagger-compact category]]. 

As such, this serves as [[categorical semantics]] for [[quantum programming languages]] like [[Quipper]] equipped with term recursion, via [[quantum CPOs]] ([Kornell, Lindenhovius & Mislove 2021](#KornellLindenhoviusMislove21)).

## Related concepts

* [[quantum CPO]]

## References

* {#PodlesWoronowicz90} [[Piotr Podleś]], [[S. L. Woronowicz|Stanisław Lech Woronowicz]], *Quantum deformation of Lorentz group*, Comm. Math. Phys. **130** (1990).

* {#KuperbergWeaver12} [[Greg Kuperberg]], [[Nik Weaver]]: *A von Neumann Algebra approach to quantum metrics*,  Mem. Amer. Math. Soc. **215** (2012) &lbrack;[arXiv:1005.0353](https://arxiv.org/abs/1005.0353), [ams:memo-215-1010](https://bookstore.ams.org/memo-215-1010)&rbrack;

* {#Weaver12} [[Nik Weaver]], *Quantum relations*, Mem. Amer. Math. Soc. **215** (2012) &lbrack;[arXiv:1005.0354](https://arxiv.org/abs/1005.0354), [ams:memo-215-1010](https://bookstore.ams.org/memo-215-1010)&rbrack;

* {#DeCommerKasprzakSkalskiSoltan18} Kenney De Commer, Paweł Kasprzak, Adam Skalski, Piotr M. Sołtan: *Quantum actions on discrete quantum spaces and a generalization of Clifford's theory of representations*, Israel J. Math. **226** (2018).

* {#Kornell20} [[Andre Kornell]]: *Quantum Sets*, J. Math. Phys. **61** 102202 (2020) &lbrack;[doi:10.1063/1.5054128](https://doi.org/10.1063/1.5054128)&rbrack;

* {#KornellLindenhoviusMislove21} [[Andre Kornell]], [[Bert Lindenhovius]], [[Michael Mislove]], §2 in: *Quantum CPOs*, EPTCS **340** (2021) 174-187 &lbrack;[arXiv:2109.02196](https://arxiv.org/abs/2109.02196), [doi:10.4204/EPTCS.340.9](https://doi.org/10.4204/EPTCS.340.9)&rbrack;
  > (in the context of [[quantum CPOs]])

* {#KornellLindenhoviusMislove22} [[Andre Kornell]], [[Bert Lindenhovius]], [[Michael Mislove]], *A category of quantum posets*, Indag. Math. **33** (2022).

* {#Kornell24} [[Andre Kornell]], *Discrete quantum structures II: Examples*, J. Noncommut. Geom. **18** (2024).

* {#Chirvasitu25} [[Alexandru Chirvasitu]], *Spans of quantum-inequality projections*, J. Math. Phys. **66** (2025), [arxiv:2504.01746](https://arxiv.org/abs/2504.01746).

* {#JencaLindenhovius25} Gejza Jenča, [[Bert Lindenhovius]],  *Monoidal quantaloids* (2025), [arXiv:2504.18266](https://arxiv.org/abs/2504.18266).

* {#ChirvasituKornell25} [[Alexandru Chirvasitu]], [[Andre Kornell]], *A new characterization of Kac-type discrete quantum groups* (2025), [arXiv:2511.20958] (https://arxiv.org/abs/2511.20958).



[[!redirects quantum sets]]

