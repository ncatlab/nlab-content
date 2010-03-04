
#Contents#
* automatic table of contents goes here
{:toc}

## Standard definition

Let $X$ be a topological space which is _[[well-connected space|well-connected]]_ in that it is

* [[path-connected space|path-connected]], 

* [[locally path-connected space|locally path-connected]] 

* and [[semi-locally simply-connected space|semi-locally simply-connected]] 

Then there is a connected and [[simply connected space|simply connected]] [[covering space]] $X^{(1)} \to X$ with the [[universal property]] that for any other [[covering space]] $\widetilde{X} \to X$ there is a map of covering spaces $X^{(1)} \to \widetilde{X}$. 

There is a functorial construction of a covering space of a pointed space

$$
  Top_*^{wc} \to Cov_*
$$

where $Top_*^{wc}$ is the full subcategory of $Top_*$ with objects the well-connected spaces and $Cov$ is the subcategory of $Top_*^2$ of pointed maps of spaces with objects the covering space maps.

+-- {: .query}

[[David Roberts]]: We should move the construction of the universal covering space from [[covering space]] to here, but I have limited time.

[[Urs Schreiber]]: some of it is now below. Some not.

=--


## As the homotopy fiber of $X \hookrightarrow \Pi_1(X)$

We describe now how the universal cover construction may be understood from the [[nPOV]]. In the next section this point of view is then used to conceive notions of covering spaces and higher covering spaces in more general contexts of [[(∞,1)-topos]]es.

To a topological space $X$ is associated the [[topological ∞-groupoid|topological groupoid]] $\Pi_1(X)$ -- its [[fundamental groupoid]]. With $X$ regarded as a [[discrete category|categorically discrete]] topological groupoid, there is a canonical morphism

$$
  X \to \Pi(X)
$$

that includes $X$ as the collection of constants paths.



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






## Universal covering objects in an $(\infty,1)$-topos {#InInftTopos}

+-- {: .query}

[[Urs Schreiber]]: here is something that I am thinking about.

=--


Let $\mathbf{H}$ be a [[locally contractible (∞,1)-topos]] $\mathbf{H} \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}} \infty Grpd$. Write 

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

+-- {: .query}

[[Urs Schreiber]]: various $n$s here will be off by $\pm 1$. Too tired to straighten this out right now.

=--


Write

$$
  \mathbf{\Pi}_n : \mathbf{H} \stackrel{\mathbf{\tau}_{\leq n}}{\to} \mathbf{H}
$$

for the internal **homotopy $n$-groupoid**. For $X \in \mathbf{H}$ we have the [[Postnikov tower in an (∞,1)-category|(∞,1)-Postnikov tower]]

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

By running this construction through the Postnikov tower for $\mathbf{\Pi}(X)$, we obtain the **Whitehead tower**

$$
  \cdots \to X^{(2)} \to X^{(1)} \to X
$$

of $X \in \mathbf{H}$.


## Reference


An account of the traditional way to think of the construction of the universal covering space is 

* _[Covering spaces, Building a universal cover](http://www.mathreference.com/at-cov,build.html)_ , [Math Reference Project](http://www.mathreference.com/) 


[[!redirects universal cover]]