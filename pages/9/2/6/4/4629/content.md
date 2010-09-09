
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Definition

In a [[2-category]], the composition of [[2-morphism]]s along [[object]]s is called _horizontal composition_ .

+-- {: style="text-align:center"}
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

This is in contrast to the [[vertical composition]] of 2-morphisms, which is their composition along 1-[[morphism]]s. 

## Properties

Horizontal and vertical composition are subject to the compatibility condition called the [[interchange law]].

## Examples

* In [[Cat]], horizontal composition is the [[Godement product]] of [[natural transformation]]s.

