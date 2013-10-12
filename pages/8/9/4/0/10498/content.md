
# The polarization identity
* table of content
{: toc}

## Idea

Any [[symmetric bilinear form]] $(-) \cdot (-)$ defines a [[quadratic form]] $(-)^2$.  The polarization identity reconstructs the bilinear form from the quadratic form.  More generally, starting from any [[bilinear form]], the polarization identity reconstructs its symmetrization.  A slight variation applies this also to [[sesquilinear form]]s.  The whole business actually applies to [[bilinear operator]]s, not just forms (that is, taking arbitrary values, not just values in the [[base field]] or some other [[line]]).  The linearity is crucial: polarization doesn\'t work without addition (and subtraction); we must also be able to divide by $2$.


## Statement

Let $R$ be a [[commutative ring]].  Let $V$ and $W$ be $R$-[[modules]], and let $m\colon V \times V \to X$ be a [[bilinear operator]]; that is, we have an $R$-module [[homomorphism]] $V \otimes V \to W$.  Let $Q\colon V \to W$ be the [[quadratic operator]] given by $Q(v) = m(v,v)$; this is *not* an $R$-module homomorphism.

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

Now suppose that $m$ is [[symmetric bilinear operator|symmetric]], so that $x y = y x$.  And suppose that $2 \coloneqq 1 + 1$ is (not merely cancellable but also) invertible in $W$.  Then the polarization identities read:

* $x y = \frac{1}{4} (x + y)^2 - \frac{1}{4} (x - y)^2$,
* $x y = \frac{1}{2} (x + y)^2 - \frac{1}{2} x^2 - \frac{1}{2} y^2$,
* $x y = \frac{1}{2} x^2 + \frac{1}{2} y^2 - \frac{1}{2} (x - y)^2$;

That is, we may recover $m$ from $Q$ (in any of these ways).  Regardless of the original symmetry of $m$, we may recover its symmetrization $x \circ y = (x y + y x)/2$.

We can go the other direction: given a quadratic operator $Q$, if $2$ is invertible, then any polarization identity defines a symmetric bilinear operator $m$; these all agree if $Q$ obeys the parallelogram law, and then $Q$ may be recovered from this $m$ once more.


[[!redirects polarization identity]]
[[!redirects polarization identities]]
[[!redirects polarisation identity]]
[[!redirects polarisation identities]]
