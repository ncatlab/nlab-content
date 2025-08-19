+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


\tableofcontents

## Idea 

For $G$ a [[locally compact Hausdorff space|locally compact Hausdorff]] [[topological group]], with $C_c(G)$ denoting its [[algebra of functions|algebra of]] [[compact support|compactly supported]] [[continuous functions]] from $G$ to $\mathbb{R}$,  a _Haar integral_ $\int_G $ is a [[continuous map|continuous]] [[linear map]] $C_c(G) \rightarrow \mathbb{R}$ to the [[real numbers]] which is [[invariant]] under the obvious [[group action]] of $G$ on $C_c(G)$. It turns out that there exists a unique such [[integral]], up to a scalar multiple. The [[Riesz representation theorem]] then allows one to conclude the existence of a unique _Haar measure_, which is a $G$-invariant [[Borel measure]] on $G$.

The archetypal example of Haar measure is the [[Lebesgue measure]] on the (additive group underlying) [[Cartesian space]] $\mathbb{R}^n$.

## Definition

Let $G$ be a [[locally compact Hausdorff space|locally compact Hausdorff]] [[topological group]]. Let $C_c(G)$ denote the [[vector space]] of [[continuous map|continuous]] [[real numbers|real-valued]] [[functionals]] with [[compact support]] on $G$. This is a [[locally convex topological vector space]] where the locally convex structure is specified by the family of [[seminorms]] 

$$
  \rho_K(f) 
   \;=\; 
  \sup_{x \in K} {|f(x)|}
  \,,
$$ 

where $K$ ranges over [[compact subsets]] of $G$. Recall that a *[[Radon measure]]* on $G$ may be described as a continuous linear functional 

$$
  \int_G 
    \,\colon\, 
  C_c(G) \to \mathbb{R}
  \,.
$$ 

Such a Radon measure defines a [[measure]] $\mu$ on the [[sigma-algebra|$\sigma$-algebra]] of [[Borel sets]] in the usual sense of [[measure theory]], where 

$$
  \mu(B) 
   \;=\; 
  sup 
  \Big\{
     \textstyle{\int_G} f 
       \,\colon\, 
     supp(f) = K \subseteq B,\, \rho_K(f) = 1 
  \Big\}
  \,.
$$ 


In this context, a (left) **Haar integral** on $G$ is a nonzero such linear functional $\int_G$ such that
$$ 
  \int_G f 
   \;\geq\; 0 
   \;\;\text{when}\; f \geq 0
$$
$$ 
  \int_G f^g 
    \;=\; 
  \int_G f
$$
for each $f \in C_c(G)$ and each $g \in G$, where $f^g \colon G \rightarrow \mathbb{R}$ sends $x$ to $f(g x)$.

Correspondingly, a (left) **Haar measure** on $G$ is a nonzero Radon measure $\mu$ such that 

$$
  \mu(g B) 
    \;=\; 
  \mu(B)
$$ 

for all $g \in G$ and all Borel sets $B$. 

## Properties

### Existence and Uniqueness

Any locally compact Hausdorff topological group $G$ admits a Haar integral (and therefore Haar measure) that is unique up to scalar multiple. This result was first proven by [[André Weil]]. Proofs may be found in [Alfsen 1963](#Alfsen63) ([[constructive mathematics|consructive]]) and [Rubinstein-Salzedo 2004](#Rubinstein-Salzedo04). 

A particular argument for the case of a compact Hausdorff topological group was provided by [Bader 2020](#Bader20), which is what we follow now:
 
\begin{theorem}
Let $G$ be a compact Hausdorff topological group. Write $C^0(G)$ for the Banach space of continuous $\mathbb{R}$-valued functions on $G$. There is a unique $G$-invariant $\mathbb{R}$-linear map of Banach-spaces $\int \colon C^0(G) \rightarrow \mathbb{R}$ such that $0 \leq \int f^2$ for all $f  \in C^0(G)$.
\end{theorem}

\begin{proof}
Consider the set $S$ of subsets $C$ of $C^0(G)^*$ which satisfy

(1) ($G$-invariance) for all functionals $\phi$ in $C$, the continuous functional $\phi^g$ sending $f$ to $\phi(f^{g^{-1}})$ is contained in $C$.

(2) (compactness) The subtopology on $C$ is compact.

(3) (convexity) for elements $\phi_1, \ldots, \phi_n$ in $C$ and $a_1, ..., a_n \in [0,\infty)$ such that $\sum_{i = 1}^n a_i = 1$, $\sum_{i = 1}^n a_i \phi_i \in C$.

(4) (nonemptiness) there is an element of $C^0(G)^*$ contained in $C$.

Claim 1: $S$ is nonempty. 

Recall that the [[Hahn-Banach theorem]] theorem for a Banach space with squared Minkowski seminorm $\text{sup}_{i \in I} \phi_i \overline{\phi_i}$ for continuous functionals $\{ \phi_i \}_{i \in I}$ provides the existence of a continuous functional $\phi : C^0(G) \rightarrow \mathbb{R}$. $\{ \phi \}$ satisfies (4) and (2) but possibly not (3) or (1).

The $\infty$-norm topology on $C^0(G)$ given by the squared Minkowski seminorm $\text{sup}_{g \in G} ev_g \overline{ev_g}$ is equivalently described as the compact open topology on continuous functions from $G$ to $\mathbb{R}$. 

For any $f \in C^0(G)$, $\{ f \} \subset C^0(G)$ is closed because it is a single point in a Hausdorff space. Write $\mu_{g^{-1}} : G \rightarrow G$ for the continuous function sending $h$ to $hg^{-1}$. For a continuous function $f : G \rightarrow \mathbb{R}$, write $f^g : G \rightarrow \mathbb{R}$ for $f \circ \mu_{g^{-1}}$.

The composition

$$
  \text{ev} \circ 
  \Big(1 \times 
    \big(\mu \circ 
      (1 \times \text{Inv})
    \big)
  \Big) 
  \;\colon\; 
  [G,\mathbb{R}] \times G \times G 
    \longrightarrow 
  \mathbb{R}
$$

is continuous, from which we get that

$$
  [G,\mathbb{R}] \times G 
    \longrightarrow 
  [G,\mathbb{R}]
$$


is continuous, using the calculus of [[mates]] for [[exponentiable objects]] in topological spaces, along with the fact that a compact space is exponentiable. $[G,\mathbb{R}] \times G \rightarrow [G,\mathbb{R}]$ sending $(f,g)$ to the continuous function $f^g$ sending $h$ to $f(hg^{-1}) = f \circ \mu_{g^{-1}} (h)$ is continuous. It follows that image of $\{ f \} \times G$ in $[G,\mathbb{R}]$ is compact. This is the $G$-orbit $\{ f^g : g \in G \}$. $\{ f^g : g \in G \}$ satisfies (1) (2) and (4), but possibly not (3).

The Krein-Smulian theorem, applied to $G \cdot f$ which is compact in the Banach space $C^0(G)^*$, gives that the convex hull $\overline{G \cdot f}$ of $G \cdot f$ is compact in the weak topology on $C^0(G)^*$ (not to be confused with the weak${}^*$ topology on $C^0(G)^*$). We can conclude that $\overline{G \cdot f}$ is $G$-invariant, compact (relative to the weak topology), convex, and nonempty. Therefore $\overline{G \cdot f} \in S$.

Claim 2: given a chain $\{ C_n \}_{n \in \mathbb{N}}$ of elements $C_n \in S$ such that $C_{n+1} \subset C_n$, $\cap_{n \in \mathbb{N}} C_n \in S$.

(1) ($G$-invariance) if $\phi \in \cap_{n \in \mathbb{N}} C_n$, then $\phi \in C_n$ for each $n \in \mathbb{N}$, so $\phi^g \in C_n$ for each $n \in \mathbb{N}$, so $\phi^g \in \cap_{n \in \mathbb{N}} C_n$.

(2) (compactness) $\cap_{n \in \mathbb{N}} C_n$ is closed so

(3) (convexity) $\cap_{n \in \mathbb{N}} C_n$ is closed so

(4) (nonemptiness) $C_n$ is a decreasing chain of compact subsets of a Hausdorff topological space, from which we can conclude that it is nonempty.

Claim 3: [[Zorn's Lemma]] for the case of the partial order defined on $S$ by which $C_1 \leq C_2$ if and only if $C_2 \subseteq C_1$ is satisfied because of claim 2 and claim 3. This implies that we may find a minimal element of $S$ in this collection, where $S$ is ordered where $A \leq B$ when $A \subset B$. 

Choose such an element $C$.

Claim 4: $C$ is a singleton.

The Krein-Milman theorem, applied to the compact, convex subset $C$ of $C^0(G)^*$ (again as a locally convex topological vector space under the weak topology), gives that $C$ is the convex hull of its extreme points.

The continuous group action of $G$ on $C$ sends the subspace $\text{Inext}(C)$ of inextremal points to itself, as the average $\sum_{i = 1}^n a_i f_i$ of $f_i$ with $a_i \neq 0$, $a_i \in (0,\infty)$, and $\sum_{i = 1}^n a_i$ remains an average with respect to the same weights $a_i \neq 0$, $a_i \in (0,\infty)$, with $\sum_{i = 1}^n a_i$:

$$
(a_1 f_1 + a_2 f_2)^g  = a_1 f_1^g + a_2 f_2^g
$$

Since $G$ acts by homeomorphisms on $C$, $G$ must send the subspace of extremal points $\text{Ext}(C)$ of $C$ to itself. Using again that $G$ acts by homeomorphisms, we can conclude that $\phi$ is extremal if and only if $\phi^g$ is extremal. 

For any $f \in \text{Inext}(C)$, one can construct an object in $S$ using the facts above (the compactness of any $G$-orbit and the resulting compactness of its convex hull $\tilde{C}$ within $C^0(X)^*$), and from that the inclusions $\{ f \} \subset \text{Inext}(C) \subsetneq C$ imply inclusions of the $G$-orbits $G \cdot \{ f \} \subset \text{Inext}(C) \subsetneq C$, which imply inclusions $\overline{G \cdot \{ f \}} \subset \text{Inext}(C) \subseteq C$, from which we can conclude that $C$ is not minimal, a contradiction!

Therefore $0 = \text{card}(\text{Inext}(C))$. This implies $1 = \text{card}(\text{Ext}(C))$, i.e. $C$ is a [[singleton]], and its unique element a $G$-invariant functional extending $f$.
\end{proof}


### Extensive and Intensive Properties

In Lawvere's thinking about [extensive and intensive quantities](intensive+or+extensive+quantity),
 
* $C(G)$ is a space of _intensive quantities_ on $G$.

* $[C(G), \mathbb{R}]_{\text{Ban}}$ is the space of _extensive quantities_ on $X$, where $\text{Ban}$ is the category of Banach spaces with bounded maps as maps. The Haar integral is the unique $G$-invariant element of this space of norm $1$.

* the [[integration]] map is the canonical [[evaluation]] pairing

  $$
    \int_G \;\colon\; C(G) \times [C(G), \mathbb{R}]_{\text{Ban}}  \longrightarrow \mathbb{R}
    \,.
  $$

If we suggestively write $\int_G f d \phi$ for $\int_G (f, \phi) = \phi(f)$, then $\int_G - d \phi$ becomes a way of writing $\phi$. In particular, choosing $\phi$ to be the Haar measure, we can write $\phi$ as $\int_G - d \phi$.

## Left and Right Haar Measures that Differ

The left and the right Haar measure may or may not coincide, groups for which they coincide are called **unimodular**.
Consider the matrix subgroup
$$
G := \left\{ \left.\, \begin{pmatrix} y & x \\ 0 & 1 \end{pmatrix}\,\right|\, x, y \in \mathbb{R}, y \gt 0  \right\}
$$
The left and right invariant measures are, respectively,
$$
  \mu_L = y^{-2} \,\mathrm{d}x \,\mathrm{d}y,\quad   \mu_R = y^{-1} \,\mathrm{d}x \,\mathrm{d}y
$$
and so G is not unimodular.

[[Abelian groups]] are obviously unimodular; so are [[compact Hausdorff space|compact]] groups and [[discrete topology|discrete]] groups.


## References

Textbook account:

* {#Bredon72} [[Glen Bredon]], Section 0.3 of: _[[Introduction to compact transformation groups]]_, Academic Press  (1972) &lbrack;[ISBN 9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf)&rbrack;

Proofs:

* {#Alfsen63} E. M. Alfsen: *A Simplified Constructive Proof of the Existence and Uniqueness of Haar Measure*, Mathematica Scandinavica **12**  (1963) &lbrack;[doi:10.7146/math.scand.a-10675](https://doi.org/10.7146/math.scand.a-10675)&rbrack;

* {#Rubinstein-Salzedo04} Simon Rubinstein-Salzedo: *On the existence and uniqueness of invariant measures on locally compact groups* (2004) &lbrack;[pdf](http://simonrs.com/HaarMeasure.pdf)&rbrack;

* {#Bader20} Uri Bader, MO answer (2020) &lbrack;[MO:a/351405](https://mathoverflow.net/a/351405/381)&rbrack;

See also:

* [[Uffe Haagerup]], Agata Przybyszewska: *Proper metrics on locally compact groups, and proper affine isometric actions on Banach spaces* &lbrack;[arXiv:math/0606794](https://arxiv.org/abs/math/0606794)&rbrack;

* Wikipedia: *[Haar measure](https://en.wikipedia.org/wiki/Haar_measure)*




[[!redirects Haar measure]]
[[!redirects Haar measures]]
[[!redirects haar measure]]
[[!redirects haar measures]]
