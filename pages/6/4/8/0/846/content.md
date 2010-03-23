#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The **join** $S \star T$ of two [[simplicial set]]s $S$ and $T$ is a new simplicial set that may geometrically be thought of as a [[cone]] over $T$ with tip of shape $S$. Topologically, it can also be thought of as the union of line segments connecting $S$ to $T$ if both are placed in general position. 

If the simplicial sets in question are [[quasi-categories]] the notion of join on them produces the notion of [[join of quasi-categories]] that underlies many constructions in [[higher category theory]] such as the definition of [[limit in a quasi-category]].

The join of [[simplicial set]]s extends that historically given for [[simplicial complex|simplicial complexes]], cf. for instance the description and discussion in [[Spanier|Spanier's classical text]] (page 109 and then pages 114 -116). 

The adaptation of this to simplicial sets reveals a neat link with some categorical structure in the category, $\Delta_a$, of finite ordinals (including the empty one).  


## Motivating examples

When $S = \Delta^0$ is the [[point]], then the join $S \star T$ is a genuine [[cone]] over $T$. Or if $S = 2$ is the discrete two-point space, the join is the [[suspension]] of $T$.

For example, consider the two cones over $[2]$, the standard 2-simplex.  The first picture represents $[0]\star [2]$, while the second represents $[2]\star [0]$.  

+-- {: style="text-align:center"}
<svg width="470" height="300" xmlns="http://www.w3.org/2000/svg" se:nonce="90800" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_fw1" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000"/>
  </marker>
  <marker viewBox="0 0 10 10" id="se_arrow_bk2" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="2">
   <path d="m10,0l-10,5l10,5l-5,-5l5,-5z" fill="#000"/>
  </marker>
  <marker viewBox="0 0 10 10" id="se_arrow_fw3" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <g id="svg_90800_8">
   <g id="svg_90800_7">
    <path d="m273.899261,50.184601l102.532623,1.93298l68.666626,28.003544l-171.199249,-29.936523z" transform="rotate(171.277, 359.406, 64.2637)" fill="#d3d3d3" stroke="#000" stroke-width="0" stroke-dasharray="null" id="svg_124"/>
    <path d="m286.528839,195.433014l69.399536,28.428802l-47,-167.000027l-22.399536,138.571224z" transform="rotate(171.277, 321.287, 140.334)" fill="#d1cfcf" stroke="#000" stroke-width="0" stroke-dasharray="null" id="svg_125"/>
    <path d="m333.971008,213.648163l121.404419,-140.879189l-22,143.000023l-99.404419,-2.12085z" transform="rotate(171.277, 394.68, 144.234)" fill="#b5b5b5" stroke="#000" stroke-width="0" stroke-dasharray="null" id="svg_126"/>
   </g>
   <g id="svg_90800_6">
    <text x="273.762" y="71.1651" id="svg_86" fill="#000000" stroke="#000000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="24" font-family="serif">0</text>
    <text x="344.746" y="87.3238" id="svg_87" fill="#000000" stroke="#000000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="24" font-family="serif">1</text>
    <text x="444.18" y="75.3433" id="svg_88" fill="#000000" stroke="#000000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="24" font-family="serif">2</text>
    <text x="346.41" y="231.868" id="svg_89" fill="#000000" stroke="#000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="24" font-family="serif">[0]</text>
   </g>
  </g>
  <g id="svg_90800_5">
   <g id="svg_90800_3">
    <path d="m23.90435,209.648621l102.532631,1.932983l68.666641,28.00354l-171.199272,-29.936523z" id="svg_61" fill="#a3a3a3" stroke="#000" stroke-width="0" stroke-dasharray="null" transform="rotate(-8.04566, 109.506, 224.617)"/>
    <path d="m115.353127,206.267456l67.999992,27.000031l-46.999985,-167.000023l-21.000008,139.999992z" id="svg_63" fill="#b7b7b7" stroke="#000" stroke-width="0" stroke-dasharray="null" transform="rotate(-8.04566, 149.352, 149.768)"/>
    <path d="m12.445761,212.673386l123.534037,-138.933708l-21.999985,143.000038l-101.534052,-4.066315z" id="svg_62" fill="#d1d1d1" stroke="#000" stroke-width="0" stroke-dasharray="null" transform="rotate(-8.04566, 74.2129, 145.24)"/>
   </g>
   <g id="svg_90800_4">
    <text x="21.4613" y="229.463" id="svg_71" fill="#000000" stroke="#000000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="24" font-family="serif" transform="rotate(1.91612, 21.4609, 221.463)">0</text>
    <text x="124.847" y="217.771" id="svg_72" fill="#000000" stroke="#000000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="24" font-family="serif" transform="rotate(1.91612, 124.848, 209.771)">1</text>
    <text x="193.993" y="234.297" id="svg_73" fill="#000000" stroke="#000000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="24" font-family="serif" transform="rotate(1.91612, 193.992, 226.299)">2</text>
    <text x="138.883" y="74.7254" id="svg_74" fill="#000000" stroke="#000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="24" font-family="serif" transform="rotate(-8.12388, 125.043, 68.3871) matrix(0.982818, 0.184576, -0.184576, 0.982818, 1.23277, -24.7929)">[0]</text>
   </g>
  </g>
  <polyline stroke-width="2" se:connector="svg_86 svg_88" id="svg_97" points="278.762,63.2867 358.971,65.2539 439.18,67.2211" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_87 svg_88" id="svg_96" points="347.746,78.9628 393.463,73.4545 439.18,67.9462" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_86 svg_87" id="svg_95" points="278.762,64.3024 310.254,71.4718 341.746,78.6412" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_88 svg_89" id="svg_94" points="439.246,75.3438 396.22,145.105 353.194,214.867" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_87 svg_89" id="svg_93" points="344.837,87.3242 345.561,151.096 346.285,214.867" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_86 svg_89" id="svg_92" points="277.334,71.1641 309.416,143.016 341.499,214.867" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_71 svg_73" id="svg_80" points="26.6172,221.634 107.432,223.865 188.246,226.096" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_72 svg_73" id="svg_79" points="127.676,210.442 157.961,217.707 188.246,224.972" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_71 svg_72" id="svg_78" points="26.6172,220.906 74.1465,215.485 121.676,210.065" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_74 svg_73" id="svg_77" points="129.839,79.6758 159.913,148.869 189.988,218.062" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_74 svg_71" id="svg_76" points="117.567,79.6758 72.0921,146.791 26.6172,213.905" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <polyline stroke-width="2" se:connector="svg_74 svg_72" id="svg_75" points="125.014,79.6758 124.855,140.621 124.697,201.566" stroke="#000" fill="none" marker-end="url(#se_arrow_fw3)"/>
  <path d="m-997.370361,873.996216l123,-139.999939l-22,142.999939l-101,-3z" transform="rotate(-180, 2680.15, -6316.13) matrix(0.988881, -0.148709, 0.148709, 0.988881, -20.793, 54.4602)" fill="#bcbcbc" stroke="#000" stroke-width="0" stroke-dasharray="null" id="svg_85"/>
  <path d="m255.030853,69.940491l101.466675,1.933327l66.000061,26.933342l-167.466736,-28.866669z" transform="rotate(-180, -2305.71, 268.625) matrix(0.988881, -0.148709, 0.148709, 0.988881, 3.38641, 45.8432)" fill="#a5a5a5" stroke="#000" stroke-width="0" stroke-dasharray="null" id="svg_83"/>
  <g id="svg_105" transform="rotate(8.6766, 307.787, 139.809) rotate(-8.61437, 307.787, 139.809) rotate(-8.61437, 307.787, 139.809)"/>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="21" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#000000" id="svg_90800_1" y="269.383" x="120">[0] &#9733; [2]</text>
  <text transform="matrix(1, 0, 0, 1, 0, 0)" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="20" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#000000" id="svg_90800_2" y="269" x="345">[2] &#9733; [0]</text>
 </g>
</svg>
=--  

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
f\cong g \cong [1] \Rightarrow f\star g \cong [3]
\end{gathered}
$$

## Definition

We first define the **join of simplicial sets** as the restriction to simplicial sets of the extension of the **ordinal sum** operation on the augmented [[simplex category]] $\Delta_a$ to augmented simplicial sets.

Then we give the more explicit definition in terms of concrete formulas.


### Ordinal sum

The objects of the _augmented_ [[simplex category]] $\Delta_a$ can be identified with the finite [[total order|totally ordered]] [[set]]s, _including_ the [[empty set]], which we write in this context as

$$
  [-1] :=  \emptyset
$$

so that then

$$
  [0] = *
$$

is the singleton set, as usual and

$$
  [1] = \{ 0 \lt 1\}
$$

and so on, so that $[n] = \{ 0 \lt \ldots \lt n\}$

This counting is off by one compared to the [[cardinality]] of these sets. 



The monoidal structure on $\Delta_a$ that we are interested in now is, at the level of the sets, just union, but we have to consider the order on that 'union'. If we have $[n]$ and $[m]$, we form the union of the two sets, where we know the order on two elements we keep it, but it we have two elements one, $i$, say, from the $[n]$ and the other, $j$, from $[m]$ we put $i\lt j$.

As an example, consider $[1] = \{ 0 \lt 1\}$ and $[2] =  \{ \overline{0} \lt \overline{1} \lt \overline{2}\}$, where the overlines are just so that we can keep track of where the different elements come from. We form the union of the two sets and the rule says that anything without an overline is less than anything with one.  This gives a linear order
$$[1]+[2] = \{0 \lt 1\lt \overline{0} \lt \overline{1} \lt \overline{2}\},$$
which is isomorphic as a poset to $[4]$. Similarly $[1]+[1] = [3]$, which helps explain the picture above.

We can thus think of the operation as the **addition of cardinalities**, but must remember that $[n]$ has $n+1$ elements. In terms of the counting 'off-by-one', this reads

$$
  ([n], [m]) \mapsto [n + m + 1]
  \,,
$$

but remember there is also the order to keep track of.

This operation extends to give the **ordinal sum** structure  on $\Delta_a$ (for details see the discussion in the entry [[simplex category]]) making it a [[monoidal category]], whose product operation is

$$
  \boxplus: \Delta_a \times \Delta_a \to \Delta_a
$$
$$
  ([n], [m]) \mapsto [n + m + 1]
  \,.
$$

### Join of simplicial sets via Day convolution

Via the general process of [[Day convolution]], the ordinal sum monoidal structure on $\Delta_a$ is lifted to a monoidal structure on [[presheaf|presheaves]] on $\Delta_a$, i.e. to the the category [[ASSet]] of augmented [[simplicial set]]s. This is given by the [[end|coend]] formula

$$
  \star : ASSet \times ASSet \to ASSet
$$
$$
  (S \star S')(-)
  :=
  \int^{[i],[j] \in \Delta_a}
    (S_i \times S'_j) \times Hom_{\Delta_a}(-,[i] \boxplus [j])
  \,.
$$

**Remark** This is an abuse of notation because $Hom_{\Delta_a}(-,[i] \boxplus [j])$ is a functor, while $(S_i \times S'_j)$ is a set.  To be precise, the second $\times$ should be replaced with $\cdot$, which denotes the [[indexed copower]].

Note that the join of simplicial sets $S \star T$ is [[cocontinuous functor|cocontinuous]] in each of its separate arguments $S$, $T$ (this is true generally of Day convolution products). 

**Proposition**
This join tensor product forms part of a [[closed monoidal category|closed monoidal structure]] on the category of
augmented simplicial sets, [[ASSet]] $ := Sets^{\Delta_a^{op}}$. The [[internal hom]] is given by
$$[X, Y ]_n =asS(X; Dec^{n+1}Y )\,,$$
where $Dec$ is the [[decalage]] functor.

**Definition**
For $S$ a simplicial set, let $\hat S$ denote the augmented simplicial set which equals $S$ in all degrees except in degree -1, where it is the point, $({\hat S})_{-1} = pt$. This is the **tivial augmentation** of $S$.

**Definition**
The **join** of two ordinary [[simplicial set]]s $S_1$ and $S_2$ is the join of their _trivial augmentation_ :

$$
  S_1 \star S_2 := {\hat S_1} \star {\hat S_2}
  \,.
$$



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
      (d_i \sigma, \tau) & if i \leq j , j \neq 0
      \\
      (\sigma, d_{i-j-1}) & if i \gt j, k \neq 0
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
in [definition 1.2.8.1, p. 42](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=42) of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .


## Examples {#Examples}

Recall that the join of simplicial sets $S \star T$ is a [[cocontinuous functor]] in each of its separate arguments $S$, $T$ (this is true generally of [[Day convolution]] products). 

This observation can help simplify calculations. For example, simplicial joins preserve unions in the first argument $S$, and inasmuch as [[horn]]s are unions of face simplices, this allows to compute joins of horns with simplices.

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

Notice that while thus $\Delta[n+1] \simeq  \Delta[0]\star\Delta[n] \simeq \Delta[n] \star \Delta[0]$ the identifications of the cone point of course differ in both cases. The asymmetry is seen for instance by restricting attenion to the cone over the boundary of the $n$-simplex, where we have

$$
  \partial \Delta[n] \star \Delta[0] = \Lambda_{n+1}[n+1]
$$

and

$$
  \Delta[0] \star \partial \Delta[n] = \Lambda_0[n+1]
  \,.
$$

### Simplicial $n$-sphere

Let $\partial \Delta[1] = \Delta[0] \coprod \Delta[0]$ the **simplicial 0-sphere**: just the disjoint union of the point. Then the $n$-fold join of $\partial \Delta[1]$ with itself is a simplicial model for the $n$-sphere

$$
  \mathbf{S}^0 := \partial \Delta[0]
$$

$$
  \mathbf{S}^n := \mathbf{S}^0 \star \mathbf{S}^{n-1}
$$

for $n \in \mathbb{N}$, $n \gt 0$. The [[geometric realization]] of $\mathbf{S}^n$ is equivalent to the topological $n$-sphere.

See [Ehlers/Porter p. 8](http://arxiv.org/PS_cache/math/pdf/9904/9904039v1.pdf#page=8).


## References

(please augment this?)

The join operation was studied by P. J. Ehlers, in his thesis

* _Algebraic Homotopy in Simplicially Enriched Groupoids_, 1993, 
University of Wales Bangor, available [[Ehlers-thesis.pdf|here:file]], (see also the reference below and the Menagerie notes available from [[Tim Porter]]'s homepage.),

but was there ascribed to [[Jack Duskin]] and [[Don van Osdol]] in some unpublished notes.  The main ideas were derived there from earlier work of [[Bill Lawvere]].

A useful published reference is

* P. J. Ehlers and [[Tim Porter]], _Joins for (Augmented) Simplicial Sets_,  Jour. Pure Applied Algebra, 145 (2000) 37-44
([arXiv](http://arxiv.org/abs/math.CT/9904039)) .

A useful discussion emphasizing the Day convolution operation is also in section 3.1 of

* [[Dominic Verity]], _Weak complicial sets I_ ([arXiv](http://arxiv.org/abs/math/0604414))

