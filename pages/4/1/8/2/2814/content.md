
## Idea ##

A _monoidal functor_  is a [[functor]] $F : C \to D$ between [[monoidal category|monoidal categories]] $(C,\otimes_C, I_C)$ and $(D,\otimes_D, I_D)$ that respects the [[tensor product]] and the unit up to coherent but not necessarily invertible [[morphism]]s

$$
  \epsilon : I_D \stackrel{}{\to} F(I_c)  
$$

and

$$
  \mu_{x,y} : F(x) \otimes_D F(y) \to F(x \otimes_C y)
  \,.
$$

If these structure morphisms are [[isomorphism]]s then $F$ is called a **strong monoidal functor**. If they are even identities it is called a **strict monoidal functor**. In contrast to this, a strong monoidal functor may also be called a **weak monoidal functor**.  The general situation is also called, for emphasis, a **lax monoidal functor**.

A __[[colax monoidal functor]]__ (with various alternative names), is a monoidal functor from the [[opposite categories]] $C^{op}$ to $D^{op}$.

+-- {: .query}
Am I the only one who objects to the term 'comonoidal functor'?  Surely there are people who study (at least enriched over a symmetric ---but non-cartesian--- monoidal category) categories equipped with [[comonoid]]al structures; I would want 'comonoidal functor' to describe structure-preserving functors between *them*.  For functors between bimonoidal categories, we would have a conflict.  ---Toby

You're not the only one!  The Australians call these 'comonoidal functors' [[oplax monoidal functor|oplax monoidal functors]].  ---[[John Baez]]

I know that term, which is why I included it in the list of terms (^_^).  It\'s nice that you made that page, but you should also link to it in the text here and move the redirects from the bottom of this page to that one.  (I did that now.)   ---Toby
=--

If we pass to the [[delooping]] [[2-category|2-categories]] $\mathbf{B}C$ and $\mathbf{B}D$ then a lax monoidal functor corresponds to a [[lax 2-functor]] 

$$
  \mathbf{B}F : \mathbf{B}C \to \mathbf{B}D
  \,.
$$

If $F$ is strong monoidal then this is an ordinary [[2-functor]]. If it is strict monoidal, then this is a [[strict 2-functor]].


[[!redirects lax monoidal functor]]
[[!redirects strict monoidal functor]]
[[!redirects strong monoidal functor]]
[[!redirects weak monoidal functor]]