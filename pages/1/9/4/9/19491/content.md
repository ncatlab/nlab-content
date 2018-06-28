+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The **dual fibration** of a (Grothendieck) [[Grothendieck fibration|fibration]] is a fibration over the same base but with all of the fibers dualized.

## Definition

Let $p : E \to B$ be a fibration, and let $F : B^{op} \to Cat$  be the corresponding [[indexed category]]. The dual fibration $p^d : E^d \to B$ can be defined [(Borceux)](#Borceux) as the fibration associated (via the [[Grothendieck construction]]) to the composite

$$
 B^{op} \stackrel{F}{\longrightarrow} Cat \stackrel{(-)^{op}}{\longrightarrow} Cat
$$

where $(-)^{op} : Cat \to Cat$ is the operation sending any category to its opposite (note this operation preserves the direction of the 1-cells, although it reverses the direction of the 2-cells in Cat). (See [Borceux](#Borceux) reference.) Alternatively, the dual fibration may be defined in more elementary terms as a category with the same objects as $E$, and whose morphisms are equivalence classes of [[spans]] $R \stackrel{v}{\longleftarrow} X \stackrel{h}{\longrightarrow} S$ where $v$ is _vertical_ (i.e., $p(v) = id$) and $h$ is _horizontal_ (i.e., $p$-[[cartesian morphism|cartesian]]). (See [Pavlovic](#Pavlovic90) and [Kock](#AKock15) references.)

## References

* {#Pavlovic90} [[Dusko Pavlovic|Duško Pavlović]], _Categorical Interpolation: Descent and the Beck-Chevalley Condition without Direct Images_ , pp.306-325  in _Category theory Como 1990_, LNM **1488** Springer Heidelberg 1991. ([pdf](http://www.isg.rhul.ac.uk/dusko/papers/1990-BCDE-Como.pdf))

* {#Borceux} [[Francis Borceux]], [[Handbook of Categorical Algebra]] (see Volume 2, 8.3).

* {#AKock15} [[Anders Kock]], The dual fibration in elementary terms, [arXiv:1501.01947](https://arxiv.org/abs/1501.01947).