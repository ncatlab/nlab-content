
\tableofcontents

## Idea

Minimal logic, introduced by I. Johansson in 1937, is [[intuitionistic logic]] without the _ex falso quodlibet_ rule $\bot \vdash A$.  It may also be defined by starting with Gentzen\'s [[sequent calculus]] for [[classical logic]] with $\bot$ but not $\neg$, and restricting to sequents $\Gamma \vdash \Delta$ where $\Delta$ must contain *exactly one* formula. The same is not true if you start with Gentzen\'s sequent calculus with $\neg$ but not $\bot$; for example, the sequent $ p, \neg p \vdash \neg q$ is valid in minimal logic, but it is not derivable in that sequent calculus if each succedent is required to consist of exactly one formula.

Because it is not the case here that
anything follows from a falsehood, minimal logic is a
[[paraconsistent logic]]. However, it still satisfies the weaker law
$$ A,\, \neg A \;\vdash\; \neg B $$
for any $A$ and $B$.  This is a weaker form of _ex contradictione quodlibet_, which is still strong enough to be undesirable if one wants to do serious things with a paraconsistent logic.

Models of minimal logic are cartesian closed categories, optionally
with finite $n$-ary coproducts for $n\gt 1$.  Under the [Curry-Howard
correspondence](http://en.wikipedia.org/wiki/Curry-Howard_correspondence) minimal logic corresponds to [simply-typed lambda
calculus](http://en.wikipedia.org/wiki/Simply-typed_lambda_calculus), which is roughly speaking another way of saying that both are forms of the [[internal logic]] of [[cartesian closed category|cartesian closed]] categories.

## See also

* [[cartesian closed category]]

## References

* Wikipedia, [Minimal logic](https://en.wikipedia.org/wiki/Minimal_logic)

For a definition of the minimal logic, see Chapter 2 in

* [[Sergei P. Odintsov]], _Constructive Negations and Paraconsistency_, Trends in Logic 26, Springer, 2008.  [doi](http://dx.doi.org/10.1007/978-1-4020-6867-6).

* Ingebregt Johansson, _Der  Minimalkalkül,  ein  reduzierter  intuitionistischer  Formalismus_,  Compositio Mathematica **4** (1937) pp. 119-136. ([numdam](http://www.numdam.org/item/CM_1937__4__119_0/))

