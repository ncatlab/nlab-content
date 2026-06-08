
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Statement

Classically, the **fundamental theorem of algebra** states that 

* The [[field]] of [[complex number]]s $\mathbb{C}$ is [[algebraically closed field|algebraically closed]]. In other words, every nonconstant [[polynomial function]] with [[coefficients]] in $\mathbb{C}$ has a [[root]] in $\mathbb{C}$. 

Since every non-zero polynomial could be made a [[monic polynomial]] by dividing by the leading coefficient, it could also be expressed as

* The [[field]] of [[complex number]]s $\mathbb{C}$ is [[integrally closed field|integrally closed]]. In other words, every [[monic polynomial|monic]] [[polynomial function]] with [[coefficients]] in $\mathbb{C}$ has a [[root]] in $\mathbb{C}$. 

Many proofs of this theorem are known (see the [references](#References) below); some use [[complex analysis]] (the reciprocal of a [[polynomial function]] cannot be bounded), some use [[algebraic topology]] (the degree of a map is invariant with respect to homotopy), and some use advanced calculus (polynomial functions on the complex numbers are [[open map|open mappings]]). All of these proofs involve, at some level, the fact that the real numbers are [[Dedekind real number|Dedekind complete]], which has as a consequence the fact that the real numbers are [[archimedean field|archimedean]]. 

## Algebraic proof via real closed fields 

Despite its name, the fundamental theorem of algebra makes reference to a concept from [[analysis]] (the field of complex numbers).  However, the analytic part may be reduced to a minimum: that the field of [[real numbers]] is [[real closed field|real closed]].  This has been known essentially forever, and is easily proved using (for example) the [[intermediate value theorem]].

The rest of the proof is algebraic and, unlike the other proof methods, applies to all [[real closed field]]s, which need not be archimedean. It is due to [[Emil Artin]], and forms a basic chapter in the Artin--Schreier theory of real closed fields.

We recall that a _real closed field_ is an [[ordered field]] such that every positive element has a [[square root]], and every polynomial function of odd degree has a root.  Note that the polynomial function $x^2 + 1$ cannot have any root in a real closed field --- or in fact in any ordered field, since we always have $x^2\ge 0$ and hence $x^2+1 \ge 1$.

+-- {: .num_theorem}
###### Theorem 
If $F$ is real closed, then $K = F[\sqrt{-1}]$ is algebraically closed. 
=--

+-- {: .proof} 
###### Proof 
We must show that any [[irreducible polynomial]] $p$ of degree greater than $0$ with coefficients in $K$ has a root in $K$. Since $F$ has characteristic $0$, it is a [[perfect field]]. 

Thus the [[splitting field]] of $p$ is a finite [[Galois extension]] $L$ of $F$, with [[Galois group]] $G$. If $G(2)$ is the [Sylow 2-group](http://ncatlab.org/nlab/show/class+equation#sylow_theorems) of $G$, then the [[fixed field]] $E$ of $G(2)$ is an odd degree extension of $F$. Any $\alpha \in E$ must then have an irreducible polynomial function $q \in F[x]$ of odd degree. But since $F$ is real closed, $q$ has a root in $F$; by irreducibility, $\deg(q) = 1$ and $\alpha \in F$, forcing $E = F$ and $G = G(2)$. We have ${|G|} \gt 1$ since the splitting field contains $K$. 

So $G$ is a $2$-[[primary group]]. But for any [[prime number]] $p$, a nontrivial finite $p$-group has nontrivial [[center]] (see [here](/nlab/show/class+equation#pgroup)), and is therefore [[solvable group|solvable]] by an inductive argument. Therefore the extension $L/F$ arises from a tower of non-trivial [[quadratic extension]]s 

$$F \subseteq L_1 \subseteq \ldots \subseteq L_n = L$$ 

By the [[quadratic formula]], the first field $L_1$ arises by adjoining roots to $F$ of a polynomial function $x^2 + a x + b$, 

$$\frac{-a \pm \sqrt{a^2 - 4b}}{2},$$ 

where $a^2 - 4b$ is negative. Since $F$ is real closed, the positive element $4b - a^2$ has a square root in $F$, so that the roots displayed above belong to $K = F[\sqrt{-1}]$. So $L_1 = K$. But $K$ has no nontrivial quadratic extensions by the lemma that follows, so in fact $L_1 = L_n = K$ and the theorem is proved. 
=-- 

+-- {: .num_lemma #sqrt}
###### Lemma 
Every element of $K = F[\sqrt{-1}]$ has a square root in $K$. 
=-- 

+-- {: .proof} 
###### Proof 
The proof is most easily apprehended by analogy with polar coordinate representations of complex numbers and half-angle formulas, where a square root of $r e^{i\theta}$ is given by $r^{1/2}e^{i\theta /2}$. Let $i$ be a fixed square root of $-1$, and let $a + b i$ be an arbitrary element of $K$, with $a, b \in F$. We must solve $(x + y i)^2 = a + b i$, i.e., find $x, y \in F$ that solve 

$$x^2 - y^2 = a, \qquad 2x y = b$$ 

Since $a^2 + b^2$ has a square root in $F$, we may assume by homogeneity in $x, y$ that $(a, b)$ is on the unit circle: $a^2 + b^2 = 1$. By interchanging $x$ and $y$ if need be, we may assume $0 \leq a \leq 1$; replacing $y$ by $-y$ if need be, we may assume $b \geq 0$. Taking $x, y \geq 0$ such that 

$$x^2 = \frac{1+a}{2}, \qquad y^2 = \frac{1-a}{2},$$ 

we obtain a solution (since $x^2 - y^2 = a$ and $4 x^2 y^2 = b^2$). 
=--


## Classical FTA via advanced calculus 

As noted above, many proofs of the fundamental theorem are known. The following proof, ultimately rooted in the fact that [[polynomial mappings]] on $\mathbb{C}$ are [[open mappings]], has the advantage that it requires very little machinery. From what I ([[Todd Trimble]]) understand, it is close to the method used by Argand to give his proof (1814)[^1]. 

[^1]: Despite the credit given to Gauss for his demonstration of 1799, Argand's proof is often credited as the first one that is *fully rigorous*. The proof given here also uses the Bolzano-Weierstrass theorem, first proven by Bolzano in 1817, making it somewhat contemporaneous. Argand is also widely credited as the one who introduced the cutting-edge idea of viewing complex numbers and their operations *geometrically*, which the proof here also uses (the complex plane $\mathbb{C}$ being also known as the Argand plane). 

Let $f\colon \mathbb{C} \to \mathbb{C}$ be a nonconstant polynomial mapping, and suppose $f$ has no zero. 

1. Let $s$ be the [[infimum]] of values ${|f(z)|}$; choose a [[sequence]] $z_1, z_2, z_3, \ldots$ such that ${|f(z_n)|} \to s$. Since $\lim_{z \to \infty} f(z) = \infty$, the sequence $z_n$ must be bounded; by the Bolzano-Weierstrass theorem it has a [[sequence|subsequence]] $z_{n_k}$ that converges to some point $z_0$. Then ${|f(z_{n_k})|}$ converges to ${|f(z_0)|}$ by continuity, and converges to $s$ as well, so ${|f(z)|}$ attains an absolute minimum $s$ at $z = z_0$. By supposition, $f(z_0) \neq 0$. 

2. The polynomial function $f$ may be uniquely written in the form 
$$f(z) = f(z_0) + g(z)(z - z_0)^n$$ 
where $g$ is polynomial function and $g(z_0) \neq 0$. Put 
$$F(z) = f(z_0) + g(z_0)(z - z_0)^n$$ 
and choose $\delta \gt 0$ small so that 
$${|z - z_0|} = \delta \Rightarrow {|g(z) - g(z_0)|} \lt {|g(z_0)|}.$$ 

3. $F$ maps the circle $C = \{z : {|z - z_0|} = \delta\}$ _onto_ a circle of radius $r = {|g(z_0)|}\delta^n$ centered at $f(z_0)$. (This uses the fact that any complex number has an $n^{th}$ root, which one can prove using polar coordinate representations. We omit the details.) Choose $z' \in C$ so that $F(z')$ is on the line segment between the origin and $f(z_0)$ (we can always choose $\delta$ so that also $r \lt {|f(z_0)|}$). Then 
$${|F(z')|} = {|f(z_0)|} - r$$
We also have 
$${|f(z') - F(z')|} = {|g(z') - g(z_0)|} {|z' - z_0|^n} \lt {|g(z_0)|} \delta^n = r$$ 
according to how we chose $\delta$ in 2. We conclude by observing the strict inequality 
$${|f(z')|} \leq {|F(z')|} + {|f(z') - F(z')|} \lt {|f(z_0)|} - r + r = {|f(z_0)|},$$ 
which contradicts the fact that ${|f(z)|}$ attains an absolute minimum at $z = z_0$.  




## Via cohomology of complex projective space
 {#ViaCellularCohomology}

The following expands out a proof indicated by [Bruner 2009](#Bruner2009), of the fundamental theorem of algebra via the [[integral cohomology|integral]] [[cohomology ring]] of [[complex projective space]] $\mathbb{C}P^{n-1}$:

> [Bruner 2009](#Bruner2009): "I just noticed the following proof that the complex numbers $\mathbb{C}$ are algebraically closed, and wonder if anyone has seen it in print anywhere. \linebreak
> An algebraic extension of C is a unital division algebra over $\mathbb{C}$, say of dimension $n$, so induces 
> $$ \mathbb{C}P^{n-1} \times \mathbb{C}P^{n-1} \longrightarrow \mathbb{C}P^{n-1}$$
> satisfying 
> $$ y \mapsto 1 \textstyle{\otimes} y + y \textstyle{\otimes} 1 $$
> in second integral cohomology.  Since $y^n = 0$, we must have $n=1$."

Recall here that the [[integral cohomology]] of [[complex projective space]] $\mathbb{CP}^{n-1}$ is (see [there](complex+projective+space#Cohomology)): 

$$
  H^i\big(
    \mathbb{CP}^{n-1}; 
    \mathbb{Z}
  \big) 
    \cong 
  \mathbb{Z}^{a_i}
  \mathrlap{\,,}
  \;\text{where}\;
  a_i 
    =
  \left\{ 
  \begin{array}{ll}
    1 & \text{if}\; i \in \{ 2j \vert 0 \leq j \leq n-1 \}
    \\
    0 & \text{otherwise}
  \end{array}
  \right.
$$

on which the [[cup product]] induces a ring [[isomorphism]] 

$$
  H^*\big(
    \mathbb{CP}^n, \mathbb{Z}
  \big) 
    \simeq  
  \mathbb{Z}[c] / c^n \mathbb{Z}[c]
  \mathrlap{\,,}
$$

where $c$ denotes the integral [[first Chern class]] (cf. [here](complex+projective+space#OrdinaryCohomologyOfComplexProjectiveSpace)).

\begin{theorem} 
Let $K$ be a [[finite dimensional vector space]] over $\mathbb{C}$ equipped 

1. (unit) a map $\eta : \ast \rightarrow K$ 

1. (product) a [[linear map]] $\mu \colon K \otimes_{\mathbb{C}} K \rightarrow K$

satisfying for $a,b \in K$:

1. ([[unitality]]) $\mu\big(\eta(1),a\big) = a = \mu\big(a,\eta(1)\big)$, 

1. (no [[zero-divisors]]) if $\mu (a \otimes b) = 0$, then $a = 0$ or $b = 0$.

(We do not *need* to require [[associativity]]!)

Then $K$ is [[isomorphism|isomorphic]] to $\mathbb{C}$ itself as a [[complex vector space|$\mathbb{C}$-vector space]], i.e. [[dimension of a vector space|$\text{dim}(K)$]] $= 1$.
\end{theorem}

Note that we obtain such a nonassociative $\mathbb{C}$-algebra as the [[splitting field]] of any complex [[irreducible  polynomial]].

\begin{proof}
The assumed absence of [[zero divisors]] implies that multiplication restricts to the [[complement]] of zero, and [[bilinear map|bilinearity]] of the multiplication then implies that it respects [[complex lines]] and hence descends to a [[continuous map]] between ([[product space|products]] of) [[complex projective space]]

$$
  [ \mu|_{ \mathbb{C}^n \setminus \{0\} } ] 
    \ : \ 
  \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1} 
    \longrightarrow 
  \mathbb{CP}^{n-1}
  \mathrlap{\,.}
$$

Recall that $c \in H^2(\mathbb{CP}^{n-1})$ is the generator of the [[cohomology ring]] $H^* ( \mathbb{CP}^{n-1} )$. We have:

$$
  H^2\big(
    \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1}; 
    \mathbb{Z}
  \big) 
   \cong 
  H^2\big(
    \mathbb{CP}^{n-1}; \mathbb{Z}
  \big) 
   \oplus 
  H^2\big(
    \mathbb{CP}^{n-1}; \mathbb{Z}
  \big) 
  \mathrlap{\,.}
$$

Therefore there must be $a, b \in \mathbb{Z}$ such that pullback of the generator along the product map is

$$
  H^2(\mu,\mathbb{Z})(c) 
    = 
  a \cdot (1 \textstyle{\otimes} c) 
    + 
  b \cdot (c \textstyle{\otimes} 1)
  \mathrlap{\,.}
$$

But these coefficients must satisfy the two equations which are the image in degree-2 [[integral cohomology]] of the two [[unit laws]] (the first assumed property on $K$):

$$ 
  H^2 \left( 
    \mu 
      \circ 
    \left( 
      \eta \times Id_{\mathbb{CP}^{n-1}} 
    \right) , 
    \mathbb{Z} 
  \right)   
  =  
  Id_{H^2 \left( \mathbb{CP}^{n-1} , \mathbb{Z} \right) }
  =   
  H^2 \left( 
    \mu 
    \circ 
    \left( 
      Id_{\mathbb{CP}^{n-1}} \times \eta 
    \right) , 
    \mathbb{Z} 
  \right)
  \mathrlap{\,.}
$$

This implies that:

$$
  a = 1, 
  \;\text{and}\;
  b = 1
  \mathrlap{\,.}
$$

There is an [[isomorphism]] of [[Hopf algebras]] in [[integral cohomology]] of 

$$
  \big(
    \mathbb{Z}[x]/x^n\mathbb{Z}[x]
  \big) 
    \otimes_{\mathbb{Z}}
  \big(
    \mathbb{Z}[x]/x^n\mathbb{Z}[x]
  \big)  
    \cong  
  H^\bullet\big(
   \mathbb{CP}^{n-1};
   \mathbb{Z}
  \big) 
    \otimes_{\mathbb{Z}} 
  H^\bullet\big(
    \mathbb{CP}^{n-1};
    \mathbb{Z}
  \big)  
    \cong  
  H^\bullet\big(
    \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1};
    \mathbb{Z}
  \big)
  \mathrlap{\,.}
$$

But $H^\bullet(\mu;\mathbb{Z})$ is a [[ring homomorphism]], so

$$
  H^\bullet(\mu;\mathbb{Z})(c^n) 
    = 
  (1 \textstyle{\otimes} c + c \textstyle{\otimes} 1)^n 
    = 
  \sum_{i = 0}^n 
  {\binom{n}{i}}\, 
    (1 \otimes c)^i \cdot (c \otimes 1)^{n-i} 
    = 
  \sum_{i = 0}^n 
  {\binom{n}{i}}\, 
    c^{n-i} \otimes c^{i}
$$

as elements of the commutative Hopf algebra

$$
  H^\bullet(\mathbb{CP}^{n-1}; \mathbb{Z}) 
    \otimes_{\mathbb{Z}} 
  H^\bullet(\mathbb{CP}^{n-1}; \mathbb{Z})  
   \;\cong\; 
  \left( 
    \mathbb{Z}[x]/x^n \mathbb{Z}[x] 
  \right) 
    \otimes_{\mathbb{Z}}
  \left( 
    \mathbb{Z}[x]/x^n \mathbb{Z}[x] 
  \right)
  \mathrlap{\,.}
$$

The left-hand side is $0$.

The right hand side is 

$$ 
   \sum_{i = 1}^{n-1} 
   {\binom{n}{i}}\, 
     c^{n-i} 
       \otimes 
     c^{i} 
  \mathrlap{\,.}
$$

By way of [[proof by contradiction|contradiction]], suppose that $n = \text{dim}(K)$ is greater than $1$. In this case, each of the terms $c^i \otimes c^{n-i}$ is nonzero for $0 \lt i \lt n$, and their sum is as well.

This implies that 

$$
  \sum_{i= 1}^{n-1} 
    {\binom{n}{i}}\,  
     c^{n-i} 
       \otimes 
     c^{i}
$$

is not zero, which contradicts that $c^n$ is zero using the above equation.

This implies $n = 1$ and hence the claim.
\end{proof}



## In weaker foundations

Many proofs of FTA rely explicitly on the [[double negation]] rule by first supposing that a polynomial function $p$ has no root and then deriving a [[proof by contradiction|contradiction]].  


### In constructive mathematics

In [[constructive mathematics]], the classical definition of an [[algebraic closure]] of a [[field]] is not well-behaved, since negation of equality on the real numbers. Instead, we have to use the [[tight apartness relation]] on the real numbers and define nonconstant function to mean "apart from every constant polynomial function". 

\begin{proposition}
Every [[polynomial function]] $p(z) = \sum_{i \lt n} a_n z^n$ with at least one coefficient $a_n$ in $\mathbb{C}$, with $n \gt 0$, apart from zero, has a [[root]] in $\mathbb{C}$. 
\end{proposition}

The other issue is that the notion of a field of [[real numbers]] bifurcates into multiple distinct notions of the real numbers. Different authors have ended up proving the fundamental theorem of algebra for different kinds of real numbers, without assuming any constructive [[taboos]]. 

* [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) have proven the fundamental theorem of algebra whose coefficients are valued in the field of [[complex numbers]] $\mathbb{C} = \mathbb{R}[i]/(i^2 + 1)$ of any [[sequentially Cauchy complete space|Cauchy complete]] [[Archimedean ordered field]] $\mathbb{R}$, examples of which include the [[HoTT book real numbers]], which is the [[initial object|initial]] Cauchy complete Archimedean ordered field, and the [[Dedekind real numbers]], which is the [[terminal object|terminal]] Cauchy complete Archimedean ordered field. 

* Section 5 of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) includes a list of other authors who proved the fundamental theorem of algebra, some like [[Brouwer]] with additional assumptions such as [[countable choice]]. 

Historically, the fundamental theorem of algebra was first originally proven using only monic polynomials or polynomials with a well-defined positive degree $n$ (i.e. one where $a_n$ is apart from zero and $a_m = 0$ for all $m \gt n$); which are equivalent to each other by multiplying or dividing the polynomial by the coefficient $a_n$, since $a_n$ is by definition invertible. 

* [Ruitenburg 1991](#Ruitenburg91) has proven, without using any constructive [[taboos]], that every [[monic polynomial|monic]] [[polynomial function]] with coefficients in the Cauchy complex numbers, with one of the coefficients invertible, has a root in the Cauchy complex numbers. 

* Section 5 of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) includes a list of authors who proved the fundamental theorem of algebra for monic polynomials, some like [[Brouwer]] with additional assumptions such as [[countable choice]]. 

Classical proofs of the fundamental theorem of algebra fail to work constructively if they are reliant on a [[principal square root]] function on the complex numbers, such as the proof in Lemma \ref{sqrt} which uses the [[quadratic formula]]. The principal square root cannot be proven to exist on the complex numbers, and in fact can be proven to not exist certain [[topoi]], such as [[sheaves]] over $\mathbb{C}$, because the principal square root on the complex numbers, if it exists, is not continuous at the branch cut, and it is consistent for all functions on the complex numbers to be continuous. The problem here is the failure of some amount of choice, that since the squaring function $z \mapsto z^2$ is a surjection on the [[complex numbers]], one can construct a [[right inverse]] of $z \mapsto z^2$. In general, any principal square root is only a [[partial function]] in [[neutral constructive mathematics]]. 

In light of this, [Richman 2000](#Richman00) has proposed that the FTA should be interpreted as a statement about sets of roots rather than about individual roots. He constructs a [[complete metric space]] $\hat{M}_n(\mathbb{C})$ which, classically, is the space of $n$-element [[multisets]] of complex numbers (and constructively is the completion of that space) and proves that every complex polynomial function $p$ of degree $n$ may be associated with a point in this space in such a way that the $n$ elements of that point (when viewed as a multiset, if possible, and morally in any case) are the $n$ roots of $p$. 

### In reverse mathematics

Assuming classical logic, but weak foundations, it can be shown that FTA is true in the [[reverse mathematics]] system $RCA_0$ ([Tanaka-Yamazaki 2005](#TY2005)).


## History
 {#History}

The proof was attempted many times before Gauss gave what is accepted as the first proof in his dissertation ([Gauss 1799](#Gauss1799)), although this was not without issues (Gauss 'fixed' this proof almost 50 years later, but the last gap was not filled until the 20th century).

All proofs of this fact (of which there are many) require something analytic, in the sense that ordinary algebra will not suffice: one needs to know that the real numbers (or the complex numbers) 'have no algebraic gaps'. For instance, the rational numbers famously don't contain the square root of $2$. The cleanest proof I know, due to Artin, that isolates this analytic germ, uses the step-ladder result that the real numbers form what is called a [[real closed field]]. This is essentially saying that non-negative real numbers have square roots, and odd degree polynomial functions have roots (anyone who has plotted a cubic can appreciate this fact). Alternatively, one can characterise real closed fields as those for whom the Intermediate Value Theorem (IVT) holds for polynomial functions. Accepting this result (which does need proof), the FTA follows using pure algebra (although not of the high-school sort).

However, it is of interest, partly theoretical, partly for the sake of finding the bare minimum needed to prove the FTA, to know an elementary proof, namely one that minimises the use of analytic techniques (for instance, the IVT for polynomial functions follows from the IVT for continuous functions, but that is like killing a mosquito with a bazooka). Gauss' second proof ([Gauss 1866](#Gauss1866)) is elementary (and predates Artin's by a long time). Since Gauss lacked modern algebraic techniques, some of his proof is laborious, but ([Taylor 85](#Taylor85)) gives a modern gloss. (With some amusing side notes: as Taylor puts it -- 'Gauss takes the opportunity [to] be rude to his inferior contemporaries'.) Gauss' proof, in modern language, takes up less than a page and a half, but this presupposes familiarity with some of the theory of fields (but which is pure algebra). Artin's proof, by comparison, drawing on major theorems can be given in half a page.

It should be noted, in the context of the last statement, that proofs of the FTA can be given, relying on analytic 'bazooka' theorems, that are one sentence. However, to spell out the proofs of the necessary theorems, one needs a course in analysis, of some variety, so one is merely sweeping a lot under a very small rug. 

In [[constructive mathematics]], there are multiple versions of the FTA which are inequivalent to each other, many of which are not formulated in algebraic terms. For example, the approximate version of the FTA listed above requires one to show that for all polynomials and for all [[neighborhoods]] around zero there exists a complex number $z$ such that the polynomial evaluated at $z$ is in the [[neighborhood]], which is analytic and topological rather than algebraic. 

## References
 {#References}

* {#Gauss1799} [[Carl Gauss]], _Demonstratio nova theorematis functionem algebraicam rationalem integramunius variabilis in factores reales primi vel secundi gradus resolvi posse_, Dissertation, Helmstedt (1799); Werke 3, 1&#8211;30 (1866) ([English transl. pdf](http://www.jon-arny.com/httpdocs/Gauss/Gauss%20Fundamental%20Theorem.pdf)))

* {#Gauss1866} [[Carl Gauss]], _Demonstratio nova altera theorematis omnem functionem algebraicamrationalem integram unius variabilis in factores reales primi vel secundi gradus resolviposse_, Comm. Soc. Reg. Sci. G&#246;ttingen 3, 107&#8211;142 (1816); Werke 3, 33&#8211;56 (1866)

* Michael Eisermann. _An Elementary Real-Algebraic Proof via Sturm Chains_. [pdf](http://www.jon-arny.com/httpdocs/Gauss/Constructive%20roots-annotated.pdf)

  _Another new proof of the theorem that every integral rational algebraic function of one variable can be resolved into real factors of the first or second degree_ translated by [[Paul Taylor]] and B. Leak (1983) ([web](http://www.paultaylor.eu/misc/gauss-web))

* {#Taylor85} [[Paul Taylor]], _Gauss' Second Proof_, Eureka 45 (1985) 42-47 ([pdf](http://www.jon-arny.com/httpdocs/Gauss/Eureka-2-aug24.pdf))

A proof using [[differential topology]]:

* [[John Milnor]]; pp. 8--9 in: _Topology from the differential viewpoint_, Princeton University Press (1997) &lbrack;[ISBN:9780691048338](https://press.princeton.edu/books/paperback/9780691048338/topology-from-the-differentiable-viewpoint), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnortop.pdf)&rbrack;

A [[constructive mathematics|constructive]] proof of the fundamental theorem of algebra for any [[sequentially Cauchy complete space|Cauchy complete]] [[Archimedean ordered field]]: 

* {#GWZ00} Herman Geuvers, Freek Wiedijk, Jan Zwanenburg, *A Constructive Proof of the Fundamental Theorem of Algebra without using the Rationals*, TYPES '00: Selected papers from the International Workshop on Types for Proofs and Programs, Pages 96 - 111, 08 December 2000 &lbrack;[web](https://dl.acm.org/doi/10.5555/646540.696038), [pdf](https://www.cs.ru.nl/F.Wiedijk/pubs/kneser.pdf)&rbrack;

A [[constructive mathematics|constructive]] proof of a variant using finite multisets of complex numbers: 

* {#Richman00} [[Fred Richman]], *The fundamental theorem of algebra: a constructive development without choice*, Pacific Journal of Mathematics **196** 1 (2000) 213–230 &lbrack;[doi:10.2140/pjm.2000.196.213](http://dx.doi.org/10.2140/pjm.2000.196.213), [pdf](https://msp.org/pjm/2000/196-1/pjm-v196-n1-p10-p.pdf)&rbrack;

see also:

* [[Fred Richman]], *Constructive Mathematics without Choice*,
in: *Reuniting the Antipodes -- Constructive and Nonstandard Views of the Continuum* Synthese Library **306**, Springer (2001) 199-206 &lbrack;[doi:10.1007/978-94-015-9757-9_17](https://doi.org/10.1007/978-94-015-9757-9_17)&rbrack;

A [[constructive mathematics|constructive]] algebraic proof for the [[modulated Cauchy real numbers]] without choice princples such as [[weak countable choice]]:

* {#Ruitenberg91} [[Wim Ruitenburg]]: *Constructing Roots of Polynomials over the Complex Numbers*, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract **84** Centre for Mathematics and Computer Science, Amsterdam (1991) 107–-128 &lbrack;[pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf), [[Ruitenburg-Roots.pdf:file]]&rbrack;

A full formalization in the [[Rocq]] [[proof assistant]]:

* Herman Geuvers, [[Freek Wiedijk]], Jan Zwanenburg: *A Constructive Proof of the Fundamental Theorem of Algebra without Using the Rationals &lbrack;[web](http://dl.acm.org/citation.cfm?id=696038)&rbrack;

The [above proof](#ViaCellularCohomology) using [[integral cohomology]] of [[complex projective space]]:

* {#Bruner2009} [[Robert Bruner]]: *cute proof*, message to [ALGTOP-L mailing list](https://rezk.web.illinois.edu/algtop-l/algtop-l.html) (1 Dec. 2009) &lbrack;[algtop-l:2009q4/000645](https://rezk.web.illinois.edu/algtop-l/archives2007-2023/2009q4/000645.html)&rbrack;

Discussion in the context of [[reverse mathematics]]:

* {#TK2005} Kazuyuki Tanaka, Takeshi Yamazaki: _Manipulating the reals in $RCA_0$_, inL _Reverse Mathematics 2001_, Lecture Notes in Logic **21** (2005)

See also:

* Matthew Steed: *Proofs of the Fundamental Theorem of Algebra*, [Reu2014](https://math.uchicago.edu/~may/REU2014/) &lbrack;[pdf](https://math.uchicago.edu/~may/REU2014/REUPapers/Steed.pdf)&rbrack;

* MathOverflow: _[Ways to prove the fundamental theorem of algebra](http://mathoverflow.net/questions/10535/ways-to-prove-the-fundamental-theorem-of-algebra)_


[[!redirects fundamental theorem of algebra]]
[[!redirects Fundamental Theorem of Algebra]]
[[!redirects FTA]]
