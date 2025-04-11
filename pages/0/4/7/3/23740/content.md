> This entry is about regular elements in [[ring theory]] and [[commutative algebra]]. For regular elements in [[formal logic]] and [[topology]], see [[regular element]]. For regular elements in [[physics]]/[[quantum field theory]] see at _[[regularization (physics)]]_. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given a [[commutative ring]] $R$, an [[element]] $e \in R$ is *left cancellative* or *left regular* if $e \cdot a = e \cdot b$ for all $a \in R$ and $b \in R$, then $a = b$. 

$$\mathrm{isLeftCancellative}(e) \coloneqq \forall a,b \in R.(e \cdot a = e \cdot b) \implies (a = b)$$

An element $e \in R$ is *right cancellative* or *right regular* if $a \cdot e = b \cdot e$ for all $a \in R$ and $b \in R$, then $a = b$. 

$$\mathrm{isRightCancellative}(e) \coloneqq \forall a,b \in M.(a \cdot e = b \cdot e) \implies (a = b)$$

An element $e \in R$ is *cancellative* or *regular* if it is both left cancellative and right cancellative.

$$\mathrm{isCancellative}(e) \coloneqq \mathrm{isLeftCancellative}(e) \wedge \mathrm{isRightCancellative}(e)$$

## Multiplicative subset of cancellative elements ##

The **multiplicative subset of cancellative elements** in $R$ is the [[multiplicative subset]] of all cancellative elements in $R$

$$\mathrm{Can}(R) \coloneqq \{e \in M \vert \mathrm{isCancellative}(e)\}$$

The term 'cancellative element' could be replaced with the synonym 'regular element'. If the synonym 'regular element' is used in place of 'cancellative element', such as in [Lombardi & Quitté 2010](#LombardiQuitté2010), then this multiplicative subset is typically written as $\mathrm{Reg}(R)$. 

This is also called the **[[filter of a ring|filter]] of regular elements** in $R$, as in [Lombardi & Quitté 2010](#LombardiQuitté2010). Similarly as above, 'regular element' could be replaced with 'cancellative element'. 

Since the multiplicative identity element $1$ is always cancellative, the multiplicative subset of all cancellative elements forms a [[cancellative monoid]]. 

## Properties ##

\begin{proposition}
For a commutative ring $R$, given elements $a, b \in R$, if the product $a \cdot b$ is cancellative, then both $a$ and $b$ are cancellative. 
\end{proposition} 

By this proposition, a commutative ring $R$ is a [[approximate integral domain|strict approximate integral domain]] if the following condition holds: 

* For all elements $a, b \in R$, if the $a + b$ is cancellative, then either $a$ is cancellative or $b$ is cancellative. 

\begin{theorem}
For a [[approximate integral domain|strict approximate integral domain]] $R$, the addition and multiplication operations on $R$ are strongly extensional with respect to the canonical apartness relation $\#$ defined by $x \# y$ iff $x - y$ is cancellative.

In this way $R$ becomes an internal commutative [[ring object]] in the category $\mathrm{Apart}$, consisting of sets with apartness relations and maps (strongly extensional functions) between them.
\end{theorem}

\begin{proof}
Recall that products $X \times Y$ in the category of sets with apartness relations is the cartesian product of the underlying sets equipped with the apartness relation defined by $(x, y) \# (x', y')$ iff $x \# x'$ in $X$ *or* $y \# y'$ in $Y$. Recall also that a function $f: X \to Y$ between sets with apartness relations is *strongly extensional* if $f(x) \# f(y)$ implies $x \# y$. 

For addition, for all elements $a \in R$, $b \in R$, $a' \in R$, $b' \in R$, if $(a + b) \# (a' + b')$, then $a + b - (a' + b') = (a - b') + (a - b')$ is cancellative, so $a - a'$ or $b - b'$ is cancellative since for all elements $a \in R$ and $b \in R$, if the sum $a + b$ is cancellative, then either $a$ is cancellative or $b$ is cancellative, whence $(a, b) # (a', b')$. Thus addition is strongly extensional. 

For multiplication, for all elements $a \in R$, $b \in R$, $a' \in R$, $b' \in R$, if $a \cdot b # a' \cdot b'$, then $a \cdot b - a' \cdot b'$ is cancellative. Write $a \cdot b - a' \cdot b' = (a - a') \cdot b + a' \cdot (b - b')$. Since for all elements $a \in R$ and $b \in R$, if the sum $a + b$ is cancellative, then either $a$ is cancellative or $b$ is cancellative, either $(a - a') \cdot b$ is cancellative or $a' \cdot (b - b')$ is cancellative. Since for all elements $a \in R$ and $b \in R$, if $a \cdot b$ is cancellative, then $a$ is cancellative and $b$ is cancellative, either $a - a'$ is cancellative or $b - b'$ is, whence $(a, b) # (a', b')$. So multiplication is also strongly extensional. 
\end{proof}

### Relation with zero-divisors ###

\begin{theorem}
Given a commutative ring $R$, if an element $e \in R$ is a cancellative element, then it is a non-[[zero-divisor]], where non-zero-divisor is defined as an element $a \in R$ such that for every element $b:R$, $b \cdot a = 0$ or $a \cdot b = 0$ implies that $b = 0$. 
\end{theorem}

\begin{proof}
Suppose that $e \in R$ is cancellative. This means that for all elements $a \in R$ and $b \in R$, $a \cdot e = b \cdot e$ implies that $a = b$ and $e \cdot a = e \cdot b$ implies that $a = b$. For the first equation, subtracting $b \cdot e$ from both sides of the equation leads to $(a - b) \cdot e = 0$, and for the second equation, subtraction $e \cdot b$ from both sides of the equation leads to $e \cdot (a - b) = 0$. Subtracting $b$ from both sides of $a = b$ leads to $a - b = 0$. Defining the element $c = a - b$ results in the condition that for every element $c \in R$, $c \cdot e = 0$ implies that $c = 0$ and $e \cdot c = 0$ implies that $c = 0$, which implies that $e$ is a non-[[zero-divisor]]. 
\end{proof}

\begin{theorem}
Given a commutative ring $R$, if an element $e \in R$ is a non-zero-divisor, then it is cancellative. 
\end{theorem}

\begin{proof}
Suppose that $e \in R$ is a non-zero-divisor. This means that for every element $c \in R$, $c \cdot e = 0$ or $e \cdot c = 0$ implies that $c = 0$. However, since $R$ is a commutative ring, if $c \cdot e = 0$, then $e \cdot c = 0$, so the statement $c \cdot e = 0$ or $e \cdot c = 0$ implies that $c = 0$ implies the statement that $c \cdot e = 0$ implies that $c = 0$ and $e \cdot c = 0$ implies that $c = 0$. Since $R$ is an [[abelian group]], by definition of an abelian group, the [[image]] of the binary subtraction function $a - b$ is $R$ itself, and thus, one could replace $c$ with $a - b$ for elements $a \in R$ and $b \in R$, resulting in the statement that $(a - b) \cdot e = 0$ implies that $(a - b) = 0$ and $e \cdot (a - b) = 0$ implies that $(a - b) = 0$. Adding $b \cdot e$ to each side of the first equation, $e \cdot b$ to each side of the second equation, and $b$ to each side fo the third equation leads to the statement that $a \cdot e = b \cdot e$ implies that $a = b$ and $e \cdot a = e \cdot b$ implies that $a = b$, which is precisely the definition of cancellative element. Thus, every non-zero-divisor is a cancellative element. 
\end{proof}

Thus, we have established that cancellative elements and non-zero-divisors are the same thing in a commutative ring. However, the proof relies on the [[abelian group]] structure of commutative rings, and this property does not necessarily hold in other algebraic structures where the concepts of cancellative element and non-zero-divisor make sense, such as in [[rigs]] or [[absorption monoids]]. 

Since a [[zero-divisor]] is defined in the nLab as not being a non-zero-divisor, 

\begin{theorem}
In a commutative ring $R$, an element $e \in R$ is a [[zero-divisor]] if and only if it is non-cancellative
$$\mathrm{isZeroDivisor}(e) \iff \neg \mathrm{isCancellative}(e)$$
\end{theorem}

### Integral domains ###

The theorems relating cancellative elements to zero-divisors provide alternative definition of the various (commutative) [[integral domains]] in constructive mathematics in terms of cancellative elements, in analogy with the definition of [[fields]] in terms of invertible elements:

\begin{definition}
A commutative ring $R$ is a **integral domain** if an element is non-cancellative (or equivalently, a zero-divisor) iff it is zero. In addition to $0\neq 1$, this condition means that every non-cancellative element (or equivalenty, zero-divisor) is zero.
\end{definition}

\begin{definition}
A commutative ring $R$ is a **Heyting integral domain** if it is an integral domain and additionally, for all elements $a \in R$ and $b \in R$, if the sum $a + b$ is cancellative, then either $a$ is cancellative or $b$ is cancellative. 
\end{definition}

\begin{theorem}
In addition to $0 \# 1$, the above condition in a Heyting integral domain then means that every element apart from $0$ is cancellative.
\end{theorem}

\begin{definition}
A commutative ring $R$ is a **discrete integral domain** if all elements $e \in R$ are cancellative [[xor]] equal to zero. This condition means that every element is either $0$ or cancellative, and it also implies that $0 \neq 1$.
\end{definition}

### Fields ###

Given the above definitions of an integral domain, a [[field]] could be defined as an integral domain where every cancellative element is a [[unit]], or equivalently, an integral domain whose multiplicative subset of cancellative elements is the group of units. 

### Ring of fractions ###

For every commutative ring $R$, the [[ring of fractions]] is defined in [Quinn2009](#Quinn2009) to be the [[localization of a commutative ring|localization]] of $R$ at the multiplicative subset of cancellative elements, $R[\mathrm{Can}(R)^{-1}]$. This is similar to the [[Grothendieck group]] construction of a general [[cancellative monoid]]: the multiplicative subset of cancellative elements in $R[\mathrm{Can}(R)^{-1}]$ is the [[group of units]] $R[\mathrm{Can}(R)^{-1}]^\times$ in $R[\mathrm{Can}(R)^{-1}]$. 

If $R$ is an [[integral domain]], then $R[\mathrm{Can}(R)^{-1}]$ is the [[field of fractions]] of $R$. 

### Unique factorization domains ###

In [Lombardi & Quitté 2010](#LombardiQuitté2010), a [[unique factorization domain]] is defined as a [[GCD domain]] $R$ for which the [[quotient object|quotient]] monoid of the multiplicative subset of cancellative elements by the group of units $\mathrm{Can}(R)/R^\times$ admits a complete factorization. 

## See also ##

* [[multiplicative subset]]

* [[filter of a ring]]

* [[cancellative monoid]]

* [[integral domain]]

* [[ring of fractions]]

* [[field of fractions]]

* [[group of units]]

* [[field]]

* [[torsion-free module]]

* [[GCD ring]]

* [[prefield ring]]

* [[quasiregular element]]

## References

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* {#Quinn2009} [[Frank Quinn]], *Proof Projects for Teachers* (2009) &lbrack;[pdf](https://personal.math.vt.edu/fquinn/education/pfs4teachers0.pdf), [[Quinn-ProofProjects.pdf:file]]&rbrack;


[[!redirects cancellative element]]
[[!redirects cancellative elements]]

[[!redirects cancellative element of a commutative ring]]
[[!redirects cancellative elements of a commutative ring]]
[[!redirects regular element of a commutative ring]]
[[!redirects regular elements of a commutative ring]]

[[!redirects multiplicative subset of cancellative elements]]
[[!redirects multiplicative subsets of cancellative elements]]
[[!redirects multiplicative subset of regular elements]]
[[!redirects multiplicative subsets of regular elements]]

[[!redirects filter of cancellative elements]]
[[!redirects filters of cancellative elements]]
[[!redirects filter of regular elements]]
[[!redirects filters of regular elements]]

[[!redirects monoid of cancellative elements]]
[[!redirects monoids of cancellative elements]]
[[!redirects monoid of regular elements]]
[[!redirects monoids of regular elements]]

[[!redirects submonoid of cancellative elements]]
[[!redirects submonoids of cancellative elements]]
[[!redirects submonoid of regular elements]]
[[!redirects submonoids of regular elements]]

[[!redirects multiplicative monoid of cancellative elements]]
[[!redirects multiplicative monoids of cancellative elements]]
[[!redirects multiplicative monoid of regular elements]]
[[!redirects multiplicative monoids of regular elements]]

[[!redirects multiplicative submonoid of cancellative elements]]
[[!redirects multiplicative submonoids of cancellative elements]]
[[!redirects multiplicative submonoid of regular elements]]
[[!redirects multiplicative submonoids of regular elements]]

[[!redirects regular element in a ring]]