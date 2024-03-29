
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A **triangulation** of a [[topological space]] $Y$ is a [[simplicial set]] $X$ together with a [[homeomorphism]] $h: R X \to Y$, where $R$ denotes the [[geometric realization]] [[functor]].

(Usually, in classical algebraic and geometric topology, the $X$ here is taken to be a [[simplicial complex]], but the difference does not really matter if one is considering uses in homotopy theoretic contexts. For the reason, see the discussion at [[subdivision]]. When considering polyhedral structure as such, for instance for PL manifolds, the simplical complex version would be needed. In such a case we may refer to a [[classical triangulation]].)

Explicitly, $R X$ is given by a [[coend]] formula

$$\int^{n \in \Delta} X(n) \cdot \sigma(n)$$

where $\sigma: \Delta \to Top$ is the standard affine [[simplex]] functor. Provided that $Top$ is interpreted as a [[nice category of spaces]] (such as $CGHaus$ -- see the discussion at [[geometric realization]]), the functor $R$ is left exact, and in particular preserves products.

## Triangulation
 {#StandardAffineSimplexFunctor}

There are various ways of understanding the affine simplex functor $\sigma: \Delta \to Top$ from a categorical perspective. (Note: in this article we will be working with the algebraist's version of the simplex category $\Delta$, namely the category of finite ordinals and order-preserving maps, including the initial or empty object which represents a (-1)-dimensional simplex. The $n$-element ordinal is conventionally, but perhaps unfortunately, denoted $[n-1]$, to indicate the dimension.)

### First definition 

One way begins by regarding $\Delta^{op}$ as isomorphic to the category of nonempty ordinals, for which maps are functions that preserve order and the top and bottom elements. In other words, as the category of finite intervals, where an [[interval]] is a totally ordered set with a top and bottom element. 
Indeed, for each ordinal $[n-1]$, the hom-set $\hom([n-1], [1])$ inherits from $[1]$ an interval structure under the pointwise definitions, and 

$$\hom(-, [1]) \colon \Delta^{op} \to FinInt$$ 

is an equivalence (this can also be seen as a restriction of the Stone duality between finite posets and finite distributive lattices). 

Under this contravariant equivalence, the $n$-element object $[n-1]$ of $\Delta$ corresponds to the $(n+1)$-element finite interval (again denoted $[n-1]$). Consider the functor that arises by homming into the standard unit interval $I$:

$$\Delta \simeq (FinInt)^{op} \hookrightarrow Int^{op} \stackrel{\hom(-, I)}{\to} Set$$

This functor lifts to a functor $hom_{Int}(-, I): \Delta \to Top$ that takes $[n-1]$ to the space of interval maps $[n-1] \to I$, 

$$\{(x_0, x_1, \ldots, x_n): 0 = x_0 \leq x_1 \leq \ldots \leq x_n = 1\},$$

topologized as a subspace $\{0 \leq x_1 \leq \ldots \leq x_{n-1} \leq 1\}$ of $I^{n-1}$. This gives the affine simplex functor $\sigma: \Delta \to Top$. 

The category of intervals is an $\omega$-accessible category where the finitely presentable objects are the finite intervals. It follows that each representable on $Int$, in particular $\hom(-, I): FinInt^{op} \to Set$, is a filtered colimit of representable presheaves on $FinInt$. 

### Second definition 

A second way of understanding $\sigma$ is by taking advantage of the fact that the algebraist's $\Delta$ is the [[walking structure|walking]] [[monoid]]. This means that given a monoidal structure on $Top$ and a monoid $M$ therein, there is a unique monoidal functor $\sigma: \Delta \to Top$ which sends the generic monoid $[0]$ to the monoid $M$. To this end, take the monoidal product on $Top$ to be "topological simplicial join": the join $X \star Y$ of two spaces $X$, $Y$ may be defined to be the pushout of the diagram

$$X \stackrel{\pi_1}{\leftarrow} X \times Y \stackrel{1_X \times \{0\} \times 1_Y}{\to} X \times I \times Y \stackrel{1_X \times \{1\} \times 1_Y}{\leftarrow} X \times Y \stackrel{\pi_2}{\to} Y$$

and now take the monoid in $Top$ to be the 1-point space $1$ with its unique monoid structure.

The induced monoidal functor is the affine simplex functor $\sigma: \Delta \to Top$. In effect, it identifies the $n$-dimensional simplex with an iterated simplicial join of $n+1$ copies of $1$:

$$\sigma(n) = 1 \star \ldots \star 1$$

because $[n]$ is itself the $(n+1)^{st}$ monoidal power of the 1-element ordinal $[0]$. Equivalently, it can be regarded as the result of applying the cone functor $C X = 1 \star X$ $n$ times to $1$.

## Cubulation

A **[[cubulation]]** of a [[topological space]] $Y$ is a [[cubical set]] $C$ together with a [[homeomorphism]] $h: R_{cub}C \to Y$ where $R_{cub}$ denotes the realization functor for [[cubical set]]s $Set^{\Box^{op}}$. Explicitly, $R_{cub}C$ is given by a [[coend]] formula

$$R_{cub}C = \int^{m \in Cube} C(m) \cdot \Box(m)$$

where $\Box: Cube \to Top$ is the standard geometric cube functor.

### Standard geometric cube functor

The category $Cube$ may be regarded as a "walking interval" in a sense slightly different to the sense of interval above: it is initial among monoidal categories that are equipped with an object $I$, two maps $i_0, i_1: 1 \to I$ (where $1$ is the monoidal unit) and a map $p: I \to 1$ such that $p \circ i_0 = id_1 = p \circ i_1$. The monoidal unit $1$ in $Cube$ is terminal, hence there is a unique map $!: X \to 1$ for any object $X$. The interval $I$ of $Cube$ monoidally generates $Cube$ in the sense of [[PROP|PROS]].

It follows that if $Top$ is considered as a cartesian monoidal category equipped with $I = [0, 1]$ in this sense of interval, we get an induced monoidal functor

$$\Box: Cube \to Top$$

The monoidal product on $Cube$ induces a monoidal product $\otimes$ on $Set^{Cube^{op}}$ by [[Day convolution]]. The cubical realization functor $R_{cub}: Set^{Cube^{op}} \to Top$ is, up to isomorphism, the unique cocontinuous monoidal functor which extends the monoidal functor $\Box$ along the Yoneda embedding; therefore $R_{cub}$ takes $\otimes$-products of cubical sets to the corresponding cartesian products of spaces.

## Properties

### General properties

(...)

### Relation between triangulation and cubulation

As explained below, there is a "cubulation" functor for standard simplices, $\Sigma: \Delta \to Set^{Cube^{op}}$, such that the affine simplex functor $\sigma: \Delta \to Top$ is naturally isomorphic to the composite

$$\Delta \stackrel{\Sigma}{\to} Set^{\Box^{op}} \stackrel{R_{cub}}{\to} Top$$

Given a triangulation $(X, h: R X \to Y)$ of a space $Y$, we have [[isomorphism]]s

$$\array{
Y & \cong & \int^n X(n) \cdot \sigma(n) \\
& \cong & \int^n X(n) \cdot (\int^m \Sigma_n(m) \cdot \Box(m)) \\
& \cong & \int^m (\int^n X(n) \cdot \Sigma_n(m)) \cdot \Box(m)
}$$

where in the last line we used the [[coend Fubini theorem]] for interchange of coends. Thus, defining the cubical set $C$ by

$$C(m) = \int^n X(n) \cdot \Sigma_n(m)$$

we have a homeomorphism $Y \cong \int^m C(m) \cdot \Box(m) = R_{cub} C$, i.e., we obtain a cubulation of $Y$.

There is also a triangulation functor for standard cubes, $\Box: Cube \to Set^{\Delta^{op}}$, which can be used to triangulate the realizations of cubical sets.

### Cubulating simplices and triangulating cubes

The functor $\Sigma$ effectively regards an $n$-simplex as an iterated [[join of simplicial sets]] and then produces the analogous join in the category of cubical sets. This for instance regards the 2-simplex as a square with one degenerate edge.

In other words, to define $\Sigma: \Delta \to Set^{Cube^{op}}$, we mimic the second construction of the affine simplex functor given above, replacing $Top$ by cubical sets and the topological simplicial join by a suitable "cubical simplicial join". Formally, we define a monoidal structure on cubical sets by taking $X \star Y$ to be the pushout of the diagram

$$X \stackrel{\pi_1}{\leftarrow} X \otimes Y \stackrel{1_X \otimes i_0 \otimes 1_Y}{\to} X \otimes I \otimes Y \stackrel{1_X \otimes i_1 \otimes 1_Y}{\leftarrow} X \otimes Y \stackrel{\pi_2}{\to} Y$$

where the projection maps $\pi_1$, $\pi_2$ are defined by taking advantage of the fact that the monoidal unit of $\otimes$ is terminal:

$$\pi_1 = (X \otimes Y \stackrel{1_X \otimes !}{\to} X \otimes 1 \cong X)$$

$$\pi_2 = (X \otimes Y \stackrel{! \otimes 1_Y}{\to} 1 \otimes Y \cong Y)$$

The terminal cubical set is of course a monoid with respect to this monoidal product, so by the walking monoid property we obtain a monoidal functor

$$\Sigma: \Delta \to Set^{Cube^{op}}$$

which plays a role analogous to the affine simplex functor into $Top$.

Observe that geometric realization $R_{cub}: Set^{Cube^{op}} \to Top$ takes cubical simplicial joins to topological simplicial joins, because $R_{cub}$ sends $\otimes$-products to cartesian products, and preserves pushouts because it is cocontinuous. We conclude that both $\sigma: \Delta \to Top$ and $R_{cub} \circ \Sigma: \Delta \to Top$ take monoidal products in $\Delta$ to topological simplicial joins, and both take the walking monoid of $\Delta$ to the one-point space. By the universal property of $\Delta$, it follows that there is a natural isomorphism

$$\sigma \cong R_{cub} \circ \Sigma$$

(as monoidal functors), which is what we want.

Similarly, we can easily define a monoidal functor $\Box_{\delta}: Cube \to Set^{\Delta^{op}}$ such that

$$(\Box: Cube \to Top) \cong (Cube \stackrel{\Box_\delta}{\to} Set^{\Delta^{op}} \stackrel{R}{\to} Top) \qquad (2)$$

In detail, regard the category of simplicial sets as a cartesian monoidal category equipped with the representable $hom(-, [1])$ as an interval (with two face maps from and a projection to the terminal object $hom(-, [0])$). By the walking interval property of $Cube$, there is an induced functor

$$\Box_{\delta}: Cube \to Set^{\Delta^{op}}$$

Finally, because $R: Set^{\Delta^{op}} \to Top$ is product-preserving and preserves the interval objects, the isomorphism (2) obtains by the universal property of $Cube$.

## Related concepts

* [[triangulation theorem]]

* [[equivariant triangulation]]

* [[equivariant triangulation theorem]]

* [[cubulation]]

## References

### General

Texbook accounts

in a context of [[mathematical physics]]:

* [[Mikio Nakahara]], p. 120 onwards in: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)


See also 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Triangulation_(geometry)">Triangulation (geometry)</a>_


[[!include triangulation theorems -- references]]




[[!redirects triangulations]]