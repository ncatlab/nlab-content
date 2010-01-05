## Idea

A Banach space is both a [[vector space]] and a [[metric space]], in a compatible way.  The finite-dimensional examples are all of the form $\mathbb{R}^n$, which is quite familiar; the tricky bit is to let the dimension be infinite.  Examples may be drawn from [[measure theory]], [[Hilbert space]]s, and spaces of [[sequence]]s.

## Definitions

Let $V$ be a [[vector space]] over the field of [[real number]]s.  (One can generalise the choice of [[field]] somewhat.)  A **pseudonorm** (or **seminorm**) on $V$ is a function
$$ \| - \|: V \to \mathbb{R} $$
such that:

1.  $ \|0\| \leq 0 $;
1.  $ \|r v\| = |r| \|v\| $ (for $r$ a [[scalar]] and $v$ a vector);
1.  $ \|v + w\| \leq \|v\| + \|w\| $.

It follows from the above that $\|v\| \geq 0$; in particular, $\|0\| = 0$.  A **norm** is a pseudonorm that satisfies a converse to this: $v = 0$ if $\|v\| = 0$.

A norm on $V$ is **complete** if, given any infinite [[sequence]] $(v_1, v_2, \ldots)$ such that
\[ \label{Cauchy} \lim_{m,n\to\infty} \left\| \sum_{i=m}^{m+n} v_i \right\| = 0 ,\]
there exists a (necessarily unique) **sum** $S$ such that
\[ \label{converge} \lim_{n\to\infty} \left\| S - \sum_{i=1}^n v_i \right\| = 0 ;\]
we write
$$ S = \sum_{i=1}^\infty v_i $$
(with the right-hand side undefined if no such sum exists).

Then a **Banach space** is simply a vector space equipped with a complete norm.  As in the real line, we have in a Banach space that
$$ \left\| \sum_{i=1}^\infty v_i \right\| \leq \sum_{i=1}^\infty \|v_i\| ,$$
with the left-hand side guaranteed to exist if the right-hand side exists as a finite real number (but the left-hand side may exist even if the right-hand side diverges, the usual distinction between absolute and conditional convergence).

### Banach spaces as metric spaces

The three axioms for a pseudonorm are very similar to the three axioms for a pseudo[[metric space|metric]].

Indeed, in any pseudonormed vector space, let the **distance** $d(v,w)$ be
$$ d(v,w) = \|w - v\| .$$
Then $d$ is a pseudometric.  Conversely, given any pseudometric $d$ on a vector space $V$, let $\|v\|$ be
$$ \|v\| = d(0,v) .$$
Then $\|-\|$ satisfies the axioms (1--3) for a pseudonorm, except that it may satisfy (2) only for $r = \pm 1$.  It will actually be a pseudonorm iff the pseudometric satisfies a homogeneity rule:
$$ d(r v,r w) = |r| d(v,w) .$$
Thus pseudonorms correspond precisely to homogeneous pseudometrics.

Similarly, norms correspond to homogenous metrics and complete norms correspond to complete homogeneous metrics.  Indeed, (eq:Cauchy) says that the sequence of partial sums is a [[Cauchy sequence]], while (eq:converge) says that the sequence of partial sums converges to $S$.

Thus a Banach space may equivalently be defined as a vector space equipped with a complete homogeneous metric.  Actually, one usually sees a sort of hybrid approach: a Banach space is a normed vector space whose corresponding metric is complete.

### Morphisms of Banach spaces

If $V$ and $W$ are pseudonormed vector spaces, then the **norm** of a linear function $f: V \to W$ may be defined in either of these equivalent ways:

*  $ \|f\| = \sup \{ \|f v\| \;|\; \|v\| \leq 1 \} $;
*  $ \|f\| = \inf \{ r \;|\; \forall{v},\; \|f v\| \leq r \|v\| \} $.

(Some other forms are sometimes seen, but these may break down in degenerate cases.)

For finite-dimensional spaces, any linear map has a well-defined finite norm.  In general, the following are equivalent:

*  $f$ is continuous (as measured by the pseudometrics on $V$ and $W$) at $0$;
*  $f$ is continuous;
*  $f$ is uniformly continuous;
*  $\|f\|$ is finite.

In this case, we say that $f$ is **bounded**.  (In [[constructive mathematics]], it is necessary to further require that $\|f\|$ be a located real number.)

The bounded linear maps from $V$ to $W$ themselves form a pseudonormed vector space $\mathcal{B}(V,W)$.  This will be a Banach space if (and, except for degenerate cases of $V$, only if) $W$ is a Banach space.  In this way, the category $Ban$ of Banach spaces is a [[closed category]] with $\mathbb{R}$ as the unit.

The clever reader will note that we have not yet defined $Ban$ as a category!  Na&#239;vely, one might accept all bounded linear maps between Banach spaces as morphisms, but this doesn\'t give a good notion of [[isomorphism]].  Instead, we take a morphism to be a **short** linear map: a linear map $f$ such that $\|f\| \leq 1$.  Then the isomorphisms are the (surjective) linear isometries.

Note that this makes the 'underlying set' (in the sense of $Ban$ as a [[concrete category]] like any closed category) of a Banach space its (closed) **unit ball**
$$ Hom_Ban(\mathbb{R},V) \cong \{ v \;|\; \|v\| \leq 1 \} $$
rather than the set of all vectors in $V$ (the underlying set of $V$ as a vector space).

## Examples

Many examples of Banach spaces are parametrised by an exponent $1 \leq p \leq \infty$.  (Sometimes one can also try $0 \leq p \lt 1$, but these generally don\'t give Banach spaces.)

*  $\mathbb{R}^n$ is a Banach space with
   $$ \|(x_1,\ldots,x_n)\|_p = \root p {\sum_i |x_i|^p} .$$
   (We can allow $p = \infty$ by taking a limit; the result is that $\|x\|_\infty = \max_i |x_i|$.)  Every finite-dimensional Banach space is isomorphic to this for some $n$ and $p$; in fact, once you fix $n$, the value of $p$ is irrelevant up to isomorphism.
*  Let $l^p$ be the set of infinite [[sequence]]s $(x_1,x_2,\ldots)$ of real numbers such that
   $$ \|(x_1,x_2,\ldots)\|_p = \root p {\sum_i |x_i|^p} $$
   exists as a finite real number.  (The only question is whether the sum converges.  Again $p = \infty$ is a limit, with the result that $\|x\|_\infty = \sup_i |x_i|$.)  Then $l^p$ is a Banach space with that norm.  These are all versions of $\mathbb{R}^\infty$, but they are no longer isomorphic for different values of $p$.
*  More generally, let $A$ be any [[set]] and let $l^p(A)$ be the set of [[function]]s $f$ from $A$ to $\mathbb{R}$ such that
   $$ \|f\|_p = \root p {\sum_{x: A} |f(x)|^p} $$
   exists as a finite real number.  (Again, $\|f\|_\infty = \sup_{x: A} |f(x)|$.)  Then $l^p(A)$ is a Banach space.  (This example includes the previous examples, for $A$ a countable set.)
*  On any [[measure space]] $X$, let $\mathcal{L}^p(X)$ be the set of measurable almost-everywhere-defined real-valued functions on $X$ such that
   $$ \|f\|_p = \root p {\int |f|^p} $$
   exists as a finite real number.  (Again, the only question is whether the integral converges.  And again $p = \infty$ is a limit, with the result that $\|f\|_\infty$ is the essential supremum of $|f|$.)  As such, $\mathcal{L}^p(X)$ is a complete pseudonormed vector space; but we identify functions that are equal almost everywhere to make it into a Banach space.  (This example includes the previous examples, for $X$ a set with counting measure.)
*  Any [[Hilbert space]] is Banach space; this includes all of the above examples for $p = 2$.

## Categorial operations on Banach spaces

The category of Banach spaces is [[complete category|small complete]], [[cocomplete category|small cocomplete]], and [[symmetric monoidal closed category|symmetric monoidal closed]] with respect to its standard internal hom (described at [[internal hom]]). Some details follow.

* The category of Banach spaces admits small [[product]]s. Given a small family of Banach spaces $\{X_\alpha\}_{\alpha \in A}$, its product in $Ban$ is the subspace of the vector-space product
$$\prod_{\alpha \in A} X_\alpha$$
consisting of $A$-tuples $\langle x_\alpha \rangle$ which are _uniformly_ bounded (i.e., there exists $C$ such that $\forall \alpha \in A: \|x_\alpha\| \leq C$), taking the least such upper bound as the norm of $\langle x_\alpha \rangle$. This norm is called the $\infty$-norm; in particular, the product of an $A$-indexed family of copies of $\mathbb{R}$ or $\mathbb{C}$ is what is normally denoted as $l^{\infty}(A)$.

* The category of Banach spaces admits [[equalizer]]s. Indeed, the equalizer of a pair of maps $f, g: X \rightrightarrows Y$ in $Ban$ is the [[kernel]] of $f-g$ under the norm inherited from $X$ (the kernel is closed since $f-g$ is continuous, and is therefore complete).

* The category of Banach spaces admits small [[coproduct]]s. Given a small family of Banach spaces $\{X_\alpha\}_{\alpha \in A}$, its coproduct in $Ban$ is the completion of the vector space coproduct 
  $$\bigoplus_{\alpha \in A} X_\alpha$$ 
  with respect to the norm given by
  $$ \left\| \bigoplus_{s \in S} x_s \right\| = \sum_{s \in S} \|x_s\| ,$$
  where $S \subseteq A$ is finite and $\|x_s\|$ denotes the norm of an element in $X_s$. This norm is called the $1$-norm; in particular, the coproduct of an $A$-indexed family of copies of $\mathbb{R}$ or $\mathbb{C}$ is what is normally denoted as $l^1(A)$.

* The category of Banach spaces admits [[coequalizer]]s. Indeed, the coequalizer of a pair of maps $f, g: X \rightrightarrows Y$ is the [[cokernel]] of $f-g$ under the quotient norm (in which the norm of a coset $y + C$ is the minimum norm attained by elements of $y + C$; here $C$ is the [[image]] $(f-g)(X)$, which is closed). It is standard that the quotient norm on $Y/C$ is complete given that the norm on $Y$ is complete.

To describe the tensor product of two Banach spaces (making $Ban$ symmetric monoidal closed with respect to its usual internal hom), we invoke a standard consequence of the [[uniform boundedness principle]]:

* Let $X, Y$ be Banach spaces, let $Z$ be a (pseudo)normed vector space, and suppose $f: X \times Y \to Z$ is separately linear and continuous (meaning each $f(x, -): Y \to Z$ and $f(-, y): X \to Z$ is linear and continuous). Then there is a uniform bound $C$ such that 
  $$ f(x, y) \leq C\|x\|\cdot\|y\| .$$

As a result, we may define $X \otimes_{Ban} Y$ by completing the ordinary vector space tensor product with respect to a suitable norm. In detail, let $F(X \times Y)$ be the free vector space generated by the set $X \times Y$, with norm on a typical element defined by 
$$ \left\| \sum_{1 \leq i \leq n} a_i (x_i \otimes y_i) \right\| = \sum_{1 \leq i \leq n} |a_i| \|x_i\|\cdot\|y_i\| ,$$
and let $\overline{F}(X \times Y)$ denote its completion with respect to this norm. Then take the cokernel of $\overline{F}(X \times Y)$ by the closure of the subspace spanned by the obvious bilinear relations. This quotient is $X \otimes_{Ban} Y$.

To be described:
*  duals ($p + q = p q$); 
*  completion ($Ban$ is a [[reflective subcategory]] of $PsNVect$).
*  $Ban$ as a (somewhat larger) category with duals.


[[!redirects Ban]]
[[!redirects Banach spaces]]
[[!redirects normed vector space]]
[[!redirects pseudonormed vector space]]
[[!redirects seminormed vector space]]