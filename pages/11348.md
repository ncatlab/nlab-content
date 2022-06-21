
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--
 
#Contents#
* table of contents
{:toc}

## Idea

What is called _KO-dimension_ ([Connes 95](#Connes95)) is one notion of [[dimension]] which may be associated with a [[space]] that is given by a [[spectral triple]] with "real structure". 

The definition is motivated by the fact that the [[dimension]] $d$ of an ordinary [[closed manifold]] $X$ is seen in the grading shift involved in the [[Poincaré duality]] that the manifold induces on its [[ordinary homology]]/[[ordinary cohomology]]. Now since in [[spectral geometry]] ("[[noncommutative geometry]]") a [[space]] is represented by a [[spectral triple]] and hence by a kind of [[Dirac operator]] which naturally defines a class not in [[ordinary homology]] but in [[K-homology]], so the idea of KO-dimension is that it is the shift in the grading on [[K-theory]] which is involved in a [[Poincaré duality]] for [[spectral triples]].

Now since [[complex K-theory]] is 2-[[periodic cohomology theory|periodic]] this sees such a dimension only modulo 2, and hence only sees whether the dimension is even or odd. But [[KO-theory]] is 8-periodic and hence sees dimension at least modulo 8.

The exact definition of KO-dimension given in ([Connes 95, def. 3](#Connes95)) moreover requires that the [[Poincaré duality]] is exhibited by a class in [[KR-homology]].


## Examples

For classical [[Riemannian manifolds]] KO-dimension coincides with the traditional concept of [[dimension]] of manifolds, modulo 8.

The [[Podlés spheres]] have KO-dimension 2, but classical dimension 0.

The spectral [[Kaluza-Klein compactification]] considered in the [[Connes-Lott-Chamseddine model]] ([Connes 06](#Connes06)) is taken to be along [[fibers]] with KO-dimension 6 and classical dimension 0 (just as [[perturbative string theory vacuum|perturbative superstring vacua]])


## Related concepts

* [[dimension]]

  * [[cohomological dimension]]

  * [[homotopy dimension]]

  * [[covering dimension]]

  * [[Heyting dimension]]

## References

### General

The original source is def. 3 in 

* {#Connes95} [[Alain Connes]], _Noncommutative geometry and reality_, J. Math. Phys. 36 (11), 1995 ([pdf](https://alainconnes.org/wp-content/uploads/reality.pdf))

### In Connes-Lott models and superstring vacua

With an eye towards [[phenomenology|phenomenological]] considerations of the [[spectral action]] (the [[Connes-Lott-Chamseddine model]]) this is recalled as def. 7.2 in 

* {#Connes06} [[Alain Connes]],  _Noncommutative Geometry and the standard model with neutrino mixing_, JHEP0611:081,2006 ([arXiv:hep-th/0608226](http://arxiv.org/abs/hep-th/0608226))

From p. 8 there:

> {#Connes06OnRelationToStringVacua} When one looks at the table (7.2) of Appendix 7 giving the [[KO-dimension]] of the finite space $[$ i.e. the [[noncommutative geometry|noncommutative]] [[KK-compactification]]-[[fiber]] $F$ $]$ one then finds that its [[KO-dimension]] is now equal to 6 [[modulo]] 8 (!). As a result we see that the [[KO-dimension]] of the [[Cartesian product|product space]] $M \times F$ $[$ i.e. of 4d [[spacetime]] $M$ with the [[noncommutative geometry|noncommutative]] [[KK-compactification]]-[[fiber]] $F$$]$ is in fact equal to $10  \sim 2$ [[modulo]] 8. Of course the above 10 is very reminiscent of string theory, in which the finite space $F$ might bea good candidate for an "[[effective field theory|effective]]" [[KK-compactification|compactification]] at least for low energies. But 10 is also 2 [[modulo]] 8 which might be related to the observations of [Lauscher-Reuter 06](#LauscherReuter06) about [[gravity]].

For more on this see at _[[2-spectral triple]]_.


[[!redirects KO-dimensions]]