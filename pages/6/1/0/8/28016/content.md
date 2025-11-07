
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


\tableofcontents


## Idea

[[Jordan algebras]] were invented to axiomatize some properties of the Jordan product $a \circ b = (a b + b a)/2$ of self-adjoint complex matrices, which serve as [[observables]] in quantum mechanics.  As work proceeded, some researchers found it convenient to focus on another binary operation on self-adjoint matrices, $U_a (b) = a b a$.  Axiomatizing the properties of this led to the definition of a [[quadratic Jordan algebra]].   However, it is often convenient to replace this operation $U_a(b)$ by a trilinear operation, obtained by [[polarization identity|polarization]] as follows:

$$  \{a,b,c\} = U_{a+c}(b) - U_a(b) - U_c(b) = a b c + c b a $$

A **Jordan triple system** axiomatizes the properties of this triple product of self-adjoint complex matrices.  

Later it was discovered that there are close relations between Jordan triple systems and [[Lie triple systems]]. Just as Lie triple systems naturally give $\mathbb{Z}/2$-graded [[Lie algebras]], Jordan triple systems naturally give a certain class of so-called **3-graded Lie algebras**, which are $\mathbb{Z}$-graded Lie algebras concentrated in degrees $-1,0$ and $1$.   And just as the tangent space of any point in a [[symmetric space]] is naturally a Lie triple system, the tangent space of any point in a [[hermitian]] symmetric space is naturally a Jordan triple system.

## Definition

A **Jordan triple system** is a vector space $V$ equipped with a trilinear map $\{\cdot, \cdots, \cdot \} \colon V \times V \times V \to V$ obeying two axioms:

$$ \{a,b,c\} = \{c,b,a\}$$

$$\{a,b,\{c,d,e\}\} - \{c,d,\{a,b,e\}\} = \{\{a,b,c\},d,e\} - \{c,\{b,a,d\},e\} 
$$

Any subspace of an associative algebra closed under the operation $\{a,b,c\} = a b c + c b a$ obeys these axioms, and the first axiom captures the symmetry of this operation under switching the first and last arguments.  The second, subtler axiom implies that the operations $L_{a,b} \colon V \to V$ given by $L_{a,b}(c) = \{a,b,c\}$  form a Lie algebra under commutators.

## Jordan triple systems from Jordan algebras

Any Jordan algebra gives a Jordan triple system by

$$ \{a,b,c\} = a \circ (b \circ c) + (a \circ b) \circ c - b \circ (a \circ c).$$

There are however other Jordan triple systems.  For example, let $M(m,n)$ be the space of $m \times n$ matrices with entries in a field, and given $a \in M(m,n)$ let $a^T \in M(n,m)$ be its transpose.  We can make $M(m,n)$ into a Jordan triple system by defining

$$ \{a,b,c\} = a b^t c - c b^t a .$$

## Lie triple systems from Jordan triple systems

Any Jordan triple system gives a Lie triple system with Lie triple product given by

$$ [x,y,z] = \{x,y,z\} - \{y,x,z\} .$$

## Relation to 3-graded Lie algebras

Given any 3-graded Lie algebra $\mathfrak{g}$ with an anti-graded involution $\varepsilon \colon \mathfrak{g} \rightarrow \mathfrak{g}$ (restricting to $\mathfrak{g}_{-1} \rightarrow \mathfrak{g}_1$ and $\mathfrak{g}_0 \rightarrow \mathfrak{g}_0$) and any linear subspace $V \subseteq \mathfrak{g}$ closed under the triple commutator

$$ \{u,v,w\} = [[u,\varepsilon(v)], w] ,$$

$V$ becomes a Lie triple system. Thus, given a 3-graded Lie algebra, say $\mathfrak{g} = \mathfrak{g}_{-1} \oplus  \mathfrak{g}_0 \oplus \mathfrak{g}_1$, the space $\mathfrak{g}_1$ of odd elements becomes a Jordan triple system.   

Conversely, given any Jordan triple system $V$, if we define 

$$ \mathfrak{g}_{-1} = V $$

$$ \mathfrak{g}_0 = \text{span}\{L_{u,v}: u, v \in V \} $$ 

$$ \mathfrak{g}_1 = V $$

then $\mathfrak{g} = \mathfrak{g}_{-1} \oplus  \mathfrak{g}_0 \oplus \mathfrak{g}_1$ becomes a 3-graded Lie algebra with bracket given by

$$ [(a,L,u),(b,M,v)] = (L(b) - M(a), [L,M]+L_{a,v}-L_{b,u}, L(v) - M(u)) $$

for $L,M \in \mathfrak{g}_0, u,v \in \mathfrak{g}_1$. ([Caveny & Smirnov 11 Thrm. 5.3](#CavenySmirnov11))

Let $\mathbf{LA}_{3gr}$ be the category of Lie algebras, $\mathbf{LA}_{3gr}^\varepsilon$ be the category of Lie algebras with an anti-graded involution, and $\mathbf{JTS}$ be the category of Jordan triple systems. The first construction (with $V=\mathfrak{g}_1$) describes a [[forgetful functor]] $\mathcal{F}_\mathcal{T}\colon\mathbf{LA}_{3gr}^\varepsilon\rightarrow\mathbf{JTS}$. The second construction defines a [[fully faithful functor]] $\widehat{TKK}\colon\mathbf{JTS}\rightarrow\mathbf{LA}_{3gr}^\varepsilon$, which gives and [[adjunction]]:
$$
\widehat{TKK}\dashv\mathcal{F}_\mathcal{T}.
$$

([Caveny & Smirnov 11 6.1](#CavenySmirnov11))

This adjunction is not an [[equivalence of categories]]. Thus, the counit $\widehat{TKK}\mathcal{F}_\mathcal{T}\Rightarrow Id$ is not a natural isomorphism. But since $\widehat{TKK}$ is [[fully faithful]], a suitable subcategory of $\mathbf{LA}_{3-gr}^\varepsilon$ makes the [[adjunction]] an [[equivalence of categories]], which is that of 3-graded Lie algebras $\mathfrak{g}=\mathfrak{g}_{-1}\oplus\mathfrak{g}_0\oplus\mathfrak{g}_1$ with involution, which are centrally 0-closed (meaning every central 0-extension of it splits uniquely) and 0-perfect (meaning $\mathfrak{g}_0=[\mathfrak{g}_{-1},\mathfrak{g}_1]$). ([Caveny & Smirnov 11 Crl. 6.6](#CavenySmirnov11))

## References

* {#Loos71} Ottmar Loos, _Jordan triple systems, R-spaces, and bounded symmetric domains_, Bulletin of the American Mathematical Society __77__ (1971) 558–561. [pdf](https://www.ams.org/journals/bull/1971-77-04/S0002-9904-1971-12753-2/S0002-9904-1971-12753-2.pdf)

* {#Jacobson49} [[Nathan Jacobson]]: _Lie and Jordan triple systems_, American Journal of Mathematics __71__ (1949) 149–170 &lbrack;[jstor:2372102](https://www.jstor.org/stable/2372102)&rbrack; also in: *Nathan Jacobson, Collected Mathematical Papers*, Contemporary Mathematicians. Birkhäuser Boston (1989) &lbrack;[doi:10.1007/978-1-4612-3694-8_2](https://doi.org/10.1007/978-1-4612-3694-8_2)&rbrack;

* {#CavenySmirnov11} Deanna Caveny and [[Oleg Smirnov]]: _Categories of Jordan Structures and Graded Lie Algebras_ (2011), &lbrack;[arxiv:1106.2447](https://arxiv.org/abs/1106.2447)&rbrack;

[[!redirects Jordan triple systems]]
