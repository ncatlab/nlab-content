
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
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

The _Narasimhan&#8211;Seshadri theorem_ ([Narasimhan-Seshadri 65](#NarasimhanSeshadri65)) identifies certain 
[[moduli spaces of flat connections]] over a ([[compact topological space|compact]]) [[Riemann surface]] $\Sigma$ with ([[compact topological space|compact]]) [[complex manifolds]] of [[stable vector bundles|stable]] [[holomorphic vector bundles]] over $\Sigma$.

For the special case of [[line bundles]] this may be viewed as a special case of the _[[Hodge-Maxwell theorem]]_, also of Deligne's characterization of the [[intermediate Jacobian]], see there at _[Examples -- Picard variety](intermediate+Jacobian#ExamplePicard)_. The analogue of the theorem for higher dimensional [[complex manifolds]] is the _[[Kobayashi-Hitchin correspondence]]_. The special case of that for [[Kähler manifolds]] is the _[[Donaldson-Uhlenbeck-Yau theorem]]_.

## Statement

An indecomposable Hermitian [[holomorphic vector bundle]] $E$ on a [[Riemann surface]] $(\Sigma,g)$ is [[stable vector bundle|stable]] precisely if there is a compatibly [[unitary group|unitary]] [[connection on a bundle|connection]] $\nabla$ on $E$ with constant [[center|central]] [[curvature]]

$$
  \star F_\nabla = - \mu(E)
$$

equal to (minus) the [[slope of a coherent sheaf|slope]] of $E$ (where $\star$ is the [[Hodge star]] operator).

e.g. ([Evans, p. 2](#Evans))

([Atiyah-Bott 83 (8.1)](#AtiyahBott83))


## Applications

### In Quantum field theory

In [[gauge field theories]] such as notably [[Chern-Simons theory]], moduli spaces of flat connections may appear as [[phase spaces]]. The Narasimhan&#8211;Seshadri theorem then provides a [[complex structure]] on these phase spaces and thus a [[spin^c structure]] (see there). This is the data required to obatain the [[geometric quantization by push-forward]] of the phase space. See also at _[[Hitchin connection]]_.

## Related concepts

* [[Hitchin connection]]

* [[quantization of Chern-Simons theory]]

* [[equivariant elliptic cohomology]]

Related theorems

* [[Harder-Narasimhan theorem]]

* [[Koszul-Malgrange theorem]]

* [[Donaldson-Uhlenbeck-Yau theorem]]


## References


The original article is

* {#NarasimhanSeshadri65} [[Mudumbai Narasimhan]], [[C. Seshadri]], _Stable and unitary vector bundles on a compact Riemann surface_, Annals of Mathematics. Second Series 82: 540&#8211;567, (1965) ([JSTOR]( http://www.jstor.org/stable/1970710))

and another proof appeared in 

* [[Simon Donaldson]], _A new proof of a theorem of Narasimhan and Seshadri_,  J. Differential Geom. Volume 18, Number 2 (1983), 269-277. ([EUCLID](http://projecteuclid.org/euclid.jdg/1214437664))


A good general survey and re-discussion is in 

* {#AtiyahBott83} [[Michael Atiyah]], [[Raoul Bott]], section 8 of _The Yang-Mills equations over Riemann surfaces_, Philosophical Transactions of the Royal Society of London. Series A, Mathematical and Physical Sciences
Vol. 308, No. 1505 (Mar. 17, 1983), pp. 523-615 ([jstor](http://www.jstor.org/stable/37156), [lighning summary](http://math.stackexchange.com/a/295505/58526))

A recording of a review talk is here

* {#Narasimhan16} [[Mudumbai Narasimhan]], _Moduli of vector bundles on compact Riemann surfaces_, talk Dec 2016, Bangalore ([video](https://youtu.be/7SuzfmwR6Z0))

Lecture notes include

* {#Evans} [[Jonathan Evans]], _[Aspects of Yang-Mills theory](http://www.homepages.ucl.ac.uk/~ucahjde/yangmills.htm)_, lecture notes,
_Narasimhan-Seshadri theorem_ ([lecture 13 pdf](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture13.pdf), [lecture 14 pdf](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture14.pdf), [lecture 15 pdf](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture15.pdf), [lecture 16 pdf](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture16.pdf))

A textbook providing much of the background definitions involved is

* {#HuybrechtsLehn96} [[Daniel Huybrechts]], [[Mafred Lehn]], _The Geometry of the Moduli Spaces of Sheaves_, 1996 ([[HuybrechtsLehn.pdf:file]])

Related discussion in the context of [[Hitchin connections]] is in 

* {#ScheinostSchottenloher96} Peter Scheinost, [[Martin Schottenloher]], _Metaplectic quantization of the moduli spaces of flat and parabolic bundles_, J. reine angew. Mathematik, 466 (1996) ([web](https://eudml.org/doc/153753))
 
[[!redirects Narasimhan–Seshadri theorem]]
[[!redirects Narasimhan-Seshadri theorem]]