
#Contents#
* table of contents
{:toc}

##The Knot Group of a Knot##
The **knot group**, $G(K)$, of a knot $K$ is the [[fundamental group]] of the complement of the knot.  Taking this apart, the knot, $K$, is an embedding of $S^1$ into $\mathbb{R}^3$ or $S^3$. We tend to abuse terminology and to think (and write) of $K$ as  the image of the embedding rather than the embedding itself. (If you perform an ambient [[isotopy]] on the knot then it deforms this complement into the complement of the isotopic knot.) . We can therefore write $\mathbf{R}^3-K$ for the space outside the knot, i.e. its complement.  This is clearly arcwise connected so we do not need to worry about a choice of base point any point will do.  We make the 
+--{: .un_defn}
######Definition######
$G(K) := \pi_1(\mathbf{R}^3-K)$.

=--

This is fine, but does not tell us how to calculate anything about this group for a given knot. Luckily there are two neat algorithms for giving [[group presentation|presentations]] of $G(K)$ for arbitrary knots, one due to Wirtinger, the other to Dehn.

##The Dehn Presentation##
Orient the knot diagram.  that diagram will divide the plane into various faces.  Label these faces with distinct letters. We will use $x_1,\ldots, x_n$. (These face labels will be the generators in the presentation.)  

For the relations, we get one such for each crossing:

A typical crossing will have a configuration something like this:

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="233.634"
   height="224.59447"
   id="svg2391"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="Dehn.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
  <defs
     id="defs2393">
    <marker
       inkscape:stockid="Arrow1Lstart"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow1Lstart"
       style="overflow:visible">
      <path
         id="path3183"
         d="M 0,0 L 5,-5 L -12.5,0 L 5,5 L 0,0 z"
         style="fill-rule:evenodd;stroke:#000000;stroke-width:1pt;marker-start:none"
         transform="matrix(0.8,0,0,0.8,10,0)" />
    </marker>
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 372.04724 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_z="1052.3622 : 372.04724 : 1"
       inkscape:persp3d-origin="526.18109 : 248.03149 : 1"
       id="perspective2400" />
  </defs>
  <sodipodi:namedview
     inkscape:document-units="mm"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     inkscape:pageopacity="0.0"
     inkscape:pageshadow="2"
     inkscape:zoom="1.7366334"
     inkscape:cx="196.00862"
     inkscape:cy="481.47225"
     inkscape:current-layer="layer1"
     id="namedview2395"
     showgrid="false"
     inkscape:window-width="663"
     inkscape:window-height="701"
     inkscape:window-x="37"
     inkscape:window-y="22" />
  <metadata
     id="metadata2397">
    <rdf:RDF>
      <cc:Work
         rdf:about="">
        <dc:format>image/svg+xml</dc:format>
        <dc:type
           rdf:resource="http://purl.org/dc/dcmitype/StillImage" />
      </cc:Work>
    </rdf:RDF>
  </metadata>
  <g
     inkscape:label="Layer 1"
     inkscape:groupmode="layer"
     id="layer1"
     transform="translate(-96.238895,-163.1615)">
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.99921262;stroke-linecap:butt;stroke-linejoin:miter;marker-start:url(#Arrow1Lstart);marker-mid:url(#Arrow1Lstart);marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 225.28771,269.03633 L 225.14827,373.26205 M 223.99661,163.66111 L 224.71188,253.48901"
       id="path2404"
       sodipodi:nodetypes="cccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 96.738895,246.58017 C 97.506664,246.58017 98.274433,246.58017 96.738895,246.58017 z"
       id="path2406" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 119.77197,260.40001 L 329.3729,260.40001"
       id="path2408" />
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="157.77654"
       y="209.15143"
       id="text4473"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4475"
         x="157.77654"
         y="209.15143">x_i</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="164.68645"
       y="319.71017"
       id="text4477"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4479"
         x="164.68645"
         y="319.71017">x_j</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="275.82101"
       y="317.98267"
       id="text4481"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4483"
         x="275.82101"
         y="317.98267">x_k</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="270.06274"
       y="207.99977"
       id="text4485"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4487"
         x="270.06274"
         y="207.99977">x_l</tspan></text>
  </g>
</svg>

(The underpass is oriented upwards)

Look at the underpass arc that leaves the crossing, and write down the face labels going anticlockwise around the crossing, and alternating in exponent between +1 and -1.  Here that give $x_i x_j^{-1}x_k x_l^{-1}$.  Finally set any _one_ face label, say, $x_m$, to be 1. (This last relation effectively deletes $x_m$ from the presentation.)


That gives the presentation, 

$$\langle x_1, \ldots, x_n\mid relations from crossings, x_m=1\rangle.$$

This is a presentation of $G(K)$.


##Example of a Dehn presentation##
 We will calculate the Dehn presentation for the cinquefoil knot.  (This is the next knot in the family of $(2,k)$-torus knots after the [[trefoil]].  It has five lobes when drawn in the nice symmatric form.) We orient the diagram clockwise and have labelled the faces of the diagram with the letters $a$, up to $g$.  

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="195.79779"
   height="177.19151"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   version="1.0"
   sodipodi:docname="cinquefoil.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape">
  <defs
     id="defs4">
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 526.18109 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_z="744.09448 : 526.18109 : 1"
       inkscape:persp3d-origin="372.04724 : 350.78739 : 1"
       id="perspective10" />
  </defs>
  <sodipodi:namedview
     id="base"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     gridtolerance="10000"
     guidetolerance="10"
     objecttolerance="10"
     inkscape:pageopacity="0.0"
     inkscape:pageshadow="2"
     inkscape:zoom="2.1513506"
     inkscape:cx="273.87673"
     inkscape:cy="518.54738"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="744"
     inkscape:window-height="701"
     inkscape:window-x="256"
     inkscape:window-y="22" />
  <metadata
     id="metadata7">
    <rdf:RDF>
      <cc:Work
         rdf:about="">
        <dc:format>image/svg+xml</dc:format>
        <dc:type
           rdf:resource="http://purl.org/dc/dcmitype/StillImage" />
      </cc:Work>
    </rdf:RDF>
  </metadata>
  <g
     inkscape:label="Layer 1"
     inkscape:groupmode="layer"
     id="layer1"
     transform="translate(-163.8269,-141.69629)">
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 218.93224,259.97999 C 218.93224,259.97999 202.60173,296.18216 203.59304,316.45613 C 204.18269,328.51549 298.18478,250.6835 298.18478,250.6835 M 307.01644,244.64079 C 307.01644,244.64079 363.56876,208.83066 358.84435,201.17972 C 355.78014,196.21739 241.82483,200.94731 241.82483,200.94731 M 232.99317,200.48249 C 232.99317,200.48249 168.87236,197.0043 164.78021,204.43349 C 156.80522,218.91187 256.69921,277.64332 256.69921,277.64332 M 223.58048,249.28903 C 223.58048,249.28903 249.45695,145.96586 257.28025,142.37945 C 265.6016,138.56471 281.45111,195.60183 281.45111,195.60183 M 285.63452,205.82796 C 285.63452,205.82796 331.93083,309.2097 328.16594,317.6182 C 325.0767,324.5177 265.53087,282.75638 265.53087,282.75638"
       id="path3235"
       sodipodi:nodetypes="csccsccsccsccsc" />
    <text
       xml:space="preserve"
       style="font-size:12px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="257.04782"
       y="239.2953"
       id="text3292"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan3294"
         x="257.04782"
         y="239.2953">f</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:12px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="199.87444"
       y="220.2375"
       id="text3296"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan3298"
         x="199.87444"
         y="220.2375">a</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:12px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="257.97748"
       y="182.58675"
       id="text3300"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan3302"
         x="257.97748"
         y="182.58675">b</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:12px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="311.89709"
       y="217.91339"
       id="text3304"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan3306"
         x="311.89709"
         y="217.91339">c</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:12px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="297.48755"
       y="282.52396"
       id="text3308"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan3310"
         x="297.48755"
         y="282.52396">d</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:12px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="225.9046"
       y="283.91843"
       id="text3312"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan3314"
         x="225.9046"
         y="283.91843">e</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:12px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="204.9875"
       y="167.24754"
       id="text3316"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan3318"
         x="204.9875"
         y="167.24754">g</tspan></text>
  </g>
</svg>

We start with the crossing in the top left. The underpass is going from left to right and has $b$ to its left as it exits from under the overpass. Reading off the relation for this we get $bg^{-1}af^{-1}$. We go to the next (clockwise) crossing and similarly get $cg^{-1}bf^{-1}$; continuing we get $dg^{-1}cf^{-1}$, then $eg^{-1}df^{-1}$, and for the final crossing $ag^{-1}ef^{-1}$.

We will choose to kill off $g$ setting it equal to 1 (and eliminating it from the presentation). This gives 

$$\langle a,b,c,d,e\mid baf^{-1}=cbf^{-1}= dcf^{-1}=edf^{-1}=aef^{-1}=1\rangle.$$


This is 'the' **Dehn presentation** of $G(K)$ for this knot

We can eliminate $f$ as it can be expressed in terms of the other generators.  This gives us

$$\langle a,b,c,d,e\mid ba = cb =dc= ed = ae\rangle.$$

(This does correspond to something neat.  The 'geometric' significance of the faces is they represent a path that starts above the 'page' goes down through that face then comes up through the face labelled $g$ (as we set that equal to 1). The presentation in its current form shows that going down through any of the lobes back up then down through the next one to the left you end up going through the middle!.) It can be useful to keep $f$ in the presentation as we will see.

This group presentation is [[Tietze transformation|Tietze equivalent]] to $\langle f,y\mid f^5 = y^2\rangle$. (Use the substitution $y=edcba$.)  Note that the nature of the cinquefoil as a (2,5)-[[torus knot]] can be seen in this presentation.

##The Wirtinger presentation##
To  get the Wirtinger presentation of $G(K)$, you label the arcs of the knot diagram rather than the faces. The arc labels will give the generators in this presentation and the crossings will give the relations.  

Suppose the crossing looks like

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="233.634"
   height="224.59447"
   id="svg2391"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="Wirtinger.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
  <defs
     id="defs2393">
    <marker
       inkscape:stockid="Arrow1Lend"
       orient="auto"
       refY="0.0"
       refX="0.0"
       id="Arrow1Lend"
       style="overflow:visible;">
      <path
         id="path4234"
         d="M 0.0,0.0 L 5.0,-5.0 L -12.5,0.0 L 5.0,5.0 L 0.0,0.0 z "
         style="fill-rule:evenodd;stroke:#000000;stroke-width:1.0pt;marker-start:none;"
         transform="scale(0.8) rotate(180) translate(12.5,0)" />
    </marker>
    <marker
       inkscape:stockid="Arrow1Lstart"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow1Lstart"
       style="overflow:visible">
      <path
         id="path3183"
         d="M 0,0 L 5,-5 L -12.5,0 L 5,5 L 0,0 z"
         style="fill-rule:evenodd;stroke:#000000;stroke-width:1pt;marker-start:none"
         transform="matrix(0.8,0,0,0.8,10,0)" />
    </marker>
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 372.04724 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_z="1052.3622 : 372.04724 : 1"
       inkscape:persp3d-origin="526.18109 : 248.03149 : 1"
       id="perspective2400" />
  </defs>
  <sodipodi:namedview
     inkscape:document-units="mm"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     inkscape:pageopacity="0.0"
     inkscape:pageshadow="2"
     inkscape:zoom="1.7366334"
     inkscape:cx="196.00862"
     inkscape:cy="108.29132"
     inkscape:current-layer="layer1"
     id="namedview2395"
     showgrid="false"
     inkscape:window-width="663"
     inkscape:window-height="701"
     inkscape:window-x="37"
     inkscape:window-y="22" />
  <metadata
     id="metadata2397">
    <rdf:RDF>
      <cc:Work
         rdf:about="">
        <dc:format>image/svg+xml</dc:format>
        <dc:type
           rdf:resource="http://purl.org/dc/dcmitype/StillImage" />
      </cc:Work>
    </rdf:RDF>
  </metadata>
  <g
     inkscape:label="Layer 1"
     inkscape:groupmode="layer"
     id="layer1"
     transform="translate(-96.238895,-163.1615)">
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.99921262;stroke-linecap:butt;stroke-linejoin:miter;marker-start:url(#Arrow1Lstart);marker-mid:url(#Arrow1Lstart);marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 225.28771,269.03633 L 225.14827,373.26205 M 223.99661,163.66111 L 224.71188,253.48901"
       id="path2404"
       sodipodi:nodetypes="cccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 96.738895,246.58017 C 97.506664,246.58017 98.274433,246.58017 96.738895,246.58017 z"
       id="path2406" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.99921260000000001;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;stroke-miterlimit:4;stroke-dasharray:none;marker-end:url(#Arrow1Lend)"
       d="M 119.77197,260.40001 L 329.3729,260.40001"
       id="path2408" />
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="150.86662"
       y="281.12976"
       id="text4473"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4475"
         x="150.86662"
         y="281.12976">x_i</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="228.02739"
       y="217.21301"
       id="text4477"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4479"
         x="228.02739"
         y="217.21301">x_j</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="229.17905"
       y="327.77173"
       id="text4481"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4483"
         x="229.17905"
         y="327.77173">x_k</tspan></text>
  </g>
</svg>
 with the overpass going from left to right and the underpass from bottom to top.

Pick one of the quadrants and think of a rectanglar path going anti-clockwise about the crossing.  (We will assume we have started this path in the NW quadrant, to the left of the exit.) 
Traverse this rectangular path and write down the arc label if the arc is entering the crossing and (arc label)$^{-1}$ if it is leaving it.  In the above situation we get $x_i  x_k x_i^{-1} x_j^{-1}$ which we equate to 1. Now repeat for all the other crossings.

The **Wirtinger presentation** is then

$$\langle arc labels \mid crossing relations\rangle$$

It is worth noting that any one of the crossing relations is a consequence of the others.  (HINT: If doing an example, do not throw away a crossing relation just because it is redundant, rather keep it and it will act as a check on the final form of the presentation when it has been 'processed' through some Tietze transformations. It is easy at least to start with, to make a slip in the calculation and often the presentation in nice simple knots can be reduced to a two generator one relator form.  The above trick keeps in a duplicate relator for comparison.) 




 
