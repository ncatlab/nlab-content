

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

****

## Idea

The *Bochner linearization theorem* &lbrack;[Bochner 1945](#Bochner1945)&rbrack; states that for a [[differentiable map|differentiable]] [[group action]] of a [[compact Lie group]] on a [[differentiable manifold]] there exists around each [[fixed point]] a (similarly differentiable) local  [[coordinate chart]] on which the action is [[linear representation|linear]].

(The analogous statement for [[analytic manifolds]] and [[analytic function|analytic]] [[group actions]] is attributed by [Bochner 1945](#Bochner1945) to [[Henri Cartan]], referencing [Martin 1944](#Martin44).)

This linearization theorem is the special case (for [[fixed loci]] of [[dimension of a manifold|dimension]]$=0$) of the existence of *[[equivariant tubular neighbourhoods]]*, see there for more.

## Related concepts

* [[transformation group]]

* [[orbifold]]

## References

The original article:

* {#Bochner1945} [[Salomon Bochner]]: *Compact Groups of Differentiable Transformation*, Annals of Mathematics **46** 3 (1945) 372-381 &lbrack;[doi:10.2307/1969157](https://doi.org/10.2307/1969157), [jstor:1969157](https://www.jstor.org/stable/1969157)&rbrack;

following

* {#Martin44} W. T. Martin: *Mappings by means of systems of analytic functions of several complex variables*,  Bulletin of the American Math. Society **50** 1 (1944) 5-19.

See also:

* [[Nicolas Bourbaki]]: Prop. 5 §9.3 Chapter IX, of: *Lie Groups and Algebras*, Masson (1982), Springer (2007) &lbrack;[scan](/nlab/files/Bourbaki-BochnerLinearization.png)&rbrack;


\linebreak


\begin{tikzcd}
  S^2
  \ar[
    rr,
    "{ F }"
  ]
  \ar[
    d,
    "{
     \widehat{R}
    }"
  ]
  &&
  \mathrm{Fred}(\mathcal{H})
  \ar[
    d,
    "{ U(\widehat{R}) }"
  ]
  \\
  S^2
  \ar[
    rr,
    "{ F }"
  ]
  &&
  \mathrm{Fred}(\mathcal{H})
\end{tikzcd}





****


