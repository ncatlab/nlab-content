
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

# The quadratic formula
* table of contents
{: toc}

## Idea

Consider the [[quadratic function]] 

\[ \label{eqn} f(x) \coloneqq a{x}^2 + b{x} + c \]
 
which we wish to find the elements of the [[zero set]]. In certain contexts, the elements of the zero set are given by one or more versions of the quadratic formula.

## Discussion

The coefficients $a, b, c$ of the quadratic function are commonly taken from an [[algebraically closed field]] $K$ of [[characteristic]] $0$, such as the field $\mathbb{C}$ of [[complex numbers]], although any quadratically closed field whose characteristic is not $2$ would work just as well.  Alternatively, the coefficients can be taken from a [[real closed field]] $K$, such as the field $\mathbb{R}$ of [[real numbers]]; then the solutions belong to $K[\mathrm{i}]$.  (Of course, $\mathbb{R}[\mathrm{i}]$ is simply $\mathbb{C}$ again.)  More generally, starting from any [[integral domain]] $K$ whose characteristic is not $2$, the solutions belong to some [[splitting field]] of $K$.  (Of course, there are solutions in *some* splitting field, regardless of the characteristic, but they are not given by the quadratic formula if the characteristic is $2$.)

### Forms of the formula

Explicitly, the zero set of (eq:eqn) may be given by the __usual quadratic formula__
\[ \label{usual} x_\pm = \frac{-b \pm \sqrt{b^2 - 4a{c}}}{2a} ,\]
which works as long as $a \ne 0$.  There is also an __alternate quadratic formula__
\[ \label{alt} x_\pm = \frac{2c}{-b \mp \sqrt{b^2 - 4a{c}}} ,\]
which may be obtained from (eq:usual) by rationalizing the numerator; this works as long as $c \ne 0$.  (Note that $\pm$ and $\mp$ appear here simply to indicate the two [[square roots]] of the determinant $b^2 - 4a{c}$ and how they correspond to the two solutions $x_\pm$; we do not need to have a [[function]] $\sqrt{}$ which always chooses a 'principal' square root.)

These two formulas are reconciled in the [[projective line]] of $K$.  As long as $(a, b, c) \ne (0, 0, 0)$, there are two solutions (which might happen to be equal) in the projective line.  If $a = 0$, then one of these solutions is $\infty$, and (eq:usual) correctly gives us that solution (as long as $b \ne 0$) for one choice of square root, although it gives $0/0$ for the other choice.  Similarly, (eq:alt) correctly gives us $x = 0$ when $c = 0$ and $b \ne 0$, but it does not give us the other root when $c = 0$.  Note that if $a, c = 0$ but $b \ne 0$, then (eq:usual) gives us one root ($\infty$) while (eq:alt) gives us the other ($0$).

So in general, we should be given $a \ne 0$, $b \ne 0$, or $c \ne 0$ for a nondegenerate equation (eq:eqn).  If $a \ne 0$, then we use (eq:usual); if $c \ne 0$, then we use (eq:alt).  Finally, if $b \ne 0$, then we use both; each root will be successfully given by at least one formula for some choice of square root of $b^2 - 4a{c}$.

When the coefficients come from an [[ordered field]] $K$ (which we assume real closed), then we can write down a formula specially for the case when $b \ne 0$.  This is the __numerical analysts\' quadratic formula__
\[ \label{numanal} \begin {gathered}
   \displaystyle x_{\hat{b}} = \frac{2c}{-b - \hat{b}\sqrt{b^2 - 4a{c}}} ;\\
   \displaystyle x_{-\hat{b}} = \frac{-b - \hat{b}\sqrt{b^2 - 4a{c}}}{2a} .\\
\end {gathered} \]
In this formula, $\hat{b}$ is the sign of $b$, that is $b/{|b|}$; also, we must choose a nonnegative principal square root, so that $\sqrt{b^2 - 4a{c}} \lt 0$ in $K$ is avoided (and thus the common denominator of $x_{\hat{b}}$ and numerator of $x_{-\hat{b}}$ is nonzero even if not imaginary).  Despite the name, this formula is not sufficient for all purposes in [[numerical analysis]]; one still needs all three formulas and chooses between them based on whether $a \ne 0$, $b \ne 0$, or $c \ne 0$ is best established.

### Simplified formulas and characteristic $2$

Sometimes one considers the quadratic function
\[f(x) \coloneqq a{x}^2 + 2p{x} + c \]
instead of (eq:eqn); then (eq:usual) simplifies to
\[ \label{simpl} x_\pm = \frac{-p \pm \sqrt{p^2 - a{c}}}a \]
(and similarly for (eq:alt) and (eq:numanal)).

This is valid even in characteristic $2$, but unfortunately then it is fairly useless, since $b = 2p = 0$.  More precisely, if $b = 0$, then (eq:simpl) with $p = 0$ gives the roots $\pm\sqrt{-c/a}$ in any characteristic, but in that case the equation was easy to solve without any formula.  On the other hand, if $b \ne 0$ and $\char K = 2$, then no version of the quadratic formula is applicable, yet this gives no information as to whether the polynomial is [[solvable polynomial|solvable]] and what its roots are if it is.  For example, the quadratic function $f(x) \coloneqq x^2 + x$ has roots $0$ and $1$ in $\F_2$ (or $0$ and $-1$ in any field, as may be found by factoring), while $f(x) \coloneqq x^2 + x + 1$ is not solvable over $\F_2$, yet both have $b^2 - 4a{c} = 1$ and give $0/0$ in both (eq:usual) and (eq:alt) (while (eq:numanal) and (eq:simpl) are directly inapplicable).

## In constructive mathematics

### In real analysis

For some discussion about the quadratic formula in [[constructive analysis|constructive]] [[real analysis]], see [[real quadratic function#ExactZeroes]]. 

### In complex analysis

In constructive mathematics, given a [[set]] $K$, one has to distinguish between mere existence of an element that satisfies some property $P$ on $K$, there exists $x \in K$ such that $P(x)$ holds, and constructive existence of an element that satisfies $P(x)$ via the [[BHK interpretation]] of logic, which is the structure of an element of the set $\{x \in K \vert P(x)\}$. This becomes very important in [[complex analysis]] when talking about square roots. 

In constructive [[complex analysis]], there are multiple notions of the [[fundamental theorem of algebra]]. One version that is provable without any constructive [[taboo]] for the associated [[complex numbers]] $\mathbb{C} = \mathbb{R}[i]/(i^2 + 1)$ of the [[Cauchy real numbers]] (see [Ruitenburg 1991](#Ruitenburg91)) and for any [[sequentially Cauchy complete|Cauchy complete]] [[Archimedean ordered field]] (see [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00)) uses mere existence of a root for non-constant polynomials. Mere existence of a root in the BHK sense is equivalent in strength to every non-constant polynomial function being a [[surjection]], since non-constant polynomial functions are closed under addition of constant polynomial functions. Hence, this implies that for all $a, b, c \in \mathbb{C}$, there exists a root of the quadratic function $z \mapsto a z^2 + b z + c$. 

However, the [[fundamental theorem of algebra]] is not provable if we try to use constructive existence of a root of non-constant polynomials in the sense of the [[BHK interpretation]], that one can construct a specified element $z \in \mathbb{C}$ such that $p(z) = 0$.  Constructive existence of a root in the BHK sense is equivalent in strength to having a [[section]] of every non-constant polynomial function, since non-constant polynomial functions are closed under addition of constant polynomial functions. In the case of the quadratic function $z \mapsto a z^2 + b z + c$, this implies a section of the quadratic function valid on the entirety of the complex numbers. However, such sections cannot be proven to exist on the complex numbers, and in fact can be proven to not exist in certain [[topoi]], such as [[sheaves]] over $\mathbb{R}$, because any such section on the complex numbers, if it exists, is not continuous at the value $- \frac{b}{2a}$ where the [[discriminant]] $b^2 - 4a c$ is equal to zero, and it is consistent for all functions on the complex numbers to be continuous. The problem here is the failure of some amount of choice, that since the quadratic function $z \mapsto a z^2 + b z + c$ is a surjection on the [[complex numbers]], one can construct a [[section]] of $z \mapsto a z^2 + b z + c$. 

In light of this, one can instead interpret the constructive FTA as a statement about sets of roots rather than about individual roots, an interpretation that dates from [Richman 2000](#Richman00). He constructs a [[complete metric space]] $\hat{M}_n(\mathbb{C})$ which, classically, is the space of $n$-element [[multisets]] of complex numbers (and constructively is the completion of that space) and proves that every complex polynomial function $p$ of degree $n$ may be associated with a point in this space in such a way that the $n$ elements of that point (when viewed as a multiset, if possible, and morally in any case) are the $n$ roots of $p$. The quadratic formula is then a [[partial function]] 
$$(a, b, c) \mapsto \frac{-b \pm\sqrt{b^2 - 4a c}}{2a}:\mathbb{C}^3 \to \hat{M}_2(\mathbb{C})$$ 
which takes complex numbers $a, b, c \in \mathbb{C}$, where $a$ is apart from zero, to a point 
$$\frac{-b \pm\sqrt{b^2 - 4a c}}{2a} \in \hat{M}_2(\mathbb{C})$$ 
that represents the set of roots of the quadratic function $a z^2 + b z + c$. 

## See also

* [[quadratic function]]

* [[zero locus]]

* [[completing the square]]

* [[real quadratic formula]]

## References


* {#Ruitenburg91} [[Wim Ruitenburg]]: *Constructing Roots of Polynomials over the Complex Numbers*, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract **84** Centre for Mathematics and Computer Science, Amsterdam (1991) 107–-128 &lbrack;[pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf), [[Ruitenburg-Roots.pdf:file]]&rbrack;

* {#GWZ00} Herman Geuvers, Freek Wiedijk, Jan Zwanenburg, *A Constructive Proof of the Fundamental Theorem of Algebra without using the Rationals*, TYPES '00: Selected papers from the International Workshop on Types for Proofs and Programs, Pages 96 - 111, 08 December 2000 &lbrack;[web](https://dl.acm.org/doi/10.5555/646540.696038), [pdf](https://www.cs.ru.nl/F.Wiedijk/pubs/kneser.pdf)&rbrack;

* {#Richman00} [[Fred Richman]], *The fundamental theorem of algebra: a constructive development without choice*. Pacific Journal of Mathematics **196** 1 (2000) 213–230 &lbrack;[doi:10.2140/pjm.2000.196.213](http://dx.doi.org/10.2140/pjm.2000.196.213), [pdf](https://msp.org/pjm/2000/196-1/pjm-v196-n1-p10-p.pdf)&rbrack;



[[!redirects quadratic formula]]
[[!redirects quadratic formulas]]
[[!redirects quadratic formulae]]
[[!redirects quadratic formulæ]]
