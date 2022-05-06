[[!redirects Haar measure]]

# Haar measure
* table of contents
{: toc}

## Idea 

If $G$ is a locally compact hausdorff [[topological group]], with $C_c(G)$ the algebra of compactly supported continuous functions from $C_c(G)$ to $\mathbb{R}$,  a _Haar integral_ $\int_G $ is a continuous linear map $C_c(G) \rightarrow \mathbb{R}$ which is invariant under the aparent action of $G$ on $C_c(G)$. It turns out that there exists a unique such integral, up to a scalar multiple.

The archetypal example of Haar measure is the [[Lebesgue measure]] on the (additive group underlying) [[cartesian space]] $\mathbb{R}^n$.

##Definition

Let $G$ be a locally compact hausdorff group. Let $C_c(G)$ denote the vector space of continuous real-valued functionals with compact support on $G$. This is a [[locally convex topological vector space]] where the locally convex structure is specified by the family of seminorms 

$$\rho_K(f) = \sup_{x \in K} |f(x)|$$ 

$K$ ranging over compact subsets of $G$. Recall that a [[Radon measure]] on $G$ may be described as a continuous linear functional 

$$\int_G : C_c(G) \to \mathbb{R}$$ 

This defines a measure $\mu$ on the $\sigma$-algebra of Borel sets in the usual sense of [[measure theory]], where 

$$\mu(B) = sup \{\int_G f : supp(f) = K \subseteq B, \rho_K(f) = 1\}$$ 

In this context, a (left) Haar integral on $G$ is a nonzero Radon measure $\mu$ such that
$$ \int_G f^g = \int_G f$$
for each $f \in C_c(G)$ and each $g \in G$, where $f^g : G \rightarrow \mathbb{R}$ sends $x$ to $f(gx)$.

Correspondingly, a **left Haar measure** on $G$ is a nonzero Radon measure $\mu$ such that 

$$\mu(g B) = \mu(B)$$ 

for all $g \in G$ and all Borel sets $B$. 

##Existence and Uniqueness

Any locally compact Hausdorff topological group $G$ admits a Haar integral (and therefore Haar measure) that is unique up to scalar multiple. This result was first proven by Weil. A proof by be found in these online [notes](http://simonrs.com/HaarMeasure.pdf) by Rubinstein-Salzedo. 
 
We here give a lesser known proof of the existence of the Haar integral, specifically on compact hausdorff groups $G$, which uses convex sets and the Krein Milman theorem instead of measure theory. Let $G \text{-Ban}$ be the category of Banach representations of $G$. Objects in $G \text{-Ban}$ are banach spaces $X$ over $\mathbb{R}$ with a continuous action $G \times X \rightarrow X$. Maps in $G \text{-Ban}$ are bounded, $G$-equivariant maps. (Alternatively, $G \text{-Ban}$ can be viewed as a category of certain $\mathbb{R}[G]$-modules.) 

$C_c(G) = C(G)$ is such a Banach representation. We may view $\mathbb{R}$ as a Banach representation of $G$ as well, where $gz = z$ for each $z \in \mathbb{R}$ and each $g \in G$. $\mathbb{R}$ embeds into $C(G)$ as constant functions. We may then consider the exact sequence
$$0 \rightarrow \mathbb{R} \rightarrow C(G) \rightarrow C(G)/ \mathbb{R} \rightarrow 0$$

A Haar integral on the $G$-representation $C(G)$ is equivalently a retract $\int_G : C(G) \rightarrow \mathbb{R}$ for the injection $\mathbb{R} \rightarrow C(G)$. In other words, it is a function $\int_G : C(G) \rightarrow \mathbb{R}$ such that

$$ \int_G (f_1 + f_2) = \int_G f_1 + \int_G f_2  \forall f_1, f_2 \in C(G)$$
$$ \int_G a f = a \int_G f   \forall f \in C(G), a \in \mathbb{R}$$
$$ \int_G f^g = \int_G f \forall f \in C(G), g \in G$$
$$ \exists C \in  \mathbb{R}_{\geq 0 } :  \left| \left| \int_G f \right| \right| \leq C \int_G ||f||\forall  [G, \mathbb{C}]_{\text{Top}}$$
The last of these requirements, given the others, is equivalent to continuity of $\int_G$.

In some sense, we might wish to show that $\text{Ext}^1_{G \text{-Ban}}(C(G), \mathbb{R})$ vanishes; this would show that the sequence
$$0 \rightarrow \mathbb{R} \rightarrow C(G) \rightarrow C(G)/ \mathbb{R} \rightarrow 0$$
splits by the usual characterization of extensions via $\text{Ext}^1$. On further contemplation, it is sufficient to show that the trivial $G$-representation $\mathbb{R}$ is an injective object in $G \text{-Ban}$. This could be seen as an equivariant Hahn-Banach theorem.

**Proof:** We show that $\mathbb{R}$ is an injective object in $G \text{-Ban}$. Take an injection of Banach representations of $G$, $X \rightarrow Y$. Let $f : X \rightarrow \mathbb{R}$ be a map of Banach representations of $G$. By the (usual) Hahn-Banach theorem, there exists a functional $g : Y \rightarrow \mathbb{R}$ extending $f$, though it may lack $G$-invariance.

Consider the subset of all extensions of $f$ to $Y$. Let $S$ be the collection of $G$-invariant compact convex subsets of this set. $S$ contains the convex hull of $G g$, where $g$ is some chosen extension of $f$ to $Y$, so $S$ is nonempty. Using compactness and Zorn's lemma, we may find a minimal element of $S$ in this collection, where $S$ is ordered where $A \leq B$ when $A \subset B$. Call this element $H$. $H$ must be a singleton. If $H$ contains a point which is not extremal then it contains the convex hull of the orbit of that point, which would be a proper $G$-invariant compact convex subset of $H$ (see Krein Milman theorem).

Therefore $H$ is a singleton, and its unique element is a $G$-invariant functional extending $f$.

In particular, since $\mathbb{R}$ has been shown to be injective, the map $\text{Id}_{\mathbb{R}}  : \mathbb{R} \rightarrow \mathbb{R}$ lifts along the inclusion
$$0 \rightarrow \mathbb{R} \rightarrow C(G)$$

**Remark:** by the Riesz-Markov-Kakutani representation theorem, it follows that there is a unique Haar measure on $G$.

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

[[Abelian groups]] are obviously unimodular; so are [[compactum|compact]] groups and [[discrete topology|discrete]] groups.



[1]: https://arxiv.org/abs/math/0606794


[[!redirects Haar measure]]
[[!redirects Haar measures]]
[[!redirects haar measure]]
[[!redirects haar measures]]
