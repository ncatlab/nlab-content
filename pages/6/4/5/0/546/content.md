+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea
A ([[small category|small]]) _cocategory_ is a [[category]] [[internal category|internal to]] $Set^{op}$, the [[opposite category]] of [[Set]].

More generally, if $C$ is [[finitely complete category|finitely cocomplete]], there is a notion of cocategory internal to $C$, namely a [[comonad]] in the [[bicategory]] of [[span|cospans]] in $C$. 

If $c_0 \to c_1 \leftarrow c_0$ is a cocategory object in $C$, then by homming out of $c_\bullet$, one obtains a limit-preserving functor $C \to Cat$. Under reasonable conditions, the [[adjoint functor theorem]] conversely implies that all limit-preserving functors $C \to Cat$ are obtained in this way.

## Examples

 - Many [[interval object|interval objects]] are cocategory objects. For example, the arrow category is a cocategory object in $Cat$.

 - Any [[coalgebra]] object is a cocategory object. This includes [[coring|corings]], [[Hopf algebroid|Hopf algebroids]], [[cogroupoid|cogroupoids]], etc.

 - In $Set$, every cocategory object is a coproduct of copies of the trivial cocategory object $1 \to 1 \leftarrow 1$ and the cocategory object $1 \to 2 \leftarrow 1$ where the two points are distinct. These represent the [[discrete category]] functor and the [[codiscrete category]] functors $Set \to Cat$, respectively.

## Related concepts

* [[comonoid]]
* [[Trimble n-category]]

## References

* [[Peter LeFanu Lumsdaine]], _A Small Observation on Co-categories_ &lbrack;[arXiv:0902.4743](https://arxiv.org/abs/0902.4743)&rbrack;

* Vasileios Aravantinos-Sotiropoulos, and [[Christina Vasilakopoulou]], _Sweedler theory for double categories_ &lbrack;[arXiv:2408.03180](https://arxiv.org/abs/2408.03180)&rbrack;

Presentation slides on $V$-cocategories and cocomposition:

* [[Christina Vasilakopoulou]], _Enriched duality in double categories_ &lbrack;[link](http://www.math.ntua.gr/~cvasilak/documents/EnrichedDualityDoubleCatsPlain.pdf)&rbrack;


[[!redirects cocomposition]]

[[!redirects cocategories]]
[[!redirects co-category]]
[[!redirects co-categories]]
