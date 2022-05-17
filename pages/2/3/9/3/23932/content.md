
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Ingredients

\begin{definition}\label{StableSmoothFunction}
A [[smooth map]] $f \,\colon\, X \to Y$ between [[smooth manifolds]]  is called *stable* if every nearby smooth function, hence every function in some [[open neighbourhood]] of $f$ inside the [[mapping space]] $C^\infty(X,Y) \subset C^0(X,Y)$, is equal to $f$ up to [[conjugation]] with a [[pair]] of [[diffeomorphisms]].
\end{definition}

Similarly, $f$ is *infinitesimally stable* if this statement holds to first order in [[derivatives]], in  a suitable sense.


(due to [Mather 68](#Mather68), see [Ruas 22, Def. 2.2, Def. 3.3](#Ruas22)).



## Statement

\begin{proposition}
A [[proper map|proper]] [[smooth map]] between [[smooth manifolds]] is "stable" (Def. \ref{StableSmoothFunction}) if and only if it is infinitesimally stable.
\end{proposition}

([Mather 70, Thm. 4.1](#Mather70), [Ruas 22, Thm. 3.11](#Ruas22))

## Related statements

* [[inverse function theorem]]

## References

The original articles:

* {#Mather68} [[John N. Mather]], _Stability of $C^\infty$ mappings: I.  The division theorem_,  Annals of Mathematics **87** 1 (1968) 89  $[$[doi:10.2307/1970595](http://dx.doi.org/10.2307/1970595)$]$

* {#Mather69} [[John N. Mather]], _Stability of $C^\infty$ Mappings: II. Infinitesimal Stability Implies Stability_, Annals of Mathematics **89** 2 (1969) 254  $[$[doi:10.2307/1970668](http://dx.doi.org/10.2307/1970668)$]$

* {#Mather70} [[John N. Mather]], *Stability of $C^\infty$ mappings: V. Transversality*, Advances in Mathematics **4** 3 (1970) 301-336 (<a href="https://doi.org/10.1016/0001-8708(70)90028-9">doi:10.1016/0001-8708(70)90028-9</a>)

Review:

* {#Ruas22} Maria Aparecida Soares Ruas, *Old and new results on density of stable mappings* $[$[arXiv:2201.03888](https://arxiv.org/abs/2201.03888)$]$

A proof in [[synthetic differential topology]] is provided in section 7.3 of 

* [[Marta Bunge]], Felipe Gago, Ana Maria San Luis Fernández, _Synthetic Differential Topology_, 2018, ([CUP](http://www.cambridge.org/gb/academic/subjects/mathematics/logic-categories-and-sets/synthetic-differential-topology)) ([excerpt](http://assets.cambridge.org/97811084/47232/excerpt/9781108447232_excerpt.pdf))

following

* Ana Maria San Luis Fernández, _Estabilidad transversal de gérmenes representables infinitesimalmente,_ Ph.D. Thesis, Universidad de Santiago de Compostela, 1999. ([abstract page](https://documat.unirioja.es/servlet/tesis?codigo=12609))


[[!redirects Mather stability theorem]]
