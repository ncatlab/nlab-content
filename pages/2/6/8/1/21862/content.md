
\tableofcontents

## Definition

The [[category]] of __orthogonal spaces__ is the category
of [[topological functors]] between [[topological categories]]
of finite-dimensional real inner product spaces (with linear isometric
embeddings) and topological spaces (with continuous maps).

Here a __topological space__, or simply a __space__,
refers to an object in a [[convenient category of spaces]],
namely, [[compactly generated weakly Hausdorff space]].

Orthogonal spaces are turned into a [[relative category]]
using the notion of a __global equivalence__,
which are introduced via an equivariant version of the [[Whitehead theorem]].
A morphism $f\colon X\to Y$ is a __global equivalence__
if for any [[compact Lie group]] $G$,
any continuous orthogonal representation $V$ of $G$
on a finite-dimensional real inner product space,
any $k\ge0$,
and any continuous maps $\alpha\colon\partial D^k\to X(V)^G$
and $\beta\colon D^k\to Y(V)^G$ such that $\beta|_{\partial D^k}=f(V)^G\circ\alpha$,
we can find a continuous orthogonal representation $W$ of $G$,
a $G$-equivariant linear isometric embedding $\phi\colon V\to W$
and a continuous map $\lambda\colon D^k\to X(W)^G$
such that $\lambda|_{\partial D^k}=X(\phi)^G\circ\alpha$
and $f(W)^G\circ\lambda$ is homotopic to $Y(\phi)^G\circ\beta$ relative $\partial D^k$.

In particular, if $X$ and $Y$ are [[constant functors]],
then $f\colon X\to Y$ is a global equivalence
if and only if $f(0)\colon X(0)\to Y(0)$ is a [[weak homotopy equivalence]]
of topological spaces.

Global equivalences can also be characterized as morphisms $f\colon X\to Y$
such that for any [[compact Lie group]] $G$
and for some (hence any) complete $G$-[[universe]] $U$,
the canonical map of __underlying $G$-spaces__
$$hocolim_V f(V)\colon hocolim_V X(V)\to hocolim_V Y(V)$$
is a $G$-[[equivariant weak equivalence]] (i.e., a [[weak homotopy equivalence]]
on $H$-fixed points for any closed subgroup $H$ of $G$),
where $V$ runs over all finite-dimensional subrepresentations of $U$.

## References

* [[Stefan Schwede]], _Global homotopy theory_.
