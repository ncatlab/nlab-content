
#Contents#
* table of contents
{:toc}

## Definition

For $k$ a [[natural number]] and $x$ an element of a (unital) [[ring]], the **falling factorial** or **falling power** $x^{\underline{k}}$ (also sometimes written $(x)_k$) is defined by

$$x^{\underline{k}} = x(x-1)\ldots (x-k+1).$$ 

If $X$ and $Y$ are two [[finite sets]] of [[cardinalities]] $|X| = k$ and $|Y| = n$, then the falling factorial $n^{\underline{k}}$ counts the number of [[injections]] from $X$ to $Y$. Dividing by the action of the permutation group of $X$ with $k!$ elements and counting the orbits, the so called **binomial coefficient** $\frac{n^{\underline{k}}}{k!} = \binom{n}{k}$ counts the number of subsets of $Y$ of cardinality $k$. 



## Properties 

In the calculus of finite differences, where an analogy is set up between the ordinary "continuous" derivative $(D f)(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$ and the "discrete" derivative (= difference operator) 

$$(\Delta f)(x) \coloneqq f(x+1) - f(x),$$ 

it is the falling factorial $x^{\underline{k}}$ that plays a role analogous to the ordinary power $x^k$. For example, we have $\Delta x^{\underline{k}} = k x^{\underline{k-1}}$. Compare the formula $\Delta \frac{x^{\underline{k}}}{k!} = \frac{x^{\underline{k-1}}}{(k-1)!}$ which interpolates the Pascal triangle recurrence 

$$\binom{n+1}{k} - \binom{n}{k} = \binom{n-1}{k}.$$ 

The discrete analogue of the identity $x^k x^l = x^{k+l}$ is the identity 

$$x^{\underline{k}} (x-k)^{\underline{l}} = x^{\underline{k+l}}.$$ 

This may be used to motivate the definition of $x^{\underline{k}}$ for all [[integers]] $k$. For $k$ a natural number, define 

$$x^{\underline{-k}} \coloneqq \frac1{(x+k)^{\underline{k}}} = \frac1{(x+k)(x+k-1) \ldots (x+1)}.$$ 

Then the difference formula $\Delta x^{\underline{k}} = k x^{\underline{k-1}}$ and the multiplicative identity $x^{\underline{k}} (x-k)^{\underline{l}} = x^{\underline{k+l}}$ continue to hold for all integers $k, l$. These facts have numerous applications throughout discrete mathematics. 

## Related entries 

* [[factorial]]

* [[binomial theorem]] 

## References

* [Falling Factorial](http://mathworld.wolfram.com/FallingFactorial.html) on Wolfram MathWorld. 

* Ronald Graham, Donald Knuth, and Oren Patashnik, _Concrete Mathematics_, 2$^{nd}$ edition, Addison-Wesley (1994). 

[[!redirects falling power]]
[[!redirects falling powers]]
[[!redirects falling factorials]]

