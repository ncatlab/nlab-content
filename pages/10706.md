
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

Every [[complex oriented cohomology theory]] induces a [[formal group law]] from its first [[Conner-Floyd Chern class]]. Moreover, [[Quillen's theorem on MU]] together with [[Lazard's theorem]] say that the [[cohomology ring]] $\pi_\bullet(M U)$ of [[complex cobordism cohomology]] [[MU]] is the classifying ring for formal group laws. 

The _Landweber exact functor theorem_ ([Landweber 76](#Landweber76)) says that, conversely, forming the [[tensor product]] of [[complex cobordism cohomology theory]] ([[MU]]) with a [[Landweber exactness|Landweber exact]] [[ring]] via some [[formal group law]] yields a [[cohomology theory]].

By the [[Brown representability theorem]] this defines a [[spectrum]] and the spectra arising this way are called _Landweber exact spectra_. ([e.g. Lurie lect 17, p.2](#Lurie17)).

There is an analogue of the statement also for [[even cohomology theory|even]] 2-[[periodic cohomology theories]], with [[MU]] replaced by [[MP]] ([Lurie lecture 18, prop. 11](#LurieLect18)).


## Statement

By evaluation on $X = B U(1)$, the [[classifying space]] for [[complex line bundles]] (the [[circle 2-group]]), every [[multiplicative cohomology theory|multiplicative]] [[complex oriented cohomology theory]] $E$ gives rise to a [[formal group]] over the [[graded ring]] $\pi_\bullet(E)$ (see [there](complex+oriented+cohomology+theory#FormalGroupLaw)).

Conversely, given a formal group $F$ over a [[graded ring]] $R$, one can ask whether this arises from some $E$ in this way. 

Now since the [[Lazard ring]] $L$ classifies formal groups, in that any formal group law $F$ over a [[ground ring]] $R$ is equivalently a [[ring]] [[homomorphism]] $L \longrightarrow R$, and since moreover [[Quillen's theorem on MU]] identifies $L$ with the [[cohomology ring]] of [[complex oriented cohomology theory]] $L \simeq MU_\bullet(\ast)$, one may consider the functor

$$
  X \mapsto E_\bullet(X) \coloneqq MU_\bullet(X) \underset{L}{\otimes} R
  \,.
$$

By construction this is such that $E_\bullet(\ast) \simeq R$. But this functor may fail to satisfy the axioms of a [[generalized homology theory]], hence may fail to be [[Brown representability theorem|Brown represented]] by an actual [[spectrum]] $E$.

Landweber exactness is a sufficient condition on $R$ for $E \coloneqq MU_\bullet(-)\otimes_L R$ to be indeed a [[generalized homology theory]]
(e. g. [Lurie, lect 15, theorem 9](#LurieLecture15)).

Notice that if it is, then the canonical map

$$
  MU_\bullet(X) \otimes_{MU_\bullet} E_\bullet \stackrel{}{\longrightarrow} E_\bullet(X)
$$

is an [[equivalence]]. (For $E = $ [[KU]] this was originally proven in [Conner-Floyd 66](#ConnerFloyd66).) In this form the statement has generalizations beyond [[complex oriented cohomology theory|complex orientation]]. See at _[[cobordism theory determining homology theory]]_.



## Properties of Landweber-exact spectra

### Phantom maps

Between Landweber exact spectra, every [[phantom map]] is already null-homotopic. (e.g. [Lurie lect 17, corollary 7](#Lurie)).

## Examples

* The special case of the Landweber exact functor theorem for [[complex topological K-theory]] [[KU]] is known as the _[[Conner-Floyd isomorphism]]_.


## Related theorems

* [[Lazard's theorem]]

* [[universal complex orientation on MU]]

* [[Quillen's theorem on MU]]

* [[Landweber-Novikov theorem]]

## References

For the special case of $E = $[[KU]] the statement is originally due to

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], _The relation of cobordism to K-theories_, Lecture Notes in Mathematics 28, 1966 [pdf](http://www.maths.ed.ac.uk/~aar/surgery/cf.pdf)

The general result for complex orientation originates in 

* {#Landweber76} [[Peter Landweber]], _Homological properties of comodules over $MU^\ast(MU)$ and $BP^\ast(BP)$_, American Journal of Mathematics (1976): 591-610 ([jstor:2373808](https://www.jstor.org/stable/2373808))


Lecture notes include

* {#LurieLecture15} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 15 _Flat modules over $\mathcal{M}_{FG}$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture15.pdf))
 

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 16 _The Landweber exact functor theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture16.pdf)) 

* {#Lurie17} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 17 _Phantom maps_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture17.pdf)) 
 

See also

* Wikipedia, _[Landweber exact functor theorem](http://en.wikipedia.org/wiki/Landweber_exact_functor_theorem)_

For the even 2-periodic case:


* {#LurieLect18} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010 , Lecture 18 _Even periodic cohomology theories_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture18.pdf))



[[!redirects Landweber exact spectrum]]
[[!redirects Landweber exact spectra]]

[[!redirects Landweber-exact spectrum]]
[[!redirects Landweber-exact spectra]]

