
\tableofcontents

## The modulus congruence relation

The basic relation in modular arithmetic is the modulus relation. In [[dependent type theory]] with a [[natural numbers type]], one could define the modulus relation on the natural numbers as a ternary inductive type family $m \equiv n \mod k$ indexed by natural numbers $m:\mathbb{N}$, $n:\mathbb{N}$, and $k:\mathbb{N}$, inductively defined by the following constructors:

* for each $k:\mathbb{N}$, a term 
$$\mathrm{indzero}(k):0 \equiv 0 \mod k$$
* for each $k:\mathbb{N}$, $m:\mathbb{N}$ and $n:\mathbb{N}$, a term
$$\mathrm{indsucc}(m, n, k):(m \equiv n \mod k) \to (s(m) \equiv s(n) \mod k)$$
* for each $k:\mathbb{N}$ and $n:\mathbb{N}$, a term
$$\mathrm{indmodleft}(n, k):(n k \equiv 0 \mod k))$$
* for each $k:\mathbb{N}$ and $n:\mathbb{N}$, a term
$$\mathrm{indmodright}(n, k):(0 \equiv n k \mod k))$$

where $m n$ is multiplication of two natural numbers $m:\mathbb{N}$ and $n:\mathbb{N}$. 

For each nonzero natural number $k$, the type $(\mathbb{N}, m \equiv n \mod k)$ is [[equivalence of types|equivalent]] to the [[finite type]] $\mathrm{Fin}(k)$ equipped with its canonical [[identity type]]. When $k$ is zero the type $(\mathbb{N}, m \equiv n \mod k)$ is equivalent to the type of natural numbers with its canonical identity type. 

This implies that the modulus relation is valued in [[h-propositions]] and is a family of [[decidable]] [[equivalence relations]] indexed by $k$. 

## Related concepts

* [[finite field]]
* [[cyclic group]]

## References

* Wikipedia, _[Modular arithmetic](https://en.wikipedia.org/wiki/Modular_arithmetic)_

