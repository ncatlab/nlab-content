
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

Minimal logic &lbrack;[Johansson 1937](#Johansson1937)&rbrack; is [[intuitionistic logic]] without the _[[ex falso quodlibet]]_ rule $\bot \vdash A$.  

It may also be defined by starting with Gentzen\'s [[sequent calculus]] for [[classical logic]] with $\bot$ but not $\neg$, and restricting to sequents $\Gamma \vdash \Delta$ where $\Delta$ must contain *exactly one* formula. The same is not true if you start with Gentzen\'s sequent calculus with $\neg$ but not $\bot$; for example, the [[sequent]] $ p, \neg p \vdash \neg q$ is valid in minimal logic, but it is not derivable in that sequent calculus if each [[succedent]] is required to consist of exactly one formula.

Because it is not the case here that anything follows from a falsehood, minimal logic is a [[paraconsistent logic]]. However, it still satisfies the weaker law
$$ 
  A,\, \neg A \;\vdash\; \neg B 
$$
for any $A$ and $B$.  This is a weaker form of _ex contradictione quodlibet_, which is still strong enough to be undesirable if one wants to do serious things with a paraconsistent logic.

[[categorical semantics|Categorical semantics]] of minimal logic is provided by [[cartesian closed categories]], optionally with [[finite coproducts|$n$-ary coproducts]] for $n\gt 1$.  

Under the [[Curry-Howard correspondence]] minimal logic corresponds to [[simply-typed lambda calculus]], which,  roughly speaking, is another way of saying that both are forms of the [[internal logic]] of [[cartesian closed categories]].

## See also

* [[cartesian closed category]]

## References

The original article:

* {#Johansson1937} Ingebregt Johansson: _Der  Minimalkalkül,  ein  reduzierter  intuitionistischer  Formalismus_,  Compositio Mathematica **4** (1937) 119-136 &lbrack;[numdam:CM_1937__4__119_0](http://www.numdam.org/item/CM_1937__4__119_0)&rbrack;

Review:

* Sergei P. Odintsov, Chapter 2 in: _Constructive Negations and Paraconsistency_, Trends in Logic **26**, Springer (2008)  &lbrack;[doi:10.1007/978-1-4020-6867-6](http://dx.doi.org/10.1007/978-1-4020-6867-6)&rbrack;

See also:

* Wikipedia: *[Minimal logic](https://en.wikipedia.org/wiki/Minimal_logic)*




