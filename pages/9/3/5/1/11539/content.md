


# Contents #
* table of contents 
{: toc}

## Statement

For $x$ an [[integer]] and $p$ a [[prime number]], if $x \nequiv 0 \pmod{p}$, then $x^{p-1} \equiv 1 \pmod{p}$.

This useful result is in a sense trivial, since the [[ring]] $\mathbb{Z}/(p)$ is a finite [[field]], with [[group of units]] $G$ of [[order of a group|order]] $p-1$; it is just a matter of recalling $x^{ord(G)} = 1$ for all $x$ in a [[finite group]] $G$. For the same reason, $a^{q-1} = 1$ for any nonzero $a$ in a finite field with $q$ elements. 

## Refinements 

A stronger result is that the group of units of a finite field with $q$ elements is _[[cyclic group|cyclic]]_ of order $q-1$, or indeed that every finite subgroup of the group of units of any field is cyclic. A proof may be found [here](/nlab/show/root#rootsunity). 

If $A$ is a commutative $\mathbb{F}_p$-[[associative unital algebra|algebra]], then the map $a \mapsto a^p$ is an algebra endomorphism $\sigma: A \to A$ (the preservation of addition follows easily from the [[binomial theorem]] and the fact that $\binom{p}{k} \equiv 0 \pmod{p}$ when $0 \lt k \lt p$; apparently this is also known as the [[freshman's dream]]). It follows that $\sigma: \mathbb{F}_q \to \mathbb{F}_q$ is a field _automorphism_ on a field with $q = p^k$ elements, since after all 

$$\sigma^k(a) = a^{p^k} = a^q = a^{q-1}a = a$$ 

for any $a \in \mathbb{F}_q$. See also [[Frobenius automorphism]]. 

## Pseudoprimes and Carmichael numbers 

Fermat's little theorem says that in order for a positive integer $p$ to be prime, it is necessary that $a^p \equiv a \pmod{p}$ for any integer $a$ (one may as well assume $0 \leq a \lt p$). This gives a way of showing that an integer $n$ is _not_ prime (by finding an $a$ less than $n$ such that $a^{n-1} \nequiv 1 \pmod{n}$) that, especially for large $n$, is more efficient than  actually factoring $n$. 

One type of (probabilistic) primality test for $p$ is to take a base, for example $a = 2$, and check whether $a^{p-1} = 1 \pmod{p}$. Chances are good that $p$ is in fact prime if this is satisfied, although there certainly exist composite numbers which pass this test (called pseudoprimes base $a$). The smallest pseudoprime base $2$ is $341 = 11 \cdot 31$. One effective primality test for "small" $p$ (e.g., less than $10^{15}$) is to use such a primality test coupled with a table of pseudoprimes. 

There are numbers such as $n = 561 = 3 \cdot 11 \cdot 17$ which are pseudoprimes in any base; these are called _Carmichael numbers_. A positive integer $n$ is Carmichael iff it is square-free and for each prime divisor $p$ of $n$, we have that $p-1$ is a divisor of $n-1$. They are comparatively rare, but it is known there are infinitely many (for sufficiently large $n$, there are at least $n^{2/7}$ Carmichael numbers between $1$ and $n$). 

## AKS primality test 

A generalization of Fermat's little theorem can be used to give a deterministic test for primality that can be carried out on any integer $n$ in "polynomial time" (bounded by a polynomial applied to the number of digits of $n$); it was first published only as recently as 2002. 

+-- {: .num_lemma} 
###### Lemma 
An integer $n \geq 2$ is prime if and only if 

$$(x-a)^n \equiv x^n - a \pmod{n}$$ 

for every or even any $a$ coprime to $n$ (so that, for example, the case $a=1$ would be a sufficient criterion for primality). 
=-- 

+-- {: .proof} 
###### Proof 
By the [argument at freshman's dream](nlab/show/freshman's+dream#primality), primality of $n$ is equivalent to $(x-a)^n \equiv x^n - a^n \pmod{n}$ (for every or any $a$), and then primality of $n$ implies the further reduction $a^n \equiv a \pmod{n}$ by Fermat's little theorem. 
=-- 

Given an integer $r$, and an integer $a$ relatively prime to $r$, let $ord_r(a)$ denote the order of $a \pmod{r}$ as a unit in $\mathbb{Z}/(r)$. We let $log(n)$ denote the base $2$ [[logarithm]] of $n$, and $\phi$ denotes the [[Euler totient function]] (so $\phi(r)$ is the cardinality of the [[group of units]] of $\mathbb{Z}/(r)$). 

+-- {: .num_theorem} 
###### Theorem 
**(Agrawal, Kayal, Saxena)** 
For given $n$, let $r$ be the least positive integer such that $ord_r(n) \gt (log(n))^2$. Then $n$ is prime if and only if either 

* $n \leq r$ and whenever $1 \leq a \leq r$, either $1 = \gcd(a, n)$ or $n = \gcd(a, n)$, or 

* $r \lt n$ and whenever $a$ is an integer such that $1 \leq a \leq \sqrt{\phi(r)} \cdot log(n)$, we have 
$$(x - a)^n \equiv x^n - a \pmod{x^r - 1, n}.$$ 
=-- 

From this result, one can extract an algorithm that decides primality of $n$ in time bounded by a polynomial in $log(n)$, invoking help from the following result. 

+-- {: .num_lemma} 
###### Lemma 
For each $n$ there exists $r \leq \max \{3, (log(n))^5\}$ such that $ord_r(n) \gt (log(n))^2$. 
=-- 

These results form the basis for the first algorithm for deciding primality that is general (applies to any integer $n$), runs in polynomial time, is deterministic (other known efficient tests were randomized and only guaranteed high probability of primality), and unconditional (does not depend on conjectured number-theoretic results such as forms of the [[Riemann hypothesis]]). 

## Related concepts

+ [[Fermat quotient]]

## References 

Named after _[[Pierre de Fermat]]_.

*  Manindra Agrawal, Neeraj Kayal, and Nitin Saxena, _PRIMES is in P_,  Annals of Mathematics 160 (2) (2004), 781&#8211;793. doi:10.4007/annals.2004.160.781. JSTOR 3597229. ([pdf](http://www.cse.iitk.ac.in/users/manindra/algebra/primality_v6.pdf)) 


