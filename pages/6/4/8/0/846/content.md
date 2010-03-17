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
<svg width="470" height="300" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_fw1" viewBox="0 0 10 10">
   <path fill="#000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
  <marker refX="2" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_bk2" viewBox="0 0 10 10">
   <path fill="#000" d="m10,0l-10,5l10,5l-5,-5l5,-5z"/>
  </marker>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_fw3" viewBox="0 0 10 10">
   <path fill="#000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <g id="svg_130">
   <g id="svg_128">
    <path id="svg_124" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#d3d3d3" transform="rotate(171.277 304.499 65.1274)" d="m218.899261,50.159206l102.532623,1.932983l68.666626,28.003536l-171.199249,-29.93652z"/>
    <path id="svg_125" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#d1cfcf" transform="rotate(171.277 266.228 140.336)" d="m231.528839,195.407623l69.399536,28.428802l-47,-167.000027l-22.399536,138.571224z"/>
    <path id="svg_126" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#b5b5b5" transform="rotate(171.277 339.673 144.244)" d="m278.971008,213.622772l121.404419,-140.879189l-22,143.000038l-99.404419,-2.12085z"/>
   </g>
   <g id="svg_129">
    <text font-family="serif" font-size="24" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000000" fill="#000000" id="svg_86" y="71.139696" x="218.761949">0</text>
    <text font-family="serif" font-size="24" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000000" fill="#000000" id="svg_87" y="87.298368" x="289.746416">1</text>
    <text font-family="serif" font-size="24" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000000" fill="#000000" id="svg_88" y="75.317857" x="389.180468">2</text>
    <text font-family="serif" font-size="24" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#000000" id="svg_89" y="231.842828" x="291.410478">[0]</text>
   </g>
  </g>
  <g id="svg_127">
   <g id="svg_110">
    <path transform="rotate(-8.04566 118.504 226.091)" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#a5a5a5" id="svg_61" d="m32.904354,211.12323l102.532627,1.932983l68.666641,28.00354l-171.199268,-29.936523z"/>
    <path transform="rotate(-8.04566 158.353 151.242)" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#b7b7b7" id="svg_63" d="m124.353134,207.742065l67.999985,27.000031l-46.999985,-167.000031l-21,140z"/>
    <path transform="rotate(-8.04566 83.2128 146.714)" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#d1d1d1" id="svg_62" d="m21.445765,214.147995l123.534033,-138.933708l-21.999992,143.000023l-101.53404,-4.066315z"/>
   </g>
   <g id="svg_109">
    <text transform="rotate(1.91612 30.4613 222.672)" font-family="serif" font-size="24" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000000" fill="#000000" id="svg_71" y="230.938344" x="30.461294">0</text>
    <text transform="rotate(1.91612 134.114 210.98)" font-family="serif" font-size="24" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000000" fill="#000000" id="svg_72" y="219.246262" x="133.847098">1</text>
    <text transform="rotate(1.91612 202.727 228.505)" font-family="serif" font-size="24" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000000" fill="#000000" id="svg_73" y="236.771905" x="202.993385">2</text>
    <text transform="rotate(-8.12388 134.02 69.9918) rotate(-0.04 154.4 41.0667) rotate(10.6764 154.4 41.0667)" font-family="serif" font-size="24" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#000000" id="svg_74" y="79.123145" x="139.709132">[0]</text>
   </g>
  </g>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_86 svg_88" fill="none" stroke="#000" points="224.4 62.9549 303.35 64.9935 382.3 67.0322" id="svg_97"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_87 svg_88" fill="none" stroke="#000" points="295.6 78.4742 338.95 73.2302 382.3 67.9863" id="svg_96"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_86 svg_87" fill="none" stroke="#000" points="224.4 64.182 253.75 70.9424 283.1 77.7028" id="svg_95"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_88 svg_89" fill="none" stroke="#000" points="382.8 76.8148 341.4 143.157 299.999 209.5" id="svg_94"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_87 svg_89" fill="none" stroke="#000" points="289.751 92.8 290.397 151.15 291.044 209.5" id="svg_93"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_86 svg_89" fill="none" stroke="#000" points="224.4 76.0527 254.608 142.776 284.816 209.5" id="svg_92"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_71 svg_73" fill="none" stroke="#000" points="35.8015 222.853 116.211 225.575 196.62 228.298" id="svg_80"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_72 svg_73" fill="none" stroke="#000" points="137.588 211.867 167.104 219.406 196.62 226.945" id="svg_79"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_71 svg_72" fill="none" stroke="#000" points="35.8015 222.069 82.9704 216.749 130.139 211.428" id="svg_78"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_74 svg_73" fill="none" stroke="#000" points="138.867 81.1743 168.859 150.37 198.852 219.565" id="svg_77"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_74 svg_71" fill="none" stroke="#000" points="126.435 81.1743 81.3684 147.618 36.3015 214.061" id="svg_76"/>
  <polyline marker-end="url(#se_arrow_fw3)" se:connector="svg_74 svg_72" fill="none" stroke="#000" points="134.028 81.1743 134.068 141.642 134.108 202.111" id="svg_75"/>
  <path id="svg_85" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#bcbcbc" transform="rotate(-180 926.839 -2662.98) matrix(0.988881 -0.148709 0.148709 0.988881 -20.793 54.4602)" d="m-997.370361,873.996216l123,-139.999939l-22,142.999939l-101,-3z"/>
  <path id="svg_83" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#a5a5a5" transform="rotate(-180 -977.389 173.764) matrix(0.988881 -0.148709 0.148709 0.988881 3.38641 45.8432)" d="m255.030853,69.940491l101.466675,1.933327l66.000061,26.933342l-167.466736,-28.866669z"/>
  <g transform="rotate(8.6766 307.787 139.809) rotate(-8.61437 307.787 139.809) rotate(-8.61437 307.787 139.809)" id="svg_105"/>
  <foreignObject stroke-width="0" fill="none" height="20" width="48" font-size="16" id="svg_132" y="125" x="50">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mo stretchy="false">[</mo>
      <mn>0</mn>
      <mo stretchy="false">]</mo>
      <mo>&#8902;</mo>
      <mo stretchy="false">[</mo>
      <mn>2</mn>
      <mo stretchy="false">]</mo>
     </mrow>
     <annotation encoding="application/x-tex">[0] \star [2]</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_133" y="125" x="133.5">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mo stretchy="false">[</mo>
      <mn>2</mn>
      <mo stretchy="false">]</mo>
      <mo>&#8902;</mo>
      <mo stretchy="false">[</mo>
      <mn>0</mn>
      <mo stretchy="false">]</mo>
     </mrow>
     <annotation encoding="application/x-tex">[2] \star [0]</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>
=--  

If you take two non-coplanar line segments in $\mathbb{R}^3$ (such as $A B$ and $C D$ in the picture below), then join every point in one to every point in the other, you get a 3-simplex (the tetrahedron in the picture). You can think of this as being the union of all the cones on the first segment, with cone points on the second one. We have that the join $\Delta[1]\star \Delta[1]$ is $\Delta[3]$.

+-- {: style="text-align:center"}
<svg width="640" height="480" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_fw1" viewBox="0 0 10 10">
   <path fill="#000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_fw2" viewBox="0 0 10 10">
   <path fill="#000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <g id="svg_58">
   <g id="svg_56">
    <path id="svg_55" stroke-dasharray="5,5" stroke-width="0" stroke="#000" fill="#b5b5b5" transform="rotate(-141.911 176.415 281.921)" d="m178.389618,333.890015l7.948029,-49.785004l-19.845001,-54.153015"/>
    <path transform="rotate(-141.911 203.114 305.368)" stroke-dasharray="5,5" stroke-width="0" stroke="#000" fill="#c4c4c4" id="svg_52" d="m165.690155,318.903839l74.848572,38.811615l-13.719147,-104.694855"/>
   </g>
   <g id="svg_57">
    <text id="svg_39" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" font-size="24" y="249.5" x="206.334633">0</text>
    <text id="svg_40" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" font-size="24" y="282.5" x="169.334633">1</text>
    <text id="svg_41" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" font-size="24" y="340.5" x="150.334633">0'</text>
    <text id="svg_42" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" font-size="24" y="325.5" x="240.334633">1'</text>
   </g>
  </g>
  <rect stroke-width="0" stroke-dasharray="5,5" stroke="#000" fill="#c9c9c9" id="svg_51" height="74" width="71.999994" y="81" x="392.000006"/>
  <path id="svg_54" stroke-dasharray="5,5" stroke-width="0" stroke="#000" fill="#c4c4c4" transform="rotate(-90 428.5 115.5)" d="m394,151.052002l68.041992,0.947998l0.958008,-73"/>
  <polyline se:connector="svg_40 svg_41" fill="none" marker-end="url(#se_arrow_fw2)" stroke="#000" points="164.578 288 159.582 303.25 154.586 318.5" id="svg_50"/>
  <polyline se:connector="svg_39 svg_42" fill="none" marker-end="url(#se_arrow_fw2)" stroke="#000" points="212 254.912 222.868 279.206 233.737 303.5" id="svg_49"/>
  <polyline stroke-dasharray="5,5" se:connector="svg_40 svg_42" fill="none" marker-end="url(#se_arrow_fw2)" stroke="#000" points="175 278.134 203.25 295.243 231.5 312.352" id="svg_48"/>
  <polyline se:connector="svg_41 svg_42" fill="none" marker-end="url(#se_arrow_fw2)" stroke="#000" points="158 331.167 194.75 325.042 231.5 318.917" id="svg_46"/>
  <polyline se:connector="svg_39 svg_40" fill="none" marker-end="url(#se_arrow_fw2)" stroke="#000" points="200 246.851 187.75 257.777 175.5 268.703" id="svg_45"/>
  <polyline se:connector="svg_23 svg_25" marker-end="url(#se_arrow_fw2)" fill="none" stroke="#000" points="464.182 95 464.497 118.25 464.811 141.5" id="svg_31"/>
  <polyline se:connector="svg_23 svg_24" stroke-dasharray="5,5" fill="none" marker-end="url(#se_arrow_fw2)" stroke="#000" points="458 87.7535 429.75 117.197 401.5 146.641" id="svg_30"/>
  <polyline se:connector="svg_22 svg_25" marker-end="url(#se_arrow_fw2)" fill="none" stroke="#000" points="398 87.5822 427.25 117.233 456.5 146.884" id="svg_29"/>
  <polyline se:connector="svg_22 svg_24" marker-end="url(#se_arrow_fw2)" fill="none" stroke="#000" points="392.182 95 392.497 118.25 392.811 141.5" id="svg_28"/>
  <polyline se:connector="svg_24 svg_25" marker-end="url(#se_arrow_fw2)" fill="none" stroke="#000" points="401 155.5 428.75 155.5 456.5 155.5" id="svg_27"/>
  <polyline se:connector="svg_22 svg_23" marker-end="url(#se_arrow_fw2)" fill="none" stroke="#000" points="398 81.5 428 81.5 458 81.5" id="svg_26"/>
  <polyline se:connector="svg_3 svg_4" marker-end="url(#se_arrow_fw1)" fill="none" stroke="#000" points="169 155.5 196.75 155.5 224.5 155.5" id="svg_6"/>
  <polyline se:connector="svg_1 svg_2" marker-end="url(#se_arrow_fw1)" fill="none" stroke="#000" points="165 81.5 194.75 81.5 224.5 81.5" id="svg_5"/>
  <line marker-end="url(#se_arrow_fw1)" fill="none" stroke-dasharray="null" stroke-width="5" stroke="#000" id="svg_9" y2="124.5" x2="350.000001" y1="124.5" x1="294"/>
  <text id="svg_10" font-size="21" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#000000" font-family="Serif" y="105" x="320.378906">f &#9733; g</text>
  <text font-size="24" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" id="svg_22" y="89.5" x="392">0</text>
  <text font-size="24" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" id="svg_23" y="89.5" x="464">1</text>
  <text font-size="24" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" id="svg_24" y="163.5" x="393">0'</text>
  <text font-size="24" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" id="svg_25" y="163.5" x="465">1'</text>
  <text font-family="serif" font-size="18" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#000000" id="svg_20" y="143.5" x="428.121094">g</text>
  <g id="svg_17">
   <text font-family="Serif" font-size="18" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#000000" id="svg_7" y="72" x="194.378906">f</text>
   <text font-family="serif" font-size="18" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#000000" id="svg_8" y="143.5" x="195.121094">g</text>
   <g id="svg_11">
    <text font-size="24" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" id="svg_1" y="89.5" x="159">0</text>
    <text font-size="24" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" id="svg_2" y="89.5" x="231">1</text>
    <text font-size="24" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" id="svg_3" y="163.5" x="161">0'</text>
    <text font-size="24" xml:space="preserve" font-family="serif" text-anchor="middle" stroke-width="0" stroke="#000000" fill="#000000" id="svg_4" y="163.5" x="233">1'</text>
   </g>
  </g>
  <text font-family="Serif" font-size="18" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="0" stroke="#000" fill="#000000" id="svg_19" y="72" x="427.378906">f</text>
  <path opacity="0.5" stroke-dasharray="5,5" stroke-width="0" stroke="#000" fill="#b2b2b2" id="svg_53" d="m465,82"/>
  <polyline se:connector="svg_39 svg_41" fill="none" marker-end="url(#se_arrow_fw2)" stroke="#000" points="200 251.25 179.25 284.969 158.5 318.688" id="svg_47"/>
  <g id="svg_62">
   <text transform="matrix(1.54059 -1.04908 1.07873 1.49824 -408.138 222.224)" font-family="serif" font-size="63" xml:space="preserve" text-anchor="middle" stroke-dasharray="null" stroke-width="2" stroke="#000" fill="#000000" id="svg_32" y="245" x="309.5">=</text>
   <path stroke-dasharray="null" stroke-width="4" stroke="#000" fill="none" id="svg_61" d="m274.585632,233.075333c-33.321533,-34.810257 66.225647,-11.639313 30.302063,-49.09108"/>
  </g>
 </g>
</svg>
=--


## Definition

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
  \otimes_{join}: \Delta_a \times \Delta_a \to \Delta_a
$$
$$
  ([n], [m]) \mapsto [n + m + 1]
  \,.
$$



Now, via the general process of [[Day convolution]], this monoidal structure on $\Delta_a$ is lifted to a monoidal structure on [[presheaf|presheaves]] on $\Delta_a$, i.e. to the the category [[ASSet]] of augmented [[simplicial set]]s. This is given by the [[end|coend]] formula

$$
  \otimes_{join} : ASSet \times ASSet \to ASSet
$$
$$
  (S \otimes_{join} S')_n
  :=
  \int^{[i],[j] \in \Delta_a}
    S_i \times S'_j \cdot \Delta([n],[i] \otimes_{join} [j])
  \,.
$$

Note that the join of simplicial sets $S \star T$ is [[cocontinuous functor|cocontinuous]] in each of its separate arguments $S$, $T$ (this is true generally of Day convolution products). 

### Extension to a closed monoidal structure

This join tensor product forms part of a [[closed monoidal category|closed monoidal structure]] on the category of
augmented simplicial sets, [[ASSet]] $ := Sets^{\Delta_a^{op}}$. The [[internal hom]] is given by
$$[X, Y ]_n =ASS(X; Dec^{n+1}Y )\,,$$
where $Dec$ is the [[decalage]] functor.


### Join of non-augmented simplicial sets

The **join** of two ordinary (not augmented) [[simplicial set]]s $S$ and $S'$ is the join of their _trivial augmentation_ ($S_{-1} = S'_{-1} = pt$). This yields

$$
  (S \otimes_{join} S')_n =: (S \star S')_n := S_n \cup S'_n \cup 
   (\cup_{i+j = n-1} S_i \times S'_j)
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

This observation can help simplify calculations. For example, simplicial joins preserve unions in the first argument $S$, and inasmuch as [[horn]]s are unions of face simplices, it follows easily that 

$$\Lambda^k[m] \star \Delta[n] \cong \Lambda^k[m+n+1]$$

> (Is this right? What about the following:)

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
University of Wales Bangor, (see also the reference below and the Menagerie notes available from [[Tim Porter]]'s homepage.),

but was there ascribed to [[Jack Duskin]] and [[Don van Osdol]] in some unpublished notes.  The main ideas were derived there from earlier work of [[Bill Lawvere]].

A useful published reference is

* P. J. Ehlers and [[Tim Porter]], _Joins for (Augmented) Simplicial Sets_,  Jour. Pure Applied Algebra, 145 (2000) 37-44
([arXiv](http://arxiv.org/abs/math.CT/9904039)) .

A useful discussion emphasizing the Day convolution operation is also in section 3.1 of

* [[Dominic Verity]], _Weak complicial sets I_ ([arXiv](http://arxiv.org/abs/math/0604414))

