
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
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

A (smooth) principal bibundle is a (smooth) [[principal bundle]] and notably a [[groupoid principal bundle]] with compatible [[actions]] on both the left and right.

They arise in two related situations: as the objects used to define [[nonabelian bundle gerbe]]s and as [[anafunctor]]-like morphisms between [[Lie groupoid]]s. The former is a special case of the latter. The general concept of [[bundle]] has no action and so there is nothing to do to make it a bibundle.  However, suppose that $G$ is a [[group]] and you are interested in [[G-bundle]]s.  Then a __$G$-bibundle__ is a bundle that is simultaneously a left $G$-bundle and a right $G$-bundle, such that the left and right actions of $G$ commute. This is a bibundle in the first sense. 

A __principal bibundle__ is a [[principal bundle|principal]] $G$-bundle with commuting left and right $G$-actions.

More generally, a __right principal bibundle__ between two groupoids $G$ and $H$ is a set $P$ with a $G$-$H$ [[biaction]] such that the map from $P$ to the objects of $G$ is a surjective submersion and such that the fibers are acted on by $H$ freely and transitively. See [discussion](http://sbseminar.wordpress.com/2007/07/23/a-bicategory-of-groupoids/).

This subsumes the notion of principal  bibundle defined above. A principal $G$-bibundle is the same as __right principal bibundle__ from the Lie groupoid $X$ (thought of as a [[discrete groupoid]] with only identity morphisms) to the underlying groupoid of the [[automorphism 2-group]] $(Aut(G), G)$. See Example 14 of Chris Schommer-Pries _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ [arXiv:0911.2483](http://arxiv.org/abs/0911.2483/).  

Similarly, let $(H, G)$&#8230; be a [[strict 2-group]]. Then an __$(H, G)$&#8230;-bibundle__ is a (right) principal $G$-bundle with an equivariant map $\phi: P \to H$. See [Murray's talk](http://www.mpim-bonn.mpg.de/digitalAssets/7050_Murray.pdf).

For a [[Lie groupoid]] $G$, a left (right) $G$-bundle $E$ over $X$ (equipped with  $\tau: X \to M$) is a left (right) $G$-action on $E$, and a $G$-invariant map
$\pi: E  \to M$. Then a __$G$-$H$-bibundle__ $E$ is a left $G$-bundle and a right $H$-bundle. See [Morton's talk](http://www.math.uwo.ca/~jmorton9/seminar/gpdrep.pdf).


The description of principal bibundles as maps to a [[2-group]] shows that there is an induced structure of a 2-group on the category of principal bibundles over a space. In fact this holds whenever the muliplication of the target $2$-group is given by a _bibundle_, and this allows the concept of a non-abelian [[bundle gerbe]] to be generalized past the classical setting of strict [[Lie 2-group]]s $(H,G)$. A general discussion occurs in Chris Schommer-Pries' [Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group](http://arxiv.org/abs/0911.2483/) in section 3.3,  see especially Example 61. 


Now let $G$ and $H$ be Lie groupoids. A [[manifold]] $M$ with a left $G$-action and a right $H$-action which commute, i.e., $(g \cdot m) \cdot h = g \cdot (m \cdot h)$, whenever defined, is called a __smooth $G$-$H$ bibundle__. See Definition 2.8 in _[Stacky Lie Groupoids](http://arxiv.org/abs/math/0702399)_.

## Properties

### Relation between Lie groupoid bibundles and Morita/stack morphisms

(...)

We discuss how Lie groupoid bibundles correspond to [[Morita morphism]] (morphisms of [[differentiable stacks]]/[[smooth stacks]]) between the Lie groupoids.

For $\mathcal{G}_\bullet$ a [[Lie groupoid]] write

 
$\;\;\;\mathcal{G} \in $ [[smooth groupoid|SmoothGrpd]] $\hookrightarrow $ [[Smooth∞Grpd]]

for its incarnation as a [[differentiable stack]], hence as a [[smooth stack]]. The fact that the [[Lie groupoid]] is explicitly a [[simplicial object]] means that it induces not just this object of [[Smooth∞Grpd]] but in fact a [[groupoid object in an (∞,1)-category|groupoid object internal]] to [[Smooth∞Grpd]]. By the discussion there, this is witnessed by the canonical map

$$
  \mathcal{G}_0 \to \mathcal{G}
$$

in [[Smooth∞Grpd]] which is the [[atlas]] given by the inclusion of the manifold object [[objects]] $\mathcal{G}_0 \in $ [[SmoothMfd]] $\hookrightarrow$ [[Smooth∞Grpd]].

For any $X \in $ [[Smooth∞Grpd]] a morphism $f \colon X \to \mathcal{G}$ modulates a $\mathcal{G}$-[[groupoid principal bundle]] over $X$, namely the [[homotopy pullback]] $f^\ast \mathcal{G}_0$ in 

$$
  \array{
    f^* \mathcal{G}_0 &\to& \mathcal{G}_0
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{f}{\to}& \mathcal{G}
    \,.
  }
$$

If $f$ is presented by an actual map of Lie groupoids (say because $X$ is presented by a suitable [[resolution]]), then, by the discussion at [[homotopy pullback]], $f^*$ is ... This makes manifest how this has a right $\mathcal{G}$-[[groupoid action]].

Finally then for $\mathcal{X}_\bullet$ and $\mathcal{G}_\bullet$ two Lie groupoids and $f \;\colon\; \mathcal{X} \to \mathcal{G}$ a morphism in [[Smooth∞Grpd]] between the corresponding [[differentiable stacks]], we obtain first the $\mathcal{G}$-[[groupoid principal bundle]] $f^* \mathcal{G}_0 \stackrel{p}{\to} \mathcal{X}$ and then by further homotopy pullback also the left $\mathcal{X}$-[[groupoid principal bundle]] $p^* \mathcal{X}_0$:

$$
  \array{
    p^* \mathcal{X}_0 &\to&
    f^* \mathcal{G}_0&\to& \mathcal{G}_0
    \\
    \downarrow && \downarrow^{\mathrlap{p}} && \downarrow
    \\
    \mathcal{X}_0
    &\to&
    \mathcal{X}
    &\stackrel{f}{\to}&
    \mathcal{G}
  }
  \,.
$$

Here $p^* \mathcal{X}_0$ still has a right $\mathcal{G}_\bullet$-action, albeit no longer a principal one. (...) Hence it is an $\mathcal{X}_\bullet$-$\mathcal{G}_\bullet$-groupoid bibundle, principal for the left action.

Conversely, given a $\mathcal{X}_\bullet$-$\mathcal{G}_\bullet$-Lie groupoid bibundle which is principal on the left

$$
  \array{
    \mathcal{P} &\to& \mathcal{B} &\to& \mathcal{G}_0
    \\
    \downarrow && && \downarrow
    \\
    \mathcal{X}_0 &\to& \mathcal{X} && \mathcal{G}
  }
$$

we recover the Morita morphism $f$ that it coresponds to by the [[Giraud-Rezk-Lurie axioms]]: first $p$ is the induced map between the [[homotopy colimits]] of the Cech nerves of the two left horizontal maps

$$
  \array{
    \mathcal{P} &\to& \mathcal{B} &\to& \mathcal{G}_0
    \\
    \downarrow && \downarrow^{\mathrlap{p}} && \downarrow
    \\
    \mathcal{X}_0 &\to& \mathcal{X} && \mathcal{G}
  }
$$

and then $f$ is similarly the map between the homotopy colimits of the Cech nerves of the two right vertical maps.


(...)

### Relation to groupoid convolution bimodules

The [[2-functor]] from [[Lie groupoids]] to [[C-star-algebras]] and [[Hilbert C-star-bimodules]] between them given by forming [[groupoid convolution algebras]] is naturally exhibited by Lie groupoid bibundles: the [[groupoid convolution algebra]] of the totoal space of hte bibindle becomes a [[bimodule]] over the two other groupoid convolution algebras.

(...)


## References

* [[Chris Schommer-Pries]] _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ [arXiv:0911.2483](http://arxiv.org/abs/0911.2483/) 

* [[Michael Murray]], _Bispaces and bibundles_ ([pdf slides](http://www.mpim-bonn.mpg.de/digitalAssets/7050_Murray.pdf))

* [[Michael Murray]], [[David Roberts]], [[Danny Stevenson]], _On the existence of bibundles_ LMS (2012)([arXiv:1102.4388](http://arxiv.org/abs/1102.4388))

[[!redirects bibundle]]
[[!redirects bibundles]]
