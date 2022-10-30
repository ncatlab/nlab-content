# Contents #
* table of contents 
{: toc}

## Statement

For $x$ an [[integer]] and $p$ a [[prime number]], if $x \nequiv 0 \pmod{p}$, then $x^{p-1} \equiv 1 \pmod{p}$.

This useful result is in a sense trivial, since the [[ring]] $\mathbb{Z}/(p)$ is a finite [[field]], with [[group of units]] $G$ of [[order of a group|order]] $p-1$; it is just a matter of recalling $x^{ord(G)} = 1$ for all $x$ in a [[finite group]] $G$. For the same reason, $a^{q-1} = 1$ for any nonzero $a$ in a finite field with $q$ elements. 

## Refinements 

A stronger result is that the group of units of a finite field with $q$ elements is _[[cyclic group|cyclic]]_ of order $q-1$, or indeed that every finite subgroup of the group of units of any field is cyclic. A proof may be found [here](/nlab/show/root#rootsunity). 

If $A$ is a commutative $\mathbb{F}_p$-[[associative unital algebra|algebra]], then the map $a \mapsto a^p$ is an algebra endomorphism $\sigma: A \to A$ (this follows easily from the [[binomial theorem]] and the fact that $\binom{p}{k} \equiv 0 \pmod{p}$ when $0 \lt k \lt p$). It follows that $\sigma: \mathbb{F}_q \to \mathbb{F}_q$ is a field _automorphism_ on a field with $q = p^k$ elements, since after all 

$$\sigma^k(a) = a^{p^k} = a^q = a^{q-1}a = a$$ 

for any $a \in \mathbb{F}_q$. See also [[Frobenius automorphism]]. 

## Pseudoprimes and Carmichael numbers 

Fermat's little theorem says that in order for a positive integer $p$ to be prime, it is necessary that $a^p \equiv a \pmod{p}$ for any integer $a$ (one may as well assume $0 \leq a \lt p$). This gives a way of showing that an integer $n$ is _not_ prime (by finding an $a$ less than $n$ such that $a^{n-1} \nequiv 1 \pmod{n}$) that, especially for large $n$, is more efficient than  actually factoring $n$. 

One type of (probabilistic) primality test for $p$ is to take a base, for example $a = 2$, and check whether $a^{p-1} = 1 \pmod{p}$. Chances are good that $p$ is in fact prime if this is satisfied, although there certainly exist composite numbers which pass this test (called pseudoprimes base $a$). The smallest pseudoprime base $2$ is $341 = 11 \cdot 31$. One effective primality test for "small" $p$ (e.g., less than $10^{15}) is to use such a primality test coupled with a table of pseudoprimes. 

There are numbers such as $n = 561 = 3 \cdot 11 \cdot 17$ which are pseudoprimes in any base; these are called _Carmichael numbers_. A positive integer $n$ is Carmichael iff it is square-free and for each prime divisor $p$ of $n$, we have that $p-1$ is a divisor of $n-1$. They are comparatively rare, but it is known there are infinitely many (for sufficiently large $n$, there are at least $n^{2/7}$ Carmichael numbers between $1$ and $n$). 

## AKS primality test 

A generalization of Fermat's little theorem can be used to give a deterministic test for primality that can be carried out in "polynomial time" (bounded by a polynomial applied to the number of digits); it was  published only as recently as 2002: 

+-- {: .num_theorem} 
###### Theorem 
**(Agrawal, Kayal, Saxena)** 
An integer $n \geq 2$ is prime if and only if 

$$(x-a)^n \equiv x^n - a^n \pmod{n}$$ 

for every or even any $a$ coprime to $n$ (so that, for example, the case $a=1$ would be a sufficient criterion for primality). 
=-- 

As stated, checking such a congruence directly would be of exponential complexity, but these authors provided a clever reduction which reduces the complexity to polynomial time. 

## References 

Named after _[[Pierre de Fermat]]_.

*  Manindra Agrawal, Neeraj Kayal, and Nitin Saxena, _PRIMES is in P_,  Annals of Mathematics 160 (2) (2004), 781&#8211;793. doi:10.4007/annals.2004.160.781. JSTOR 3597229. 


