
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The __Godement product__ of two [[natural transformations]] between appropriate [[functors]] is their [[horizontal composition]] as 2-cells in the [[2-category]] [[Cat]] of [[categories]], functors and natural transformations:

$$
A\mathrlap{\underoverset{\textsize{G_1}}{\textsize{F_1}}{\begin{matrix}\begin{svg}
<svg width="76" height="39" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
 <use xlink:href="#curvearrows3466"/>
</svg>
\end{svg}\includegraphics[width=53]{curvearrows3466}\end{matrix}}}
{\phantom{a}\space{0}{0}{12}\Downarrow\mathrlap{\alpha}\space{0}{0}{12}\phantom{a}} B
\mathrlap{\underoverset{\textsize{G_2}}{\textsize{F_2}}{\begin{matrix}\begin{svg}
<svg width="76" id="curvearrows3466" height="39" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="3466">
 <g>
  <title>Layer 1</title>
  <path marker-end="url(#se_marker_end_svg_3466_2)" id="svg_3466_2" d="m1,16c24,-15 52,-15 72,0" stroke="#000000" fill="none"/>
  <path marker-end="url(#se_marker_end_svg_3466_2)" id="svg_3466_3" d="m1,26c24,15 44,15 72,0" stroke="#000000" fill="none"/>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_3466_2">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40l100,40z" id="svg_3466_1"/>
  </marker>
 </defs>
</svg>
\end{svg}\includegraphics[width=53]{curvearrows3466}\end{matrix}}}
{\phantom{a}\space{0}{0}{12}\Downarrow\mathrlap{\beta}\space{0}{0}{12}\phantom{a}} C
\mapsto 
A
\mathrlap{\underoverset{\textsize{G_2\circ G_1}}{\textsize{F_2\circ F_1}}{\begin{matrix}\begin{svg}
<svg width="86" height="39" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="3467">
 <g>
  <title>Layer 1</title>
  <path fill="none" stroke="#000000" d="m1,16c27,-15 59,-15 82,0" id="svg_3467_2" marker-end="url(#se_marker_end_svg_3467_2)"/>
  <path fill="none" stroke="#000000" d="m1,26c27,15 50,15 82,1" id="svg_3467_3" marker-end="url(#se_marker_end_svg_3467_2)"/>
 </g>
 <defs>
  <marker id="se_marker_end_svg_3467_2" markerUnits="strokeWidth" orient="auto" viewBox="0 0 100 100" markerWidth="5" markerHeight="5" refX="50" refY="50">
   <path id="svg_3467_1" d="m100,50l-100,40l30,-40l-30,-40l100,40z" fill="#000000" stroke="#000000" stroke-width="10"/>
  </marker>
 </defs>
</svg>
\end{svg}\includegraphics[width=65]{curvearrows3467}\end{matrix}}}
{\phantom{a}\quad\Downarrow\mathrlap{\beta\circ\alpha}\space{0}{0}{20}\phantom{a}} C
$$

## Definition

For [[categories]] $A,B,C$, if $\alpha\colon F_1\to G_1\colon A\to B$ and $\beta\colon F_2\to G_2\colon B\to C$ are [[natural transformation]]s of [[functor]]s, the components $(\beta \circ \alpha)_M$ of the Godement product $\beta \circ \alpha\colon F_2\circ F_1\to G_2\circ G_1\colon A\to C$ (or $\alpha \ast \beta\colon F_1 ; F_2 \to G_1 ; G_2\colon A\to C$) are defined by any of the two equivalent formulas:
$$
(\beta\circ\alpha)_M = \beta_{G_1(M)}\circ F_2(\alpha_M)
$$
$$
(\beta\circ\alpha)_M = G_2(\alpha_M)\circ \beta_{F_1(M)}
$$
that is:
$$
  \array{
    F_2(F_1(M))
    &
    \stackrel{F_2(\alpha_M)}{\to}
    &
    F_2(G_1(M))
    \\
    \beta_{F_1(M)}\downarrow
    &
    \searrow^{(\beta\circ\alpha)_M}
    &
    \downarrow \beta_{G_1(M)}
    \\ G_2(F_1(M))
    &
    \stackrel{G_2(\alpha_M)}{\to} & G_2(G_1(M))
  }
  \,.
$$

The [[interchange law]] in (general) $2$-categories (which in the case of $Cat$ boils down to assertion that the two formulas above are equivalent) is also sometimes called _Godement interchange law_.

The definition above is for the Godement product of $2$ natural transformations, but we can generalise from $2$ to any [[natural number]].  The Godement product of $0$ natural transformations is the __[[identity natural transformation]] on an [[identity functor]]__.


## Properties

The Godement product is strictly associative (so that [[Cat]] is a [[strict 2-category]]).

## References

Name after [[Roger Godement]].

[[!redirects Godement product]]
[[!redirects Godement products]]

[[!redirects horizontal composite of natural transformations]]
[[!redirects horizontal composites of natural transformations]]
[[!redirects horizontal composition of natural transformations]]
[[!redirects horizontal compositions of natural transformations]]
