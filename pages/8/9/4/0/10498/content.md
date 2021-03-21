
> This entry is about the notion in [[linear algebra]] relating bilinear and quadratic forms. For the notion in [[symplectic geometry]] see at _[[polarization]]_. For polarization of light, see _[[wave polarization]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# The polarization identity
* table of contents
{: toc}

## Idea

Any [[symmetric bilinear form]] $(-) \cdot (-)$ defines a [[quadratic form]] $(-)^2$.  The _polarization identity_ reconstructs the bilinear form from the quadratic form.  More generally, starting from any [[bilinear form]], the polarization identity reconstructs its symmetrization.  A slight variation applies this also to [[sesquilinear forms]], which don\'t require any kind of symmetry to work.  The whole business actually applies to [[bilinear maps]], not just forms (that is, taking arbitrary values, not just values in the [[base field]] or some other [[line]]).  Some kind of linearity is crucial: polarization doesn\'t work without addition (and subtraction); we must also be able to divide by $2$ for the best results.  It is also possible to generalize from quadratic forms to higher-order [[homogenous form]]s if we can divide by larger integers.


## Statements

Let $R$ be a [[commutative ring]].  Let $V$ and $W$ be $R$-[[modules]], and let $m\colon V \times V \to W$ be a [[bilinear map]]; that is, we have an $R$-module [[homomorphism]] $V \otimes V \to W$.  Let $Q\colon V \to W$ be the [[quadratic map]] given by $Q(x) = m(x,x)$; this is *not* an $R$-module homomorphism.

Then we have:

* the _[[parallelogram law]]_: $2 Q(x) + 2 Q(y) = Q(x + y) + Q(x - y)$, and
* the __polarization identity__: $2 m(x,y) + 2 m(y,x) = Q(x + y) - Q(x - y)$.

Writing $Q(x)$ as $x^2$ and $m(x,y)$ as $x y$, these read:

* $2 x^2 + 2 y^2 = (x + y)^2 + (x - y)^2$,
* $2 x y + 2 y x = (x + y)^2 - (x - y)^2$.

The polarization identity also has these alternative forms:

* $x y + y x = (x + y)^2 - x^2 - y^2$,
* $x y + y x = x^2 + y^2 - (x - y)^2$;

these may derived by adding or subtracting the parallelogram law and the first polarization identity assuming that multiplication by $2$ is cancellable in $W$; they can also both be proved directly without any such assumption.

The most general form of such expressions is
$$ k x y + k y x = \sum_i c_i (a_i x + b_i y)^2 $$
for any [[finite sequence]] of triples $(a,b,c)$ from $R$ such that
$$ \sum_i a_i ^ 2 c_i = \sum_i b_i ^ 2 c_i = 0 ,$$
if
$$ k = \sum_i a_i b_i c_i .$$
In the three specific versions of the polarization identity listed above, the values of $a$, $b$, and $c$ are all always $0$, $1$, or $-1$, but there is no reason to restrict ourselves to this or even assume that they are integers (or even rational numbers or more generally members of the [[prime field]] of $R$).  (If we want to allow $R$ to be a [[rig]], then we can use a version of this with sums on both sides of the equation, but that seems like [[centipede mathematics]] since I don\'t know any application of that case.)

Now suppose that $m$ is [[symmetric bilinear map|symmetric]], so that $x y = y x$.  And suppose that multiplication by $2$ is (not merely cancellable but also) invertible in $W$.  (If $1/2 \in R$, then that is more than sufficient.)  Then the polarization identities read:

* $x y = \frac{1}{4} (x + y)^2 - \frac{1}{4} (x - y)^2$,
* $x y = \frac{1}{2} (x + y)^2 - \frac{1}{2} x^2 - \frac{1}{2} y^2$,
* $x y = \frac{1}{2} x^2 + \frac{1}{2} y^2 - \frac{1}{2} (x - y)^2$.

That is, we may recover $m$ from $Q$ (in any of these ways).  The second one is probably the most widely used.  Regardless of the original symmetry of $m$, we may recover its symmetrization $x \circ y = (x y + y x)/2$ (the [[Jordan product]]) in any these ways.  The most general formula for $x \circ y$ is
$$ x \circ y
= \frac{\sum_i c_i (a_i x + b_i y)^2}
{\sum_i 2 a_i b_i c_i} $$
when the sums of $a^2 c$ and $b^2 c$ are zero (as above) and the sum in the denominator is invertible.  (In that case, one could also normalize the $c$s so that the denominator becomes $1$.)  Notice that $2$ must be invertible to have any hope of recovering $m$ or its symmetrization; but we could recover $x y + y x$ without that.

We can also go the other direction: given a quadratic map $Q$, if $2$ is invertible, then any polarization identity defines a symmetric bilinear map $m$; these all agree iff $Q$ obeys the parallelogram law, and then $Q$ may be recovered from this $m$ once more.

If $R$ is a $*$-[[star-ring|ring]], then $m$ could be [[sesquilinear map|sesquilinear]] instead of bilinear.  Then $Q$ would satisfy $Q(t x) = t^* t Q(x)$ (which I don\'t know a term for, maybe 'sesqui-quadratic'? or using whatever\'s Latin for 3/4?) instead of $Q(t x) = t^2 Q(x)$ as for a quadratic map.  Since everything is still bilinear or quadratic over the [[integers]], the parallelogram identity still follows, as do the polarization identities in which only integers appear and before assuming symmetry.  Then *regardless* of whether $m$ is symmetric (or conjugate-symmetric or anything else), we can recover $m$ from $Q$ if $R$ has (in addition to $1/2$) an [[imaginary unit]]: an element $i$ such that $i + i^* = 0$ and $i^* i = 1$.  Specifically,
$$ m(x,y) = \frac{1}{4} Q(x + y) - \frac{1}{4} Q(x - y) - \frac{1}{4} i Q(x + i y) + \frac{1}{4} i Q(x - i y) $$
when $m$ is conjugate-linear in the first variable and linear in the second.  (Swap the signs on the two terms involving $i$ if $m$ is linear in the first variable and conjugate-linear in the second.)  The more general version of this is
$$ m(x,y)
= \frac{\sum_i c_i Q(a_i x + b_i y)}
{\sum_i a_i^* b_i c_i} $$
when
$$ \sum_i a_i^* a_i c_i = \sum_i b_i^* b_i c^i = \sum_i a_i b_i^* c_i = 0 $$
and the denominator is invertible.  (Notice that the last two of these conditions are contradictory if the involution is trivial; or rather, they imply that $R$ is the [[trivial ring]].)


## Examples

This is best known in the case of bilinear and quadratic *forms*, where $W$ is the [[ground ring]] $R$.  Here, $m$ is an [[inner product]], making $V$ into an [[inner product space]], and $Q$ is (the square of) the norm, making $V$ into a [[normed space]].  Instead of abbreviating $m(x,y)$ as $x y$, we might abbreviate it as $\langle x, y \rangle$ (or any other common notation for an inner product) and $Q(x)$ as $\|x\|^2$.  (In the general algebraic context that we are assuming here, $Q$ may not have a [[square root]], much less a canonical 'principal' square root to give meaning to $\|x\|$ alone.  Even assuming that $R$ is the field $\mathbb{R}$ of [[real numbers]], that $Q(x) \geq 0$ is an additional assumption, the [[positive-definite|positive (semi)-definiteness]] of the inner product.)

Besides forms, the general theory also applies to [[commutative algebras]], where $W$ is $V$.  Actually, there is no need for $m$ to be associative; although one rarely studies commutative but [[non-associative algebras]], we have an exception with [[Jordan algebras]].  Although the Jordan identity is simpler to express in terms of the multiplication operation (as usual), the application to [[quantum mechanics]] may be more easily motivated through the squaring operation (since the square of an [[observable]] has a more obvious meaning than the Jordan product of two observables), and the polarization identities allow us to recover multiplication from squaring (and subtraction and division by $2$).

When $V = W$ is a $*$-[[*-algebra|algebra]] over $R$, then although the usual multiplication is bilinear, we can also define a (nonassociative) sesquilinear operator $m$ by explicitly taking the adjoint of one argument: $m(x,y) \coloneqq x^* y$.  When $R$ is a complete [[normed field]] and $V = W$ is a $C^*$-[[C-star algebra|algebra]], the resulting 3/4-quadratic operator $Q$ must have a principal square root, but now we write $Q(x) \coloneqq x^* x$ as $|x|^2$ rather than $\|x\|^2$, which is taken.  (However, $|{-}|$ is not an [[absolute value]], since it\'s not multiplicative, only submultiplicative.)


## Higher order

Let $R, V, W$ be as before.  Let $p$ be a [[natural number]], and let $Q\colon V \to W$ be homogeneous of degree $p$; that is,
$$ Q(t v) = t^p Q(v) .$$
We wish to turn $Q$ into a symmetric [[multilinear map]] $m$ of rank $p$ (so $m\colon \Sym_p V \to W$ is linear) as follows:

* If $p = 0$, $m() = Q(0)$;
* If $p = 1$, $m(v_1) = Q(v_1)$;
* If $p = 2$, $m(v_1, v_2) = Q(v_1 + v_2) - Q(v_1) - Q(v_2)$;
* If $p = 3$, $m(v_1, v_2, v_3) = Q(v_1 + v_2 + v_3) - Q(v_1 + v_2) - Q(v_1 + v_3) - Q(v_2 + v_3) + Q(v_1) + Q(v_2) + Q(v_3)$;
* If $p = 4$, $m(v_1, v_2, v_3, v_4) = Q(v_1 + v_2 + v_3 + v_4) - Q(v_1 + v_2 + v_3) - Q(v_1 + v_2 + v_4) - Q(v_1 + v_3 + v_4) - Q(v_2 + v_3 + v_4) + Q(v_1 + v_2) + Q(v_1 + v_3) + Q(v_1 + v_4) + Q(v_2 + v_3) + Q(v_2 + v_4) + Q(v_3 + v_4) - Q(v_1) - Q(v_2) - Q(v_3) - Q(v_4)$;
* etc.

(Morally, the expressions on the right-hand side of each item above should end with $\pm Q(0)$, but $Q(0) = 0$ for any homogeneous map $Q$ of positive degree (since $Q(0) = Q(0 v) = 0^p Q(v) = 0 Q(v) = 0$ when $p \gt 0$), so it is convenient to leave off this term except for $p = 0$.  The $p = 0$ case is instead $Q(0) = Q(0 v) = 0^p Q(v) = 1 Q(v) = Q(v)$, so a homogeneous map of degree $0$ is simply a constant map, and we are defining $m$ to be this constant.)

So defined, $m$ is manifestly symmetric, but it might *not* be multilinear just because $Q$ is homogeneous (for $p \gt 0$); instead, we *define* a __homogeneous polynomial__ of degree $p$ from $V$ to $W$ be such a homogeneous map $Q$ such that $m$ *is* multilinear.  Then a __polynomial__ from $V$ to $W$ is a sum of homogeneous polynomials of various degrees.  Note that if $V$ is the [[free module]] $R^n$ and $W$ is $R$, then this is the usual notion of a polynomial function on $n$ variables over $R$.  (But different [[polynomials]] can give rise to the same polynomial function; see there for examples.)

To get the same $m$ as in earlier sections of this text, the expressions here must be divided by the [[factorial]] $p!$.  Of course, this only works if $p!$ is invertible in $R$; even if $R$ is a [[field]], we need its [[characteristic]] to be $0$ (or at least greater than $p$ if we are only interested in certain values of $p$).  The expressions above work regardless of this to define what a homogeneous polynomial is.  However, if you wish to recover $Q$ from $m$, then you do need to divide by the factorial; otherwise, the only rule that holds in general is that
$$ m(v,\ldots,v) = p!\, Q(v) .$$


## Related concepts

* [[cubical structure on a line bundle]]


[[!redirects polarization identity]]
[[!redirects polarization identities]]
[[!redirects polarisation identity]]
[[!redirects polarisation identities]]
