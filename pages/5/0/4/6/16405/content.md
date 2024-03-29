

> This entry contains one chapter of _[[geometry of physics]]_. See there for background and context

> previous chapter _[[geometry of physics -- manifolds and orbifolds]]_

#Contents#
* table of contents
{:toc}

## **$G$-Structure and Cartan geometry**

### Model Layer

#### $G$-Structure

$$
  \mathbf{B}G \to \mathbf{B}K
$$

given a $K$-[[principal bundle]]


$$
  \array{
    \tilde X &\to &\mathbf{B}K
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

a [[reduction of the structure group]] along $G \to K$ is

$$
  \array{
    \tilde X &&\to&& \mathbf{B}G
    \\
    & \searrow &\swArrow_{e}& \swarrow
    \\
    && \mathbf{B}K
  }
$$

#### Examples

##### Vielbein, orthogonal structure, Riemannian geometry
 {#RiemannianGeometry}

* [[vielbein]], [[orthogonal structure]]

[[reduction of the structure group]] along

$\mathbf{B}O(n) \to \mathbf{B}GL(n)$

$$
  \array{
    \tilde X &&\to&& \mathbf{B}O(n)
    \\
    & {}_{\mathllap{\vdash T \Sigma}}\searrow &\swArrow_{e}& \swarrow
    \\
    && \mathbf{B}GL(n)
  }
$$

$e$ is [[vielbein]]: definition of an [[orthonormal frame]]
at each point

###### Electromagnetism in gravitational background

example: the other 2 [[Maxwell equations]]: $\mathbf{d} \star F = j_{el}$.

[[Einstein-Maxwell theory]]

##### Almost complex structure

* [[almost complex structure]]

##### Almost Hermitean structure

* [[almost Hermitean structure]]

##### Almost symplectic structure

* [[almost symplectic structure]]

##### Metaplectic structure

* [[metaplectic structure]]

##### Metalinear structure

* [[metalinear structure]]

##### Generalized complex geometry

* [[generalized complex geometry]]

##### Type II geometry

* [[type II geometry]]

##### Generalized Calabi-Yau structure

* [[generalized Calabi-Yau manifold]]

##### Exceptional generalized geometry

* [[exceptional generalized geometry]]

##### Spin structure, String structure, Fivebrane structure

* [[spin structure]]

* [[string structure]]

* [[fivebrane structure]]




### Semantics Layer

+-- {: .num_defn #GStructure}
###### Definition

Given a homomorphism of groups $G \longrightarrow GL(V)$, a _[[G-structure]]_ on a $V$-manifold $X$ is a lift $\mathbf{c}$ of the [[frame bundle]] $\tau_X$ of prop. \ref{FrameBundle} through this map

$$
  \array{
    X && \stackrel{}{\longrightarrow} && G
    \\
    & {}_{\mathllap{\tau_X}}\searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}GL(V)
  }
  \,.
$$

=--

+-- {: .num_remark #ModuliForGStructures}
###### Remark

As in remark \ref{ModuliForFramings}, it is useful to express def. \ref{GStructure} in terms of the [[slice topos]] $\mathbf{H}_{/\mathbf{B}GL(V)}$. Write $G\mathbf{Struc}\in \mathbf{H}_{/\mathbf{B}GL(V)}$ for the given map $\mathbf{B}G\to \mathbf{B}GL(V)$ regarded as an object in the slice. Then a $G$-structure according to def. \ref{GStructure} is equivalently a choice of morphism in $\mathbf{H}_{/\mathbf{B}GL(V)}$ of the form

$$
  \mathbf{c} \;\colon\; \tau_X \longrightarrow G\mathbf{Struc}
  \,.
$$

In other words, $G\mathbf{Struc} \in \mathbf{H}_{/\mathbf{B}GL(v)}$ is the _[[moduli stack]]_ for $G$-structures.

=--

+-- {: .num_example #GStructureFromLeftTranslationFraming}
###### Example

A choice of [[framing]] $\phi$, def. \ref{Framing}, on a $V$-manifold $X$ induces a [[G-structure]] for any $G$, given by the [[pasting diagram]] in $\mathbf{H}$

$$
  \array{
     X &\longrightarrow& \ast &\longrightarrow&
     \\
     & \searrow & \downarrow & \swarrow
     \\
     && \mathbf{B}GL(V)
  }
$$

or equivalently, via remark \ref{ModuliForFramings} and remark \ref{ModuliForGStructures}, given as the [[composition]]

$$
  \mathbf{c}_{li}
  \;\colon\;
  \tau_X \stackrel{\phi}{\longrightarrow} V\mathbf{Frame} \longrightarrow G\mathbf{Struc}\,.
$$

We call this the _left invariant $G$-structure_.

=--

+-- {: .num_defn #IntegrabilityOfGStructure}
###### Definition

For $X$ a $V$-manifold, then 
a [[G-structure]] on $X$, def. \ref{GStructure}, is 
_[[integrable G-structure|integrable]]_ if for any $V$-[[atlas]] $V \leftarrow U \rightarrow X$  the pullback of the $G$-structure on $X$ to $V$ is equivalent there to  the left-inavariant $G$-structure on $V$ of example \ref{GStructureFromLeftTranslationFraming}, i.e. if we have an [[correspondence]] in the double [[slice topos]] $(\mathbf{H}_{/\mathbf{B}GL(V)})_{/G\mathbf{Struc}}$ of the form

$$
  \array{
     && \tau_U
     \\
     & \swarrow && \searrow
     \\
     \tau_V && \swArrow && \tau_X
     \\
     & {}_{\mathllap{\mathbf{c}_{li}}}\searrow && \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && G \mathbf{Struc}
  }
  \,.
$$

The $G$-structure is _infintesimally integrable_ if this holds true at at after restriction along the [[relative shape modality]] $\flat^{rel} U \to U$, def. \ref{RelativeFlat}, to all the infinitesimal disks in $U$:

$$
  \array{
     && \tau_{\flat^{rel}U}
     \\
     & \swarrow && \searrow
     \\
     \tau_V && \swArrow && \tau_X
     \\
     & {}_{\mathllap{\mathbf{c}_{li}}}\searrow && \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && G \mathbf{Struc}
  }
  \,.
$$

=--

+-- {: .num_defn #CartanGeometry}
###### Definition


Consider an [[infinity-action]] of $GL(V)$ on $V$ which linearizes to the canonical $GL(V)$-action on $\mathbb{D}^V_e$ by def. \ref{GeneralLinearGroup}. Form the [[semidirect product]] $GL(V) \rtimes V$. Consider any group homomorphism $G\to GL(V)$. 

A _$(G\to G\rtimes V)$-[[Cartan geometry]]_ is a $V$-manifold $X$ equipped with a $G$-structure, def. \ref{GStructure}. The Cartan geometry is called _(infinitesimally) integrable_ if the $G$-structure is so, according to def. \ref{IntegrabilityOfGStructure}.

=--

+-- {: .num_remark}
###### Remark

For $V$ an [[abelian group]], then in traditional contexts the infinitesimal integrability of def. \ref{IntegrabilityOfGStructure} comes down to the [[torsion of a G-structure]] vanishing. But for $V$ a [[nonabelian group]], this definition instead enforces that the torsion is on each [[infinitesimal disk]] the intrinsic left-invariant torsion of $V$ itself.

Traditionally this is rarely considered, matching the fact that ordinary [[vector spaces]], regarded as [[translation groups]] $V$, are [[abelian groups]]. But [[super vector spaces]] regarded (in suitable dimension) as [[super translation groups]] are _[[nonabelian groups]]_ (we discuss this in detail below in _[The super-Klein geometry: super-Minkowski spacetime](#SuperMinkowskiSpacetime)_). Therefore super-vector spaces $V$ may carry intrinsic torsion, and therefore first-order integrable $G$-structures on $V$-manifolds are torsion-ful. 

Indeed, this is a phenomenon known as the [[torsion constraints in supergravity]]. Curiously, as discussed there, for the case of [[11-dimensional supergravity]] the [[equations of motion]] of the gravity theory are _equivalent_ to the super-Cartan geometry satisfying this torsion constraint. This way super-Cartan geometry gives a direct general abstract route right into the heart of [[M-theory]].

=--


### Syntax Layer

(...)


