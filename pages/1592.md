
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition



### In point-set topology
 {#Definition}

The following is the classical discussion of universal covering spaces in [[point-set topology]].

+-- {: .num_prop #SimplyConnectedCoveringUniqueness}
###### Proposition
**([[essentially unique|essential uniqueness]] of simply connected covering spaces)**

Let $X$ be a [[topological space]] which is

1. [[path-connected topological space|path-connected]],

1. [[locally path-connected topological space|locally path connected]].

Then if $E_i \overset{p_i}{\to} X$ are two [[covering spaces]]
over $X$, $i \in \{1,2\}$, which are both [[path-connected topological space|path-connected]] and [[simply connected topological space|simply connected]], then they are [[isomorphism|isomorphic]] as covering spaces.

=--

+-- {: .proof}
###### Proof

Since both $E_1$ and $E_2$ are simply connected, the assumption of the lifting theorem for covering spaces is satisfied ([this prop.](covering+space#TheTheoremLifting)). This says that there are horizontal continuous function making the following diagrams commute:

$$
  \array{
    E_1 && \overset{f}{\longrightarrow} && E_2
    \\
    & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && X
  }
  \phantom{AAAAAA}
  \array{
    E_2 && \overset{g}{\longrightarrow} && E_1
    \\
    & {}_{\mathllap{p_2}}\searrow && \swarrow_{\mathrlap{p_1}}
    \\
    && X
  }
$$

$$
  \array{
    E_i && \overset{id}{\longrightarrow} && E_i
    \\
    & {}_{\mathllap{p_i}}\searrow && \swarrow_{\mathrlap{p_i}}
    \\
    && X
  }
$$

and that these are _unique_ once we specify the image of a single point, which we may freely do (in the given fiber).

So if we pick any point $x \in X$ and $\hat x_1 \in E_1$ with $p(\hat x) = x$ and $\hat x_2 \in E_2$ with $p(\hat x_2) = x$ and specify that $f(\hat x_1) = \hat x_2$ and $g(\hat x_2) = \hat x_1$ then uniqueness applied to the composites implies $f \circ g = id_{E_{2}}$ and $g \circ f = id_{E_1}$. 

=--

+-- {: .num_defn #CoveringUniversal}
###### Definition
**(universal covering space)**

Let $X$ be a [[topological space]] which is

1. [[path-connected topological space|path-connected]],

1. [[locally path-connected topological space|locally path connected]].

Then a [[path-connected topological space|path-connected]] and [[simply connected topological space|simply connected]] [[covering space]], is called [[generalized the|the]] _universal covering space_ of $X$. This is well-defined, if it exists, up to [[isomorphism]], by prop. \ref{SimplyConnectedCoveringUniqueness}.

=--

+-- {: .num_prop #ReconstructCoveringForFreeAndTransitiveMonodromyRepresentation}
###### Proposition
**([[universal covering space]] reconstructed from [[free action|free]] and [[transitive action|transitive]] [[fundamental group]] [[representation]])**

Let $X$ be a topological space which is _[[well-connected space|well-connected]]_ in that it is

* [[path-connected space|path-connected]], 

* [[locally path-connected space|locally path-connected]] 

* and [[semi-locally simply-connected space|semi-locally simply-connected]] 

Then a universal covering space of $X$ (def. \ref{CoveringUniversal}) exists.

=--

+-- {: .proof}
###### Proof

By [this prop.](covering+space#CoveringConnectivityViaMonodromy) the covering space is connected and simply connected precisely if its [[monodromy]] representation is free and transitive. By the [[fundamental theorem of covering spaces]] every [[permutation representation]] of the [[fundamental groupoid]] $\Pi_1(X)$ arises as the monodromy of some covering space. Hence it remains to see that a free and transitive representation of $\Pi_1(X)$ exists. Let $x \in X$ be any point, then $Hom_{\Pi_1(X)}(x,-)$ is such a representation. 

=--


This is a  functorial construction of a universal covering spaces

$$
  Top_*^{wc} \longrightarrow Cov_*
$$

where $Top_*^{wc}$ denotes the [[full subcategory]] of [[pointed topological spaces]] $Top_*$ on the well-connected spaces and $Cov$ is the subcategory of $Top_*^2$ of pointed maps of spaces with objects the covering space maps.

Specifically, if $X$ is a space with basepoint $x_0$, we define $X^{(1)}$ to be the space whose points are homotopy classes of paths in $X$ starting at $x_0$, with the projection $X^{(1)}\to X$ projecting to the endpoint of a path.  We can equip this set $X^{(1)}\to X$ with a topology coming from $X$ so that it becomes a universal covering space as above.  As described at [[covering space]], under the correspondence between covering spaces and $\Pi_1(X)$-actions, the space $X^{(1)}$ corresponds to the "regular representation" of $\Pi_1(X)$.

+-- {: .un_remark}
###### Remark
This [[regular representation]] can be seen to arise by taking a [[category of elements]] in the same way that the regular representation of a group is gotten by taking its action on itself: we can see that the  _universal covering groupoid_ $\Pi(X)^{(1)}$ in the [[slice category]] $\mathbf{Grpd}/\Pi(X)$ (see the universal covering $\infty$-groupoid below) is just the category of elements of the action of $\Pi(X)$ on itself, and can be topologized in a natural way by lifting the topology on $X$ along the canonical projection $\Pi(X)^{(1)} \to \Pi(X)$; decategorifying this yields $X^{(1)}$.
=--



### In cohesive homotopy theory
 {#InCohesiveHomotopyTheory}

We describe now how the universal cover construction may be understood from the [[nPOV]], using a [[fragment]] of [[cohesive homotopy theory]].

 The basic idea is that the universal cover of a space $X$ is the [[homotopy fiber]] of the canonical morphism

$$
  X \longrightarrow \Pi_1(X)
$$ 

from $X$ to its [[fundamental groupoid]], which exists if both objects are regarded as "[[topological ∞-groupoids]]".  We may think of this as a precise way of the intuitive idea of "[[forcing]] $\Pi_1(X)$ to become trivial in a universal way".  


+-- {: .num_example #ExamplesOfCohesiveToposesOfTopologicalGroupoids}
###### Example
**(cohesive higher toposes of topological groupoids)**

Let $\mathcal{S}$ be some [[∞-cohesive site]] of [[spaces]] and consider 

$$
  \mathbf{H} \coloneqq Sh_\infty(\mathcal{S})
$$ 

the corresponding [[cohesive (∞,1)-topos]] over this site. This is the [[(∞,1)-category]] of "[[topological ∞-groupoids]]" modeled on $\mathcal{S}$.

A canonical choice relating to the traditional discussion would be $\mathcal{S} = Top^\kappa_{lcont}$ a [[small category|small]] [[full subcategory]] of [[Top]] on [[locally contractible topological spaces]], in which case the objects of $\mathbf{H}$ might be called "[[locally contractible topological ∞-groupoids]]".

A more restrictive choice would be $\mathcal{S} = $ [[CartSp]], in which case the objects of $\mathbf{H}$ might be called [[Euclidean-topological ∞-groupoids]].

In fact for the discussion of just universal [[covering spaces]] as opposed to the higher stages in the [[Whitehead tower]] it would be sufficient and more natural to take $\mathcal{S}$ the full subcategory of [[locally simply connected topological spaces]] and consider just the [[(2,1)-category]] $\mathbf{H}$ of [[stacks]] over this site.  

=--

But the following discussion is completely formal and applies globally to all such realizations. Namely all we need is that 

+-- {: .num_defn #AssumptionOnH}
###### Assumption

Assume that

1. $\mathbf{H}$ is a [[cohesive (∞,1)-topos|cohesive (n,1)-topos]]

   $$
     \mathbf{H}
       \array{
         \overset{\Pi}{\longrightarrow}
         \\
         \overset{\Delta}{\longleftarrow}
         \\
         \overset{\Gamma}{\longrightarrow}
         \\
         \overset{\nabla}{\longleftarrow}
       }
     \mathbf{B}
   $$

   over the given [[base (∞,1)-topos|base (n,1)-topos]] of [[n-groupoids]].

1. such that its [[shape modality]] preserves [[homotopy fiber products]] over [[discrete objects]] (objects in the essential image of $\Delta$). 

We write

$$
  &#643; \coloneqq \Delta \Pi
$$

for the induced [[shape modality]] and 

$$
  X \overset{\eta_X}{\longrightarrow} &#643; X
$$

for its [[unit of an adjunction|unit]] morphism ona given object $X$.

=--

+-- {: .num_example}
###### Example

Assumption \ref{AssumptionOnH} is satisfied for the case of $(\infty,1)$-toposes over an [[∞-cohesive site]] and for $(n,1)$-toposes by an $n$-cohesive site as in example \ref{ExamplesOfCohesiveToposesOfTopologicalGroupoids}: by [this prop.](cohesive+infinity-topos#PiPreservesPullbacksOverDiscretes).

=--

Now consider $X \in \mathbf{H}$ any object, for instance a [[topological space]] regarded as a [[0-truncated object|0-truncated]] [[topological infinity-groupoid]].
 
Assume, just for ease of discussion, that $X$ is _geometrically connected_ in that the [[0-truncated object|0-truncation]] of its [[shape]] is [[contractible]]:

$$
  \tau_0(&#643; X) \simeq \ast
  \,.
$$


Using the [[axiom of choice]] in the base topos $\mathbf{H}$ we choose a point 

$$
  \ast \to \tau_1(&#643; X)
  \,.
$$

+-- {: .num_defn }
###### Definition

The _universal cover_ of $X$ is the [[homotopy pullback]] in 


$$
  \array{
    \hat X &\longrightarrow& \ast
    \\
    \downarrow &(pb)& \downarrow
    \\
    X &\underset{L_{\tau_1} \circ \eta_X}{\longrightarrow}& \tau_1(&#643; X)
  }
  \,.
$$


=--

The [[universal property]] of $\hat X$ is immediate from the abstract setup:

1. $\hat X$ is simply connected, in that $\tau_1 &#643; \hat X \simeq \ast$

   This is because $&#643; X$ is discrete by construction, and hence so is $\tau_1(&#643; X)$. So by assumption \ref{AssumptionOnH} applying $&#643;$ to the above square yields another homotopy pullback of the form

   $$
     \array{
       &#643; \hat X &\longrightarrow& \ast
       \\
       \downarrow &(pb)& \downarrow
       \\
       &#643; X &\underset{&#643; \eta_X}{\longrightarrow}& \tau_1(&#643; X)
     }
     \,.
   $$

   Now the [[long exact sequence of homotopy groups]] (in $\mathbf{B}$) applied to this [[homotopy fiber sequence]] is of the form


   $$
     0 \to \pi_1(&#643; \hat X) \longrightarrow \pi_1(&#643; X) \overset{=}{\longrightarrow} \pi_1(\tau_1 &#643; X) \to \cdots
   $$

   which implies that $\pi_1( &#643; \hat X )$ and hence $\tau_1 &#643; \hat X$ is indeed trivial.

1. Let $E \longrightarrow X$ be any other object of $\mathbf{H}_{/X}$ such that $\tau_1(&#643; E) \simeq \ast$, then there is a morphism

   $$
     \array{
       E && \longrightarrow && \hat X
       \\
       & \searrow && \swarrow
       \\
       && X
     }
   $$

   This is because the naturality of the shape unit and of the truncation unit gives a homotopy commuting square of the form

   $$
     \array{
       E &\overset{\eta_E}{\longrightarrow}& &#643; E &\overset{}{\longrightarrow}& \tau_1(&#643; E ) \simeq \ast
       \\
       \downarrow && && \downarrow
       \\
       X &\underset{\eta_X}{\longrightarrow}& &#643; X &\longrightarrow& \tau_1 &#643; X
     }
   $$

   and thus a [[cone]] over the diagram which defines $\hat X$ via its [[universal property]].

This shows that $\hat X$ is the universal cover on abstract grounds.

We may also check explicitly that $\hat X$ is given as the space of homotopy classes of [[paths]] in $X$ from the given basepoint. To that end we use that, at least over the site [[CartSp]], the [[shape modality|shape]] of $X$ is represented by the topological [[path ∞-groupoid]]. See at _[[shape via cohesive path ∞-groupoid]]_.

> The following is old material that deserves to be harmonized a bit more with the above stuff.

+-- {: .un_prop}
###### Proposition

Let $X$ be a suitably well behaved pointed space. The universal cover $X^{(1)}$ of $X$ is (equivalent to) the [[homotopy fiber]] of $X \to \Pi(X)$ in the [[(∞,1)-category]] $\mathbf{H} = Sh_{(\infty,1)}(Top_{cg})$ of [[topological ∞-groupoid]]s.

In other words, the [[principal ∞-bundle]] classified by the [[cocycle]] $X \to \Pi_1(X)$ is the universal cover $X^{(1)}$: we have a [[homotopy pullback]] square

$$
  \array{
    X^{(1)} &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& \Pi(X)
  }
  \,.
$$

=--

+-- {: .query}

[[Urs Schreiber]]: may need polishing.

=--


+-- {: .proof}
###### Proof

We place ourselves in the context of [[topological ∞-groupoid]]s and regard both the space $X$ as well as its [[fundamental ∞-groupoid]] $\Pi(X)$ and its truncation to the [[fundamental groupoid]] $\Pi_1(X)$ as objects in there.

The canonical morphism $X \to \Pi(X)$ hence $X \to \Pi_1(X)$ given by the inclusion of constant paths may be regarded as a [[cocycle]] for a $\Pi(X)$-[[principal ∞-bundle]], respectively for a $\Pi_1(X)$-principal bundle.

Let $\pi_0(X)$ be the set of connected components of $X$, regarded as a topological $\infty$-groupoid, and choose any [[section]]  $\pi_0(X) \to \Pi(X)$ of the projection $\Pi(X) \to \pi_0(X)$.

Then the $\Pi(X)$-principal $\infty$-bundle classified by the [[cocycle]] $X \to \Pi(X)$ is its [[homotopy fiber]], i.e. the [[homotopy pullback]]

$$
  \array{
    UCov(X) &\to& \pi_0(X)
    \\
    \downarrow && \downarrow
    \\
    X &\to& \Pi(X)
  }
  \,.
$$

We think of this topological $\infty$-groupoid $UCov(X)$ as the **universal covering $\infty$-groupoid** of $X$. To break this down, we check that its [[decategorification]] gives the ordinary universal covering space: 

for this we compute the [[homotopy pullback]]

$$
  \array{
    UCov_1(X) &\to& {*}
    \\
    \downarrow && \downarrow^{\mathrlap{x}}
    \\
    X &\to& \Pi_1(X)
  }
  \,,
$$

where we assume $X$ to be connected with chosen baspoint $x$ just to shorten the exposition a little. By the laws of [[homotopy pullback]]s in general and [[homotopy fiber]]s in particular, we may compute this as the ordinary [[pullback]] of a weakly equivalent diagram, where the point $*$ is resolved to the [[generalized universal bundle|universal]] $\Pi_1(X)$-principal bundle

$$
  \mathbf{E}_x \Pi_1(X) = T_x \Pi_1(X)
  \,.
$$

> (More in detail, what we do behind the scenes is this: we regard the diagram as a diagram in the _global_ [[model structure on simplicial presheaves]] on [[Top]]. In there all our topological groupoids are fibrant, hence all we have to ensure is that one of the morphisms of the diagram becomes a fibration, which is what the passage to $\mathbf{E}_x \Pi_1(X)$ achieves. Then the ordinary pullback in the category of simplicial presheaves is the homotopy pullback in $\infty$-prestacks. Then by left exactness of $\infty$-stackification, the image of that in $\infty$-stacks is still a homotopy pullback. )

The topological groupoid $\mathbf{E}_x \Pi_1(X)$ has as objects homotopy classes rel endpoints of paths in $X$  starting at $x$ and as morphisms $\kappa : \gamma \to \gamma'$ it has commuting triangles

$$
  \array{
    && x
    \\
    &{}^{\mathllap{\gamma}}\swarrow && \searrow^{\mathrlap{\gamma'}}
    \\
    y &&\stackrel{\kappa}{\to}&& y'
  }
$$

in $\Pi_1(X)$. The topology on this can be deduced from thinking of this as the [[pullback]]


$$
  \array{
   \mathbf{E}_x \Pi_1(X) &\to& {*}
   \\
   \downarrow && \downarrow^{\mathrlap{x}}
   \\
   \Pi_1(X)^I &\stackrel{d_0}{\to}& \Pi_1(X)
  }
$$

in simplicial presheaves on [[Top]]. Unwinding what this means we find that the open sets in $Mor(\mathbf{E}_x \Pi_1(X))$ are those where the endpoint evaluation produces an open set in $X$.

Now it is immediate to read off the homotopy pullback as the ordinary pullback

$$
  \array{
    UCov_1(X) &\to& \mathbf{E}_x \Pi_1(X)
    \\
    \downarrow && \downarrow
    \\
    X &\to& \Pi_1(X)
    \,.
  }
$$

Since $X$ is categorically discrete, this simply produces the space of objects of $\mathbf{E}_x \Pi_1(X)$ over the points of $X$, which is just the space of all paths in $X$ starting at $x$ with the projection $UCov_1(X) \to X$ being endpoint evaluation. 

This indeed is then the usual construction of the universal covering space in terms of paths, as described for instance in 

* _[Covering spaces, Building a universal cover](http://www.mathreference.com/at-cov,build.html)_ , [Math Reference Project](http://www.mathreference.com/) 

=--


### In the petit $\infty$-toposes over the space

On the other hand, we can view a space $X$ as the little $(\infty,1)$-topos $Sh_{(\infty,1)}(X)$ of $(\infty,1)$-sheaves on $X$.  If $X$ is locally connected and locally simply connected in the "coverings" sense, then $Sh(X)$ is locally 1-connected.

In fact, for the construction of the universal cover we require only the (2,1)-topos $Sh_{(2,1)}(X)$ of sheaves (stacks) of [[groupoids]] on $X$, so we will work in that context because it is simpler.  The construction can be adapted, however, to produce a "universal cover" of any locally 1-connected $(\infty,1)$-topos.

Let $E$ be any (2,1)-topos which is locally 1-connected.  This means that in the unique [[global sections]] [[geometric morphism]] $(E^*,E_*)\colon E\to Gpd$, the functor $E^*$ has a left adjoint $E_!\colon E \to Gpd$, which is automatically $Gpd$-[[indexed functor|indexed]].  The [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos|fundamental groupoid]] of $E$ is defined to be $\Pi_1(E)\coloneqq E_!(*)$, where $*$ is the [[terminal object]] of $E$.

As discussed [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos|here]] in the $(\infty,1)$-case, the construction of $\Pi_1(E)$ is a left adjoint to the inclusion of groupoids into locally 1-connected (2,1)-toposes (which sends $G\mapsto Gpd/G \simeq Gpd^G$).  Thus we have a geometric morphism $E\to \Pi_1(E)$ (where we regard $\Pi_1(E)$ as the (2,1)-topos $Gpd^{\Pi_1(E)}$).

Suppose, for simplicity, that $E$ is connected.  Then $\Pi_1(E)$ is also connected, and so we have an essentially unique functor $*\to \Pi_1(E)$.  We define the **universal cover** of $E$ to be the pullback (2,1)-topos:
$$\array{ E^{(1)} & \to & E \\ \downarrow & & \downarrow \\ * & \to & \Pi_1(E)}$$
(where of course $*$ denotes the terminal (2,1)-topos $Gpd$).

Now observe that $*\to \Pi_1(E)$ is a [[local homeomorphism of toposes]], since we have $Gpd \simeq Gpd/\Pi_1(E)/(*\to \Pi_1(E))$.  Since local homeomorphisms of toposes are stable under pullback, $E^{(1)}\to E$ is also a local homeomorphism, i.e. there exists an object $\widetilde{E}\in E$ and an equivalence $E^{(1)} \simeq E/\widetilde{E}$ over $E$.  Moreover, it is not hard to see that $\widetilde{E}$ can be identified with the pullback
$$\array{ \widetilde{E} & \to & * \\ \downarrow & & \downarrow \mathrlap{\eta} \\ * & \to & E^*(\Pi_1(E)) \mathrlap{= E^*(E_!(*))}}$$
in $E$.  Note that the bottom map $*\to E^*(E_!(*))$ is $E^*$ applied to the unique map $*\to E_!(*)$, while the right-hand map is the unit of the adjunction $E_!\dashv E^*$.

In order to see that this is a sensible definition, we first observe that $E^{(1)}$ is itself locally 1-connected (since it is etale over $E$).  Moreover, it is actually 1-connected, which is equivalent to saying that $E_!(\widetilde{E}) = *$.  This is because the "Frobenius reciprocity" condition for the adjunction $E_!\dashv E^*$ (which is equivalent to saying that $E_!$ is $Gpd$-indexed) applied to the defining pullback of $\widetilde{E}$ implies that we also have a pullback
$$\array{ E_!(\widetilde{E}) & \to & E_!(*) \\ \downarrow & & \downarrow \mathrlap{id} \\ * & \to & E_!(*)}$$
which clearly implies that $E_!(\widetilde{E}) = *$.

Thus, $E^{(1)}$ is a connected and simply connected space with a local homeomorphism to $E$, but is it a covering space?  In other words, is it locally trivial?  Since we have supposed that $E$ is locally 1-connected, as a (2,1)-category it can be generated by 1-connected objects, i.e. objects $U$ such that $E_!(U)\simeq *$.  In particular, we have a 1-connected object $U$ and a [[regular 1-epic]] $U\to *$.

We claim that if $U$ is any 1-connected object of $E$, then $\widetilde{E}$ is trivialized (or split) over $U$, in that $U\times \widetilde{E}$ is equivalent, over $U$, to $U\times E^*S$ for some $S\in Gpd$.  For pulling back the defining pullback to $U$, we obtain
$$\array{ U\times \widetilde{E} & \to & U \\ \downarrow & & \downarrow \mathrlap{U\times \eta} \\ U & \to & U\times E^*(\Pi_1(E)).}$$
But $U\times E^*(\Pi_1(E)) \cong (E/U)^* (\Pi_1(E))$, so to give a map $U \to (E/U)^* (\Pi_1(E))$ over $U$ is the same as to give a map $(E/U)_!(*) \to \Pi_1(E)$ in $Gpd$.  But $(E/U)_!(*)\simeq *$, since $U$ is 1-connected, and $\Pi_1(E)$ is connected, so there is only one such morphism.  Therefore, the two maps $U\to U\times E^*(\Pi_1(E))$ in the pullback above are in fact the same, and in particular both are the pullback to $E/U$ of the map $*\to \Pi_1(E)$.  Thus, $U\times \widetilde{E}$ is equivalent to $(E/U)^*(S) \cong U\times E^*(S)$, where $S= \Omega(\Pi_1(E))$ is the loop object of $\Pi_1(E)$, i.e. what we might call the fundamental *group* of the connected (2,1)-topos $E$.

Therefore, since $\widetilde{E}$ is trivialized over any 1-connected object, and $E$ is generated by 1-connected objects, $\widetilde{E}$ is locally trivial.  Moreover, since $*$ is a [[discrete object]] of $E$, so is $\widetilde{E}$.  Thus, if we specialize all this to the case $E=Sh_{(2,1)}(X)$ of (2,1)-sheaves on a topological space, then we conclude that $\widetilde{E}$ is an honest 1-sheaf on $X$ which, when regarded as a local homeomorphism over $X$, is locally trivial (hence a covering space), connected, and 1-connected---i.e. a universal cover of $X$.


## Examples
  {#Example}

+-- {: .num_example #UniversalCoveringOfCircleRealLine}
###### Example
**([[real line]] is universal covering of [[circle]])**

Let 

1. $\mathbb{R}^1$ be the [[real line]] with its [[Euclidean space|Euclidean]] [[metric topology]];

1. $S^1 \coloneqq \left\{ x\in \mathbb{R}^2 \;\vert\; {\Vert x\Vert} = 1 \right\} \subset \mathbb{R}^2$ be the [[circle]] with its [[subspace topology]] induced from the [[Euclidean plane]].

Consider the [[continuous function]]

$$
  \array{
     \mathbb{R}^1
       &\overset{p}{\longrightarrow}& 
     S^1 \subset \mathbb{R}^2
     \\
     t &\mapsto& (\cos(2\pi t), \sin(2\pi t)) 
  }  
  \,.
$$

This exhibits the universal covering space (def. \ref{CoveringUniversal}) of the circle.

=--

+-- {: .proof}
###### Proof


Let $p \in S^1$ be any point. It is clear that we have a [[homeomorphism]] of the form

$$
  \array{
    S^1 \setminus p
      &\overset{\simeq}{\longrightarrow}&
    (0, 1)  
  }
  \,.
$$

and hence a [[homeomorphism]] of the form

$$
  \array{
    S^1 \times Disc(\mathbb{Z}) &\simeq& (0,1) \times Disc(\mathbb{Z})
    &\overset{\simeq}{\longrightarrow}&
    p^{-1}(S^1 \setminus \{p\}) 
    \\
    && (t,n) &\mapsto& (cos(2\pi n t), \sin(2\pi n t))
  }
  \,.
$$

Now for $p_1 \neq p_2$ two distinct point in $S^1$, their [[complements]] constitute an [[open cover]]

$$
  \left\{ S^1 \setminus p_i \subset S^1  \right\}_{i \in \{1,2\}}
$$

and so this exhibits $p \colon \mathbb{R}^1 \to S^1$ as being covering spaces.

Now 

1. $S^1$ is [[path-connected topological space|path-connected]] and [[locally path-connected topological space|locally path connected]] ([this example](LocallyPathConnectedCircle));

1. $\mathbb{R}^1$ is [[simply connected topological space|simply connected]] ([this example](fundamental+group#EuclideanSpaceFundamentalGroup)).

Therefore $p$ exhibits $\mathbb{R}^1$ as a universal covering space of $S^1$, by def. \ref{CoveringUniversal}.


=--


## Related entries

* [[fundamental theorem of covering spaces]]


## References

See the references at _[[covering space]]_.


[[!redirects universal cover]]
[[!redirects universal covers]]
[[!redirects universal covering spaces]]
[[!redirects universal cover of a topos]]
[[!redirects universal cover of a (2,1)-topos]]
[[!redirects universal cover of an (∞,1)-topos]]
[[!redirects universal cover of an (infinity,1)-topos]]
[[!redirects universal covering topos]]
[[!redirects universal covering (2,1)-topos]]
[[!redirects universal covering (∞,1)-topos]]
[[!redirects universal covering (infinity,1)-topos]]
[[!redirects universal covering groupoid]]
