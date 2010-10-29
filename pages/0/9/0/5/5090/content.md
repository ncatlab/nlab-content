
#Contents#
* table of contents
{:toc}

##The Knot Group of  Knot##
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