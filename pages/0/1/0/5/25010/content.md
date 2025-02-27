
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

While in general, [[integral domains]] are non-[[trivial rings]], it is sometimes useful in [[commutative algebra]] for the [[trivial ring]] to be an integral domain. Thus, the idea of a **possibly trivial integral domain**. 

## Definition

Let $R$ be a [[commutative ring]] and let $D \subseteq R$ be the subset of all [[zero divisors]] or non-[[cancellative elements]] in $D$. A **possibly trivial integral domain** is a [[commutative ring]] $R$ such that every element in the [[two-sided ideal]] $I_D$ generated by $D$ is equal to zero, or that the quotient ring $R/I_D$ is isomorphic to $R$. 

If $R$ is the [[trivial ring]], $D$ is the [[empty subset]], the ideal generated by the empty subset is the trivial ideal $0R$, and $R/0R$ is always isomorphic to $R$. 

This is equivalent to the following definition:

\begin{definition}
A **possibly trivial integral domain** is a [[commutative ring]] $R$ such that for all elements $x \in R$ and $y \in R$, $x \cdot y = 0$ implies that $x = 0$ or $y = 0$. 
\end{definition}

Alternatively, one can define possibly trivial integral domains using a weakened version of [[negation]] from [Lombardi & Quitté 2010](#LombardiQuitté2010) in the definition of an integral domain: 

\begin{definition}
A **possibly trivial integral domain** is a [[commutative ring]] $R$ such that for all elements $x \in R$, if $x$ being a [[cancellative element]] implies that $0 = 1$, then $x = 0$. 
\end{definition}

## Constructing a possibly trivial integral domain from a commutative ring

From every commutative ring, one could construct a possibly trivial integral domain. 

As above, let $R$ be a [[commutative ring]], let $D \subseteq R$ be the subset of all [[zero divisors]] or non-[[cancellative elements]] in $D$, and let $I_D$ be the [[two-sided ideal]] generated by $D$. The quotient of $R$ by $I_D$ is the possibly trivial integral domain of $R$. 

$R/I_D$ is a possibly trivial integral domain, because the quotient of $R$ by $I_D$ takes all elements of $I_D$ to zero. If $R$ is an [[approximate integral domain]], then $R/I_D$ is an [[integral domain]]; otherwise, $R/I_D$ is the [[trivial ring]]. 

## In constructive mathematics

In constructive mathematics, the notion of integral domain bifurcates into multiple notions. While the definition given above results in the usual notion of an integral domain as a commutative ring whose zero divisors are equal to zero, there are also possibly trivial [[Heyting integral domains]] and possibly trivial [[discrete integral domains]], which refer directly to cancellative elements. 

\begin{definition}
A possibly trivial integral domain $R$ is **Heyting** if it has a [[tight apartness relation]] and where every element apart from zero is cancellative. The trivial ring is trivially Heyting because the set of elements apart from zero is the empty subset. 
\end{definition}

\begin{definition}
A possibly trivial integral domain is **discrete** if every element of $R$ is either equal to zero or cancellative. The trivial ring is trivially discrete because every element is both equal to zero and cancellative. These are simply called *integral domains* in [LombardiQuitté2010](#LombardiQuitté2010). Possibly trivial discrete integral domains have [[decidable equality]]. 
\end{definition}

## See also

* [[commutative ring]]
* [[integral domain]]
* [[possibly trivial field]]

## References

The concept of a possibly trivial integral domain appeared in 

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

where the possibly trivial discrete integral domains are simply called "integral domains". 

[[!redirects possibly trivial integral domain]]
[[!redirects possibly trivial integral domains]]