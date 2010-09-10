
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

+--{: style="text-align:center"}
<svg width="340" height="84" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="57183">
 <g>
  <title>Layer 1</title>
  <foreignObject height="22" width="340" font-size="16" id="svg_57183_1" y="29" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>A</mi>
      <mspace width="2em"/>
      <mo>&#8659;</mo>
      <mpadded width="0">
       <mi>&#945;</mi>
      </mpadded>
      <mspace width="2em"/>
      <mi>B</mi>
      <mspace width="2em"/>
      <mo>&#8659;</mo>
      <mpadded width="0">
       <mi>&#946;</mi>
      </mpadded>
      <mspace width="2em"/>
      <mi>C</mi>
      <mspace width="thickmathspace"/>
      <mo>&#8614;</mo>
      <mspace width="thickmathspace"/>
      <mi>A</mi>
      <mspace width="2em"/>
      <mspace width="thickmathspace"/>
      <mo>&#8659;</mo>
      <mpadded width="0">
       <mrow>
        <mi>&#945;</mi>
        <mo>*</mo>
        <mi>&#946;</mi>
       </mrow>
      </mpadded>
      <mspace width="2em"/>
      <mspace width="thickmathspace"/>
      <mi>C</mi>
     </mrow>
     <annotation encoding="application/x-tex">A\qquad\Downarrow\mathrlap{\alpha}\qquad B\qquad\Downarrow\mathrlap{\beta}\qquad C\;\mapsto\; A\qquad\; \Downarrow\mathrlap{\alpha\ast\beta}\qquad\; C</annotation>
    </semantics>
   </math>
  </foreignObject>
  <path marker-end="url(#se_marker_end_svg_57183_2)" id="svg_57183_2" d="m19.5,33.75c22.666656,-15 49.069595,-15 68,0" stroke="#000000" fill="none"/>
  <path marker-end="url(#se_marker_end_svg_57183_3)" id="svg_57183_3" d="m19.5,52.5c22.666656,14.333344 42.133331,15.666656 68,1" stroke="#000000" fill="none"/>
  <path id="svg_57183_4" marker-end="url(#se_marker_end_svg_57183_4)" d="m102.5,33.75c24.666656,-15 53.399261,-15 74,0" stroke="#000000" fill="none"/>
  <path id="svg_57183_5" marker-end="url(#se_marker_end_svg_57183_5)" d="m239.5,33.75c27.999969,-15 60.615387,-15 84,0" stroke="#000000" fill="none"/>
  <path id="svg_57183_6" marker-end="url(#se_marker_end_svg_57183_6)" d="m103.5,52.5c24.333313,14.333344 45.231354,15.666656 73,1" stroke="#000000" fill="none"/>
  <path id="svg_57183_7" marker-end="url(#se_marker_end_svg_57183_7)" d="m239.5,52.5c27.666687,14.333344 51.42746,15.666656 83,1" stroke="#000000" fill="none"/>
  <foreignObject height="20" width="20" font-size="16" id="svg_57183_8" y="0" x="45">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>F</mi>
       <mn>1</mn>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">F_1</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_57183_9" height="20" width="20" font-size="16" y="0" x="132">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>F</mi>
       <mn>2</mn>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">F_2</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_57183_17" height="20" width="20" font-size="16" y="64" x="45">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>G</mi>
       <mn>1</mn>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">G_1</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_57183_25" height="20" width="20" font-size="16" y="64" x="133">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>G</mi>
       <mn>2</mn>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">G_2</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_57183_33" y="0" x="258">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>F</mi>
       <mn>1</mn>
      </msub>
      <mo lspace="verythinmathspace">:</mo>
      <msub>
       <mi>F</mi>
       <mn>2</mn>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">F_1\colon F_2</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_57183_34" height="20" width="48" font-size="16" y="63" x="258">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>G</mi>
       <mn>1</mn>
      </msub>
      <mo lspace="verythinmathspace">:</mo>
      <msub>
       <mi>G</mi>
       <mn>2</mn>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">G_1\colon G_2</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_57183_2">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_57183_3">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_57183_4">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_57183_5">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_57183_6">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_57183_7">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
 </defs>
</svg>
=--

## Definition

For [[categories]] $A,B,C$, if $\alpha\colon F_1\to G_1\colon A\to B$ and $\beta\colon F_2\to G_2\colon B\to C$ are [[natural transformation]]s of [[functor]]s, the components $(\alpha * \beta)_M$ of the Godement product $\alpha * \beta\colon F_1 ; F_2 \to G_1 ; G_2$ (or $\beta \circ \alpha\colon F_2\circ F_1\to G_2\circ G_1$) are defined by any of the two equivalent formulas:
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


[[!redirects Godement product]]
[[!redirects Godement products]]

[[!redirects horizontal composite of natural transformations]]
[[!redirects horizontal composites of natural transformations]]
[[!redirects horizontal composition of natural transformations]]
[[!redirects horizontal compositions of natural transformations]]
