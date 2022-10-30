
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
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[[moduli space|Moduli spaces]] and [[moduli stacks]] of [[vector bundles]] and of $G$-[[principal bundles]] for a complex [[algebraic group]] $G$ have been widely studied in geometry, with many deep results, especially for the case that the base space is a [[complex curve]] or [[algebraic curve]]. In a classical work of [[Grothendieck]] presented in [[FGA]] (see [[FGA explained]]), moduli schemes of [[coherent sheaves]] with certain parameters fixed, so called [[Quot scheme]]s. Later the geometric invariant theory defined other class of moduli spaces of bundles. Especially important is the case of moduli space of [[stable bundle]]s on a Riemann surface which is extremely important for [[mathematical physics]], as the [[Narasimhan–Seshadri theorem]] related it to the [[moduli space of flat connection]] ([[instanton|self-dual solutions of Yang-Mills equations]]; study of spaces of [[conformal blocks]]; [[representation theory]] of [[affine Lie algebras]] and [[loop groups]]; [[integrable systems]], esp. [[Hitchin system]] etc.). 

## Examples

### Bundles over curves and the Langlands correspondence
 {#OverCurvesAndTheLanglandsCorrespondence}

For $G$ some [[complex Lie group]] and $\Sigma$ some [[complex curve]], then the [[moduli stack]] of $G$-[[principal bundles]] on $\Sigma$ (which are equivalently [[holomorphic vector bundles]] when $G = \coprod_{n} GL(n,\mathbb{C})$) has a standard description as a [[double coset space]] [[quotient stack]] of the collection of [[formal power series]] around finitely many points in $\Sigma$ --  the _[[Weil uniformization theorem]]_. We frist disucss an easy toplogical version of this statement in 

* [Over smooth real surfaces](#OverRealSurfaces)

and then we discuss the complex-analytic version 

* [Over complex curves](#OverComplexCurves)

Notice here that the sub-moduli space of _[[stable vector bundles|stable]]_ $GL$-principal bundles is related via the [[Narasimhan-Seshadri theorem]] to that of [[flat connection|flat]] $GL$-[[principal connections]] which is the [[phase space]] of $G$-[[Chern-Simons theory]] and via the [[holographic principle|holographic]] relation of that to the [[WZW model]] an ingredient of the [[modular functor]] and of [[equivariant elliptic cohomology]] etc. This relation serves to explain to some extent why this object is of such interest.

Now the double quotient description is noteworthy because in this incarnation the moduli stack has, via the [[function field analogy]], an immediate analog in [[algebraic geometry]] and in fact in [[arithmetic geometry]] over any [[number field]]. This we discuss below in the section 

* [Over algebraic curves](#OverAlgebraicCurves). 

This parallel or analogy between the moduli stack of $G$-bundles over curves in analytic geometry and in arithmetic geometry is the underlying reason for the parallel between the [[number theory|number theoretic]] [[Langlands correspondence]] and the [[geometric Langlands correspondence]] (review includes [Frenkel 05, section 3.2](#Frenkel05)). It is also at the heart of the [[Weil conjecture on Tamagawa numbers]].

In summary/preview, the analogy is this:

[[!include function field analogy -- table]]

#### Over smooth real surfaces
 {#OverRealSurfaces}

Let 

* $\Sigma$ be a [[smooth manifold|smooth]] [[closed manifold]] of [[dimension]] 2 -- a real [[surface]];

* $G$ a [[connected topological space|connected]] [[topological group]].

* $x \in X$ any point;

* $X^\ast \coloneqq X - \{x\}$

* $D \subset X$ a [[neighbourhood]] of $x$ [[homeomorphism|homeomorphic]] to a [[disk]];

* $D^\ast \coloneqq D - \{x\}$ the corresponding punctured disk around $x$.

+-- {: .num_prop}
###### Proposition

There is a [[bijection]] between 

$$
   [X^\ast,G] \backslash [D^\ast,G] / [D,G]
   \simeq
    G Bund(X)_{\sim}
$$

between the [[double coset space]] of [[topological groups]] as shown on the left and the set of [[equivalence classes]] of topological $G$-[[principal bundles]] on $X$.

=--

e.g. ([Sorger 99, prop. 4.1.1](#Sorger99))

+-- {: .proof}
###### Proof

The key observation is that in $X^\ast$ every $G$-bundle trivializes. Therefore 

$$
  X^\ast \coprod D \longrightarrow X
$$

is a [[cover]] of $X$ which is good enough in that degree-1 [[nonabelian cohomology|nonabelian]] [[Cech cohomology]] on this cover with [[coefficients]] in $G$ classifies $G$-[[principal bundles]].

For this cover the group $[D^\ast, G]$ is precisely that of Cech cocycles, and $[D \coprod X^\ast, G]$ that of Cech coboundaries.

=--

#### Over complex curves 
 {#OverComplexCurves}

(...)

e.g. [Frenkel 05, section 3.2](#Frenkel05)

(...)

#### Over algebraic curves
 {#OverAlgebraicCurves}

Let 

* $k$ an [[algebraically closed field]];

* $G$ an [[affine variety|affine]] [[algebraic group]];

* $x\in X$ a [[closed point]];

* $X^\ast = X- \{x\}$;

* $D \coloneqq Spf(k[ [t_x] ])$;

* $D^\ast = \coloneqq Spf(k( (t_x)) )$;

+-- {: .num_prop}
###### Proposition
**(Weil uniformization theorem)**

There is an Equivalence of [[stacks]]

$$
   [X^\ast] \backslash [D^\ast,G]/[D,G]
   \simeq
   Bun_G(X)
$$

between the double [[quotient stack]] as shown on the left and the stack of algebraic $G$-[[principal bundles]] on $X$.

=--

e.g. ([Sorger 99, theorem 5.1.1](#Sorger99))



## Related concepts

* [[moduli space of flat connections]]

* [[Narasimhan–Seshadri theorem]], [[Donaldson-Uhlenbeck-Yau theorem]], [[Kobayashi-Hitchin correspondence]]

* [[moduli space of (higher) line bundles]]

## References

### General

### Over complex curves


* [[Mudumbai Narasimhan]], [[C. Seshadri]], _Stable and unitary vector bundles on a compact Riemann surface_, Ann. Math. __82__, No. 3 (Nov., 1965), pp. 540-567, [jstor](http://www.jstor.org/pss/1970710), [doi](http://dx.doi.org/10.2307%2F1970710)

* A. Ramanathan, _Stable principal bundles on a compact Riemann surface_, Math Ann __213__, 129-152 (1975).


* {#AtiyahBott83} [[Michael Atiyah]], [[Raoul Bott]], _The Yang-Mills equations over Riemann surfaces_, Philos. Trans. Roy. Soc. London __308__ (1983), 523&#8211;615.

* A. Beauville, Y. Laszlo, _Conformal blocks and generalized theta functions_, Comm. Math. Phys. __164__ (1994), 385&#8211;419.


### Over algebraic curves

* [[Gerd Faltings]], _Vector bundles on curves_, 1995 Bonn lectures, write up by M. Stoll, [pdf](http://www.mathe2.uni-bayreuth.de/stoll/lecture-notes/vector-bundles-Faltings.pdf)

* [[Gerd Faltings]]], _Moduli-stacks for bundles on semistable curves_,   Math. Ann. __304__, 3 (1996) 489-515; _Stable $G$-bundles and projective connections_, J. Algebraic Geom. __2__, 3 (1993) 507-568, [doi](http://dx.doi.org/10.1007/BF01446303), _Algebraic loop groups and moduli spaces of bundles_, J. Eur. Math. Soc. __5__ (2003), 41-68.

* [[Gerd Faltings]], _Line-bundles on the moduli-space of G-torsors_, lecture at MSRI 2002, [video and pdf](http://www.msri.org/publications/ln/msri/2002/langlands/faltings/2/index.html)

* [[Günter Harder]], [[Mudumbai Narasimhan]], _On the cohomology groups of moduli spaces of vector bundle on curves_, Math Ann. __212__, 215-248 (1975).

* [[Nigel Hitchin]], _Stable bundles and integrable systems_,  Duke Math. J.  __54__  (1987)  pp. 91&#8211;114


* V. B. Mehta, [[C. Seshadri]], _Moduli of vector bundles on curves with parabolic structures_, Math. Ann. __248__ (1980), 205&#8211;239. 

* P. E. Newstead, _Characteristic classes of stable bundles of rank 2 over an algebraic curve_, Trans. Amer. Math. Soc. __169__ (1972), 337&#8211;345. 

*  S. Ramanan, _The moduli spaces of vector bundles over an algebraic curve_, Math. Ann. __200__ (1973), 69&#8211;84.

* [[Carlos Simpson]], _Higgs bundles and local systems_, Publ. Math&#233;matiques de l'IH&#201;S __75__ (1992), p. 5-95, [numdam](http://www.numdam.org/item?id=PMIHES_1992__75__5_0)

* [[Constantin Teleman]], C. T. Woodward, _The index formula for the moduli
of G-bundles on a curve_, Ann. Math. __170__, 2, 495&#8211;527 (2009) [pdf](http://annals.princeton.edu/annals/2009/170-2/annals-v170-n2-p01-p.pdf)

* {#Sorger99} [[Christoph Sorger]], _Lectures on moduli  of principal $G$-bundles over algebraic curves_, 1999 ([pdf](http://users.ictp.it/~pub_off/lectures/lns001/Sorger/Sorger.pdf))

* {#Heinloth09} [[Jochen Heinloth]], _Uniformization of $\mathcal{G}$-bundles_ ([pdf](http://staff.science.uva.nl/~heinloth/Uniformization_17-8-09.pdf))

* [[Jonathan Wang]], _The moduli stack of $G$-bundles_, [arXiv:1104.4828](http://arxiv.org/abs/1104.4828v1).

* References for moduli spaces of bundles over *singular* curves are discussed at MathOverflow [here](http://mathoverflow.net/questions/20702/reference-request-moduli-spaces-of-bundles-over-singular-curves/)

### Over arithmetic curves

* {#Hoffmann02} Norbert Hoffmann, _On vector bundles over algebraic and arithmetic curves_, 2002 ([pdf](http://www.maths.mic.ul.ie/hoffmann/diss.pdf))


Review in the context of [[geometric Langlands duality]] is in

* {#Frenkel05} [[Edward Frenkel]], _Lectures on the Langlands Program and Conformal Field Theory_, in _Frontiers in number theory, physics, and geometry II_, Springer Berlin Heidelberg, 2007. 387-533. ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172))


[[!redirects moduli spaces of bundles]]

[[!redirects moduli stack of bundles]]
[[!redirects moduli stacks of bundles]]

[[!redirects moduli space of G-principal bundles]]
[[!redirects moduli spaces of G-principal bundles]]
[[!redirects moduli stack of G-principal bundles]]
[[!redirects moduli stacks of G-principal bundles]]

[[!redirects moduli space of principal bundles]]
[[!redirects moduli spaces of principal bundles]]
[[!redirects moduli stack of principal bundles]]
[[!redirects moduli stacks of principal bundles]]

[[!redirects moduli stack of vector bundles]]
[[!redirects moduli stacks of vector bundles]]

[[!redirects moduli stack of line bundles]]
[[!redirects moduli stacks of line bundles]]
