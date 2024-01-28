
# Square roots
* table of contents
{: toc}

## Definitions

If $K$ is a [[magma]], such as a [[monoid]], (which we write multiplicatively) and $x$ is an element of $K$, then the element $x^2$ is the __square__ of $x$.  Conversely, if $x^2 = y$, then $x$ is a __square root__ of $y$.

If $K$ is an [[integral domain]], then (in [[classical mathematics]]) $x$ and $-x$ are the only square roots of $x^2$.  If $y$ has a square root, then we often denote its square roots together as $\pm\sqrt{y}$, although there is no meaning of $\sqrt{y}$ itself.

If $K$ is a [[linearly ordered field]], then every element $y$ has a unique nonnegative square root if it has a square root at all; this is the __principal square root__ of $y$ and denoted $\sqrt{y}$.


## In constructive analysis

In [[constructive mathematics]] (here specifically: [[constructive analysis]]), it is not provable that $x$ and $-x$ are the only square roots of $x^2$.  In the [[ordered field]] of [[real numbers]], for example, the [[absolute value]] ${|x|}$ (like $-{|x|}$, for that matter) is also a square root of $x^2$, yet it is not constructively provable that ${|x|} = x$ or ${|x|} = -x$.  Without using the [[lesser limited principle of omniscience]], if $x$ is close to [[zero]] (and we do not yet know whether it is exactly zero), we cannot decide whether $x$ is nonnegative (so that ${|x|} = x$) or nonpositive (so that ${|x|} = -x$).

However, in any [[linearly ordered field]] with an [[absolute value]] (including any [[real-closed field]]), we still have a unique [[nonnegative number|nonnegative]] square root of $x^2$, which is in fact ${|x|}$.  Thus, we can still use the notation $\sqrt{y}$, but we cannot prove that every square root of $y$ is one of $\pm\sqrt{y}$.  However, we can prove, in any integral domain even, that if $x \neq \sqrt{y}$ and $x \neq -\sqrt{y}$, then $x^2 \neq y$.  (We are using the weak notions of field and integral domain so that $\mathbb{R}$ will be an example.)

If we accept results in the [[complex numbers]] (or in $K[\mathrm{i}]$ for $K$ any real-closed field), then every element of $K$ has a square root.  Even if $y$ is close to zero, we can still use
$$ \sqrt{y} \coloneqq \sqrt{\frac{{|y|} + y}2} + \sqrt{\frac{{|y|} - y}2}\mathrm{i} $$
to construct a square root of $y$.  However, we *cannot* prove that every complex number has a square root in the [[internal language]] of an arbitrary [[W-topos]], although [[weak countable choice]] is enough to prove this.  (See [Richman (1998)](#Richman).)  A counterexample is the topos of [[sheaves]] on the [[real line]], since there is no [[continuous map|continuous]] function $\sqrt{}\colon U \to \mathbb{C}$ for $U$ any [[neighbourhood]] of $0$ in $\mathbb{C}$.  This is important for interpreting the [[quadratic formula]].

+-- {: .query}
How much choice is needed to prove that every element of $K[\mathrm{i}]$ has a square root, where $K$ is *any* real-closed field?  Maybe [[COSHEP]] will do?
=--

Note that there is never any trouble finding a square root of $y$ if we assume that $y \neq 0$, nor (obviously) is there any trouble if we assume that $y = 0$.  Accordingly, the classical results hold for [[discrete fields]] and [[integral domain|discrete integral domains]], but this doesn\'t apply constructively to analysis.


## Related concepts

* [[root]]

* **square root**

* [[root of unity]]

* [[real square root function]]

* [[Euclidean field]]

## References

* [[Fred Richman]], *The fundamental theorem of algebra: a constructive development without choice*. Pacific Journal of Mathematics **196** 1 (2000) 213–230 &lbrack;[doi:10.2140/pjm.2000.196.213](http://dx.doi.org/10.2140/pjm.2000.196.213), [pdf](https://msp.org/pjm/2000/196-1/pjm-v196-n1-p10-p.pdf)&rbrack;

More generally, square roots of [[positive operator|positive]] [[self-adjoint operators]]:

* Zoltán Sebestyén, Zsigmond Tarcsay, *On the square root of a positive selfadjoint operator*, Period Math Hung **75**  (2017) 268–272 &lbrack;[doi:10.1007/s10998-017-0192-1](https://doi.org/10.1007/s10998-017-0192-1)&rbrack;


[[!redirects square root]]
[[!redirects square roots]]

[[!redirects principal square root]]
[[!redirects principal square roots]]
