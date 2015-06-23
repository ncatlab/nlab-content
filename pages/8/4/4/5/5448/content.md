[[!redirects fpqc-site]]

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

The **fpqc-site** (over $S$) is the [[site]] 

* whose underlying category is the category $Aff/S$ of [[affine scheme]]s [[over category|over]] $S$;

* whose [[coverage]] has as [[covering]] families $\{f : U_i \to X\}$
  those families of morphisms that are  such that 

  * each $f_i$ is a [[flat morphism]];

  * for every affine open $W \hookrightarrow X$ there exists $n \geq  0$, a [[function]] $a : \{1, \cdots, n\} \to I$ and affine opens
    $V_j \hookrightarrow T_{a(j)}$ with

    $$
      \cup_{j = 1}^{n} f_{a(j)}(V_j) = W
      \,.
    $$
  
=--

This appears as ([Stacks Project, def. 27.8.1](#Stacks)). ([[David Roberts|DR]]: this reference is now incorrect! It should be tag number, but I can't find it)

+-- {: .un_remark}
###### Remark

The last condition does imply that $\cup_i f_i(U_i) = X$.

=--

+-- {: .un_remark}
###### Remark


The abbreviation "fpqc" is for _fid&#232;lement plat quasi-compacte_ : faithfully flat and quasi-compact.

=--

+-- {: .un_remark}
###### Remark


Because the collection of fpqc covers of a scheme does not have a small collection of refinements (Stacks project, [Tag 0BBK](http://stacks.math.columbia.edu/tag/0BBK)), working with the fpqc topology can be set-theoretically tricky.  Indeed, in 1975, Waterhouse gave an example of a functor on schemes that admits no fpqc sheafification.  This contradicts many claims in the literature that fpqc sheafification and stackification is functorial (and such claims continue to be made).

=--

## Related concepts

**fpqc-site** $\to$ [[fppf-site]] $\to$ [[syntomic site]] $\to$ [[étale site]] $\to$ [[Nisnevich site]] $\to$ [[Zariski site]]


## References

Chaper 27.8 in 

* _[[The Stacks Project]]_
{#Stacks}

* W. C. Waterhouse, _Basically bounded functors and flat sheaves_, Pacific Journal of Mathematics __57__ (1975), no. 2, 597--610 [MR396578](http://www.ams.org/mathscinet-getitem?mr=396578), [euclid](http://projecteuclid.org/euclid.pjm/1102906018)

[[!redirects fpqc-site]]
[[!redirects fpqc topology]]
[[!redirects fpqc-topology]]