+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Talk about the decimal number system for integers and decimal fractions, and then infinite sequences of decimals as a [[terminal coalgebra for an endofunctor]].

## Natural numbers

### As a free monoid

Define a set of digits $D$, and the [[free monoid]] $D^*$ on $D$ with unit $\epsilon$, quotiented by an equivalence relation. Then define a function $s$ on $D^*$ such that $D^*,\epsilon,s$ is a [[natural numbers object]]. 

### As a rig

$$\mathbb{N} \cong \mathbb{N}[10] \coloneq \mathbb{N}[x]/(x=10)$$

## Finite decimals

Localisation of the [[rig]] of natural numbers at 10 $\mathbb{N}[1/10]$, finite decimals as canonical representatives of $\mathbb{N}[1/10]$, and then [[group completion]] of the additive monoid to $\mathbb{Z}[1/10]$.

## Infinite decimals

### As an terminal coalgebra

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

Let $(\mathbb{Z},0,s,n,\lt)$ be the set of integers, the initial set with an element $0$, a [[linear order]] $\lt$, a [[monotone]] $s$ such that $a \lt s(a)$ for all $a \in \mathbb{Z}$, and an [[antitone]] $n$ such that $n(0)=0$ and $n = s \circ n \circ s$. Let $\mathbb{R}$ be a set with a structure preserving function $g:\mathbb{Z}\to\mathbb{R}$ and a [[monotone]] $f:[0,1]\to \mathbb{R}$ such that $f(0) = g(0)$ and $f(1) = s(g(0))$. The set $\mathbb{R}$ of [[real numbers]] is the initial such system. The arithmetic operations on any such system can be defined by the properties of the [[function algebra]] of $\mathbb{R}$ and [[currying]]. 

### As a $\mathbb{Z}$-graded cochain complex of abelian groups

Let $\mathbb{Z}/10\mathbb{Z}$ be the [[cyclic group]] consisting of 10 elements, and let $C_\bullet$ be a [[chain complex]] of [[abelian groups]] consisting of a sequence of $\mathbb{Z}/10\mathbb{Z}$ indexed by $\mathbb{Z}$. The indices $i:\mathbb{Z}$ are called __place values__, and $i$-[[cochains]] are called __digits__. 

A __10-adic number__ is a cochain such that $c_i = 0$ for all $i \lt j$ or $c_i = 9$ for all $i \lt j$ for $i,j:\mathbb{Z}$. A __10-adic integer__ is a cochain such that $c_i = 0$ for all $i \lt 0$ or $c_ i = 9$ for all $i \lt 0$.

A cyclic group $G$ has a canonical [[cyclic order]] $[(-),(-),(-)]:(G \times G \times G) \to \Omega$. We define the cyclic order on $\mathbb{Z}/10\mathbb{Z}$ such that $[0,n,1]$ is false for all $n:\mathbb{Z}/10\mathbb{Z}$. 

For each $i:\mathbb{Z}$, there exists a [[cocycle]] $f_i: (C_i \times C_i) \to C_{i + 1}$ called the __digitwise carry__ function at place value $i$, defined such that for all $a,b:C_i$, $f_i(a,b) = 0$ if $[a,0,a+b]$ is false, and $f_i(a,b) = 1$ if $[a,0,a+b]$ is true.

We define the __addition without carry__ on the cochain complex $(-)\oplus(-): (C_\bullet \times C_\bullet) \to C_\bullet$ as the addition of all digits using the abelian group operation, and we define the __carry__ $carry: (C_\bullet \times C_\bullet) \to C_\bullet$ as the digitwise carry of all digits. Then, __addition__ $(-)+(-): (C_\bullet \times C_\bullet) \to C_\bullet$ is defined [[recursion|recursively]] as $a+b = (a\oplus b)+carry(a,b)$. 

The cochains consisting of all $n$s for all $n:\mathbb{Z}/10\mathbb{Z}$ are additive [[identity elements]] of the addition operation defined above. As such, they are algebraically equal to the same chain $0$ __zero__, the chain consisting of all zeroes. We define __negation__ $-(-): C_\bullet \to C_\bullet$ such that for all chains $c:C_\bullet$, the digits in $-c$ are $(-c)_i = 9 + -c_i$. As a result, the chain complex itself is an abelian group, and the subset of $C_\bullet$. $C_\bullet$ also forms a [[cyclic group]], so a cyclic order could be put on $C_\bullet$. 

Let us define an $\mathbb{N}$-[[action]] $act: (\mathbb{N}^+\times C_\bullet) \to C_\bullet$ such that $act(0,0) = 0$ and $act(n + 1,c) = act(n,c) + c$ for all $n:\mathbb{N}^+$ and $c:C_\bullet$. This represents the $n$-fold sum of a cochain $c$. The [[archimedean property]] for cyclic orders then states that for all $a,b:C_\bullet$, there exist $n:\mathbb{N}^+$ such that $[0, a, act(n,b)]$ or $[act(n,b),a,0]$. Let $1$ __one__ denote the cochain with all digits equal to zero except at place value $0$, where the digit is equal to $1$. Then the __real numbers__ $\mathbb{R}$ is the largest abelian subgroup of $C_\bullet$ that contains $1$ and is archimedean. A __decimal rational__ is a real 10-adic number, and an __integer__ is a real 10-adic integer. 

One could also establish a [[ring]] structure on $\mathbb{Z}/10\mathbb{Z}$ and construct a multiplication operation on the chain complex such that when restricted to real numbers yields multiplication of real numbers. The chain complex itself with the defined multiplication should be equivalent to the [[quotient ring]] of the [[Laurent series]] $\mathbb{Z}[[x,x^{-1}]]/(x-10)\mathbb{Z}[[x,x^{-1}]]$. 

## Related concepts

* [[decimal rational number]]

## References

* Wikipedia, _[Decimal](https://en.wikipedia.org/wiki/Decimal)_

* Wikipedia, _[Decimal representation](https://en.wikipedia.org/wiki/Decimal_representation)_

[[!redirects decimal numbers]]