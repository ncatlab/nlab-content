#Contents#

* table of contents
{: toc}

## Idea

A *graded module* is a [[module object]] over a [[graded ring]].

## Definition

Let $G$ be a [[monoid]] (written additively), typically one uses $(\mathbb{Z},+,0)$. Let $R$ be an [[graded ring|$M$-graded ring]]. It consists of abelian groups $R_n$ for $n \in G$ and multiplication maps $R_n \times R_m \to R_{n+m}$ in particular. Also, we have a unit $1 \in R_0$.

We now define the category $grMod_R$ of graded $R$-modules. It has several equivalent definitions.

### Concrete Definition
 
A *graded module* consists of abelian groups $M_n$ for $n \in G$ and multiplication maps $R_n \times M_m \to M_{n+m}$, written $(r,x) \mapsto r \cdot x$, such that the module axioms hold: The maps $\cdot$ are additive in each variable, we have $1 \cdot x = x$ for $x \in M_m$, and we have $(r \cdot s) \cdot x = r \cdot (s \cdot x)$ for $r \in R_n$, $s \in R_m$, $x \in M_k$.

A morphism of graded modules $M \to N$ is a family of group homomorphisms $M_n \to N_n$ that are compatible with the multiplication maps.

This defines the objects and morphisms of a category $grMod_R$.

Notice that when $R$ is a ring, we can see it as a graded ring concentrated in degree $0$, and we get [[graded modules]] over the ring $R$.

### Functorial Definition

Assume that $G$ is an abelian group. Consider the [[Ab-enriched category]] $\mathcal{R}$ whose objects are the elements $n \in G$ and whose morphisms are $\hom(n,m) = R_{m-n}$. The multiplication in $R$ serves as the composition. The category $grMod_R$ is just the category of [[enriched functor|Ab-enriched functors]] $\mathcal{R} \to Ab$.

This description makes it obvious that $grMod_R$ is an [[abelian category]] since $Ab$ is. Moreover, it is [[complete]] and [[cocomplete]] since $Ab$ is.

### Direct Sum Definition

In the literature, it is most common to define a graded ring as a ring $R$ with a direct sum decomposition $R = \bigoplus_{n \in G} R_n$ of its underlying abelian group such that $1 \in R_0$ and $R_n \cdot R_m \subseteq R_{n+m}$. (It turns out that $1 \in R_0$ is a consequence, from the rest of axioms, but it is unnatural to remove this from the definition.)

Likewise, a graded $R$-module is defined as an $R$-module $M$ with a direct sum decomposition $M = \bigoplus_{n \in G} M_n$ such that $R_n \cdot M_m \subseteq M_{n+m}$. A morphism of graded $R$-module $f : M \to N$ is then defined as a homomorphism of $R$-modules $f : M \to N$ that maps $M_n$ into $N_n$, for every $n \in G$.

This defines a category $grMod_R$. It is equivalent to the previous definitions.

### Abstract Definition

Consider the [[monoidal category]] of graded abelian groups: its underlying category is just the [[product category]] $Ab^G$. The tensor product is

$(A \otimes B)_k := \bigoplus_{n+m = k} A_n \otimes B_m.$

The monoidal unit is the graded abelian group concentrated in degree $0$ with value $\mathbb{Z}$.

A [[monoid object]] in this monoidal category $(Ab^G,\otimes,\mathbb{Z})$ is the same as a graded ring $R$.

We define the category $grMod_R$ as the category of [[module object|module objects]] over $R$. Spelling out what this means, we arrive at the first definition.

This abstract definition makes precise that the relationship between modules and rings is exactly the relationship between graded modules and graded rings; we just exchange the monoidal category. Moreover, it allows to replace ad-hoc proofs for properties of $grMod_R$ by more general statements about the category of module objects in a monoidal category.

## Properties

Let $R$ be a graded ring. The category $grMod_R$ is a [[Grothendieck abelian category]]. In fact, it is cocomplete, abelian, and filtered colimits are exact since $Ab$ has these properties, and there is a canonical [[generating set]] given by the graded $R$-modules $R[d]$ defined by $R[d]_n = R_{d+n}$ for $d \in G$.

If $grMod_R$ is a category of modules over a (non-graded) ring depends on the choice of $R$, see [MO/85505](https://mathoverflow.net/questions/85505). For example, if $R$ is concentrated in degree $0$ and $k = R_0$, then $grMod_R \cong \prod_{g \in G} Mod_k$. When $G$ is finite, this is equivalent to $Mod_{k^G}$, where $k^G$ is the [[cartesian product|product ring]] of $G$ copies of $k$. But when $G$ is infinite and $k \neq 0$, this category has no [[finitely presentable object|finitely presentable]] [[generator]], thus cannot be a module category; in fact, it cannot be a category of models of a single-sorted [[algebraic theory]].

The category $grMod_R$ is always a [[locally strongly finitely presentable category]] since graded modules can be modelled with a multi-sorted [[algebraic theory]] having sorts $(S_n)_{n \in G}$ and unary operations $r : S_m \to S_{n+m}$ for $r \in R_n$. In particular, the category is [[locally finitely presentable category|locally finitely presentable]].

When $R$ is commutative, $grMod_R$ carries a [[symmetric monoidal category|symmetric monoidal structure]].

## Examples

1. When the graded ring $R$ is concentrated in degree $0$ and we abbreviate $k = R_0$, then (as mentioned above) $grMod_R$ identifies with the [[product category]] $\prod_{g \in G} Mod_k$.

2. Let $k$ be a ring. Consider the $\mathbb{Z}$-graded ring $R$ with $R_n = k$ for every $n \in \mathbb{Z}$ and the evident multiplication maps. Using the "direct sum definition" of graded rings indicated above, this is just the ring $k[T,T^{-1}]$ of [[Laurent polynomial|Laurent polynomials]] over $k$, where $T$ has degree $1$. A graded $R$-module consists of $k$-modules $(M_n)_{n \in \mathbb{Z}}$ and $k$-linear isomorphisms $T : M_n \to M_{n+1}$. Therefore, $grMod_R$ identifies with $Mod_k$.

3. Let $k$ be a ring. Consider the $\mathbb{N}$-graded ring $R$ with $R_n = k$ for every $n \in \mathbb{N}$ and the evident multiplication maps. Using the "direct sum definition" of graded rings indicated above, this is just the [[polynomial ring]] $k[T]$ over $k$, where $T$ has degree $1$. A graded $R$-module consists of $k$-modules $(M_n)_{n \in \mathbb{Z}}$ and $k$-linear maps $T : M_n \to M_{n+1}$. Hence, it can be seen as a sequence $M_0 \longrightarrow M_1 \longrightarrow M_2 \longrightarrow \cdots$.

4. As a variation of the previous example, consider the graded ring $R = k[T]/\langle T^2 \rangle$. Then $grMod_R$ is the category of [[cochain complex|cochain complexes]] of $k$-modules in non-negative degrees.

## Related concepts

- [[Mod]]
- [[graded vector space]]
- [[graded set]] 