## Idea
Quasilimits (sometimes called _soft limits_) are a relaxation of [[2-limits]] so as to make them satisfy a 'quasi-universal' property, i.e. instead of being singled out up to unique isomorphism, they are identified only up to unique _adjunction_. They've been defined by [[John Gray|Gray]] in [his seminal 1974 book](#Gray74) on 2-category theory.

## Definition
Recall limits and colimits of a given diagram $F:\mathbf K \to \mathbf C$ can be defined as the right and left adjoint, respectively, to the diagonal $\Delta_{(-)} : \mathbf C \to [\mathbf K, \mathbf C]$ (aka constant functor):
\[
   \colim \vdash \Delta \vdash \lim
\]
Suppose now $\mathbf C$ is a [[2-category]] and $\mathbf K$ is a [[small category|small 2-category]]. Gray defines quasi(co)limits by relaxing the previous adjunction to be only a [[local adjunction]]:
\[
   \mathrm{qcolim} \vdash_{\mathrm{lax}} \Delta \vdash_{\mathrm{lax}} \mathrm{qlim}
\]
This means that, naturally in $X : \mathbf C$ and $F : \mathbf K \to \mathbf C$, there are adjunctions (instead of equivalences, like in a [[2-adjunction]]) between hom-categories:
\[
   \mathbf C(X, \lim F) \rightleftarrows \mathrm{Nat}(\Delta_X, F)
\]

Alternatively, one can give a definition in terms of a weakened representability property.

Let $F : \mathbf K \to \mathbf C$ be a small [[diagram]] in $\mathbf C$. Then recall that a [[2-limit]] for $F$ is an object $\lim F:\mathbf C$ equipped with a natural isomorphism
\[
  \phi_X : \mathbf C(X, \lim F) \cong \mathrm{Nat}(1, \mathbf C(X, F(-)))
\]
where $\Delta_{(-)} : \mathbf C \to [\mathbf K, \mathbf C]$ is the diagonal functor.

A **quasi-limit** for $F$ is then an object $\mathrm{qlim} F:\mathbf C$ equipped with a adjunctions
\[
  \psi_X : \mathbf C(X, \mathrm{qlim}F) \rightleftarrows \mathrm{Nat}(1, \mathbf C(X, F(-)))
\]
naturally in $X:\mathbf C$.

Notice that by replacing $1 : \mathbf C \to \mathrm{Cat}$ with an arbitrary weight $W$ we can easily give the definition of _weighted quasilimit_.

## References

Quasi-limits and their duals have been defined in §I.7.9 of:

* {#Gray74} [[John Gray]], _[[Adjointness for 2-Categories|Formal category theory: adjointness for 2-categories]]_, Lecture Notes in Mathematics, Vol. 391. 
Springer 1974 ([doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280))

See also

* _["Very lax" 2
-dimensional co/limits](https://mathoverflow.net/questions/386414/very-lax-2-dimensional-co-limits)_, MathOverflow
