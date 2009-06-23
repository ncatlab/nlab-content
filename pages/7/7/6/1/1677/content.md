Let $A$ and $B$ be [[algebraic theory|algebraic theories]]. The category $[A,B]$ of **$(A,B)$-bimodels** and their homomorphisms is the category of $A$-models and homomorphisms in $B Mod^{op}$. An alternative description is that is a co-$A$-model in $B Mod$. Each such bimodel $M$ determines and is determined by a pair of [[adjoint functor]]s

$$Hom_B(M,-): B Mod \to A Mod$$

$$M\otimes_A -: A Mod \to B Mod$$

Composition of such adjoint pairs yields a functor

$$\otimes_B: [B,C]\times [A,B] \to [A,C]$$

The category $[A,A]$ has a unit object -- it would be churlish not to overload our notation yet further by calling it $A$, corresponding to the fact that the free $A$-model on one generator has a canonical co-$A$-structure. So we have a bicategory; the 0-cells are algebraic theories, the 1-cells are bimodels and the 2-cells are homomorphisms of bimodels. Consider a monad in this bicategory: an algebraic theory $A$, an $(A,A)$-bimodel $M$, and homomorphisms $\eta : A\to M$, $\mu : M\otimes_A M \to M$ satisfying the usual rules. A module of this monad is given by an $A$-model $B$ together with an action $M\otimes_A B \to B$ satisfying the usual rules. It should be clear that such modules are models of an algebraic theory, which we shall confusingly denote by $M$. This theory is an extension of $A$ by unary operations (the elements of the underlying set of the underlying $A$-model of the underlying $(A,A)$-bimodel of the monad). The rules for composing them are given by $\mu$. They satisfy distributive laws over the operations of $A$ given by the co-$A$-structure of $M$.

We may overload $\eta$ to refer both to a homomorphism of bimodels and to a map of algebraic theories. The forgetful functor $MMod \to AMod$ has for its left adjoint the functor $M\otimes_A ?$, but it also has a right adjoint $Hom_A(M,?)$. So in this case the forgetful functor preserves colimits as well as limits. In fact all maps of theories whose associated forgetful functors have right adjoints must arise from such a monad in the bicategory of bimodels.

I would like some snappier terminology at this point. What should we call these monads in the bicategory of bimodels? If we use words like _algebra_ or _monad_ our rickety overloaded onomastic scaffolding starts to creak ominously. Put on your hard hats. We are in territory where to discriminate too meticulously between different views of the same thing is to invite fuddlement. And yet we have to hold in our heads that isomorphism is not equality, and that too cavalier an approach to identification can sometimes lead to error.