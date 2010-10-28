#Contents#
* automatic table of contents goes here
{:toc}

## The category of cubes

The category $Cube$ may be defined universally to be a [[walking structure|walking]] [[interval]]: it is initial among monoidal categories that are equipped with an object $I$, two maps $i_0, i_1: 1 \to I$ (where $1$ is the monoidal unit) and a map $p: I \to 1$ such that $p \circ i_0 = id_1 = p \circ i_1$. The monoidal unit $1$ in $Cube$ is terminal, hence there is a unique map $!: X \to 1$ for any object $X$. The interval $I$ of $Cube$ monoidally generates $Cube$ in the sense of [[PROP|PROS]]. 

It may be shown that if $m \leq n$, there are $\binom{n}{m}2^{n-m}$ injections $I^{\otimes m} \to I^{\otimes n}$, the same as the number of $m$-dimensional faces of the geometric $n$-cube. There are no diagonal maps in the category of cubes as defined here. 

* A different possibility is to consider the [[Lawvere theory]] of two constants, which gives a different category of cubes with diagonal maps. 

## Standard geometric cube functor

From the universal property of $Cube$, it follows that if $Top$ is considered as a cartesian monoidal category equipped with $I = [0, 1]$ in this sense of interval, we get an induced monoidal functor

$$\Box: Cube \to Top$$

The monoidal product on $Cube$ induces a monoidal product $\otimes$ on $Set^{Cube^{op}}$ by [[Day convolution]]. The cubical realization functor $R_{cub}: Set^{Cube^{op}} \to Top$ is, up to isomorphism, the unique cocontinuous monoidal functor which extends the monoidal functor $\Box$ along the Yoneda embedding; therefore $R_{cub}$ takes $\otimes$-products of cubical sets to the corresponding cartesian products of spaces. 

In terms of an explicit formula, the cubical realization of a cubical set $C: \Cube^{op} \to Set$ is given by the coend formula 

$$R_{cub} C = \int^{m \in Ob(Cube)} C(m) \times \Box(m)$$ 

## Definition 

A **cubulation** of a [[topological space]] $Y$ is a [[cubical set]] $C: Cube^{op} \to Set$ together with a [[homeomorphism]] $h: R_{cub}C \to Y$. 

## Relation between triangulation and cubulation

In rough terms, a space can be triangulated if and only if it can be cubulated. This can be shown by simple conceptual arguments, as follows. 

### Cubulating a triangulated space 

In this section, $Top$ may be taken to be the category of topological spaces, or otherwise any sufficiently convenient category of spaces (completeness and cocompleteness are baseline assumptions). 

#### Simplices as cubical sets

We define a functor 

$$\Sigma: \Delta \to Set^{Cube^{op}}$$ 

The functor $\Sigma$ effectively regards an $n$-simplex as an iterated [[join of simplicial sets]] and then produces the analogous join in the category of cubical sets. This for instance regards the 2-simplex as a square with one degenerate edge.

To define $\Sigma: \Delta \to Set^{Cube^{op}}$, we mimic the [second definition](http://ncatlab.org/nlab/show/triangulation#second_definition_5) of the affine simplex functor given at [[triangulation]], replacing $Top$ by cubical sets and the topological simplicial join by a suitable "cubical simplicial join". Formally, we define a monoidal structure on cubical sets by taking $X \star Y$ to be the pushout of the diagram

$$X \stackrel{\pi_1}{\leftarrow} X \otimes Y \stackrel{1_X \otimes i_0 \otimes 1_Y}{\to} X \otimes I \otimes Y \stackrel{1_X \otimes i_1 \otimes 1_Y}{\leftarrow} X \otimes Y \stackrel{\pi_2}{\to} Y$$

where the projection maps $\pi_1$, $\pi_2$ are defined by taking advantage of the fact that the monoidal unit of $\otimes$ is terminal:

$$\pi_1 = (X \otimes Y \stackrel{1_X \otimes !}{\to} X \otimes 1 \cong X)$$

$$\pi_2 = (X \otimes Y \stackrel{! \otimes 1_Y}{\to} 1 \otimes Y \cong Y)$$

The terminal cubical set is of course a monoid with respect to this monoidal product, so by the walking monoid property we obtain a monoidal functor

$$\Sigma: \Delta \to Set^{Cube^{op}}$$

which plays a role analogous to the affine simplex functor into $Top$.

#### Cubulating geometric simplices 

Observe that geometric realization $R_{cub}: Set^{Cube^{op}} \to Top$ takes cubical simplicial joins to topological simplicial joins, because $R_{cub}$ sends $\otimes$-products to cartesian products, and preserves pushouts because it is cocontinuous. We conclude that both $\sigma: \Delta \to Top$ and $R_{cub} \circ \Sigma: \Delta \to Top$ take monoidal products in $\Delta$ to topological simplicial joins, and both take the walking monoid of $\Delta$ to the one-point space. By the universal property of $\Delta$, it follows that there is a natural isomorphism

$$\sigma \cong R_{cub} \circ \Sigma$$

(as monoidal functors), giving the canonical cubulation of affine simplices. In terms of an explicit formula, we have 

$$\sigma(n) \cong \int^m \Sigma_n(m) \cdot \Box(m)$$ 

#### Standard cubulation of a triangulated space

Given a [[triangulation]] $(X, h: R X \to Y)$ of a space $Y$, we have [[isomorphism]]s

$$\array{
Y & \cong & \int^n X(n) \cdot \sigma(n) & & \\
 & \cong & \int^n X(n) \cdot (\int^m \Sigma_n(m) \cdot \Box(m)) & & cubulation of \sigma(n) \\
 & \cong & \int^m (\int^n X(n) \cdot \Sigma_n(m)) \cdot \Box(m) & & interchange of coends
}$$

where in the last line we used the [[coend Fubini theorem]]. Thus, defining the cubical set $C$ by

$$C(m) = \int^n X(n) \cdot \Sigma_n(m)$$

we have a homeomorphism $Y \cong \int^m C(m) \cdot \Box(m) = R_{cub} C$, i.e., we obtain a cubulation of $Y$.

### Triangulating a cubulated space

In this section we assume $Top$ is a [[convenient category of spaces]], so that [[geometric realization]] of simplicial sets is product-preserving. 

#### Cubes as simplicial sets 

Define a monoidal functor $\Box_{\delta}: Cube \to Set^{\Delta^{op}}$ as follows: regard the category of simplicial sets as a cartesian monoidal category equipped with the representable $hom(-, [1])$ as an interval (with two face maps from and a projection to the terminal object $hom(-, [0])$). By the walking interval property of $Cube$, there is an induced functor

$$\Box_{\delta}: Cube \to Set^{\Delta^{op}}$$

#### Triangulating geometric cubes 

Next, because $R: Set^{\Delta^{op}} \to Top$ is preserves cartesian products and preserves the interval objects, we have an isomorphism 

$$(\Box: Cube \to Top) \cong (Cube \stackrel{\Box_\delta}{\to} Set^{\Delta^{op}} \stackrel{R}{\to} Top) \qquad (2)$$

by the universal property of $Cube$. In terms of an explicit formula, we have 

$$\Box(m) \cong \int^n \Box_{\delta m}(n) \cdot \sigma(n)$$ 

#### Standard triangulation of a cubulated space

Given a cubulation $(C, h: R_{cub} X \to Y)$ of a space $Y$, we have [[isomorphism]]s

$$\array{
Y & \cong & \int^m C(m) \cdot \Box(m) & & \\
 & \cong & \int^m C(m) \cdot (\int^n \Box_{\delta m}(n) \cdot \sigma(n)) & & triangulation of \Box(m) \\
 & \cong & \int^n (\int^m C(m) \cdot \Box_{\delta m}(n)) \cdot \sigma(n) & & interchange of coends
}$$

where in the last line we used the [[coend Fubini theorem]]. Thus, defining the simplicial set $X$ by

$$X(n) = \int^m C(m) \cdot \Box_{\delta m}(n)$$

we have a homeomorphism $Y \cong \int^n X(n) \cdot \sigma(n) = R X$, i.e., we obtain a triangulation of $Y$. 


[[!redirects cubulation]]