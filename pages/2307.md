

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[cobordism theory]], a [[generalized cohomology theory]] [[Brown representability theorem|represented]] by a [[Thom spectrum]] is called a _cobordism cohomology theory_. (Dually, the corresponding [[generalized homology theory]] is called _[[bordism homology theory]]_.)

By default "cobordism cohomology" usually refers to what is represented by [[MO]].  The cohomology represented by [[MU]] is _[[complex cobordism cohomology]]_. Both are unified by the [[equivariant cohomology theory]] called [[MR-theory]]. The [[periodic cohomology theory]] version is denoted [[MP]].

On the other hand, [[framed manifold|framed]] cobordism cohomology theory ($M G$ for $G$ the [[trivial group]]) is _[[stable cohomotopy]]_ (by the [[Pontryagin-Thom theorem]]).

See at those entries for more.


## Examples

[[!include flavours of cobordism cohomology theories -- table]]


## Geometric model

We discuss a geometric model for the cobordism cohomology theory,
due to [[Quillen]] \cite[Section 1]{Quillen}.
We concentrate on the complex case, corresponding to the [[Thom spectrum]] $\mathrm{M} \mathrm{U}$.

For a [[manifold]] $X$, the group $\mathrm{M} \mathrm{U}^q(X)$
is constructed as the set of proper [[complex-oriented]] maps
of relative codimension $q$.

Here two [[proper]] [[complex-oriented]] maps $f_i\colon Z_i \to X$
are __cobordant__ if there is a proper complex-oriented map $b\colon W\to X\times\mathbf{R}$
such that $X\times\{0\}$ and $X\times\{1\}$ are [[transversal]] to $b$
and pulling back $b$ to these submanifolds yields $f_0$ and $f_1$.

A [[complex orientation]] of a [[smooth map]] $f\colon Z\to X$
is defined as follows.

If the relative codimension of $f$ is even at all points of $Z$,
then a complex orientation is an equivalence class
of factorizations of $f$
in the form
$$p\circ i\colon Z\to E\to X,$$
where $p\colon E\to X$ is a [[complex vector bundle]]
and $i\colon Z\to E$ is an [[embedding]]
equipped with a [[complex structure]] on its [[normal bundle]].

Two such factorizations $(i,p)$ and $(i',p')$
are equivalent if there is another factorization $(i'',p'')$
together with embeddings of [[complex vector bundles]] $E\to E'$ and $E\to E''$
and a homotopy
$i''\colon X\times[0,1]\to E''\times [0,1]$$
over $[0,1]$
equipped with a [[complex structure]] on its [[normal bundle]]
that restricts to the corresponding complex structures
on $X\times0$ and $X\times1$.

## Related concepts

* the refinement of cobordism cohomology theory to [[differential cohomology]] is [[differential cobordism cohomology]].

* [[cobordism theory determining homology theory]]

* [[equivariant complex cobordism cohomology theory]]

* [[Adams-Novikov spectral sequence]]


\linebreak

[[!include chromatic tower examples - table]]


## References

### General

Original articles introducing cobordism as a [[Whitehead-generalized cohomology theory]]:

* [[Michael Atiyah]], _Bordism and Cobordism_, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 57, Issue 2, April 1961, pp. 200 - 208 ([doi:10.1017/S0305004100035064](https://doi.org/10.1017/S0305004100035064), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahb.pdf))
  > (introducing the concept, with focus on[[MSO]])

* [[Daniel Quillen]], _Elementary Proofs of Some Results of Cobordism Theory Using Steenrod Operations_, Advances in Mathematics 7 (1971), 29–56.
[doi](http://dx.doi.org/10.1016/0001-8708(71)90041-7).

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

  > (relating [[complex cobordism theory]] to [[topological K-theory]] and the [[e-invariant]])

Early survey:

* [[Victor Buchstaber]], _Cobordisms in problems of algebraic topology_,  J Math Sci 7, 629–653 (1977) ([doi:10.1007/BF01084983](https://doi.org/10.1007/BF01084983))

* [[Peter Landweber]], _A survey of bordism and cobordism_, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 100, Issue 2 September 1986, pp. 207-223 ([doi:10.1017/S0305004100066032](https://doi.org/10.1017/S0305004100066032))

 
Textbook accounts:

* {#Stong68} [[Robert Stong]], _Notes on Cobordism theory_, Princeton University Press, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [ISBN:9780691649016](http://press.princeton.edu/titles/6465.html))

* {#Rudyak98} [[Yuli Rudyak]], _On Thom spectra, orientability and cobordism_, Springer Monographs in Mathematics, 1998 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rudyakthom.pdf))



The [[twisted cohomology|twisted]] and [[equivariant cohomology|equivariant]] versions:

* {#Cruickshank99} [[James Cruickshank]], _Twisted  Cobordism and its Relationship to Equivariant Homotopy Theory_, 1999 ([pdf](http://www.collectionscanada.gc.ca/obj/s4/f2/dsk1/tape9/PQDD_0030/NQ46823.pdf), [[Cruickshank99.pdf:file]])

* {#Cruickshank03} [[James Cruickshank]], _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">arXiv:10.1016/S0166-8641(02)00183-9</a>)

### Relation to divisors

Relation of [[complex cobordism cohomology]] with [[divisors]], [[algebraic cycles]] and [[Chow groups]]:

* [[Burt Totaro]], _Torsion algebraic cycles and complex cobordism_, J. Amer. Math. Soc. 10 (1997), 467-493 ([doi:10.1090/S0894-0347-97-00232-4](https://doi.org/10.1090/S0894-0347-97-00232-4))

* [MO discussion](https://mathoverflow.net/a/272131/381)



[[!redirects cobordism cohomology theories]]

[[!redirects cobordism cohomology]]
[[!redirects cobordism cohomologies]]

[[!redirects cobordism homology theory]]
[[!redirects cobordism homology theories]]

[[!redirects cobordism homology]]
[[!redirects cobordism homologies]]

[[!redirects bordism homology]]
[[!redirects bordism homologies]]

[[!redirects bordism cohomology theory]]
[[!redirects bordism cohomology theories]]


