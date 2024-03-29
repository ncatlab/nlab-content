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
* table of contents
{:toc}

## Idea

An ordinary _[[spin structure]]_ on a [[special orthogonal group]]-[[principal bundle]] is a lift of the corresponding [[cocycle]] $g : X \to \mathbf{B} SO$ through the [[spin group]] [[fibration]] $\mathbf{B} Spin \to \mathbf{B} SO$. The [[obstruction]] for this to exist is a [[cohomology class]] $w_2 \in H^2(X, \mathbb{Z}_2)$ -- the second [[Stiefel-Whitney class]]: it exists precisely if this class is trivial, $[w_2(g)] = 0$.

Conversely, one can ask for an $SO$-cocycle $g$ with prescribed non-trivial obstruction $[w_2(g)] = \alpha \in H^2(X, \mathbb{Z}_2)$. These may usefully be understood as  _$\alpha$-twisted_ $spin$-structures, following the general logic of [[twisted cohomology]].

## Definition

Let 

$$
  \mathbb{Z}_2 \to Spin \to SO \to \mathbf{B} \mathbb{Z}_2
$$ 

be the [[fiber sequence]] in $\mathbf{H} = $[[ETop∞Grpd]] or $\mathbf{H} = $[[Smooth∞Grpd]] given by the [[spin group]] extension of the [[special orthogonal group]] (regarded as a [[topological group]] or as a [[Lie group]], respectibely). Its [[delooping]] defines the second [[Stiefel-Whitney class]]

$$
  w_2 : \mathbf{B }SO \to \mathbf{B}^2 \mathbb{Z}_2
$$ 

so that for any $X \in \mathbf{X}$ we have a [[characteristic class]]

$$
  w_2 : \mathbf{H}(X,\mathbf{B}SO) \to \mathbf{H}(X, \mathbf{B}^2 \mathbb{Z}_2)
$$

$$
  [w_2] : SO Bund(X) \to H^2(X,\mathbb{Z}_2)
  \,.
$$


For $X$ a [[manifold]] define the **groupoid of twisted spin-structures** $SpinStruc_{tw}(X)$ to be the [[(∞,1)-pullback]]

$$
  \array{
    SpinStruc_{tw}(X) &\to& H^2(X, \mathbb{Z}_2)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}SO)
    &\stackrel{w_2}{\to}&
    \mathbf{H}(X, \mathbf{B}^2 \mathbb{Z}_2)
  }
  \,,
$$

where the right vertical morphism picks one [[cocycle]] representative in each [[cohomology]] class.

The [[cocycle]]s in $SpinStruc_{tw}(X)$ are [[twisted bundles|twisted Spin-bundles]].

The obstruction cocycles in $\mathbf{H}(X, \mathbf{B}^2 \mathbb{Z}_2)$ are $\mathbf{B}\mathbb{Z}_2$-[[principal 2-bundle]]s. These may be modeled by $\mathbb{Z}_2$-[[bundle gerbe]]s. In this incarnation the obstruction cocycles $w_2(g)$ above have been discussed as _spin gerbes_ in ([MurraySinger](#MurraySinger)).

## Related concepts

* [[cohomology]], [[twisted cohomology]], [[Whitehead tower]], [[twisted smooth cohomology in string theory]]

* [[orientation]]

* [[twisted differential c-structure]]

  * [[spin structure]], **twisted spin structure**

  * [[string structure]], [[differential string structure]]

  * [[fivebrane structure]], [[differential fivebrane structure]]


## References

A model of twisted spin structures by [[bundle gerbes]] is discussed in

* [[Michael Murray]], Michael Singer, _Gerbes, Clifford modules and the index theorem_  Annals of Global Analysis and Geometry
Volume 26, Number 4, 355-367, DOI: 10.1023/B:AGAG.0000047514.71785.96 ([arXiv:math/0302096](http://arxiv.org/abs/math/0302096))
 {#MurraySinger}

* Atsushi Tomoda, _A relation of spin-bundle gerbes and Mayer's Dirac operator_ ([pdf](http://ton.prosou.nu/official/procNCG20050413.pdf))

The general abstract discussion given above appears as an example in

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Differential Structures]]_

[[!redirects twisted spin structures]]

[[!redirects twisted differential spin structures]]
