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

+-- {: style="text-align:center"}
<svg width="640" height="200" xmlns="http://www.w3.org/2000/svg" se:nonce="40405" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <title/>
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_fw1" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000"/>
  </marker>
  <marker viewBox="0 0 10 10" id="se_arrow_fw2" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000"/>
  </marker>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_40405_fw3" viewBox="0 0 10 10">
   <path fill="#000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g>
  <g id="svg_40405_5">
   <g id="svg_40405_3">
    <g id="svg_40405_1">
     <rect x="275.000006" y="32.75" width="71.999994" height="74" id="svg_51" fill="#bfbdbd" stroke="#000" stroke-dasharray="5,5" stroke-width="0"/>
     <path d="m277,102.802002l68.041992,0.947998l0.958008,-73" transform="rotate(-90, 311.5, 67.25)" fill="#d1d1d1" stroke="#000" stroke-width="0" stroke-dasharray="5,5" id="svg_54"/>
    </g>
    <g id="svg_40405_2">
     <text x="275" y="41.25" id="svg_22" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" font-size="24">0</text>
     <text x="347" y="41.25" id="svg_23" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" font-size="24">1</text>
     <text x="276" y="115.25" id="svg_24" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" font-size="24">0'</text>
     <text x="348" y="115.25" id="svg_25" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" font-size="24">1'</text>
     <text x="311.121" y="95.25" id="svg_20" fill="#000000" stroke="#000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="18" font-family="serif">g</text>
     <text x="310.379" y="23.75" id="svg_19" fill="#000000" stroke="#000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="18" font-family="Serif">f</text>
    </g>
   </g>
   <g id="svg_17">
    <text x="77.379" y="23.75" id="svg_7" fill="#000000" stroke="#000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="18" font-family="Serif">f</text>
    <text x="78.121" y="95.25" id="svg_8" fill="#000000" stroke="#000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="18" font-family="serif">g</text>
    <g id="svg_11">
     <text x="42" y="41.25" id="svg_1" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" font-size="24">0</text>
     <text x="114" y="41.25" id="svg_2" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" font-size="24">1</text>
     <text x="44" y="115.25" id="svg_3" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" font-size="24">0'</text>
     <text x="116" y="115.25" id="svg_4" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" font-size="24">1'</text>
    </g>
   </g>
   <g id="svg_40405_4">
    <line x1="177" y1="76.25" x2="233.000001" y2="76.25" id="svg_9" stroke="#000" stroke-width="5" stroke-dasharray="null" fill="none" marker-end="url(#se_arrow_fw1)"/>
    <text x="203.379" y="56.75" font-family="Serif" fill="#000000" stroke="#000" stroke-width="0" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="21" id="svg_10">f &#9733; g</text>
   </g>
  </g>
  <g id="svg_58">
   <g id="svg_56">
    <path d="m528.389648,109.890015l7.947998,-49.785004l-19.844971,-54.153015" transform="rotate(-141.911, 526.414, 58.0341)" fill="#b5b5b5" stroke="#000" stroke-width="0" stroke-dasharray="5,5" id="svg_55"/>
    <path d="m515.690186,94.903839l74.848511,38.811615l-13.719116,-104.694855" id="svg_52" fill="#c4c4c4" stroke="#000" stroke-width="0" stroke-dasharray="5,5" transform="rotate(-141.911, 553.138, 81.2382)"/>
   </g>
   <g id="svg_57">
    <text x="556.335" y="25.5" font-size="24" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" id="svg_39">0</text>
    <text x="519.335" y="58.5" font-size="24" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" id="svg_40">1</text>
    <text x="500.335" y="116.5" font-size="24" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" id="svg_41">0'</text>
    <text x="590.335" y="101.5" font-size="24" fill="#000000" stroke="#000000" stroke-width="0" text-anchor="middle" font-family="serif" xml:space="preserve" id="svg_42">1'</text>
   </g>
  </g>
  <g transform="rotate(35.423, 434.16, 66.8887)" id="svg_62">
   <text x="309.5" y="245" id="svg_32" fill="#000000" stroke="#000" stroke-width="2" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="63" font-family="serif" transform="matrix(1.54059, -1.04908, 1.07873, 1.49824, -279.138, 66.9606)">=</text>
   <path d="m403.585632,77.811661c-33.321533,-34.810257 66.225647,-11.639313 30.302063,-49.09108" id="svg_61" fill="none" stroke="#000" stroke-width="4" stroke-dasharray="null"/>
  </g>
  <title>Layer 1</title>
  <polyline se:connector="svg_40 svg_41" id="svg_50" points="516.715,58.5 509.836,79.5 502.957,100.5" stroke="#000" marker-end="url(#se_arrow_fw2)" fill="none"/>
  <polyline se:connector="svg_39 svg_42" id="svg_49" points="560.02,25.5 573.836,55.5 587.652,85.5" stroke="#000" marker-end="url(#se_arrow_fw2)" fill="none"/>
  <polyline se:connector="svg_40 svg_42" id="svg_48" points="522.336,52.2917 553.836,71.1042 585.336,89.9167" stroke="#000" marker-end="url(#se_arrow_fw2)" fill="none" stroke-dasharray="5,5"/>
  <polyline se:connector="svg_41 svg_42" id="svg_46" points="507.336,107.346 546.336,100.918 585.336,94.489" stroke="#000" marker-end="url(#se_arrow_fw2)" fill="none"/>
  <polyline se:connector="svg_39 svg_40" id="svg_45" points="551.336,21.9595 536.836,34.8919 522.336,47.8243" stroke="#000" marker-end="url(#se_arrow_fw2)" fill="none"/>
  <polyline se:connector="svg_23 svg_25" id="svg_31" points="347.216,41.25 348,70.25 348.784,99.25" stroke="#000" fill="none" marker-end="url(#se_arrow_fw2)"/>
  <polyline se:connector="svg_23 svg_24" id="svg_30" points="344,36.3768 313.5,68.1655 283,99.9542" stroke="#000" marker-end="url(#se_arrow_fw2)" fill="none" stroke-dasharray="5,5"/>
  <polyline se:connector="svg_22 svg_25" id="svg_29" points="280,38.25 311.5,69.75 343,101.25" stroke="#000" fill="none" marker-end="url(#se_arrow_fw2)"/>
  <polyline se:connector="svg_22 svg_24" id="svg_28" points="275.108,41.25 275.5,70.25 275.892,99.25" stroke="#000" fill="none" marker-end="url(#se_arrow_fw2)"/>
  <polyline se:connector="svg_24 svg_25" id="svg_27" points="283,107.25 313,107.25 343,107.25" stroke="#000" fill="none" marker-end="url(#se_arrow_fw2)"/>
  <polyline se:connector="svg_22 svg_23" id="svg_26" points="280,33.25 312,33.25 344,33.25" stroke="#000" fill="none" marker-end="url(#se_arrow_fw2)"/>
  <polyline se:connector="svg_3 svg_4" id="svg_6" points="51,107.25 81,107.25 111,107.25" stroke="#000" fill="none" marker-end="url(#se_arrow_fw1)"/>
  <polyline se:connector="svg_1 svg_2" id="svg_5" points="47,33.25 79,33.25 111,33.25" stroke="#000" fill="none" marker-end="url(#se_arrow_fw1)"/>
  <path d="m465,82" id="svg_53" fill="#b2b2b2" stroke="#000" stroke-width="0" stroke-dasharray="5,5" opacity="0.5"/>
  <polyline se:connector="svg_39 svg_41" id="svg_47" points="551.413,25.5 528.336,63 505.259,100.5" stroke="#000" marker-end="url(#se_arrow_fw2)" fill="none"/>
  <g id="svg_40405_28">
   <text xml:space="preserve" text-anchor="middle" font-family="Serif" font-size="21" stroke-dasharray="5,5" stroke-width="0" stroke="#000" fill="#000000" id="svg_40405_7" y="168.531" x="142">f</text>
   <g id="svg_40405_8" transform="rotate(35.423, 173.357, 162.182)">
    <text id="svg_40405_9" x="309.5" y="245" fill="#000000" stroke="#000" stroke-width="2" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="63" font-family="serif" transform="matrix(0.550903, -0.375143, 0.385746, 0.535759, -81.5646, 162.131)">=</text>
    <path id="svg_40405_10" d="m162.572357,166.010895c-11.915543,-12.447906 23.681808,-4.16214 10.835785,-17.554596" fill="none" stroke="#000" stroke-width="2" stroke-dasharray="null"/>
   </g>
   <g id="svg_40405_11" transform="rotate(35.423, 232.357, 162.932)">
    <text id="svg_40405_12" x="309.5" y="245" fill="#000000" stroke="#000" stroke-width="2" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="63" font-family="serif" transform="matrix(0.550903, -0.375143, 0.385746, 0.535759, -22.565, 162.881)">=</text>
    <path id="svg_40405_13" d="m221.572357,166.760895c-11.915543,-12.447906 23.681793,-4.16214 10.835785,-17.554596" fill="none" stroke="#000" stroke-width="2" stroke-dasharray="null"/>
   </g>
   <text xml:space="preserve" text-anchor="middle" font-family="Serif" font-size="21" stroke-dasharray="5,5" stroke-width="0" stroke="#000" fill="#000000" id="svg_40405_14" y="169.781" x="201">g</text>
   <text xml:space="preserve" text-anchor="middle" font-family="Serif" font-size="21" stroke-dasharray="5,5" stroke-width="0" stroke="#000" fill="#000000" id="svg_40405_15" y="168.279" x="269">[1]</text>
   <text xml:space="preserve" text-anchor="middle" font-family="Serif" font-size="21" stroke-dasharray="5,5" stroke-width="0" stroke="#000" fill="#000000" id="svg_40405_17" y="169.766" x="398">f &#9733; g</text>
   <g id="svg_40405_18" transform="rotate(35.423, 449.357, 162.908)">
    <text id="svg_40405_19" x="309.5" y="245" fill="#000000" stroke="#000" stroke-width="2" stroke-dasharray="null" text-anchor="middle" xml:space="preserve" font-size="63" font-family="serif" transform="matrix(0.550903, -0.375143, 0.385746, 0.535759, 194.435, 162.859)">=</text>
    <path id="svg_40405_20" d="m438.572357,166.73941c-11.915558,-12.447906 23.681793,-4.16214 10.835785,-17.554596" fill="none" stroke="#000" stroke-width="2" stroke-dasharray="null"/>
   </g>
   <text xml:space="preserve" text-anchor="middle" font-family="Serif" font-size="21" stroke-dasharray="5,5" stroke-width="0" stroke="#000" fill="#000000" id="svg_40405_21" y="170.258" x="489">[3]</text>
   <g id="svg_40405_26">
    <text transform="matrix(2.5, 0, 0, 2.5, -294, -243.75)" xml:space="preserve" text-anchor="middle" font-family="Serif" font-size="21" stroke-width="0" stroke="#000" fill="#000000" id="svg_40405_24" y="170.3" x="244.8">=</text>
    <line transform="rotate(11.5922, 333.67, 163.543)" marker-end="url(#se_arrow_40405_fw3)" fill="none" stroke-width="7" stroke="#000" id="svg_40405_25" y2="160.453832" x2="346.030645" y1="166.63392" x1="321.310291"/>
   </g>
  </g>
 </g>
</svg>
=--


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

