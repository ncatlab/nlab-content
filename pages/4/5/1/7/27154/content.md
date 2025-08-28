
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

* table of contents
{:toc}

## Idea

In 2-categorical algebra, there are many kinds of morphism  between objects: e.g. [[strict morphisms]], [[pseudo morphisms]], [[lax morphisms]], [[colax morphisms]], etc. Typically it is the pseudo and (co)lax morphisms that arise in practice (for instance, we are rarely interested in [[strict monoidal functors]]), but the strict morphisms tend to be simpler to work with.

In many situations, we can study the weaker kinds of morphism using the strict kinds of morphism using a **weak morphism classifier**. A weak morphism classifier for an object $A$ is an object $A'$ such that weak morphisms $A \to B$ are in [[natural bijection]] with strict morphisms $A' \to B$.

Dually, a **weak morphism coclassifier** is an object $B'$ such that weak morphisms $A \to B$ are in natural bijection with strict morphisms $A \to B'$.

## Definition

### For algebras of 2-monads

Let $T$ be a [[2-monad]] and denote by $T-Alg_s$ the 2-category of [[strict algebras]] and [[strict morphisms]] for $T$. Denote by $T-Alg_w$ the 2-category of [[strict algebras]] and *$w$-weak morphisms* for $T$ (where $w$ is *pseudo*, *lax*, *colax*, etc.). There is an [[identity-on-objects]] [[2-functor]]:
$$T-Alg_s \to T-Alg_w$$
If this admits a left 2-adjoint $(-)' : T-Alg_w \to T-Alg_s$, we call this the **$w$-weak morphism classifier** for $T$. It if admits a right 2-adjoint $T-Alg_w \to T-Alg_s$, we call this the **$w$-weak morphism coclassifier** for $T$.

Weak morphism classifiers exist if and only if certain [[codescent objects]] exist in $T-Alg_s$.

Under minimal assumptions, the $w$-weak morphism classifier 2-adjunction is [[lax-idempotent 2-adjunction|$w$-idempotent]] ([Blackwell 1976](#Blackwell)).

## Related pages

* [[2-monad]]

* [[lax morphism]], [[colax morphism]], [[pseudo morphism]]


## References

* {#Blackwell} [[Robert Blackwell]], _Some existence theorems in the theory of doctrines_, PhD thesis (1976), ([pdf](https://unsworks.unsw.edu.au/server/api/core/bitstreams/820c3175-88e9-4201-8f4a-2fecd46f2b24/content))
* [[Robert Blackwell]], [[Max Kelly]], [[John Power]], _Two-dimensional monad theory_, ([doi](https://doi.org/10.1016/0022-4049%2889%2990160-6))
* [[Stephen Lack]], _Codescent objects and coherence_, Stephen Lack, J. Pure and Appl. Algebra __175__ (2002) 223-241 <a href="https://doi.org/10.1016/S0022-4049(02)00136-6">doi</a>
* [[Stephen Lack]] and [[Michael Shulman]], _Enhanced 2-categories and limits for lax morphisms_, Advances in Mathematics 229.1 (2012): 294-356.
* [[Stephen Lack]], _Morita contexts as lax functors_, Applied Categorical Structures 22.2 (2014): 311-330.
* Kengo Hirata, _Generalization of formal monad theory to lax functors_, [arXiv:2301.06420](https://arxiv.org/abs/2301.06420) (2023).

[[!redirects weak morphism classifiers]]
[[!redirects lax morphism classifier]]
[[!redirects lax morphism classifiers]]
[[!redirects colax morphism classifier]]
[[!redirects colax morphism classifiers]]
[[!redirects oplax morphism classifier]]
[[!redirects oplax morphism classifiers]]
[[!redirects pseudo morphism classifier]]
[[!redirects pseudo morphism classifiers]]

