
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What may be called *Borel-equivariant rational homotopy theory* (this is not an established term, but it fits well) is the [[rational homotopy theory]] of [[G-spaces]] regarded in [[Borel model structure|Borel equivariant homotopy theory]], hence where [[weak equivalences]] are simply the [[underlying]] ([[forgetful functor|forgetting]] the [[group action]]) [[weak homotopy equivalences]]. This is in contrast to the [[fixed locus]]-wise weak hom. equivalences, as in [[fine model structure on topological G-spaces|proper equivariant homotopy theory]], which leads to [[equivariant rational homotopy theory|proper equivariant rational homotopy theory]].

Borel-equivariant rational homotopy theory is relevant even and particularly to the study of plain (non-equivariant) [[homotopy types]], as it provides the means to conceptualize their [[rationalization]] 
beyond the constraint of these being [[nilpotent topological space|nilpotent]] or even [[simply connected topological space|simply connected]], hence outside the scope of plain [[rational homotopy theory]]:

Namely, given any [[connected topological space|connected]] space $X$ (but the same discussion applies to each [[connected component]] of a non-connected space), without any restriction on its [[fundamental group]], it fits into a [[homotopy fiber sequence]]

$$
  \array{
    \widehat X 
    &\xrightarrow{\;\;}&
    X
    \\
    && 
    \big\downarrow
    \\
    &&
    B \pi_1(X)    
  }
$$

with 

* its [[universal cover]] $\widehat X$, which *is* [[simply connected topological space|simply connected]]; 

* the [[classifying space]] $B \pi_1(X)$ of its [[fundamental group]] $\pi_1(X)$.


Now, by the general discussion at *[[infinity-action|$\infty$-action]]* and at *[[Borel model structure]]* ([here](Borel+model+structure#RelationToSliceOverSimplicialClassifyingSpace)) -- this means that $X$ regarded in the [[slice (infinity,1)-category|slice]] over $B \pi$ is [[equivalence in an (infinity,1)-category|equivalent]] to the [[covering space]] $\widehat X$ *equipped* with its canonical [[group action]] by $\pi$.

This allows to regard the [[rationalization]] of non-[[nilpotent spaces]] $X$ as being the image of the [[universal covers]] $\widehat X$ in $\pi_1(X)$-eqjuivariant homotopy theory. (Since the $\pi_1(X)$-action on a universal covering space is [[free action|free]], this is necessarily Borel-equivariant.)

This perspective is really due to 
[Brown & Szczarba 95](#BrownSzczarba95) (based on [Brown & Szczarba 90](#BrownSzczarba90), [Brown & Szczarba 93](#BrownSzczarba93)) -- to spot it there, look ([here](#BrownSzczarba95Pages)) for: 2nd par. on  p. 883 (16 of 48) and around Thm. 4.4 on p. 896 (29 of 48).

## Related concepts

* [[twisted equivariant Chern character]]

* [[equivariant de Rham complex]]

## References

Rational homotopy theory (as well as [[real homotopy theory]]) for general connected spaces $X$ and regarded as Borel-equivariant rational homotopy theory of their [[covering spaces]] is laid out, and the corresponding [[fundamental theorem of dg-algebraic rational homotopy theory]] is proven, in: 

* {#BrownSzczarba95} [[Edgar Brown]], [[Robert H. Szczarba]], _Real and Rational Homotopy Theory_, Chapter 17 in: *[[Handbook of Algebraic Topology]]*, North Holland (1995) 869-915 ([doi:10.1016/B978-044481779-2/50018-3](https://doi.org/10.1016/B978-044481779-2/50018-3), [ZB](http://mirrors.library.cornell.edu/ZMATH/zmath/en/zmath/search/?an=0865.55009))

  * {#BrownSzczarba95Pages} see p. 883 & 896 (16 & 29 of 48):  [[BrownSzczarba_BorelEquivariantRHT.pdf:file]]

based on

* {#BrownSzczarba90} [[Edgar Brown]], [[Robert H. Szczarba]], _Continuous cohomology and Real homotopy type II_ Asterisque 191, Societe Mathematique De France (1990) ([numdam:AST_1990__191__45_0](http://www.numdam.org/book-part/AST_1990__191__45_0))

* {#BrownSzczarba93} [[Edgar Brown]], [[Robert H. Szczarba]], *Real and rational homotopy theory for spaces with arbitrary fundamental group*, Duke Mathematical Journal 71. (1993): 229-316 ([doi:10.1215/S0012-7094-93-07111-6](https://projecteuclid.org/journals/duke-mathematical-journal/volume-71/issue-1/Rational-and-real-homotopy-theory-with-arbitrary-fundamental-groups/10.1215/S0012-7094-93-07111-6.short))

A textbook account (apparently independently?!) is in:

* {#FelixHalperinThomas15} [[Yves Félix]], [[Steve Halperin]], [[Jean-Claude Thomas]], _Rational Homotopy Theory II_, World Scientific 2015 ([doi:10.1142/9473](https://doi.org/10.1142/9473))

(While [FHT 15](#FelixHalperinThomas15) does discuss, mostly in its Section 7, some aspects of non-simply connected spaces via the rational homotopy of their [[covering spaces]] with attention to $\pi_1$-actions, it does not seem to establish or mention aspects of a systematic generalization of the [[fundamental theorem of dg-algebraic rational homotopy theory]] to this situation.)

