
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
* automatic table of contents goes here
{:toc}

## Idea

A _principal 2-bundle_ is the generalization of a $G$-[[principal bundle]] over a [[group]] $G$ to a principal structure over a [[2-group]]. It is a special case of a [[principal ∞-bundle]].

For $G = AUT(H)$ the [[automorphism 2-group]] of a group $G$, $G$-principal bundles are equivalent to $H$-[[gerbe]] (see [[gerbe (general idea)]] for more background.). An $H$-[[nonabelian bundle gerbe]] is a model for the total space of an $AUT(H)$-principal 2-bundle.

An expository introduction to the concepts is at [[infinity-Chern-Weil theory introduction]].

## Definition

For $G$ a [[Lie 2-group]], a $G$-principal 2-bundle $P \to X$ is a [[Lie groupoid]] that arises as the [[homotopy fiber]] of a [[cocycle]] $X \to \mathbf{B}G$ in [[?LieGrpd]], i.e. as an [[(∞,1)-pullback]] of the form

$$
  \array{
    P &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    X &\to& \mathbf{B}G
  }
  \,.
$$

By the general rules of [[homotopy pullback]]s, this may be modeled by an ordinary pullback of [[Lie 2-groupoid]]s of the form

$$
  \array{
    P &\to& \mathbf{E}G
    \\
    \downarrow && \downarrow
    \\
    C(U) &\to& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
  \,,
$$

where $\mathbf{E}G$ is the [[universal principal infinity-bundle|universal principal 2-bundle]] ([RS](#RS)).

## Connections 

An ordinary [[principal bundle]] may be equipped with a [[connection on a bundle|connection]] by refining the cocycle

$$
  X \to \mathbf{B} G
$$

to a cocycle

$$
  P_1(X) \to \mathbf{B} G
$$

where $P_1(X)$ is the [[path groupoid]] of $X$.

Similarly, 2-bundles may be equipped with connections by refining their cocycles $X \to \mathbf{B}H$ to cocycles out of a higher path groupoid. Details on this are at [[schreiber:differential cohomology in an (∞,1)-topos -- survey]]. 

## References

The general description of higher bundles internal to generalized spaces modeled as [[∞-stacks]] is discussed in

* Jardine, _Cocycle categories_ ([pdf](http://arxiv.org/abs/math.AT/0605198)) .

The above situation of ordinary $G$-[[principal bundles]] is section 2.1 _[[torsor|Torsors]] for [[sheaves]] of groups_ in that article. The generalization to principal 2-bundles and [[principal ∞-bundles]] is then briefly indicated in section 2.2, _Diagrams and torsors_ .

The point is that in the [[(∞,1)-topos]] of topological or smooth or whatever [[∞-groupoids]] (i.e. in the [[(∞,1)-category]] of [[∞-stacks]] on our category of [[space and quantity|test spaces]]) the above situation generalizes straightforwardly:

For $G$ a [[2-group]], a $G$-principal $2$-bundle is a fibration of groupoids $P \to X$ that arises as the [[fibration sequence|homotopy fiber]] of a classifying morphism $X \to \mathbf{B}G$ (a $2$-[[2-anafunctor|anafunctor]])

$$
 \array{
  P &\to& {*}
  \\
  \downarrow && \downarrow
  \\
  X &\to& \mathbf{B}G
 }
  \,.
$$

This may be modeled by the pullback of the [[universal principal infinity-bundle|universal principal 2-bundle]] as described in

* [[Urs Schreiber]], [[David Roberts]], _The inner automorphism 3-group of a strict 2-group_ ([arXiv](http://arxiv.org/abs/0708.1741))
{#RS}

As ordinary [[principal bundles]], the gadgets obtained this way may be described from various points of view, using [[anafunctor]] cocycles $g : X \stackrel{\simeq}{\to}\leftarrow Y \to \mathbf{B}H$ in [[nonabelian cohomology]], or the corresponding total spaces being 2-[[torsors]] equipped with 2-group [[action]], or certain variants of this. 

Maybe the earliest explicit description of a principal $\infty$-bundle using a [[geometric definition of higher category]] is

* P. Glenn, _Realization of cohomology classes in arbitrary exact categories_, J. Pure Appl. Algebra 25, 1982, no. 1, 33- 105.

This describes [[torsors]] over [[∞-groupoids]] in terms of the corresponding $\infty$-[[action groupoids]].

This theory of higher bundles and [[gerbes]] was made to look manifestly like a systematic [[vertical categorification|categorification]] of the familiar description of ordinary [[principal bundles]] in terms of cocycles and local trivializations in

*  Luca Mauri, PhD thesis, 1998
   ([pdf](http://home.aubg.bg/faculty/aganchev/Category%20Theory/Mauri%20%28papers%29/mauri-2.pdf));

An abridged version is

*  L. Mauri, M. Tierney, _Two-descent, two-torsors and local equivalence_ , J. Pure Appl. Algebra 143 (1999), 313--327.

The first article in the differential-geometric context was

* [[Toby Bartels]], _2-Bundles_ ([arXiv](http://arxiv.org/abs/math.CT/0410328), [web](http://toby.bartels.name/2bundles/))

One should notice that if one uses categories internal to [[diffeological spaces]], then these are (under their [[nerve]]) in particular [[simplicial presheaf|simplicial presheaves]], and that the [[anafunctors]] used as morphisms between these simplicial presheaves represent precisely the morphisms the corresponding [[(∞,1)-category of (∞,1)-sheaves]] using the [[model structure on simplicial presheaves]] or, more lightweight, the structure of a Brown [[category of fibrant objects]] on $\infty$-groupoid valued sheaves.

A description of higher principal bundles (see also [[principal ∞-bundle]]) in terms of the [[model structure on simplicial presheaves]] appears in

* Jardine, Luo, _Higher order principal bundles_ ([pdf](http://www.math.uiuc.edu/K-theory/0681/cocycles6.pdf))

The relation of such 2-categorical constructions of 2-bundles to the one of simplicially modeled $\infty$-bundles by Glenn was established in

* [[Igor Bakovic]], _Bigroupoid 2-torsors_ ([pdf](http://edoc.ub.uni-muenchen.de/9209/1/Bakovic_Igor.pdf)).

Still more explicit descriptions of these constructions are given in 

* Christoph Wockel, _A global perspective to gerbes and their gauge stacks_ ([arXiv](http://arxiv.org/abs/0803.3692)) .

These constructions either work internal to [[Diff]] or internal to some [[topos]].

More generally, a principal 2-bundle is a ([[n-truncated object of an (infinity,1)-category|2-truncated]] [[principal ∞-bundle]]) in a [[(∞,1)-topos]] of [[∞-stack]]s over some [[site]].

This is for instance in

* [[Behrang Noohi]], E. Aldrovandi, _Butterflies II: Torsors for 2-group stacks_,[arXiv](http://arxiv.org/abs/0910.1818)

Notice that [[torsor]] is just another word for (internal) [[principal bundle]].



[[!redirects principal 2-bundles]]