
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Manifolds and Cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Functorial Quantum Field Theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

$n$-Dimensional [[manifolds]] (possibly and usually equipped with certain structure, notably for instance with [[orientation]], [[framing]]-structure or more general [[G-structure]]) should naturally form an [[(∞,n)-category]] of [[extended cobordisms]] whose

* [[objects]] are 0-dimensional (oriented) manifolds (disjoint unions of (oriented) points);

* 1-[[morphisms]] are (oriented) [[cobordisms]] between disjoint unions of (oriented) points;

* 2-morphisms are cobordisms between 1-dimensional cobordisms

* etc.

* (n+1)-morphisms are _diffeomorphisms_ between $n$-dimensional cobordisms;

* (n+2)-morphisms are smooth homotopies of these;

* etc.

The $(\infinity,n)$-category of cobordisms is the subject of the [[cobordism hypothesis]].


## Definition

### As an $n$-fold complete Segal space

Here is an outline of the idea of the definition of 
$Bord_{(\infty,n)}$ as given in ([Lurie](#LurieQFT)) where the main point, apart from the [[(∞,n)-category]] machinery in the background, is definition 2.2.9.

The idea is to start with thinking of $n$-dimensional cobordisms as forming something like an [[n-fold category]] by simply saying that the collection of composites of cobordisms is given by big cobordisms with markings on them, indicating where we think of them as being composed.

Let's first do this for composition in one direction, as in an ordinary 1-category of $n$-dimensional cobordisms.

consider a [[manifold]] $X \hookrightarrow V \times \mathbb{R}$ embedded in a [[vector space]] of the form $V \times \mathbb{R}$. We can think of this as a manifold canonically equipped with a coordinate function $\phi : X \hookrightarrow V \times \mathbb{R} \to \mathbb{R}$ that measures the "height" or maybe better the "length" of the embedded manifold. 

We can pick a bunch of numbers $\{t_j \in \mathbb{R}\}$ and think of these as marking a bunch of slices of $X$, the preimages $\phi^{-1}(t_j)$. We can think of these slices as being the $(n-1)$-dimensional boundary manifolds at which a sequence of manifolds have been glued together to produce $X$. 

> (there is an obvious picture to be drawn and uploaded here, maybe somebody finds the time and energy)

In this way an embedded manifold $X \hookrightarrow V \times \mathbb{R} $ and a set of $k$-numbers $\{t_i\}$ may represent an element in the space of sequences of composable cobordisms. To make this work as expected, the markings on $X$ may not be too irregular, so we should impose some conditions on what qualifies as a marked manifold. The precise statement is given further below.

The collection of these tuples, consisting of an embedded manifold $X \hookrightarrow V \times \mathbb{R}$ and a collection of $k$ numbers $\{t_i \in \mathbb{R}\}$ naturally form a [[simplicial set]], which is like the [[nerve]] of the 1-category of $n$-dimensional cobordisms under composition in one direction.

To generalize this from just a 1-categorical structure to an $n$-categorical structure, we simply take a manifold $X$ as before, but now draw markings on it in $n$ transversal directions, thereby putting a kind of grid on it that subdivides the manifold into cubical slices. A manifold with such subdivision on it may then be regarded as giving an element in the space of $n$-dimensional pasting diagrams in an $n$-fold category.

To formalize this more general case, we embed $X$ not just into a $V \times \mathbb{R}$, but a $V \times \mathbb{R}^n$. This then provides us with $n$ different coordinate functions $\phi_i : X \hookrightarrow V \times \mathbb{R}^n \stackrel{p_i}{\to} \mathbb{R}$ on $X$, each running along one of the directions in which we may think of $X$ as having been glued from smaller manifolds.

A collection of markings indicating such gluing is now a collection of numbers $\{t_j^1\}, \;\{t_j^2\}, \; \cdots \{t_j^n\}$, one for each of these directions.

For each direction this yields a [[simplicial set]] of such structures, to be thought of as the [[nerve]] of the category of cobordisms under composition in one of these directions. Taken together this is an $n$-fold simplicial set

$$
  \Delta^{op} \times \Delta^{op} \times \cdots \times \Delta^{op}
  \to Set
$$

which is like the nerve of an $n$-fold category of cobordisms. 

When suitable regularity conditions are imposed on this data, there is naturally a [[topology]] on each of these sets of embedded marked cobordisms, that makes this into an $n$-fold simplicial [[topological space]]

$$
  \Delta^{op} \times \Delta^{op} \times \cdots \times \Delta^{op}
  \to Top
  \,.
$$

To get rid of the dependence of this construction on $V$, we can let $V$ "grow arbitrarily large" by taking the [[colimit]] of the above $n$-fold cosimplicial spaces as $V$ ranges over the finite dimensional subspaces of $\mathbb{R}^\infty$.

The resulting $n$-fold simplicial topological space obtained by this colimit then is essentially the [[(∞,n)-category]] $Bord_n$ that we are after. It turns out that it actually is an $n$-fold Segal space. We just formally _complete_ it to an [[n-fold complete Segal space]]

$$
  Bord_n : (\Delta^{op})^n \to Top
  \,.
$$

This, then, is a model for the [[(∞,n)-category]] of extended $n$-dimensional cobordisms.

### As a blob $n$-category

There is a definition of a [[blob n-category]] of $n$-cobordisms. See there for more details.

## Examples

### $Bord_2^{fr}$
 {#Framed2Bordisms}

Some comments on 2-[[framed manifold|framed]] 2-cobordisms.

Consider the pictures in ([Schommer-Pries 13, figure 5](#SchommerPries13)).

> Somebody should produce pictures like this here...

Let $\gamma$ be a 1-dimensional manifold of the form of the interval $[0,1]$. A 2-[[framing]] of $\gamma$ is a trivialization of $T\gamma \oplus \mathbb{R}$. Let $\{1\} \subset \mathbb{R}$ be the canonical [[basis]] of $\mathbb{R}$. If we think of the plane $\mathbb{R}^2$ as equipped with its canonical 2-framing, then a 2-framing of $\gamma$ is induced by embedding $\gamma$ into the plane and shading one of its two sides. This identifies at each point  $x \in \gamma$ the tangent space to $\gamma$ at that point with the tangent vector to the embedding of $\gamma$ as a vector in $\mathbb{R}^2$ and identifies $1\in \mathbb{R}$ with the vector in $\mathbb{R}^2$ orthogonal to this tangent vector and pointing into the shaded region.

This shows that if $\gamma$ is regarded with its two endpoints both as incoming or both as outgoing, then the induced 2-framing of these endpoints is opposite to each other. This way such an arc is a morphism from the union of the "positive point" and the "negative point" to the empty 0-manifold, hence is a unit/counit exhibiting these as [[dual objects]].




## Properties 
 {#Properties}

### Adjoints

$Bord_n$ is an [[(∞,n)-category with all adjoints]].

### Relation to Thom spectrum

For $n \to \infty$ we have that $Bord_{(\infty,\infty)}$ is the [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[∞-groupoid]] ($\simeq$ [[infinite loop space]]) $\Omega^\infty M O$ that underlies the [[Thom spectrum]].

Its [[homotopy group]]s are the [[cobordism ring]]s

$$
  \pi_n Bord_{(\infty,\infty)} \simeq \Omega_n
  \,.
$$

Therefore a symmetric monoidal  $\infty$-functor

$$
  Bord_{(\infty,\infty)} \to S
$$

to some symmetric monoidal $\infty$-groupoid $S$ is a [[genus]].

## Related concepts

* [[cobordism]], [[extended cobordism]]

* [[category of cobordisms]]

* **(∞,n)-category of cobordisms**

* [[cobordism hypothesis]]


## References

### General

A specific realization of this idea in terms of [[(∞,n)-category]] modeled as [[n-fold complete Segal space]] is in (definition 2.2.9, page 36)

*  {#LurieQFT} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

* [[Jacob Lurie]], [Video Stream](http://www.youtube.com/watch?v=Bo8GNfN-Xn4)

In that article a proof of the [[cobordism hypothesis]] is indicated. A review is in 

* [[Julie Bergner]], _Models for $(\infty,n)$-Categories and the Cobordism Hypothesis_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Available [on the arxiv](http://arxiv.org/abs/1011.0110). 

Other discussions of higher categories of cobordisms are

* [[Marco Grandis]], _[[Cospans in Algebraic Topology]]_

* [[Eugenia Cheng]] and [[Nick Gurski]], _Toward an $n$-category of cobordisms_ , Theory and Applications of Categories 18 (2007), 274-302. ([tac](http://www.tac.mta.ca/tac/volumes/18/10/18-10abs.html))


### In dimension 2

A detailed construction of the [[(n,r)-category|(2,2)-category]] of 2-dimensional cobordisms is

* [[Chris Schommer-Pries]], _[[2-category of 2-dimensional cobordisms]]_.

* {#SchommerPries13} [[Chris Schommer-Pries]], _Dualizability in Low-Dimensional Higher Category Theory_ ([arXiv:1308.3574](http://arxiv.org/abs/1308.3574))

### In dimension 3

* [[Bruce Bartlett]], [[Christopher Douglas]], [[Christopher Schommer-Pries]], [[Jamie Vicary]], _Extended 3-dimensional bordism as the theory of modular objects_ ([arXiv:1411.0945](http://arxiv.org/abs/1411.0945))

### In dimension $\infty$

For a discussion of the relation of $Bord_{(\infty,\infty)}$ to the [[Thom spectrum]] and the [[cobordism ring]] see also

* [[John Francis]], _Cobordisms_ (notes by [[Owen Gwilliam]]) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))



[[!redirects (∞,n)-category of cobordisms]]

[[!redirects (∞,n)-categories of cobordisms]]
[[!redirects (infinity,n)-categories of cobordisms]]

