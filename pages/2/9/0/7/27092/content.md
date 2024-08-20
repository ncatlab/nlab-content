+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

## Definition

If $R$ is a commutative [[integral domain]]. An $R$-module $M$ is divisible if $r M = M$ for all $0\neq r \in R$. 

According to [Levy 1963](#Levy1963), in the case of a general ring $R$, we require this only for $r$ which are regular elements (non-zero-divisors).

For a general [[torsion theory]] $(T,F)$ (torsion class, torsionfree class) on $R-mod$ for any ring $R$, we say that $M$ in $R-Mod$ is divisible if $E(M)/M$ is torsionfree where $E(M)$ is the [[injective hull]] of $M$. This is equivalent to be $J$-[[injective module]] where $J$ is the class of all monomorphisms whose cokernel is torsion. In other words, $M$ is divisible if whenever $B/A$ is torsion then any $A\to M$ can be extended to $B\to M$ along the inclusion $A\hookrightarrow B$.

Similarly, $M$ is $(T,F)$-codivisible if for every epimorphism $B\to A$ whose kernel is torsionfree, every map $M\to A$ can be extended to $B$ (in other words it is $K$-[[projective module|projective]] where $K$ is the class of all epimorphisms with torsionfree kernel).


## Properties

If $R$ is a commutative domain, consider the sum $\sigma M$ of all divisible $R$-submodules of $M$ (that is, the maximal divisible $R$-submodule of $M$). The correspondence $M\to\sigma M$ is functorial, in fact $\sigma$ extends to an additive subfunctor of the identity which is idempotent, satisfies $\sigma(M/\sigma(M)) = 0$, but $\sigma$ is not left exact in general.

## Literature

For general [[torsion theories]]

* [[Joachim Lambek]], _Torsion theories, additive semantics, and rings of quotients_, Springer Lecture Notes in Math. __177__, 1971

* Paul E. Bland, _Divisible and codivisible modules_, Mathematica Scandinavica __34__:2 (1974) 153--161 [jstor](https://www.jstor.org/stable/24490642)

* Mark Lawrence Teply, _A class of divisible modules_, Pacific J. Math. __45__:2 (1973) 653--668 [doi](https://doi.org/10.2140/pjm.1973.45.653)

A notion of divisibility of left $R$-modules with respect to some class $\Sigma$ of left ideals in a unital ring $R$ is introduced in 

* D. Sanderson, _A generalization of divisibility and injectivity in modules_, Canad. Math. Bull. 8 (1965) 505--513

In the case of commutative domains (studying "conditions, some necessary, some sufficient, for the torsion submodule of a divisible module to be a direct summand") see

* Eben Matlis, _Divisible modules_, Proc. Amer. Math. Soc. __11__:3 (1960) 385--391 [jstor](https://www.jstor.org/stable/2034781)

A version for noncommutative domains

* {#Levy1963} Lawrence Levy, _Torsion-free and divisible modules over non-integral-domains_, Canadian J. Math. 15 (1963) 132--151 [doi](https://doi.org/10.4153/CJM-1963-016-1)

category: algebra

[[!redirects codivisible module]]
[[!redirects divisible modules]]

