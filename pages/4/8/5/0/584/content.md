

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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
* automatic table of contents goes here
{:toc}

## Idea

$n$-Dimensional [[manifolds]] (possibly and usually equipped with certain structure, notably for instance with orientation) should naturally form an [[(∞,n)-category]] of [[extended cobordisms]] whose

* [[objects]] are 0-dimensional (oriented) manifolds (disjoint unions of (oriented) points);

* 1-[[morphisms]] are (oriented) [[cobordisms]] between disjoint unions of (oriented) points;

* 2-morphisms are cobordisms between 1-dimensional cobordisms

* etc.

* (n+1)-morphims are _diffeomorphisms_ between $n$-dimensional cobordisms;

* (n+2)-morphisms are smooth homotopies of these;

* etc.

The $(\infinity,n)$-category of cobordisms is the subject of the [[cobordism hypothesis]].


## Definition

### As an $n$-fold complete Segal space

Here is an outline of the idea of the definition of 
$Bord_{(\infty,n)}$ as given in 

*  [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

where the main point, apart from the [[(∞,n)-category]] machinery in the background, is definition 2.2.9.

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

The resulting $n$-fold simplicial topological space obtained by this colimit then is essentially the [[(∞,n)-category]] $Bord_n$ that we are after. It turns out that it actually is an $n$-fold Segal soace. We just formally _complete_ it to an [[n-fold complete Segal space]]

$$
  Bord_n : (\Delta^{op})^n \to Top
  \,.
$$

This, then, is a model for the [[(∞,n)-category]] of extended $n$-dimensional cobordisms.

### As a blob $n$-category

There is a definition of a [[blob n-category]] of $n$-cobordisms. See there for more details.


## Properties {#Properties}

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



## References

A specific realization of this idea in terms of [[(∞,n)-category]] modeled as [[n-fold complete Segal space]] is in (definition 2.2.9, page 36)

*  [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

In that article a proof of the [[cobordism hypothesis]] is indicated.

A detailed construction of the [[(n,r)-category|(2,2)-category]] of cobordisms is

* [[Chris Schommer-Pries]], [[2-category of 2-dimensional cobordisms]] .

For a discussion of the relation of $Bord_{(\infty,\infty)}$ to the [[Thom spectrum]] and the [[cobordism ring]] see also

* [[John Francis]], _Cobordisms_ (notes by [[Owen Gwilliam]]) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))


Other discussions of higher categories of cobordisms are

* [[Marco Grandis]], _[[Cospans in Algebraic Topology]]_

* [[Eugenia Cheng]] and [[Nick Gurski]], _Toward an $n$-category of cobordisms_ , Theory and Applications of Categories 18 (2007), 274-302. ([tac](http://www.tac.mta.ca/tac/volumes/18/10/18-10abs.html))


[[!redirects (∞,n)-category of cobordisms]]



