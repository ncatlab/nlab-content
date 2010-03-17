### Introduction ###

The [[path groupoid]] is a groupoid internal to some category of [[generalized smooth spaces]].  Its space of morphisms is defined by taking a quotient of a variant of a [[path space]] by the notion of [[thin homotopy]].  The path space is, generally, the same in all proposed categories of [[generalized smooth space]] but as the path groupoid is formed by taking a quotient, its structure will vary depending on the choice.

This page was started in response to a question on MathOverflow by Theo Johnson-Freyd.  The question was "[What is the infinite dimensional manifold structure on the space of smooth paths  mod thin homotopy?](http://mathoverflow.net/questions/17803/what-is-the-infinite-dimensional-manifold-structure-on-the-space-of-smooth-paths)".

### Linear Structure ###

To find a linear structure, we consider the path groupoid in a vector space, specifically $\mathbb{R}^n$.  Thus we consider the space of all smooth paths in $\mathbb{R}^n$ and quotient by the equivalence relation of thin homotopy.

The most important point to realise about the linear structure on this quotient is that it doesn't exist.

The quotient is not by cosets of a subspace and so the linear structure on $P\mathbb{R}^n$ does not descend to $P^1\mathbb{R}^n$.  For it to descend we would need to know that the sum of two paths which are both thin homotopic to the zero path is again thin homotopic to the zero path.  Here's an example where that fails:

$$
\begin{aligned}
\alpha(t) &= (\cos(2\pi t), 0) \\
H_\alpha(s,t) &= (s\cos(2\pi t),0) \\
\beta(t) &= (0,\sin(2\pi t)) \\
H_\beta(s,t) &= (0,s\sin(2\pi t)) \\
(\alpha + \beta)(t) &= (\cos(2\pi t), \sin(2\pi t))
\end{aligned}
$$

Note that, for simplicity, we are defining the path groupoid as the quotient of **all** smooth paths by the corresponding thin homotopical relation.  The resulting space is the same as that formed by taking paths with sitting instants, or paths which are flat at the end-points.

The reason for this failure is seen when we examine how the sum of two paths is formed.  The sum of two arbitrary paths $\alpha$ and $\beta$ is defined as the composition

$$
I \to I \times I \to \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}^n.
$$

Here, and hereafter, $I = [0,1]$.

If $\alpha$ and $\beta$ are thinly homotopic to the zero path, then the obvious way to construct a thin homotopy from the sum to the zero path is to take the sum of the thin homotopies.

$$
I^2 \to I^2 \times I^2 \to \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}^n.
$$

One cannot compute the exact rank of this without knowing the maps involved, but one can get bounds.  In particular, the upper bound on the rank is the minimum of the upper bounds of each piece.  The crucial point here is that (unless $n = 1$), the map with the lowest rank is the map $I^2 \times I^2 \to \mathbb{R}^n \times \mathbb{R}^n$.  This is constructed from two thin homotopies, and so has maximum rank $2$!

Of course, this does not **prove** that it does not always work (the counterexample given above does that) since it might be the case that the maps are always such that this upper bound is not achieved.  What this does is explain why the existence of the counterexample is not surprising: it would take a considerable number of coincidences for no counterexample to exist.

Extending this further, we observe that the process of taking the path groupoid is not a product-preserving functor.  This is obvious from considering the case of $\mathbb{R}^2$: in $\mathbb{R}$, every path is thinly homotopic to every other (with the same end-points) and so $P^1\mathbb{R}$ simply has objects $\mathbb{R}$ with a single morphism between each two objects.  However, $\mathbb{R}^2$ is much, much larger than the corresponding product as it has plenty of paths not thinly homotopic to each other (even with the same end-points).

Finally, the lack of a linear structure on $P^1 \mathbb{R}^n$ rules out any interesting manifold structure on $P^1 M$.

### Diffeological Structure ###

The diffeological structure is simple to explain.  A map $\phi \colon U \to P^1M$ is a plot if and only if it locally lifts to $P M$.  That is, if there is a cover $\mathcal{V}$ of $U$ and for each $V \in \mathcal{V}$ a lift of $\phi|_V \colon V \to P^1 M$ to a smooth map $V \to P M$.

The fact that plots have to lift locally does mean that it is not always possible to patch together smooth curves, even with suitable reparametrisation.  That is, if two smooth curves $\alpha, \beta \colon I \to P^1 M$ are such that $\alpha(1) = \beta(0)$ and each is flat at that point, then it may not be possible to concatenate them to a smooth path $\alpha # \beta$.  Here is an example.  Note that a smooth path in $P^1 M$ locally lifts to a smooth path in $P M$, which adjoints to a smooth surface in $M$.  So we define $\alpha$ and $\beta$ as maps $I^2 \to M$ with the first parameter being the parameter along the path in $P^1 M$.

$$
\begin{aligned}
\alpha(s,t) &= \big((1 - s) \sin(2 \pi t),1 - \cos(2 \pi t)\big) \\
\beta(s,t) &= \big(s \sin(2 \pi t), -1 + \cos(2 \pi t)\big)
\end{aligned}
$$

<svg width="501" height="300" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_fw" viewBox="0 0 10 10">
   <path fill="#000000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <line fill="none" stroke-width="2" stroke="#000000" id="svg_32298_1" y2="148" x2="451" y1="148" x1="51"/>
  <circle stroke-width="2" stroke="#0000ff" fill="none" id="svg_32298_2" r="50" cy="98" cx="51"/>
  <ellipse ry="50" rx="25" stroke-width="2" stroke="#0000ff" fill="none" id="svg_32298_3" cy="98" cx="140"/>
  <ellipse ry="50" rx="9" stroke-width="2" stroke="#0000ff" fill="none" id="svg_32298_4" cy="98" cx="204"/>
  <line fill="none" stroke-width="2" stroke="#0000ff" id="svg_32298_5" y2="48" x2="251" y1="148" x1="251"/>
  <g transform="rotate(180, 395, 198)" id="svg_32298_10">
   <circle id="svg_32298_6" stroke-width="2" stroke="#7f007f" fill="none" r="50" cy="198" cx="339"/>
   <ellipse id="svg_32298_7" ry="50" rx="25" stroke-width="2" stroke="#7f007f" fill="none" cy="198" cx="428"/>
   <ellipse id="svg_32298_8" ry="50" rx="9" stroke-width="2" stroke="#7f007f" fill="none" cy="198" cx="492"/>
   <line id="svg_32298_9" fill="none" stroke-width="2" stroke="#7f007f" y2="148" x2="539" y1="248" x1="539"/>
  </g>
  <line marker-end="url(#se_arrow_fw)" fill="none" stroke-width="2" stroke="#000000" id="svg_32298_11" y2="22" x2="206" y1="22" x1="40"/>
  <line id="svg_32298_12" marker-end="url(#se_arrow_fw)" fill="none" stroke-width="2" stroke="#000000" y2="274" x2="444" y1="274" x1="278"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_32298_13" y="0" x="93">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#945;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\alpha</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_32298_14" y="280" x="335">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#946;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\beta</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>
We then reparametrise these in $s$ so that $\alpha$ and $\beta$ are flat (but without sitting instants) at the appropriate end-points ($s = 1$ for $\alpha$, $s = 0$ for $\beta$).  At the end-points, we have $\alpha(1,t) = (0,\sin(2 \pi t))$ which is thinly homotopic to the zero map. Similarly, $\beta(0,t) = (0,-\sin(2\pi t))$ which is, again, thinly homotopic to the zero map.  So $\alpha(1,t) = \beta(0,t)$ but even with the reparametrisation, there is no way to lift the concatenation, $\alpha # \beta$, to $P^1 M$.

If we include a sitting instant at the concatentation point then it is possible to concatentate these paths.  This is because the quotient sets are themselves path-connected, so there is a smooth path between $\alpha(1,t)$ and $\beta(0,t)$ which lies wholly within the space of paths thinly homotopic to the zero map.  While we "sit" at the concatenation point in $P^1 M$, the lifted map is frantically dashing from $\alpha(1,t)$ to $\beta(0,t)$.

### Fr&#246;licher Structure ###

The Fr&#246;licher structure on $P^1 M$ is determined by the fact that smooth functions $P^1 M \to \mathbb{R}$ are those functions that compose to smooth functions $P M \to \mathbb{R}$.  Then the smooth curves are those that compose to smooth curves under all smooth functions.  This means that concatenations such as the one above are allowed.

