
# The polarization identity
* table of content
{: toc}

## Idea

Any [[symmetric bilinear form]] $(-) \cdot (-)$ defines a [[quadratic form]] $(-)^2$.  The polarization identity reconstructs the bilinear form from the quadratic form.  More generally, starting from any [[bilinear form]], the polarization identity reconstructs its symmetrization.  A slight variation applies this also to [[sesquilinear form]]s.  The whole business actually applies to [[bilinear operator]]s, not just forms (that is, taking arbitrary values, not just values in the [[base field]] or some other [[line]]).  The linearity is crucial: polarization doesn\'t work without addition (and subtraction); we must also be able to divide by $2$.


## Statement

Let $R$ be a [[commutative ring]].  Let $V$ and $W$ be $R$-[[modules]], and let $m\colon V \times V \to X$ be a [[bilinear operator]]; that is, we have an $R$-module [[homomorphism]] $V \otimes V \to W$.  Let $Q\colon V \to W$ be the [[quadratic operator]] given by $Q(v) = m(v,v)$; this is *not* an $R$-module homomorphism.

Then we have:
* the _[[parallelogram law]]_: $2Q(x) + 2Q(y) = Q(x+y) + Q(x-y)$, and
* the __polarization identity__: $m(x,y) + m(y,x) = Q(x+y) - Q(x) - Q(y)$.

Writing $Q(x)$ as $x^2$ and $m(x,y)$ as $x y$, these read:
* $2x^2 + 2y^2 = (x+y)^2 + (x-y)^2$,
* $x y + y x = (x+y)^2 - x^2 - y^2$.

Now suppose that $m$ is [[symmetric bilinear operator|symmetric]] in that
$$ V \otimes V \overset{twist}\to V \otimes V \overset{m}\to W $$
(where $twist$ is the twist map or [[braiding]]) equals $m$; that is, $m(x,y) = m(y,x)$.  And suppose that $2 \coloneqq 1 + 1$ is [[invertible element|invertible]] in $R$.  Then the polarization identity reads:
$$ x y = \frac 1 2 (x+y)^2 - \frac 1 2 x^2 - \frac 1 2 y^2 .$$
That is, we may recover $m$ from $Q$.


[[!redirects polarization identity]]
[[!redirects polarization identities]]
[[!redirects polarisation identity]]
[[!redirects polarisation identities]]
