
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 


## Idea

The _&#233;tale site_ of a [[scheme]] is an analog of the [[category of open subsets]] of a [[topological space]]. The corresponding [[cohomology]] is [[étale cohomology]].

The &#233;tale topology has similar cohomological properties to complex [[analytic topology]], and in particular it is much finer for cohomological purposes than the [[Zariski topology]]. 


## Definition

+-- {: .un_defn}
###### Definition

Let $X$ be a [[scheme]]. 

The **[[big site|big]] &#233;tale [[site]]** $Sch{/X,et}$ of $X$ is the [[over category]] $Sch_{/X}$ of [[scheme]]s over $X$ equipped with the [[coverage]] given by [[étale cover]]s (after forgetting the maps to $X$).

The **[[small site|small]] &#233;tale [[site]]** $i : X_{et} \hookrightarrow Sch/{X,et}$ is the full [[subcategory]] of $Sch_{/X}$on the [[étale morphism]]s $U \to X$.


=--

The [[abelian sheaf cohomology]] of the &#233;tale site is called [[étale cohomology]]. 

## Properties




+-- {: .un_prop}
###### Proposition

The [[inverse image]] restriction functor $i^* Sh(Sch_{/X,et}, Ab) \to Sh(X_{et}, Ab)$ on the [[categories of sheaves]] with values in [[Ab]]

* is an [[exact functor]] 

* maps [[injective object]]s to injective objects.

=--

+-- {: .un_cor}
###### Corollary

For $X$ a [[scheme]] and $F \in Sh(Sch_{/{X,et}, Ab)$ we have that the [[etale cohomology]] of $X$ with coefficients in $F$ may be computed on the small site:

$$
  H^p(X_{et}, F|_{et}) \simeq H^p(X,F)
  \,.
$$

=--

This appears for instance in ([deJong, prop. 3.4](#deJong)).

## References

The classical references are

* [[Pierre Deligne]] et al., _Cohomologie &#233;tale_ , Lecture Notes in Mathematics, no. 569, Springer-Verlag, 1977.
{#Deligne}

* [[James Milne]], _Etale cohomology_, Princeton Mathematical Series __33__, 1980. xiii+323 pp.

Lecture notes are

* [[James Milne]], _Lectures on etale cohomology_ ([pdf](http://www.jmilne.org/math/CourseNotes/LEC.pdf))

* [[Aise Johan de Jong]], _&#201;tale cohomology_ ([pdf](http://math.columbia.edu/~pugin/Teaching/Etale_files/EtaleCohomology.pdf))
{#deJong}



[[!redirects étale site]]

[[!redirects etale sites]]
[[!redirects étale sites]]


[[!redirects étale topology]]
[[!redirects etale topology]]

[[!redirects étale topologies]]
[[!redirects etale topologies]]

