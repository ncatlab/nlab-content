[[!redirects ∞-Chern-Weil theory]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

> This entry is based on material that was being developed on the personal web of [[Urs Schreiber]]: [[schreiber:differential cohomology in an (∞,1)-topos -- examples|here]]. It has been moved here when [[Domenico Fiorenza]] indicated inclination to work on this, too. 


#Contents#
* table of contents
{:toc}

## Idea

By _$\infty$-Chern-Weil theory_ we want to understand the generalization of ordinary [[Chern-Weil theory]] to [[(∞,1)-category theory]]: where [[Lie group]]s are generalized to [[∞-Lie group]]s, [[Lie algebra]]s are generalized to [[∞-Lie algebra]]s and [[principal bundle]]s to [[principal ∞-bundle]]s.

Using the notion of [[schreiber:differential cohomology in an (∞,1)-topos]] applied to the [[(∞,1)-topos]] $\mathbf{H} =$[[?LieGrpd]] of [[∞-Lie groupoids]] there is a very general abstract notion of refinement of [[characteristic class]]es in [[cohomology]] to [[curvature characteristic forms|curvature characteristic classes]] in [[differential cohomology]]. &#228;

The main construction in ∞-Chern-Weil theory is a concrete _model_ or _presentation_ of this very abstract operation in terms of [[Lie integration]] of objects in [[∞-Lie algebra cohomology]]. This construction is seen to be the higher analog of the [[Chern-Weil homomorphism]]. Its crucial intermediate step is the definition and construction of _$\infty$-connections_ on [[principal ∞-bundle]]s. 

This model is build on concrete constructions in [[differential geometry]] and can be studied and appreciated in itself without recourse to the higher topos theory that we claim it provides a model for. The so inclined reader can ignore all the general abstract discussion in the following and concentrate on the concrete differential geometry. 



## $\infty$-Chern-Weil theory {#ChernWeil}

For $G,A$ [nLab:∞-group]]s in an [[nLab:∞-connected (∞,1)-topos]] $\mathbf{H}$ with [[nLab:delooping]]s $\mathbf{B}G$ and $\mathbf{B}A$, respectively, every [[nLab:characteristic class]] $c : \mathbf{B}G \to A$ serves to pull back the <a href="spring">canonical intrinsic curvature form</a> $curv_A : A \to \mathbf{\flat}_{dR} \mathbf{B}A$ to an <a href="spring">intrinsic differential form</a> $curv_A\circ c  : \mathbf{B}G \to \mathbf{\flat}_{dR} \mathbf{B}A$ on $\mathbf{B}G$. 

For $G$ an ordinary [[nLab:Lie group]] regarded naturally as an object in $\mathbf{H} = $ [[nLab:?LieGrpd]], we show that the ordinary [[nLab:Chern-Weil homomorphism]] for $G$-[[nLab:principal bundle]]s may be understood as a concrete _model_ for this simple abstract situation, which applies to those characteristic classes $c$ that happen to be in the image of the [Lie intgeration of Lie algebra cocycles](spring).

More generally, this construction applies for $G$ an [[nLab:∞-Lie group]] with [[nLab:∞-Lie algebra]] $\mathfrak{g}$ and $c$ a characteristic class on $\mathbf{B}G$ that arises from Lie integration of a cocycle in the [[nLab:∞-Lie algebra cohomology]] of $\mathfrak{g}$.

The ordinary [[nLab:Chern-Weil homomorphism]] uses a [[nLab:connection on a bundle]] $\nabla$ as an intermediate tool for interpolating from a $G$-[[nLab:principal bundle]] to its curvature characteristic, represented by the [[nLab:curvature characteristic form]] $\langle F_\nabla \rangle$, where $F_\nabla$ is the [[nLab:curvature]] of $\nabla$ and $\langle - \rangle$ is an [[nLab:invariant polynomial]] on $\mathfrak{g}$. The choice of connection in this construction may be understood as providing a correspondence space in the following construction.

We know from the discussion of abelian differential cohomology [above](#AbGerbe) that the intrinsic morphism

$$
  \mathbf{B}^n \mathbb{R}/\mathbb{Z} \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}/\mathbb{Z}
$$

in $\mathbf{H} = \infty LieGrpd$ is modeled in $[CartSp^{op}, sSet]_{proj,cov}$ by the correspondence

$$
  \array{
     \mathbf{B}^n \mathbb{R}/\Gamma_{diff,simp} &\stackrel{curv}{\to}&
     \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}_{simp}
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     \mathbf{B}^n \mathbb{R}/\Gamma_{simp}
  }
  \,.
$$

If we write 

$$
  \exp(b^{n-1}\mathbb{R} \to inn(b^{n-1}\mathbb{R}))
  :
  \mathbf{cosk}_{n+1}(
  (U,[k])
  \mapsto
  \left\{
    \array{
      C^\infty(U)\otimes \Omega^\bullet(\Delta^k)
      &\leftarrow&
      CE(b^{n-1}\mathbb{R})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
      &\leftarrow&
      W(b^{n-1}\mathbb{R})
    }
  \right\}
  )
$$

and so forth, then this correspondence is

$$
  \array{
     \exp(b^{n-1}\mathbb{R}\to inn(b^{n-1}\mathbb{R}))
     &\to&
     \exp(* \to b^n \mathbb{R})
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     \exp(b^{n-1}\mathbb{R}\to *)
  }
  \,.
$$

If now $\mathbf{B}G \to \mathbf{B}^n \mathbb{R}/\mathbb{Z}$ is modeled by the Lie integration of a cocycle $\mu$ on a Lie $k$-algebra

$$
  \mathbf{cosk}_{k+1} \exp(\mathfrak{g})
  \stackrel{\exp(\mu)}{\to}
  \exp(b^{n-1}\mathbb{R})/\Gamma
  =
  \exp(b^{n-1}\mathbb{R} \to *)/\Gamma
$$

for $k \geq n-1$, then the total intrinsic differential form $\mathbf{B}G \to \mathbf{B}^n \mathbb{R}/\Gamma \to \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}$ is modeled by the zig-zag of morphisms

$$
  \array{
     && \exp(b^{n-1}\mathbb{R}\to inn(b^{n-1}\mathbb{R}))
     &\to&
     \exp(* \to b^n \mathbb{R})
     \\
     && \downarrow^{\mathrlap{\simeq}}
     \\
     \mathbf{cosk}_{k+1}\exp(\mathfrak{g})
     &\stackrel{\exp(\mu)}{\to}& 
     \exp(b^{n-1}\mathbb{R}\to *)
  }
$$

in $[CartSp^{op}, sSet]$. In order to compute with such zig-zags of morphisms, in particular in order to compute [[nLab:homotopy fiber]]s, it is helpful to complete this to a single correspondence. There is a fairly evident choice for the tip of this total corresponence, namely 

$$
  \mathbf{B}G_{diff}
  :=
  \mathbf{cosk}_{n+1} \exp(\mathfrak{g} \to inn(\mathfrak{g}))
  \,.
$$

It remains to complete the square and extend the [[nLab:∞-Lie algebra cohomology|∞-Lie algebra cocycle]] $\mu : \mathfrak{g} \to b^{n-1}\mathb{R}$ to a morphism $(\mathfrak{g} \to inn(\mathfrak{g})) \to (b^{n-1}\mathbb{R} \to inn(b^{n-1}\mathbb{R}))$. This is accomplished by an [[nLab:invariant polynomial]] 

$$
  \langle -\rangle_\mu
  :
  inn(\mathfrak{g}) \stackrel{(\langle - \rangle_\mu, cs_\mu)}{\to} 
  inn(b^{n-1}\mathbb{R})
  \to
  b^n \mathbb{R}
$$

which is in transgression with $\mu$, witnessed by the [[nLab:Chern-Simons form|Chern-Simons element]] $cs_\mu$. Using this, we obtain the total diagram

$$
  \array{
     \mathbf{cosk}_{k+1}\exp(\mathfrak{g} \to inn(\mathfrak{g}))
     &\stackrel{(\langle - \rangle_\mu, cs_\mu)}{\to}& 
     \exp(b^{n-1}\mathbb{R}\to inn(b^{n-1}\mathbb{R}))
     &\to&
     \exp(* \to b^n \mathbb{R})
     \\
     \downarrow^{\mathrlap{\simeq}}
     && \downarrow^{\mathrlap{\simeq}}
     \\
     \mathbf{cosk}_{k+1}\exp(\mathrak{g})
     &\stackrel{\exp(\mu)}{\to}& 
     \exp(b^{n-1}\mathbb{R}\to *)
  }
  \,.
$$

By the fact that this commutes, we have that the correspondence

$$
  \left(
  \array{
    \mathbf{B}G_{diff,simp}
    &\to&
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}_{simp}
    \\
    \downarrow
    \\
    \mathbf{B}G_{simp}
  }
  \right)
  \;\;
  :=
  \;\;
  \left( 
  \array{
    \mathbf{cosk}_{k+1}\exp(\mathfrak{g} \to inn(\mathfrak{g}))
    &\to&
    \exp(* \to b^n \mathbb{R})
    \\
    \downarrow
    \\
    \mathbf{cosk}_{k+1}\exp(\mathfrak{g} \to *)
  }
  \right)
$$

in $[CartSp^{op}, sSet]_{proj,cov}$ models the intrinsic curvature characteristic form $\mathbf{B}G \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}$.

We may identify cocycles with values in $\mathbf{B}G_{diff}$ as _(pseudo)-$\infty$-connections_ on the underlying $\mathbf{B}G$-cocycle. If their curvature is represented by a cocycle in $\mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}$ which is given by a globally defined form, then these are _genuine_ $\infty$-connections. In either case, they serve as an intermediate step in computing the curvature characteristics.


### $\infty$-Lie algebra valued connections {#InfinityLieAlgebraConnection}

We discuss now a generalization of the notion of [[nLab:connection on a bundle]] to [[∞-Lie algebroid valued differential forms|∞-Lie algebra valued connection]] on [[nLab:principal ∞-bundle]]s. It generalizes the notion of (pseudo-)connections on abelian $\infty$-bundles discussed [above](#AbGerbesConnection) and serves to interpolate from a principal $\infty$-bundle to its [[nLab:curvature characteristic form]]s and hence to implement the [∞-Chern-Weil homomorphism](#InfChernWeil).

From the discussion at [differential cohomology in an (∞,1)-topos -- Local connections](#spring) we have that these may be represented by cocycles with values in the presheaf of diagrams

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

where $\mathbf{E}G$ is a [[nLab:groupal model for universal principal ∞-bundles]]. The following construction effectively obtains such presheaves from [[nLab:Lie integration]] of diagrams of [[nLab:∞-Lie algebroid]]s.

Recall that for $\mathfrak{g}$ an [[nLab:∞-Lie algebra|Lie n-algebra]], we say the [[nLab:∞-Lie group|Lie n-group]] $G$ integrating it is that given by

$$
  \mathbf{B}G := \mathbf{cosk}_{n+1} \exp(\mathfrak{g})
  :
  \mathbf{cosk}_{n+1}(
    (U,[n]) \mapsto
    Hom_{dgAlg}(CE(\mathfrak{g}), C^\infty(U) \otimes' \Omega^bullet(\Delta^n ))
  )
  \,.
$$

We write $inn(\mathfrak{g})$ for the [[nLab:∞-Lie algebra]] whose [[Chevalley-Eilenberg algebra]] is the [[nLab:Weil algebra]] of $\mathfrak{g}$:

$$
  CE(inn(\mathfrak{g})) = W(\mathfrak{g})
  \,.
$$

There is a canonical morphism $\mathfrak{g} \to inn(\mathfrak{g})$ whose [[nLab:Lie integration]] is $\mathbf{B}G \to \mathbf{B}\mathbf{E}G$ for $\mathbf{E}G$ a [[nLab:groupal model for universal principal ∞-bundles|groupal model for the universal G-principal ∞-bundle]].

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
       C^\infty(U) \otimes' \Omega^\bullet(\Delta^k)
       &\leftarrow& CE(\mathfrak{g})
       \\
       \uparrow && \uparrow
       \\
       \Omega^\bullet(U \times \Delta^k)
       &\leftarrow&
       W(\mathfrak{g})
    }
  \right\}
  )
  \,.
$$

=--

+-- {: .un_remark }
###### Remark

For given $U,[k]$ the commuting diagram of [[nLab:dg-algebra]] morphism encodes a collection of [[∞-Lie algebroid valued differential forms|∞-Lie algebra valued differential forms]] on $U \times\Delta^k$ such that their [[curvature]] forms have no components with all legs on $\Delta^k$.

=--

+-- {: .un_def }
###### Definition
**(coefficient for genuine $\infty$-Lie algebra valued connections)**

Write $\mathbf{B}G_{conn} \hookrightarrow \mathbf{B}G_{diff}$
for the sub-presheaf assigning to $(U,[k])$ only those 
[[∞-Lie algebroid valued differential forms|∞-Lie algebra valued differential forms]] whose [[curvature]] forms have _no_ leg along $\Delta^n$.

This are those morphisms of [[nLab:dg-algebra]]s $\Omega^\bullet(U \times \Delta^k) \leftarrow W(\mathfrak{g})$ such that the underlying morphism of graded algebras fits into a diagram

$$
  \array{
    \Omega^\bullet(U) \otimes \Omega^\bullet(\Delta^n) &\leftarrow& W(\mathfrak{g})
    \\
    \uparrow && \uparrow
    \\
    C^\infty(U) \otimes' \Omega^\bullet(\Delta^n)
    &\leftarrow&
    \wedge^\bullet \mathfrak{g}^*[1]
  }
  \,.
$$

of graded algebras.

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

By the [[nLab:free functor|free property]] of $W(\mathfrak{g})$ we have lifts in all diagrams

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

So the morphism is an acyclic [[nLab:Kan fibration]] over each $U$, and hence an acyclic fibration in the projective [[nLab:model structure on simplicial presheaves]].

=--


+-- {: .un_def }
###### Definition
**($\infty$-Lie algebra valued (pseudo-)connections)**

Let $\hat X \in [CartSp^{op}, sSet]_{proj}$ be a (cofibrant) object, such that a morphism $\hat X\to \mathbf{B}G$ is a cocycle for a $G$-[[nLab:principal ∞-bundle]] on $\hat X$.

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

Such $\infty$-Lie algebra valued connection data was introduced and studied in (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">SSSI</a>).


### Curvature characteristics {#InfChernWeil}


+-- {: .un_def }
###### Definition
**(Chern-Weil curvature characteristics)**

Let $\langle -\rangle : inn(\mathfrak{g}) \to b^{p} \mathbb{R}$ be an [[nLab:invariant polynomial]] on the [[nLab:∞-Lie algebra|Lie n-algebra]] $\mathfrak{g}$. Postcomposition with the corresponding diagram of dg-algebras

$$
  \array{
    CE(\mathfrak{g}) &\leftarrow& 0
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{g}) &\stackrel{\langle -\rangle}{\leftarrow}&
    CE(b^p \mathbb{R})
  }
$$

induces a morphism of [[nLab:simplicial presheaves]]

$$
   \langle F_{(-)} \rangle
   :
  \mathbf{B}G_{diff} \to 
  \mathbf{cosk}_{n+1} \mathbf{\flat}_{dR} \mathbf{B}^{p+1}\mathbb{R}_{simp}
$$

into the $(n+1)$-[[nLab:simplicial skeleton|coskeleton]] of the model for the de Rham coefficient object $\mathbf{\flat}_{dR}\mathbf{B}^{p+1}\mathbb{R}$ discussed [above](#U1FromLieIntegration).

For $\nabla : \hat X \to \mathbf{B}G_{diff}$ a connection, we call the 
induced intrinsic de Rham cocycle

$$
  \langle F_\nabla \rangle : 
  \hat X \stackrel{\nabla}{\to}  
  \mathbf{B}G_{diff}
  \stackrel{\langle -\rangle}{\to}
  \mathbf{cosk}_{n+1} \mathbf{\flat}_{dR} \mathbf{B}^{p+1}\mathbb{R}_{simp} 
$$

the Chern-Weil [[nLab:curvature characteristic form]] of $\nabla$ with respect to $\langle -\rangle$. 


=--

+-- {: .un_lemma }
###### Lemma

For $\nabla : \hat X \to \mathbf{B}G_{conn} \hookrightarrow \mathbf{B}G_{diff}$ a genuine connection, the induced curvature characteristic forms are globally defined closed forms, in that their cocycle factors through the sheaf $\Omega^{p+1}_{cl}(-)$ of closed $(p+1)$-forms:

$$
  \array{
     && \mathbf{B}G_{conn} &\stackrel{\langle F_{(-)}\rangle}{\to}& \Omega^{p+1}_{cl}(-)
     \\
    & \nearrow & \downarrow && \downarrow
    \\
    \hat X &\stackrel{}{\to}&
    \mathbf{B}G_{diff} 
    &\stackrel{\langle F_{(-)}\rangle}{\to}&  
    \mathbf{cosk}_{n+1} \mathbf{\flat}_{dR} \mathbf{B}^{p+1} \mathbb{R}_{simp}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

for given $(U,[k])$ notice that $\langle F_{\nabla}\rangle(U,[k]) \in \Omega^\bullet(U\times \Delta^k)$ is closed and for $\nabla$ a genuine connection has no leg along $\Delta^k$: for $\partial_t$ a vector field along $\Delta^k$ we have $\iota_{\partial_t} \langle F_A\rangle = 0$. Therefore the [[nLab:Lie derivative]] along a vector $\partial_t$ along the simplex vanishes:

$$
  \mathcal{L}_t \langle F_A\rangle = d \iota_t \langle F_A\rangle +
  \iota_t d \langle F_A\rangle = 0  
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

As for the groupal case [above](#AbGerbesConnection), we hence find that the genuine $\infty$-connections are selected among all pseudo-connections as those whose curvature characteristic has a 0-[[nLab:truncated]] cocycle representative. 

=--

So a genuine $\infty$-Lie algebra valued connection is a cocycle with values in the $(n+1)$-coskeleton of the simplicial presheaf of diagrams, which over $U,[k]$ assigns the set of diagrams

$$
  \array{
    C^\infty(U)\otimes \Omega^\bullet(\Delta k)
    &\leftarrow&
    CE(\mathfrak{g})
    &&&
    cocycle\;for\;underlying\;G-principal\;\infty-bundle
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)\otimes \Omega^\bullet(X)
    &\leftarrow&
    CE(inn(\mathfrak{g})) = W(\mathfrak{g})  
    &&&
    connection\;and\;curvature
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U) &\leftarrow& inv(\mathfrak{g})
    &&&
    curvature\;characteristic\;forms
  }
  \,,
$$

where the top morphism encodes the cocycle for the underlying $G = \tau_n\exp(\mathfrak{g})$-[[nLab:principal ∞-bundle]], where the middle morphism encodes the connection data and the bottom morphism the [[nLab:curvature characteristic form]]s.

Such $\infty$-Lie algebra valued connections were introduced in <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">SSSI</a> and further studied in <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">SSSIII</a>.

+-- {: .un_prop}
###### Proposition
**(existence of $\infty$-connections)**

In $\mathbf{H} = $ [[nLab:?LieGrpd]] over a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] $X$, every $G$-[[nLab:principal ∞-bundle]] for $G = \tau_n \exp(\mathfrak{g})$ obtained from [[nLab:Lie integration]] admits a genuine $\infty$-connection.

=--

+-- {: .proof}
###### Proof

By the assumptions on $X$, there is a [[nLab:good open cover]] $\{U_i \to X\}$ and a [[nLab:partition of unity]] $(\rho_i \in C^\infty(U_i))$ subordinate to that cover. 

Let $C(\{U_i\})$ be the [[nLab:Cech nerve]] of the cover and let $g : C(\{U_i\}) \to cosk_{n+1} \exp(\mathfrak{g})$ be a cocycle for the given $G$-principal $\infty$-bundle on $X$. This is given by a collection of [[∞-Lie algebroid valued differential forms|∞-Lie algebra valued differential forms]]

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

We will now use this existence of $\infty$-connections to make a statement on principal $\infty$-bundles without connection that generalizes the following familiar construction: for ordinary principal bundles $P \to X$ we can explicitly construct a local trivialization by choosing a connection $\nabla$ on $P$, choosing for each patch $\{U_i \to X\}$ of a good open cover a smooth contraction $f : U_i \times [0,1] \to U_i$ and then using the parallel transport of the connection along the paths $f(x,-) : [0,1] \to U_i$ from $x$ to a fixed base point $x_0$ to identify all fibers of $P$ over $U_i$ with the fiber $P_{x_0}$.




### Chern character {#RefinedCharacteristics}


Above we have considered [∞-Lie algebra valued connections](#InfinityLieAlgebraConnection) and their [curvature characteristic forms](#InfChernWeil). We now wish to show how these model the intrinsic [[Chern character in an (∞,1)-topos]].

$$
  ch_{\mathbf{B}G} : \mathbf{B}G \to \mathbf{\Pi}(\mathbf{B}G) \to \mathbf{\Pi}(\mathbf{B}G)\otimes R
  \,.
$$

Since our ambient [[nLab:(∞,1)-topos]] is assumed to be [[nLab:locally ∞-connected (∞,1)-topos|locally ∞-connected]] we have in addition to the notion of [[nLab:Postnikov tower in an (∞,1)-category]] the notion of [[nLab:Whitehead tower in an (∞,1)-topos]]. Both notions are dual to each other: for $A \in \mathbf{H}$ any object and 

$$
  \mathbf{\Pi}(A)
  \to
  \cdots
  \to
  \tau_{\leq 2}\mathbf{\Pi}(A)
  \to 
  \tau_{\leq 1}\mathbf{\Pi}(A)
  \to \tau_{\leq 0}\mathbf{\Pi}(A)
  = *
$$

the [[nLab:Postnikov tower in an (∞,1)-category|intrinsic Postnikov tower]] of its [[path ∞-groupoid]], the [[nLab:pasting]] composite of [[nLab:(∞,1)-pullback]]s 

$$
  \array{
    \vdots && && && \vdots
    \\
    \downarrow && && && \downarrow
    \\
    A_2 && &\to& \cdots &\to& \mathbf{B}\mathbf{\pi}_3(A) &\to& *
    \\
    \downarrow && && && && \downarrow
    \\
    A_1 && &\to& \cdots && && \mathbf{B}\mathbf{\pi}_2(A) &\to& *
    \\
    \downarrow
    && && && && \downarrow  && \downarrow
    \\
    A
    &\to&
    \mathbf{\Pi}A
    &\to& 
    \cdots
    &\to& 
    \tau_{\leq 3} \mathbf{\Pi}A
    &\to& 
    \tau_{\leq 2} \mathbf{\Pi}A
    &\to& 
    \tau_{\leq 1} \mathbf{\Pi}A
  }
  \,,
$$


defines the [[nLab:Whitehead tower in an (∞,1)-topos|Whitehead tower]] 

$$  
  * \to \cdots \to A_3 \to A_2 \to A_1 \to A_0 = A
$$

of $A$.



Since our $\mathbf{H}$ is assumed to be even [[nLab:∞-connected (∞,1)-topos|∞-connected]], the Postnikov tower of $\mathbf{\Pi}(A)$ is the image under $LConst : \infty Grpd \to \mathbf{H}$ of the ordinary [[nLab:Postnikov tower]] of $\Pi(A)$ in $\infty Grpd$. Accordingly, we have $\mathbf{B} \mathbf{\pi}_n(A) = LConst B^n \pi_n \Pi(A)$

The point now is that in $\mathbf{H} = $ [[nLab:?LieGrpd]] we may form smooh refinements of these discrete extensions: every discrete $(n+1)$-group $\mathbf{B}^{n+1}\mathbb{Z}$ we want to refine to a smooth $n$-group $\mathbf{B}^n U(1)$. By the discussion at <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#GeomReal">geometric realization</a>, both have equivalent underlying $\infty$-groupoids

$$
  \Pi(\mathbf{B}^{n+1}\mathbb{Z}) \simeq \Pi(\mathbf{B}^n U(1))
  \simeq
   K(\mathbb{Z},n+1)
  \,.
$$ 

For every direct summand abelian group $\mathbb{Z}$ in one of the $\mathbf{\pi}_n(A)$ we can ask for a refinement of the cocycle from coefficients $\mathbf{B}^n \mathbb{Z}$ to $\mathbf{B}^{n-1}\mathbb{R}/\mathbb{Z}$. This does not change the geometric realization, up to equivalence, but does change the smooth structure. And it allows to refine to differential coefficients by postcomposing further with
$curv : \mathbf{B}^{n-1}\mathbb{R}/\mathbb{Z} \to
 \mathbf{\flat}_{dR}\mathbf{B}^{n}\mathbb{R}$.

For instance for $A = \mathbf{B}Spin \in \mathbf{H} = \infty Lie Grpd$ the [[nLab:delooping]] of the [[nLab:spin group]], we refine the internal Whitehead tower to 

$$
  \array{
    \vdots
    \\
    \mathbf{B}Fivebrane &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{B}String &\to& \mathbf{B}^7 U(1) &\to& *
    \\
    \downarrow && \downarrow &&  \downarrow  
    \\
    \mathbf{B}Spin &\to& \cdots &\to& \mathbf{B}^3 U(1)
  }
  \,,
$$

where the deloopings of the [[nLab:string 2-group]] and the [[nLab:fivebrane 6-group]] appear.

The result of such a smooth refinement is that we may apply the intrinsic curvature classes and the intrinsic de Rham theorem to obtain cocycles in realified cohomology, for instance 

$$
  \mathbf{B}Spin    
  \to
  \mathbf{B}^3 U(1)
  \stackrel{curv}{\to}
  \mathbf{\flat}_{dR} \mathbf{B}^4 U(1)
  =
  \mathbf{\flat}_{dR} \mathbf{B}^4 \mathbb{R}
  \,.
$$

If we have a $Spin$-principal bundle $X \to \mathbf{B}G$, we may form over it the covering circle $n$-group bundles on which these higher cocycles naturally live

$$
  \array{
    P_2 &\to& \mathbf{B}Fivebrane &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    P_1 &\to& \mathbf{B}String &\to& \mathbf{B}^7 U(1) &\to& *
    \\
    \downarrow && \downarrow &&  && \downarrow  
    \\
    X &\to& \mathbf{B}Spin &\to& \cdots &\to& \mathbf{B}^3 U(1)
  }
  \,.
$$

Here for $X$ an ordinary space, $X = \tau_0 X$, the higher circle $n$-group principal bundes $P_k$ have the property that also $\tau_0 P_k = X$. Therefore the 0-truncation of the entire composite

$$
  P_1 \to \mathbf{B}^7 U(1) \to \mathbf{\flat}_{dR}\mathbf{B}^8 \mathbb{R}
$$

defines a closed 8-form on $X$. This is the curvature characeristic form given by the Chern-Weil homomorphism in this degree. Its refinement to Deligne cohomology in this construction lives naturally not on $X$, but on the covering $P_1$ of $X$.


(...)















## Examples


### Principal 1-bundles with connection

We spell out here how the general theory of [∞-Lie algebra valued connection](#InfinityLieAlgebraConnection) reduces to the standard notion of [[nLab:connection on a bundle|connections]] on ordinary $G$-[[nLab:principal bundle]]s and how the [∞-Chern-Weil homomorphism](#InfChernWeil) reduces on these to the ordinary [[nLab:Chern-Weil homomorphism]].

Let $\mathfrak{g}$ be a (finite dimensional) [[nLab:Lie algebra]]. Then

$$
  \mathbf{cosk}_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G
$$

is the [[nLab:delooping]] of the simply connected [[nLab:Lie group]] $G$ integrating $\mathfrak{g}$.


+-- {: .un_prop }
###### Proposition

The coefficient object $\mathbf{B}G_{conn}$ of [genuine ∞-Lie algebra connections](#InfinityLieAlgebraConnection) for $\mathfrak{g}$ an ordinary [[nLab:Lie algebra]] is weakly equivalent to the simplicial presheaf

$$
  \mathbf{B}G_{conn}
  \stackrel{\simeq}{\to}
  \Xi[G\times \Omega^1(-,\mathfrak{g}) \stackrel{
   \overset{Ad_{p_1}(p_2)+ p_1 d p_1^{-1}}{\to}}{\underset{p_2}{\to}} \Omega^1(-,\mathfrak{g})]
$$

that assigns objectwise the [[nLab:groupoid of Lie-algebra valued 1-forms]].

This is moreover isomorphic to the simplicial presheaf

$$
  \cdots = 
  [CartSp^{op},sSet](\mathbf{P}_1(-),\mathbf{B}G])
$$

of morphisms out of the [[nLab:path groupoid]].

The flat coefficient object $\mathbf{\flat}\mathbf{B}G$ is modeled by the subobject

$$
  \Xi[G\times \Omega^1_{flat}(-,\mathfrak{g}) \stackrel{
   \overset{Ad_{p_1}(p_2)+ p_1 d p_1^{-1}}{\to}}{\underset{p_2}{\to}} \Omega^1_{flat}(-,\mathfrak{g})]
$$

of groupoids of Lie-algebra valued forms with vanishing [[nLab:curvature]] 2-form.

This is isomorphic to 

$$
  \cdots = 
  [CartSp^{op},sSet](\mathbf{\Pi}_1(-),\mathbf{B}G])
$$

of morphism out of the [[nLab:fundamental groupoid]].

=--


+-- {: .proof}
###### Proof

The statements about morphisms out of the path groupoid are discussed in detail in [SchrWalI](http://arxiv.org/abs/0705.0452).

=--

+-- {: .un_cor }
###### Corollary

For $X$ a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] and $\{U_i \to X\}$ a [[nLab:good open cover]] we have a natural equivalence of groupoids

$$
  [CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}G_{conn})
  \simeq
  G Bund_\nabla(X)
$$

with the groupoid of smooth $G$-principal bundles with connection on $G$. 

For $\langle - \rangle : inn(\mathfrak{g}) \to b^p \mathbb{R}$ an [[nLab:invariant polynomial]] on $\mathfrak{g}$, the [induced morphism](#InfChernWeil)

$$
  [CartSp^{op}, sSet](C(\U_i\}), \mathbf{B}G_{diff})
  \stackrel{\langle F_{(-)}\rangle}{\to}
  \Omega^{p+1}_{cl}(X)
$$

is that of the ordinary [[nLab:Chern-Weil homomorphism]].

=--

We have seen that a refinement of the Chern-Weil homomorphism is available. The above morphism extends to a morphism

$$
  \langle F_{(-)}\rangle :  \mathbf{H}(-, \mathbf{B}G)
  \to 
  \mathbf{H}(-,
    \tau_{1} \mathbf{\flat}_{dR}\mathbf{B}^{p+1} \mathbb{R}
  )
$$

in $\mathbf{H} = \infty LieGrpd$ represented by

$$
 \array{
  [CartSp^{op},sSet](-, \mathbf{B}G_{diff})
  &\to&
  [CartSp^{op},sSet](-, \mathbf{cosk}_2 \mathbf{\flat}_{dR}\mathbf{B}^{p+1} \mathbb{R})
  \\
  \downarrow^{\simeq}
  \\
  [CartSp^{op},sSet](-, \mathbf{B}G)
  }
  \,.
$$

For $X$ a smooth manifold with good cover $\{U_i \to X\}$ we have that 
$ [CartSp^{op},sSet](C\{U_i\}, \mathbf{cosk}_2 \mathbf{\flat}_{dR}\mathbf{B}^{p+1} \mathbb{R})$ is the groupoid whose objects are closed $p+1$-forms on $X$ and whose morphisms are given by $p$-forms modulo exact forms.

Let $i \in I$ range over a set of generators for all [[nLab:invariant polynomial]]s. Then 

$$
  \mathbf{H}(-,\mathbf{B}G)
  \to 
  \prod_i \tau_1\mathbf{\flat}_{dR}\mathbf{B}^{n_i} \mathbb{R}
$$

is an approximation to the intrinsic Chern-character. We may consider its [[nLab:homotopy fiber]]s over a given set $Q_i$ of curvature characteristic forms.

Assume $\nabla, \nabla' : C(\{U_i\}) \to \mathbf{B}G_{diff}$ are two genuine connections with coinciding curvature characteristic classes $\{Q_i\}$. Then in the homotopy fiber they are coboundant cocycles precisely if all the [[nLab:Chern-Simons form]]s $CS_i(\nabla,\nabla')$ vanish modulo an exact form.

This equivalence relation is that which defines [[nLab:Simons-Sullivan structured bundle]]s. Their [[nLab:Grothendieck group]] completion yields [[nLab:differential K-theory]].


### Principal 2-bundles with connection

(...)

Let $\mathfrak{g}$ be a Lie [[nLab:strict 2-group]] coming from a [[nLab:differential crossed module]] $(\mathfrak{g}_2 \to \mathfrak{g}_1)$. Then we have two candidate Lie 2-groups integrating this: on the one hand the [[nLab:strict 2-group]] coming from the [[nLab:crossed module]] $(G_2 \to G_1)$ that integrates $(\mathfrak{g}_2 \to\mathfrak{g}_1)$ degreewise as ordinary Lie algebras, and on the other hand $cosk_k\exp(\mathfrak{g})$.

+-- {: .un_prop }
###### Proposition

The morphism

$$
  \tau_2 \exp(\mathfrak{g}) \to 
  \mathbf{B}(G_2 \to G_1)
$$

given by evaluating 2-dimensional [[nLab:parallel transport]] is a weak equivalence.
=--

+-- {: .proof}
###### Proof


Use the 3-dimensional nonabelian Stokes theorem from the appendix of [SchrWalII](http://arxiv.org/abs/0802.0663).

=--

+-- {: .un_cor }
###### Corollary

The object $\mathbf{B}(G_2 \to G_1)_{conn}$ assigns to $U \in CartSp$ the [[nLab:2-groupoid of Lie 2-algebra valued forms]] over $U$.

=--

This is described in detail in [SchrWalII](http://arxiv.org/abs/0802.0663), subject to the extra constraint that the 2-form curvature vanishes.


+-- {: .un_cor }
###### Corollary

A genuine connection on a $(G_2 \to G_1)$-[[nLab:principal 2-bundle]] with given cocycle $X \stackrel{\simeq}{\leftarrow} C(\{U_i\}) \to \mathbf{B}(G_2 \to G_1)$ is a cocycle $X \stackrel{\simeq}{\leftarrow} C(\{U_i\}) \to \mathbf{B}(G_2 \to G_1)_{conn}$ given as follows:

1. on $U_i$ a pair of forms $A_i \in \Omega^1(U_i, \mathfrak{g}_1)$, $B_i \in \Omega^2(U_i, \mathfrak{g}_2)$;

1 on $U_i \cap U_j$ a function $g_{i j} \in C^\infty(U_{i}\cap U_j , G_1)$ and a 1-form $a_{i j} \in \Omega^1(U_i \cap U_j, \mathfrak{g}_2)$ such that ...

1. and so forth
   

=--

This is described in detail in [SchrWalIII](), subject to the extra constraint that the 2-form curvature vanishes.

(...)




### Twisted differential $String-$ and $Fivebrane$-structures {#DiffStringStruc}

We discuss a motivating class of example for the notion of an $\infty$-Chern-Weil homomorphism in $\mathbf{H} =$ [[nLab:?LieGrpd]]. Details on this are [below](#StringStructure).

Consider the [[nLab:spin group]] $G =  Spin$. Its topological [[nLab:classifying space]] $\mathcal{B}G$ has $H^4(\mathcal{B}G, \mathbb{Z}) \simeq \mathbb{Z}$, and the generator of this cohomology group is the [[nLab:characteristic class]] called $\frac{1}{2}p_1$.

$$
  H^1(X,G)
  = H(X, \mathcal{B}G) \stackrel{\frac{1}{2}p_1}{\to} H(X, \mathcal{B}^4 \mathbb{Z})
  = H^4(X,\mathcal{Z})
  \,.
$$

If a $G$-[[nLab:principal bundle]] $P \to X$ is _smooth_ , then this topological cohomology class in $H^1(X,\mathcal{B}G)$ has a counterpart in [[nLab:differential geometry]]:
the [[nLab:Chern-Weil homomorphism]] produces from any choice of [[nLab:connection on a bundle|connection]] $\nabla$ on $P$ a smooth [[nLab:differential form|differential 4-form]] $\langle F_\nabla \wedge F_\nabla \rangle \in \Omega^4_{cl}(X)$, representing a class in $H_{dR}^4(X)$: the [[nLab:curvature characteristic form]].  Under the [[nLab:de Rham theorem|de Rham isomorphism]], these classes match.

But even more is true: even the precise way in which the differential 4-form refines the integral 4-class has a natural expression: we have a $U(1)$-2-gerbe with connection, equivalently a 
$\mathbf{B}^3 U(1)$-[[nLab:principal ∞-bundle|principal 3-bundle]] with connection $String(P,\nabla) \in H_{diff}(X,\mathbf{B}^3 U(1))$
which interpolates between the integral and the differential class, in that these are its images under the two natural projections

$$
    H_{diff}(X,\mathbf{B}^3 U(1)) \to H^4_{dR}(X) \times H^4(X,\mathbb{Z})    
$$

$$
  String(P,\nabla) \mapsto (\langle F_\nabla \wedge F_\nabla\rangle, \frac{1}{2}p_1(P))
  \,.
$$

So far this is at the level of cohomology classes. If we lift the classification of principal bundles from the $(\infty,1)$-topos $Top$ to $\mathbf{H} = \infty Lie Grpd$, then we can refine  all this to a map of cocycle $\infty$-groupoids

$$
  \frac{1}{2}\hat p_1 :
  \mathbf{H}(X,\mathbf{B}Spin)
  \to 
  \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
$$

which covers the underlying characteristic class

$$
  \frac{1}{2}p_1 : \mathbf{H}(X,\mathbf{B}G) \to 
  \mathbf{H}(X,\mathbf{B}^3 U(1))
  \,.
$$

Recall that a [[nLab:string structure]] on $X$ is an element in the homotopy kernel of this class. More precisely, the $\infty$-groupoid of [[nLab:string structure]]s on $X$ is the [[nLab:homotopy fiber]] of $\frac{1}{2}p_1$. 

Therefore we say the $\infty$-groupoid of [[nLab:string structure|differential string structure]]s is the [[nLab:(∞,1)-pullback]]

$$
  \array{
    String_{diff}(X) &\to& *
    \\
    \downarrow &{}^{\simeq}& \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}Spin(n)) &\to& \mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))
  }
  \,.
$$

Cocycles in $String_{diff}(X)$ are pairs consisting of a $Spin$-principal bundle with connection $\nabla$ and a trivialization of the corresponding String-lifting [[nLab:Chern-Simons 2-gerbe]] with connection
$CS(\nabla)$ and curvature $\langle F_\nabla \wedge F_\nabla\rangle$.

More generally, we can define the $\infty$-groupoid of 
**twisted differential string structures** as the $(\infty,1)$-pullback of all
degree 4 differential classes.

$$
  \array{
    String_{diff}(X) &\to& H_{diff}(X,\mathbf{B}^3 U(1))
    \\
    \downarrow &{}^{\simeq}& \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}Spin(n)) &\to& \mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))
  }
$$

A cocycle in $String_{diff}(X)$ over a given class is a $G$-principal bundle with  connection $\nabla$ together with a cocycle between the Chern-Simons 2-gerbe of that data and the fixed 2-gerbe with connection.

What makes all this work is that the characteristic class $\frac{1}{2}p_1$ has an infinitesimal origin: it arises by Lie integration of an invariant polynomial on the Lie algebra  $\mathfrak{so}$. This $\infty$-Lie integration of invariant polynomials on Lie algebras
is what secretly underlies the Chern-Weil homomorphism.

But the above discussion suggests that we may want to go further: the characteristic class $\frac{1}{2}p_1(P)$ vanishes precisely if $P$ has [[nLab:string structure]]. This means
that its classifying map $X \to \mathbf{B}G$ lifts through the [[nLab:string 2-group]] projection $\mathbf{B}String \to \mathbf{B}Spin$. In fact we have a [[nLab:fiber sequence]]

$$
  \array{
     \mathbf{B}String &\to& *
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}Spin
     &\stackrel{\frac{1}{2}p_1}{\to}&
     \mathbf{B}^3 U(1)
  }
$$

in $\infty Lie Grpd$ which induces a fiber sequence of cocycle $\infty$-groupoids

$$
  \array{
     \mathbf{H}(X,\mathbf{B}String) &\to& *
     \\
     \downarrow && \downarrow
     \\
     \mathbf{H}(X,\mathbf{B}Spin)
     &\stackrel{\frac{1}{2}p_1}{\to}&
     \mathbf{H}(X,\mathbf{B}^3 U(1))
  }
  \,.
$$

This means in particular that if we do have a (differential) String-structure $\in String_{diff}(X)$, then we may consider the $String$-principal 2-bundle $\hat P$ that lifts the $Spin$-bundle $P$.

Now, there is a higher degree cocycle analogous to $\frac{1}{2}p_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)$. That's $\frac{1}{6}p_2 : \mathbf{B}String \to \mathbf{B}^7 U(1)$. It corresponds to the 
canonical degree 8-cocycle on the Lie algebra $\mathfrak{so}$. But it is also an invariant polynomial on the [[nLab:string Lie 2-algebra]] $\mathfrak{string}$.

This suggests that we find a refined Chern-Weil homomorphism for String-principal 2-bundles with connection, such that we obatain a morphism

$$
  \frac{1}{6}\hat p_2 : 
  \mathbf{H}(X,\mathbf{B}String)
  \to
  \maathbf{H}_{diff}(X,\mathbf{B}^7 U(1))
$$

of $\infty$-groupoids of cocycles, whose [[nLab:homotopy fiber]]s are
**twisted differential 5-brane structures** on $X$

$$
  \array{
    Fivebrane_{diff}(X) &\to& H_{diff}(X,\mathbf{B}^7 U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}String)
    &\stackrel{frac{1}{6}\hat p_2}{\to}&
    \mathbf{H}(X,\mathbf{B}^7 U(1))
  }
  \,.
$$

The local connection form data on these twisted differential string and fivebrane structures was discussed in ([SatiSchreiberStasheffIII]()).

(...)




#### The string-lifting Chern-Simons 3-bundle with connection {#StringStructure}

We describe the special case of the general [∞-Chern-Weil homomorphism](#InfChernWeil) for [∞-Lie algebra valued connections](#InfinityLieAlgebraConnection) corresponding to the [[nLab:characteristic class]]  $\frac{1}{2}p_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)$: the first fractional [[nLab:Pontryagin class]] of the [[nLab:spin group]] $\mathbf{B}Spin$. The $\mathbf{B}^3 U(1)$-differential cocycle that it produces from a given $Spin$ [[nLab:principal bundle]]
is the [[nLab:Chern-Simons 2-gerbe|Chern-Simons 2-bundle]] with connection whose class is the obstruction for the existence of a [[nLab:string structure]].


Let $\mathfrak{g} = \mathfrak{so}$ be the [[nLab:Lie algebra]] of the [[nLab:special orthogonal group]]. Write $P = \langle -,-\rangle \in W(\mathfrak{g})$ for the canonical binary [[nLab:invariant polynomial]].

The corresponding [[nLab:Lie algebra cohomology|3-cocycle]] is $\mu : \mathfrak{so} \to b^2 \mathbb{R}$

$$
  \mu = \langle -, [-,-]\rangle \in CE(\mathfrak{g})
  \,.
$$

As a Lie algebra cocycle it is the one that classifies the [[nLab:string Lie 2-algebra]] extension $\mathfrak{string} \to \mathfrak{o} \to b^2$

Reecall first the [[nLab:Lie integration]] of this bare cocycle:

The simply connected Lie group $G = Spin$ corresponding to $\mathfrak{g}$ has $\pi_2(G) = 0$ and $\pi_3(G) = \mathbb{Z}$. The Lie integrated model for $\mathbf{B}G$ on which the cocycle integrates is

$$
  \mathbf{B}G \stackrel{\simeq}{\leftarrow}
  \mathbf{cosk}_3 (\exp(\mathfrak{g})
  =
  \mathbf{cosk}_3(
  (U,[k]) \mapsto 
  \Omega^1_{flat}(\Delta^k,\mathfrak{g}) \otimes C^\infty(U))
  )
  \,.
$$

The weak equivalence to $\mathbf{B}G$ is given by [[nLab:parallel transport]]: it sends a flat $\mathfrak{g}$-valued form $A = \lambda d t$ with $\lambda \in C^\infty(U,\mathfrak{g})$ to the group element $P \exp(\int_0^1 \lambda d t)$.

Two such 1-forms $\lambda d t$ and $\lambda' d t$ are equivalent in $\mathbf{cosk}_3 \exp(\mathfrak{g})$ precisely if they are the restrictions of a flat $\mathfrak{g}$-valued 1-form on the disk, which indeed, by the [[nLab:nonabelian Stokes theorem]] is the case precisely if their parallel transport coincides. By identifying the basepoint with the neutral element in $G$, flat $\mathfrak{g}$-valued 1-form on $\Delta^k$ correspond bijectively with smooth maps $\Delta^k \to G$. Since $\pi_2(G)$ vanishes, any two such flat 1-forms on disks with coinciding boundary can be filled by a 3-ball. The coskeleton operation finally identifies all 3-balls with coinciding boundary. 

The integrated cocycle

$$
  \exp(\mu)
  : 
  \mathbf{cosk}_3 \exp(\mathfrak{g})
  \to 
  \mathbf{B}^3 \mathbb{R}/\mathb{Z}
$$

sends a 3-ball $\sigma : \Delta^3 \to G$ to the integral of $\mu$ over it

$$
  \exp(\mu) : \sigma \mapsto \int_{\Delta^3} \sigma^* \mu \; mod \mathbb{Z}
  \,.
$$

Now given a Cech cocycle $\{g_{i j}\}$ for a $G$-bundle, we may always find a refined cover $\{U_i \to X\}$ on which the cocycle lifts to this resolution

$$
  \array{
    && \exp(\mathfrak{g})_{\sim_3, \mathbb{Z}}
    \\
    & {}^{\hat g}\nearrow & \downarrow
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

Choosing $\hat g$ amounts to

1. choosing on each double intersection $U_{i} \cap U_j$ a smooth based family of paths $\hat g_{i j} : U_i \cap U_j \times \Delta^1 \to G$ such that $\hat g_{i j}(0) = e$ and $\hat g_{i j}(1) = g_{i j}$;

1. choosing on each triple intersection a smooth family of based disks $\hat g_{i j k} : U_i \cap U_j \cap U_k \times \Delta^2 \to G$ in $G$, cobounding these paths.

1. choosing on each quadruple intersection a smooth family of based balls $\hat g_{i j k l} : U_i \cap U_j \cap U_k \cap U_l \times \Delta^3 \to G$ in $G$, cobounding these disks, or rather their homotopy class, relative boundaries, $[\hat g_{i j k l}]$.

That these choices exist locally, and hence for sufficiently refined cover $\{U_i \to X\}$ is the fact that $\pi_0(G) = *$ and $\pi_1(G) = 0$ and $\pi_2(G) = 0$, which is essential part of the statement that the morphism $\mathbf{B}G \stackrel{\simeq}{\leftarrow} \exp(\mathfrak{g})/_{\sim_3}$ that we are lifting through is indeed a weak equivalence.

The characteristic class corresponding to the Lie integated cocycle $\exp(\mu)$ is then modeled by the morphism

$$
  \array{
    && \exp(\mathfrak{g})_{\sim_3, \mathbb{Z}}
    &\stackrel{\exp(\mu)}{\to}&
    \exp(b^2 \mathbb{R})_{\sim_3 / \mathbb{Z}}
    \\
    & {}^{\hat g}\nearrow & \downarrow^{\mathrlap{\simeq}} && 
    \downarrow^{\mathrlap{\simeq}}
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G && \mathbf{B}^3 \mathbb{R}/\mathbb{Z}
  }
$$

which on quadruple intersections takes $[\hat g_{i j k l}]$ to $\int_{\Delta^3} \hat g_{i j k l}^* \mu  mod \; \mathbb{Z}$.

This [[nLab:Cech cohomology]] model for $\frac{1}{2}p_1$ appears on p. 9 of (<a href="http://www.springerlink.com/content/762g1m76jp6425x5/">BrylinskiMacLaughlin</a>).

We now further resolve this model in order to lift the characteristic class to differential cohomology.

$$
  \array{
     && 
     \exp(\mathfrak{g} \to inn(\mathfrak{g}))/_{\sim_3,\mathbb{Z}}
     &\stackrel{\exp(\mu,P)}{\to}&
     \exp(\mathfrak{b^2 \mathbb{R}} \to inn(b^2 \mathbb{R}))/_{\sim_3,\mathbb{Z}}
    &\to&
    \exp(* \to b^3 \mathbb{R})
    \\
    &{}^{\mathllap{\hat \nabla}}\nearrow& \downarrow^{\mathrlap{\simeq}} 
    && \downarrow^{\mathrlap{\simeq}}
    && \downarrow^{\mathrlap{\simeq}}
    \\
    && \exp(\mathfrak{g})_{\sim_3, \mathbb{Z}}
    &\stackrel{\exp(\mu)}{\to}&
    \exp(b^2 \mathbb{R})_{\sim_3 / \mathbb{Z}}
    && \mathbf{\flat}_{dR} \mathbf{B}^4 U(1)_{simp}
    \\
    & {}^{\hat g}\nearrow & \downarrow^{\mathrlap{\simeq}} 
    && \downarrow^{\mathrlap{\simeq}}
    && \downarrow^{\mathrlap{\simeq}}
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G && \mathbf{B}^3 \mathbb{R}/\mathbb{Z}
   && \mathbf{\flat}_{dR} \mathbf{B}^4 U(1)_{chn}
  }
  \,.
$$

For the connection $\hat \nabla$ we need to choose

1. $\mathfrak{g}$-valued 1-forms $A_i \in \Omega^1(U_i, \mathfrak{g})$;

1. $\mathfrak{g}$-valued 1-forms $\hat A_{i j} = A_{i j} + \lambda_{i j} \in \Omega^1(U_{i j} \times \Delta^1)$ whose restriction $\lambda_{i j}$ to $\Delta^1$ is the given path in $G$;

1. etc.

Recall that we say this forms a _genuine_ connection if the coresponding [[nLab:curvature]] 2-forms have no component along the simplices.

We can build a genuine connection $\hat \nabla$ from the cocycle $\{g_{i j}, A_i\}$ for an ordinary connection 
on the underlying ordinary cocycle $g_{i j}$: take $\hat A_{i j}(0) = A_i$ and then let $\hat A_{i j}$ be the unique solution to the differential equation

$$
  \frac{\partial}{\partial t} A_{i j}
  =
  d \lambda_t + [lambda_t, \hat A_{i j}]
  \,.
$$

This is precisely the condition that he curvature 2-form has no component along the 1-simplex.

In other words, if $\hat g_{i j} : U_{i j } \times \Delta^1 \to G$ is the path obtained from parallel transport of $\lambda$, then we set

$$
  A_{i j}(t) := \hat g_{i j}(t)^{-1} (A_i + d) \hat g_{i j}(t)
  \,.
$$

Notably, by the fact that $\{A_i, g_{i j}\}$ is assumed to be a cocycle for an ordinary connection, this way we have

$$
  A_{i j}(1) = g_{i j}^{-1} (A_i + d) g^{i j} = A_j
 \,.
$$

Similarly we may transport the connection 1-forms around over the higher simplices to obtain $\hat A_{i j k}$ and $\hat A_{i j k l}$. This defines a lift $\hat \nabla : C(\{U_i\}) \to \exp(\mathfrak{g} \to inn(\mathfrak{g}))/_{\sim_3, \mathbb{Z}}$.

By collecting all this data, we find

+-- {: .un_prop }
###### Proposition

The composite morphism

$$
  C(\{U_i\})
  \stackrel{\hat \nabla}{\to}
  \exp(\mathfrak{g} \to inn(\mathfrak{g})/_\sim
  \stackrel{\exp(\mu,P)}{\to}
  \exp(b^2 \mathbb{R} \to inn(b^2 \mathbb{R})/_\sim
  \stackrel{\int_{\Delta^\bullet}}{\to}
  \mathbf{B}^3 U(1)_{diff}
$$

is the Cech-Deligne cocycle

$$
  (CS(A_i), \int_{\Delta^1} CS(\hat A_{i j} ), \int_{\Delta^2} CS(\hat A_{i j k}), \int_\Delta^3 \mu(A_{i j k l}))
  \,.
$$


This is is exactly equal to the one written down on page 10 of (<a href="http://www.springerlink.com/content/762g1m76jp6425x5/">BrylinskiMacLaughlin</a>). It represent a canonical differential refinement of the first fractional Pontryagin class of the original $Spin$-principal bundle. 

This composite morphism is a model for the differential cohomology refinement

$$
  \frac{1}{2}\hat p_1 : 
  \mathbf{H}(-,\mathbf{B}Spin)
  \to 
  \mathbf{H}_{diff}(-, \mathbf{B}^3 U(1))
$$

of the first fractional Pontryagin class.

=--



#### Differential string structures

Let 

$$
  \frac{1}{2}\hat p_1 : 
  \mathbf{H}(-,\mathbf{B}Spin)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^3 U(1))
$$

be the differential refinement of the first fractional Pontryagin class discussed [above](#StringStructure).

+-- {: .un_def }
###### Definition

For $X \in \mathbf{H} =$ [[nLab:?LieGrpd]], the $\infty$-groupoid  of **differential string-structures** $String_{diff}(X)$ is the [[nLab:homotopy fiber]] of    $\frac{1}{2}p_1(X) : \mathbf{H}(X,\mathbf{B}Spin) \to \mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))$.

More generally, the $\infty$-groupoid of **twisted differential string structures** is the [[nLab:(∞,1)-pullback]] $String_{diff,tw}(X)$ in

$$
  \array{
    String_{diff,tw}(X) &\to& H_{diff}(X,\mathbf{B}^3 U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}Spin)
    &\stackrel{\frac{1}{2}\hat p_1}{\to}&
    \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
  }
  \,.
$$

=--

In terms of just the underlying $\infty$-Lie algebra valued local connection data, i.e. before Lie integration in the above sense, this has been considered in [SatiSchreiberStasheffIII](spring). 

For the case where the twist is given just by globally defined 3-forms, i.e. by  trivial 2-gerbes with connection, essentially this definition, explicitly modeled on [[nLab:bundle gerbe]]s, has been given in ([Waldorf09](http://arxiv.org/PS_cache/arxiv/pdf/0906/0906.0117v1.pdf)).

We describe now the Lie integration of the $\infty$-Lie algebraic model in [SatiSchreiberStasheffIII](spring) to a model of the above homotopy pullback.

In order to compute the homotopy pullback as an ordinary pullback, we want to model the morphism     
$\mathbf{H}(X,\mathbf{B}Spin) \stackrel{\frac{1}{2}\hat p_1}{\to \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))$ in $\infty Lie Grpd$ by a fibration in $[CartSp^{op}, sSet]_{proj,cov}$. To that end, we replace the Lie algebra $\mathfrak{g}$ by an equivalent Lie 3-algebra

+-- {: .un_def }
###### Definition

Let $\hat \mathfrak{g}$ be the $\infty$-Lie algebra defined by the fact that its [[nLab:Chevalley-Eilenberg algebra]] is

$$
  CE(\hat \mathfrak{g}) = 
  (\wedge^\bullet(  \mathfrak{g}^* \oplus \langle b\rangle \oplus \langle c \rangle ), d)
  \,,
$$

with $b$ a generator in degree 2, and $c$ a generator in degree 3, and with differential

$$
  d|_{\mathfrak{g}^*} = [-,-]^*
  \,; 
$$

$$
  d : b \mapsto \langle - , [-,-]\rangle + c
$$

$$
  d : c \mapsto 0
  \,.
$$

=--

+-- {: .un_prop }
###### Proposition

The canonical correspondence

$$
  \array{
    \mathbf{cosk}_3\exp(\hat \mathfrak{g})
    &\to&
    \mathbf{B}^3 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}G
  }
$$

obtained by projecting out onto the 3-forms induced by the generator $c$ and then integrating is another model for $\frac{1}{2}p_1$, with the special property that the top morphism is a fibration in $[CartSp^{op}, sSet]_{proj}$.

=--

With this observation we can read off the cocycles in $String_{diff,tw}(X)$ from the diagrams of dg-algebras in SSSIII.

(...)

#### The Fivebrane-lifting Chern-Simons 6-bundle with connection {#FivebraneStructure}


We show now that the Lie integration of the differential $\infty$-Lie algebra cocycle corresponding to the degree 7 cocycle on the [[nLab:string lie 2-algebra]] $\mathfrak{string}$

$$
  \exp(\mathfrak{string} \to inn(\mathfrak{string}))/\sim
  \stackrel{\exp(\mu_7, P_8)}{\to}
  \exp(b^6 \mathbb{R} \to inn(b^6 \mathbb{R})/\sim
  \to
  \mathbf{B}^7 U(1)_{diff}
$$

is a model for the differential refinement of the second fractional Pontryagin class

$$
  \frac{1}{6}p_2
  : 
  \mathbf{H}(-, \mathbf{B}String)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^7 U(1))
  \,.
$$

The discussion is entirely analogous to the discussion of the differential refinekent of the first fractional Pontryagin class [above](#StringStructure).

(...)

#### Differential fivebrane structures

Let 

$$
  \frac{1}{6}\hat p_2 : 
  \mathbf{H}(-,\mathbf{B}String)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^7 U(1))
$$

be the differential refinement of the second fractional Pontryagin class discussed [above](#FivebraneStructure).


**Definition** 

For $X \in \mathbf{H} =$ [[nLab:?LieGrpd]], the $\infty$-groupoid  of **differential fivebrane-structures** $Fivebrane_{diff}(X)$ is the [[nLab:homotopy fiber]] of    $\frac{1}{6}p_2(X) : \mathbf{H}(X,\mathbf{B}String) \to \mathbf{H}_{diff}(X, \mathbf{B}^7 U(1))$.

More generally, the $\infty$-groupoid of **twisted differential fivebrane structures** is the [[nLab:(∞,1)-pullback]] $Fivebrane_{diff,tw}(X)$ in

$$
  \array{
    Fivebrane_{diff,tw}(X) &\to& H_{diff}(X,\mathbf{B}^7 U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}String)
    &\stackrel{\frac{1}{6}\hat p_2}{\to}&
    \mathbf{H}_{diff}(X,\mathbf{B}^7 U(1))
  }
  \,.
$$

In terms of the underlying $\infty$-Lie algebra valued local connection data, i.e. before Lie integration in the above sense , this has been considered in (SatiSchreiberStasheffIII). 

(...)

***


