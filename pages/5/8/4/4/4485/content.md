
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $X$ and $Y$ be two [[smooth manifolds]] of finite [[dimension]] and let $f : X \to Y$ be a [[differentiable function]] between them

In components, the definition of submersion reads as follows.

+-- {: .num_defn}
###### Definition

The function $f : X \to Y$ is called a __submersion__ precisely if its [[differential]] $d f\colon T X \to T Y$ is for every point $x \in X$ a [[surjection]] $d f_x\colon T_x X \to T_{f(x)} Y$; hence if all points in its [[image]] are [[regular values]].


=--

More abstractly formulated, this means equivalently the following.

+-- {: .num_defn}
###### Definition


The function  $f : X \to Y$ is a submersion precisely if the canonical morphism

$$
  T X \to X \times_Y T Y \eqqcolon f^* T Y
$$

from the [[tangent bundle]] of $X$ to the [[pullback]] of the tangent bundle of $Y$ along $f$ is a [[surjection]].

=--

This morphism is the one induced by the [[universal property]] of the [[pullback]] from the [[commuting diagram]]

$$
  \array{
    T X &\stackrel{d f}{\to}& T Y
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{f}{\to}& Y
  }
  \,.
$$


In terms of coordinates, the map $f$ is a submersion at a point $p\colon X$ if and only if there exists a [[coordinate chart]] on $X$ near $p$ and a coordinate chart on $Y$ near $f(p)$ relative to which $f$ is the projection $f(x_1,\ldots,x_n) = (x_1,\ldots,x_m)$.  This definition applies to infinite-dimensional manifolds, to non-differentiable maps, even between non-differentiable manifolds.


## Properties

### Pullbacks

While the [[category]] [[Diff]] of (finite dimensional) [[smooth manifold]]s does not have all [[pullback]]s,  the [[pullback]] along a submersion always exists. This is because a submersion is [[transverse maps|transversal]] to every other smooth map into its codomain. Moreover, submersions are stable under pullback.

### Epimorphisms and coverings

The [[surjection|surjective]] submersions (that is the submersions that are also [[epimorphisms]] in [[Diff]]) are [[regular epimorphism]]s.

Surjective submersions form a singleton [[Grothendieck pretopology]] on [[Diff]], and so may be used in [[internal category|internal]] [[category theory]] when using $Diff$ as the ambient category. They appear notably in the definition of [[Lie groupoids]].

### Ehresmann's theorem

[[Ehresmann's theorem]] states that a [[proper morphism|proper]] submersion is a [[locally trivial bundle|locally trivial]] [[fibration]].

### Normal form

For $f : X \to Y$ a submersion, then around every point of $X$ there is an [[open neighbourhood]] on which $f$ restricts to a [[projection]].

### Characterization in infinitesimal cohesion

A [[smooth function]] $f : X \to Y$ between [[smooth manifolds]] is canonically regarded as a morphism in the [[cohesive (∞,1)-topos]] [[SynthDiff∞Grpd]]. With respect to the canonical [[infinitesimal cohesion|infinitesimal neighbourhood inclusion]] $i : $ [[Smooth∞Grpd]] $\hookrightarrow$ [[SynthDiff∞Grpd]] there is a notion of [[formally smooth morphism]] in $SynthDiff\infty Grpd$.

$f$ is a submersion precisely if it is formally smooth with respect to this infinitesimal cohesion.

See the discussion at [[SynthDiff∞Grpd]] for details.

## Variants

The [[algebraic geometry]] analogue of a submersion is a [[smooth morphism of schemes|smooth morphism]].

The analogue between arbitrary [[topological spaces]] (not manifolds) is simply an [[open map]]. There is also [[topological submersion]], of which there are two versions.

## Related concepts

* [[immersion]], **submersion**, [[local diffeomorphism]]


## References

* {#Boothby} [[William M. Boothby]], Def. III 4.3 in: *An introduction to differentiable manifolds and Riemannian geometry*, Academic Press (1975, 1986), Elsevier (2002) &lbrack;[ISBN:9780121160517](https://shop.elsevier.com/books/an-introduction-to-differentiable-manifolds-and-riemannian-geometry-revised/boothby/978-0-08-057475-2), [pdf](https://aetemad.iut.ac.ir/sites/aetemad.iut.ac.ir/files/files_course/william_m._boothby_an_introduction_to_differentibookfi.org_.pdf)&rbrack;


* [[Serge Lang]], chapter XIV in: _Fundamentals of differential geometry_ Springer (1991)

Ehresmann's theorem is due to

* [[Charles Ehresmann]], _Les connexions infinit&#233;simales dans un espace fibr&#233; diff&#233;rentiable_, Colloque de Topologie, Bruxelles (1950), 29-55.

[[!redirects submersion]]
[[!redirects submersions]]

[[!redirects surjective submersion]]
[[!redirects surjective submersions]]

[[!redirects submersion of differentiable manifolds]]
[[!redirects submersions of differentiable manifolds]]
