Classically, the **fundamental theorem of algebra** states that 

* The [[field]] of [[complex number]]s is algebraically closed. 

Many proofs of this theorem are known; some use complex analysis (the reciprocal of a polynomial cannot be bounded), some use algebraic topology (the degree of a map is invariant with respect to homotopy), and some use advanced calculus (polynomial functions on the complex numbers are open mappings). Most of these proofs involve, at some level, the fact that the real numbers are [[Dedekind real number|Dedekind complete]], which has as a classical consequence the fact that the real numbers are archimedean. 

The following proof is algebraic and, unlike the proof methods cited above, applies more generally to [[real closed field]]s, which need not be archimedean. It is due to Emil Artin, and forms a basic chapter in the Artin-Schreier theory of real closed fields. 

We recall that a _real closed field_ is an ordered field such that every positive element has a square root, and every polynomial of odd degree has a root. Clearly the polynomial $x^2 + 1$ has no root in a real closed field. 

+-- {: .un_thm}
######Theorem 
If $F$ is real closed, then $K = F[\sqrt{-1}]$ is algebraically closed. 
=--

+-- {: .proof} 
######Proof 
We must show that any irreducible polynomial $p$ with coefficients in $K$ has a root in $K$. 

The splitting field of $p$ is a finite Galois extension $L$ of $F$, with Galois group $G$. If $G(2)$ is the Sylow 2-group of $G$, then the fixed field of $G(2)$ is an odd degree extension of $F$, given by the splitting field of an odd degree irreducible polynomial $q$ over $F$. But since $F$ is real closed, $q$ has a root in $F$; by irreducibility, the degree must be 1, so that in fact $G = G(2)$. We may assume $|G| \gt 1$. 

So $G$ is a 2-group. But for any prime $p$, a finite $p$-group has nontrivial center, and is therefore solvable by an inductive argument. Therefore the extension $L/F$ arises from a tower of non-trivial quadratic extensions 

$$F \subseteq L_1 \subseteq \ldots \subseteq L_n = L$$ 

By the [[quadratic formula]], the first field $L_1$ arises by adjoining roots to $F$ of a polynomial $x^2 + a x + b$, 

$$\frac{-a \pm \sqrt{a^2 - 4b}}{2},$$ 

where $a^2 - 4b$ is negative. Since $F$ is real closed, the positive element $4b - a^2$ has a square root in $F$, so that the roots displayed above belong to $K = F[\sqrt{-1}]$. So $L_1 = K$. But $K$ has no nontrivial quadratic extensions by the lemma that follows, so in fact $L_1 = L_n = K$ and the theorem is proved. 
=-- 

+-- {: .un_lem}
######Lemma 
Every element of $K = F[\sqrt{-1}]$ has a square root in $K$. 
=-- 

+-- {: .proof} 
######Proof 
The proof is most easily apprehended by analogy with polar coordinate representations of complex numbers and half-angle formulas. Put $i = \sqrt{-1}$ and let $a + b i$ be an arbitrary element of $K$, with $a, b \in F$. We must solve $(r + s i)^2 = a + b i$, i.e., find $r, s \in F$ such that 

$$r^2 - s^2 = a, \qquad 2r s = b$$ 

Since $a^2 + b^2$ has a square root in $F$, we may assume without loss of generality that $a^2 + b^2 = 1$. By interchanging $r$ and $s$ if necessary, we may assume $a \geq 0$; by replacing $s$ by $-s$ if necessary, we may also assume $b \geq 0$. Since $0 \leq a \leq 1$, we may choose nonnegative $r$ and $s$ such that 

$$r^2 = \frac{1+a}{2}, \qquad s^2 = \frac{1-a}{2}$$ 

and this provides the solution. 
=--
