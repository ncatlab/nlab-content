

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

A weaker notion of [[integral domain]] which allows for some [[zero divisors]], but for which one may [[quotient ring|quotient out]] the zero divisors to obtain an [[integral domain]]. 

"Approximate integral domain" is a placeholder name for a concept which may or may not have another name in the mathematics literature. The idea however is that approximate integral domains are to integral domains as [[local rings]] are to [[Heyting fields]], and as [[weak local rings]] are to [[weak Heyting fields]]. 

## Definition

An **approximate integral domain** is a [[commutative ring]] $R$ such that:

* $R$ is nontrivial ($0 \ne 1$); and

* The [[zero divisors]] form an [[ideal]]. (equivalently, the non-[[cancellative elements]] form an [[ideal]]). 

Thus, the [[quotient ring|quotient]] of an approximate integral domain by its [[ideal]] of [[zero divisors]] is an [[integral domain]]. 

Every approximate integral domain has an [[equivalence relation]] $\approx$, defined as $x \approx y$ if and only if $x - y$ is a [[zero divisor]]. Hence the name "approximate" integral domain. Then [[integral domains]] are precisely the approximate integral domains for which $\approx$ implies [[equality]]. 

## In constructive mathematics

In constructive mathematics, similar to the notion of [[local ring]], [[integral domain]], and [[field]], the notion of approximate integral domain bifurcates into multiple distinct notions:

A **weak approximate integral domain** is an approximate integral domain defined as above. 

Recall that a [[cancellative element]] in a commutative ring $R$ is an element $a \in R$ for which both left and right multiplication by $a$ is an injection, and [[zero divisors]] are precisely the elements in $R$ which are not cancellative. 

A **strict approximate integral domain** is a weak approximate integral domain for which additionally the cancellative elements form an [[anti-ideal]]:

* $0$ is not cancellative;
* if $a + b$ is cancellative, then either $a$ is cancellative or $b$ is cancellative;
* if $a \cdot b$ is cancellative, then $a$ is cancellative and $b$ is cancellative (this is trivially true in any commutative ring).

The [[quotient object|quotient ring]] of a strict approximate integral domain by its anti-ideal of cancellative elements is a [[Heyting integral domain]].

One can define an [[apartness relation]] in any strict approximate integral domain: $x \# y$ iff $x - y$ is cancellative. Then the local ring is a Heyting field if and only if this apartness relation is [[tight relation|tight]].

+-- {: .num_prop #internal} 
###### Proposition 
The addition and multiplication operations on a strict approximate integral domain $R$ are strongly extensional with respect to the canonical apartness relation $\#$ defined by $x \# y$ iff $x - y$ is cancellative. In this way a strict approximate integral domain becomes an internal [[ring object]] in the category $Apart$, consisting of sets with apartness relations and maps (strongly extensional functions) between them. 
=-- 

+-- {: .proof} 
###### Proof 
Recall that products $X \times Y$ in the category of sets with apartness relations is the cartesian product of the underlying sets equipped with the apartness relation defined by $(x, y) \# (x', y')$ iff $x \# x'$ in $X$ *or* $y \# y'$ in $Y$. Recall also that a function $f: X \to Y$ between sets with apartness relations is *strongly extensional* if $f(x) \# f(y)$ implies $x \# y$. 

For addition, if $(x + y) \# (x' + y')$, then $x + y - (x' + y') = (x - x') + (y - y')$ is cancellative, so $x - x'$ or $y - y'$ is cancellative since $R$ is a strict approximate integral domain, whence $(x, y) # (x', y')$. Thus addition is strongly extensional. 

For multiplication, if $x y # x' y'$, then $x y - x' y'$ is cancellative. Write $x y - x' y' = (x - x')y + x'(y - y')$. Since $R$ is a strict approximate integral domain, either $(x - x')y$ is a cancellative element or $x'(y - y')$ is a cancellative element. From this we easily conclude $x - x'$ is a cancellative element or $y - y'$ is, since cancellative elements are closed under multiplicaiton, whence $(x, y) # (x', y')$. So multiplication is also strongly extensional. 
=-- 

\begin{theorem}
For a strict approximate integral domain, the [[ring of fractions]] obtained by inverting the cancellative elements is a [[local ring]]. 
\end{theorem}

## Examples and non-examples

* The [[integers]] are an approximate integral domain which are an [[integral domain]]. 

* The [[dual numbers|dual]] integers $\mathbb{Z}[\epsilon]/\epsilon^2$ is an approximate integral domain where the [[nilpotent]] [[infinitesimal]] $\epsilon \in \mathbb{Z}[\epsilon]/\epsilon^2$ is a non-[[zero]] [[zero divisor]]. 

* For any [[prime number]] $p$ and any [[positive number|positive]] [[natural number]] $n$, the [[prime power local ring]] $\mathbb{Z}/p^n\mathbb{Z}$ is an approximate integral domain, whose [[ideal]] of [[zero divisors]] is the ideal $p(\mathbb{Z}/p^n\mathbb{Z})$. The quotient of $\mathbb{Z}/p^n\mathbb{Z}$ by its ideal of [[zero divisors]] is the [[finite field]] $\mathbb{Z}/p\mathbb{Z}$, indicating that it is also a [[weak local ring]]. 

* There exist commutative rings which are not approximate integral domains. For example, the [[integers modulo]] 6 $\mathbb{Z}/6\mathbb{Z}$ is not an approximate integral domain, because $3$ and $4$ are both zero divisors, but $3 + 4$ is cancellative. When one tries to quotient out the zero divisors, the resulting ring is [[trivial ring|trivial]]. 

## See also

* [[integral domain]]

* [[ordered integral domain]]

* [[weak local ring]]

* [[local ring]]

[[!redirects approximate integral domain]] 
[[!redirects approximate integral domains]] 

[[!redirects weak approximate integral domain]] 
[[!redirects weak approximate integral domains]] 

[[!redirects strict approximate integral domain]] 
[[!redirects strict approximate integral domains]] 