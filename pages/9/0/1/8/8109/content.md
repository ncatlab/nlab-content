
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


By the construction of [[complex oriented cohomology theories]] from [[formal groups]] (via the [[Landweber exact functor theorem]]), the [[height of a formal group|height filtration]] of formal groups induces a "[[chromatic filtration|chromatic]]" [[filtration]] on [[complex oriented cohomology theories]]. 
_Chromatic homotopy theory_ is the study of [[stable homotopy theory]] and specifically of [[complex oriented cohomology theories]] by means of and along this [[chromatic filtration]].

More in detail, for each [[prime]] $p \in \mathbb{N}$ and for each  $n \in \mathbb{N}$ there is a [[Bousfield localization of spectra]]

$$
  L_n \coloneqq L_{K(0)\vee \cdots \vee K(n)}
  \,,
$$

where $K(n)$ is the $n$th [[Morava K-theory]] (for the given [[prime]] $p$). These arrange into the [[chromatic tower]] which for each spectrum $X$ is of the form

$$  
  X \to \cdots \to L_n X \to L_{n-1} X \to \cdots \to L_0 X
  \,.
$$

The [[chromatic convergence theorem]] states mild conditions under which the [[homotopy limit]] over this tower is the $p$-[[Bousfield localization of spectra|localization]] 

$$
  X \to X_{(p)}
$$

of $X$. 

Since moreover $L_n X$ is the [[homotopy fiber product]]

$$
  L_n X \simeq L_{K(n)}X \underset{L_{n-1}L_{K(n)}X}{\times} L_{n-1}X
$$

it follows that in principle one can study a spectrum $X$ by understanding all its "chromatic pieces" $L_{K(n)} X$. 


## Examples

[[!include chromatic tower examples - table]]

## Related concepts

* [[stable homotopy theory]]

* [[complex oriented cohomology theory]]

* [[complex cobordism cohomology theory]]

  * [[Lazard's theorem]]

  * [[Quillen's theorem on MU]]

  * [[Landweber exact functor theorem]]

* [[formal group law]]

  * [[moduli stack of formal groups]]

  * [[height of a formal group]]

  * [[Morava stabilizer group]]

* [[Morava K-theory]]

  * [[∞-field]]

  * [[integral Morava K-theory]]

* [[Morava E-theory]]

  * [[Lubin-Tate theory]]

* [[chromatic filtration]]

  * [[chromatic tower]]

  * [[monochromatic layer]]

  * [[periodicity theorem]]

  * [[chromatic convergence theorem]]

* [[telescopic complexity]], [[telescopic localization]]

* [[red-shift conjecture]]

* [[J-homomorphism]]

* [[motivic chromatic homotopy theory]]


## References 
 {#References}

Comprehensive lecture notes are in

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010 ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html))
 {#LurieLectures}

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_

Brief surveys include

* [[Haynes Miller]], _"Chromatic" homotopy theory_ May 2011 ([pdf](http://www-math.mit.edu/~hrm/papers/chromatic.pdf))

A lightning review of results by Henn with Goerss, Mahowald, Rezk, and Karamanov is in 

* Hans-Werner Henn, _Recent developments in stable homotopy theory_ ([pdf](http://math.berkeley.edu/~aaron/saft/henn.pdf))


Random useful discussion is in 

* _[Chromotopy](http://chromotopy.org/)_

Discussion of generalization [[elliptic cohomology]] to higher chromatic homotopy theory is discussed in

* [[Doug Ravenel]], _Toward higher chromatic analogs of elliptic cohomology_ [pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/high1.pdf)

* [[Doug Ravenel]], _Toward higher chromatic analogs of elliptic cohomology II_, Homology, Homotopy and Applications, vol. 10(1), 2008, pp.1-36 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/high2.pdf), [pdf slides](http://www.math.rochester.edu/people/faculty/doug/mypapers/halifax.pdf))


[[!redirects chromatic level]]
[[!redirects chromatic filtration]]
[[!redirects chromatic levels]]