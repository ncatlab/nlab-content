[[!redirects connection on a principal infinity-bundle]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In every [[cohesive (∞,1)-topos]] there is an <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#ChernWeilTheory">intrinsic notion of ∞-Chern-Weil theory</a> that gives rise to a notion of _connection_ on [[principal ∞-bundle]]s. We describe here details of the realization of this general abstract structure in the cohesive $(\infty,1)$-topos [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s.

For $G$ an [[∞-Lie group]], a _connection_ on a smooth $G$-[[principal ∞-bundle]] is a structure that supports the [[Chern-Weil homomorphism in Smooth∞Grpd]]: it interpolates between the [[nonabelian cohomology]] class $c \in H^1_{smooth}(X,G)$ of the bundle and its intrinsic [[curvature characteristic form|curvature characteristic class]]es in [[de Rham cohomology]] $H_{dR}^{n+1}(X)$ and furthermore in [[ordinary differential cohomology]] $H^n_{diff}(X,U(1))$. 

This generalizes the  notion of [[connection on a bundle]] and the ordinary [[Chern-Weil homomorphism]] in [[differential geometry]].


## Definition

(...)

We discuss now a generalization of the notion of [[connection on a bundle]] to [[∞-Lie algebra valued forms]]s on [[principal ∞-bundle]]s. It generalizes the notion of (pseudo-)connections on abelian $\infty$-bundles discussed at [[circle n-bundle with connection]] and serves to interpolate from a principal $\infty$-bundle to its [[curvature characteristic form]]s and hence to implement the [[∞-Chern-Weil theory|∞-Chern-Weil homomorphism]].

From the discussion at <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#Connections">differential cohomology in an (∞,1)-topos -- Local connections</a> we have that these may be represented by cocycles with values in the presheaf of diagrams

$$
  \array{
    (-) &\to& \mathbf{B}G &&& underlying\;cocycle
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_R(-) &\to& \mathbf{B}\mathbf{E}G
    &&&
    \; connection\;and\;curvature
  }
  \,,
$$

where $\mathbf{E}G$ is a [[groupal model for universal principal ∞-bundles]]. The following construction effectively obtains such presheaves from [[Lie integration]] of diagrams of [[∞-Lie algebroid]]s.

Recall from [[Lie integration]] that for $\mathfrak{g}$ an [[∞-Lie algebra|Lie n-algebra]], we say the [[∞-Lie group|Lie n-group]] $G$ integrating it is that given by

$$
  \mathbf{B}G := \mathbf{cosk}_{n+1} \exp(\mathfrak{g})
  :
  \mathbf{cosk}_{n+1}(
    (U,[n]) \mapsto
    Hom_{dgAlg}(CE(\mathfrak{g}), C^\infty(U) \otimes' \Omega^bullet(\Delta^n ))
  )
  \,.
$$

We write $inn(\mathfrak{g})$ for the [[∞-Lie algebra]] whose [[Chevalley-Eilenberg algebra]] is the [[Weil algebra]] of $\mathfrak{g}$:

$$
  CE(inn(\mathfrak{g})) = W(\mathfrak{g})
  \,.
$$

There is a canonical morphism $\mathfrak{g} \to inn(\mathfrak{g})$ whose [[nLab:Lie integration]] is $\mathbf{B}G \to \mathbf{B}\mathbf{E}G$ for $\mathbf{E}G$ a [[groupal model for universal principal ∞-bundles|groupal model for the universal G-principal ∞-bundle]].

+-- {: .un_def }
###### Definition
**(coefficient for $\infty$-Lie algebra valued connections)**

With $\mathfrak{g}$ and $G$ as above, write $\mathbf{B}G_{diff} in [CartSp^{op}, sSet]$ for the [[nLab:simplicial presheaf]] given by 

$$
  \mathbf{B}G_{diff}
  =
  \mathbf{cosk}_{n+1}
  (
  (U,[k])
  \mapsto
  \left\{
    \array{
       \Omega^\bullet_{vert}(U \times \Delta^k)
       &\stackrel{A_{vert}}{\leftarrow}& CE(\mathfrak{g})
       \\
       \uparrow && \uparrow
       \\
       \Omega^\bullet(U \times \Delta^k)
       &\stackrel{A}{\leftarrow}&
       W(\mathfrak{g})
    }
  \right\}
  )
  \,.
$$

=--

Here $\Omega^\bullet(U \times \Delta^k)_{vert}$ is the dg-algebra of [[vertical differential form]]s on the bundle $U \times \Delta^n \to U$.

+-- {: .un_remark }
###### Remark

For given $U,[k]$ the commuting diagram of [[dg-algebra]] morphism encodes a collection of [[∞-Lie algebra valued differential forms]] on $U \times\Delta^k$ such that their [[curvature]] forms have no components with _all_ legs on $\Delta^k$.

=--

+-- {: .un_prop }
###### Proposition

The evident forgetful morphism

$$
  \mathbf{B}G_{diff} \to \mathbf{B}G
$$

is an acyclic fibration in $[CartSp^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

By the [[free functor|free property]] of $W(\mathfrak{g})$ we have lifts in all diagrams

$$
  \array{
     \partial \Delta[k] &\to& \mathbf{B}G_{diff}(U)
     \\
     \downarrow && \downarrow 
     \\
     \Delta[k] &\to& \mathbf{B}G(U)
  }
  \,.
$$

The bottom morphism is a collection of forms on $U \times \Delta^k$, satisfying a flatness condition for their $d_{\Delta^k}$-differentials. The top morphism is a collection of forms on $U \times \partial \Delta^k $given by a morphism of graded algebra $\wedge^\bullet \mathfrak{g}^* \to \Omega^\bullet(U \times\Delta^k )$ such that those with no component along $U$ coincide with the restriction of those of the bottom morphism to the boundary. These extend uniquely to the interior of the simplex. The remaining forms may be smoothly interpolated for instance to 0 in the interior of the simplex, while keeping at least one leg along $U$. Since for the top morphism there is no condition on the differentials, any choice will do.

So the morphism is an acyclic [[Kan fibration]] over each $U$, and hence an acyclic fibration in the projective [[model structure on simplicial presheaves]].

=--



+-- {: .un_def }
###### Definition
**(coefficient for $\infty$-Lie algebra valued connections)**

Write $\mathbf{B}G_{conn} \hookrightarrow \mathbf{B}G_{diff}$
for the sub-presheaf assigning to $(U,[k])$ only those 
[[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebra valued differential forms]] whose [[curvature characteristic form]]s have no dependency on the simplicial directions:

$$
  \mathbf{B}G_{conn'}
  =
  \mathbf{cosk}_{n+1}
  (
  (U,[k])
  \mapsto
  \left\{
    \array{
       \Omega^\bullet(U \times \Delta^k)_{vert}
       &\stackrel{A_{vert}}{\leftarrow}& CE(\mathfrak{g})
       \\
       \uparrow && \uparrow
       \\
       \Omega^\bullet(U \times \Delta^k)
       &\stackrel{A}{\leftarrow}&
       W(\mathfrak{g})
       \\
       \uparrow && \uparrow
       \\
       \Omega^\bullet(U)
       &\stackrel{\langle F_A \rangle}{\leftarrow}&
       inv(\mathfrak{g})
    }
  \right\}
  )
$$

and $\mathbf{B}G_{conn} \subset \mathbf{B}G_{conn'}$ for the supobject on those elements for which the [[curvature]]s themselves vanish when evaluated on a tangent $v \in \Gamma(T \Delta^l)$ to the simplex

$$
  \iota_v F_A = 0
  \,.
$$

=--



+-- {: .un_def }
###### Definition
**($\infty$-Lie algebra valued (pseudo-)connections)**

Let $\hat X \in [CartSp^{op}, sSet]_{proj}$ be a (cofibrant) object, such that a morphism $\hat X\to \mathbf{B}G$ is a cocycle for a $G$-[[principal ∞-bundle]] on $\hat X$.

We say a morphism 

$$
  \nabla : \hat X \to \mathbf{B}G_{diff}
$$ 

is a **pseudo-connection** on the principal $\infty$-bundle given by the composite $\hat X\to \mathbf{B}G_{diff}\to \mathbf{B}G$.

We say this is a **genuine connection** if it factors through the inclusion $\mathbf{B}G_{conn} \to \mathbf{B}G_{diff}$.


=--

$$
  \array{
    && \mathbf{B}G_{conn} &&& connection
    \\
    & \nearrow & \downarrow
    \\
    \hat X &\to& \mathbf{B}G_{diff} &&& pseudo-connection
    \\
    & \searrow & \downarrow^{\mathrlap{\simeq}}
    \\
    && \mathbf{B}G &&& principal\;\infty-bundle
  }
  \,.
$$

Such $\infty$-Lie algebra valued connection data was introduced in ([SSSI](#SSSI))

+-- {: .un_def }
###### Definition

We write

$$
  \mathbf{H}_{conn}(-, \mathbf{B}G) := \mathbf{H}(-, \mathbf{B}G_{conn})
  \,.
$$

=--


## Properties

### Existence of $\infty$-connections

+-- {: .un_prop #ExistenceOfInftyConnections}
###### Proposition
**(existence of $\infty$-connections)**

In $\mathbf{H} = $ [[nLab:?LieGrpd]] over a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] $X$, every $G$-[[nLab:principal ∞-bundle]] for $G = \tau_n \exp(\mathfrak{g})$ obtained from [[nLab:Lie integration]] admits a genuine $\infty$-connection.

=--

+-- {: .proof}
###### Proof

By the assumptions on $X$, there is a [[nLab:good open cover]] $\{U_i \to X\}$ and a [[nLab:partition of unity]] $(\rho_i \in C^\infty(U_i))$ subordinate to that cover. 

Let $C(\{U_i\})$ be the [[nLab:Cech nerve]] of the cover and let $g : C(\{U_i\}) \to cosk_{n+1} \exp(\mathfrak{g})$ be a cocycle for the given $G$-principal $\infty$-bundle on $X$. This is given by a collection of [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebra valued differential forms]]

$$
  ( C^\infty(U_{i_0, \cdots i_k})\otimes \Omega^\bullet(\Delta^k) 
  \leftarrow
  CE(\mathfrak{g}) : \lambda_{i_0, \cdots, i_n})
  \,.
$$

We need to extend these to a cocycle of differential forms

$$
  ( \Omega^\bullet(U_{i_0, \cdots i_k})\otimes \Omega^\bullet(\Delta^k) 
  \leftarrow
  W(\mathfrak{g}) : (\lambda_{i_0, \cdots, i_n},A_{i_0, \cdots, i_n})) 
$$

such that the curvature components have no leg along the simplices.  This constraint is hierarchy of systems of partial differential equations. consider first the $A_{i_0, \cdots, i_k}(\frac{\partial}{\partial u}, \{\frac{\partial}{\partial t_r}\})$ with exactly one leg along $U_{i_0, \cdots, i_k}$. For these the constraint is a system of differential equations of the schematic form


$$
  \frac{\partial}{\partial t_r} A
  =
  d_U \lambda(\frac{\partial}{\partial t_r})
  + 
  [\lambda(\frac{\partial}{\partial t_r}), A]
$$

By the [[nLab:Bianchi identity]] and the fact that the curvature with all components along the simplex vabishes, it follows that this is an integrable system of partial differential equations. Fixing the boundary condition that $A$ vanishes in the $0$-corner of $\Delta^k$, this has a unique solution. $\hat A_{i_0, \cdots, i_k}$.

Set then 

$$
  A_{i_1, \cdots, i_k} := \sum_{i_0} \rho_{i_0} \hat A_{i_0, \cdots, i_k}|_{\delta_0(\Delta^k)}
  \,.
$$


The system of differential forms obtained this way does satisfy the cocycle condition and the curvature component with one leg along $U$ and the other legs along the simplices vanish:

$$
  \frac{\partial}{\partial t_r} 
  A_{i_1, \cdots, i_k}
  =
  \frac{\partial}{\partial t_r} 
\sum_{i_0} \rho_{i_0}  \hat A_{i_0, \cdots, i_k}
  =
  \sum_{i_0} \rho_{i_0} d_U \lambda(\frac{\partial}{\partial t_r})
  + 
  [\lambda(\frac{\partial}{\partial t_r}), \sum_{i_0} \rho_{i_0} \hat A_{i_0, \cdots, i_k}]
  =
  d_U \lambda(\frac{\partial}{\partial t_r})
  + 
  [\lambda(\frac{\partial}{\partial t_r}), A_{i_1, \cdots, i_k}]
  \,.
$$

Next continue iteratively in the above fashion, by induction on the number of legs of the forms along $U$.

=--



## Related concepts

* [[connection on a bundle]]

* [[connection on a 2-bundle]] / [[connection on a gerbe]] / [[connection on a bundle gerbe]]

* [[connection on a 3-bundle]] / [[connection on a bundle 2-gerbe]]

* **connection on an ∞-bundle**



## References

The local differential form data of $\infty$-connections was discussed in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]],
  _$L_\infty$-algebra connections_ in Fauser (eds.) Recent Developments in QFT, Birkh&#228;user (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)
  {#SSSI}

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential String- and Fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">web</a>).
{#SSSIII}


The global description is discussed in 

* [[Domenico Fiorenza]], [[Urs Schreiber]] , [[Jim Stasheff]], _Cech cocycles for differential characteristic classes -- An $\infty$-Lie theoretic construction_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#FSS">web</a>)


[[!redirects ∞-connection on a principal ∞-bundle]]
[[!redirects ∞-connection on a principal ∞-bundle]]

[[!redirects connection on a principal ∞-bundle]]

[[!redirects connection on an ∞-bundle]]
[[!redirects connections on an ∞-bundle]]

[[!redirects connection on an infinity-bundle]]

[[!redirects connections on ∞-bundles]]
[[!redirects connections on infinity-bundles]]

[[!redirects connection on a smooth principal ∞-bundle]]
[[!redirects connections on smooth principal ∞-bundles]]