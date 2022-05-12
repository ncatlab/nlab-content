+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A [[mathematical structure]] used to define the [[real numbers]] in [[Alfred Tarski]]'s axioms for the [[real numbers]]. 

## Definition ##

A [[Tarski group]] is a [[pointed set|pointed]] [[commutative invertible semigroup]] $(G, +, -, 1)$ with a [[dense linear order]] $\lt$ such that $1 \lt 1 + 1$, $a \lt b + c + a$ implies $a \lt b + a$ or $a \lt c + a$, and $a \lt b$ implies $c + a \lt c + b$. 

As a result, every Tarski group is an [[abelian group]] with [[identity element]] $0 \coloneqq 1 - 1$, and a [[trivial group|nontrivial]] [[ordered group]].

## Tarski's axioms for the real numbers ##

Tarski's axioms for the real numbers are as follows:

* Axiom 5 says that $\mathbb{R}$ is a [[commutative semigroup]]. 

* Axiom 6 with axiom 5 together say that $\mathbb{R}$ is a [[commutative invertible semigroup]]. 

* Axiom 8 says that $\mathbb{R}$ is a [[pointed set]], which with axioms 5 and 6 imply that $\mathbb{R}$ is an [[abelian group]]. 

* Axiom 1 says that $\mathbb{R}$ has a [[connected relation]] $\lt$. 

* Axiom 2 says that $\lt$ is an [[asymmetric relation]] and thus an [[irreflexive relation]]. 

* The fragment of Axiom 4 that only refers to [[singleton]] [[subsets]] says that $\lt$ is a [[comparison]], making $\lt$ into a [[linear order]]. (the full axiom 4 is the [[Dedekind completion|Dedekind completeness]] condition). 

* Axiom 3 says that $\lt$ is a [[dense linear order]].

* Axiom 7 says that for all $a, b, c, d \in G$, $a + b \lt c + d$ implies that $a \lt c$ or $b \lt d$, which imply that $\mathbb{R}$ is a linearly [[ordered group]]. 

* Axiom 9 says that $1 \lt 1 + 1$, which indicates that $\mathbb{R}$ is not [[trivial group|trivial]]. 

## The archimedean field structure on the Dedekind-complete Tarski group ##

Let us denote the Dedekind-complete Tarski group as $\mathbb{R}$. There is an [[archimedean field]] structure on $\mathbb{R}$. 

+-- {: .num_prop} 
###### Proposition
$\mathbb{R}$ is a [[Archimedean group|Archimedean]] [[ordered group|ordered]] [[abelian group]].
=--

+-- {: .proof} 
###### Proof
Since $\mathbb{R}$ is [[Dedekind-complete]] and a strictly ordered abelian group, $\mathbb{R}$ is [[Archimedean group|Archimedean]], because the Dedekind-completion of any totally ordered abelian group with [[infinity|infinite elements]] or [[infinitesimals]] is not an [[abelian group]], and the Dedekind-completion of any Archimedean ordered abelian group is still Archimedean.
=--

+-- {: .num_prop}
###### Proposition
$\mathbb{R}$ has a [[complete metric]]
=--

+-- {: .proof} 
###### Proof
Since $\mathbb{R}$ is strictly ordered, it is a [[totally ordered abelian group]]. As a result, there exist [[maximum]] and [[minimum]] [[binary functions]] $\max:\mathbb{R} \times \mathbb{R} \to \mathbb{R}$ and $\min:\mathbb{R} \times \mathbb{R} \to \mathbb{R}$, with the [[absolute value]] function defined as $\vert x \vert = \max(x, -x)$.

Since $\mathbb{R}$ is [[Dedekind-complete]], Archimedean, and a totally ordered abelian group, $\mathbb{R}$ is a [[metric space]] with respect to the absolute value $\vert x \vert$ and thus a [[Hausdorff space]], and every [[Cauchy net]] in $\mathbb{R}$ [[limit of a net|converges]] to a unique element of $\mathbb{R}$, and thus the absolute value $\vert x \vert$ is a [[complete metric]] on $\mathbb{R}$. 
=--

+-- {: .num_prop}
###### Proposition
$\mathbb{Q}$ embeds in $\mathbb{R}$.
=--

+-- {: .proof} 
###### Proof
Since $\mathbb{R}$ is an [[abelian group]], it is a $\mathbb{Z}$-[[module]], and since $\mathbb{R}$ is totally ordered, it is a [[flat module]] and thus a [[torsion-free abelian group]], which means that the integers $\mathbb{Z}$ [[embedding|embed]] in $\mathbb{R}$, with [[injection|injective]] [[group homomorphism]] $f:\mathbb{Z} \to \mathbb{R}$ where $f(0) = 0$ and $f(1) = 1$. As a result, for every integer $a \in \mathbb{Z}$ and $b \in \mathbb{Z}$ the [[affine function]]s $x \mapsto a x + b$ are well defined in $\mathbb{R}$. 

Since $\mathbb{R}$ is [[Dedekind-complete]], Archimedean, and a totally ordered abelian group, any [[closed interval]] $[a, b]$ on $\mathbb{R}$ is [[compact space|compact]] and [[connected space|conencted]]. Since $\mathbb{R}$ is also a complete metric space, the [[intermediate value theorem]] is satisfied for every function from a closed interval $[a, b]$ to $\mathbb{R}$. Because $x \mapsto a x + b$ are [[monotonic]] for $a \gt 0$, and for $a \lt 0$ the function is just the negation of a monotonic function, $x \mapsto a x + b$ have a [[root of a function|root]] for $\vert a \vert \gt 0$. Thus $\mathbb{R}$ is a [[divisible group]] and a $\mathbb{Q}$-[[vector space]], with an [[injection|injective]] [[group homomorphism]] $f:\mathbb{Q} \to \mathbb{R}$ where $f(0) = 0$ and $f(1) = 1$, and $\mathbb{Q}$ embeds in $\mathbb{R}$.
=--

+-- {: .num_prop}
###### Proposition
$\mathbb{R}$ is a [[commutative ring]].
=--

+-- {: .proof} 
###### Proof
Since every [[Cauchy net]] in $\mathbb{R}$ [[limit of a net|converges]] to a unique element of $\mathbb{R}$, for every directed set $A$ and Cauchy net $(a_i)_{i \in A}$ in the rational numbers, there exists a Cauchy net of [[linear functions]] $(f_i)_{i \in A}$ defined as $f_i(x) = a_i x$. The limit of the Cauchy net $\lim_{i \in A} (f_i)_i$ exists and is a unique function $g(x) = \lim_{i \in A} (a_i)_i x$. Since every real number is the limit of a Cauchy net of rational numbers, there is an $\mathbb{R}$-action $\mu:\mathbb{R} \to (\mathbb{R} \to \mathbb{R})$ which takes a real number $r$ to the linear function $x \mapsto r x$, with $\alpha(1) = x \mapsto x$ being the [[identity function]]. The [[uncurrying]] of $\alpha$ leads to a [[bilinear function]] $(-)(-):\mathbb{R} \times \mathbb{R} \to \mathbb{R}$ called multiplication of the real numbers, defined on the entire domain of the binary function. Since linear functions in the [[function space]] with [[function composition]] and the [[identity function]] is a [[commutative monoid]], $\mathbb{R}$ with multiplication and the multiplicative [[identity element]] $1$ is also [[commutative monoid]], which means that $\mathbb{R}$ is a commutative ring.
=--

+-- {: .num_prop}
###### Proposition
$\mathbb{R}$ is a [[field]]
=--

+-- {: .proof} 
###### Proof
Since $\mathbb{R}$ is a commutative ring, [[power series]] are well defined, and because all Cauchy nets converge in $\mathbb{R}$, all Cauchy sequences and all Cauchy power series converge in $\mathbb{R}$. In particular, every [[geometric series]] is a Cauchy power series and the limit of the geometric series 
$$\sum_{n=0}^\infty x^n$$ 
and 
$$\sum_{n=0}^\infty (-1)^n x^n$$
[[limit of a sequence|converges]] in the [[open interval]] $(-1, 1)$. Thus let us define functions $f:(-1, 1) \to \mathbb{R}$ and $g:(-1, 1) \to \mathbb{R}$ as 

$$f(x) := \sum_{n=0}^\infty x^n$$

$$g(x) := \sum_{n=0}^\infty (-1)^n x^n$$

Let us define the function

$$h(x, a) := (-a) \sum_{n=0}^\infty a^n (x + f(a + 1))^n$$

for $a \lt 0$ and

$$k(x, a) := a \sum_{n=0}^\infty (-a)^n (x + g(a - 1))^n$$

for $a \gt 0$. These are functions which converge on the open interval $(1/a, 0)$for $h(x, a)$ and $(0,1/a)$ for $k(x, a)$, and satisfy the identity $h(x, a) x = 1$ for all $a \lt 0$ and $x \in (1/a, 0)$, and $k(x, a) x = 1$ for all $a \gt 0$ and $x \in (0,1/a)$, by definition of the geometric series. 

The [[reciprocal]] is piecewise defined as 
$$
\frac{1}{x} =
\begin{cases}
\lim_{a \to 0^-} h(x, a)  & \mathrm{if}\ x \lt 0 \\
\lim_{a \to 0^+} k(x, a)  & \mathrm{if}\ x \gt 0 \\
\end{cases}
$$

As [[algebraic limit theorem|limits preserve multiplication]], $\frac{1}{x} x = 1$ for all $x \in \mathbb{R}$. Thus, $\mathbb{R}$ is a field.
=--

## See also ##

* [[abelian group]]

* [[commutative invertible semigroup]]

* [[pointed set]]

* [[dense linear order]]

* [[ordered group]]

* [[real numbers]]

## References ##

* [[Alfred Tarski]],  *Introduction to Logic and to the Methodology of Deductive Sciences* (4th edition). Oxford University Press. (1994) $[$[doi:10.2307/2180610](https://doi.org/10.2307/2180610), ISBN 978-0-19-504472-0$]$

* Ucsnay, Stefanie (Jan 2008), A Note on Tarski's Note. The American Mathematical Monthly, Vol 115 No. 1, pg 66–68. JSTOR 27642393

[[!redirects Tarski groups]]

[[!redirects Tarski real numbers]]
[[!redirects Tarski's axioms for the real numbers]]
[[!redirects Tarski's axiomatization of the real numbers]]
[[!redirects Tarski's axiomatisation of the real numbers]]