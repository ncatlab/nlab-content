
#Contents#
* table of contents
{:toc}

## Idea

A generalization of the concept of _[[monad (in computer science)]]_. In particular, it generalizes the attitude that monads in computer science are useful insofar as they generate a [[Kleisli category]].
Thus an arrow abstracts the hom-profunctor of $\mathrm{Kl}(T)$ for a strong monad $T: \mathbf C \to \mathbf C$ as an endoprofunctor on $\mathbf C$.

Therefore, an arrow $A : \mathbf C^{op} \times \mathbf C \to \mathbf{Set}$ can be thought as a putative replacement of $\mathrm{Hom}_{\mathbf C} : \mathbf C^{op} \times \mathbf C \to \mathbf{Set}$. In fact an arrow comes equipped with a transformation $\mathrm{arr} : \mathrm{Hom}_{\mathbf C} \Rightarrow A$ that lift morphisms of $\mathbf C$ to the 'augmented' morphisms given by $A$, and with a transformation $\ggg : A \circ A \Rightarrow A$ that behaves like a composition operation. Then one requires that $\ggg$ is associative and that $\mathrm{arr}(1_a)$ is the unit of this operation.

These data makes $A$ a [[promonad]] on $\mathbf C$, i.e. a monad on $\mathbf C$ in the bicategory of [[profunctors]]. Since every monad on $\mathbf{Set}$ (or on any reasonable enriching base where programmers work) is strong, arrows traditionally generalize the hom-profunctor of [[strong monads]]. The additional requirement that $A$ is a [[strong profunctor]] (and the laws it is required to satisfy) imply that an arrow is a [[strong monad|strong monad]] in the bicategory [[profunctors]] ([Asada10](#Asada10)).

## Definition
\begin{definition}
  An arrow $A$ on a [[monoidal category]] $\mathbf C$ is a monoid in the category of [[strong profunctor|strong endoprofunctors]] on $\mathbf C$, i.e. it's a functor $\mathbf C^{op} \times \mathbf C \to \mathbf{Set}$ equipped with the following structure:

1. A natural family of morphisms $\mathrm{arr} : \mathbf C(a,b) \to A(a,b)$ (the unit of the monoid),
2. A natural family of morphisms called *composition* $\ggg : A(a,b) \times A(b,c) \to A(a,c)$ (the multiplication of the monoid), which satisfy an associative law and for which $\mathrm{arr}_{a,a}(1_a)$ is the unit,
3. A family of morphisms called *strength* $s_{a,b,m} : A(a,b) \to A(m \otimes a, m \otimes b)$, which is [[dinatural transformation|dinatural]] in $m$ and natural in $a, b$, and satisfies coherence laws that make $(A, s)$ a [[strong profunctor]].

\end{definition}

## References

Arrows originate in Section 2 of

* [[John Hughes]], _Generalising monads to arrows_, Sci. Comput. Program. 37(1--3), pp. 67--111, 2000 ([doi:10.1016/S0167-6423(99)00023-4](https://doi.org/10.1016/S0167-6423%2899%2900023-4), [pdf](http://www.cse.chalmers.se/~rjmh/Papers/arrows.pdf))

The 'justification' of arrows as strong monads in $\mathbf{Prof}$ is given in


* {#Asada10} Kazuyuki Asada, _Arrows are strong monads_, 2010 ([pdf](http://www.riec.tohoku.ac.jp/~asada/papers/arrStrMnd.pdf))

Comparisons of monads with [[applicative functors]] (also known as idioms) and with [[arrows (in computer science)]] are in 

* [[Sam Lindley]], [[Philip Wadler]], [[Jeremy Yallop]], _Idioms are Oblivious, Arrows are Meticulous, Monads are Promiscuous_, Electron. Notes Theor. Comput. Sci. 229(5), pp. 97--117, 2011 ([doi:10.1016/j.entcs.2011.02.018](https://doi.org/10.1016/j.entcs.2011.02.018))
* [[Exequiel Rivas]], _Relating Idioms, Arrows and Monads from Monoidal Adjunctions_, MSFP@FSCD 2018, pp. 18--33 ([arXiv:1807.04084](https://arxiv.org/abs/1807.04084), [doi:10.4204/EPTCS.275.3](https://doi.org/10.4204/EPTCS.275.3))

[[!redirects arrows (in computer science)]]


