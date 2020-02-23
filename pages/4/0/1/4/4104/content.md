
# Haar measure
* table of contents
{: toc}

## Idea 

If $G$ is a [[topological group]], a _Haar measure_ is a translation-invariant measure on the [[Borel set]]s of $G$. The archetypal example of Haar measure is the [[Lebesgue measure]] on the (additive group underlying) [[cartesian space]] $\mathbb{R}^n$. 


## Definition 

The proper generality in which to discuss Haar measure is where the topological group $G$ is assumed to be [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]], and from here on we assume this. (For [[topological group]]s, the Hausdorff assumption is rather mild; it is equivalent to the $T_0$ separation condition. See the discussion at [[uniform space]].) 

Let $C_c(G)$ denote the vector space of continuous real-valued functionals with compact support on $G$. This is a [[locally convex topological vector space]] where the locally convex structure is specified by the family of seminorms 

$$\rho_K(f) = \sup_{x \in K} |f(x)|,$$ 

$K$ ranging over compact subsets of $G$. Recall that a [[Radon measure]] on $G$ may be described as a continuous linear functional 

$$\mu: C_c(G) \to \mathbb{R}$$ 

which is _positive_ in the sense that $\mu(f) \geq 0$ whenever $f \geq 0$. This defines a measure $\hat{\mu}$ on the $\sigma$-algebra of Borel sets in the usual sense of [[measure theory]], where 

$$\hat{\mu}(B) = sup \{\mu(f): supp(f) = K \subseteq B, \rho_K(f) = 1\}$$ 

By abuse of notation, we generally conflate $\mu$ and $\hat{\mu}$. 

A **left Haar measure** on $G$ is a nonzero Radon measure $\mu$ such that 

$$\mu(g B) = \mu(B)$$ 

for all $g \in G$ and all Borel sets $B$. 


## Existence and Uniqueness 

Any locally compact Hausdorff topological group $G$ admits a Haar mesaure that is unique up to scalar multiple. This result was first proven by Weil. A proof by be found in these online [notes](http://simonrs.com/HaarMeasure.pdf) by Rubinstein-Salzedo. 


### Left and Right Haar Measures that Differ

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

### The Haar Integral

Let $G$ be a topological group, and let $\mathbb{C}[G]$, the group ring over $G$. Let $G \text{-Ban}$ be the category of Banach representations of $G$. Objects in $G \text{-Ban}$ are banach spaces $X$ over $\mathbb{C}$ with a continuous action $G \times X \rightarrow X$. Maps in $C$ are bounded, $G$-equivariant maps. (Alternatively, $G \text{-Ban}$ can be viewed as a category of certain $\mathbb{C}[G]$-modules.)

Let $\text{Top}$ be the category of topological spaces, and consider $[G, \mathbb{C}]_{ \text{Top}}$, a Banach representation of $G$ with action $G \times [G, \mathbb{C}]_{ \text{Top}} \rightarrow [G, \mathbb{C}]_{ \text{Top}}$. 

We may view $\mathbb{C}$ as a Banach representation of $G$ where $gz = z$ for each $z \in \mathbb{C}$ and each $g \in G$. $\mathbb{C}$ embeds into $[G, \mathbb{C}]_{\text{Top}}$ as constant functions. We may then consider the exact sequence
$$0 \rightarrow \mathbb{C} \rightarrow [G, \mathbb{C}]_{\text{Top}} \rightarrow [G, \mathbb{C}]_{\text{Top}}/ \mathbb{C} \rightarrow 0$$

A Haar integral on the $G$-representation $[G, \mathbb{C}]_{\text{Top}}$ is a retract $\int_G : [G, \mathbb{C}]_{\text{Top}} \rightarrow \mathbb{C}$ for the injection $\mathbb{C} \rightarrow [G, \mathbb{C}]_{\text{Top}}$. In other words, it is a function $\int_G :  [G, \mathbb{C}]_{\text{Top}} \rightarrow \mathbb{C}$ such that

$$ \int_G (f_1 + f_2) = \int_G f_1 + \int_G f_2  \forall f_1, f_2 \in [G, \mathbb{C}]_{\text{Top}}$$
$$ \int_G a f = a \int_G f   \forall f \in [G, \mathbb{C}]_{\text{Top}}, a \in \mathbb{C}$$
$$ \int_G f^g = \int_G f \forall f \in  [G, \mathbb{C}]_{\text{Top}}, g \in G$$
$$ \exists C \in  \mathbb{R}_{\geq 0 } :  \left| \left| \int_G f \right| \right| \leq C \int_G ||f||\forall  [G, \mathbb{C}]_{\text{Top}}$$
The last of these requirements,  given the others, is equivalent to continuity of $\int_G$.

It is a fundamental theorem, which we will now show, that there is precisely one Haar Measure.

**Remark:** In some sense, we might wish to show that $\text{Ext}^1_{\mathbb{C}[G]}([G, \mathbb{C}]_{\text{Top}}, \mathbb{C})$ vanishes in an appripriate category; this would show that the sequence
$$0 \rightarrow \mathbb{C} \rightarrow [G, \mathbb{C}]_{\text{Top}} \rightarrow [G, \mathbb{C}]_{\text{Top}}/ \mathbb{C} \rightarrow 0$$
splits by the usual characterization of extensions via $\text{Ext}^1$. On further contemplation, however, it is sufficient only to show that the trivial $G$-representation $\mathbb{C}$ is an injective object in $G \text{-Ban}$. This could be seen as an equivariant Hahn-Banach theorem.

**Proof:** From the remark, it is sufficient to show that $\mathbb{C}$ is an injective object in $G \text{-Ban}$. Take an injection of Banach representations of $G$, $X \rightarrow Y$. Let $f : X \rightarrow \mathbb{C}$ be a map of Banach representations of $G$. By the (usual) Hahn-Banach theorem, there exists a functional $g : Y \rightarrow \mathbb{C}$ extending $f$, though it may lack $G$-invariance.

Consider the subset of all extensions of $f$ to $Y$. Let $S$ be the collection of $G$-invariant compact convex subsets of this set. $S$ contains the convex hull of $G g$, where $g$ is some chosen extension of $f$ to $Y$, so $S$ is nonempty. Using compactness and Zorn's lemma, we may find a minimal element of $S$ in this collection, where $S$ is ordered where $A \leq B$ when $A \subset B$. Call this element $H$. $H$ must be a singleton. If $H$ contains a point which is not extremal then it contains the convex hull of the orbit of that point, which would be a proper $G$-invariant compact convex subset of $H$ (see Krein Milman theorem).

Therefore $H$ is a singleton, and its unique element is a $G$-invariant functional extending $f$.

In particular, since $\mathbb{C}$ has been shown to be injective, the map $\text{Id}_{\mathbb{C}}  : \mathbb{C} \rightarrow \mathbb{C}$ lifts along the inclusion
$$0 \rightarrow \mathbb{C} \rightarrow [G, \mathbb{C}]_{\text{Top}}$$

**Remark:** this alone does not show uniqueness. However, uniqueness is not hard.

**Remark:** by the Riesz-Markov-Kakutani representation theorem, it follows that there is a unique Haar measure on $G$.


[1]: https://arxiv.org/abs/math/0606794


[[!redirects Haar measure]]
[[!redirects Haar measures]]
[[!redirects haar measure]]
[[!redirects haar measures]]
