## Definition

Let $M$ be a [[category]] with two [[model category|model structures]] $(C_q,W_q,F_q)$ and $(C_h,W_h,F_h)$, and assume that $F_h\subseteq F_q$ and $W_h \subseteq W_q$.  

+-- {: .un_theorem}
###### Theorem
There is a **mixed model structure** $(C_m,W_q,F_h)$ on $M$ in which the fibrations are the $h$-fibrations, but the weak equivalences are the $q$-equivalences.
=--

## Properties

An object is cofibrant in the mixed model structure if and only if it has the $h$-homotopy type of a $q$-cofibrant object.

## Examples

* From the Quillen and Str&#248;m [[model structures on topological spaces]], we obtain a mixed model structure in which the weak equivalences are the [[weak homotopy equivalences]], the fibrations are the [[Hurewicz fibrations]], and the cofibrant objects are those of the [[m-cofibrant space|homotopy type of a CW complex]].  (This example influences the notation above; the $q$-model structure is the Quillen one, the $h$-model structure is the "Hurewicz" (or "homotopy") one.)

* Similarly, we can mix the $q$- and $h$- [[model structures on chain complexes]].

* Let $T$ be an [[accessible functor|accessible]] [[strict 2-monad]] on a [[locally finitely presentable category|locally finitely presentable]] [[strict 2-category]] $K$.  Then by a theorem of Lack, the category $T Alg_s$ of strict $T$-[[algebra over a monad|algebras]] admits a [[transferred model structure]] from the [[2-trivial model structure]] on $K$, where the weak equivalences and fibrations are the morphisms which become internal equivalences and internal isofibrations in $K$.

  On the other hand, $T Alg_s$ has its own 2-trivial model structure.  Since the forgetful functor $T Alg_s \to K$ preserves equivalences and isofibrations (the latter since it has a strict left 2-adjoint), we can mix these two model structures to obtain one whose weak equivalences are the equivalences in $K$ (which are also the equivalences in the category $T Alg$ of $T$-algebras and [[pseudo morphisms]]), but whose fibrations are the isofibrations in $T Alg_s$.

## References

The original paper is

* [[Michael Cole]], *Mixing model structures*, Top. Appl. 153 (2006) 1016&#8211;1032

There is also an exposition in

* [[Peter May]] and [[Kate Ponto]], *More Concise Algebraic Topology*, section 17.3.
