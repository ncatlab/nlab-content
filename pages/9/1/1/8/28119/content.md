
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--


\tableofcontents


## Idea

### The formula

For $k \leq n \in \mathbb{N}$, the *binomial coefficient* $\left(n \atop k\right)$ is the [[natural number]] which is the [[fraction]] of the [[factorial]] of $n$ by the factorials of $k$ and $(n-k)$:

\[
  \label{PlainDefinition}
  \binom{n}{k}
  \;\coloneqq\;
  \frac{
    n!
  }{
    k! \cdot (n-k)!
  }
  \;=\;
  \frac{
    n \cdot (n-1) \cdot \cdots \cdot (n-k+1)
  }{
    1 \cdot 2 \cdot \cdots \cdot k
  }
  \mathrlap{\,.}
\]

Notice that

\[
  \label{Symmetry}
  \binom{n}{k}
  \;=\;
  \binom{n}{n-k}
  \mathrlap{\,.}
\]

The name "binomial coefficient" refers to the *[[binomial theorem]]* where these numbers appear as [[coefficients]] of the following [[polynomials]] in two [[variables]] $x$ and $y$, for $n \in \mathbb{N}$:

$$
  (x + y)^n
  \;=\;
  \sum_{ 0 \leq k \leq n}
  \binom{n}{k}
  \cdot
  x^k \cdot y^{n-k}
  \,.
$$

### The combinatorics

Namely, [[combinatorics|combinatorially]], $\left(n \atop k\right)$ is the count of the number of ways to *choose $k$ items from $n$ items without repetition but irrespective of order*: 

First, if the order did matter then there would be $n$ ways to pick the first item (one out of $n$), followed by $(n-1)$ ways to pick the second item (one out of the remaining $n-1$), and so on, up to $(n - (k-1))$ ways to pick the $k$th item, for a total of 

$$
  n \cdot (n-1) \cdot \cdots \cdot (n-(k-1)) 
  \;=\;
  \frac{
    n!
  }{
    (n-k)!
  }
$$

ways. But if/since order does not matter then all $k!$ [[permutations]] of a sequence of $k$ elements picked count as the same choice, reducing the number of choices to (eq:PlainDefinition).

This perspective shows in particular that the fraction (eq:PlainDefinition) is indeed an [[integer]]; and from this perspective, equation (eq:Symmetry) reflects the FACT that the set of ways to *taking* $k$ items from a set of $n$ is in [[bijection]] to the set of ways of *leaving* $(n-k)$ items in the set.


### Variants

In this vein, one may alternatively ask for the number of ways to choose $k$ items from $n$ items *with possible repetition* (hence now without a bound on $k$) but still irrespective of order.

This question is reduced to the previous one by observing that these choices are in [[bijection]] to the set of [[string (computer science)|strings]] consisting of $k$ stars "$\star$" and $(n-1)$ bars "$\vert$". For instance, for $k = 6$ and $n = 4$, the string

$$
  \star \star \vert \star \vert \vert \star \star \star
$$

represents the choice where the first item is chosen two times, the second item one time, the third item zero times, and the fourth item three times.

But, by the previous discussion, there are

$$
  \left(\binom{n}{k}\right)
  \;\coloneqq\;
  \left(
    {k + n - 1} \atop k
  \right)
  \;=\;
  \left(
    {r + n - 1} \atop n-1
  \right)
$$

such strings (choose $k$ stars, or complementarily $(n-1)$ bars, from $k + (n - 1)$ symbols) and hence as many ways to choose $k$ items from a set of $n$ with possible repetition.

## Related entries

* [[binomial theorem]]

* [[multinomial coefficient]]


## References

See also: 

* Wikipedia: *[Binomial coefficient](https://en.wikipedia.org/wiki/Binomial_coefficient)*

[[!redirects binomial coefficients]]

