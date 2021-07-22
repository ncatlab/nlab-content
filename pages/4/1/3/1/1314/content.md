
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 

There are various [[simplicial object|simplicial]] [[dg-algebra]]s that assign to the standard $n$-[[simplex]] a kind of [[de Rham algebra]] on $\Delta^n$.

By the discussion at [[differential forms on presheaves]], each such extends to a notion of differential forms on simplicial sets. 

## Definition

### Smooth differential forms

+-- {: .num_defn #SmoothnSimplex}
###### Definition
**(smooth $n$-simplex)**

For $n \in \mathbb{N}$ the _smooth [[n-simplex]]_ $\Delta^n_{smth}$ is the [[smooth manifold]] with [[manifold with boundary|boundary]] and [[manifold with corners|corners]] defined, up to [[isomorphism]], as the following locus inside the [[Cartesian space]] $\mathbb{R}^{n+1}$:

$$
  \Delta^n_{smth}
  \;\coloneqq\;
  \left\{
    (x_0, x_1, \cdots, x_n)
    \in 
    \mathbb{R}^{n+1}
     \;\vert\;
     0 \leq x_i \leq 1
     \;\text{and}\;
     \underoverset{i = 0}{n}{\sum}
     x_i 
     \; = 0
  \right\}
  \hookrightarrow
  \mathbb{R}^{n+1}
  \,.
$$ 

For $0 \leq i \leq n$ the [[function]]

$$
  x_i \;\colon\; \Delta^n_{smth} \to \mathbb{R}
$$

which picks the $i$th component in the above definition is called the $i$th _barycentric coordinate function_.

For

$$
  f \;\colon\; [n_1] \longrightarrow [n_2]
$$

a morphism of finite non-empty [[linear orders]] $[n] \coloneqq \{0 \lt 1 \lt \cdots \lt n\}$, let 

$$
  \Delta_{smth}(f) 
     \;\colon\; 
  \Delta^{n_1}_{smth} 
    \longrightarrow 
  \Delta^{n_2}_{smth} 
$$

be the [[smooth function]] defined by $x_i \mapsto x_{f(i)}$.


 
=--


+-- {: .num_defn #SmoothDifferentialFormsOnSmoothnSimplex}
###### Definition
**(smooth differential forms on the smooth $n$-simplex)

For $k \in \mathbb{N}$ then a [[smooth differential k-form]] on the smooth $n$-simplex (def. \ref{SmoothnSimplex}) is a smooth differential form in the sense of [[smooth manifolds]] with [[manifold with boundary|boundary]] and [[manifold with corners|corners]]. Explicitly this means the following.

Let 

$$
  F^n
  \;\coloneqq\;
  \left\{
    (x_0, x_1, \cdots, x_n)
    \in 
    \mathbb{R}^{n+1}
     \;\vert\;
     \underoverset{i = 0}{n}{\sum}
     x_i 
     \; = 0
  \right\}
  \hookrightarrow
  \mathbb{R}^{n+1}
$$ 

be the affine plane in $\mathbb{R}^{n+1}$ that contains $\Delta^n_{smth}$ in its defining inclusion from def. \ref{SmoothnSimplex}. This is a [[smooth manifold]] [[diffeomorphism|diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^{n}$.

A smooth differential form on $\Delta^n_{smth}$ of degree $k$ is a collection of [[linear functions]]

$$
  \wedge^k T_x F^n \longrightarrow \mathbb{R}
$$

out of the $k$-fold skew-symmetric [[tensor power]] of the [[tangent space]] of $F^n$ at some point $x$ to the [[real numbers]], for all $x \in \Delta^n_{smth}$ such that this extends to a smooth differential $k$-form on $F^n$.

Write $\Omega^\bullet(\Delta^n_{smth})$ for the graded [[real vector space]] defined this way. By definition there is then a canonical linear map

$$
  \Omega^\bullet(F^n) \longrightarrow \Omega^\bullet(\Delta^n_{smth})
$$

from the [[de Rham complex]] of $F^n$ and there is a unique structure of a [[differential graded-commutative algebra]] on $\Omega^\bullet(\Delta^n_{smth})$ that makes is a [[homomorphism]] of [[dg-algebras]] form the [[de Rham algebra]] of $F^n$. This is the de Rham algebra of smooth differential forms on the smooth $n$-simplex.

For $f \colon [n_1] \to [n_2]$ a homomorphism of finite non-empty [[linear orders]] with $\Delta_{smth}(f) \colon \Delta^{n_1}_{smth} \to \Delta^{n_2}_{smth}$ the corresponding smooth function according to def. \ref{SmoothnSimplex}, there is the induced [[homomorphism]] of [[differential graded-commutative algebras]]

$$
  (\Delta_{smth}(f))^\ast
    \;\colon\;
  \Omega^\bullet(\Delta^{n_2}_{smth})
    \longrightarrow
  \Omega^\bullet(\Delta^{n_1}_{smth})
$$

induced from the usual [[pullback of differential forms]] on $F^n$. This makes smooth differential forms on smooth simplices be a [[simplicial object]] in [[differential graded-commutative algebras]]:

$$
  \Omega^\bullet(\Delta^{(-)}_{smth})
    \;\colon\;
   \Delta^{op}
     \longrightarrow
   dgcAlg_{\mathbb{R}}
  \,.
$$

=--




The standard proof of the [[Poincaré lemma]] applies to show that 

$$
  H^\bullet(\Omega^\bullet(\Delta^n_{smth})) \simeq \mathbb{R}
  \,.
$$


Each element of $\Omega^p_{poly}(\Delta^n)$ may be uniquely written


$$\Phi =\sum_{1\leq i_1\lt\ldots\lt i_p\leq n}\Phi_{i_1\ldots i_p}d b_{i_1}\wedge\ldots d b_{i_p},$$


where $b_j$ is as above the $j^{th}$ barycentric coordinate function and each $\Phi_{i_1\ldots i_p}$ is a $C^\infty$-function on $\mathbf{\Delta}^n$.



With this representation the multiplication and differential are given by the usual formulae. The multiplication is defined by $\Phi \wedge \Psi$ and extends linearly the product 

$$(d b_{i_1}\wedge\ldots d b_{i_p})\wedge (d b_{j_1}\wedge\ldots d b_{j_q}) = (d b_{i_1}\wedge\ldots d b_{i_p}\wedge d b_{j_1}\wedge\ldots d b_{j_q})$$

on the generating forms. Now if $f$ is a differentiable function
 
$$d f = \sum_{i=1}^{n} \frac{\partial f}{\partial x^i}d x_i,$$ 

so if 

$$\Phi =\sum_{1\leq i_1\lt \ldots\lt i_p\leq n}\Phi_{i_1\ldots i_p}d b_{i_1}\wedge\ldots d b_{i_p},$$

then 

$$d\Phi =\sum_{1\leq i_1\lt\ldots\lt i_p\leq n} d\Phi_{i_1\ldots i_p} \wedge d b_{i_1} \wedge \ldots d b_{i_p},$$



### Polynomial differential forms 
  {#Polynomial}


+-- {: .num_defn #PolynomialDifferentialForms}
###### Definition

For $n \in \mathbb{N}$ write

$$
  \Omega_{poly}^{\bullet}(\Delta^n)
   \;\coloneqq\;
  Sym^\bullet_{\mathbb{Q}} 
   \langle t_0, \cdots, t_n, d t_0, \cdots, d t_n\rangle/\left(\sum t_i -1, \sum d t_i \right)
$$

for the [[quotient]] of the $\mathbb{Z}$-graded [[symmetric algebra]] over the [[rational numbers]] on $n+1$ generators $t_i$ in degree 0 and $n+1$ generators $d t_i$ of degree 1.

In particular, in degree 0 these are called the _polynomial functions_

$$
  \Omega^0_{poly}(\Delta^n)
  \;=\;
  \mathbb{Q}[t_0, t_1, \cdots t_n]/\left( \underset{i}{\sum} t_i = 0 \right)
$$

due to the canonical inclusion

$$
  \Omega^0_{poly}(\Delta^n)
    \hookrightarrow
  C^\infty(\Delta^n_{smth})
$$

into the [[smooth functions]] on the $n$-simplex according to def. \ref{SmoothDifferentialFormsOnSmoothnSimplex}, obtained by regarding the generator $t_i$ as the $i$th barycentric coordinate function.

Observe that the [[tensor product]] of the polynomial differential forms over these polynomial functions with the [[smooth functions]] on the $n$-simplex, is canonically [[isomorphism|isomorphic]] to the space $\Omega^\bullet(\Delta^n_{smth})$ of smooth [[differential forms]], according to def. \ref{SmoothDifferentialFormsOnSmoothnSimplex}:

$$
  \Omega^\bullet(\Delta^n_{smth})
    \simeq
  C^\infty(\Delta^n_{smth}) \otimes_{\Omega^0_{poly}(\Delta^n)}
  \Omega^\bullet_{poly}(\Delta^n)
$$

where moreover the generators $d t_i$ are identified with the de Rham differential of the $i$th barycentric coordinate functions.

This defines a canonical inclusion

$$
  \Omega^\bullet_{poly}(\Delta^n)
    \hookrightarrow
  \Omega^\bullet(\Delta^n_{smth})
$$

and there is uniquely the structure of a [[differential graded-commutative algebra]] on $\Omega^\bullet_{poly}(\Delta^n)$ that makes this a [[homomorphism]] of [[dg-algebras]]. This is the _dg-algebra of polynomial differential forms_.


For $f \colon [n_1] \to [n_1]$ a [[morphism]] of finite non-empty [[linear orders]], let

$$
  \Omega^\bullet_{poly}(f) 
   \;\colon\; 
  \Omega^\bullet_{poly}(\Delta^{n_2}) \to \Omega^\bullet_{poly}(\Delta^{n_1})
$$

be the morphism of dg-algebras given on generators by 

$$
  \Omega^\bullet_{poly}(f) : t_i \mapsto \sum_{f(j) = i} t_j
  \,.
$$

This yields a [[simplicial object|simplicial]] [[differential graded-commutative algebra]]

$$
  \Omega^\bullet_{poly}(\Delta^{(-)}) : \Delta^{op} \to cdgAlg_k
$$

which is a sub-simplicial object of that of smooth differential form

$$
  \Omega^\bullet_{poly}(\Delta^{(-)})
    \hookrightarrow
  \Omega^\bullet(\Delta_{smth}^{(-)})
  \,.
$$

=--


### Piecewise polynomial differential forms
 {#PiecewisePolynomialDifferentialForms}

By left [[Kan extension]] the functor of polynomial differential forms from def. \ref{PolynomialDifferentialForms} yields a functor on all [[simplicial sets]]

$$
  \Omega^\bullet_{poly} \colon sSet \longrightarrow cdgAlg_k^{op}
  \,.
$$


This is the [[left adjoint]] in a [[nerve and realization]] [[adjunction]]

$$
  (\Omega^\bullet_{poly} \dashv \mathcal{K}_{poly})
    \;\colon\;
  (dgcAlg_{\mathbb{Q}, \geq 0})^{op}
    \underoverset
      {\underset{K_{poly}}{\longrightarrow}}
      {\overset{\Omega^\bullet_{poly}}{\longleftarrow}}
      {\bot}
  sSet 
  \,.
$$



Composing with the [[singular simplicial complex]] functor

$$
  Sing \;\colon\; Top \longrightarrow sSet
$$

on [[topological spaces]], this yields a functor on topological spaces

$$
  \Omega^\bullet_{pwpoly}
   \;\colon\;
  Top
   \overset{Sing}{\longrightarrow}
  sSet
   \overset{\Omega^\bullet_{poly}}{\longrightarrow}
  (dgcAlg_{\mathbb{Q}, \geq 0})^{op}
$$

which we may think of as assigning "piecewise polynomial" differential forms.

This is the starting point of the Sullivan approach to [[rational homotopy theory]]. See there for more


## Properties {#Properties}

Let $k$ be a [[field]] of [[characteristic]] 0. Let $\Omega^\bullet_{poly} : sSet \to cdgAlg_k^{op}$ be the left [[Kan extension]] of $\Omega^\bullet_{poly} : \Delta \to cdgAlg_k^{op}$ from [above](#Polynomial).

+-- {: .num_defn }
###### Definition

For $S \in sSet$,  define a morphism of graded $k$-vector spaces

$$
  \int : \Omega^\bullet_{poly}(S) \to C^\bullet(S, k)
$$

from polynomial differential forms on simplices to [[cochains on simplicial sets]] by sending $\omega \in \Omega^n_{poly}(K)$ to the cochain that sends $\sigma \in K_n$ to

$$
  \int_\sigma f := \int_{\Delta^n} f_{max}(\sigma) d t_1 \wedge \cdots d t_n
  \,,
$$

where on the right we have the ordinary [[integral]] of the $1,\cdots,n$-component of the restriction of $f$ to $\sigma$.

=--

+-- {: .num_prop }
###### Proposition

The morphism $\int$ is a [[quasi-isomorphism]] of cochain complexes.

=--

This is ([Bousfield-Gugenheim, theorem 2.2, corollary 3.4](#BousfieldGugenheim)).

The following is the central fact of the Sullivan approach to [[rational homotopy theory]]:

+-- {: .num_prop }
###### Proposition

The functor $\Omega^\bullet_{poly}$ is the [[left adjoint]] of a [[Quillen adjunction]]

$$
  (\Omega^\bullet_{poly} \dashv R)
  \;\colon\;
  sSet 
    \underoverset
      {\underset{\Omega^\bullet_{poly}}{\to}}
      {\overset{R}{\leftarrow}}
      {\bot}
  cdgAlg_k^{op}
$$

for the standard [[model structure on simplicial sets]] and the projective [[model structure on dg-algebras|model structure on commutative dg-algebras]].

=--

This is shown in ([Bousfield-Gugenheim, section 8](#BousfieldGugenheim)).

So in particular $\Omega^\bullet_{poly}$ sends cofibrations of simplicial sets to fibrations of dg-algebras. Hence for $i : \partial \Delta[k] \hookrightarrow \Delta[k]$ a boundary inclusion the corresponding restriction

$$
  i^* : \Omega^\bullet_{poly}(\Delta^k) \to \Omega^\bullet_{poly}(\partial \Delta^k)
$$

is degreewise surjective.

+-- {: .num_prop #RespectForProduct}
###### Proposition

The functor $\Omega^\bullet_{poly}$ is a [[lax monoidal functor]] whose lax monoidal structure map

$$
  \nabla_{X,Y}
  :
  \Omega^\bullet_{poly}(X)
  \otimes
  \Omega^\bullet_{poly}(Y)
  \to 
  \Omega^\bullet_{poly}(X \times Y)
$$

is a [[quasi-isomorphism]].

=--

This is reviewed for instance in ([Hess, page 12](#Hess)).

## Applications

Applications include

* the [[Sullivan construction]] in [[rational homotopy theory]];

* the [[sSet]]-[[enriched category|enrichment]] of the [[model structure on dg-algebras over an operad]].

* higher [[Lie integration]]

## Related concepts

[[PL de Rham complex]]

## References

Original sources

* [[Dennis Sullivan]], _Infinitesimal computations in topology_, Publications Math&#233;matiques de l'IH&#201;S, 47 (1977), p. 269-331 ([numdam](http://www.numdam.org/item/PMIHES_1977__47__269_0/))

* {#BousfieldGugenheim} [[Aldridge Bousfield]] and V. K. A. M. Gugenheim, &#167;1 and &#167;2 of: _On PL De Rham Theory and Rational Homotopy Type_ , Memoirs of the A. M. S., vol. 179, 1976.

* {#GriffithMorgan13} [[Phillip Griffiths]], [[John Morgan]], _Rational Homotopy Theory and Differential Forms_,  Progress in Mathematics Volume 16, Birkhauser (2013) ([doi:10.1007/978-1-4614-8468-4](https://doi.org/10.1007/978-1-4614-8468-4))

Review:

* [[Stephen Halperin]], _Lecture Notes on Minimal Models_, Publications de l'U.E.R. Math&#233;matiques  Pures et Appliqu&#233;es, Universit&#233; des Sciences et techniques, Lille, Vol 3 (1981) Fasc.3. 

* {#Hess} [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv:math.AT/0604626](http://arxiv.org/abs/math.AT/0604626))



[[!redirects polynomial differential form]]
[[!redirects polynomial differential forms]]

[[!redirects polynomial differential forms on simplices]]


[[!redirects piecewise polynomial differential form]]
[[!redirects piecewise polynomial differential forms]]

[[!redirects polynomial differential forms on the n-simplex]]
[[!redirects polynomial differential forms on n-simplices]]

[[!redirects smooth differential forms on simplices]]

[[!redirects Sullivan differential form]]
[[!redirects Sullivan differential forms]]



