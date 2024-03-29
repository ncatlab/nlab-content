[[!redirects fppf-site]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Fix some [[scheme]] $S$.

+-- {: .un_defn}
###### Definition

the **fppf-site** (over $S$) is the [[site]] 

* whose underlying category is the category $Aff/S$ of [[affine scheme]]s [[over category|over]] $S$;

* whose [[coverage]] has as [[covering]] families $\{f : U_i \to X\}$
  those families of morphisms that are  such that 

  * each $f_i$ is a [[flat morphism]];

  * each $f_i$ is [[locally of finite presentation]];

  * we have that $X = \cup_i f_i(U_i)$.
  
=--

This appears as ([de Jong, def. 27.7.1, def 27.7.6, lemma 27.7.11](#deJong)).


+-- {: .un_remark}
###### Remark


The abbreviation "fppf" is for _fid&#232;lement plat de pr&#233;sentation finie_ : faithfully flat and of finite presentation. 

But notice that it is common practice, as in the above definition, to require only _local_ finite presentability.

=--

## Related concepts

[[fpqc-site]] $\to$ **fppf-site** $\to$ [[syntomic site]] $\to$ [[étale site]] $\to$ [[Nisnevich site]] $\to$ [[Zariski site]]


## References

Chaper 27.7 in 

* [[Aise Johan de Jong]], _[[The Stacks Project]]_
{#deJong}


[[!redirects fppf topology]]
[[!redirects fppf-topology]]