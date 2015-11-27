
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


For $G \to K$ a [[monomorphism]] of groups, a $G$-structure on a $K$-[[principal bundle]] is a _reduction_ of the [[structure group]] from $K$ to $G$.

Alternatively, for $G \to K$ an [[epimorphism]] of groups, a $G$-structure on a $K$-[[principal bundle]] is a _lift_ of the structure group from $K$ to $G$.

A $G$-reduction of the [[frame bundle]] of a [[smooth manifold]] is called a _[[G-structure]]_.

+-- {: .num_remark #EpiMonoNonintrinsic}
###### Remark

As one passes to [[higher differential geometry]], the [[(epi, mono) factorization system]] dissolves into the infinite tower of [[(n-epi, n-mono) factorization systems]], and hence the distinction between reduction and lift of structure groups blurs. One may just consider generally for $G\to K$ a homomorphism of [[∞-groups]] the problem of factoring a [[modulating morphism]] $X\to \mathbf{B}K$ through this morphism, up to a chosen [[homotopy]].

=--

## Definition

We spell out three equivalent definitions.

Let $\mathbf{H}$ be the ambient [[(∞,1)-topos]], let $G,K \in Grp(\mathbf{H})$ be two [[∞-groups]] and let $\phi : G \to K$ be a homomorphism, hence $\mathbf{B}\phi : \mathbf{B}G \to \mathbf{B}K$ the morphism in $\mathbf{H}$ between their [[deloopings]]. Write

$$
  \array{
    K\sslash G &\to& \mathbf{B}G
    \\
    && \downarrow^{\mathrlap{\mathbf{B}\phi}}
    \\
    && \mathbf{B}K
  }
$$

for the corresponding [[fiber sequence]], with $K \sslash G$ the [[homotopy fiber]] of the given morphism. By the discussion at _[[∞-action]]_ this exhibits the canonical $K$-[[∞-action]] on the [[coset]] object $K\sslash G$.

Let furthermore $P \to X$ be a $K$-[[principal ∞-bundle]] in $\mathbf{H}$. By the discussion there this is modulated essentially uniquely by a [[cocycle]] morphism $k : X \to \mathbf{B}K$ such that there is a [[fiber sequence]]

$$
  \array{
    P &\to& X
    \\
    && \downarrow
    \\
    && \mathbf{B}K
  }
  \,.
$$


### Reduction of the cocycle

The reduction of the structure of the cocycle $k$ is a diagram

$$
  \array{
     X &&\stackrel{\sigma}{\to}&& \mathbf{B}G
     \\
     & {}_{\mathllap{k}}\searrow &\swArrow_{\tilde\sigma}& \swarrow
     \\
     && \mathbf{B}K
  }
$$

in $\mathbf{H}$, hence a morphism 

$$
  \sigma : k \to \mathbf{B}\phi
$$

in the [[slice (∞,1)-topos]] $\mathbf{B}_{/\mathbf{B}K}$.

### Section of the associated coset-bundle

By the discussion at [[associated ∞-bundle]] such a diagram is equivalently a section

$$
  \sigma \in \Gamma_X(P \times_{K} K\sslash G)
$$

of the [[associated ∞-bundle|associated]] $K \sslash G$ [[fiber ∞-bundle]].


### Equivariant map to the coset

The above is the [[categorical semantics]] of what in the [[homotopy type theory]] [[internal language]] of $\mathbf{H}$ is given by the [[syntax]]

$$
  \vdash (\prod_{x : \mathbf{B}K} P \to K\sslash G) : Type
  \,.
$$

See the discussion at _[[∞-action]]_.

This expresses the fact that the reduction of the structure group along $\phi$ is equivalently a $K$-equivariant map $P \to K\sslash G$.




## Examples
 {#Examples}

* reduction of [[tangent bundle]] along [[orthogonal group]] inclusion $O(n) \hookrightarrow GL(n)$:  [[vielbein]], [[orthogonal structure]],

* reduction of [[tangent bundle]] along [[symplectic group]] inclusion $Sp(2n) \to GL(2n)$: [[almost symplectic structure]];

  subsequent lift to the [[metaplectic group]] $Mp(2n) \to Sp(2n)$: [[metaplectic structure]]

  induced lift over [[Lagrangian submanifolds]] to the [[metalinear group]] $Ml(n) \to GL(n)$: [[metalinear structure]];

* reduction of [[tangent bundle]] along inclusion of [[complex numbers|complex]] [[general linear group]] $GL(n, \mathbb{C}) \hookrightarrow GL(2n, \mathbb{R})$: [[almost complex structure]];

  further reduction to the [[unitary group]] $U(n) \hookrightarrow GL(n,\mathbb{C})$: [[almost Hermitian structure]];

* reduction of [[generalized tangent bundle]] along $U(n,n) \hookrightarrow O(2n,2n)$: [[generalized complex geometry]], 

  * further reduction along $SU(n,n) \hookrightarrow O(2n,2n)$: [[generalized Calabi-Yau manifold]] ;

    * for $n = 3$: further reduction along $SU(3) \times SU(3) \hookrightarrow SU(3,3)$, [N=2 type II sugra compactification](exceptional+generalized+geometry#HigherSupersymmetry)

* reduction of [[generalized tangent bundle]] along $G_2 \times G_2 \hookrightarrow SO(7,7)$: [[G2-structure]];

* reduction of [[generalized tangent bundle]] along $O(n) \times O(n) \hookrightarrow O(n,n)$: [[generalized vielbein]], [[type II geometry]];

* reduction of [[exceptional tangent bundle]] along [[maximal compact subgroup]] of [[exceptional Lie group]] $H_n \hookrightarrow E_{n(n)}$: [[exceptional generalized geometry]]

* reduction of [[exceptional tangent bundle]] along $SU(7) \hookrightarrow E_{7(7)}$: [N=1 11d sugra compactification on ](exceptional+generalized+geometry#HigherSupersymmetry)

## References

In the generality of [[principal infinity-bundles]], reductions/lifts of structure groups are discused in section 4.3 of

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- General theory]]_ ([arXiv:1207.0248](http://arxiv.org/abs/1207.0248))
 {#NSS}
 
 
[[!redirects lift of structure groups]]
[[!redirects lift of structure group]]
[[!redirects lift of the structure group]]

[[!redirects reduction of structure group]]
[[!redirects reduction of the structure group]]

[[!redirects extension of principal bundles]]
[[!redirects extension of a principal bundle]]

[[!redirects reduction of structure groups]]