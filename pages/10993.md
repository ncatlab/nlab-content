
#Contents#
* table of contents
{:toc}


## Idea

A _relative monad_ is what is to a _[[relative adjunction]]_ as a [[monad]] is to an [[adjunction]].

In [ACU14](#ACU14), the authors proved that a relative monad on a functor $J:\mathbf J \to \mathbf C$ are 'skew-monoids in the [[skew-monoidal category]] $[\mathbf J, \mathbf C]$' (see below).

## Definition
Let $\mathbf J, \mathbf C$ be categories and $J: \mathbf J \to \mathbf C$ be a functor.

\begin{definition}
\label{def}
A **relative monad $T$ on $J$** is a functor $T:\mathbf J \to \mathbf C$ equipped with

* a _unit_ $\eta_X : JX \to TX$ natural in $X : \mathbf J$,
* a _Kleisli extension_ $(-)^* : \mathbf C(JX, TY) \to \mathbf C(TX, TY)$ in both $X,Y:\mathbf J$

such that for every $X,Y,Z:\mathbf J$ and $k:JX \to TY$,

* _(left unital law)_ $k = k^* \circ \eta_X$,
* _(right unital law)_ $\eta_X^* = 1_{TX}$,
* _(associativity law)_ $(\ell^* \circ k)^* = \ell^* \circ k^*$ for every $\ell : JY \to TZ$.

\end{definition}

Notice that for any $f:X \to Y$ in $\mathbf J$, one has
\[
    Tf = (\eta_{JY} \circ Jf)^*.
\]

In computer science, monads are usually defined by a unit and an extension operator, as above, so that relative monads are very close to plain monads in that regard. Since $[\mathbf J, \mathbf C]$ lacks a monoidal structure (unlike $[\mathbf C, \mathbf C]$), to define relative monads like mathematicians define monads (as monoids in a category of endofunctors) we need to be more clever.

### As skew-monoids
A [[skew-monoidal category]] is like a monoidal category except its unitors and associators are not necessarily invertible. A monoid in a skew-monoidal category is called a 'skew-monoid'.

Composition of functors $F,G:\mathbf J \to \mathbf C$ can be defined by first [[left Kan extension|extending]] $F$ along $J$ and then composing with $G$. The resulting composition product on $[\mathbf J, \mathbf C]$ is coherent but only laxly so, hence the need to appeal to skew-monoidal categories.

\begin{theorem}[Theorem 3.4]
Suppose $J:\mathbf J \to \mathbf C$ is such that $\mathrm{Lan}_J : [\mathbf J, \mathbf C] \to [\mathbf C, \mathbf C]$ exists (e.g. if $\mathbf J$ is small and $\mathbf C$ cocomplete).
Then $[\mathbf J, \mathbf C]$ is skew-monoidal, with unit $J$ and product $F \circ^J G = (\mathrm{Lan}_J F) \circ G$, and a relative monad is a monoid in $([\mathbf J, \mathbf C], J, \circ^J)$.
\end{theorem}


## Related pages

* [[relative comonad]]

## References

Discussion with an eye towards [[monad (in computer science)|monads in computer science]] is in 

* {#ACU14} [[Thorsten Altenkirch]], James Chapman, Tarmo Uustalu, _Monads need not be endofunctors_, Logical methods in computer science ([arxiv](https://arxiv.org/abs/1412.7148))


[[!redirects relative monads]]

