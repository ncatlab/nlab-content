
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

Given a [[commutative monoid]] $(M, \cdot, 1)$, we say that [[element]] $a \in M$ *divides* $b \in M$ ($a \vert b$) if there exists an element $c \in M$ such that $a \cdot c = b$ and $c \cdot a = b$. 

Let $F \colon CRing \to CMon$ be the [[forgetful functor]] from [[CRing]] to [[CMon]] that only remember the multiplicative monoid structure of commutative rings. Given a [[commutative ring]] $R$, let us define the [[cancellative monoid]] $\mathrm{Can}(R)$ as the cancellative [[submonoid]] of the multiplicative monoid $F(R)$ such that every other cancellative submonoid $S$ of $F(R)$ is a cancellative submonoid of $\mathrm{Can}(R)$. 

\begin{definition}
A [[commutative ring]] $R$ is a **GCD ring** if for every [[element]] $a \in \mathrm{Can}(R)$ and $b \in \mathrm{Can}(R)s$, there is an element $c \in \mathrm{Can}(R)$ such that $c \vert a$ and $c \vert b$, and for every other element $d \in \mathrm{Can}(R)$ such that $d \vert a$ and $d \vert b$, $d \vert c$. 
\end{definition}

## See also ##

* [[commutative ring]]

* [[GCD domain]]

* [[reciprocal ring]]

* [[field]]

## References ##

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

[[!redirects GCD rings]]
