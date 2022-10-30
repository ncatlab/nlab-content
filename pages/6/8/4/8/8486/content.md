

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

Let $(X_1 \stackrel{(d_0, d_1)}{\to} X_0 \times X_0)$ be a [[Lie groupoid]].

A **bisection** of is a [[smooth function]] $\sigma : X_0 \to X_1$ such that

1. $\sigma$ is a [[section]] of $d_1$;

1. $d_0 \circ \sigma : X_0 \to X_0$ is a [[diffeomorphism]].

Bisections naturally form a [[group]] under pointwise composition in $X$, the **group of bisections** of the Lie groupoid.

=-- 

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


[[!redirects bisections of a Lie groupoid]]

[[!redirects group of bisections]]

[[!redirects bisection]]
[[!redirects bisections]]

[[!redirects ∞-bisection]]
[[!redirects ∞-bisections]]


[[!redirects ∞-group of bisections]]
[[!redirects ∞-groups of bisections]]
