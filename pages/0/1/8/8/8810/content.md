
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[vector bundle]] (typically considered in [[complex-analytic geometry]] or [[algebraic geometry]]) is called _(semi-)stable_ if it is a _[[GIT-stable point|(semi-)stable point]]_ in the [[moduli space of bundles]] in the sense of [[geometric invariant theory]]. 

Under suitable conditions this is equivalent to a certain [[inequality]] on the [[slope of a coherent sheaf|slopes]] of the sub-bundles (see [below](#OverARiemannSurface)), and this inequality is what tends to be stated as the definition of stability of vector bundles.

For more discussion (informal and formal) of this concept of stability see at _[[Bridgeland stability condition]]_.



## Definition

### Over a Riemann surface / over an algebraic curve
 {#OverARiemannSurface}

For $\Sigma$ a [[Riemann surface]], a [[complex vector bundle]] $E \to \Sigma$ over $\Sigma$ is called **(slope-)stable** if for all non-trivial subbundles $K \hookrightarrow E$ the [[inequality]]

$$
  \mu(K) \lt \mu(E)
$$

between their [[slope of a coherent sheaf|slopes]] holds, i.e. if the inequality

$$
  \frac{deg(K)}{rank(K)}
  \lt
  \frac{deg(E)}{rank(E)}
$$

holds between the fractions of [[degree of a coherent sheaf|degree]] and [[rank]] of the vector bundles  holds.

e.g. ([Huybrechts-Lehn 96, bottom of p. 24](#HuybrechtsLehn96))


### Over a general (Noetherian) scheme

e.g. ([Huybrechts-Lehn 96, def. 1.2.4, def. 1.2.12](#HuybrechtsLehn96))



## Examples

Every [[line bundle]] is slope-stable. The [[extension]] of a degree-0 line bundle by a degree-1 line bundle is stable.

e.g. ([Huybrechts-Lehn 96, example 1.2.10](#HuybrechtsLehn96))

## Properties

### Relation to GIT-stability 
 {#RelationToGITStability}

The slope-(semi-)stable vector bundles are essentially the [[stable point|(semi-)stable points]] in the sense of [[geometric invariant theory]] in the [[moduli space of bundles]]. The precise statement is discussed in ([King 94](#King94)) reviewed for instance in ([Saiz 09, section 2.3](#Saiz09).


### Relation to connections

The [[Narasimhan–Seshadri theorem]] identifies [[moduli spaces]] of stable vector bundles over [[complex curves]] with those of certain [[flat connections]].

The [[Donaldson-Uhlenbeck-Yau theorem]] relates semi-stable vector bundles over [[Kähler manifolds]] to [[Hermite-Einstein connections]].

Still more generally, the [[Kobayashi-Hitchin correspondence]] relates semi-stable vector bundles over [[complex manifolds]] to Hermite-Einstein connections.

### Relation to Bridgeland stability conditions

Slope-stability of vector bundles is a special case of a [[Bridgeland stability condition]], see [there](Bridgeland+stability+condition#SlopeStabilityOfVectorBundles) For review see e.g. ([Engenhorst 14, sections 3 and 4](#Engenhorst14)) and see [King 94](#King94).

## Related concepts

* [[Harder-Narasimhan filtration]]

* [[moduli space of bundles]]

* [[stable point]]

* [[positive line bundle]], [[ample line bundle]]

* [[Bridgeland stability condition]]

* [[geometric invariant theory]]

## References


The concept was introduced in 

* [[David Mumford]], _Geometric invariant theory_, Ergebnisse Math. Vol 34 Springer (1965)

* F. Takemoto, _Stable vector bundles on algebraic surfaces_, Nagoya Math. J.  47 (1972) 29-48 ([euclid](http://projecteuclid.org/euclid.nmj/1118798682)); _II_, 52 (1973) ([euclid](http://projecteuclid.org/euclid.nmj/1118794885))

*  {#MumfordFogartyKirwan65} [[David Mumford]], John Fogarty, Frances Clare Kirwan, _Geometric invariant theory_, Ergebnisse der Mathematik und ihrer Grenzgebiete (2) __34__, Springer-Verlag (1965)



Review is in 

* {#AtiyahBott83} [[Michael Atiyah]], [[Raoul Bott]], section 7 of _The Yang-Mills equations over Riemann surfaces_, Philosophical Transactions of the Royal Society of London. Series A, Mathematical and Physical Sciences
Vol. 308, No. 1505 (Mar. 17, 1983), pp. 523-615 ([jstor](http://www.jstor.org/stable/37156), [lighning summary](http://math.stackexchange.com/a/295505/58526))


A textbook account is in

* {#HuybrechtsLehn96} [[Daniel Huybrechts]], [[Manfred Lehn]], _The Geometry of the Moduli Spaces of Sheaves_, 1996 ([[HuybrechtsLehn.pdf:file]])

More discussion with regards to [[geometric invariant theory]] and [[Bridgeland stability conditions]] is in

* {#King94} [[Alastair King]], _Moduli of representations of finite dimensional algebras_, The Quarterly Journal of Mathematics 45.4 (1994): 515-530 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.623.649&rep=rep1&type=pdf))

* {#Engenhorst14} Jan Engenhorst, _Bridgeland Stability Conditions in Algebra, Geometry and Physics_, 2014 ([pdf](https://www.freidok.uni-freiburg.de/fedora/objects/freidok:9595/datastreams/FILE1/content))


See also

* Paolo de Bartolomeis, [[Gang Tian]], _Stability of complex vector bundles_, J. Diff. Geometry __43__:2 (1996) ([pdf](https://www.intlpress.com/JDG/archive/1996/43-2-231.pdf))

* Wei-Ping Li, Zhenbo Qin, _Stable vector bundles on algebraic surfaces_ ([pdf](http://arxiv.org/pdf/math/9411233.pdf))

* {#Saiz09} Alfonso Zamora Saiz, _On the stability of vector bundles_, Master thesis 2009 ([[SaizStableBundles.pdf:file]])



Discussion for [[equivariant vector bundles]] is in 

* [[C. S. Seshadri]], _Moduli of $\pi$-Vector Bundles over an Algebraic Curve_, In: Marchionna E. (eds) Questions on Algebraic Varieties. C.I.M.E. Summer Schools, vol 51. Springer, Berlin, Heidelberg ([doi:10.1007/978-3-642-11015-3_5](https://doi.org/10.1007/978-3-642-11015-3_5))

* Oscar García-Prada, _Invariant connections and vortices_,  Commun.Math. Phys. (1993) 156: 527 ([doi:10.1007/BF02096862](https://doi.org/10.1007/BF02096862))

[[!redirects stable vector bundles]]

[[!redirects stable coherent sheaf]]
[[!redirects stable coherent sheaves]]