
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

\begin{definition}
A [[commutative ring]] $R$ is a **GCD ring** if there is a function $\gcd:R \times R \to R$ such that for every [[element]] $a \in R$ and $b \in R$, $\gcd(a, b) \vert a$ and $\gcd(a, b) \vert b$, and for every other function $f:R \times R \to R$ such that $f(a, b) \vert a$ and $f(a, b) \vert b$, $f(a, b) \vert \gcd(a, b)$. 
\end{definition}

\begin{definition}
A [[commutative ring]] $R$ is a **GCD ring** if there are functions $\gcd:R \times R \to R$, $q_0:R \times R \to R$, and $q_1:R \times R \to R$ such that for every [[element]] $a \in R$ and $b \in R$, $q_0(a, b) \cdot \gcd(a, b) = a$ and $q_1(a, b) \cdot \gcd(a, b) = b$, and for every other triple of functions $f:R \times R \to R$, $r_0:R \times R \to R$, $r_1:R \times R \to R$ such that $r_0(a, b) \cdot f(a, b) = a$ and $r_1(a, b) \cdot f(a, b) = b$, there is a function $s:R \times R \to R$ such that $s(a, b) \cdot f(a, b) = \gcd(a, b)$. 
\end{definition}

\begin{definition}
A [[commutative ring]] $R$ is a **GCD ring** if there are functions $\gcd:R \times R \to R$, $q_0:R \times R \to R$, and $q_1:R \times R \to R$ such that for every [[element]] $a \in R$ and $b \in R$, $q_0(a, b) \cdot \gcd(a, b) = a$ and $q_1(a, b) \cdot \gcd(a, b) = b$, and $\gcd:R \times R \to R$ is a [[semilattice]] with unit element $0$. 
\end{definition}

The last definition implies that GCD rings are [[algebraic theory|algebraic]]. 

## See also ##

* [[commutative ring]]

* [[Bézout ring]]

* [[GCD domain]]

* [[Euclidean ring]]

## References ##

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

[[!redirects GCD rings]]
