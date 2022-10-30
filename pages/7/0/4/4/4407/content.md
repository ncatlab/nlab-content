
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Statement

Classically, the **fundamental theorem of algebra** states that 

* The [[field]] of [[complex number]]s $\mathbb{C}$ is [[algebraically closed field|algebraically closed]]. In other words, every nonconstant [[polynomial]] with [[coefficients]] in $\mathbb{C}$ has a [[root]] in $\mathbb{C}$. 

Many proofs of this theorem are known (see the [references](#References) below); some use [[complex analysis]] (the reciprocal of a [[polynomial]] cannot be bounded), some use [[algebraic topology]] (the degree of a map is invariant with respect to homotopy), and some use advanced calculus (polynomial functions on the complex numbers are [[open map|open mappings]]). All of these proofs involve, at some level, the fact that the real numbers are [[Dedekind real number|Dedekind complete]], which has as a classical consequence the fact that the real numbers are [[archimedean field|archimedean]]. 



## Algebraic proof via real closed fields 

Despite its name, the fundamental theorem of algebra makes reference to a concept from [[analysis]] (the field of complex numbers).  However, the analytic part may be reduced to a minimum: that the field of [[real numbers]] is [[real closed field|real closed]].  This has been known essentially forever, and is easily proved using (for example) the [[intermediate value theorem]].

The rest of the proof is algebraic and, unlike the other proof methods, applies to all [[real closed field]]s, which need not be archimedean. It is due to [[Emil Artin]], and forms a basic chapter in the Artin--Schreier theory of real closed fields.

We recall that a _real closed field_ is an [[ordered field]] such that every positive element has a [[square root]], and every polynomial of odd degree has a root. Clearly the polynomial $x^2 + 1$ has no root in a real closed field. 

+-- {: .num_theorem}
###### Theorem 
If $F$ is real closed, then $K = F[\sqrt{-1}]$ is algebraically closed. 
=--

+-- {: .proof} 
###### Proof 
We must show that any [[irreducible polynomial]] $p$ of degree greater than $0$ with coefficients in $K$ has a root in $K$. 

The [[splitting field]] of $p$ is a finite [[Galois extension]] $L$ of $F$, with [[Galois group]] $G$. If $G(2)$ is the [[Sylow group|Sylow 2-group]] of $G$, then the [[fixed field]] of $G(2)$ is an odd degree extension of $F$, given by adjoining a root of an odd degree irreducible polynomial $q$ over $F$. But since $F$ is real closed, $q$ has a root in $F$; by irreducibility, the degree must be $1$, so that in fact $G = G(2)$. We have ${|G|} \gt 1$ since the splitting field contains $K$. 

So $G$ is a $2$-[[primary group]]. But for any [[prime number]] $p$, a nontrivial finite $p$-group has nontrivial [[center]], and is therefore [[solvable group|solvable]] by an inductive argument. Therefore the extension $L/F$ arises from a tower of non-trivial [[quadratic extension]]s 

$$F \subseteq L_1 \subseteq \ldots \subseteq L_n = L$$ 

By the [[quadratic formula]], the first field $L_1$ arises by adjoining roots to $F$ of a polynomial $x^2 + a x + b$, 

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

As noted above, many proofs of the fundamental theorem are known. The following proof has the advantage that it requires very little machinery; it hardly uses anything not known by [[Karl Gauss|Gauss]][^1]. 

[^1]: Maybe the bit involving compactness wasn't available in Gauss's time. It would be interesting to write this bit out so that the entire proof would be understood by an eighteenth-century mathematician. 

Let $f\colon \mathbb{C} \to \mathbb{C}$ be a nonconstant polynomial mapping, and suppose $f$ has no zero. 

1. First, ${|f(z)|}$ attains an absolute (positive) minimum. For, choose any $z' \in \mathbb{C}$. Since $\lim_{z \to \infty} f(z) = \infty$, there exists some [[compact subspace|compact]] [[ball]] $B$ containing $z'$ so that ${|f(z)|} \gt {|f(z')|}$ whenever $z \notin B$. By compactness, ${|f(z)|}$ attains an absolute minimum for $z$ ranging over $B$; by choice of $B$, it is the same minimum as for $z$ ranging over all of $\mathbb{C}$. 

2. Suppose ${|f|}$ attains an absolute minimum at $z = z_0$. The polynomial $f$ may be uniquely written in the form 
$$f(z) = f(z_0) + (z - z_0)^n g(z)$$ 
where $g$ is polynomial and $g(z_0) \neq 0$. Put 
$$F(z) = f(z_0) + g(z_0)(z - z_0)^n$$ 
and choose $\delta \gt 0$ small so that 
$${|z - z_0|} = \delta \Rightarrow {|g(z) - g(z_0)|} \lt {|g(z_0)|}$$ 

3. $F$ maps the circle $C = \{z : {|z - z_0|} = \delta\}$ onto a circle of radius $r = {|g(z_0)|}\delta^n$ centered at $f(z_0)$. (This uses the fact that any complex number has an $n^{th}$ root, which one can prove using polar coordinate representations. We omit the details.) Choose $z' \in C$ so that $F(z')$ is on the line segment between the origin and $f(z_0)$. Then 
$${|F(z')|} = {|f(z_0)|} - r$$
We also have 
$${|f(z') - F(z')|} = {|g(z') - g(z_0)|} {|z' - z_0|^n} \lt {|g(z_0)|} \delta^n = r$$ 
according to how we chose $\delta$. We conclude by observing 
$${|f(z')|} \leq {|F(z')|} + {|f(z') - F(z')|} \lt {|f(z_0)|} - r + r = {|f(z_0)|},$$ 
which yields the desired contradiction.  


## In weak foundations

Many proofs rely explicitly on the [[double negation]] rule by first supposing that a polynomial $p$ has no root and deriving a contradiction.  However, the algebraic proof is almost entirely [[constructive mathematics|constructive]].  (Some general results on splitting fields are problematic in constructive algebra, as is the intermediate value theorem in constructive analysis, but their usage in this proof is fine.)

In fact, the only problem is Lemma \ref{sqrt}.  This may fail in a [[topos]] (such as [[sheaves]] over $\mathbb{C}$), since we not be able to find a square root of a complex number $x$ (or element of $K[\sqrt{-1}]$ more generally) if we do not whether or not $x$ is apart from zero (because there is no [[continuous map|continuous]] square-root function).

Most varieties of [[constructive mathematics]] (including that in [[Errett Bishop]]\'s book) nevertheless accept the FTA, because the needed square roots follow from [[weak countable choice]] ($WCC$, which is a consequence of either excluded middle or [[countable choice]]).  A fully choice-free constructive proof also exists for the [[Cauchy real number|Cauchy complex numbers]] (which agree with the [[Dedekind real number|Dedekind complex numbers]] by $WCC$).

[[Fred Richman]] ([1998](#Richman)) has proposed that, in the absence of $WCC$, the FTA should be interepreted as a statement about sets of roots rather than about individual roots.  He constructs a [[complete metric space]] $\hat{M}_n(\mathbb{C})$ which, classically, is the space of $n$-element [[multisets]] of complex numbers (and constructively is the completion of that space) and proves that every complex polynomial $p$ of degree $n$ may be associated with a point in this space in such a way that the $n$ elements of that point (when viewed as a multiset, if possible, and morally in any case) are the $n$ roots of $p$.

## History
 {#History}

The proof was attempted many times before Gauss gave what is accepted as the first proof in his dissertation ([Gauss 1799](#Gauss1799)), although this was not without issues (Gauss 'fixed' this proof almost 50 years later, but the gap was not filled until the 20th century).

All proofs of this fact (of which there are many) require something analytic, in the sense that ordinary algebra will not suffice: one needs to know that the real numbers (or the complex numbers) 'have no algebraic gaps'. For instance, the rational numbers famously don't contain the square root of 2. The cleanest proof I know, due to Artin, that isolates this analytic germ, uses the step-ladder result that the real numbers form what is called a [[real closed field]]. This is essentially saying that non-negative real numbers have square roots, and odd degree polynomials have roots (anyone who has plotted a cubic can appreciate this fact). Alternatively, one can characterise real closed fields as those for whom the Intermediate Value Theorem (IVT) holds for polynomials. Accepting this result (which does need proof), the FTA follows using pure algebra (although not of the high-school sort).

However, it is of interest, partly theoretical, partly for the sake of finding
the bare minimum needed to prove the FTA, to know an elementary proof, namely one that minimises the use of analytic techniques (for instance, the IVT for polynomials follows from the IVT for continuous functions, but that is like killing a mosquito with a bazooka ). Gauss' second proof ([Gauss 1866](#Gauss1866)) is elementary (and predates Artin's by a long time). Since Gauss lacked modern algebraic techniques, some of his proof is laborious, but ([Taylor 85](#Taylor85)) gives a modern gloss. (With some amusing side notes: as Taylor puts it -- 'Gauss takes the opportunity [to] be rude to his inferior contemporaries'.) Gauss' proof, in modern language, takes up less than a page and a half, but this presupposes familiarity with some of the theory of fields (but which is pure algebra). Artin's proof, by comparison, drawing on major theorems can be given in half a page.

It should be noted, in the context of the last statement, that proofs of the FTA can be given, relying on analytic 'bazooka' theorems, that are one sentence. However, to spell out the proofs of the necessary theorems, one needs a course in analysis, of some variety, so one is merely sweeping a lot under a very small rug. 


## References
 {#References}

* {#Gauss1799} [[Carl Gauss]], _Demonstratio nova theorematis functionem algebraicam rationalem integramunius variabilis in factores reales primi vel secundi gradus resolvi posse_, Dissertation, Helmstedt (1799); Werke 3, 1&#8211;30 (1866) ([English transl. pdf](http://www.jon-arny.com/httpdocs/Gauss/Gauss%20Fundamental%20Theorem.pdf)))

* {#Gauss1866} [[Carl Gauss]], _Demonstratio nova altera theorematis omnem functionem algebraicamrationalem integram unius variabilis in factores reales primi vel secundi gradus resolviposse_, Comm. Soc. Reg. Sci. G&#246;ttingen 3, 107&#8211;142 (1816); Werke 3, 33&#8211;56 (1866)

  _Another new proof of the theorem that every integral rational algebraic function of one variable can be resolved into real factors of the first or second degree_ translated by [[Paul Taylor]] and B. Leak (1983) ([web](http://www.paultaylor.eu/misc/gauss-web))

* {#Taylor85} [[Paul Taylor]], _Gauss' Second Proof_, Eureka 45 (1985) 42-47 ([pdf](#http://www.jon-arny.com/httpdocs/Gauss/Eureka-2-aug24.pdf))

*  [[Fred Richman]]; 1998; _The fundamental theorem of algebra: a constructive development without choice_; [Fred Richman's Documents](http://math.fau.edu/richman/HTML/DOCS.HTM)
{#Richman}

A full formalization in the [[Coq]] [[proof assistant]] is in

* Herman Geuvers, [[Freek Wiedijk]], Jan Zwanenburg, A Constructive Proof of the Fundamental Theorem of Algebra without Using the Rationals ([web](http://dl.acm.org/citation.cfm?id=696038))

See also

* MathOverflow, _[Ways to prove the fundamental theorem of algebra](http://mathoverflow.net/questions/10535/ways-to-prove-the-fundamental-theorem-of-algebra)_

[[!redirects fundamental theorem of algebra]]
[[!redirects FTA]]