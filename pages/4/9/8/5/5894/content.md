
This entry is about the article

* [[Yvonne Choquet-Bruhat]]:

  \linebreak

  **The Cauchy Problem in Classical Supergravity**

  \linebreak

  Letters in Mathematical Physics **7** (1983) 459-467

  [doi:10.1007/BF00402245](https://doi.org/10.1007/BF00402245)


## Summary

Here is the quintessence of the article.

### Terminology

The article considers super fields valued in a "single, arbitrary, large enough" [[Grassmann algebra]] in the sense exposed in the book

* Bryce de Witt, Supermanifolds, Cambridge Monographs on Mathematical Physics, 1984, 1992

In the following we shall not quite follow this, but make use of the observation that this really means that we are working over the [[sheaf topos]] on the [[site]] of [[superpoint]]s, as described at [[super ∞-groupoid]]. This changes nothing about the actual computations and formulas, but somewhat strenghtens the conceptual background.

### Field configurations

Let $\mathfrak{siso}(d,1)$ be the [[super Poincare Lie algebra]] in some dimension. The field [[configuration space]] of [[supergravity]] is the [[groupoid of Lie-algebra valued forms]] $\Omega^1(X, \mathfrak{siso})$ on a given [[spacetime]] manifold $X$. This is the [[super-groupoid]] that assigns to a given [[superpoint]] $\mathbb{R}^{0|q}$ with function algebra the [[Grassmann algebra]] $\Lambda_q$ the ordinary [[groupoid of Lie-algebra valued forms]] of the ordinary [[Lie algebra]] $(\mathfrak{g} \otimes \Lambda_q)_{even}$:

$$
 \Omega^1(X, \mathfrak{g}) : \mathbb{R}^{0|q} \mapsto
  \Omega^1(X, (\mathfrak{g} \otimes \Lambda_q)_{even})
  \,.
$$

Its [[object]]s are the field configurations, its [[morphism]]s the [[gauge transformation]]s.  The collection of objects over $\mathbb{R}^{0|q}$ is the collection of [[dg-algebra]]s homomorphims

$$
  Hom_{dgAlg}(W(\mathfrak{g} \otimes \Lambda_q)_{even}), \Omega^\bullet(X))
  \,,
$$

where on the left we have the [[Weil algebra]] of $(\mathfrak{g} \otimes \Lambda_q)_{even}$. The Weil algebra is a [[free construction|free]] dg-algebra on the generators

* $\{e^a \otimes (\Lamba_q^*)_{even} \}$  

* $\{\omega^{a b} \otimes (\Lamba_q^*)_{even} \}$  

* $\{\psi^{\alpha} \otimes (\Lamba_q^*)_{odd} \}$ .

Accordingly a field configuration over $\mathbb{R}^{0|q}$ is

1. the [[graviton]] given by

   1. the [[vielbein]] $\{E^a_\mu : X \to (\Lambda_q)_{even}\}$;

   1. the [[spin connection]] $\{\Omega_\mu{}^{a b} : X \to (\Lambda_q)_{even}\}$;

1. the [[gravitino]] given by $\Psi_\mu^\alpha : X \to (\Lambda_q)_{odd}$.


### The Cauchy problem

The [[Euler-Lagrange equation]]s for these fields are schematically of the form

$$
  R_{\mu \nu}^{a b } + F = 0
$$

$$
  D \Psi = 0
  \,.
$$

These are over each $\mathbb{R}^{0|q}$ equations in $C^\infty(X, \Lambda_q)$. In degree 0 in the Grassmann generators this is just the ordinary Einstein equaitons of [[gravity]] for the 0-Grassmann degree component of the fields. This is a well defined and causal Cauchy problem.

The observation now is: the equations can be solved by [[induction]] over the total number of Grassmann generators. In each step, the problem is a well-defined causal Cauchy problem in a version of ordinary [[gravity]] coupled to a bunch of extra fields.

category: reference