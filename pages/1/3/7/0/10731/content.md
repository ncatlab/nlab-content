
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


## Statement

Write $MU$ for the [[E-∞ ring]] [[spectrum]] of [[complex cobordism cohomology theory]]. Since this is a [[complex oriented cohomology theory]], by [[Lazard's theorem]] there is associated a commutative 1-dimensional [[formal group law]] classified by a [[ring]] homomorphism of the form

$$
  L \longrightarrow \pi_\bullet(MU)
$$

from the [[Lazard ring]] $L$.

+-- {: .num_theorem}
###### Theorem

This canonical homomorphism is an [[isomorphism]] 

$$
  L \stackrel{\simeq}{\longrightarrow} \pi_\bullet(MU)
  \,.
$$

=--

This is due to ([Quillen 69](#Quillen69)), based on ([Milnor 60](#Milnor60)), reproduced e.g. as ([Kochmann 96, theorem 4.4.13](#Kochmann96)).

**Proof strategy:** (for Milnor's part) Compute the [[homology of MU]] and apply the [[Boardman homomorphism]] to get the statement over the [[rational numbers]]. Deduce that $\pi_\bullet(MU)$ is finitely generated so that it is now sufficient to prove it over the [[p-adic integers]] for all $p$. Using the [[change of rings theorem]], this finally follows from inspection of the filtration in the $H\mathbb{F}_p$-[[Adams spectral sequence]] for $MU$.

+-- {: .num_remark}
###### Remark

The dual generalized [[Steenrod algebra]] $MU_\bullet(MU)$ has a structure of 
[[Hopf algebroid over a commutative base]] which is the 
[[Lazard ring]].
This is the content of the [[Landweber-Novikov theorem]].

=--


## Related theorems

* [[Lazard's theorem]]

* [[Landweber exact functor theorem]]

* [[Landweber-Novikov theorem]]

## References

The computation of $\pi_\bullet(M U)$ was first due to

* {#Milnor60} [[John Milnor]] , On the Cobordism Ring ft* and a Complex Analogue, Amer. J.  Math., 82 (1960), 505-521. 

the proof that the canonical morphism $L \to \pi_\bullet(M U)$ is an isomorphism is due to

* {#Quillen69} [[Daniel Quillen]], _On the formal group laws of unoriented and complex cobordism theory_, Bull. Amer. Math. Soc. 75 (1969), 1293&#8211;1298. ([Euclid](http://projecteuclid.org/euclid.bams/1183530915))
 
According to 

* {#Hopkins99} [[Mike Hopkins]], section 4 of _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

the best reference as of turn of the millenium was still

* {#Adams74} [[Frank Adams]], part II, section 6-8 of _[[Stable homotopy and generalised homology]]_, Chicago lectures in mathematics, 1974

But see

* {#Kochmann96} [[Stanley Kochmann]], section 4.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, 
   
  Lecture 7 _The homology of MU_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture7.pdf)) 
 
  Lecture 9 _The Adams spectral sequence for MU_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture9.pdf))

  Lecture 10 _The proof of Quillen's theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture10.pdf)) 


Other review includes

* {#Kochmann96} [[Stanley Kochmann]], theorem 3.7.7 (Milnor's theorem) of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* [[Akhil Mathew]], _[Quillen's theorem on the formal group law of MU](https://amathew.wordpress.com/2012/05/28/quillens-theorem-on-the-formal-group-law-of-mu/#more-3345)_

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, chapter 4 _$B P$-Theory and the Adams-Novikov spectral sequence_, [pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel4.pdf)

[[!redirects Milnor's theorem on MU]]

[[!redirects Quillen's theorem on MU]]
[[!redirects Milnor-Quillen's theorem on MU]]

[[!redirects Quillen's theorem about MU]]


