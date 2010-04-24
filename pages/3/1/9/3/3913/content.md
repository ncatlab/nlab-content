#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **Thom space** $Th(V)$ of a [[vector bundle]] $V \to X$ over a [[topological space]] $X$ is the space obtained by first forming the disk bundle $D(V)$ of (unit) disks in the [[fiber]]s of $V$ and then identifying the boundary of each disk, i.e. forming the quotient by the sphere bundle $S(V)$:

$$
  Th(V) := D(V)/S(V)
  \,.
$$

This is equivalently the [[mapping cone]]

$$
  \array{
    S(V) &\to& *
    \\
    \downarrow^{\mathrlap{p}} && \downarrow
    \\
    X &\to& Th(V)
  }
$$

in [[Top]] of the [[sphere]] [[bundle]] of $V$. Therefore more generally, for $P \to X$ any $S^n$-[[bundle]] over $X$, its Thom space is the the [[mapping cone]]

$$
  \array{
    P &\to& *
    \\
    \downarrow^{\mathrlap{p}} && \downarrow
    \\
    X &\to& Th(P)
  }
$$

of the bundle projection.

## References

* [[eom]], _[Thom space](http://eom.springer.de/t/t092680.htm)_

* [[Rene Thom]],   _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_  Comm. Math. Helv. , 28  (1954)  pp. 17&#8211;86

* R.E. Stong, _Notes on cobordism theory_ , Princeton Univ. Press  (1968)

* W.B. Browder, _Surgery on simply-connected manifolds_ , Springer  (1972)

* [[Dave Husemöller]], _Fibre bundles_ , McGraw-Hill  (1966)

* [[Michael Atiyah]], _Thom complexes_, Proc. London Math. Soc. __11__  (1961)  pp. 291&#8211;310

* Yuli B. [[Rudyak]], _On Thom spectra, orientability, and cobordism_, Springer 1998 [googB](http://books.google.hr/books?isbn=3540620435)
