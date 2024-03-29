
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

## Idea

Over a [[ring]] whose [[characteristic]] is a [[prime number]] $p$ it is true that

$$
  (a+b)^p = a^p + b^p
  \,,
$$

because all the non-trivial [[binomial theorem|binomial coefficients]] are multiples of $p$. 

## Primality 

+-- {: .num_lemma #primality} 
###### Lemma 
An integer $n \geq 2$ is prime if and only if the [[binomial coefficients]] satisfy 

$$\binom{n}{k} \equiv 0 \pmod{n}$$ 

whenever $0 \lt k \lt n$. 
=-- 

+-- {: .proof} 
###### Proof 
If $p$ is prime, then $p$ divides neither $k!$ nor $(p-k)!$ if $0 \lt k \lt p$. So, since $p$ divides 

$$p! = \binom{p}{k}k! \cdot (p-k)!,$$

it must divide $\binom{p}{k}$. 

If $n$ is composite, write $n = p q$ where $p$ is any prime dividing $n$, so that $0 \lt p \lt n$. If the factor $p$ appears with multiplicity $j$ in $n$, then it appears with multiplicity $j$ in $n(n - 1) \ldots (n - p + 1)$ and with multiplicity $1$ in $p! = p(p-1)\ldots 1$, and so it appears with multiplicity $j-1$ in $\binom{n}{p}$. It follows that $n$ cannot divide $\binom{n}{p}$, i.e., $\binom{n}{p} \nequiv 0 \pmod{n}$. 
=-- 

## Related concepts

* [[Frobenius morphism]]


## References

* Wikipedia, _[Freshman's dream](http://en.wikipedia.org/wiki/Freshman's_dream)_

[[!redirects freshman dream arithmetic]]
[[!redirects freshman's dream arithmetic]]
