[[!redirects Haar measure]]

#Contents#
* table of contents
{: toc}

## Idea 

If $G$ is a locally compact Hausdorff [[topological group]], with $C_c(G)$ the algebra of compactly supported continuous functions from $C_c(G)$ to $\mathbb{R}$,  a _Haar integral_ $\int_G $ is a continuous linear map $C_c(G) \rightarrow \mathbb{R}$ which is invariant under the aparent action of $G$ on $C_c(G)$. It turns out that there exists a unique such integral, up to a scalar multiple. The Riesz representation theorem then allows one to conclude the existence of a unique _Haar measure_, which is a $G$-invariant Borel measure  on $G$.

The archetypal example of Haar measure is the [[Lebesgue measure]] on the (additive group underlying) [[cartesian space]] $\mathbb{R}^n$.

## Definition

Let $G$ be a locally compact Hausdorff group. Let $C_c(G)$ denote the vector space of continuous real-valued functionals with compact support on $G$. This is a [[locally convex topological vector space]] where the locally convex structure is specified by the family of seminorms 

$$\rho_K(f) = \sup_{x \in K} |f(x)|$$ 

$K$ ranging over compact subsets of $G$. Recall that a [[Radon measure]] on $G$ may be described as a continuous linear functional 

$$\int_G : C_c(G) \to \mathbb{R}$$ 

Such a Radon measure defines a measure $\mu$ on the $\sigma$-algebra of Borel sets in the usual sense of [[measure theory]], where 

$$\mu(B) = sup \left\{\int_G f : supp(f) = K \subseteq B, \rho_K(f) = 1 \right\}$$ 

In this context, a (left) **Haar integral** on $G$ is a nonzero such linear functional $\int_G$ such that
$$ \int_G f \geq 0 \text{ when } f \geq 0$$
$$ \int_G f^g = \int_G f$$
for each $f \in C_c(G)$ and each $g \in G$, where $f^g : G \rightarrow \mathbb{R}$ sends $x$ to $f(gx)$.

Correspondingly, a (left) **Haar measure** on $G$ is a nonzero Radon measure $\mu$ such that 

$$\mu(g B) = \mu(B)$$ 

for all $g \in G$ and all Borel sets $B$. 

## An Analogy with the Finite Case

There is an analogy between Haar measure and scaled-cardinality on a [[finite group]]. In fact, the latter is a special case of the former, as we may view a finite group as a discrete topological group. While measure on a (discrete) finite group is subsumed by the notion of Haar measure, it may be of interest to build intuition.

Let $G_{fin}$ be a finite group.  Let $G_{fin} \text{-Rep}$ be the category of $G$-[[representations]] of $R$-modules, where $R$ is a ring in which $|G_{fin}|$ is invertible. This category is equivalent to $R[G]$-mod. We can view $R$ as a trivial $G_{fin}$-representation, where $ga = a$ for each $a \in R$ and each $g \in G$.

Let $G$ be a [[compactum]]. Let $G \text{-Ban}$ be the category of Banach representations of $G$. Objects in $G \text{-Ban}$ are banach spaces $X$ over $\mathbb{R}$ with a continuous norm preserving action $G \times X \rightarrow X$, i.e. $||gx|| = ||x|| \forall g \in G \forall x \in X$. Maps in $G \text{-Ban}$ are short maps which are $G$-equivariant. (Alternatively, $G \text{-Ban}$ can be viewed as a category of certain $\mathbb{R}[G]$-modules.) We can view $\mathbb{R}$ as a trivial $G$-representation, where $ga = a$ for each $a \in \mathbb{R}$ and each $g \in G$.

Let $C(G_{fin})$ be the ring of set-maps from $G_{fin}$ to $R$. $G$ acts on $C(G_{fin})$ where $f^g : G_{fin} \rightarrow R$ sends $x$ to $f(gx)$. There is a map of abelian groups $\int_{G_{fin}} : C(G_{fin}) \rightarrow R$ sending $f$ to $\frac{1}{|G|} \sum_{g \in G} f(g)$, analogous to the Haar integral. Indeed,
$$\int_{G_{fin}} f + g = \int_{G_{fin}} f + \int_{G_{fin}} g \forall f, g \in C(G_{fin}) $$
$$\int_{G_{fin}} a f = a \int_{G_{fin}} f \forall f \in C(G_{fin}) \forall a \in R$$
$$\int_{G_{fin}} f^g = \int_{G_{fin}} f \forall f \in C(G_{fin}) \forall g \in G$$
$$\int_{G_{fin}} f \geq 0 \text{ when } f \geq 0 \forall f \in C(G_{fin}) $$

What corresponds to the Haar measure on $G$ is simply cardinality (though we must appropriately divide by the cardinality of $G$, to get a function $\mu_{fin} : P(G) \rightarrow R$ from the power set of $G$ to $R$ sending $S$ to $\frac{|S|}{|G|}$).

Using the Haar integral, we may define [[convolution product]]: $* : C(G \times G) \rightarrow C(G)$ sending $f : G \times G \rightarrow \mathbb{R}$ to the map $G \rightarrow \mathbb{R}$ sending $\int_{h \in G} f(gh^{-1}, h) = \int_{hk = g} f(h, k)$. This is analogous to the map $*_{fin} : C(G_{fin} \times G_{fin}) \rightarrow C(G_{fin})$ sending $f$ to the map $C(G_{fin} )$ sending $g$ to $\frac{1}{|G_{fin}|} \sum_{h k = g} f(h, k)$.

In both cases, we get a "[[bar construction]]". For the compact Hausdorff case, we get:
$$
    \cdots
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
   C(G  \times G)
    \stackrel{\stackrel{* }{\longrightarrow}}{\stackrel{ f \mapsto \left( g \mapsto \int_{h \in G} f( g, h) \right)  }{\longrightarrow}}
    C(G) \stackrel{\int_G}{\longrightarrow} \mathbb{R}
$$
and for the finite case, we get:
$$
    \cdots
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
   C(G_{fin}  \times G_{fin})
    \stackrel{\stackrel{*_{fin} }{\longrightarrow}}{\stackrel{ f \mapsto \left( g \mapsto  \frac{1}{|G_{fin}|} \sum_{h \in G} f( g, h) \right)  }{\longrightarrow}}
    C(G_{fin}) \stackrel{f \mapsto \frac{1}{|G_{fin}|} \sum_{g \in G} f(g)}{\longrightarrow} \mathbb{R}
$$
Calling this a bar resolution is a slight abuse of terminology; the "monad" involved is actually has no unit, as $C(G)$ has no unit for the convolution product. However, convolution makes $C(G)$ an assocciative nonunitial algebra, so that the resolution is still a _unitless_ monad. Hence there are evident face maps without degeneracies.

While $C(G)$ has no unit, there is a canonical way of adding units to it: take products with $\mathbb{R}[G]$. Write $\sum_{g \in G} a_g \delta_g$ for the elements of $\mathbb{R}[G]$; since $\delta_1$ is a formal unit for convolution, we may think of it as a Dirac delta function. Now the bar resolution
$$
    \cdots
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
   C(G  \times G) \prod \mathbb{R}[G]
    \stackrel{\stackrel{* }{\longrightarrow}}{\stackrel{ f \mapsto \left( g \mapsto \int_{h \in G} f( g, h) \right)  }{\longrightarrow}}
    C(G) \prod \mathbb{R}[G] \stackrel{\int_G}{\longrightarrow} \mathbb{R}
$$
has degeneracies as well.

## Properties

### Existence and Uniqueness

Any locally compact Hausdorff topological group $G$ admits a Haar integral (and therefore Haar measure) that is unique up to scalar multiple. This result was first proven by Weil. A proof can be found in these online [notes](http://simonrs.com/HaarMeasure.pdf) by Rubinstein-Salzedo. A different, constructive proof, due to E.M. Alfsen, can be found in the article "[A simplified and constructive proof of the existence and uniqueness of haar measure](https://www.mscand.dk/article/view/10675)".
 
We here give a lesser known proof of the existence of the Haar integral, specifically on compact Hausdorff groups $G$, which uses convex sets and the Krein Milman theorem instead of measure theory. Let $G \text{-Ban}$ be the category of Banach representations of $G$ (see "Analogy with the Finite Case").

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

**Proof:** We show that $\mathbb{R}$ is an injective object in $G \text{-Ban}$. Take an injection of Banach representations of $G$, $X \rightarrow Y$. Let $f : X \rightarrow \mathbb{R}$ be a map of Banach representations of $G$. By the (usual) Hahn-Banach theorem, there exists a map $g : Y \rightarrow \mathbb{R}$ in the category of Banach spaces and short maps extending $f$, though it may lack $G$-invariance.

Consider the subset of all extensions of $f$ to $Y$. Let $S$ be the collection of $G$-invariant compact convex subsets of this set. $S$ contains the convex hull of $G g$, where $g$ is some chosen extension of $f$ to $Y$, so $S$ is nonempty. Using compactness and [[Zorn's Lemma]], we may find a minimal element of $S$ in this collection, where $S$ is ordered where $A \leq B$ when $A \subset B$. Call this element $H$. $H$ must be a singleton. If $H$ contains a point which is not extremal then it contains the convex hull of the orbit of that point, which would be a proper $G$-invariant compact convex subset of $H$ (see Krein Milman theorem). Therefore $H$ is a singleton, and its unique element is a $G$-invariant functional extending $f$.

In particular, since $\mathbb{R}$ has been shown to be injective, the map $\text{Id}_{\mathbb{R}}  : \mathbb{R} \rightarrow \mathbb{R}$ lifts along the inclusion
$$0 \rightarrow \mathbb{R} \rightarrow C(G)$$
giving a retract $\int_G : C(G) \rightarrow \mathbb{R}$ for $0 \rightarrow \mathbb{R} \rightarrow C(G)$ in $G \text{-Ban}$.

It follows that $\int_G$ has norm $1$, and from this positivity follows immediately.

### Extensive and Intensive Properties

In Lawvere's thinking about [extensive and intensive quantities](https://ncatlab.org/nlab/show/intensive+or+extensive+quantity),
 
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

[[Abelian groups]] are obviously unimodular; so are [[compactum|compact]] groups and [[discrete topology|discrete]] groups.


## References

* {#Bredon72} [[Glen Bredon]], Section 0.3 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN 9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))


[1]: https://arxiv.org/abs/math/0606794


[[!redirects Haar measure]]
[[!redirects Haar measures]]
[[!redirects haar measure]]
[[!redirects haar measures]]
