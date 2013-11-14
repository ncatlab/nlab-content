
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

Every [[complex oriented cohomology theory]] induces a [[formal group]]. The _Landweber exact functor theorem_ says that, conversely, forming the [[tensor product]] of [[complex cobordism cohomology theory]] ([[MU]]) with a [[Landweber exactness|Landweber exact]] [[ring]] via some [[formal group law]] yields a [[cohomology theory]].

By the [[Brown representability theorem]] this defines a [[spectrum]] and the spectra arising this way are called _Landweber exact spectra_. ([e.g. Lurie lect 17, p.2](#Lurie17)).

## Statement

By evaluation on $X = B U(1)$, every [[multiplicative cohomology theory|multiplicative]] [[complex oriented cohomology theory]] $E$ gives rise to a [[formal group]] over the [[graded ring]] $\pi_\bullet(E)$.

Conversely, given a formal group $F$ over a [[graded ring]] $R$, one can ask whether this arises from some $E$ in this way. 

Now since the [[Lazard ring]] $L$ classifies formal groups in that $F$ is equivalently given by a [[ring]] [[homomorphism]] $L \longrightarrow R$ and since moreover $L$ is the [[cohomology ring]] of [[complex oriented cohomology theory]] $L \simeq MU_\bullet(\ast)$, one can consider the functor

$$
  X \mapsto E_\bullet(X) \coloneqq MU_\bullet(X) \underset{L}{\otimes} R
  \,.
$$

By construction this is such that $E_\bullet(\ast) \simeq R$. But this functor may fail to satisfy the axioms of a [[generalized homology theory]], hence may fail to be [[Brown representability theorem|Brown represented]] by an actual [[spectrum]] $E$.

Landwever exactness is a sufficient condition on $R$ for $MU_\bullet(-)\otimes_L R$ to be indeed a generalized homology theory

(...)

([Lurie, lect 15, theorem 9](#LurieLecture15))

(...)

## Properties of Landweber-exact spectra

### Phantom maps

Between Landweber exact spectra, every [[phantom map]] is already null-homotopic. (e.g. [Lurie lect 17, corollary 7](#Lurie)).

## Related theorems

* [[Lazard's theorem]]

* [[Landweber exact functor theorem]]

* [[Quillen's theorem on MU]]

* [[Landweber-Novikov theorem]]

## References

* Wikipedia, _[Landweber exact functor theorem](http://en.wikipedia.org/wiki/Landweber_exact_functor_theorem)_


* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, 
Lecture 15 _Flat modules over $\mathcal{M}_{FG}$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture15.pdf))
 {#LurieLecture15}

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 16 _The Landweber exact functor theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture16.pdf)) 

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 17 _Phantom maps_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture17.pdf)) 
 {#Lurie17}


[[!redirects Landweber exact spectrum]]
[[!redirects Landweber exact spectra]]

[[!redirects Landweber-exact spectrum]]
[[!redirects Landweber-exact spectra]]

