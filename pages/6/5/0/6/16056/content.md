
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

* table of contents
{:toc}

Overconvergent derived loop spaces are analogs of [[derived loop spaces]] adapted to the setting of [[overconvergent global analytic geometry]]. Their aim is to give a take at overconvergent analogs of $\mathcal{D}$-modules.

## Overconvergent de Rham space

Let $X$ be a global analytic space over a Banach ring $R$. The [[de Rham space]] $X_{dR}$ is usually defined as the quotient of $X$ by the formal groupoid obtained by formal completion of the groupoid of pairs $X\times X$ acting on $X$ along its unit section (given by the diagonal map). If $X$ is separated, then this diagonal map is closed, and we may (in the affine case), see this formal completion as the spectrum of the projective limit of the quotients $\mathcal{O}_{X\times X}/\mathcal{I}_{\Delta}^n$.
To get an overconvergent version of this formal neighborhood of the diagonal in $X\times X$, we may simply take the ind-Ring of germs of functions on $X\times X$ around the diagonal. It may be an interesting question to try to relate sheaves on the corresponding quotient $X^\dagger_{dR}$ of $X$ by the corresponding groupoid to modules over the ring $\mathcal{D}^\infty$ of differential operators of infinite order.

## Overconvergent derived loop spaces

The basic idea of overconvergent derived loop spaces is to give a loop space version of the above construction of $X^\dagger_{dR}$. Recall that if $X$ is an analytic Artin derived stack, we may define the associated formal loop space as the formal completion $\hat{L} X$ of the loop space groupoid $LX=Hom_{dSt}(S^1,X)$ along the constant loop unit section $c:X\to LX,\;x\mapsto c_x$.

Recall that more concretely, one will have $LX\cong X\times^h_{X\times X} X$. In some sense, this construction corresponds to the intuitive idea of using a kind of (derived) tubular neighborhood of the diagonal to make its auto-intersection interesting (of course, the classical auto-intersection is equal to itself).
One may be tempted to replace both $X$'s that appear in the above formula by
the corresponding germs neighborhood of the diagonal $X$ inside $X\times X$, denoted $X^dagger_{X\times X}$, and computing the associated homotopical fiber product
$$
L^\dagger X=X^\dagger_{X\times X}\times^h_{X\times X} X^\dagger_{X\times X}.
$$
To get a sensible dagger generalization of the formal completion of $L^dagger X$ along the constant loop unit section $c:X\to LX$, we will (be careful, It is not so clear that such a construction will fulfill smooth descent, so that we may need to restrict to usual analytic spaces to get a sensible result) take the analytic germs completion $\hat{L}^\dagger X$ of $L^\dagger X$ along $c:X\to LX$. This means that we consider the filtered colimit (aka intersection) of all _Berkovich_ open subspaces of $L^\dagger X$ that contain $c(X)$. Trying to work everywhere with convergent power series seems like a very natural thing to do if we are doing analytic geometry.