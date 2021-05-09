## Idea

Talk about the decimal number system for integers and decimal fractions, and then infinite sequences of decimals as a [[terminal coalgebra for an endofunctor]].

## Integers

Define a set of digits $D$, and the [[free monoid]] $D^*$ on $D$ with unit $\epsilon$, quotiented by an equivalence relation. Then define a function $s$ on $D^*$ such that $D^*,\epsilon,s$ is a [[natural numbers object]]. Define addition and multiplication in the usual way, prove that  $D^*$ with addition and multiplication form a commutative [[rig]], and then group complete the additive monoid of $\mathbb{N}$ to $\mathbb{Z}$

## Finite decimals

Localisation of the [[rig]] of natural numbers at 10 $\mathbb{N}[1/10]$, finite decimals as canonical representatives of $\mathbb{N}[1/10]$, and then [[group completion]] of the additive monoid to $\mathbb{Z}[1/10]$.

## Infinite decimals and real numbers

Consider the [[category]] of [[intervals]] $Int$, i.e., linearly ordered sets with identified elements $1$ and $0$, and let 

$$F: Int \to Int$$ 

be the endofunctor which takes an interval $X$ to $\bigvee_{0 \leq i \lt 10} X$, the the interval obtained by taking ten copies of $X$ and identifying the $1$ of the $(i-1)$-th copy with the $0$ of the $i$-th copy, for $0 \lt i \lt 10$. The real interval $[0, 1]$ becomes a coalgebra if we identify $\bigvee_{0 \leq i \lt 10} X$ with $[0, 10]$ and consider the multiplication-by-10 map $[0, 1] \to [0, 10]$ as giving a coalgebra structure. 

+-- {: .num_theorem} 
######Theorem 
The interval $[0, 1]$ is terminal in the category of such coalgebras. 
=-- 

+-- {: .proof} 
######Proof (sketch) 
Given any coalgebra structure $f: X \to \bigvee_{0 \leq i \lt 10} X$, any value $f(x)$ lands either in the $n$-th tenth (the $n$-th $X$ in $\bigvee_{0 \leq i \lt 10} X$) for $0\lt n \leq 10$, or at the precise spot between them, where the $1$ in the $n$-th copy is glued to the $0$ in the $(n+1)$-th for $0\lt n \lt 10$. Intuitively, one could think of a coalgebra structure $\theta: X \to \bigvee_{0 \leq i \lt 10}$ as giving an automaton where on input $x_0$ there is output of the form $(x_1, h_1)$, where $h_1$ is one of 19 states, "0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "either 0 or 1", "either 1 or 2", "either 2 or 3", "either 3 or 4", "either 4 or 5", "either 5 or 6", "either 6 or 7", "either 7 or 8", and "either 8 or 9". By iteration, this generates a behavior stream $(x_n, h_n)$. Let "0", "1", "2", "3", "4", "5", "6", "7", "8", and "9" be decimal digits $D$, the $h_n$ form a decimal expansion to give a number between 0 and 1, and therefore we have an interval map $X \to [0, 1]$ which sends $x_0$ to that number. Of course, if $h_n$ is ever one of the "either $d_l$ or $d_u$" states, for $d_l,d_u:D$ we have a choice to resolve it as either $(1_X, d_l)$ or $(0_X, d_u)$ and continue the stream, but these streams are identified, and this corresponds to the identifications of decimal expansions 

$$h_1... h_{n-1} 100000... = .h_1... h_{n-1}099999...$$ 

$$h_1... h_{n-1} 200000... = .h_1... h_{n-1}199999...$$ 

$$h_1... h_{n-1} 300000... = .h_1... h_{n-1}299999...$$ 

$$h_1... h_{n-1} 400000... = .h_1... h_{n-1}399999...$$ 

$$h_1... h_{n-1} 500000... = .h_1... h_{n-1}499999...$$ 

$$h_1... h_{n-1} 600000... = .h_1... h_{n-1}599999...$$ 

$$h_1... h_{n-1} 700000... = .h_1... h_{n-1}699999...$$ 

$$h_1... h_{n-1} 800000... = .h_1... h_{n-1}799999...$$ 

$$h_1... h_{n-1} 900000... = .h_1... h_{n-1}899999...$$ 

as real numbers. In this way, we produce a unique well-defined interval map $X \to [0, 1]$, so that $[0, 1]$ is the terminal coalgebra. 
=--

The non-negative real numbers $\mathbb{R}^{\geq 0}$ is defined as 

$\mathbb{R}^{\geq 0} \cong \mathbb{N} \times [0,1]$

with $\lt$ defined as $(n,p) \lt (m,q)$ if $n + 1 \lt m$, $(n,p) \lt ((n+1),q)$ if $p \neq 99999...$ and $q \neq 00000...$, and

$$(n,99999...) = ((n+1),00000...)$$ 

for all $n,m:N$, $p,q:[0,1]$.

The linear order of real numbers $\mathbb{R}$ is defined as 

$$\mathbb{R} \cong (\mathbb{R}^{\geq 0})^{\op} + \mathbb{R}^{\geq 0}$$ 

with coproduct monomorphisms $+:\mathbb{R}^{\geq 0} \to \mathbb{R}$ and $-:(\mathbb{R}^{\geq 0})^{\op} \to \mathbb{R}$, such that $-p \lt +p$ for all $p:\mathbb{R}^{\geq 0}, p \neq 0,00000....$, and $-0,00000... = +0,00000...$.

To do: prove that $\mathbb{Z}[1/10]$ are embedded in the reals, define addition and a metric on $\mathbb{R}$, prove that $\mathbb{R}$ is an [[archimedean group]] and prove that the [[Cauchy complete category|Cauchy completion]] of $\mathbb{Z}[1/10]$ is embedded in $\mathbb{R}$. 

## Related concepts

* [[decimal rational number]]

## References

* Wikipedia, _[Decimal](https://en.wikipedia.org/wiki/Decimal)_

* Wikipedia, _[Decimal representation](https://en.wikipedia.org/wiki/Decimal_representation)_

[[!redirects decimal numbers]]