
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


## Definition

+-- {: .un_defn}
###### Definition

Let $X$ be a [[scheme]]. 

The **[[big site|big]] &#233;tale [[site]]** $Sch/{S,et}$ of $X$ is the [[over category]] $Sch/S$ equipped with the [[coverage]] given by [[étale cover]]s.

The **[[small site|small]] &#233;tale [[site]]** $i : X_{et} \hookrightarrow Sch/{S,et}$ is the full [[subcategory]] on the open inclusions (...) $U \to X$.


=--

The [[abelian sheaf cohomology]] of the &#233;tale site is called [[étale cohomology]]. 

## Properties

The &#233;tale topology has similar cohomological properties to complex [[analytic topology]], and in particular it is much finer for [[cohomology|cohomological]] purposes than the [[Zariski topology]]. 



+-- {: .un_prop}
###### Proposition


The [[inverse image]] restriction functor $i^* Sh(Sch/{S,et}, Ab) \to Sh(S_{et}, Ab)$ on the [[categories of sheaves]] with values in [[Ab]]

* is an [[exact functor]] 

* maps [[injective object]]s to injective objects.

=--

+-- {: .un_cor}
###### Corollary

For $X$ a [[scheme]] and $F \in Sh(Sch/_{S,et}, Ab)$ we have that the [[etale cohomology]] of $X$ with coefficients in $F$ may be computed on the small site:

$$
  H^p(S_{et}, F|_{et}) \simeq H^p(S,F)
  \,.
$$

=--

This appears for instance in ([deJong, prop. 3.4](#deJong)).

## References


Section 3 in


* [[Aise Johan de Jong]], _&#201;tale cohomology_ ([pdf](http://math.columbia.edu/~pugin/Teaching/Etale_files/EtaleCohomology.pdf))
{#deJong}


[[!redirects étale site]]

[[!redirects etale sites]]
[[!redirects étale sites]]
