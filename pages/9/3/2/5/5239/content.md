

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
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

For $\mathcal{C}$ a [[cofibrantly generated model category]] and $T \colon \mathcal{C} \longrightarrow \mathcal{C}$ a [[monad]] on $\mathcal{C}$, there is under mild conditions a natural [[model category]] structure on the category of [[algebras over a monad]] over $T$.

## Definition

Let $\mathcal{C}$ be a [[cofibrantly generated model category]] and $T \colon \mathcal{C} \longrightarrow \mathcal{C}$ a [[monad]] on $\mathcal{C}$. 

Then under mild conditions there exists the [[transferred model structure]] on the category of [[algebras over a monad]], transferred along the [[free functor]]/[[forgetful functor]] [[adjunction]]

$$
  (F \dashv U) 
      \;\colon\; 
   Alg_T(\mathcal{C}) 
     \stackrel{\overset{F}{\longleftarrow}}{\underset{U}{\longrightarrow}} 
   \mathcal{C}
  \,.
$$

See ([Schwede-Shipley 00, lemma 2.3](#SchwedeShipley00)).

## Related concepts

* [[model structure on monoids in a monoidal model category]]

* [[model structure on algebras over an operad]]

* **model structure on algebras over a monad**

* [[model structure on coalgebras over a comonad]]

* [[model structure on simplicial T-algebras]]

## References

* {#SchwedeShipley00} [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_, Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf)) 





