
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Christoffel symbols#
* table of contents
{:toc}


##Idea

What is called a _Christoffel symbol_ is part of a notation and language from the early times of [[differential geometry]] at the end of the 19th and the beginning of the 20th century designed to deal with what today is called an [[affine connection]]: a [[connection on a bundle|connection]] on a [[tangent bundle]] $T X \to X$.

The _Christoffel symbols_ are the components of a [[connection on a bundle|connection 1-form]] on a coordinate patch $\mathbb{R}^n \simeq U \subset X$ of the underlying [[manifold]] $X$, in terms of the basis of the tangent bundle $T U$ induded by these coordinates.

As every concrete component expression, Christoffel symbols may be useful in certain computations. Unfortunately, almost every textbook on [[gravity]] in theoretical physics follows the long-outdated tradition of describing (or not describing) the entire notion of [[connection on a bundle|connection]]s on [[tangent bundle]]s without introducing these conceptually but just describing the Yoga of how to handle the Christoffel symbol component.
This way their main effect to science nowadays is to make it harder for students of theoretical physics to understand what is really going on in the universe. It's all so simple. Speaking always in terms of Christoffel symbols and never in terms of the abstract notion of [[connection on a bundle|connection]] makes it all so hard.


## Details

The [[tangent bundle]] $T X$ of an (oriented, say) [[manifold]] $X$ is a [[vector bundle]] that may be thought of as being the [[associated bundle]] to a $SL(n)$-[[principal bundle]] $P \to X$. This means just a little than that each fiber $T_x X$ of the tangent bundle looks like $\mathbb{R}^n$ and that the [[group]] of linear transformations $GL(n)$ acts on this.

Every tangent bundle may even be regarded as the [[associated bundle]] to a $O(n)$-principal bundle, i.e. one with structure group the [[orthogonal group]]. This is often useful. But for the discussion of Christoffel symbols we need the more general general group $GL(n)$. 


A [[connection on a bundle|connection]] on the tangent bundle is the same as a [[connection on a bundle|connection]] on the underlying $GL(n)$-[[principal bundle]]: locally on $X$ this is a [[Lie-algebra valued 1-form]] with values in the [[general linear Lie algebra]] $\mathfrak{gl}(n)$.


We may write such a $1$-form as

$$
  A = A^a t_a
  \,,
$$

where $\{t_a\}$ is a basis for the [[Lie algebra]] $\mathfrak{gl}(n)$. But this Lie algebra is naturally thought of as nothing but the Lie algebra of $n \times n$ matrices $Mat(n)$. Every choice of basis $\{v^\mu\}$ of $\mathbb{R}^n$ yields a corresponding choice of basis of $Mat(n)$: the matrix denoted $T^{\nu}{}_{\mu}$ is the matrix that in the basis given by the $\{v^\mu\}$ has zeros everywhere except in the $\mu$-$\nu$-position, where it has a $1$.

Using this, we may write the local connection 1-form as

$$
  A = A^\mu{}_\nu T^\nu{}_\mu
  \,.
$$

Moreover now, since $A$ is just defined on a patch $U \subset X$ which is diffeomorphic to $\mathbb{R}^n$, we may fix such a diffeomorphism in that we find coordinates on $U$. Then we can express each $1$-form $A^\mu{}_\nu$ in terms of the coordinate basis of $1$-forms $\{d x^\lambda\}$ as

$$
  A^{\mu}{}_{\nu} = A^{\mu}{}_{\lambda\nu} d x^\lambda
  \,.
$$

This way we obtain on each patch $U$ from the choice of a [[connection on a bundle|connection]] on the [[tangent bundle]] and a choice of basis of $\mathbb{R}^n$ and a choice of coordinates on $U$ a collection

$$
  \{
    A^{\mu}{}_{\lambda\nu} \in C^\infty(U)
  \}_{\lambda, \mu, \nu, = 1,\cdots n}
$$

of functions, which are the components of the local $\mathfrak{gl}(n)$-valued connection $1$-form with respect to all the choices made.

This collection is called the **Christoffel symbols** of the connection, and then traditionally not denoted by the 
letter $A$ but by the letter $\Gamma$

$$
  \{
    \Gamma^{\mu}{}_{\lambda\nu} \in C^\infty(U)
  \}_{\lambda, \mu, \nu, = 1, \dots, n}
  \,.
$$


## Relation to spin connection 

The literature that uses Christoffel symbols falls in two parts: one leaves it at that and never considers anything else. The other eventually talks about "spin connections" or "moving frames". 

A "spin connection" is just a [[connection on a bundle|connection]] on the [[tangent bundle]] of an [[orientation|oriented]] [[manifold]] which regards the tangent bundle as being [[associated bundle|associated]] to an $SO(n)$-[[principal bundle]] with structure group the [[special orthogonal group]]. This is locally a connection $1$-form $A$ with values in the [[special orthogonal Lie algebra]] $\mathfrak{so}(n) \subset \mathfrak{gl}(n)$. By this embedding we may regard it still as a $\mathfrak{gl}(n)$-valued form, whose coefficients happen to take values in skew-symmetric matrices. For the standard basis $\{v^a\}$ of $\mathbb{R}^n$, there is as before a canonical basis for such matrtices, denoted $T^{b}{}_{a}$. So the $\mathfrak{so}(n)$-valued connection 1-form may be expanded in this basis as

$$
  A = A^{a}{}_{b} T^{b}{}_a
  \,.
$$

Using the same coordinates as before for the patch that this is defined on allows us to expand the component 1-forms $A^b{}_a$ further as

$$
  A^{b}{}_{a} = A_{\lambda}{}^{b}{}_{a} d x^\lambda
  \,.
$$
In the relevant literature a connection $1$-form as this is traditionally denoted by the letter $\omega$:

$$
  \{
    \omega_{\lambda}{}^{a}{}_{b} \in C^\infty(C)
  \}
  \,.
$$


This is what is often called the "spin connection".

There is a [[vector bundle]] [[isomorphism]]

$$
  e : T X \to T X
$$

that identifies the tangent vectors thought of locally with respect to the basis $\{v^\mu\}$ to those thought of locally in terms of the basis $\{v^a\}$. On the given patch $U$ this is over each point $x \in U$ a $GL(n)$-valued function $e \in C^\infty(X, GL(n))$ that gives pointwise a linear map $\mathbb{R}^n \to \mathbb{R}^n$ of tangent spaces with components

$$
  e : v^a \mapsto e^{a}{}_\mu v^\mu
  \,.
$$

This is traditionally called the _vielbein_ or $n$-bein (for German: _Bein_ = _leg_, with the same root as the English _bone_; _viel_ = _many_, based on the special case _vierbein_ with _vier_ = _four_).

Generally, for $\phi \in C^\infty(X,G)$ some bundle automorphism, a function with values in the structure group of the bundle takes a connection $1$-form $A$ to

$$
  A' = \phi A \phi^{-1} + \phi d \phi^{-1}
  \,,
$$

where the first term denotes pointwise the [[adjoint action]] of the Lie group $G$ on its Lie algebra $\mathfrak{g}$, and where the second term denotes the pullback $\phi^* \theta$ of the [[Maurer-Cartan form]] $\theta$ on $GL(n)$ along $\phi$.

For the case at hand $e$ relate the Christoffel symbols to the "spin connection". In full component beauty this is traditionally written as

$$
  \omega_{\lambda}{}^{a}{}_{b} = 
  e^{a}{}_{\mu} \Gamma^{\mu}{}_{\lambda\nu} e^{\nu}{}_{b}
  + 
  e^{a}{}_{\mu} \partial_\lambda  e^{\mu}{}_{b}
  \,,
$$

where $\{e^{\mu}{}_{a}\}$ denote the components of the inverse $e^{-1}$ bundle automorphism.

This is traditionally the way that the Christoffel symbols are related to the notion of connection. But really both the Christoffel symbols as well as the spin connection components are nothing but a local component expression of the general notion of a connection $1$-form on a $GL(n)$-[[principal bundle]].

## Related concepts

* [[affine connection]]

## References

Originally due to 

* [[Elwin Bruno Christoffel]], _Über die Transformation der homogenen Differentialausdrücke zweiten Grades_, Journal für die reine und angewandte Mathematik 70 (1869), 46–70. [doi:10.1515/crll.1869.70.46](https://doi.org/10.1515/crll.1869.70.46), [doi:10.1515/9783112389409-003](https://doi.org/10.1515/9783112389409-003).

[[!redirects Christoffel symbol]]