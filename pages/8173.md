
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Adams-Novikov spectral sequence_ is the $E$-[[Adams spectral sequence]], for $E = $ [[MU]].

More in detail, the _Adams-Novikov spectral sequence_ is a class of [[spectral sequences]], which refine the _[[classical Adams spectral sequence]]_ by replacing [[ordinary cohomology]] with [[coefficients]] in [[Fp]] by [[complex cobordism cohomology theory]] [[MU]]. This makes the Adams-Novikov spectral sequence converge to the full [[homotopy groups]] of [[connective spectra]], hence in particular to the full [[stable homotopy groups of spheres]] ([Novikov 67, Theorems 3.1, 3.3](#Novikov67), reviewed as [Ravenel 78, Thm. 3.1](#Ravenel78)).

More generally for $E$ any suitable [[E-infinity ring]] there is an Adams-Novikov-type spectral sequence involving $E$-[[generalized cohomology]]/[[generalized homology]]. This fully general notion is often again just referred to as the _$E$-[[Adams spectral sequence]]_. Accordingly, see there for more. For detailed introduction, see at _[[Introduction to the Adams Spectral Sequence]]_.

## Properties

### Adams Chart
 {#AdamsChart}

[Isaksen 14](#Isaksen14):

\begin{imagefromfile}
  "file_name": "IsaksenANSSE2p.jpg"
\end{imagefromfile}

\begin{imagefromfile}
  "file_name": "IsaksenANSSEinfinityp.jpg"
\end{imagefromfile}


### Relation to Brown-Peterson spectrum

The $p$-component of the $E^2$-term of the Adams-Novikov spectral sequence for the [[sphere spectrum]], hence the one converging to the 
[[stable homotopy groups of spheres]] $\pi_\ast(\mathbb{S})$ is

$$
  Ext_{BP_\ast(BP)}(BP_\ast, BP_\ast)
  \,,
$$

where $BP$ denotes the [[Brown-Peterson spectrum]] at prime $p$.

recalled e.g. as [Ravenel, theorem 1.4.2](#Ravenel)



## Related concepts

* [[stable homotopy groups of spheres]]

* [[chromatic spectral sequence]]

* [[EHP spectral sequence]]

## References

The generalization of the [[Adams spectral sequence]] from $E = $ [[HA]] to $E = $ [[MU]] is due to 

* {#Novikov67} [[Sergei Novikov]], _The methods of algebraic topology from the viewpoint of cobordism theories_, Izv. Akad. Nauk. SSSR. Ser. Mat. 31 (1967), 855&#8211;951 (Russian) ([[Novikov67.pdf:file]])

While that article was still being translated to English, [[Frank Adams]] learned of and then lectured about this work in 1967 in Chicago. This lecture together with two later lectures in 1970 and in 1971 constitute the book

* {#Adams74} [[Frank Adams]],  _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

Further early development of this Adams-Novikov spectral sequence:

* {#Zahler72} [[Raphael Zahler]], _The Adams-Novikov Spectral Sequence for the Spheres_, Annals of Mathematics Second Series, Vol. 96, No. 3 (Nov., 1972), pp. 480-504 ([doi:10.2307/1970821](https://doi.org/10.2307/1970821))

Review:

* {#Ravenel78} [[Douglas Ravenel]], _A Novice's guide to the Adams-Novikov spectral sequence_, in: [[Michael Barratt]], [[Mark Mahowald]] (eds.) _Geometric Applications of Homotopy Theory II_. Lecture Notes in Mathematics, vol 658, Springer 1978 ([doi:10.1007/BFb0068728](https://doi.org/10.1007/BFb0068728), [pdf](https://people.math.rochester.edu/faculty/doug/mypapers/Novice.pdf))


* {#Ravenel} [[Douglas Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, page 11 of chapter I _An introduction to the homotopy groups of spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel1.pdf))


* [[Doug Ravenel]], _[Complex cobordism and stable homotopy groups of spheres](http://www.math.rochester.edu/people/faculty/doug/mu.html)_, chapter IV _$B P$-Theory and the Adams-Novikov Spectral Sequence_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel4.pdf))

* {#Kochman96} [[Stanley Kochman]], sections 4.7 and 5.6 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


* [[Jacob Lurie]], _Localizations and the Adams-Novikov Spectral Sequence_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture30.pdf))

The Adams chart of the ANSS for large order has been presented in 

* {#Isaksen14} [[Daniel Isaksen]], _Classical and motivic Adams-Novikov charts_ ([arXiv:1408.0248](http://arxiv.org/abs/1408.0248))


[[!redirects Adams-Novikov spectral sequence]]

[[!redirects Adams-Novikov spectral sequences]]