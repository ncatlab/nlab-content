
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The **join** $S \star T$ of two [[simplicial set]]s $S$ and $T$ is a new simplicial set that may geometrically be thought of as a [[cone]] over $T$ with tip of shape $S$. Topologically, it can also be thought of as the union of line segments connecting $S$ to $T$ if both are placed in general position. 

If the simplicial sets in question are [[quasi-categories]] the notion of join on them produces the notion of [[join of quasi-categories]] that underlies many constructions in [[higher category theory]] such as the definition of [[limit in a quasi-category]].

The join of [[simplicial set]]s extends that historically given for [[simplicial complex|simplicial complexes]], cf. for instance the description and discussion in [[Spanier|Spanier's classical text]] (page 109 and then pages 114 -116). 

The adaptation of this to simplicial sets reveals a neat link with some categorical structure in the category, $\Delta_a$, of finite ordinals (including the empty one).  


## Motivating examples

When $S = \Delta^0$ is the [[point]], then the join $S \star T$ is a genuine [[cone]] over $T$. Or if $S = 2$ is the discrete two-point space, the join is the [[suspension]] of $T$.

For example, consider the two cones over $[2]$, the standard 2-simplex.  The first picture represents $[0]\star [2]$, while the second represents $[2]\star [0]$.  

$$
\begin{matrix}
\begin{svg}
<svg width="205" height="183" xmlns="http://www.w3.org/2000/svg" se:nonce="92019" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_92019_fw" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000000"/>
  </marker>
  <linearGradient id="svg_92019_7" x1="0" y1="0" x2="1" y2="1">
   <stop offset="0" stop-color="#000000" stop-opacity="0"/>
   <stop offset="1" stop-color="#000000" stop-opacity="0.25"/>
  </linearGradient>
 </defs>
 <g>
  <title>Layer 1</title>
  <path fill="url(#svg_92019_7)" stroke-width="2" d="m106.666656,19.33334l4.708,116.302189l80.708687,36.197815l-85.416687,-152.500004z" id="svg_92019_6"/>
  <path d="m106.375,20l-92,151l178,1l-86,-152z" id="svg_92019_1" fill="#000000" stroke-width="2" fill-opacity="0.25"/>
  <path d="m14.125,170.75l97.734283,-36.5l80.515717,37.75" id="svg_92019_2" fill="#000000" fill-opacity="0.25" stroke-width="2"/>
  <foreignObject x="96" y="0" id="svg_92019_3" font-size="16" width="20" height="20">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mo stretchy="false">[</mo>
      <mn>0</mn>
      <mo stretchy="false">]</mo>
     </mrow>
     <annotation encoding="application/x-tex">[0]</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="0" y="163.125" id="svg_92019_4" font-size="16" width="16" height="20">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
     </mrow>
     <annotation encoding="application/x-tex">0</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="104" y="136" font-size="16" width="16" height="20" id="svg_92019_5">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
     </mrow>
     <annotation encoding="application/x-tex">1</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="188.875" y="162.875" font-size="16" width="16" height="20" id="svg_92019_12">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>2</mn>
     </mrow>
     <annotation encoding="application/x-tex">2</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line x1="14.875" y1="170.5" x2="109.125" y2="135.375" id="svg_92019_26" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_92019_fw)"/>
  <line x1="14.625" y1="171" x2="181.25001" y2="172.125" id="svg_92019_27" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_92019_fw)"/>
  <line x1="112.125" y1="134.625" x2="183.875" y2="168" id="svg_92019_28" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_92019_fw)"/>
  <line x1="106.37498" y1="19.87501" x2="16.874986" y2="166.999999" id="svg_92019_29" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_92019_fw)"/>
  <line x1="109.072297" y1="20.497995" x2="108.197297" y2="132.619014" id="svg_92019_30" stroke="#000000" stroke-width="2" fill="none" transform="rotate(-3.16201, 108.635, 76.5585)" marker-end="url(#se_arrow_92019_fw)"/>
  <line x1="106.375" y1="19" x2="187.875" y2="164.99999" id="svg_92019_31" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_92019_fw)"/>
 </g>
</svg>
\end{svg}
&
\begin{svg}
<svg width="205" height="183" xmlns="http://www.w3.org/2000/svg" se:nonce="82471" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_82471_fw" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000000"/>
  </marker>
  <linearGradient y2="1" x2="1" y1="0" x1="0" id="svg_82471_16">
   <stop stop-opacity="0" stop-color="#000000" offset="0"/>
   <stop stop-opacity="1" stop-color="#000000" offset="1"/>
  </linearGradient>
 </defs>
 <g>
  <title>Layer 1</title>
  <path fill="#000000" stroke-width="2" d="m14,8l87,156.25l87,-156.25l-174,0z" id="svg_82471_1" fill-opacity="0.25"/>
  <line fill="none" stroke="#000000" stroke-width="2" fill-opacity="0.25" x1="14.75" y1="9" x2="96.75" y2="157.125006" id="svg_82471_3" marker-end="url(#se_arrow_82471_fw)"/>
  <line fill="none" stroke="#000000" stroke-width="2" fill-opacity="0.25" x1="186.500007" y1="10.562499" x2="105.062506" y2="157.062488" id="svg_82471_4" marker-end="url(#se_arrow_82471_fw)"/>
  <line fill="none" stroke="#000000" stroke-width="2" fill-opacity="0.25" x1="14.375" y1="7.875" x2="88.875006" y2="47.125002" id="svg_82471_5" marker-end="url(#se_arrow_82471_fw)"/>
  <line fill="none" stroke="#000000" stroke-width="2" fill-opacity="0.25" x1="91.124998" y1="47.25" x2="178.437491" y2="11.937498" id="svg_82471_6" marker-end="url(#se_arrow_82471_fw)"/>
  <line fill="none" stroke="#000000" stroke-width="2" fill-opacity="0.25" x1="16.375007" y1="7.625" x2="176.312498" y2="7.9375" id="svg_82471_7" marker-end="url(#se_arrow_82471_fw)"/>
  <line fill="none" stroke="#000000" stroke-width="2" fill-opacity="0.25" x1="90.500001" y1="50" x2="101.062501" y2="155.625003" id="svg_82471_8" marker-end="url(#se_arrow_82471_fw)"/>
  <foreignObject x="91.25" y="163.25" id="svg_82471_9" font-size="16" width="20" height="20">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mo stretchy="false">[</mo>
      <mn>0</mn>
      <mo stretchy="false">]</mo>
     </mrow>
     <annotation encoding="application/x-tex">[0]</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="0" y="0" id="svg_82471_10" font-size="16" width="16" height="20">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
     </mrow>
     <annotation encoding="application/x-tex">0</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="189" y="0.1875" id="svg_82471_11" font-size="16" width="16" height="20">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>2</mn>
     </mrow>
     <annotation encoding="application/x-tex">2</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="83.75" y="27.25" id="svg_82471_12" font-size="16" width="14" height="20">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
     </mrow>
     <annotation encoding="application/x-tex">1</annotation>
    </semantics>
   </math>
  </foreignObject>
  <path id="svg_82471_2" d="m188,7.916668l-97.666649,40.355015l10.610336,115.978271" fill-opacity="0.25" stroke-width="2" fill="#000000"/>
  <path id="svg_82471_13" d="m14.999999,8.666668l85.666665,155.000004l-9.666664,-114.666672" fill-opacity="0.25" stroke-width="2" fill="url(#svg_82471_16)"/>
 </g>
</svg>
\end{svg} \\
[0]\star [2] & [2]\star [0]
\end{matrix}
$$

If you take two non-coplanar line segments in $\mathbb{R}^3$ (such as $A B$ and $C D$ in the picture below), then join every point in one to every point in the other, you get a 3-simplex (the tetrahedron in the picture). You can think of this as being the union of all the cones on the first segment, with cone points on the second one. We have that the join $\Delta[1]\star \Delta[1]$ is $\Delta[3]$.

$$
\begin{gathered}
\begin{matrix}
0\overset{f}{\longrightarrow}1\\
\\
0'\underset{g}{\longrightarrow}1'
\end{matrix}
\overset{\quad f\star g\quad}{\longrightarrow}
\array{\arrayopts{\rowalign{center}} 
\begin{svg}
<svg width="96" height="116" xmlns="http://www.w3.org/2000/svg" se:nonce="91144" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_fw1" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000"/>
  </marker>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_91144_fw" viewBox="0 0 10 10">
   <path fill="#000000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g display="inline">
  <title>Layer 1</title>
  <rect fill-opacity="0.25" stroke-width="2" fill="#000000" id="svg_91144_6" height="80.249997" width="80.75" y="19.875" x="6.375"/>
  <path stroke-width="2" fill-opacity="0.15" fill="#000000" id="svg_91144_7" d="m6.625,20.25l80.25,80.027077l-80.25,0.222923"/>
  <ellipse fill-opacity="0.5" ry="7.625" rx="7.375" stroke-width="2" fill="#ffffff" id="svg_91144_12" cy="99.874999" cx="87.125"/>
  <ellipse fill-opacity="0.5" id="svg_91144_11" ry="8.374999" rx="8.3125" stroke-width="2" fill="#ffffff" cy="99.625" cx="9.3125"/>
  <ellipse fill-opacity="0.5" id="svg_91144_10" ry="6.875" rx="6.4375" stroke-width="2" fill="#ffffff" cy="21.75" cx="86.187501"/>
  <ellipse fill-opacity="0.5" ry="6.75" rx="5.5625" stroke-width="2" fill="#ffffff" id="svg_91144_1" cy="21.75" cx="7.0625"/>
  <polyline se:connector="svg_97259_9 svg_97259_2" marker-end="url(#se_arrow_91144_fw)" stroke-dasharray="2,2" fill="none" stroke-width="2" stroke="#000000" points="79.2069,28 47.9784,60.0575 16.75,92.115" id="svg_91144_2"/>
  <polyline se:connector="svg_97259_1 svg_97259_9" id="svg_97259_23" points="12.375,19.75 45.125,19.75 77.875,19.75" stroke="#000" stroke-width="2" fill="none" marker-end="url(#se_arrow_fw1)"/>
  <line marker-end="url(#se_arrow_91144_fw)" fill="none" stroke-width="2" stroke="#000000" id="svg_91144_4" y2="90" x2="6.375" y1="28.25" x1="6.375"/>
  <line id="svg_91144_5" marker-end="url(#se_arrow_91144_fw)" fill="none" stroke-width="2" stroke="#000000" y2="90" x2="86.875" y1="28.25" x1="86.875"/>
  <line marker-end="url(#se_arrow_91144_fw)" fill="none" stroke-width="2" stroke="#000000" id="svg_91144_8" y2="93.999999" x2="80.250002" y1="25.25" x1="11.375"/>
  <foreignObject height="20" width="16" font-size="16" id="svg_91144_13" y="96.25" x="35">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>g</mi>
     </mrow>
     <annotation encoding="application/x-tex">g</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line x1="17.374999" y1="100" x2="78" y2="100" id="svg_91144_14" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_91144_fw)"/>
 </g>
 <g>
  <title>Layer 2</title>
  <foreignObject x="1.875" y="91.75" font-size="16" width="14" height="16" id="svg_97259_2">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">0'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="81.875" y="91.75" font-size="16" width="14" height="16" id="svg_97259_16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">1'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="78" y="12" font-size="16" width="18" height="16" id="svg_97259_9">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
     </mrow>
     <annotation encoding="application/x-tex">1</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="0" y="12" id="svg_97259_1" font-size="16" width="12" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
     </mrow>
     <annotation encoding="application/x-tex">0</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="16" font-size="16" id="svg_91144_9" y="0" x="35">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>f</mi>
     </mrow>
     <annotation encoding="application/x-tex">f</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>
\end{svg}
}
\cong
\array{\arrayopts{\rowalign{center}} 
\begin{svg}
<svg width="108" height="110" xmlns="http://www.w3.org/2000/svg" se:nonce="22396" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_fw" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000000"/>
  </marker>
  <marker viewBox="0 0 10 10" id="se_arrow_22396_fw" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000000"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <path d="m3.8125,49.25l33.375,53.125l63.125,-41.625l-62.75,-52.875l-33.75,41.375z" id="svg_4422_11" fill="#000000" stroke-width="2" stroke-dasharray="2,2" fill-opacity="0.25"/>
  <ellipse fill-opacity="0.5" cx="98" cy="63.375001" id="svg_22396_4" fill="#ffffff" stroke-width="2" rx="5.25" ry="11.125"/>
  <path d="m3.875,49.0625l35.25,55.75l0.25,-97.25" id="svg_4422_12" fill="#000000" fill-opacity="0.15" stroke-width="2" stroke-dasharray="2,2"/>
  <ellipse fill-opacity="0.5" cx="38.90625" cy="102.125" id="svg_22396_3" fill="#ffffff" stroke-width="2" rx="10.90625" ry="7.75"/>
  <ellipse fill-opacity="0.5" cx="5.25" cy="51" id="svg_22396_2" fill="#ffffff" stroke-width="2" rx="4.5" ry="7"/>
  <ellipse fill-opacity="0.5" cx="37.250001" cy="9.25" id="svg_22396_1" fill="#ffffff" stroke-width="2" rx="9.749999" ry="8.25"/>
  <line x1="8.375" y1="56.750001" x2="32.062498" y2="93.875" id="svg_22396_6" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="92.75" y1="65.875" x2="48.062501" y2="95.250001" id="svg_22396_8" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="10.000001" y1="51.5" x2="91" y2="61" id="svg_22396_9" stroke="#000000" stroke-width="2" stroke-dasharray="2,2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="39.5" y1="17.625" x2="39.375" y2="92.375" id="svg_22396_5" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="31.5" y1="16.25" x2="8.249999" y2="43.249999" id="svg_22396_10" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="45" y1="14" x2="92.999999" y2="53.999999" id="svg_22396_11" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
 </g>
 <g>
  <title>Layer 2</title>
  <foreignObject y="0" x="30.75" id="svg_4422_1" font-size="16" width="14" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
     </mrow>
     <annotation encoding="application/x-tex">0</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="92.375" y="52" id="svg_4422_4" font-size="16" width="16" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">1'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="33.25" y="94.375" id="svg_4422_2" font-size="16" width="16" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">0'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="0" y="41.25" id="svg_4422_3" font-size="16" width="8" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
     </mrow>
     <annotation encoding="application/x-tex">1</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>
\end{svg}
}\\
f\cong g \cong [1] \Rightarrow f\star g \cong \Delta[3]
\end{gathered}
$$

## Definition

We first define the **join of simplicial sets** as the restriction to simplicial sets of the extension of the [[ordinal sum]] operation on the augmented [[simplex category]] $\Delta_a$ to augmented simplicial sets.

Then we give the more explicit definition in terms of concrete formulas. We first refer to the description of [[ordinal sum]], and then how it induces structure on the category of augmented simplicial sets.


### By Day convolution {#DayConvolution}

Via the general process of [[Day convolution]], the [[ordinal sum]] [[monoidal structure]] on $\Delta_a$ is lifted to a [[monoidal structure]] on [[presheaf|presheaves]] on $\Delta_a$, i.e. to the the category [[asSet]] or $sSet_+$ of [[augmented simplicial set]]s. This is given by a [[end|coend]] formula:

+-- {: .un_prop}
###### Definition/Proposition

The join of simplicial set is equivalently expressed as

$$
  \star : sSet_+ \times sSet_+ \to sSet_+
$$
$$
  (S \star S')(-)
  :=
  \int^{[i],[j] \in \Delta_a}
    (S_i \times S'_j) \times Hom_{\Delta_a}(-,[i] \boxplus [j])
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

This is an abuse of notation because $Hom_{\Delta_a}(-,[i] \boxplus [j])$ is a functor, while $(S_i \times S'_j)$ is a set.  To be precise, the second $\times$ should be replaced with $\cdot$, which denotes the [[copower|indexed copower]].

=--

Note that the join of simplicial sets $S \star T$ is [[cocontinuous functor|cocontinuous]] in each of its separate arguments $S$, $T$ (this is true generally of Day convolution products). 

+-- {: .un_prop}
###### Proposition

This join tensor product forms part of a [[closed monoidal category|closed monoidal structure]] on the category of
augmented simplicial sets, [[asSet]] $ := Sets^{\Delta_a^{op}}$. The [[internal hom]] is given by
$$[X, Y ]_n =asS(X; Dec^{n+1}Y )\,,$$
where $Dec$ is the [[total décalage]] functor (see also at _[[décalage]]_).

=--

+-- {: .un_defn}
###### Definition

For $S$ a simplicial set, let $\hat S$ denote the augmented simplicial set which equals $S$ in all degrees except in degree -1, where it is the point, $({\hat S})_{-1} = pt$. This is the **trivial augmentation** of $S$.

=--

+-- {: .un_defn}
###### Definition

The **join** of two ordinary [[simplicial set]]s $S_1$ and $S_2$ is the join of their _trivial augmentation_ :

$$
  S_1 \star S_2 := {\hat S_1} \star {\hat S_2}
  \,.
$$

=--

+-- {: .un_remark}
###### Remark
Note that the join operation is not commutative.  This comes from the fact that the [[monoidal structure]] given by [[ordinal sum]] on the [[augmented simplex category]] is not [[symmetric monoidal category|symmetric monoidal]].  See the discussion at [[augmented simplex category]] for more details.

=--

### Concrete formulas

The join of two non-augmented simplicial sets is given by the formula

$$
  (S \star S')_n := S_n \cup S'_n \cup 
   (\cup_{i+j = n-1} S_i \times S'_j)
  \,.
$$

The $i$-th boundary map 

$$
  d_i : (S \star T)_n \to (S \star T)_{n-1}
$$ 

is defined on $S_n$ and $T_n$ using the $i$th boundary map on $S$ and $T$. 

Given $\sigma \in S_j$ and $\tau \in T_k$ , we have:

$$
  d_i (\sigma, \tau) = 
  \left\{
    \array{
      (d_i \sigma, \tau) & if\; i \leq j , j \neq 0
      \\
      (\sigma, d_{i-j-1}) & if\; i \gt j, k \neq 0
    }
  \right.
$$

If $j = 0$ then 

$$
  d_0(\sigma, \tau) = \tau \in T_{n-1} \subset (S \star T)_{n-1}
  \,.
$$

If $k = 0$ then

$$
  d_n(\sigma, \tau) = \sigma \in S_{n-1} \subset (S \star T)_{n-1} 
  \,.
$$


### Join of quasi-categories

If the simplicial sets in question are [[quasi-categories]], their join computes the corresponding [[join of quasi-categories]], effectively an [[over quasi-category]] construction.

In this sense the join can then also be computed -- up to equivalence of quasi-categories -- as the [[homotopy colimit|homotopy pushout]] of the two projections out of $S \times S'$.

In this form, the join is used
in [definition 1.2.8.1, p. 42](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=42) of [[Higher Topos Theory|HTT]]



## Examples {#Examples}

Recall that the join of augmented simplicial sets $S \star T$ is a [[cocontinuous functor]] in each of its separate arguments $S$, $T$ (this is true generally of [[Day convolution]] products).

This observation can help simplify calculations. For example, simplicial joins preserve unions in the first argument $S$, and inasmuch as [[horn]]s are unions of face simplices, this allows one to compute joins of horns with simplices.

As an operation on simplicial sets, $S \star T$ merely commutes with connected colimits (since these preserve the property of having trivial augmentation). However, for each $S$, the natural inclusion $S \cong S \star \varnothing \to S \star T$ induces a functor $S \star (-) : sSet \to S/sSet$ that does preserve colimits. Similarly, $(-) \star T : sSet \to T/sSet$ preserves colimits.

### Joins with the point: cones

For $\{v\} = \Delta[0]$ the [[point]], a join with the point is called a **cone** with cone vertex $v$: for $S \in sSet$ we say

* $S^\triangleleft := \{v\} \star S$ is the **cone** over $S$;  

* $S^\triangleright :=  S \star \{v\}$ is the **co-cone** under $S$;  

Universal images of cones and cocones over a fixed base $S$ in a [[quasi-category]] $C$ are [[limit in a quasi-category|limits and colimits in that quasi-category]].


For instance the cone over the interval $\Delta[1]$ is the 2-simplex

$$
  \{v\} \star \Delta[1]
  =
  \left(
    \array{
      && v
      \\
      & \swarrow &\swArrow& \searrow
      \\
      0 &&\to&& 1
    }
  \right)
  \simeq
  \Delta[2]
  \,.
$$

More generally, the cone over the $n$-[[simplex]] is the $(n+1)$-simplex

$$
  \Delta[n]^{\triangleleft} \simeq \Delta[n+1]
  \,.
$$

Cones of 2-[[horn]]s are simplicial 2-squares $\simeq \Delta[1] \times \Delta[1]$:

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \{v\} \star \Lambda_2[2]
  = 
  \left(
  \array{
    v &\to& 1
    \\
    \downarrow &{}_{\swArrow}\searrow^{\swArrow}& \downarrow
    \\
    0 &\to& 2
  }
  \right)
$$

and

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \Lambda_0[2] \star \{v\}
  = 
  \left(
  \array{
    0&\to& 1
    \\
    \downarrow &{}_{\swArrow}\searrow^{\swArrow}& \downarrow
    \\
    2 &\to& v
  }
  \right)
  \,.
$$




### Joins of simplices

Effectively by the definition from ordinal sum, we have that the join of two [[simplex|simplices]] is another simplex:

$$
  \Delta[k] \star \Delta[l] = \Delta[k + l + 1]
  \,.
$$

In particular the cone over the $n$-simplex is the $(n+1)$-simplex

$$
  \Delta[0] \star \Delta[n] = \Delta[n+1]
$$

and hence

$$
  \Delta[n] = \Delta[0] \star \cdots \star \Delta[0]
  \,.
$$

Notice that while thus $\Delta[n+1] \simeq  \Delta[0]\star\Delta[n] \simeq \Delta[n] \star \Delta[0]$ the identifications of the cone point of course differ in both cases. The asymmetry is seen for instance by restricting attention to the cone over the boundary of the $n$-simplex, where we have

$$
  \partial \Delta[n] \star \Delta[0] = \Lambda_{n+1}[n+1]
$$

and

$$
  \Delta[0] \star \partial \Delta[n] = \Lambda_0[n+1]
  \,.
$$

### Simplicial $n$-sphere

Let $\partial \Delta[1] = \Delta[0] \sqcup \Delta[0]$ the **simplicial 0-sphere**: just the disjoint union of the point. Then the $n$-fold join of $\partial \Delta[1]$ with itself is a simplicial model for the $n$-sphere
$$\mathbf{S}^0 := \partial \Delta[1]$$
$$\mathbf{S}^n := \mathbf{S}^0 \star \mathbf{S}^{n-1}$$
for $n \in \mathbb{N}$, $n \gt 0$. The [[geometric realization]] of $\mathbf{S}^n$ is equivalent to the topological $n$-sphere.

See [Ehlers/Porter p. 8](http://arxiv.org/PS_cache/math/pdf/9904/9904039v1.pdf#page=8).

## Properties

### Compatibility with quasi-categories

+-- {: .un_prop}
###### Proposition

If $S, S' \in $ [[sSet]] are both [[quasi-categories]], then so is their join $S \star S'$.

=--

This is due to [[Andre Joyal]]. A proof appears as [[Higher Topos Theory|HTT, prop. 1.2.8.3]].


### Compatibility with homotopy coherent nerve

There is also a join operations on [[categories]] and [[sSet-categories]]:


+-- {: .un_def}
###### Definition

Let $C,D \in sSet Cat$. Then define $C \star D$ to be the $sSet$-category given by

$$
  Obj(C \star D) = Obj(C) \coprod Obj(D)
$$

$$
  C \star D(x,y) = 
  \left\{
    \array{
       C(x,y) & for\; x,y \in C
       \\
       D(x,y) & for\; x,y \in D
       \\
       \emptyset & for \;x \in D, y \in C
       \\
       * & for\; x \in C , y \in D
   }
  \right.
$$

with the obvious composition operations.

=--

Write

$$
  \tau_{hc} : sSet \to sSet Cat
$$

for the [[left adjoint]] of the [[homotopy coherent nerve]] functor (denoted $\mathfrak{C}$ in [[Higher Topos Theory|HTT]]. ) 

+-- {: .un_prop}
###### Proposition

For $S, S'$ two [[simplicial set]]s we have that 

* the two inclusions $\tau_{hc}(S), \tau_{hc}(S') \to \tau_{hc}(S\star S')$ are [[full and faithful functor|full and faithful]].

* $\tau_{hc}(S \star S')$ is in general not [[isomorphic]] to $\tau_{hc}(S) \star \tau_{hc}(S')$;

* the canonical morphism

  $$
    \tau_{hc}(S \star S') \to \tau_{hc}(S) \star \tau_{hc}(S')
  $$

  is an equivalence in the [[model structure on sSet-categories]].

=--

This is [[Higher Topos Theory|HTT, corollary 4.2.1.4]].

## Related concepts

* [[join of topological spaces]]

* [[join of categories]], [[join of quasi-categories]]

* [[join of maps]]


## References

The join operation was studied by P. J. Ehlers, in his thesis

* _Algebraic Homotopy in Simplicially Enriched Groupoids_, 1993, 
University of Wales Bangor, available [[Ehlers-thesis.pdf|here:file]], (see also the reference below and the Menagerie notes available from [[Tim Porter]]'s homepage.),

but was there ascribed to [[Jack Duskin]] and [[Don van Osdol]] in some unpublished notes.  The main ideas were derived there from earlier work of [[Bill Lawvere]].

A useful published reference is

* [[Phil Ehlers|P. J. Ehlers]] and [[Tim Porter]], _Joins for (Augmented) Simplicial Sets_,  Jour. Pure Applied Algebra, 145 (2000) 37-44, ([arXiv](http://arxiv.org/abs/math.CT/9904039)) .

A useful discussion emphasizing the Day convolution operation is also in section 3.1 of

* [[Dominic Verity]], _Weak complicial sets I_ ([arXiv](http://arxiv.org/abs/math/0604414))

Discussion in [[homotopy type theory]] (with application to [[n-image]] factorization) is in


* {#Rijke17} [[Egbert Rijke]], _The join construction_ ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))

