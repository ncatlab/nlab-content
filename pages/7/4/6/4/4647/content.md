Given a pair $L\dashv R$ of [[adjoint functors]], $L:A\to B:R$, with counit $\epsilon$ and unit $\eta$, one forms a [[comonad]] $\mathbf{\Omega} = (\Omega, \delta,\epsilon)$ by $\Omega := LR$, $\delta := L\eta R$. $\mathbf{\Omega}$ comodules form a category $B_{\mathbf{\Omega}}$ and there is a natural comparison functor $K = K_{\mathbf{\Omega}} : A\to B_{\mathbf{\Omega}}$ given by $A\mapsto (LA,LA\stackrel{L(\eta_A)}\to LRLA)$. 

A functor $L:A\to B$ is __comonadic__ if it has a right adjoint $R$ and the corresponding comparison functor $K$ is an [[equivalence of categories]].  The adjunction $L\dashv R$ is said to be a **comonadic adjunction**.

Beck's [[monadicity theorem]] has its dual, comonadic analogue. To discuss it, observe that for every $\Omega$-comodule $(N,\rho)$, 

+--{: style="text-align:center"}
<svg width="284" height="85" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="37863">
 <g>
  <title>Layer 1</title>
  <foreignObject height="54" width="284" font-size="16" id="svg_37863_1" y="31.00003" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>N</mi>
      <munderover>
       <mo>&#8594;</mo>
       <mi>&#961;</mi>
       <mspace width="2em"/>
      </munderover>
      <msup>
       <mi>Q</mi>
       <mo>*</mo>
      </msup>
      <msub>
       <mi>Q</mi>
       <mo>*</mo>
      </msub>
      <mi>N</mi>
      <munderover>
       <mo>&#8649;</mo>
       <mrow>
        <mspace width="thickmathspace"/>
        <msup>
         <mi>Q</mi>
         <mo>*</mo>
        </msup>
        <msub>
         <mi>&#951;</mi>
         <mrow>
          <msub>
           <mi>Q</mi>
           <mo>*</mo>
          </msub>
          <mi>N</mi>
         </mrow>
        </msub>
        <mspace width="1em"/>
       </mrow>
       <mrow>
        <mspace width="thickmathspace"/>
        <msup>
         <mi>Q</mi>
         <mo>*</mo>
        </msup>
        <msub>
         <mi>Q</mi>
         <mo>*</mo>
        </msub>
        <mi>&#961;</mi>
        <mspace width="1em"/>
       </mrow>
      </munderover>
      <msup>
       <mi>Q</mi>
       <mo>*</mo>
      </msup>
      <msub>
       <mi>Q</mi>
       <mo>*</mo>
      </msub>
      <msup>
       <mi>Q</mi>
       <mo>*</mo>
      </msup>
      <msub>
       <mi>Q</mi>
       <mo>*</mo>
      </msub>
      <mi>N</mi>
     </mrow>
     <annotation encoding="application/x-tex">N\xrightarrow[\rho]{\qquad}Q^*Q_* N\underoverset{\; Q^* \eta_{Q_*N}\quad}{\;Q^* Q_* \rho\quad}{\rightrightarrows}Q^* Q_*Q^* Q_* N</annotation>
    </semantics>
   </math>
  </foreignObject>
  <path marker-end="url(#se_marker_end_svg_37863_3)" id="svg_37863_3" d="m215,43.144531c-41,-26.024994 -82.000031,-25.020004 -123,0" stroke="#000000" fill="none"/>
  <path id="svg_37863_4" marker-end="url(#se_marker_end_svg_37863_4)" d="m65.5,42.644531c-16,-12.43103 -32,-11.950989 -48,0" stroke="#000000" fill="none"/>
  <foreignObject height="22" width="60" font-size="16" id="svg_37863_5" y="0" x="122.5">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>&#1013;</mi>
       <mrow>
        <msup>
         <mi>Q</mi>
         <mo>*</mo>
        </msup>
        <msub>
         <mi>Q</mi>
         <mo>*</mo>
        </msub>
        <mi>N</mi>
       </mrow>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">\epsilon_{Q^* Q_* N}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_37863_6" height="22" width="20" font-size="16" y="10" x="32">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>&#1013;</mi>
       <mi>N</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">\epsilon_{N}</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37863_3">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40l100,40z" id="svg_37863_21"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37863_4">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40l100,40z" id="svg_37863_22"/>
  </marker>
 </defs>
</svg>
=--

manifestly exhibits a [[split equalizer]] sequence.

...

[[!redirects comonadic functor]]
[[!redirects comonadic functors]]
[[!redirects comonadicity theorem]]
[[!redirects comonadic adjunction]]
[[!redirects comonadic adjunctions]]
