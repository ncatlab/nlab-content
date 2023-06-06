+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

\tableofcontents

\section{Definition}

\begin{definition}\label{PointedAbelianGroups}
A **pointed abelian group** is an [[abelian group]] $(A, +, 0, -)$ equipped with the [[structure|choice]] of an [[element]] $1 \in A$. A [[homomorphism]] of pointed abelian groups is a homomorphism of [[underlying]] groups which preserves the choice of the extra points.
\end{definition}

\begin{remark}
Pointed abelian groups are "pointed" in the sense of *[[pointed objects in a monoidal category]]*, in that the choice of an element $1 \in A$ is equivalently the choice of a [[homomorphism]] $\mathbb{Z} \longrightarrow A$ out of the additive group of [[integers]] (which is fixed by its [[image]] of $1 \in \mathbb{Z}$).

Therefore the [[category]] of pointed abelian groups is equivalently the [[coslice category]] $Ab^{\mathbb{Z}/}$ of [[Ab]] under $\mathbb{Z}$.
\end{remark}

\begin{remark}\label{AsCosliceObjects}
The additive [[neutral element]] $0 \in A$ is *not* actually needed in the definition of apointed abelian groups (Def. \ref{PointedAbelianGroups}): Pointed abelian groups could equally be defined as [[pointed set|pointed]] [[commutative semigroup|commutative]] [[invertible semigroups]], hence as [[commutative semigroups]] $(A, +)$ equipped with an element $1 \in A$ and a [[function]] $- \colon A \to A$ such that for all [[elements]] $a \in A$ and $b \in A$, $a + b + (-b) = a$. 

From [[commutativity]] and [[associativity]] one may derive the other three invertibility properties for an [[invertible semigroup]]: $a + (-b) + b = a$, $b + (-b) + a = a$, and $(-b) + b + a = a$. The element $1 + (-1)$ is both left [[unit|unital]] and right unital with respect to the binary operation $+$, so by defining $0 \coloneqq 1 + (-1)$, $A$ becomes an [[abelian group]] $(A, +, 0, -)$ with an additional point $1 \in A$; hence a pointed abelian group. 
\end{remark}

\section{Examples}

\begin{example}\label{TrivialPointing}
Every [[abelian group]] becomes a pointed abelian group (Def. \ref{PointedAbelianGroups}) by taking the point to be the [[neutral element]] $0$. Since the neutral element $0$ is necessarily preserved by an [[group homomorphism]], this constitutes a [[full subcategory]]-inclusion
$$
  Ab \hookrightarrow Ab^{\mathbb{Z}/}
  \,.
$$
\end{example}


On the other hand:
\begin{example}
The notation $1 \in A$ is motivated from the case of [[rings]] $(R,0,+,1,\cdot)$, [[underlying]] which is the pointed abelian group $(R,0,+,1)$ with the "point" being the ring's [[unit]] element $1 \in R$. 
\end{example}


\section{Properties}

\begin{remark}
Despite the inclusion Exp. \ref{TrivialPointing}, the [[category]] of pointed abelian groups (Def. \ref{PointedAbelianGroups}) is not [[equivalence of categories|equivalent]] to the [[category of abelian groups]] ($\mathrm{Ab}$): 

In [[Ab]], the [[initial object]] and [[terminal objects]] are the same, both are given by the [[trivial group]]. However, in the category of pointed abelian groups, while the [[terminal object]] is still the [[trivial group]], the [[initial object]] is the additive group [[integers]] $\mathbb{Z}$ (manifestly so from Rem. \ref{AsCosliceObjects}). In this, the category of pointed abelian groups has more in common with the categories [[Ring]] and [[CRing]] of [[rings]] and of [[commutative rings]], respectively.
\end{remark}


\section{Related concepts}

* [[pointed module]]

* [[pointed object in a monoidal category]]

* [[commutative invertible semigroup]]

* [[abelian group]]

* [[Tarski group]]

* [[lattice]]

## References

* W. Edwin Clark, Xiang-dong Hou, *Galkin Quandles, Pointed Abelian Groups, and Sequence A000712* &lbrack;[arXiv:1108.2215](https://arxiv.org/abs/1108.2215)&rbrack;

* A. M. Nurakunov, *Quasivariety Lattices of Pointed Abelian Groups*, Algebra and Logic **53** (2014) 238–257 &lbrack;[doi:10.1007/s10469-014-9286-5](https://doi.org/10.1007/s10469-014-9286-5)&rbrack;

[[!redirects pointed abelian group]]
[[!redirects pointed abelian groups]]

[[!redirects category of pointed abelian groups]]

[[!redirects pointed commutative invertible semigroup]]
[[!redirects pointed commutative invertible semigroups]]

[[!redirects category of pointed commutative invertible semigroups]]