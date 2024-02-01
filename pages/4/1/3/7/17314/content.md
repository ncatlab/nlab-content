
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[functor]] $F\colon \mathcal{C}\to \mathcal{D}$ is said to _lift_ [[limits]] of a particular shape $I$ if for any diagram $J:I\to C$, any limiting [[cone]] for $F \circ J$ in $\mathcal{D}$ is the image of a limiting cone for $J$ in $\mathcal{C}$.

The above definition is not invariant under [[equivalences of categories]].
It can be made invariant if we demand instead
that any limiting cone for $F\circ J$ is isomorphic
to the image of a limiting cone for $J$. Alternatively, this says that, if $F \circ J$ has a limit, then $J$ also has a limit and that limit is [[preserved limit|preserved]] by $F$.

## Terminological remarks

Lifting limits is closely related to [[created limits|creating them]].  The relationships between these notions were the subject of a post by Aleks Kissinger at the categories mailing list, [here](https://raw.githubusercontent.com/punkdit/categories/26b751bbcbe6765fe447e805629ff6416f4c38b1/gmane/science/mathematics/categories/6644), but there is [some dispute](https://nforum.ncatlab.org/discussion/7024/lifted-limit/?Focus=56765#Comment_56765) about its correctness.

## Related concepts

* [[preserved limit]]

* [[reflected limit]]

* [[created limit]]

* [[topological concrete category]] 

* **lifted limit** 

[[!redirects lifted limits]]

## References

See Definition 13.17 in [[Adamek]], [[Herrlich]], [[Strecker]]: [Abstract and Concrete Categories](http://katmat.math.uni-bremen.de/acc/acc.pdf).  Remark 13.38 provides a useful diagram of relations between reflected/created/lifted limits.
