## Idea

In general an assignment of an object of linear algebra to a $p$-divisible group is called a [[Dieudonné theory]].

There is a Dieudonn&#233; theory assigning to a formal $p$-divisible group $X$ over an excellent [[p-adic ring]] $R$ an object called *a display*. On the display one can read off the structural equations for the [[Cartier module]] of $X$.

## Definition

Let $R\in CRing$ a commutative unitary ring. Let $W(R)$ denote the ring of [[Witt vectors]] of $R$. Let

$$w_n:\begin{cases}
W(R)\to R
\\
(x_0,\dots,x_i,\dots)\mapsto x_0^{p^n}+p x_1^{p^{n-1}}+ \dots + p^n x_n
\end{cases}$$

denote the morphism of rings assigning to Witt vector its correspnding [[Witt polynomial]]. Let

$$w_n:\begin{cases}
W(R)\to W(R)
\\
(x_0,\dots,x_i,\dots)\mapsto (0,x_0,\dots,x_i,\dots)
\end{cases}$$

denote the [[Verschiebung morphism]] which is a morphism of the underlying additive groups. Let $p$ be a [[prime number]] and let

$$F:W(R)\to W(R)$$

denote the [[Frobenius morphism]]. Then Frobenius, Verschiebung, and the Witt-polynomial morphism satisfy the ''$p$-adic Witt-Frobenius identities'':

$$w_n(F(x))=w_{n+1}(x),\; n\ge 0$$

$$w_n(V(x))=w_{n-1}(x),\; n\gt 0$$

$$w_0(V(x))=0$$

$$FV=p$$

$$VF(xy)=xV(y)$$

+-- {: .num_defn}
###### Definition
A *$3n$-display over R* is defined to be a quadruple $(P, Q, F, V^{-1})$ where $P$ is a finitely generated projective $W(R)$-module, $Q \subset P$ is a submodule and $F$ and $V^{-1}$ are $F$-linear maps $F : P \to P$, $V^{-1}: Q \to P$.

The following properties are satisfied:

1. $ker(w_0)P \subset  Q \subset P$ and $P /Q$ is a direct summand of the $W (R)$&#8722;module $P /ker(w_0)P$. 

1. $V^{-1} : Q \to P$ is a $F$-linear epimorphism. 

1.  For $x \in P$ and $w \in W (R)$, we have $V^{-1} ( V wx) = wF x$. 

=--

+-- {: .num_defn}
###### Definition
Let $(\alpha_{ij})$ be a invertible matrix satisfying


a) $F e_j=\sum_{i=1}^h\alpha_{ij} e_i, \; j=1,\dots ,d$

b) $V^{-1} e_j=\sum_{i=1}^h\alpha_{ij} e_i, \; j=1,\dots ,h$

Let $(\beta_{kl})$ denote the inverse matrix of $(\alpha_{ij})$. Let $B:=(w_0(\beta_{kl})modulo\; p)_{k,l=d+1,\dots,k}$ let $B^{(p)}$ deonte the matrix obtained by raising all entries to the $p$-th power. $(\alpha_{ij})$ is said to satisfy *the $V$-nilpotence condition* if there is a natural number $N\in \mathbb{N}$ such that $B^{p^{N-1}}\cdot\dots\cdot B^{(p)}\cdot B=0$.

Then a $3n$-display satisfying the $V$-nilpotence condition locally on the [[spectrum]] $Spec R$ is called a *display*.
=--

## Properties

The following theorem compares the Dieudonn&#233; theory in terms of displays and the [[crystalline Dieudonné theory]] of Grothendieck and Messing [Messing](#Messing).

+-- {: .num_theorem}
###### Theorem
Let $\mathcal{P}:=(P,Q,F,V^{-1})$ be a display over $R$. Then there is an isomorphism of [[crystal|crystals]]

$$D_\mathcal{P}\stackrel{\sim}{\to}\mathbf{D}_{B T_\mathcal{P}}(S)$$

where on the right side is the crystal defined in [Messing](#Messing).
=--

## Examples

## References

* [[Lawrence Breen]], [[Pierre Berthelot]], [[William Messing]], Th&#233;orie de Dieudonn&#233; cristalline II {#Messing}

* T. Zink, the display of a formal p-divisible group, to appear in [[Astérisque]], [pdf](http://www.math.uni-bielefeld.de/~zink/display.pdf)

* T. Zink, Windows for displays of p-divisible groups. in:Moduli of Abelian Varieties, Progress in Mathematics 195, Birkh&#228;user 2001, [pdf](http://www.math.uni-bielefeld.de/~zink/Texel.pdf)
