+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
##### Fusion categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

On this whole page, assume that $G$ is a finite group. Denote by $\underline{G}$ the corresponding discrete monoidal category, and by $\operatorname{Rep}_G$ its finite dimensional $k$-representations. Further, for a monoidal category $\mathcal{C}$, denote by $\mathcal{C}-\mathcal{MOD}$ the bicategory of $k$-linear [[module category|$\mathcal{C}$-module categories]], module functors and natural transformations.

# Main idea

There are 2-functors $D : \operatorname{Rep}_G-\mathcal{MOD} \rightleftarrows \underline{G}-\mathcal{MOD} : E$, called equivariantisation and deequivariantisation, respectively.
They become weak inverses once we restrict to semisimple module categories.
In a sense, (de)equivariantisation generalises the Morita equivalence between $\operatorname{Rep}_G$ and $\operatorname{Vec}_G$ for finite groups.

## Detailed definitions

A $\underline{G}$-action (a $\underline{G}$-module category structure) on a $k$-linear semisimple category $\mathcal{C}$ amounts to the following data:

* for each group element $g \in G$ a (linear) equivalence $\rho(g)\colon \mathcal{C} \to \mathcal{C}$
* natural isomorphisms $\rho^{2}(g,h)_X\colon \rho(g)(\rho(h) X) \to \rho(gh)X$
* a natural isomorphism $\rho^0_X\colon X \to \rho(1)X$
* satisfying certain obvious coherence axioms

### Equivariantisation

__Definition__ A _$G$-equivariant object_ in $\mathcal{C}$ is then an object $X$ in $\mathcal{C}$ and a family of isomorphisms $u_g\colon \rho(g) X \to X$ compatible with the action and $\gamma$.

The $G$-equivariant objects form a category (where morphisms need to commute with the $u_g$), which is denoted by $\mathcal{C}^G$.

The primordial example for this construction is the category of finite dimensional vector spaces $k-\operatorname{Vect}$, which has a trivial $G$-action. Its $G$-equivariant objects $k-\operatorname{Vect}^G$ are simply $\operatorname{Rep}_G$.

Since $k-\operatorname{Vect}$ has a natural action on any $k$-linear category like $\mathcal{C}$, $k-\operatorname{Vect}^G \simeq \operatorname{Rep}_G$ acquires an action on $\mathcal{C}^G$. Explicitly, let $(V, \phi\colon G \to \operatorname{End}(V))$ a representation, and $(X, u_g)$ an equivariant object, then the module structure $-\triangleright-\colon \operatorname{Rep}(G) \boxtimes \mathcal{C}^G \to \mathcal{C}^G$ is defined as $(V, \phi) \triangleright (X, u_g) = (V \triangleright X, \phi(g) \otimes u_g)$. Thus we define the 2-functor $E$ as $E\mathcal{C} = \mathcal{C}^G$.

### Deequivariantisation

First note that the function algebra $k(G)$ is an object in $\operatorname{Rep}(G)$ by means of left multiplication with $G$. It has an additional $G$-representation by right inverse multiplication. Furthermore, it is an internal algebra.

__Definition__ Let $\mathcal{C}$ be a $\mathcal{M}$-module category, and $A$ an algebra internal to $\mathcal{M}$. An $A$-module in $\mathcal{C}$ is an object $X$ in $\mathcal{C}$ and a morphism $A \triangleright X \to X$ satisfying the obvious action axioms.

We can therefore form the category of $k(G)$-modules in $\mathcal{C}$, since we have a  $\operatorname{Rep}(G)$ module structure, and denote it by $\mathcal{C}_G$. Since $k(G)$ has the additional right $G$-representation, $\mathcal{C}_G$ inherits the $G$-action. Thus the 2-functor $D\mathcal{C} = \mathcal{C}_G$ is defined.

### Mutual inverses

__Theorem__ The previously defined 2-functors $D$ and $E$ are mutually (weakly) inverse 2-equivalences between the bicategory of semisimple $k$-linear categories with $G$-action, and the bicategory of semisimple $k$-linear categories with $\operatorname{Rep}_g$-action. In particular, $\mathcal{C} \simeq (\mathcal{C}^G)_G$.

### Forgetful and induction functors

* There is an obvious faithful forgetful functor $U \colon \mathcal{C}^G \to \mathcal{C}$.
* There is a left and right adjoint to $U$, the induction functor $IX = \oplus_{g \in G} \rho(g) X$.
* There is an obvious forgetful functor $U'\colon \mathcal{C}_G \to \mathcal{C}$.
* There is a left adjoint to $U$, the canonical functor $FX = k(G) \otimes X$, with the trivial action on $X$.

# Monoidal and braided categories, and central functors

The previous constructions generalise easily when our categories acquire monoidal or braided structures.

Actions of groups on monoidal categories are simply a monoidal equivalence for every group element with the same extra structure as mentioned before. Actions of groups on braided categories are additionally required to preserve the braiding. (Following the idea of [[stuff, structure, and properties]], an action on a symmetric category are simply actions on the underlying braided category.)

The action of $k-\operatorname{Vect}$ on a _monoidal_ linear category $\mathcal{C}$ can also be understood as the canonical monoidal functor $k-\operatorname{Vect} \to \mathcal{C}$ sending $k$ to the monoidal unit, followed by the tensor product.
In this situation, the $\operatorname{Rep}_G$ module structure on $\mathcal{C}$ can then also be understood as the canonical functor $\operatorname{Rep}_G \to \mathcal{C}^G$.

By abstract nonsense, an action on an algebraic object should be a morphism into its [[center]]. Consequently, the action of a braided category $\mathcal{B}$ on a monoidal category $\mathcal{C}$ should be given by a functor $\mathcal{B} \to \mathcal{Z}(\mathcal{C})$, where $\mathcal{Z}$ is the [[Drinfeld center]]. This is called a _central functor_. Similarly, the action of a _symmetric category_ $\mathcal{A}$ on a braided category $\mathcal{B}$ should be a functor $\mathcal{A} \to \mathcal{B}'$, where $\mathcal{B}'$ is the "symmetric center", or "M&#252;ger center".

The previously mentioned functor $\operatorname{Rep}_G \to \mathcal{C}^G$ factors through the forgetful functor $\mathcal{Z}(\mathcal{C}) \to \mathcal{C}$ (or, in the case of a braided category, through the inclusion $\mathcal{C}' \hookrightarrow \mathcal{C}$), so we have an action in this sense.

__Theorem__ By equivariantisation, the bicategory of fusion categories with $G$-actions is 2-equivalent to the bicategory of fusion categories with central functors from $\operatorname{Rep}_G$. Similarly, the bicategory of braided fusion categories with braided $G$-actions is 2-equivalent to the bicategory of fusion categories (symmetric central functors from $\operatorname{Rep}_G$.

## Modularisation

Each  braided fusion category $\mathcal{B}$ has a canonical symmetric subcategory, its symmetric centre $\mathcal{B}'$. By choosing a trivial twist, $\mathcal{B}'$ has a canonical spherical structure. If all the quantum dimensions are positive, that is, if $\mathcal{B}'$ is _tannakian_, it is equivalent to $\operatorname{Rep}_G$ for a unique group $G$ (since there is a canonical fibre functor). The obvious construction is then to deequivariantise over $\mathcal{B}' \simeq \operatorname{Rep}_G$, which yields $\mathcal{B}_G$, the __modularisation__ of $\mathcal{B}$.

There is an "exact sequence" of braided fusion categories:
$$ k-\operatorname{Vect} \hookrightarrow \mathcal{B}' \simeq \operatorname{Rep}_G \hookrightarrow \mathcal{B} \twoheadrightarrow \mathcal{B}_G$$
It is exact in the sense that $\mathcal{B}'$ is the maximal symmetric subcategory of $\mathcal{B}$, and that $\mathcal{B}_G$ is the maximal modular category such that $\mathcal{B}'$ is sent to sums of the monoidal unit.

# References

* Vladimir Drinfeld, Shlomo Gelaki, Dmitri Nikshych, Victor Ostrik, _On braided fusion categories I_, section 4 [arXiv](https://arxiv.org/abs/0906.0620)
* Alain Brugui&#232;res, _Cat&#233;gories pr&#233;modulaires, modularisations et invariants des vari&#233;t&#233;s de dimension 3_ (french) [pdf](http://www.math.univ-montp2.fr/~bruguieres/docs/modular.pdf)
* Michael M&#252;ger, _Galois Theory for Braided Tensor Categories and the Modular Closure_
[arXiv](https://arxiv.org/abs/math/9812040)

[[!redirects equivariantisation]]
[[!redirects deequivariantisation]]
[[!redirects de-equivariantisation]]
[[!redirects deequivariantization]]
[[!redirects de-equivariantization]]
