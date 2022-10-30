
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

More in detail, the _Adams-Novikov spectral sequence_ is a class of [[spectral sequences]] which converge to and hence are used to compute [[homotopy groups]] of [[connective spectra]],  hence in particular the [[stable homotopy groups of spheres]]. It refines the _[[Adams spectral sequence]]_ by replacing [[ordinary cohomology]] with [[coefficients]] in [[Fp]] by [[complex cobordism cohomology theory]], i.e. with coefficients in [[MU]].

More generally for $E$ any suitable [[E-infinity ring]] there is an Adams-Novikov-type spectral sequence involving $E$-[[generalized cohomology]]/[[generalized homology]]. This fully general notion is often again just referred to as the _$E$-[[Adams spectral sequence]]_. Accordingly, see there for more.

## Properties

### Adams Chart
 {#AdamsChart}

[Isaksen 14](#Isaksen14):

<img src="http://ncatlab.org/nlab/files/IsaksenANSSE2p.jpg" />

<img src="http://ncatlab.org/nlab/files/IsaksenANSSEinfinityp.jpg" />


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


Reviews include

* {#Ravenel} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, page 11 0f chapter I _An introduction to the homotopy groups of spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel1.pdf))


* [[Doug Ravenel]], _[Complex cobordism and stable homotopy groups of spheres](http://www.math.rochester.edu/people/faculty/doug/mu.html)_, chapter IV _$B P$-Theory and the Adams-Novikov Spectral Sequence_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel4.pdf))

* [[Jacob Lurie]], _Localizations and the Adams-Novikov Spectral Sequence_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture30.pdf))

The Adams chart of the ANSS for large order has been presented in 

* {#Isaksen14} [[Daniel Isaksen]], _Classical and motivic Adams-Novikov charts_ ([arXiv:1408.0248](http://arxiv.org/abs/1408.0248))


[[!redirects Adams-Novikov spectral sequence]]

[[!redirects Adams-Novikov spectral sequences]]