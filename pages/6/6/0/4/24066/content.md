+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}


## Idea

For $\mathcal{C}$ a [[monoidal model category]] and $A \in Mon(\mathcal{C})$ a [[monoid in a monoidal category|monoid in]] $\mathcal{C}$, there is under mild conditions a natural [[model category]] structure on its [[category of modules|category of]] [[module over a monoid|modules over]] $A$. ([Schwede & Shipley 2000, Thm. 4.1 (3.1 in the preprint)](#SchwedeShipley00)).

## Statement

\begin{proposition}\label{SchwedeShipleyExistenceStatement}
  Let $(\mathcal{C}, \otimes, \mathbb{1})$ be a [[cofibrantly generated model category|cofibrantly generated]] [[monoidal model category]] and let $R \,\in\, Mon(\mathcal{C}, \otimes, \mathbb{1})$ be a [[monoid object]] whose [[underlying]] object is [[cofibrant object|cofibrant]] in $\mathcal{C}$. Then:

1. The category $R Mod(\mathcal{C}, \otimes, \mathbb{1})$ of [[internalization|internal]] $R$-[[module objects]] carries a [[cofibrantly generated model category|cofibrantly generated model structure]] whose [[weak equivalences]] and [[fibrations]] are those whose [[underlying]] maps are so in $\mathcal{C}$, hence which is [[transferred model structure|right transferred]] along the [[forgetful functor]] $U$:

   $$
     R Mod(\mathcal{C})
     \underoverset
       {\underset{ U }{\longrightarrow}} 
       {\overset{F}{\longleftarrow}}
       {\;\;\;\;\;\; \bot_{\mathrlap{Qu}} \;\;\;\;\;\;}
     \mathcal{C}
     \,.
   $$

1. If $R$ is in addition a [[commutative monoid object]] then the [[tensor product of modules]] makes $R Mod(\mathcal{C})$ itself into a [[monoidal model category]].

\end{proposition}

([Schwede & Shipley 2000, Thm. 3.1 with Rem. 3.2](#SchwedeShipley00))

## Related concepts

* **[[model structure on monoids in a monoidal model category]]**

  * [[model structure for ring spectra]]

* [[model structure on commutative monoids in a symmetric monoidal model category]]

* [[model structure on algebras over an operad]]

* [[model structure on algebras over a monad]]

* [[model structure on simplicial T-algebras]]

## References

General discussion:

* {#SchwedeShipley00} [[Stefan Schwede]], [[Brooke Shipley]], *Algebras and modules in monoidal model categories*, Proc. London Math. Soc. **80** 2  (2000)  491-511  &lbrack;[arXiv:math/9801082](https://arxiv.org/abs/math/9801082), [doi:10.1112/S002461150001220X](https://doi.org/10.1112/S002461150001220X)&rbrack;

Examples:

* [[Jordan Williamson]], §2.1 in: *Algebraic models of change of groups functors in (co)free rational equivariant spectra*, J. Pure Appl. Algebra **226** 11 (2022) 107108 &lbrack;[doi:10.1016/j.jpaa.2022.107108](https://doi.org/10.1016/j.jpaa.2022.107108), [arXiv:2003.12412](https://arxiv.org/abs/2003.12412)&rbrack;


{#TheSpecialCaseInFunctorCategory} The special case of the model structure on modules in a [[functor category]] with values in a closed symmetric [[monoidal model category]] is (re-)derived (see the discussion [here](https://nforum.ncatlab.org/discussion/14400/model-structure-on-modules-in-a-monoidal-model-category/?Focus=99231#Comment_99231)) in:

* Angelos Anastopoulos, [[Marco Benini]], Sec. 2.4 of *Homotopy theory of net representations*, Rev. Math. Phys. (2023) &lbrack;[arXiv:2201.06464](https://arxiv.org/abs/2201.06464), [doi:10.1142/S0129055X23500083](https://doi.org/10.1142/S0129055X23500083)&rbrack;

(there for the purpose of desribing representations of [[nets of observables]] in [[homotopical algebraic quantum field theory]]). 



[[!redirects model structures on modules in a monoidal model category]]
