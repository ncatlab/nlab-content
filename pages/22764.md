+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The idea of a closed midpoint algebra comes from [[Peter Freyd]]. 

## Definition

A __closed midpoint algebra__ is a [[cancellative midpoint algebra]] $(M,\vert)$ with two elements $\bot:M$ and $\top:M$. 

## Examples

The [[unit interval]] with $a \vert b \coloneqq \frac{a + b}{2}$, $\bot = 0$, and $\top = 1$ is an example of a closed midpoint algebra. 

The set of truth values in Girard's [[linear logic]] is a closed midpoint algebra. 

## Properties

Every closed midpoint algebra with $\bot = \top$ is [[trivial object|trivial]]. 

### Partial order

Every closed midpoint algebra has a natural [[partial order]] defined as $a \leq b$ for elements $a$ and $b$ in $M$ if there exists $c$ in $M$ such that $a \vert \top = b \vert c$. Dually, $a \leq b$ for elements $a$ and $b$ in $M$ if there exists $c$ in $M$ such that $c \vert a = \bot \vert b$.

Every closed midpoint algebra [[homomorphism]] is a [[monotone]]. 

### Function algebras

For any set $S$ and any closed midpoint algebra $M$, the set of functions from $S$ to $M$ is a closed midpoint algebra $(S\to M,\vert_{S\to M},\bot_{S\to M},\top_{S\to M})$, defined by 

* $(f\vert_{S\to M} g)(x) = f(x)\vert_M g(x)$ for all $f,g:S\to M$ and $x:M$

* $(\bot_{S\to M})(x) = \bot_M$ for all $x:M$

* $(\top_{S\to M})(x) = \top_M$ for all $x:M$

### Definite integration

Let $M$ and $N$ be [[continuous space|continuous]] closed midpoint algebras and let $M\to_C N$ be the space of [[continuous functions]] from $M$ to $N$. Then there exists an [[operator]] $\int (-)(x) \mathrm{d}x: (M\to_C N)\to (M\to_C N)$ called __[[definite integration]]__ such that

$$\int \top_{M\to N}(x) \mathrm{d}x = \top_N$$

$$\int \bot_{M\to N}(x) \mathrm{d}x = \bot_N$$

$$\int f(x) \vert_N g(x) \mathrm{d}x = \int f(x) \mathrm{d}x \vert_N \int g(x) \mathrm{d}x$$

$$\int f(x) \mathrm{d}x = \int f(\bot_M \vert_M x) \mathrm{d}x \vert_N \int f(x \vert_M \top_M) \mathrm{d}x$$

for all $x$ in $M$.

When $M$ is the [[unit interval]] on the [[real numbers]] $[0,1]$, and $N$ is an interval $[a,b]$ on the real numbers, written in conventional notation the axioms become: 

$$\int_{0}^{1} a(x) \mathrm{d}x = a$$

$$\int_{0}^{1} b(x) \mathrm{d}x = b$$

$$\int_{0}^{1} \frac{f(x) + g(x)}{2} \mathrm{d}x = \frac{\int_{0}^{1} f(x) \mathrm{d}x + \int_{0}^{1} g(x) \mathrm{d}x}{2}$$

$$\int_{0}^{1} f(x) \mathrm{d}x = \frac{\int_{0}^{1} f(\frac{0 + x}{2}) \mathrm{d}x + \int_{0}^{1} f(\frac{x + 1}{2}) \mathrm{d}x}{2}$$

## Related concepts

* [[definite integration]]

* [[cancellative midpoint algebra]]

* [[symmetric closed midpoint algebra]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))


