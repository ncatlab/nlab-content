
# Square roots
* table of contents
{: toc}

## Definitions

If $K$ is a [[magma]], such as a [[monoid]], (which we write multiplicatively) and $x$ is an element of $K$, then the element $x^2$ is the __square__ of $x$.  Conversely, if $x^2 = y$, then $x$ is a __square root__ of $y$.

If $K$ is an [[integral domain]], then (in [[classical mathematics]]) $x$ and $-x$ are the only square roots of $x^2$.  If $y$ has a square root, then we often denote its square roots together as $\pm\sqrt{y}$, although there is no meaning of $\sqrt{y}$ itself.

If $K$ is a [[linearly ordered field]], then every element $y$ has a unique nonnegative square root if it has a square root at all; this is the __principal square root__ of $y$ and denoted $\sqrt{y}$.


## In constructive analysis

In [[constructive mathematics]] (here specifically: [[constructive analysis]]), it is not provable that $x$ and $-x$ are the only square roots of $x^2$. In the [[ordered field]] of [[real numbers]], for example, the [[absolute value]] ${|x|}$ (like $-{|x|}$, for that matter) is also a square root of $x^2$, yet it is not constructively provable that ${|x|} = x$ or ${|x|} = -x$.  Without using the [[lesser limited principle of omniscience]], if $x$ is close to [[zero]] (and we do not yet know whether it is exactly zero), we cannot decide whether $x$ is nonnegative (so that ${|x|} = x$) or nonpositive (so that ${|x|} = -x$).

However, in any [[linearly ordered field]] with an [[absolute value]] (including any [[real-closed field]]), we still have a unique [[nonnegative number|nonnegative]] square root of $x^2$, which is in fact ${|x|}$.  Thus, we can still use the notation $\sqrt{y}$, but we cannot prove that every square root of $y$ is one of $\pm\sqrt{y}$.  However, we can prove, in any integral domain even, that if $x \neq \sqrt{y}$ and $x \neq -\sqrt{y}$, then $x^2 \neq y$.  (We are using the weak notions of field and integral domain so that $\mathbb{R}$ will be an example.)

If we accept results in the [[complex numbers]], the [[fundamental theorem of algebra]] is provable without any constructive [[taboo]] for the associated [[complex numbers]] $\mathbb{C} = \mathbb{R}[i]/(i^2 + 1)$ of the [[Cauchy real numbers]] (see [Ruitenburg 1991](#Ruitenburg91)) and for any [[sequentially Cauchy complete|Cauchy complete]] [[Archimedean ordered field]] (see [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00)), implying that every complex quadratic function has a square root. More generally, when working in $K[\mathrm{i}]$ for $K$ any real-closed field, then every element $a$ of $K$ has a square root in the sense that there exists an element $x$ of $K[i]$ such that $x^2 = a$, since $K[i]$ is a subfield of the complex numbers. 

However, we *cannot* prove that every complex number has a *principal square root*.  (See [Richman 2000](#Richman00).) The principal square root cannot be proven to exist on the complex numbers, and in fact can be proven to not exist in certain [[topoi]], such as [[sheaves]] over $\mathbb{R}$, because the principal square root on the complex numbers, if it exists, is not continuous at the branch cut, and it is consistent for all functions on the complex numbers to be continuous. The problem here is the failure of some amount of choice, that since the squaring function $z \mapsto z^2$ is a surjection on the [[complex numbers]], one can construct a [[right inverse]] of $z \mapsto z^2$. In general, any principal square root is only a [[partial function]] in [[neutral constructive mathematics]]. This is important for interpreting the [[quadratic formula]]. 

Note that there is never any trouble finding a principal square root of $y$ if we assume that $y \neq 0$, nor (obviously) is there any trouble if we assume that $y = 0$.  Accordingly, the classical results hold for [[discrete fields]] and [[integral domain|discrete integral domains]], but this doesn\'t apply constructively to analysis.

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
