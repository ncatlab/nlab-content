
> this entry is going to be one chapter of [[geometry of physics]]

> previous chapters: _[[geometry of physics -- smooth homotopy types|smooth homotopy types]]_

> next chapter: _[[geometry of physics -- principal connections|principal connections]]_

***

#Contents#
* table of contents
{:toc}

## Flat connections

### Model Layer

#### Flat 1-connections

* [[flat connection]]

$X$ [[connected topological space|connected]], $\pi_1(X) \in $[[Grp]] its [[fundamental group]] for any choice of basepoint, then the [[holonomy]] pairing

$$
  hol \colon [S^1,X]\times H^1_{conn}(X,G) \to G

$$

descends to homotopy classes of (based) loops

$$
  hol
  \colon
  H^1_{conn,flat}(X,G)
  \stackrel{\simeq}{\to}
  Hom_{Grp}(\pi_1(X), G)/G
$$

to a _[[bijection]]_ from equivalence classes of [[flat conenction|flat]] $G$-[[principal connections]] to the [[quotient]] set of [[group]] [[homomorphisms]] $\pi_1(X) \to G$ modulo the [[adjoint action]] of $G$ on itself.

### Semantic Layer

+-- {: .num_defn #FlatCohesiveConnection}
###### Definition

For $G \in Grp(\mathbf{H})$ and $X \in \mathbf{H}$ a **flat $G$-connection** $\nabla$ on $X$ is a morphism

$$
  \nabla \colon X \to \flat \mathbf{B}G
  \,.
$$

We write

$$
  \mathbf{H}_{flat}(X, \mathbf{B}G)
  \coloneqq 
  \mathbf{H}(X, \flat \mathbf{B}G)
$$

and accordingly

$$
  H^1_{flat}{X, G} \coloneqq \pi_0 \mathbf{H}_{flat}(X,G)
$$

for the [[cohomology]] of $X \in \mathbf{H}$ **with flat coefficients**.

=--

+-- {: .num_remark}
###### Remark

By adjunction,

$$
  \frac{X \stackrel{\nabla}{\to} \flat \mathbf{B}G}{\Pi(X) \stackrel{transport(\nabla)}{\to} \mathbf{B}G}
$$

a flat $G$-connection is equivalently a morphism 

$$
  transport(\nabla) \colon \Pi(X) \to \mathbf{B}G
  \,.
$$

Since $\Pi(X)$ is the [[fundamental infinity-groupoid]] of $X$, this manifestly encodes the [[higher parallel transport]] of the flat connection.

=--

+-- {: .num_defn}
###### Definition

Write

$$
  UnderlyingBundle_{\mathbf{B}G} \colon \flat \mathbf{B}G \to \mathbf{B}G
$$

for the $(Disc \vdash \Gamma)$-[[unit of an adjunction|counit]]-

=--


+-- {: .num_defn #UnderlyingBundleOfFlatConnection}
###### Definition

For $\nabla \colon X \to \flat \mathbf{B}G$ the [[composition|composite]]

$$
  UnderlyingBundle(\nabla) 
   \colon 
  X 
    \stackrel{\nabla}{\to} 
  \flat\mathbf{B}G
    \stackrel{UnderlyingBundle_{\mathbf{B}G}}{\to}
  \mathbf{B}G
$$

modulates a $G$-[[principal ∞-bundle]] on $X$, by def. \ref{spring}. This we call the **underlying $G$-principal bundle** of $\nabla$.

=--




$$
  ConstantPaths_{X} \colon X \to \Pi(X)
$$

### Syntactic Layer

$$
  \mathbf{B}G \colon Type
  \;\vdash \;
  UnderlyingBundle \colon \flat \mathbf{B}G \to \mathbf{B}G
$$
