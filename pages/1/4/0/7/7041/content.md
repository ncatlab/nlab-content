
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _bump function_ is a [[smooth function]] with [[compact support]], especially one that is not zero on a space that is not [[compact space|compact]].

One reason the category [[SmthMfd]] of [[smooth manifolds]] (with  [[smooth functions]] between them) is important, hence one reason why [[differential geometry]] is special, is that a good supply of bump functions exists. This fact accounts for the great flexibility of smooth objects, in stark contrast to [[analytic geometry]] or [[algebraic varieties]] (since non-zero analytic or algebraic functions with compact support exist only on [[compact spaces]]). For instance, bump functions can be used to construct _[[partitions of unity]]_, which can in turn be used to smoothly patch together local structures into a global structure without obstruction, as for example [[Riemannian metric|Riemannian metrics]] and more generally [[inner products on vector bundles]] (see [this prop.](inner+product+on+vector+bundles#ExistenceOfInnerProductOfTopologicalVectorBundlesOverParacompactHausdorffSpaces)).


## Constructions

+-- {: .num_defn #BumpFunction}
###### Definition

A _bump function_ is a [[function]] on [[Cartesian space]] $\mathbb{R}^n$, for some $n \in \mathbb{R}$ with values in the [[real numbers]] $\mathbb{R}$

$$
  b 
    \;\colon\;
  \mathbb{R}^n
    \longrightarrow
  \mathbb{R}
$$

such that

1. $b$ is [[smooth function|smooth]];

1. $b$ has [[compact support]].

=--


+-- {: .num_example}
###### Example

For every [[closed ball]] $B_{x_0}(\epsilon) = \{x \in \mathbb{R}^n \,\vert\, {\Vert x - x_0 \Vert} \leq \epsilon\} \subset \mathbb{R}^n$ there exists a bump function $b \colon \mathbb{R}^n \to \mathbb{R}$ (def. \ref{BumpFunction}) with 

$$
  Supp(b) = B_{x_0}(\epsilon)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the function

$$
  \phi \;\colon\; \mathbb{R}^n \longrightarrow \mathbb{R}
$$

given by

$$
  \phi(x) 
    \;\coloneqq\;
  \left\{
    \array{
      \exp\left(
       \frac{1}{{\Vert x \Vert}^2 - 1}
      \right)
       & \vert & { \Vert x \Vert} \lt 1
      \\
      0 &\vert & \text{otherwise}
     }
  \right.
  \,.
$$ 

By construction the [[support]] of this function is the closed unit ball at the origin, $Supp(\phi) = B_0(1)$. 

We claim that $\phi$ is smooth. That it is smooth away from $r \coloneqq {\Vert x \Vert} = 1$ is clear, hence smoothness only need to be checked at $r = 1$, where it amounts to demanding that all the [[derivatives]] of the exponential function vanish as $r \to 1$.

But that is the case since

$$
  \frac{d}{d r}
  \left(
    \exp\left(
     \frac
       {1}
       {
         r^2 - 1
       }
    \right)
  \right)
  =
  \frac{
    -2 r
  }
  {
    \left( r^2 - 1 \right)^2
  }
    \exp\left(
     \frac
       {1}
       {
         r^2 - 1
       }
    \right)
  \,.
$$

This clearly tends to zero as $r \to 1$. A quick way to see this is to consider the inverse function and expand the [[exponential]] to see that this tends to $\infty$ as $r \to 1$:

$$
  \frac{
    \left( 1- r^2  \right)^2
  }
  {
    2 r
  }
  \exp\left(
     \frac
       {1}
       {
         1- r^2 
       }
    \right)
  = 
  \sum_{n = 0}^\infty 
    \frac{1}{n!}
  \frac{
    \left( 1- r^2  \right)^2
  }
  {
    2 r
  }
   \frac{1}
     {
       (1- r^2)^n
     }
$$


The form of the higher derivatives is similar but with higher inverse powers of $(r^2 -1)$ and so this conclusion remains the same for all derivatives. Hence $\phi$ is smooth.

Now for arbitrary radii $\varepsilon \gt 0$ define 

$$
  \phi_\varepsilon(x) \coloneqq \phi(x/\varepsilon)
  \,.
$$

This is clearly still smooth and $Supp(\phi_{\varepsilon}) = B_0(\epsilon)$.

Finally the function $x \mapsto \phi_\varepsilon(x-x_0)$ has support the closed ball $B_{x_0}(\varepsilon)$.

=--

Define

$$
  \psi_\varepsilon 
    \coloneqq
  \frac{\phi_\varepsilon}{{\|\phi_\varepsilon\|}_1}
$$ 

so that the family $(\psi_\varepsilon)_\varepsilon$ is a smooth approximation to the identity (of convolution, the [[Dirac distribution|Dirac functional]]), compactly supported on the closed ball of radius $\varepsilon$ and having an $L^1$-norm equal to $1$. Then, it is standard that for any pair $K \subset V$ with $K$ [[compact subspace|compact]] and $V$ [[open subspace|open]] in a cartesian space $\mathbb{R}^n$, we can choose an open $U$ containing $K$ and with compact [[closure]] contained in $V$, and then taking the [[convolution]] product 
$$\psi_\varepsilon \ast \chi_U$$ 
of $\psi_\varepsilon$ with the [[characteristic function]] $\chi_U$, for $\varepsilon$ sufficiently small, we obtain a smooth function equal to $1$ on $K$ and equal to $0$ outside $V$.

By performing the above construction in [[charts]], we obtain, in any [[smooth manifold]], a smooth function equal to $1$ on any [[compact subspace]] $K$ and equal to $0$ outside any [[neighbourhood]] $V$ of $K$.  (This is a smooth [[completely regular space|regularity property]].)


## Properties


+-- {: .num_prop }
###### Proposition

[Smooth manifolds admit smooth partitions of unity](partition+of+unity#ExistenceOnSmoothManifolds)

=--


+-- {: .num_prop}
###### Proposition
**([[Paley-Wiener-Schwartz theorem]])**


For $n \in \mathbb{N}$ the vector space $C^\infty_c(\mathbb{R}^n)$ of bump functions on [[Euclidean space]] $\mathbb{R}^n$ is (algebraically and topologically) [[isomorphism|isomorphic]], via the [[Fourier transform]], to the space of [[entire functions]] $F$ on $\mathbb{C}^n$ which satisfy the following estimate: there is a [[positive number|positive]] [[real number]] $B$ such that for every [[integer]] $N \gt 0$ there is a real number $C_N$ such that:

$$ 
  \underset{\xi \in \mathbb{C}^n}{\forall} 
  \left(
    {\Vert  F(\xi) \Vert}
    \le C_N (1 + {\vert \xi\vert })^{-N} \exp{ (B \; |Im(\xi)|)}
  \right)
  \,.
$$ 

=--




## References

Textbook account:

* {#Lee12} [[John Lee]], Prop. 2.25 in: *Introduction to Smooth Manifolds*, Springer (2012) &lbrack;[doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [book webpage](https://sites.math.washington.edu/~lee/Books/ISM/), [pdf](https://math.berkeley.edu/~jchaidez/materials/reu/lee_smooth_manifolds.pdf)&rbrack;


See also:

* Wikipedia, _[Bump function](http://en.wikipedia.org/wiki/Bump_function)_

A different example is examined in detail in

* Juan Arias de Reyna, _An infinitely differentiable function with compact support: Definition and properties_, arXiv:[1702.05442](https://arxiv.org/abs/1702.05442) (English translation of: _Definici&#243;n y estudio de una funci&#243;n indefinidamente diferenciable de soporte compacto_, Rev. Real Acad. Ciencias 76 (1982) 21-38 available from [Universidad de Sevilla repository](http://hdl.handle.net/11441/28557))

One can also build bump functions that are _nowhere_ analytic (as opposed to merely on the boundary of the support, as above) using, for instance, the Fabius function:

* Wikipedia, [_Fabius function_](https://en.wikipedia.org/wiki/Fabius_function)

[[!redirects bump function]]
[[!redirects bump functions]]

[[!redirects smooth bump function]]
[[!redirects smooth bump functions]]
