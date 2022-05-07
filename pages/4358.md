

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/SomePrimes.jpg" width="60"/>
</div>

A _prime number_ is a nonzero [[natural number]] that cannot be written as a [[multiplication|product]] of finitely many natural numbers (all) other than itself, hence a natural number greater than 1 that is [[division|divisible]] only by 1 and itself.

This means that every [[natural number]] $n \in \mathbb{N}$ is, up to re-ordering of factors, _uniquely_ expressed as a product of a tuple of prime numbers:

$$
  n \;=\; 2^{n_1}  \cdot 3^{n_2} \cdot  5^{n_3} \cdot 7^{n_4} \cdot  11^{ n_5 } \cdots
$$

This is called the _prime factorization_ of $n$.

Notice that while the number $1 \in \mathbb{N}$ is, clearly, only divisible by one and by itself, hence might look like it deserves to be counted as a prime number, too, this would break the uniqueness of this prime factorization. In view of the general phenomenon in classifications in [[mathematics]] of some objects being _[[too simple to be simple]]_ one could say that 1 is "too prime to be prime".

However, historically, some authors did count 1 as a prime number, see e.g. [Roegel 11](#Roegel11).


## Relation to ideals and arithmetic geometry
  {#RelationToIdeals}

A number is prime if and only if it generates a [[maximal ideal]] in the [[rig]] $\mathbb{N}$ of [[natural numbers]].

Prime numbers do *not* quite match the [[prime elements]] of $\mathbb{N}$, since $0$ generates a [[prime ideal]] but not a maximal ideal; instead they match the [[irreducible elements]] ([Wikipedia](http://secure.wikimedia.org/wikipedia/en/wiki/Irreducible_element)).

From the [[Isbell duality|Isbell-dual]] point of view, where a [[commutative ring]] such as the [[integers]] $\mathbb{Z}$ is regarded as the [[ring of functions]] on some [[variety]], namely on [[Spec(Z)]], the fact that prime numbers $p$ correspond to [[maximal ideals]] means that they correspond to the _[[closed points]]_ in this variety (see [this Example](Zariski+topology#SpecZ)), one also writes

$$
  (p) \in Spec(\mathbb{Z})
  \,.
$$

This [[Isbell duality|dual]] perspective on [[number theory]] as being the [[geometry]] ([[algebraic geometry]]) over [[Spec(Z)]] is called _[[arithmetic geometry]]_.

[[!include function field analogy -- table]]


## Properties


### Riemann hypothesis

see at _[[Riemann hypothesis]]_

### Goldbach conjecture

see at _[[Goldbach conjecture]]_

### Asymptotic distribution

see at _[[prime number theorem]]_

## Specific classes of prime numbers

* [[Fermat prime]]
* [[Mersenne prime]]
* [[twin prime]]

## Related concepts

* [[prime factor]]

* [[coprime integers]]

* [[Bertrand's postulate]]

* [[p-localization]]

* [[prime geodesic]]

* [[prime knot]]


## References

For historical discussion see

* {#Roegel11} Denis Roegel, _A reconstruction of Lehmer's table of primes (1914)_, 2011 ([pdf](http://locomat.loria.fr/lehmer1914/lehmer1914doc.pdf))

See also

* Wikipedia, _[Prime number](https://en.wikipedia.org/wiki/Prime_number)_

[[!redirects prime number]]
[[!redirects prime numbers]]
[[!redirects theory of primes]]

[[!redirects prime]]
[[!redirects primes]]
