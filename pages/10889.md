
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called _effective homology_ is the study of (effective) [[algorithms]] for computing invariants in [[algebraic topology]], such as [[homology groups]] but also [[homotopy groups]].

From the first part of "Effective homology, a survey", we can see why effective homology is useful.

It's much better to consider only the simply-connected spaces. We have two methods

1. Sullivan method for rational homotopy (based on minimal model
   theory) [fn:1]
2. Edgar Brown method for integer homotopy. [fn:2]

Sullivan's method is more restrictive (to Q) but much more
efficient than Brown's method. Brown's method is not practical at
all, even with the most powerful computer at hand. Nevertheless,
even Sullivan's method is at least #P-hard.

That's how effective method kicks in. It adapts Hirsch's
method [fn:3]. Using functional programming, this becomes a real
computing tool for homology and homotopy groups.




## Related concepts

* [[persistent homology]]

## References

* [[Francis Sergeraert]], _Effective homology, a survey_ ([pdf](http://www-fourier.ujf-grenoble.fr/~%20sergerar/Papers/Survey.pdf))

* [fn:1] [20] Dennis Sullivan. Infinitesimal calculations in
topology.

* [fn:2] [3] Edgar H. Brown Jr.. Finite computability of Postnikov
complexes. Annals of Mathematics, 1957, vol. 65, pp 1-20.

* [fn:3] [11] G. Hirsch. Sur les groupes d’homologie des espaces
fibr´es.

[[!redirects effective homology theory]]