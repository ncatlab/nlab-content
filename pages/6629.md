
> under construction -- warning -- currently inconsistent

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition 

+-- {: .num_defn}
###### Definition

A [[cofibrantly generated model category|cofibrantly generated]] [[simplicial model category]] $C$ is **compactly generated** if

* there exists a [[small set]] $S \subset Obj(C)$ of [[object]]s 

* such that

  1. each $K \in S$ is cofibrant;

  1. each $K \in S$ is a homotopy [[compact object]]: for all [[filtered colimit]] diagram $Y : D \to C$ the morphism

     $$
       \mathbb{L}\lim_{\to_i} C(K, Y_i)
       \simeq
       C(K, \mathbb{L}\lim_{\to_i} Y_i)
     $$

     (where $\mathbb{L}\lim_\to$ denotes the $Ho_C$ is the [[homotopy category]] of $C$) is a [[weak homotopy equivalence]] in [[sSet]];

  1. a morphism $X \to Y$ in $C$ is a [[weak equivalence]] precisely if for all $K \in S$ the induced morphism

     $$
       Ho_C(K, X) \to Ho_C(K,Y)
     $$

     is a bijection.

> Something needs to be added/fixed here!!

=--


See ([Jardine11, page 14](#Jardine)), ([Marty, def 1.7](#Marty)).

## Related concepts

* [[compactly generated triangulated category]]

* [[compactly generated (∞,1)-category]]

## References

Page 88 (14) of 

* {#Jardine} [[J. F. Jardine]], _Representability theorems for presheaves of spectra_ J. Pure Appl. Algebra
215 (2011) ([pdf](http://www.math.uwo.ca/~jardine/papers/preprints/rep-2010.pdf))
  

Def. 1.7 of 

* Florian Marty, _Smoothness in relative geometry_ (2009) ([pdf](http://webdoc.sub.gwdg.de/ebook/serien/e/mpi_mathematik/2010/2009_104.pdf))

A different meaning of "compactly generated model category" is used in Definition 5.9 of 

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], *[[Model categories of diagram spectra]]*, Proceedings of the London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [doi:10.1112/S0024611501012692]( https://doi.org/10.1112/S0024611501012692))


[[!redirects compactly generated model categories]]


