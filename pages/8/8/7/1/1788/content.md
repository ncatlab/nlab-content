
Which can be restated in terms of representable profunctors as follows.
A cwf consists of

1. a category $C$,
2. a presheaf $Ty : \hat C$ of types in context.
3. a presheaf $Tm : \widehat {\int Ty}$ of typed terms in context.
4. a functor $ext : \widehat {\int Ty} \to C$ of context extension that represents the profunctor ${\int Tm}(-,ty=) \odot {\int Tm}(ctx(ty(-)),=) : \int Ty &#8696; C$ where $ty : \int Tm \to \int Ty$ and $ctx : \int Ty \to C$ are the projections of the [[Grothendieck construction]].

Writing the profunctor as P, it is equivalent to the following definition:

$$P(\Delta, (\Gamma, A)) = (\gamma : \Delta \to \Gamma) \times (a : Tm(\Gamma, A[\gamma]))$$

then the universal property of the context extension is that there is a natural isomorphism $\Delta \to ext(\Gamma, A) \cong P(\Delta,(\Gamma,A))$




+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a group $G\;$, the **theory of G-torsors** is the logical theory whose models in a category $\mathcal{C}$ are the [[torsor|G-torsors]].


## Definition

Let $G$ be a [[group]]. The _theory of G-torsors_ $\mathbb{T}_G$ is the [[geometric theory]] over the signature with one sort $U$, a set of unary functions symbols ${g\in G}$ and the following axiom scheme:

$$
\begin{aligned}
\top & \vdash (g_i g_j)u=g_i(g_j u)\quad\text{for all}\; g_i,g_j
\\ 
\top&\vdash \exists u\; u\epsilon U \quad\text{(U is inhabited)}
\\
g_{i}u = g_{j}u &\vdash \bot\quad \text{for all pairs}\;g_i\neq g_j\quad\text{(G acts freely)}
\\
\top &\vdash \exists x \bigvee_{g\in G} gx=y\quad \text{(G acts transitively)}\quad .
\end{aligned}
$$

## Properties

Let $G$ be a group in $Set$ and $\mathcal{E}$ be a [[Grothendieck topos]] with $\Delta\dashv \Gamma:\mathcal{E}\to Set$. Recall that a _G-torsor_ over $\mathcal{E}$ is defined as an object $T$ of $\mathcal{E}$ together with a left action $\mu:\Delta(G)\times T\to T$ such that $T\to 1$ is epi and $\mu$ induces an isomorphism $(\mu,\pi_2):\Delta(G)\times T\to T \times T$.

The category of models of $\mathbb{T}_G$ in $\mathcal{E}$ is the category $Tor(\mathcal{E},G)$ of G-torsors over $\mathcal{E}$ and, furthermore, $Tor(\mathcal{E},G)\cong Hom_{Top}(\mathcal{E},Set^{G^{op}})$ i.e. $Set^{G^{op}}$ is the [[classifying topos]] $Set[\mathbb{T}_G]$ of $\mathbb{T}_G$.

It is a standard fact that Boolean presheaf toposes correspond precisely to toposes $Set^{\mathcal{G}^{op}}$ of actions of groupoids $\mathcal{G}$ whereas toposes $Set^{G^{op}}$ of group actions correspond to the connected toposes among these whence the toposes of the form $Set^{G^{op}}$ can be characterized as the connected Boolean presheaf toposes.

This affords a logical characterization of $\mathbb{T}_G$ as a **complete Boolean theory of presheaf type** since Boolean presheaf toposes are atomic and atomic toposes are connected precisely when they are [[two-valued topos|two-valued]] which is equivalent to the completeness of the classified theory (See at [[two-valued topos]] and [[theory of presheaf type]] for the logical terminology). To sum up: toposes $Set^{G^{op}}$ of group actions are up to equivalence precisely the classifying toposes of complete Boolean theories of presheaf type.[^finite]

[^finite]: Looking at $\mathbb{T}_G$ it seems reasonable to conjecture that the toposes of _finite_ group actions correspond precisely to the classifying toposes of the finitely presentable complete Boolean theories of presheaf type i.e. those with finitely many function symbols and a finite list of axioms.


## Related entries

* [[torsor]]

* [[theory of objects]]

* [[theory of decidable objects]]

* [[classifying topos]]

## References

The syntactic theory is explicitly stated p.42 in

* {#Lawvere75}[[F. William Lawvere]], _Variable sets etendu and variable structure in topoi_ , Lecture notes University of Chicago 1975.

The "semantic" side was well known to the Grothendieck school and its elements are nicely exposed e.g. in section VIII.2 of 

* {#MM94} [[Saunders Mac Lane|S. Mac Lane]], [[I. Moerdijk|Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994.



[[!redirects Theory of G-torsors]]
[[!redirects theory of torsors]]