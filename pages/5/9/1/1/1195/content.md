Minimal logic, introduced by I. Johansson in 1936, is [[intuitionistic logic]] without the _ex falso quodlibet_ rule $\bot \vdash A$.  It may also be defined by starting with Gentzen\'s [[sequent calculus]] for [[classical logic]] with $\bot$ but not $\neg$, and restricting to sequents $\Gamma \vdash \Delta$ where $\Delta$ must contain *exactly one* formula. The same is not true if you start with Gentzen\'s sequent calculus with $\neg$ but not $\bot$; for example, the sequent $ p, \neg p \vdash \neg q$ is valid in minimal logic, but it is not derivable in that sequent calculus if each succedent is required to consist of exactly one formula.

Because it is not the case here that
anything follows from a contradiction, minimal logic is a
[[paraconsistent logic]].

Models of minimal logic are cartesian closed categories, optionally
with finite $n$-ary coproducts for $n\gt 1$.  Under the [Curry-Howard
correspondence](http://en.wikipedia.org/wiki/Curry-Howard_correspondence) minimal logic corresponds to [simply-typed lambda
calculus](http://en.wikipedia.org/wiki/Simply-typed_lambda_calculus), which is roughly speaking another way of saying that both are forms of the [[internal logic]] of [[cartesian closed category|cartesian closed]] categories.


## References

For a definition of the minimal logic, see Chapter 2 in

* [[Sergei P. Odintsov]], _Constructive Negations and Paraconsistency_, Trends in Logic 26, Springer, 2008.  [doi](http://dx.doi.org/10.1007/978-1-4020-6867-6).
