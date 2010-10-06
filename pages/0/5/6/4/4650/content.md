A [[fork]]

$$
A\xrightarrow[\quad e \quad]{}B\underoverset{\quad g \quad}{f}{\rightrightarrows}C
$$
is **split** if it can be embedded into a diagram

$$
\begin{svg}
<svg width="112" height="61" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="48015">
 <g>
  <title>Layer 1</title>
  <foreignObject height="42" width="112" font-size="16" id="svg_48015_1" y="19.491677" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mpadded lspace="-50%width" width="0">
       <mrow>
        <mi>A</mi>
        <munder>
         <mo>&#8594;</mo>
         <mrow>
          <mspace width="1em"/>
          <mi>e</mi>
          <mspace width="1em"/>
         </mrow>
        </munder>
        <mi>B</mi>
        <munderover>
         <mo stretchy="true">&#8649;</mo>
         <mrow>
          <mspace width="1em"/>
          <mi>g</mi>
          <mspace width="1em"/>
         </mrow>
         <mi>f</mi>
        </munderover>
        <mi>C</mi>
       </mrow>
      </mpadded>
     </mrow>
     <annotation encoding="application/x-tex">\mathclap{A\xrightarrow[\quad e \quad]{}B\underoverset{\quad g \quad}{f}{\rightrightarrows}C}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <path fill="none" stroke="#000000" d="m63.583351,32.549999c13.519966,-19.398649 19.108238,-19.52702 30.125008,0.027042" id="svg_48015_2" marker-start="url(#se_marker_start_svg_48015_2)"/>
  <path fill="none" stroke="#000000" d="m16.17498,33.94997c9.440479,-9.454929 17.148819,-9.609211 27.625038,0.192581" marker-start="url(#se_marker_start_svg_48015_3)" id="svg_48015_3"/>
  <foreignObject x="76.075001" y="0" id="svg_48015_4" font-size="14" width="12" height="18">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>t</mi>
     </mrow>
     <annotation encoding="application/x-tex">t</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="23.991668" y="8.500001" font-size="14" width="12" height="18" id="svg_48015_5">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>s</mi>
     </mrow>
     <annotation encoding="application/x-tex">s</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
 <defs>
  <marker id="se_marker_start_svg_48015_2" markerUnits="strokeWidth" orient="auto" viewBox="0 0 100 100" markerWidth="5" markerHeight="5" refX="50" refY="50">
   <path id="svg_48015_6" d="m0,50l100,40l-30,-40l30,-40l-100,40z" fill="#000000" stroke="#000000" stroke-width="10"/>
  </marker>
  <marker id="se_marker_start_svg_48015_3" markerUnits="strokeWidth" orient="auto" viewBox="0 0 100 100" markerWidth="5" markerHeight="5" refX="50" refY="50">
   <path id="svg_48015_7" d="m0,50l100,40l-30,-40l30,-40l-100,40z" fill="#000000" stroke="#000000" stroke-width="10"/>
  </marker>
 </defs>
</svg>
\end{svg}\includegraphics[width=86]{SplitFork}
$$
in which $s e = id_A$, $t g = id_B$ and $t f = e s$ (we used here Leibniz order for [[composition]] of morphisms). 

Surely, $f$ and $g$ can be interchanged in the definition (a matter of unimportant convention). 

Every split fork is an [[absolute limit|absolute]] [[equalizer]], but not conversely.  See also [[split coequalizer]].


[[!redirects split equalizer]]
[[!redirects split equalizers]]
[[!redirects split equaliser]]
[[!redirects split equalisers]]
[[!redirects split fork]]
[[!redirects split forks]]
