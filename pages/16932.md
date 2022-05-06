

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The Reissner-Nordstr&#246;m solution to the [[equations of motion]] of [[Einstein-Maxwell theory]] describes the [[spacetime]] outside of a [[electric charge|electrically charged]] (and/or [[magnetic charge|magnetically charged]]) point [[mass]], hence describes a _charged_ [[black hole]].

## Details

### Metric

For [[mass]] $M$, [[electric charge]] $Q$ and [[magnetic charge]] $P$ the [[pseudo-Riemannian metric]] for the Reissner-Nordstr&#246;m spacetime is, in [[polar coordinates]] $(t,r,\phi,\theta)$ on $\mathbb{R}^4 - \{0\} = \mathbb{R} \times \mathbb{R}_{\gt 0} \times S^2$, given by

$$
  ds^2_{M,Q,P} \coloneqq - H d t^2 + H^{-1} d r^2 + r^2 ds_{S^2}^2
$$

where (in natural units)

$$
  H \coloneqq 1 - \frac{M}{r} + \frac{Q^2 + P^2}{r^2}
  \,.
$$

The corresponding [[Faraday tensor]]/electromagnetic [[field strength]] [[curvature|curvature 2-form]] is

$$
  F = \frac{Q}{r^2} d t \wedge d r + P \sin(\theta) d\theta \wedge d\phi
  \,.
$$

> (check sign)


### Horizons

The function $H$ above vanishes at

$$
  r_{\pm} 
    \coloneqq 
  \tfrac{1}{2}\left(
    M \pm \sqrt{M^2 - 4 (P^2 + Q^2)}
  \right)
  \,.
$$

The larger of the two solutions is an [[event horizon]], the other is a [[Cauchy horizon]]. In the case that they coincide, for $M = 2\sqrt{Q^2 + P^2}$, one speaks of an [[extremal black hole]] (at least when also $P = 0$).

## Properties

### Penrose diagrams
 {#PenroseDiagrams}

The [[Penrose diagram]] for maximally extended RN black holes (from [HE 73, Section 5.5](#HE73)):

\linebreak

\begin{imagefromfile}
    "file_name": "RNBHPenroseDiagramHEFig25.jpg",
    "width": 550,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [HE 73, Fig. 25](#HE73)"
\end{imagefromfile}

\linebreak

\linebreak

\begin{imagefromfile}
    "file_name": "RNBHPenroseDiagramHEFig26.jpg",
    "width": 550,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [HE 73, Fig. 26](#HE73)"
\end{imagefromfile}


### Interior solutions
 {#InteriorSolutions}

Instead of having a mass and charge of singular support at the singular locus of the RN-spacetime, one may consider a finite mass and charge distribution, i.e. a "charged star". Outside of this mass/charge distribution then the metric is the RN-spacetime as above, but in the interior it becomes smoothed out to a non-singular interior solution.

Several attempts have been made to round out the Reissner metric with an interior. [Tiwari-Rao-Kanakamedala 85](#TiwariRaoKanakamelda85)  found an interior with the condition $g_{11} g_{44} = 1$, which obviously holds for the exterior Reissner, but does not match the interior Schwarzschild solution for e = 0. [Kyle-Martin 67](#KyleMartin67) found a rather complicated solution. They discussed the self-energy of the fields of charged matter. [Wilson 69](#Wilson69) modified this solution assuming a different value for the total charge. [Cohen-Cohen 69](#CohenCohen69) applied this solution to the special case of a charged thin shell and showed that the energy density of the electromagnetic field contributes to the mass. [Boulware 73](#Boulware73) studied the time development of thin shells. [Graves-Brill 60](#GravesBrill60) considered a possible oscillatory character of the Reissner-Nordstr&#246;m metric by examining the metric by Kruskal-like coordinates [Bekenstein 71](#Bekenstein71) studied another ansatz for the stress-energy-tensor of charged matter. [Krori-Jayantimala 75](#KroriJayantimala75) made use of the same ansatz, and he found a solution free of singularities. [Gautreau-Hoffman 73](#GautreauHoffman73) studied the sources of Weyl-type electrovac fields. They obtained the parameters for the source with the junction condition for the exterior solution. [Efinger 64](#Efinger64) deduced the stability of a charged particle from the self-energy of the gravitation field. In [Burghardt 09](#Burghardt09) is constructed another interior solution with the help of embedding the geometry in a 5-dimensional flat space.

(Literature summary taken from [Burghardt 09](#Burghardt09))

See also ([Mehra 82](#Mehra82), [WX 87](#WX87), [Gupta-Kumar-Pratibha 12](#GuptaKumarPratibha12)).


## Related concepts

* [[no-hair theorem]]

[[!include charged and rotating black holes -- table]]

## References

Review includes

* Mammadov, _Reissner-Nordstr&#246;m metric_ ([pdf](http://gmammado.mysite.syr.edu/notes/RN_Metric.pdf))
 
* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Reissner%E2%80%93Nordstr%C3%B6m_metric">Reissner-Nordstr&#246;m metric</a>_

That the [[near horizon geometry]] of the [[extremal black hole|extremal]] Reissner-Nordström black hole in 4d ins 2d [[anti de Sitter spacetime]] times the [[2-sphere]], $AdS_2 \times S^2$, was observed in 

* [[Gary Gibbons]], in F. del Aguila, [[J. de Azcarraga]], [[Luis Ibanez]] (eds.) _Supersymmetry, Supergravity and Related Topics_


   (see section 11.1 here: [pdf](http://www.hartmanhep.net/topics2015/11-nearhorizon.pdf) [[ExtremalReissnerNordstrom.pdf:file]])

Discussion of interior solutions includes

* {#GravesBrill60} Graves J. C., Brill D. R., _Oscillatory character of Reissner-Nordstr&#246;m metric for an ideal charged wormehole._ Phys. Rev. 120, 1507, 1960

* {#Efinger64} Efinger H. J., _Der kugelsymmetrische Fall einer statischen Ladungsverteilung bei stark komprimierter Materie in der allgemeinen Relativit&#228;tstheorie. Acta Phys. Austr. 17, 347, 1964.

  _&#220;ber die Selbstenergie und Ladung eines durch Gravitationswirkung stabilisierten Teilchens in einem gekr&#252;mmten Raum_, Acta Phys. Austr. 188, 31, 1965

* {#KyleMartin67} Kyle C. F., Martin A. W., _Self-energy considerations in general relativity and the exact fields of charge and mass distribution_, Nuov. Cim 50, 883, 1967


* {#CohenCohen69} Cohen J. M., Cohen M. D., _Exact fields of charge and mass distributions in general relativity_. Nuov. Cim. 60, 241, 1969

* {#Wilson69} Wilson, S. J., _Exact solution of a static charged sphere in general relativity_. Can. Journ. Phys. 47, 2401, 1969


* {#Bekenstein71} [[Jacob Bekenstein]], _Hydrostatic equilibrium and gravitational collapse of relativistic charged fluid balls_, Phys. Rev. D 4, 2185, 1971

* {#HE73} S. W. Hawking, G. F. R. Ellis, Section 5.5 of: _The Large Scale Structure of Space-Time_, Cambridge University Press (1973) ([doi:10.1017/CBO9780511524646](https://doi.org/10.1017/CBO9780511524646))



* {#Boulware73} Boulware, D. G., _Naked singularities, thin shells, and the Reissner-Nordstr&#246;m metric_, Phys. Rev. D 8, 2363, 1973


* {#GautreauHoffman73} Gautreau R., Hoffman R. B., The structure of Weyl-type electrovac fields in general relativity. Nouv. Cim. 16 B, 162, 1973

* {#KroriJayantimala75} Krori K. D., Jayantimala B., _A singularity-free solution for a charged fluid in general relativity_, J. Phys. A 8, 508, 1975

* {#Mehra82} A.L. Mehra, _An interior solution for a charged sphere in general relativity_,  Physics Letters A Volume 88, Issue 4, 8 March 1982, Pages 159-161 ([publisher](http://www.sciencedirect.com/science/article/pii/0375960182905515))

* {#TiwariRaoKanakamelda85} Tiwari R. N., Rao J. R., Kanakamedala R. R., _Electromagnetic mass models in general relativity_, Phys. Rev. D 30, 489, 1984

* {#WX87} Wang Xingxiang, _Exact Solution of a Static Charged Sphere in
General Relativity_, General Relativity and Gravitation, Vol. 19, No. 7, 1987

* {#Burghardt09} Rainer Burghardt, _Reissner exterior and interior_ [arXiv:0902.0918](https://arxiv.org/abs/0902.0918)

* {#GuptaKumarPratibha12} Gupta, Y. K.; Kumar, Jitendra; Pratibha, _A Class of Well Behaved Charged Analogues of Schwarzchild's Interior Solution_, International Journal of Theoretical Physics October 2012, Volume 51, Issue 10, pp 3290&#8211;3302 ([publisher](http://link.springer.com/article/10.1007%2Fs10773-012-1209-4))



[[!redirects Reissner-Nordström spacetimes]]

[[!redirects Reissner-Nordstrom spacetime]]
[[!redirects Reissner-Nordstrom spacetimes]]

[[!redirects Reissner-Nordström black hole]]
[[!redirects Reissner-Nordström black holes]]

[[!redirects Reissner-Nordstrom black hole]]
[[!redirects Reissner-Nordstrom black holes]]


[[!redirects charged black hole]]
[[!redirects charged black holes]]

