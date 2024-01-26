

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Bisections of Lie groupoids#
* table of contents
{:toc}

## Definition

### In components

+-- {: .num_defn #TraditionalDefinition}
###### Definition

Let $X=(X_1 \stackrel{(d_0, d_1)}{\to} X_0 \times X_0)$ be a [[Lie groupoid]].

A **bisection** of $X$ is a [[smooth function]] $\sigma : X_0 \to X_1$ such that

1. $\sigma$ is a [[section]] of $d_1$;

1. $d_0 \circ \sigma : X_0 \to X_0$ is a [[diffeomorphism]].

Bisections naturally form a [[group]] under pointwise composition in $X$, the **group of bisections** of the Lie groupoid.
=--

One can prove that the bisection group is a [[infinite-dimensional Lie group]] in the sense of Milnor (see Neeb's survey) (under some mild assumptions on the underlying Lie groupoid). 
The infinite-dimensional Lie group of bisections is closely connected to the underlying Lie groupoid (see references below), e.g.

1. From the knowledge of the smooth structure of the bisection group and the manifold of units, one can even reconstruct the underlying Lie groupoid (again under some assumptions).

1. The construction is functorial in a suitable sense and extending this one can even relate (smooth) representations of Lie groupoids to smooth representations of its bisection group 
 

### Abstractly

Let $\mathbf{H} = $ [[Smooth∞Grpd]]. Let $X \in \mathbf{H}$ be equipped with an _atlas_, hence with an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] $U \to X$ out of a [[0-truncated object]]. 

We may regard this atlas as an object in the [[slice (∞,1)-topos]]
$\mathbf{X} \in \mathbf{H}_{/X}$

+-- {: .num_defn}
###### Definition

The **[[smooth ∞-group]] of bisections** of $\mathbf{X}$ is its [[automorphism ∞-group]]

$$
  \mathbf{BiSect}(X,U) \coloneqq
  \mathbf{Aut}_{/X}(\mathbf{X}, \mathbf{X})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

For $X$ a 1-groupoid as above and $U = X_0$, a bisection is precisely a smooth [[natural transformation]] of the form

$$
  \array{
    U &&\stackrel{\simeq}{\to}&& U
    \\
    & \searrow &\swArrow_{\mathrlap{\eta}}& \swarrow
    \\
    && X
  }
  \,.
$$

Here the top morphism is a [[diffeomorphism]] $\phi : X \to X$
and since the diagonal morphisms are identities onto the object manifold the component map of $\eta$ is

$$
  x \mapsto  (x \stackrel{\eta(x)}{\to} \phi(x))  \,.
$$

This is precisely the bisection in the traditional sense of 
def. \ref{TraditionalDefinition}.

=--

## Properties

### Relation to Lie-Rinehart algebras

For $U \to X$ a Lie groupoid with atlas as above, write
$\mathfrak{g} = Lie(\mathbf{BiSect}(X,U))$
for the [[Lie algebra]] of the group of bisections.
Then $(C^\infty(X), \mathfrak{g})$ is the [[Lie-Rinehart algebra]] corresponding to the [[Lie algebroid]] of the Lie groupoid.

### Relation to Atiyah groupoids

> for the moment see at _[[Atiyah groupoid]]_ and _[[higher Atiyah groupoid]]_.

## References

* [[Ieke Moerdijk]], [[Janez Mrčun]], p. 114 of _[[Introduction to foliations and Lie groupoids]]_, Cambridge Studies in Advanced Mathematics __91__, 2003. x+173 pp. ISBN: 0-521-83197-0

* [[Alexander Schmeding]], [[Christoph Wockel]], _The Lie group of bisections of a Lie groupoid_ ([arXiv:1409.1428](http://arxiv.org/abs/1409.1428))

* [[Alexander Schmeding]], [[Christoph Wockel]], _(Re)constructing Lie groupoids from their bisections and applications to prequantisation_ ([arXiv:1506.05415](https://arxiv.org/pdf/1506.05415.pdf))

* [[Alexander Schmeding]], [[Christoph Wockel]], _Functorial aspects of the reconstruction of Lie groupoids from their bisections_ ([arXiv:1506.05587](https://arxiv.org/abs/1506.05587))

* Habib Amiri, [[Alexander Schmeding]], _Linking Lie groupoid representations and representations of infinite-dimensional Lie groups_ ([arXiv:1805.03935
](https://arxiv.org/pdf/1805.03935.pdf))

[[!redirects bisections of a Lie groupoid]]

[[!redirects group of bisections]]

[[!redirects bisection]]
[[!redirects bisections]]

[[!redirects ∞-bisection]]
[[!redirects ∞-bisections]]


[[!redirects ∞-group of bisections]]
[[!redirects ∞-groups of bisections]]
