
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Boman\'s Theorem
* table of contents
{: toc}

## Idea

In considering certain types of [[generalized smooth spaces]], one may try to describe the [[smooth structure]] on a space by specifying the smooth [[curves]].  Boman\'s Theorem shows that this is sufficient to describe the smooth structure on a [[smooth manifold]].


## Statement

The following theorem appears (as Theorem 1) in the paper [Boman 1967](#Boman1967), where it is first proved, by Jan Boman:
+-- {: .num_theorem}
###### Theorem
Let $f$ be a function from $\mathbb{R}^d$ to $\mathbb{R}$, and assume that the composed function $f \circ u$ belongs to $C^\infty(\mathbb{R},\mathbb{R})$ for every $u \in C^\infty(\mathbb{R}, \mathbb{R}^d)$.  Then $f \in C^\infty(\mathbb{R}^d, \mathbb{R})$.
=--
Here, $\mathbb{R}^d$ is a [[Cartesian space]], and $C^\infty(X,Y)$ is the set of [[smooth maps]] from $X$ to $Y$.

The theorem is quoted with a proof in [Kriegl & Michor 1997](#KrieglMichor1997) (Theorem 3.4).


## Less than smooth functions

This theorem is for [[smooth functions]], that is $C^\infty$ maps.  A similar theorem could be stated for [[continuous functions]], that is $C^0$ maps.  The situation is slightly less than ideal, however, for [[continuously differentiable functions]], that is $C^1$ maps, or more generally $C^p$ maps for $0 \lt p \lt \infty$.

[Boman 1967](#Boman1967) has this as part of Theorem 2:
+-- {: .num_theorem}
###### Theorem
Let $f$ be a function from $\mathbb{R}^d$ to $\mathbb{R}$, and assume that the composed function $f \circ u$ belongs to $C^p(\mathbb{R},\mathbb{R})$ for every $u \in C^\infty(\mathbb{R}, \mathbb{R}^d)$.  Then $f \in C^{p-1}(\mathbb{R}^d, \mathbb{R})$.
=--
Note that $p$ has become $p - 1$ in the conclusion.  (Boman\'s full Theorem 2 gives stronger results involving [[Lipschitz continuous function|Lipschitz conditions]].)

Boman\'s Theorem 8 gives the desired result if we use parametrized [[surfaces]] instead of curves:
+-- {: .num_theorem}
###### Theorem
Let $f$ be a function from $\mathbb{R}^d$ to $\mathbb{R}$, and assume that the composed function $f \circ u$ belongs to $C^p(\mathbb{R}^2,\mathbb{R})$ for every $u \in C^\infty(\mathbb{R}^2, \mathbb{R}^d)$.  Then $f \in C^p(\mathbb{R}^d, \mathbb{R})$.
=--
Here we have $\mathbb{R}^2$ instead of $\mathbb{R}$ as the domain of $u$.

Boman\'s Theorem 3 guarantees such counterexamples as
$$ f\colon x, y \mapsto \frac{y^3}{x^2 + y^2} $$
(continuously extended so that $f(0,0) = 0$).  Given any smooth ---or even $C^1$--- curve $u\colon t \mapsto (g(t), h(t))$, it may be shown (by several tedious cases) that $(f \circ u)'$ is continuous.  Nevertheless, $f$ is _not_ $C^1$ at $(0,0)$.  (The general pattern, expressed in Boman\'s Theorem 10, is to use a non-polynomial function that is homogeneous in degree $p$ and $C^p$ except at $\vec{0}$.  So long as $d \gt 1$, such functions exist.)  Additionally, $(f \circ u)'$ exists even if $u$ is merely [[differentiable map|differentiable]], but $f$ is not even differentiable at $(0,0)$.

This does not contradict the well known theorem (often taken as a definition!) that a function is $C^1$ already if only its [[partial derivatives]] are continuous; while the partial derivatives of $f$ may be expressed as derivatives of $f \circ u$ for appropriate smooth $u$ (taken from a space of curves identifiable with $d \mathbb{R}^d$), the continuity of the partial derivatives requires not that $(f \circ u)'(t)$ be continuous in $t$ (although this will follow) but that it be continuous in $u$.


## References

* Jan Boman, _Differentiability of a function and of its compositions with functions of one variable_, _Math. Scand._ **20** 1967 249&#8211;268, [MR237728](http://www.ams.org/mathscinet-getitem?mr=237728) [pdf](http://www.mscand.dk/article/view/10835/8856)
  {#Boman1967}

* Andreas Kriegl, Peter W. Michor, _The convenient setting of global analysis_, Math. Surveys and Monographs __53__, Amer. Math. Soc. 1997. x+618 pp. ISBN: 0-8218-0780-3 [html](http://www.ams.org/publications/online-books/surv53-index) [MR1471480](http://www.ams.org/mathscinet-getitem?mr=1471480)
  {#KrieglMichor1997}


[[!redirects Boman's theorem]]
[[!redirects Boman's Theorem]]
[[!redirects Boman's theorems]]
[[!redirects Boman's Theorems]]
[[!redirects Boman\'s theorem]]
[[!redirects Boman\'s Theorem]]
[[!redirects Boman\'s theorems]]
[[!redirects Boman\'s Theorems]]
[[!redirects Boman's theorem]]
[[!redirects Boman's Theorem]]
[[!redirects Boman's theorems]]
[[!redirects Boman's Theorems]]
[[!redirects Boman theorem]]
[[!redirects Boman Theorem]]
[[!redirects Boman theorems]]
[[!redirects Boman Theorems]]
