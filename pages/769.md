The **comma object** of two morphisms $f:A\to C$ and $g:B\to C$ in a [[2-category]] is an object $(f/g)$ equipped with projections $p:(f/g)\to A$ and $q:(f/g)\to B$ and a 2-cell

+--{: style="text-align:center"}
<svg xmlns="http://www.w3.org/2000/svg" width="10em" height="10em" viewBox="-30 -10 160 150">
 <desc>Comma Square</desc>
 <defs>
  <marker id="svg295arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
 </defs>
 <g font-size="16" markdown="1">
  <foreignObject x="-10"  y="0" width="45" height="25">$(f/g)$</foreignObject>
  <foreignObject x="100"  y="0" width="20" height="20">$A$</foreignObject>
  <foreignObject x="0"  y="100" width="20" height="20">$B$</foreignObject>
  <foreignObject x="100"  y="100" width="20" height="20">$C$</foreignObject>
  <foreignObject x="110"  y="50" width="20" height="20">$f$</foreignObject>
  <foreignObject x="50"  y="110" width="20" height="25">$g$</foreignObject>
  <foreignObject x="-10"  y="50" width="20" height="20">$q$</foreignObject>
  <foreignObject x="50"  y="-10" width="20" height="25">$p$</foreignObject>
  <foreignObject x="60"  y="60" width="20" height="25">$\alpha$</foreignObject>
 </g>
 <g fill="none" stroke="#000" stroke-width="1.5" marker-end="url(#svg295arrowhead)">
   <line x1="40" y1="10" x2="90" y2="10"/>
   <line x1="30" y1="110" x2="90" y2="110"/>
   <line y1="30" x1="10" y2="90" x2="10"/>
   <line y1="30" x1="110" y2="90" x2="110"/>
   <line x1="65" y1="55" x2="55" y2="65"/>
 </g>
</svg>
=--

which is universal in the sense of a [[2-limit]].  Part of this is the statement that for any object $D$, 1-morphisms $p':D\to A$, $q':D\to B$ and 2-cell $\sigma:f p'\Rightarrow g q'$ there is a 1-morphism $u:D\to(f/g)$ and isomorphisms $p u\cong p'$, $q u\cong q'$ such that modulo these isomorphisms, we have $\sigma u=\alpha$.  There is also an additional "2-dimensional universality" saying that given $u:D\to (f/g)$ and $v:D\to (f/g)$ and 2-cells $\mu:p u \to p v$ and $\nu:q u \to q v$ such that $\alpha v. f \mu = g\nu . \alpha u$, there exists a unique 2-cell $\beta:u\to v$ such that $p\beta = \mu$ and $q \beta = \nu$.  Note that the 2-dimensional property implies that in the 1-dimensional property, the 1-morphism $u$ is unique up to unique isomorphism.  A square containing a 2-cell with this property is sometimes called a **comma square**.

A **strict comma object** is analogous but has the universal property of a [[strict 2-limit]].  This means that given $p'$, $q'$, and $\sigma$ as above, there exists a _unique_ $u:D\to (f/g)$ such that $p u = p'$, $q u = q'$, and $\sigma u = \alpha$.  Note that any strict comma object is a comma object, but the converse is not in general true.

In [[Cat]], (strict) comma objects are [[comma category|comma categories]], and give their name to the general notion.
