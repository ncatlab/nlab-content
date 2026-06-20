
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Square roots
* table of contents
{: toc}

## Definitions

Let $(K, \cdot)$ be a [[magma]] [[object]] in [[abelian groups]] or [[commutative monoids]], such as a [[ring]] or a [[rig]]. Given an element $x \in K$, the element $x^2 = x \cdot x$ is the **square** of $x$. Conversely, given elements $x \in K$ and $y \in K$, if $x^2 = y$, then $x$ is a **square root** of $y$. 

### Square roots as functions

Alternatively, the term *square root* is also used to denote a [[partial function]] that is a [[right inverse]] of the squaring function in $K$. Let $K_{\mathrm{sq}}$ be a subset of $K$ such that for all $x \in K_{\mathrm{sq}}$ there exists $y \in K$ such that $x^2 = y$. A **square root** is a function $f:K_{\mathrm{sq}} \to K$ such that $f(x)^2 = x$ for all $x \in K_{\mathrm{sq}}$. If the squaring function $x \mapsto x^2$ is [[split epimorphism|split]] [[surjective]], then there exists a square root function that is a [[total function]] on all of $K$. 

One sometimes fixes a function $\sqrt{(-)}:K_{\mathrm{sq}} \to K$ on $K$; this is the **principal square root** of $K$. For example, in [[complex analysis]] the principal square root on the [[complex numbers]] is defined as $z \mapsto \vert z \vert e^{\frac{i \arg(z)}{2}}$, where $\arg(z)$ is defined such that $-\frac{\tau}{2} \lt \arg(z) \leq \frac{\tau}{2}$ for all complex numbers $z$. 

## Examples

* The square root of every element in a [[boolean ring]] and more generally a [[multiplicatively idempotent rig]] exists and is unique because the multiplicative monoid is [[idempotent]]. The [[identity function]] is thus a square root function defined on the entirety of the ring or rig. 

* Since both $1$ and $-1$ are square roots of $1$ in every [[ring]], that the square root of $1$ is unique implies that the ring has [[characteristic]] $2$, where $1 = -1$. 

* The square root of every non-negative [[real number]] exists and is unique on the [[rig]] of non-negative [[real numbers]]. 

* If $K$ is an [[integral domain]], then (in [[classical mathematics]]) $x$ and $-x$ are the only square roots of $x^2$. If $y$ has a square root, then we often denote its square roots together as $\pm\sqrt{y}$, where the symbols $\pm\sqrt{y}$ is just notation and doesn't necessarily have an official definition. However, if $K$ has a principal square root function, we can define $\pm\sqrt{(-)}$ to be a function $\pm\sqrt{(-)}:K_{\mathrm{sq}} \to K^2$ such that $\pm\sqrt{y} = (\sqrt{y}, -\sqrt{y})$.

## In constructive mathematics

In [[constructive mathematics]] (here specifically: [[constructive analysis]]), it is not provable that $x$ and $-x$ are the only square roots of $x^2$. In the [[ordered field]] of [[real numbers]], for example, the [[absolute value]] ${|x|}$ (like $-{|x|}$, for that matter) is also a square root of $x^2$, yet it is not constructively provable that ${|x|} = x$ or ${|x|} = -x$.  Without using the [[lesser limited principle of omniscience]], if $x$ is close to [[zero]] (and we do not yet know whether it is exactly zero), we cannot decide whether $x$ is nonnegative (so that ${|x|} = x$) or nonpositive (so that ${|x|} = -x$).

However, in any [[linearly ordered field]] with an [[absolute value]] (including any [[real-closed field]]), we still have a unique [[nonnegative number|nonnegative]] square root of $x^2$, which is in fact ${|x|}$.  Thus, we can still use the notation $\sqrt{y}$, but we cannot prove that every square root of $y$ is one of $\pm\sqrt{y}$.  However, we can prove, in any integral domain even, that if $x \neq \sqrt{y}$ and $x \neq -\sqrt{y}$, then $x^2 \neq y$.  (We are using the weak notions of field and integral domain so that $\mathbb{R}$ will be an example.)

Note that there is never any trouble finding a principal square root of $y$ if we assume that $y \neq 0$, nor (obviously) is there any trouble if we assume that $y = 0$.  Accordingly, the classical results hold for [[discrete fields]] and [[integral domain|discrete integral domains]], but this doesn\'t apply constructively to analysis.

### In complex analysis

In constructive mathematics, given a [[set]] $K$, one has to distinguish between mere existence of an element that satisfies some property $P$ on $K$, there exists $x \in K$ such that $P(x)$ holds, and constructive existence of an element that satisfies $P(x)$ via the [[BHK interpretation]] of logic, which is the structure of an element of the set $\{x \in K \vert P(x)\}$. This becomes very important in [[complex analysis]] when talking about square roots. 

In constructive [[complex analysis]], there are multiple notions of the [[fundamental theorem of algebra]]. One version uses mere existence of a root for non-constant polynomials and is provable without any constructive [[taboo]] for the associated [[complex numbers]] $\mathbb{C} = \mathbb{R}[i]/(i^2 + 1)$ of the [[Cauchy real numbers]] (see [Ruitenburg 1991](#Ruitenburg91)). 
[Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) considers the case for any [[sequentially Cauchy complete|Cauchy complete]] [[Archimedean ordered field]], but it is currently unclear whether the proof of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) is actually valid in [[neutral constructive mathematics]] or requires some choice. While the [[Rocq]] formalization of [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00) does not seem to use any choice, [[Toby Bartels]] claims [here](https://nforum.ncatlab.org/discussion/20169/square-root/?Focus=127242#Comment_127242) that the proof of Lemma 5 in the paper itself requires [[dependent choice]], and [Ruitenburg 1991](#Ruitenburg91) states that 

> if we are able to construct a solution $x$ of an equation $f(x) = 0$ over the (Dedekind) reals using topos intuitionism, then $x$ is locally continuous in the parameters of the equation. So, for example, we cannot show the existence of a solution of $X^3 + p X + q = 0$ over the (Dedekind) reals when $(p, q)$ is close to $(0, 0)$, because it would imply the existence of a continuous solution $X(p, q)$ in a neighborhood of $(0, 0)$ [6]. For the same reason we cannot find a solution to the equation $X^2 + c = 0$ over the (Dedekind) complex numbers when c is near 0. 

Mere existence of a root in the BHK sense is equivalent in strength to every non-constant polynomial function being a [[surjection]], since non-constant polynomial functions are closed under addition of constant polynomial functions. Hence, this implies that for all $c \in \mathbb{C}$, there exists a root of the function $z \mapsto z^2 - c$, implying that there exists a square root of $c$ for all $c \in \mathbb{C}$. 

However, the [[fundamental theorem of algebra]] is not provable if we try to use constructive existence of a root of non-constant polynomials in the sense of the [[BHK interpretation]], that one can construct a specified element $z \in \mathbb{C}$ such that $p(z) = 0$.  Constructive existence of a root in the BHK sense is equivalent in strength to having a [[section]] of every non-constant polynomial function, since non-constant polynomial functions are closed under addition of constant polynomial functions. In the case of the squaring function $z \mapsto z^2$, this implies a square root function on the entirety of the complex numbers. Such a square root function is a [[section]] of the squaring function $z \mapsto z^2$ and so cannot be proven to exist on the complex numbers from surjectivity of $z \mapsto z^2$, since the square root on the complex numbers, if it exists, is [[discontinuous]] at zero, which implies the constructive taboo [[analytic WLPO]] for the [[real numbers]] and [[decidable equality]] for the complex numbers. In fact, in certain [[topoi]], such as [[sheaves]] over $\mathbb{C}$, one can prove that there are no square root functions because in those topoi all functions on the complex numbers are continuous. 

In light of this, one can instead interpret the constructive FTA as a statement about sets of roots rather than about individual roots, an interpretation that dates from [Richman 2000](#Richman00). He constructs a [[complete metric space]] $\hat{M}_n(\mathbb{C})$ which, classically, is the space of $n$-element [[multisets]] of complex numbers (and constructively is the completion of that space) and proves that every complex polynomial function $p$ of degree $n$ may be associated with a point in this space in such a way that the $n$ elements of that point (when viewed as a multiset, if possible, and morally in any case) are the $n$ roots of $p$. The square root function is then a function $\pm\sqrt{(-)}:\mathbb{C} \to \hat{M}_2(\mathbb{C})$ which takes each complex number $c \in \mathbb{C}$ to a point $\pm\sqrt{c} \in \hat{M}_2(\mathbb{C})$ that represents the set of square roots of $c$. 

In addition, the principal square root of the complex numbers, defined as $z \mapsto \vert z \vert e^{\frac{i \arg(z)}{2}}$, where $\arg(z)$ is defined such that $-\frac{\tau}{2} \lt \arg(z) \leq \frac{\tau}{2}$ for all complex numbers $z$, is only a [[partial function]] in [[neutral constructive mathematics]]. This is important for interpreting the [[quadratic formula]].

## Related concepts

* [[root]]

* **square root**

* [[root of unity]]

* [[real square root function]]

* [[Euclidean field]]

## References


* {#Ruitenburg91} [[Wim Ruitenburg]]: *Constructing Roots of Polynomials over the Complex Numbers*, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract **84** Centre for Mathematics and Computer Science, Amsterdam (1991) 107–-128 &lbrack;[pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf), [[Ruitenburg-Roots.pdf:file]]&rbrack;

* {#GWZ00} Herman Geuvers, Freek Wiedijk, Jan Zwanenburg, *A Constructive Proof of the Fundamental Theorem of Algebra without using the Rationals*, TYPES '00: Selected papers from the International Workshop on Types for Proofs and Programs, Pages 96 - 111, 08 December 2000 &lbrack;[web](https://dl.acm.org/doi/10.5555/646540.696038), [pdf](https://www.cs.ru.nl/F.Wiedijk/pubs/kneser.pdf)&rbrack;

* {#Richman00} [[Fred Richman]], *The fundamental theorem of algebra: a constructive development without choice*. Pacific Journal of Mathematics **196** 1 (2000) 213–230 &lbrack;[doi:10.2140/pjm.2000.196.213](http://dx.doi.org/10.2140/pjm.2000.196.213), [pdf](https://msp.org/pjm/2000/196-1/pjm-v196-n1-p10-p.pdf)&rbrack;

More generally, square roots of [[positive operator|positive]] [[self-adjoint operators]]:

* Zoltán Sebestyén, Zsigmond Tarcsay, *On the square root of a positive selfadjoint operator*, Period Math Hung **75**  (2017) 268–272 &lbrack;[doi:10.1007/s10998-017-0192-1](https://doi.org/10.1007/s10998-017-0192-1)&rbrack;


[[!redirects square root]]
[[!redirects square roots]]

[[!redirects principal square root]]
[[!redirects principal square roots]]

[[!redirects square root function]]
[[!redirects square root functions]]

[[!redirects principal square root function]]
[[!redirects principal square root functions]]
