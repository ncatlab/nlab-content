
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

* [[connection on a bundle]]

* [[connection on a 2-bundle]] / [[connection on a gerbe]] / [[connection on a bundle gerbe]]

* [[connection on a 3-bundle]] / [[connection on a bundle 2-gerbe]]

* **connection on an ∞-bundle**

***



#Contents#
* table of contents
{:toc}

## Idea

A _connection_ on a $G$-[[principal ∞-bundle]] in the [[(∞,1)-topos]] $\mathbf{H} =$ [[?LieGrpd]] is a structure that serves to interpolate between the [[nonabelian cohomology]] class $c \in H(X, \mathbf{B}G)$ of tbe bundle and its intrinsic [[curvature characteristic form|curvature characteristic class]]es in de Rham cohomology $H_{dR}^{n+1}(X)$ or even in [[ordinary differential cohomology]] $H_{diff}(X,\mathbf{B}^n U(1))$. This is the content of the [[∞-Chern-Weil homomorphism]].

This generalizes the notion of [[connection on a bundle]] and the ordinary [[Chern-Weil homomorphism]].


For $G$ a [[∞-Lie group]], a _connection_ on a $G$-[[principal ∞-bundle]] coming from a [[cocycle]] $g : X \to \mathbf{B}G$ is a lift of the cocycle to the  [[∞-groupoid of ∞-Lie-algebra valued forms]] $\mathbf{B}G_{conn}$

$$
  \array{
     && \mathbf{B}G_{conn}
     \\
     & {}^{\mathllap{\nabla}}\nearrow & \downarrow
     \\
     X &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

## Definition


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
  \mathbf{B}G_{conn}
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



## Examples


* [[circle n-bundle with connection]]


## References

* SSSI (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)
{#SSSI}


[[!redirects ∞-connection on a principal ∞-bundle]]
[[!redirects ∞-connection on a principal ∞-bundle]]

[[!redirects connection on a principal ∞-bundle]]

[[!redirects connection on an ∞-bundle]]
[[!redirects connections on an ∞-bundle]]

[[!redirects connection on an infinity-bundle]]

[[!redirects connections on ∞-bundles]]
[[!redirects connections on infinity-bundles]]
