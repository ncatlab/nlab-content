{: toc}

## Idea

A _free variable theory_ is a [[first-order theory]] of [[quantifier]]-free open formulas that includes an [[inference rule]] for the [[substitution]] of [[terms]] for [[variables]].  For example, in an equational calculus such as [[primitive recursive arithmetic]] (PRA), we have
$$ \frac{F(x) = G(x)}{F(A) = G(A)} \quad \text{(Subst)} $$

## Arithmetic Theories

| Free Variable Theory                                                             | Definable functions                                  | Corresponding First-Order Theory                                       |
|----------------------------------------------------------------------------------|------------------------------------------------------|------------------------------------------------------------------------|
| [[polynomial time arithmetic]] (PTA), a.k.a. Cook's PV                           | [[polynomial time]] computable functions             | Buss's [[bounded arithmetic]] $\mathrm{S}_2^1$                         |
| [[elementary recursive arithmetic]] (ERA), a.k.a. $\mathcal{E}'$-arithmetic      | Kalmár [[elementary functions]]                      | [[elementary function arithmetic|EFA]] ($\mathrm{I}\Delta_0 + {\exp}$) |
| [[primitive recursive arithmetic]] (PRA), a.k.a. $\mathcal{F}_\omega$-arithmetic | [[primitive recursive functions]]                    | $\mathrm{I}\Sigma_1$                                                   |
| [[provably recursive arithmetic]], a.k.a. $\mathcal{E}^\ast$-arithmetic          | [[Peano arithmetic|PA]]-provably recursive functions | [[Peano arithmetic]] (PA)                                              |

We say that a free variable arithmetic theory _corresponds_ to a first-order theory whenever the functions definable in the former are exactly the provably total functions in the latter.

## References

* [[Reuben Goodstein]], _Logic-free formalisations of recursive arithmetic_, Mathematica Scandinavica **2** (1954). &lbrack;[doi:10.7146/math.scand.a-10412](https://doi.org/10.7146/math.scand.a-10412)&rbrack;
* [[Reuben Goodstein]], _Recursive Number Theory_, North Holland Publishing Company (1957).
* [[Harvey E. Rose]], _Subrecursion: Functions and Hierarchies_, Oxford University Press (1984).
* [[Petr Hájek]], [[Pavel Pudlák]], _Metamathematics of First-Order Arithmetic_, Springer (1993).

[[!redirects free variable theories]]