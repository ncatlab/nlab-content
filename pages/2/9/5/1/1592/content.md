
#Contents#
* automatic table of contents goes here
{:toc}

## Standard definition

Let $B$ be a topological space which is [[path-connected space|path-connected]], [[locally path-connected space|locally path-connected]] and [[semi-locally simply-connected space|semi-locally simply-connected]] (or more briefly, _[[well-connected space|well-connected]]_). Then there is a connected and simply connected [[covering space]] $B^{(1)} \to B$ such that for any other covering space $\widetilde{B} \to B$ there is a map of covering spaces $B^{(1)} \to \widetilde{B}$. There is a functorial construction of a covering space of a pointed space
$$
Top_*^{wc} \to Cov_*
$$
where $Top_*^{wc}$ is the full subcategory of $Top_*$ with objects the well-connected spaces and $Cov$ is the subcategory of $Top_*^2$ of pointed maps of spaces with objects the covering space maps.

+-- {: .query}

[[David Roberts]]: We should move the construction of the universal covering space from [[covering space]] to here, but I have limited time.

[[Urs Schreiber]]: some of it is now below. Some not.

=--

## As the homotopy fiber of $X \hookrightarrow \Pi_1(X)$

To a topological space $X$ is associated the [[topological groupoid]] $\Pi_1(X)$ -- its [[fundamental groupoid]]. With $X$ regarded as a [[discrete category|categorically discrete]] topological groupoid, there is a canonical morphism

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






## Universal covering objects in an $(\infty,1)$-topos

+-- {: .query}

[[Urs Schreiber]]: here is something that I am thinking about.

=--


...



## Reference


An account of the traditional way to think of the construction of the universal covering space is 

* Karl Dahlke, _[Covering spaces, Building a universal cover](http://www.mathreference.com/at-cov,build.html)_ , [Math Reference Project](http://www.mathreference.com/) 


[[!redirects universal cover]]