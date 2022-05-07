

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
 {#Idea}

In [[algebraic topology]], a [[Whitehead-generalized cohomology theory]] [[Brown representability theorem|represented]] by a [[Thom spectrum]] is called a _cobordism cohomology theory_ ([Atiyah 61](#Atiyah61)), in [[duality]] with the corresponding [[generalized homology theory]] called _[[bordism homology theory]]_.  

In both cases, a version of the [[Pontryagin-Thom construction]] identifies the (co)homology classes of these (co)homology theories with [[bordism]]-[[equivalence classes]] of [[manifolds]] (carrying some given [[extra structure]]), whence the name. For [[bordism homology theory]] this was understood since the very inception of the subject ([Thom 54](#Thom54)), while for cobordism cohomology theory this identification is made explicit in 
[Atiyah 61, Sec. 3](#Atiyah61), [Quillen 71](#Quillen71) (relying on results from [Thom 54](#Thom54) nonetheless), see below at _[Geometric model via cobordism classes](#GeometricModel)_.

Accordingly, cobordism cohomology theories are fundamental concepts of [[bordism theory]] in [[differential topology]]. But in  addition they turn out to play a special role in the more abstract [[stable homotopy theory]] of [[complex oriented cohomology theories]] (with its variants such as [[quaternionic oriented cohomology|quaternionic-oriented theories]]) and in the resulting [[chromatic homotopy theory]], see for instance the [[universal complex orientation on MU]]. This way, cobordism cohomology embodies a remarkable confluence of the [[differential topology]] of [[smooth manifolds]] with deep issues in abstract [[homotopy theory]]. 

There are many different flavours of cobordism cohomology theories (see the list of [Examples](#Examples) below), depending on the [[tangential structure]] $f$ encoded in the representing [[Thom spectrum]] $M f$. Among the most commonly considered versions are these:

* The [[cohomology theory]] [[Brown representability theorem|represented]] by [[MO]] is the base case, in the sense that the [[orthogonal group]] $O(n)$ is [[homotopy equivalence|homotopy equivalent]] to the [[general linear group]] $GL_{\mathbb{R}}(n)$ (namely the [[maximal compact subgroup]]), so that $O$-[[tangential structure]] corresponds to no extra [[tangential structure]].

* The cohomology theory represented by [[MU]] is _[[complex cobordism cohomology]]_. Its [[periodic cohomology theory]] version is sometimes denoted [[MP]]. The cohomology theories [[MO]] and [[MU]] are unified by the [[equivariant cohomology theory]] called [[MR-theory]].  

* On the other hand, [[framed manifold|framed]] cobordism cohomology theory [[MFr]] is equivalently _[[stable Cohomotopy theory]]_ (by the [[Pontryagin-Thom theorem]]). In its unstable version as plain [[Cohomotopy theory]] this -- and its relation to cobordism classes of [[normally framed submanifolds]] (the [Pontryagin construction](cohomotopy#RelationToCobordismGroup)) -- this was the historical origin of [[cobordism theory]] (in [Pontrjagin 38](#Pontrjagin38), [Pontrjagin 55](#Pontrjagin55)).


## Geometric model via cobordism classes
 {#GeometricModel}

We discuss a geometric model for the cobordism cohomology theory, due to [Quillen 71, Section 1](#Quillen71). We concentrate on the complex case, corresponding to the [[Thom spectrum]] [[MU]]:


+-- {: .num_prop}  
###### Proposition

For a [[smooth manifold]] $X$, the cobordism [[cohomology group]] 
$\mathrm{M} \mathrm{U}^q(X) \;\coloneqq\; [\Sigma^\infty X_+, \Sigma^q MU]$
is equivalently the set of [cobordism classes](#CobordismClassesOfMaps) of [[proper maps|proper]] [complex-oriented](#ComplexOrientedMaps) maps $f \colon Z \to X$ of [[codimension]] $q$.

=--

([Quillen 71, Prop. 1.2](#Quillen71))

This uses the following definitions:


+-- {: .num_defn #ComplexOrientedMaps}  
###### Definition
**(complex-oriented maps)**

Let $f \colon Z \to X$ be a [[smooth map]].

If the relative [[codimension]] of $f$ is even at all points of $Z$, then a _complex orientation_ is an [[equivalence class]] of factorizations of $f$
in the form 

$$
  p \circ i 
    \;\colon\; 
  Z 
    \longrightarrow 
  E  
    \longrightarrow 
  X
  \,,
$$ 

where $p\colon E\to X$ is a [[complex vector bundle]] and $i \colon Z\to E$ is an [[embedding of topological spaces|embedding]] equipped with a [[complex structure]] on its [[normal bundle]].

Two such factorizations $(i,p)$ and $(i',p')$ are regarded as equivalent if there is another factorization $(i'',p'')$ together with embeddings of [[complex vector bundles]] $E\to E'$ and $E\to E''$ and a [[homotopy]]  $i''\colon X\times[0,1]\to E''\times [0,1]$ over $[0,1]$ equipped with a [[complex structure]] on its [[normal bundle]] that restricts to the corresponding complex structures on $X \times \{0\}$ and $X \times \{1\}$.

=--

+-- {: .num_defn #CobordismClassesOfMaps}  
###### Definition
**(cobordism classes of maps)**

Here two [[proper map|proper]] [complex-oriented](#ComplexOrientedMaps) maps $f_i \colon Z_i \to X$ are called _cobordant_ if there is a proper complex-oriented map $b\colon W\to X\times\mathbf{R}$ such that $X\times\{0\}$ and $X\times\{1\}$ are [[transversal map|transversal]] to $b$ and pulling back $b$ to these submanifolds yields $f_0$ and $f_1$.

=--

([Quillen 71, p. 31](#Quillen71))


## Examples
 {#Examples}

[[!include flavours of cobordism cohomology theories -- table]]


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

* {#Atiyah61} [[Michael Atiyah]], _Bordism and Cobordism_, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 57, Issue 2, April 1961, pp. 200 - 208 ([doi:10.1017/S0305004100035064](https://doi.org/10.1017/S0305004100035064), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahb.pdf))
  > (introducing the concept, with focus on[[MSO]])

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

  > (relating [[complex cobordism theory]] to [[topological K-theory]] and the [[e-invariant]])

* {#Quillen71} [[Daniel Quillen]], _Elementary Proofs of Some Results of Cobordism Theory Using Steenrod Operations_, Advances in Mathematics 7 (1971), 29–56 (<a href="http://dx.doi.org/10.1016/0001-8708(71)90041-7">doi:10.1016/0001-8708(71)90041-7</a>)


Early survey:

* [[Victor Buchstaber]], _Cobordisms in problems of algebraic topology_,  J Math Sci 7, 629–653 (1977) ([doi:10.1007/BF01084983](https://doi.org/10.1007/BF01084983))

* [[Peter Landweber]], _A survey of bordism and cobordism_, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 100, Issue 2 September 1986, pp. 207-223 ([doi:10.1017/S0305004100066032](https://doi.org/10.1017/S0305004100066032))

 
Textbook accounts:

* {#Stong68} [[Robert Stong]], _Notes on Cobordism theory_, Princeton University Press, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [ISBN:9780691649016](http://press.princeton.edu/titles/6465.html), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/stongcob.pdf))

* {#Rudyak98} [[Yuli Rudyak]], _On Thom spectra, orientability and cobordism_, Springer Monographs in Mathematics, 1998 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rudyakthom.pdf))



The [[twisted cohomology|twisted]] and [[equivariant cohomology|equivariant]] versions:

* {#Cruickshank99} [[James Cruickshank]], _Twisted  Cobordism and its Relationship to Equivariant Homotopy Theory_, 1999 ([pdf](http://www.collectionscanada.gc.ca/obj/s4/f2/dsk1/tape9/PQDD_0030/NQ46823.pdf), [[Cruickshank99.pdf:file]])

* {#Cruickshank03} [[James Cruickshank]], _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">arXiv:10.1016/S0166-8641(02)00183-9</a>)


[[!include Pontryagin-Thom construction -- references]]



### Relation to divisors

Relation of [[complex cobordism cohomology]] with [[divisors]], [[algebraic cycles]] and [[Chow groups]]:

* [[Burt Totaro]], _Torsion algebraic cycles and complex cobordism_, J. Amer. Math. Soc. 10 (1997), 467-493 ([doi:10.1090/S0894-0347-97-00232-4](https://doi.org/10.1090/S0894-0347-97-00232-4))

* [MO discussion](https://mathoverflow.net/a/272131/381)



[[!redirects cobordism cohomology theories]]

[[!redirects Cobordism cohomology theory]]
[[!redirects Cobordism cohomology theories]]

[[!redirects cobordism cohomology]]
[[!redirects cobordism cohomologies]]

[[!redirects Cobordism cohomology]]
[[!redirects Cobordism cohomologies]]


[[!redirects cobordism homology theory]]
[[!redirects cobordism homology theories]]

[[!redirects cobordism homology]]
[[!redirects cobordism homologies]]

[[!redirects bordism homology]]
[[!redirects bordism homologies]]

[[!redirects bordism cohomology theory]]
[[!redirects bordism cohomology theories]]

[[!redirects Cobordism theory]]

