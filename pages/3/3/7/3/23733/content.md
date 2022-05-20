
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


## Definition ##

Given a [[commutative monoid]] $(M, \cdot, 1)$, we say that [[element]] $a \in M$ *divides* $b \in M$ ($a \vert b$) if there exists an element $c \in M$ such that $a \cdot c = b$ and $c \cdot a = b$. If the commutative monoid has an [[absorbing element]] $0$, then for all $a \in M$, $a \vert 0$. 

\begin{definition}
A [[commutative ring]] $R$ is a **GCD ring** if for every [[element]] $a \in R$ and $b \in R$, there is an element $c \in R$ such that $c \vert a$ and $c \vert b$, and for every other element $d \in R$ such that $d \vert a$ and $d \vert b$, $d \vert c$. 
\end{definition}

Equivalently, 

\begin{definition}
A [[commutative ring]] $R$ is a **GCD ring** if there is a function $\gcd:R \times R \to R$ such that for every [[element]] $a \in R$ and $b \in R$, $\gcd(a, b) \vert a$ and $\gcd(a, b) \vert b$, and for every other element function $f:R \times R \to R$ such that $f(a, b) \vert a$ and $f(a, b) \vert b$, $f(a, b) \vert \gcd(a, b)$. 
\end{definition}

## See also ##

* [[commutative ring]]

* [[GCD domain]]

* [[Bézout ring]]

* [[Euclidean ring]]

* [[prefield]]

* [[field]]

## References ##

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

[[!redirects GCD rings]]
