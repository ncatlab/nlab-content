
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

The _Milnor-Quillen theorem on $MU$_ determines the structure of the [[graded ring]] $\pi_{\bullet}(MU)$ of [[stable homotopy groups]] of the universal complex [[Thom spectrum]] [[MU]].

In ([Milnor 60](#Milnor60)) it was shown this is the [[polynomial ring]] $\mathbb{Z}[y_1, y_2, \cdots]$ on generators $y_{n+1}$ in degree $2(n+1)$ for all $n \in \mathbb{N}$. 

Notice that by [[Thom's theorem]], this is also isomorphic to the [[cobordism ring]] $\Omega_\bullet^U \simeq \pi_\bullet(M U)$ of [[smooth manifolds]] equipped with stable [[almost complex structure]].

Moreover, by [[Lazard's theorem]], this graded ring is also abstractly [[isomorphism|isomorphic]] to the [[Lazard ring]] $L$.

But the [[universal complex orientation on MU]] induces a preferred ring [[homomorphism]]

$$
  L \longrightarrow \pi_\bullet(M U) \simeq \Omega_\bullet^U \simeq \mathbb{Z}[y_1, y_2, \cdots]
  \,.
$$

A priori it is not clear whether this particular canonical homomorphism exhibits the [[isomorphism]]. But it does, this is the result of ([Quillen 69](#Quillen69)).

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

This is due to ([Quillen 69](#Quillen69)), based on ([Milnor 60](#Milnor60)), reproduced e.g. as ([Kochman 96, theorem 3.7.7, theorem 4.4.13](#Kochman96)).

**Proof strategy:** (for Milnor's part) 

Apply the [[Boardman homomorphism]] to get the statement over the [[rational numbers]]. Deduce that $\pi_\bullet(MU)$ is finitely generated so that it is now sufficient to prove it over the [[p-adic integers]] for all $p$. 

Now use the $H\mathbb{F}_p$-[[Adams spectral sequence]], which, on its second page, expresses these homotopy groups by the $H\mathbb{F}_p$-[[homology of MU]].

The [[homology of MU]] may be computed by reducing, via the [[Thom isomorphism]], to computation of the homology of the [[classifying space]] [[BU|$B U$]], which in turn is given by [[Kronecker pairing]] from the [[Conner-Floyd Chern classes]]. 

Using this and applying the [[change of rings theorem]], the [[Adams spectral sequence]] is seen to collapse right away, and so the result may now be obtained by explicitly computing the relevant comodule [[Ext]]-groups of the [[homology of MU]]

+-- {: .num_remark}
###### Remark

The dual generalized [[Steenrod algebra]] $MU_\bullet(MU)$ has a structure of 
[[commutative Hopf algebroid]] over the [[Lazard ring]]. This is the content of the [[Landweber-Novikov theorem]].

=--


## Related theorems

* [[Lazard's theorem]]

* [[Landweber exact functor theorem]]

* [[Landweber-Novikov theorem]]

## References

The computation of $\pi_\bullet(M U)$ was first due to

* {#Milnor60} [[John Milnor]], _On the Cobordism Ring ft* and a Complex Analogue_, Amer. J.  Math., 82 (1960), 505-521. 

the proof that the canonical morphism $L \to \pi_\bullet(M U)$ is an isomorphism is due to

* {#Quillen69} [[Daniel Quillen]], _On the formal group laws of unoriented and complex cobordism theory_, Bull. Amer. Math. Soc. 75 (1969), 1293&#8211;1298. ([Euclid](http://projecteuclid.org/euclid.bams/1183530915))
 
According to 

* {#Hopkins99} [[Mike Hopkins]], section 4 of _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

the best reference as of turn of the millennium was still

* {#Adams74} [[Frank Adams]], part II, section 6-8 of _[[Stable homotopy and generalised homology]]_, Chicago lectures in mathematics, 1974

But see

* {#Kochman96} [[Stanley Kochman]], section 4.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, 
   
  Lecture 7 _The homology of MU_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture7.pdf)) 
 
  Lecture 9 _The Adams spectral sequence for MU_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture9.pdf))

  Lecture 10 _The proof of Quillen's theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture10.pdf)) 


Other review includes

* {#Kochman96} [[Stanley Kochman]], theorem 3.7.7 (Milnor's theorem) of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, chapter 4 _$B P$-Theory and the Adams-Novikov spectral sequence_, [pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel4.pdf)

also

* [[Charmaine Sia]], section 2 of _Calculating the $E_2$-term of the Adams spectral sequence_ ([pdf](http://www.math.harvard.edu/~sia/notes/classical_topology_adams.pdf))

* [[Sam Nolen]], sections 1 and 2 of _The Adams-Novikov spectral sequence_ ([pdf](http://samnolen.com/Adams%20Novikov.pdf))

* [[Akhil Mathew]], _[Quillen's theorem on the formal group law of MU](https://amathew.wordpress.com/2012/05/28/quillens-theorem-on-the-formal-group-law-of-mu/#more-3345)_


[[!redirects Milnor's theorem on MU]]

[[!redirects Quillen's theorem on MU]]
[[!redirects Milnor-Quillen's theorem on MU]]

[[!redirects Quillen's theorem about MU]]


