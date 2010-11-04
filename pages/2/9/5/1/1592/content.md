
#Contents#
* automatic table of contents goes here
{:toc}

## Standard definition

Let $X$ be a topological space which is _[[well-connected space|well-connected]]_ in that it is

* [[path-connected space|path-connected]], 

* [[locally path-connected space|locally path-connected]] 

* and [[semi-locally simply-connected space|semi-locally simply-connected]] 

Then there is a connected and [[simply connected space|simply connected]] [[covering space]] $X^{(1)} \to X$ with the [[universal property]] that for any other [[covering space]] $\widetilde{X} \to X$ there is a map of covering spaces $X^{(1)} \to \widetilde{X}$.

There is a functorial construction of a universal covering space of a pointed space

$$
  Top_*^{wc} \to Cov_*
$$

where $Top_*^{wc}$ is the full subcategory of $Top_*$ with objects the well-connected spaces and $Cov$ is the subcategory of $Top_*^2$ of pointed maps of spaces with objects the covering space maps.

Specifically, if $X$ is a space with basepoint $x_0$, we define $X^{(1)}$ to be the space whose points are homotopy classes of paths in $X$ starting at $x_0$, with the projection $X^{(1)}\to X$ projecting to the endpoint of a path.  We can equip this set $X^{(1)}\to X$ with a topology coming from $X$ so that it becomes a universal covering space as above.  As described at [[covering space]], under the correspondence between covering spaces and $\Pi_1(X)$-actions, the space $X^{(1)}$ corresponds to the "regular representation" of $\Pi_1(X)$.


## As the homotopy fiber of $X \rightarrow \Pi_1(X)$

We describe now how the universal cover construction may be understood from the [[nPOV]].  The basic idea is that the universal cover of a space $X$ is the (homotopy) fiber of the map $X\to \Pi_1(X)$ from $X$ to its fundamental groupoid.  We can think of this as a way of precisely saying "make $\Pi_1$ trivial in a universal way."  There are at least two slightly different ways of making this precise in the language of $(\infty,1)$-toposes, depending on whether we view $X$ as a [[little topos]] or as an object of a [[big topos]].

### In terms of big toposes

In this section we work in the big [[(∞,1)-topos]] of sheaves on $TopBalls$, the [[site]] of topological [[balls]] with the [[good open cover]] [[coverage]].  We call objects of this $(\infty,1)$-topos "topological ∞-groupoids."

Now, to a topological space $X$ is associated the [[topological ∞-groupoid|topological groupoid]] $\Pi_1(X)$ -- its [[fundamental groupoid]]. With $X$ regarded as a [[discrete category|categorically discrete]] topological groupoid, there is a canonical morphism

$$
  X \to \Pi(X)
$$

that includes $X$ as the collection of constant paths.



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

We place ourselves in the context of [[topological ∞-groupoid]]s and regard both the space $X$ as well as its [[schreiber:homotopy ∞-groupoid]] $\Pi(X)$ and its truncation to the [[fundamental groupoid]] $\Pi_1(X)$ as objects in there.

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


### In terms of little toposes

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


## Higher universal covering objects

The nPOV descriptions above lend themselves easily to generalization.


### Universal covering objects in a big $(\infty,1)$-topos {#InInftTopos}

+-- {: .query}

[[Urs Schreiber]]: here is something that I am thinking about.

=--


Let $\mathbf{H}$ be a [[locally ∞-connected (∞,1)-topos]] $\mathbf{H} \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}} \infty Grpd$. Write 

$$
  \mathbf{\Pi} := LConst \circ \Pi : \mathbf{H} \to \mathbf{H}
$$

for the _internal_ [[schreiber:homotopy ∞-groupoid]] functor. 

For $n \in \mathbb{N}$ write

$$
  \mathbf{H}_{\leq n} \stackrel{\overset{\tau_{\geq n}}{\leftarrow}}{\overset{}{\hookrightarrow}} \mathbf{H}
$$

for the [[reflective (∞,1)-subcategory]] of [[n-truncated object of an (∞,1)-category|n-truncated objects]] and $\mathbf{\tau}_{\leq n}$ for the localization

$$
  \mathbf{\tau}_{\leq n} : \mathbf{H} \stackrel{\tau_{\leq n}}{\to}
  \mathbf{H}_{\leq n} \hookrightarrow \mathbf{H}
  \,.
$$



Write

$$
  \mathbf{\Pi}_n : \mathbf{H} \stackrel{\mathbf{\tau}_{\leq n}}{\to} \mathbf{H}
$$

for the **[[fundamental infinity-groupoid of a locally infinity-connected (infinity,1)-topos|internal fundamental n-groupoid]]**. For $X \in \mathbf{H}$ we have the [[Postnikov tower in an (∞,1)-category|(∞,1)-Postnikov tower]]

$$
  \cdots \to \mathbf{\Pi}_2(X) \to \mathbf{\Pi}_1(X) \to \mathbf{\Pi}_0(X)
  \,.
$$

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$, the **universal geometric $n$-connected cover** of $X$ is the [[homotopy fiber]] of $X \to \mathbf{\Pi}_n(X)$. 

=--

We have that $\mathbf{\Pi}_n(X) \simeq LConst \tau_{\leq n} \Pi(X)$.

A homotopy-commuting diagram

$$
  \array{
    X^{(n)} &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_n(X)
  }
$$

in $\mathbf{H}$ corresponds by the [[adjoint (∞,1)-functor|adjunction relation]] to diagram 

$$
  \array{
    \Pi(X^{(n)}) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \Pi(X) &\to& {\Pi}_n(X)
  }
$$

in [[∞Grpd]]. This being universal means that $\Pi(X^{(n)})$ is $n$-connected, and universal with that property as an object over $\Pi(X)$.

By running this construction through the Postnikov tower for $\mathbf{\Pi}(X)$, we obtain the **[[Whitehead tower in an (∞,1)-topos]]**

$$
  \cdots \to X^{(2)} \to X^{(1)} \to X
$$

of $X \in \mathbf{H}$.

### Universal covers of a little $(\infty,1)$-topos

If we instead generalize the "little topos" picture, then if $E$ is an $(n,1)$-topos (or, more generally, an $(\infty,1)$-topos) which is locally $n$-connected, we have an $n$-groupoid $\Pi_n(E)$ and we can define the universal $n$-connected cover as the pullback topos
$$\array{ E^{(n)} & \to & E \\ \downarrow & & \downarrow \\ * & \to & \Pi_n(E)}$$
The same arguments as above, generalized from 1 to $n$, show that $E^{(n)}\to E$ is a locally trivial local homeomorphism and that $E^{(n)}$ is $n$-connected.


## Reference


An account of the traditional way to think of the construction of the universal covering space is 

* _[Covering spaces, Building a universal cover](http://www.mathreference.com/at-cov,build.html)_ , [Math Reference Project](http://www.mathreference.com/) 


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
