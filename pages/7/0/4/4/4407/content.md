#Contents#
* automatic table of contents goes here
{:toc}


## Statement

Classically, the **fundamental theorem of algebra** states that 

* The [[field]] of [[complex number]]s $\mathbb{C}$ is [[algebraically closed field|algebraically closed]]. In other words, every polynomial with coefficients in $\mathbb{C}$ has a root in $\mathbb{C}$. 

Many proofs of this theorem are known; some use complex analysis (the reciprocal of a polynomial cannot be bounded), some use algebraic topology (the degree of a map is invariant with respect to homotopy), and some use advanced calculus (polynomial functions on the complex numbers are open mappings). All of these proofs involve, at some level, the fact that the real numbers are [[Dedekind real number|Dedekind complete]], which has as a classical consequence the fact that the real numbers are archimedean. 

## Algebraic proof via real closed fields 

The following proof is algebraic and, unlike the proof methods cited above, applies more generally to [[real closed field]]s, which need not be archimedean. It is due to Emil Artin, and forms a basic chapter in the Artin-Schreier theory of real closed fields. (Of course, the fact that the real numbers form a real closed field uses Dedekind completeness.)

We recall that a _real closed field_ is an ordered field such that every positive element has a square root, and every polynomial of odd degree has a root. Clearly the polynomial $x^2 + 1$ has no root in a real closed field. 

+-- {: .un_thm}
######Theorem 
If $F$ is real closed, then $K = F[\sqrt{-1}]$ is algebraically closed. 
=--

+-- {: .proof} 
######Proof 
We must show that any irreducible polynomial $p$ with coefficients in $K$ has a root in $K$. 

The splitting field of $p$ is a finite Galois extension $L$ of $F$, with Galois group $G$. If $G(2)$ is the Sylow 2-group of $G$, then the fixed field of $G(2)$ is an odd degree extension of $F$, given by the splitting field of an odd degree irreducible polynomial $q$ over $F$. But since $F$ is real closed, $q$ has a root in $F$; by irreducibility, the degree must be 1, so that in fact $G = G(2)$. We have $|G| \gt 1$ since the splitting field contains $K$. 

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
The proof is most easily apprehended by analogy with polar coordinate representations of complex numbers and half-angle formulas, where a square root of $r e^{i\theta}$ is given by $r^{1/2}e^{i\theta /2}$. Let $i$ be a fixed square root of $-1$, and let $a + b i$ be an arbitrary element of $K$, with $a, b \in F$. We must solve $(x + y i)^2 = a + b i$, i.e., find $x, y \in F$ such that 

$$x^2 - y^2 = a, \qquad 2x y = b$$ 

Since $a^2 + b^2$ has a square root in $F$, we may assume without loss of generality that $a^2 + b^2 = 1$. By interchanging $x$ and $y$ if necessary, we may assume $a \geq 0$; by replacing $y$ by $-y$ if necessary, we may also assume $b \geq 0$. Since $0 \leq a \leq 1$, we may choose nonnegative $x$ and $y$ such that 

$$x^2 = \frac{1+a}{2}, \qquad y^2 = \frac{1-a}{2}$$ 

and this provides the solution. 
=--

## Classical FTA via advanced calculus 

As noted above, many proofs of the fundamental theorem are known. The following proof has the advantage that it requires very little machinery; it hardly uses anything not known by Gauss$^{[1]}$. 

Let $f: \mathbb{C} \to \mathbb{C}$ be a polynomial mapping, and suppose $f$ has no zero. 

* **Step 1.** First, $|f(z)|$ attains an absolute (positive) minimum. For, choose any $z' \in \mathbb{C}$. Since $\lim_{z \to \infty} f(z) = \infty$, there exists some compact ball $B$ containing $z'$ so that $|f(z)| \gt |f(z')|$ whenever $z \notin B$. By compactness, $|f(z)|$ attains an absolute minimum for $z$ ranging over $B$; by choice of $B$, it is the same minimum as for $z$ ranging over all of $\mathbb{C}$. 

* **Step 2.** Suppose $|f|$ attains an absolute minimum at $z = z_0$. The polynomial $f$ may be uniquely written in the form 
$$f(z) = f(z_0) + (z - z_0)^n g(z)$$ 
where $g$ is polynomial and $g(z_0) \neq 0$. Put 
$$F(z) = f(z_0) + g(z_0)(z - z_0)^n$$ 
and choose $\delta \gt 0$ small so that 
$$|z - z_0| = \delta \Rightarrow |g(z) - g(z_0)| \lt |g(z_0)|$$ 

* **Step 3.** $F$ maps the circle $C = \{z: |z - z_0| = \delta\}$ onto a circle of radius $r = |g(z_0)|\delta^n$ centered at $f(z_0)$. (This uses the fact that any complex number has an $n^{th}$ root, which one can prove using polar coordinate representations. We omit the details.) Choose $z' \in C$ so that $F(z')$ is on the line segment between the origin and $f(z_0)$. Then 
$$|F(z')| = |f(z_0)| - r$$
We also have 
$$|f(z') - F(z')| = |g(z') - g(z_0)| |z' - z_0|^n \lt |g(z_0)| \delta^n = r$$ 
according to how we chose $\delta$. We conclude by observing 
$$|f(z')| \leq |F(z')| + |f(z') - F(z')| \lt |f(z_0)| - r + r = |f(z_0)|,$$ 
which yields the desired contradiction.  

$[1]$ Maybe the bit involving compactness wasn't available in Gauss's time. It would be interesting to write this bit out so that the entire proof would be understood by an eighteenth-century mathematician. 
