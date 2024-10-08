
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

## Definition ##

Given a [[commutative monoid]] $(M, \cdot, 1)$, we say that [[element]] $a \in M$ *divides* $b \in M$ ($a \vert b$) if there exists an element $c \in M$ such that $a \cdot c = b$. 

Given a [[commutative ring]] $R$, let $\mathrm{Reg}(R)$ be the [[multiplicative submonoid of regular elements]] in $R$. 

\begin{definition}
A [[commutative ring]] $R$ is a **GCD ring** if for every [[element]] $a \in \mathrm{Reg}(R)$ and $b \in \mathrm{Reg}(R)$, there is an element $c \in \mathrm{Reg}(R)$ such that $c \vert a$ and $c \vert b$, and for every other element $d \in \mathrm{Reg}(R)$ such that $d \vert a$ and $d \vert b$, $d \vert c$. 
\end{definition}

## See also ##

* [[commutative ring]]

* [[Bézout ring]]

* [[unique factorization ring]]

* [[GCD domain]]

* [[Euclidean ring]]

## References ##

* {#Lombardi,Quitté10}[[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

[[!redirects GCD rings]]
