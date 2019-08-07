
> This entry is about the notion in [[linear algebra]] relating bilinear and quadratic forms. For the notion in [[symplectic geometry]] see at _[[polarization]]_. For polarization of light, see _[[wave polarization]]_ (if we ever write it).

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

Any [[symmetric bilinear form]] $(-) \cdot (-)$ defines a [[quadratic form]] $(-)^2$.  The _polarization identity_ reconstructs the bilinear form from the quadratic form.  More generally, starting from any [[bilinear form]], the polarization identity reconstructs its symmetrization.  A slight variation applies this also to [[sesquilinear form]]s.  The whole business actually applies to [[bilinear maps]], not just forms (that is, taking arbitrary values, not just values in the [[base field]] or some other [[line]]).  The linearity is crucial: polarization doesn\'t work without addition (and subtraction); we must also be able to divide by $2$.  It is also possible to generalize from quadratic forms to higher-order [[homogenous form]]s.


## Statement

Let $R$ be a [[commutative ring]].  Let $V$ and $W$ be $R$-[[modules]], and let $m\colon V \times V \to W$ be a [[bilinear map]]; that is, we have an $R$-module [[homomorphism]] $V \otimes V \to W$.  Let $Q\colon V \to W$ be the [[quadratic map]] given by $Q(v) = m(v,v)$; this is *not* an $R$-module homomorphism.

Then we have:

* the _[[parallelogram law]]_: $2 Q(x) + 2 Q(y) = Q(x + y) + Q(x - y)$, and
* the __polarization identity__: $2 m(x,y) + 2 m(y,x) = Q(x + y) - Q(x - y)$.

Writing $Q(x)$ as $x^2$ and $m(x,y)$ as $x y$, these read:

* $2 x^2 + 2 y^2 = (x +y )^2 + (x - y)^2$,
* $2 x y + 2 y x = (x + y)^2 - (x - y)^2$.

The polarization identity also has these alternative forms:

* $x y + y x = (x + y)^2 - x^2 - y^2$,
* $x y + y x = x^2 + y^2 - (x - y)^2$;

these may derived by adding or subtracting the parallelogram law and the first polarization identity; although the derivation requires cancelling $2$, the alternative polarization identities remain valid regardless of whether $2$ is cancellable in $W$.

Now suppose that $m$ is [[symmetric bilinear map|symmetric]], so that $x y = y x$.  And suppose that $2 \coloneqq 1 + 1$ is (not merely cancellable but also) invertible in $W$.  Then the polarization identities read:

* $x y = \frac{1}{4} (x + y)^2 - \frac{1}{4} (x - y)^2$,
* $x y = \frac{1}{2} (x + y)^2 - \frac{1}{2} x^2 - \frac{1}{2} y^2$,
* $x y = \frac{1}{2} x^2 + \frac{1}{2} y^2 - \frac{1}{2} (x - y)^2$;

That is, we may recover $m$ from $Q$ (in any of these ways).  Regardless of the original symmetry of $m$, we may recover its symmetrization $x \circ y = (x y + y x)/2$.

We can go the other direction: given a quadratic map $Q$, if $2$ is invertible, then any polarization identity defines a symmetric bilinear map $m$; these all agree if $Q$ obeys the parallelogram law, and then $Q$ may be recovered from this $m$ once more.

If $R$ is a $*$-[[star-ring|ring]], then $m$ could be conjugate-symmetric ([[Hermitian map|Hermitian]]).  Then $Q$ would satisfy $Q(t x) = t^* t Q(x)$ instead of $Q(t x) = t^2 Q(x)$ as for a quadratic map.  Since everything is still bilinear or quadratic over the [[integers]], the parallelogram identity still follows, as does the polarization identity in its general forms (before assuming that $m$ is symmetric).  We can still recover $m$ from $Q$ if $R$ has an [[imaginary unit]]: an element $i$ such that $i + i^* = 0$ and $i i^* = 1$; we do this as follows:
$$ x y = \frac{1}{4} Q(x + y) - \frac{1}{4} Q(x - y) + \frac{1}{4} i Q(x + i y) - \frac{1}{4} i Q(x - i y) .$$


## Examples

This is best known in the case of bilinear and quadratic *forms*, where $W$ is the [[ground ring]] $R$.  Here, $m$ is an [[inner product]], making $V$ into an [[inner product space]], and $Q$ is (the square of) the norm, making $V$ into a [[normed space]].

This also applies to [[commutative algebras]], where $W$ is $V$.  Actually, there is no need for $m$ to be associative; although one rarely studies commutative but [[non-associative algebras]], we have an exception with [[Jordan algebras]].  Although the Jordan identity is simpler to express in terms of the multiplication operation (as usual), the application to [[quantum mechanics]] may be more easily motivated through the squaring operation (since the square of an [[observable]] has a more obvious meaning than the Jordan product of two observables), and the polarization identities allow us to recover multiplication from squaring (and subtraction).


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

So defined, $m$ is manifestly symmetric, but it might *not* be multilinear just because $Q$ is homogeneous (except for $p = 1$); instead, we *define* a __homogeneous polynomial__ of degree $p$ from $V$ to $W$ be such a homogeneous $Q$ such that $m$ *is* multilinear.  (Then a __[[polynomial]]__ from $V$ to $W$ is a sum of homogeneous polynomials of various degrees.)  Note that if $V$ is the [[free module]] $R^n$, then this is the usual notion of a polynomial with $n$ variables.

Morally, the expressions on the right-hand side of each item above should end with $\pm Q(0)$, but this ends up not mattering for the definition of a homogeneous polynomial (except when $p = 0$), in which case $Q(0) = 0$ (including when $p = 0$).  If one were ever to consider the polarization of a non-polynomial homogeneous map, however, then presumably this term would need to be restored.

To get the same $m$ as in earlier sections of this text, the expressions here must be divided by the [[factorial]] $p!$.  Of course, this only works if $p!$ is invertible in $R$; even if $R$ is a [[field]], we need its [[characteristic]] to be greater than $p$ (or $0$).  The expressions above work regardless of this to define what a homogeneous polynomial is.  However, if you wish to recover $Q$ from $m$, then you do need to divide by the polynomial; otherwise, the only rule that holds in general is that
$$ m(v,\ldots,v) = p! Q(v) .$$


## Related concepts

* [[cubical structure on a line bundle]]


[[!redirects polarization identity]]
[[!redirects polarization identities]]
[[!redirects polarisation identity]]
[[!redirects polarisation identities]]
