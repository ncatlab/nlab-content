
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **de Rham theorem** asserts that the [[de Rham cohomology]] $H^n_{dR}(X)$ of a smooth [[manifold]] $X$ (without boundary) is [[isomorphism|isomorphic]] to the "ordinary" $\mathbb{R}$-valued cohomology, i.e. the [[singular cohomology|singular]] or [[Čech cohomology]] with real coefficients $H^n(X, \mathbb{R})$. 

The theorem has several dozens of different proofs. For example in the &#268;ech approach one can make a double complex whose first row is the &#268;ech complex of a covering and first column is the de Rham complex and other entries are mixed and use spectral sequence argument (see the textbook of Bott and Tu, or the geometry lectures book by Postnikov, semester III). 
 
This is maybe best formulated, understood and proven in the context of [[abelian sheaf cohomology]]:

Write $\mathbb{R}_c$ for 

* the abelian group $\mathbb{R}$ 

* regarded not as a [[Lie group]] with the standard [[manifold]] structure on $\mathbb{R}$ but as a topologically discrete group on the underlying set of $\mathbb{R}$

* and then regarded as a [[sheaf]] on $X$: the [[constant sheaf]] that sends connected $U \subset X$ to the set of _constant_ maps $U \to \mathbb{R}$.

Write $\mathbf{B}^n \mathbb{R}_c$ for the corresponding [[Eilenberg-MacLane object]] in [[chain complex]]es of sheaves of abelian groups: this is the complex of sheaves with $\mathbb{R}_c$ in degree $n$:

$$
  \mathbf{B}^n \mathbb{R}_c
  = 
  (\cdots \to 0 \to \mathbb{R}_c \to 0 \to \cdots \to 0) 
  \,.
$$ 

Next, write $\bar \mathbf{B}^n \mathbb{R}$ (without the subscript $c$!) for the [[Deligne cohomology|Deligne complex]] for $\mathbb{R}$

$$
  \bar \mathbf{B}^n \mathbb{R}
  = 
  (C^\infty(-,\mathbb{R}) \stackrel{d_{dR}}{\to}
    \Omega^1(-) \stackrel{d_{dR}}{\to}
    \Omega^2(-) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{closed}(-)) 
  \,.
$$ 

(The notation here is borrowed from that used at [[motivation for sheaves, cohomology and higher stacks]]: we can think of $\bar \mathbf{B}^n \mathbb{R}$ as a differential refinement of the object $\mathbf{B}^n \mathbb{R}_c$).

Then we have:

* "ordinary" $\mathbb{R}$-valued cohomology of $X$ is the [[abelian sheaf cohomology]] with coefficients in $\mathbf{B}^n \mathbb{R}_c$.

* [[de Rham cohomology]] of $X$ is the [[abelian sheaf cohomology]] with coefficients in $\bar \mathbf{B}^n \mathbb{R}$ (this is semi-obvious, requires a bit more discussion).

* the [[Poincare lemma]] says that every closed [[differential form]] is locally exact, and hence there is a [[quasi-isomorphism]] of chain complexes of sheaves

  $$
    \mathbf{B}^n \mathbb{R}_c \stackrel{\simeq}{\to}
    \bar \mathbf{B}^n \mathbb{R}
  $$

  given by injecting for each $U \subset X$ the set $\mathbb{R}$ as the constant functions into $C^\infty(U,\mathbb{R})$.

It is this quasi-isomorphism of coefficient objects that induces the de Rham isomorphism of [[abelian sheaf cohomology|abelian sheaf]] [[cohomology group]]s, which is ordinarily written as

$$
  H^n(X,\mathbb{R}) \simeq 
  H^n_{dR}(X)
  \,.
$$

...

## Synthetic de Rham theorem

The de Rham theorem also holds internally in the context of suitable [[smooth topos]]es $\mathcal{T}$ modelling the axioms of [[synthetic differential geometry]].

Specifically 

* the internal [[singular cohomology|singular chain complex]] in $\mathcal{T}$ is given as the $R$-linear dual of the free interal $R$-module on the [[internal hom]] objects $[\Delta^n,X]$, where $R$ is the internal incarnation of the real numbers;

* the de Rham complex is givebn by [[differential forms in synthetic differential geometry]].

The de Rham theorem in $\mathcal{T}$ then asserts that for $X$ a manifold regarded as an object in the well-adapted smooth topos $\mathcal{T}$ the morphism

$$
  \int : H^p(X) \to H_p(X,R)^*
$$

in $\mathcal{T}$ is an [[isomorphism]] for all $p \in \mathbb{N}$. This implies the standard (external) de Rham theorem.

This is discussed in chapter IV of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ for the toposes $\mathcal{T} = \mathcal{G}, \mathcal{F}$ (see [models](http://ncatlab.org/nlab/show/Models+for+Smooth+Infinitesimal+Analysis#Models)).

A little bit a long these lines for [[diffeological space]]s is also in

* Patrick Iglesias-Zemmour, _De Rham calculus_ ([pdf](http://math.huji.ac.il/~piz/documents/D6.pdf))

## References

A useful exposition of the standard de Rham theorem is in

* Arne Lorenz, _Abstract de Rham theorem_ ([pdf slides](http://wwwb.math.rwth-aachen.de/~arne/Talks/deRham.pdf))

...

[[!redirects deRham theorem]]
