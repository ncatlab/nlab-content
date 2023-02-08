
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



\tableofcontents

## Idea 

A [[double category]] consists of [[objects]], two [[classes]] of [[1-morphisms]] ([[horizontal morphism|horizontal and vertical]]), and [[2-morphisms]] between these.  

The idea behind a right-connected double category is that each vertical morphism $f \colon A \nrightarrow B$ has an *[[underlying]]* horizontal morphism $U f \colon A \rightarrow B$.
Therefore, the vertical morphisms should be understood as horizontal morphisms with certain [[properties]] or equipped with additional [[structure]].
Correspondingly, the main examples of right-connected double categories arise from [[orthogonal factorization systems]] or [[algebraic weak factorization systems]], where the vertical morphisms are in the *right class* of the factorization system. 

The concept of a right-connected double category is unrelated to the notion of a "[[connection on a double category]]". 

## Definition 

A [[double category]] $\mathbb{D} = (D_{0}, D_{1})$ is *right-connected* if its [[identity morphisms|identity]]-assigning map $id \colon D_{0} \rightarrow D_{1}$ is [[right adjoint]] to its [[codomain]]-assigning map $cod \colon D_{1} \rightarrow D_{0}$. 

Dually, a double category $\mathbb{D} = (D_{0}, D_{1})$ is *left-connected* if its [[identity morphisms|identity]]-assigning map $id \colon D_{0} \rightarrow D_{1}$ is [[left adjoint]] to its [[domain]]-assigning map $dom \colon D_{1} \rightarrow D_{0}$. 

\begin{remark}
This definition makes sense for any pseudo [[category object]] in a [[2-category]].
\end{remark}

Let $\mathbf{RcDbl}$ denote the [[2-category]] of right-connected double categories, *unitary* [[double functors]] (those which preserve vertical identities strictly), and [[vertical transformation|horizontal transformations]].

### Unpacking the definition

We can unpack the definition of right-connectedness as follows. 
Let $\rho \colon 1_{D_{1}} \Rightarrow id \circ cod$ denote the [[unit of an adjunction|unit]] of the adjunction $cod \dashv id$, and let the [[counit of an adjunction|counit]] be the identity natural transformation by the axioms of an [[internal category]]. 
Given a vertical morphism $f \colon A \nrightarrow B$ in $\mathbb{D}$, the component of the unit may be depicted as follows: 
\begin{tikzcd}
A 
\arrow[rd, phantom, "\rho_{f}"]
\arrow[d, "f"', "\bullet"{anchor=center}]
\arrow[r, "Uf"]
& B
\arrow[d, "id_{B}", "\bullet"{anchor=center}]
\\
B
\arrow[r, "1_{B}"']
& B
\end{tikzcd}
The [[triangle identities]] of an adjunction imply that: 

1. the bottom boundary of $\rho_{f}$ is an identity morphism;

2. the component of $\rho$ at an identity vertical morphism $id_{A} \colon A \nrightarrow A$ is the identity cell on $A$.

Given a cell $\alpha$ in $\mathbb{D}$, naturality of $\rho$ states that the cells 
  \begin{tikzcd}
    A
    \arrow[r, "h"]
    \arrow[d, "\bullet"{anchor=center}, "f"']
    \arrow[rd, phantom, "\alpha"]
    & C
    \arrow[d, "\bullet"{anchor=center}, "g"]
    \arrow[r, "Ug"]
    \arrow[rd, phantom, "\rho_{g}"]
    & D
    \arrow[d, "\bullet"{anchor=center}, "id_{D}"]
    \\
    B
    \arrow[r, "k"']
    & D
    \arrow[r, "1_{D}"']
    & D
    \end{tikzcd}
and 
    \begin{tikzcd}
    A
    \arrow[r, "Uf"]
    \arrow[d, "\bullet"{anchor=center}, "f"']
    \arrow[rd, phantom, "\rho_{f}"]
    & B
    \arrow[d, "\bullet"{anchor=center}, "id_{B}"]
    \arrow[r, "k"]
    \arrow[rd, phantom, "id_{k}"]
    & D
    \arrow[d, "\bullet"{anchor=center}, "id_{D}"]
    \\
    B
    \arrow[r, "1_{B}"']
    & B
    \arrow[r, "k"']
    & D
    \end{tikzcd}
are equal. 

## Examples

\begin{example}\label{horizontal-double-category}
For each category $C$, the horizontal double category $\mathbb{H}(C)$ ---whose objects and horizontal morphisms come from $C$, and whose vertical morphisms and cells are identities --- is right-connected. 

Viewing double categories as [[internal categories]] in $\mathbf{Cat}$, we can see that $\mathbb{H}(C) = (C, C)$ is the discrete internal category on $C$, 
with [[identity morphisms|identity]]-assigning map and  [[codomain]]-assigning map are both the [[identity functor]] on $C$ and therefore adjoint to each other. 
\end{example}

\begin{example}\label{double-category-of-squares}
For each category $C$, the [[double category of squares]] $\mathbb{S}q(C)$ is both right-connected and left-connected. 
\end{example}

If we modify the above example to consider only [[pullback squares]] or [[pushout|pushout squares]], then it is no longer right-connected or left-connected; we must also modify the vertical morphisms. 

\begin{example}
Consider a category $C$ equipped with a [[wide subcategory]] $M$ of [[monomorphisms]] stable under pullback along morphisms in $C$.
The double category $\mathbb{P}b(C, M)$ --- whose objects and horizontal morphisms come from $C$, whose vertical morphisms comes from $M$, and whose cells are pullback squares --- is left-connected. 

Dually, consider a category $C$ equipped with a wide subcategory $E$ of [[epimorphisms]] stable under pushout along morphisms in $C$.
The double category $\mathbb{P}o(C, E)$ --- whose objects and horizontal morphisms come from $C$, whose vertical morphisms comes from $E$, and whose cells are pushout squares --- is right-connected. 
\end{example}

\begin{example}
Given a category $C$, let $\mathbb{S}plEpi(C)$ denote the double category whose objects and horizontal morphisms come from $C$, whose vertical morphisms are [[split epimorphisms]] with a chosen [[section]], and whose cells are squares
\begin{tikzcd}
A
\arrow[d, shift left = 2, "f"]
\arrow[r, "h"]
& C
\arrow[d, shift left = 2, "g"]
\\
B
\arrow[u, shift left = 2, "s"]
\arrow[r, "k"']
& D
\arrow[u, shift left = 2, "t"]
\end{tikzcd}
such that $k \circ f = g \circ h$ and $h \circ s = t \circ k$. 
This double category is right-connected, since for each vertical morphism there is a cell:
\begin{tikzcd}
A
\arrow[d, shift left = 2, "f"]
\arrow[r, "f"]
& B
\arrow[d, shift left = 2, "1_{B}"]
\\
B
\arrow[u, shift left = 2, "s"]
\arrow[r, "1_{B}"']
& B
\arrow[u, shift left = 2, "1_{B}"]
\end{tikzcd}
If $C$ has pullbacks, the [[codomain]]-assigning map of this double category is not only a left adjoint, but also a [[Grothendieck fibration]], namely, the [[fibration of points]]. 
\end{example}

\begin{example}\label{awfs}
For each [[algebraic weak factorization system]] $(C, R, L)$ on a category $C$, the double category $R$-$\mathbb{A}lg$ of $R$-algebras is right-connected. 
\end{example}

## Properties

\begin{proposition}
If a double category is right-connected, then it has all [[cotabulators|1-cotabulators]]. 
\end{proposition}

\begin{proposition}\label{double-functor-U}
If $\mathbb{D} = (D_{0}, D_{1})$ is a right-connected double category, 
then there is a [[double functor]] $U \colon \mathbb{D} \rightarrow \mathbb{S}q(D_{0})$ with assignment given below. 
\begin{tikzcd}
A
\arrow[r, "h"]
\arrow[d, "\bullet"{anchor=center}, "f"']
\arrow[rd, phantom, "\alpha"]
& C
\arrow[d, "\bullet"{anchor=center}, "g"]
& \phantom{X}
\arrow[d, phantom, "\longmapsto"]
& A
\arrow[r, "h"]
\arrow[d, "Uf"']
& C
\arrow[d, "Ug"]
\\
B
\arrow[r, "k"']
& D
& \phantom{X}
& B
\arrow[r, "k"']
& D
\end{tikzcd} 
\end{proposition}
A proof can be found in [Bourke & Garner, Section 3.5](#BourkeGarner2016a).

Let $Obj \colon \mathbf{RcDbl} \rightarrow \mathbf{Cat}$ denote the [[2-functor]] which assigns a double category $\mathbb{D} = (D_{0}, D_{1})$ to 
its category $D_{0}$ of objects and horizontal morphisms. 
Let $\mathbb{H} \colon \mathbf{Cat} \rightarrow \mathbf{RcDbl}$ be the $2$-functor which assigns each category to its horizontal double category (see Example \ref{horizontal-double-category}), and let $\mathbb{S}q \colon  \mathbf{Cat} \rightarrow \mathbf{RcDbl}$ be the $2$-functor which assigns each category to its double category of squares (see Example \ref{double-category-of-squares}).

\begin{proposition}
There is an [[adjoint triple]] of $2$-functors: 
\begin{tikzcd}
\mathbf{RcDbl} 
\arrow[r, "\mathrm{Obj}" description]
& \mathbf{Cat}
\arrow[l, phantom, shift right = 5, "\bot"]
\arrow[l, phantom, shift left = 5, "\bot"]
\arrow[l, "\mathbb{H}"', shift right = 8, hook']
\arrow[l, "\mathbb{S}q", shift left = 8, hook']
\end{tikzcd}
\end{proposition}
\begin{proof}(*Idea*)
The component of the counit of the adjunction $\mathbb{H} \dashv \mathrm{Obj}$ at a right-connected double category $\mathbb{D} = (D_{0}, D_{1})$ is given by the double functor $\mathbb{H}(D_{0}) \rightarrow \mathbb{D}$ determined by the pair of functors $(1 \colon D_{0} \rightarrow D_{0}, id \colon D_{0} \rightarrow D_{1})$. 
The component of the unit of the adjunction $\mathrm{Obj} \dashv \mathbb{S}q$ is given in Proposition \ref{double-functor-U}. 
\end{proof}

Let $\mathbf{AWFS}_{lax}$ denote the $2$-category of [[algebraic weak factorization systems]].
There is a $2$-functor $\mathbf{AWFS}_{lax} \rightarrow \mathbf{RcDbl}$ which assigns each algebraic weak factorisation system to its double category of $R$-algebras (see Example \ref{awfs}). 
The following theorem characterises the [[essential image]] of the this $2$-functor. 

First, given a right-connected double category $\mathbb{D} = (D_0, D_1)$, 
let $U_{1} \colon D_{1} \rightarrow Sq(D_{0})$ denote the functor underlying the double functor $U \colon \mathbb{D} \rightarrow \mathbb{S}q(D_{0})$ in Proposition \ref{double-functor-U}. 

\begin{theorem}
The $2$-functor $\mathbf{AWFS}_{lax} \rightarrow \mathbf{RcDbl}$ has in its essential image exactly those right-connected double categories 
$\mathbb{D} = (D_0, D_1)$ for which the functor $U_{1} \colon D_{1} \rightarrow Sq(D_{0})$ is [[monadic|strictly monadic]]. 
\end{theorem}
The proof combines the results in Theorem 6 and Proposition 11 of [Bourke & Garner](#BourkeGarner2016a).

## References

The notion was first defined in Section 3.5 of:

 * {#BourkeGarner2016a} [[John Bourke]], [[Richard Garner]], _Algebraic weak factorisation systems I: Accessible AWFS_, Journal of Pure and Applied Algebra, **220**, 2016 ([arXiv:1412.6559](https://arxiv.org/abs/1412.6559), [doi:10.1016/j.jpaa.2015.06.002](https://doi.org/10.1016/j.jpaa.2015.06.002))

Further discussion of right-connected double categories appears in Section 2.5 of: 

 * {#BourkeGarner2016b} [[John Bourke]], [[Richard Garner]], _Algebraic weak factorisation systems II: Categories of weak maps_, Journal of Pure and Applied Algebra, **220**, 2016 ([arXiv:1412.6560](https://arxiv.org/abs/1412.6560), [doi:10.1016/j.jpaa.2015.06.003](https://doi.org/10.1016/j.jpaa.2015.06.003))

[[!redirects right-connected double categories]]
[[!redirects left-connected double category]]
[[!redirects left-connected double categories]]