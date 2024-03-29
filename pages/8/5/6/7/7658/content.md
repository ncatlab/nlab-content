
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A _double cover_ is equivalently 

* a $\mathbb{Z}_2$-[[principal bundle]];

* an [[etale space]] with local [[sections]] the 2-element set.

## Examples


### Orientation double cover

For $X$ a [[manifold]], not necessarily [[orientation|oriented]] or even orientable, write 

$$
  \array{
    && B O
    \\
    & {}^{\mathllap{\hat T X}}\nearrow & \downarrow
    \\
    X &\stackrel{T X}{\to}& B GL
  }
$$ 

for any choice of [[orthogonal structure]]. The **orientation double cover** or **orientation bundle** of $X$ is the $\mathbb{Z}_2$-[[principal bundle]] classified by the first [[Stiefel-Whitney class]] (of the [[tangent bundle]]) of $X$

$$
  w_1(\hat T X) :  X \stackrel{\hat T X}{\to} B O \stackrel{w_1}{\to} B \mathbb{Z}_2
  \,.
$$

One may identify this with the bundle that over each [[neighbourhood]] $x \in U \subset X$ of a point $x$ has as fibers the two different choices of [[volume forms]] up to positive rescaling (the two different choices of orientation).

More generally, for $E \to X$ any [[orthogonal group]]-[[principal bundle]] classified by a morphism $E : X \to \mathbf{B} O$, the corresponding orientation double cover is the $\mathbb{Z}_2$-bundle classified by

$$
  w_1(E) : X \stackrel{E}{\to} \mathbf{B} O \stackrel{w_1}{\to} \mathbf{B} \mathbb{Z}_2
  \,.
$$

### Real Hopf fibration

The [[real Hopf fibration]] is the non-trivial double cover of the [[circle]] by itself.

### Spin double cover

* [[spin group]]



## Related concepts

* [[orientifold]], [[Jandl gerbe]]

* [[orientation]]

## References

An exposition in a broader context is in the section _[higher spin structures](#)_ at

* _[[geometry of physics]]_.


[[!redirects double covers]]

[[!redirects double covering]]
[[!redirects double coverings]]


[[!redirects orientation double cover]]
[[!redirects orientation double covers]]

[[!redirects orientation bundle]]
[[!redirects orientation bundles]]
