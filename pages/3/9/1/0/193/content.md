#Definition#

An _adjunction_ is a pair of [[category|categories]] $C, D$ together with [[functor|functors]] $L: C \to D$, $R : D \to C$ and [[natural transformation|natural transformations]] $\eta : 1_C \to R L$, $\epsilon : L R \to 1_D$ satisfying some equations called the [[zig-zag identities]] or the _triangle identities_.

In this situation we call $L$ and $R$ [[adjoint functor|adjoint functors]] - and more precisely, we call $L$ the [[left adjoint]] (of $R$) and $R$ the [[right adjoint]] (of $L$).  We call $\eta$ the [[unit]] and $\epsilon$ the [[counit]] of the adjunction.

More generally, we can [[internalization|internalize]] the concept of adjunction in any [[strict 2-category|2-category]] or [[bicategory]].

#Remarks#

Essentially everything that makes category theory nontrivial and interesting can be derived from the concept of adjunction. In particular [[universal construction]]s such as [[limit|limits and colimits]] are examples of certain adjunctions.
