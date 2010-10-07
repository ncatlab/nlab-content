
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The _Reidemeister moves_ are local changes to [[knot]] or [[link]] [[knot diagram|diagrams]].  

These moves were given in the book by [Reidemeister](#Reidemeister).


## Definition

We define the Reidemeister moves in terms of link diagrams

The conventions are that part of the diagram is shown with the 'move' indicated, but that outside that, the diagram of the link is unchanged and that no other part of the diagram appears at the crossings that are changed by that move. 


+-- {: .un_remark}
###### Note
In manipulating a link diagram, the changes obtained by elongating part of the diagram, rotating it, etc., are not counted as changing the structure of the diagram provided they do not change any crossing,and so they may be done without comment.  The 'moves' outlined here do change things locally near crossings.
=--


### First Reidemeister moves

The local configurations

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="491.70352"
   height="71.294533"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="R1.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
  <defs
     id="defs4">
    <marker
       inkscape:stockid="Arrow2Lstart"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow2Lstart"
       style="overflow:visible">
      <path
         id="path3695"
         style="font-size:12px;fill-rule:evenodd;stroke-width:0.625;stroke-linejoin:round"
         d="M 8.7185878,4.0337352 L -2.2072895,0.016013256 L 8.7185884,-4.0017078 C 6.97309,-1.6296469 6.9831476,1.6157441 8.7185878,4.0337352 z"
         transform="matrix(1.1,0,0,1.1,1.1,0)" />
    </marker>
    <marker
       inkscape:stockid="Arrow2Lend"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow2Lend"
       style="overflow:visible">
      <path
         id="path3698"
         style="font-size:12px;fill-rule:evenodd;stroke-width:0.625;stroke-linejoin:round"
         d="M 8.7185878,4.0337352 L -2.2072895,0.016013256 L 8.7185884,-4.0017078 C 6.97309,-1.6296469 6.9831476,1.6157441 8.7185878,4.0337352 z"
         transform="matrix(-1.1,0,0,-1.1,-1.1,0)" />
    </marker>
    <marker
       inkscape:stockid="Arrow1Lend"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow1Lend"
       style="overflow:visible">
      <path
         id="path3680"
         d="M 0,0 L 5,-5 L -12.5,0 L 5,5 L 0,0 z"
         style="fill-rule:evenodd;stroke:#000000;stroke-width:1pt;marker-start:none"
         transform="matrix(-0.8,0,0,-0.8,-10,0)" />
    </marker>
    <marker
       inkscape:stockid="Arrow1Lstart"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow1Lstart"
       style="overflow:visible">
      <path
         id="path3677"
         d="M 0,0 L 5,-5 L -12.5,0 L 5,5 L 0,0 z"
         style="fill-rule:evenodd;stroke:#000000;stroke-width:1pt;marker-start:none"
         transform="matrix(0.8,0,0,0.8,10,0)" />
    </marker>
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
     inkscape:zoom="0.25"
     inkscape:cx="171.90552"
     inkscape:cy="621.5238"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="663"
     inkscape:window-height="701"
     inkscape:window-x="109"
     inkscape:window-y="22">
    <inkscape:grid
       type="xygrid"
       id="grid9239"
       visible="true"
       enabled="true" />
  </sodipodi:namedview>
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
     transform="translate(-57.30519,-171.86218)">
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 57.80519,242.65671 C 57.80519,242.65671 84.00609,217.31232 90,212.36218 M 60,172.36218 C 99.28571,217.36218 147.98375,254.12993 170.26054,233.52726 C 186.58852,218.42632 184.76947,190.96029 171.37662,178.72815 C 158.70779,167.02591 123.26136,183.99019 99.28571,203.79075"
       id="path2383"
       sodipodi:nodetypes="cccscs" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 240,242.36218 C 240,242.36218 265.42782,218.92903 273.20744,212.90747 C 298.96881,192.03548 340.60384,237.54528 359.22692,239.63058 C 374.87877,241.38318 365.24447,170.823 343.11085,173.00112 C 321.04694,175.17238 297.23247,193.14789 281.42715,198.09115 C 265.62184,203.03441 257.82567,194.94543 239.22692,173.55915"
       id="path2385"
       sodipodi:nodetypes="ccsssc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 424.3484,172.62081 C 424.3484,172.62081 445.006,189.41204 454,198.36218 M 420,242.36218 C 459.2857,197.36218 514.527,161.14759 536.8038,181.75026 C 553.1318,196.8512 551.3127,224.31723 537.9199,236.54937 C 525.251,248.25161 489.8046,231.28733 465.829,211.48677"
       id="path2391"
       sodipodi:nodetypes="cccscs" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.88990498px;stroke-linecap:butt;stroke-linejoin:miter;marker-start:url(#Arrow2Lstart);marker-end:url(#Arrow2Lstart);stroke-opacity:1"
       d="M 377.7646,205.35902 C 419.21279,204.34637 407.48217,205.35902 407.48217,205.35902"
       id="path2393" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.88990498px;stroke-linecap:butt;stroke-linejoin:miter;marker-start:url(#Arrow2Lstart);marker-end:url(#Arrow2Lstart);stroke-opacity:1"
       d="M 196.74301,210.07593 C 238.1912,209.06328 226.46058,210.07593 226.46058,210.07593"
       id="path9237" />
  </g>
</svg>


are interchangable;

### Second Reidemeister move
The configurations

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="649.51794"
   height="153.89018"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   version="1.0"
   sodipodi:docname="R2.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape">
  <defs
     id="defs4">
    <marker
       inkscape:stockid="Arrow2Lstart"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow2Lstart"
       style="overflow:visible">
      <path
         id="path3695"
         style="font-size:12px;fill-rule:evenodd;stroke-width:0.625;stroke-linejoin:round"
         d="M 8.7185878,4.0337352 L -2.2072895,0.016013256 L 8.7185884,-4.0017078 C 6.97309,-1.6296469 6.9831476,1.6157441 8.7185878,4.0337352 z"
         transform="matrix(1.1,0,0,1.1,1.1,0)" />
    </marker>
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
     inkscape:zoom="0.35355339"
     inkscape:cx="736.30215"
     inkscape:cy="475.74479"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="640"
     inkscape:window-height="701"
     inkscape:window-x="0"
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
     transform="translate(-171.22594,-188.01058)">
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.66998518px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 171.56093,188.34557 C 208.78998,198.79212 260.43467,215.02457 264.20271,262.98346 C 264.0013,312.9415 175.31667,331.7674 175.31667,331.7674"
       id="path2383"
       sodipodi:nodetypes="ccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.66998518px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 245.79131,304.07158 C 265.1305,317.16567 308.37308,332.58643 308.37308,332.58643 M 240.40291,224.91642 C 230.22425,232.70378 225.29963,235.53733 220.20133,258.80249 C 220.30203,283.78151 229.30926,287.04892 240.79131,299.42873 M 309.27168,192.73603 C 290.65715,197.95931 267.01015,208.20048 248.97434,219.55928"
       id="path2389"
       sodipodi:nodetypes="ccccscs" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.69240087px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 383.70415,191.35298 C 422.54732,202.0466 476.43114,218.66297 480.36254,267.75617 C 480.1524,318.89579 387.62273,338.16695 387.62273,338.16695"
       id="path2391"
       sodipodi:nodetypes="ccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.69240087px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 590.08289,188.35678 C 551.23972,199.0504 497.3559,215.66677 493.4245,264.75997 C 493.63464,315.89959 586.16431,335.17075 586.16431,335.17075"
       id="path2397"
       sodipodi:nodetypes="ccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.66998518px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 682.69812,193.39634 C 719.92717,203.84289 771.57186,220.07534 775.3399,268.03423 C 775.13849,317.99227 686.45386,336.81817 686.45386,336.81817"
       id="path2399"
       sodipodi:nodetypes="ccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.66998518px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 749.4285,306.44378 C 743.66073,301.83183 725.72494,285.97514 726.51709,266.53183 C 725.72254,249.87382 739.93286,235.6117 752.25439,228.18147 M 755.49992,311.08664 C 774.12483,325.69858 819.51027,341.56577 819.51027,341.56577 M 820.40887,197.7868 C 801.79435,203.01007 776.71877,210.75125 759.39724,223.89576"
       id="path2401"
       sodipodi:nodetypes="ccscccs" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.88990498px;stroke-linecap:butt;stroke-linejoin:miter;marker-start:url(#Arrow2Lstart);marker-end:url(#Arrow2Lstart);stroke-opacity:1"
       d="M 322.13396,269.03653 C 363.58215,268.02388 351.85153,269.03653 351.85153,269.03653"
       id="path9237" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.88990498px;stroke-linecap:butt;stroke-linejoin:miter;marker-start:url(#Arrow2Lstart);marker-end:url(#Arrow2Lstart);stroke-opacity:1"
       d="M 627.20003,273.07714 C 668.64822,272.06449 656.9176,273.07714 656.9176,273.07714"
       id="path2486" />
  </g>
</svg>

are interchangeable;

### Third Reidemeister move
The configurations

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="569.81653"
   height="233.85715"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   version="1.0"
   sodipodi:docname="R3.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape">
  <defs
     id="defs4">
    <marker
       inkscape:stockid="Arrow2Lstart"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow2Lstart"
       style="overflow:visible">
      <path
         id="path3695"
         style="font-size:12px;fill-rule:evenodd;stroke-width:0.625;stroke-linejoin:round"
         d="M 8.7185878,4.0337352 L -2.2072895,0.016013256 L 8.7185884,-4.0017078 C 6.97309,-1.6296469 6.9831476,1.6157441 8.7185878,4.0337352 z"
         transform="matrix(1.1,0,0,1.1,1.1,0)" />
    </marker>
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
     inkscape:zoom="0.98994949"
     inkscape:cx="418.33704"
     inkscape:cy="426.13595"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="640"
     inkscape:window-height="701"
     inkscape:window-x="0"
     inkscape:window-y="22">
    <inkscape:grid
       type="xygrid"
       id="grid2506"
       visible="true"
       enabled="true" />
  </sodipodi:namedview>
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
     transform="translate(-148.07143,-145.02305)">
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 157.14286,149.80877 L 342.85714,378.3802"
       id="path2413" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 300,217.66591 L 374.28571,218.3802 M 219.64285,218.3802 L 261.42857,218.3802 L 289.64286,218.3802 M 148.57143,218.3802 L 205,218.3802"
       id="path2417"
       sodipodi:nodetypes="ccccccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 258.92857,280.52305 L 237.14286,318.38019 L 205.71429,372.66591 M 331.42857,155.52305 L 300,209.80876 L 263.21429,273.73734"
       id="path2419"
       sodipodi:nodetypes="cccccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 494.28572,145.52305 L 680,374.09448"
       id="path2421" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 645.8071,326.2881 L 717.38796,327.29825 M 569.31545,328.3084 L 628.63451,328.3084 M 491.67368,327.29825 L 548.10225,327.29825"
       id="path2423"
       sodipodi:nodetypes="cccccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1.03613663px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 588.29877,277.13263 L 527.37631,376.38207 M 658.10521,152.20428 L 596.2613,262.22259"
       id="path2425"
       sodipodi:nodetypes="cccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1.65551579px;stroke-linecap:butt;stroke-linejoin:miter;marker-start:url(#Arrow2Lstart);marker-end:url(#Arrow2Lstart);stroke-opacity:1"
       d="M 400,264.09448 C 477.10726,262.21062 455.28445,264.09448 455.28445,264.09448"
       id="path2393" />
  </g>
</svg>

are interchangeable.

## Properties

+-- {: .un_theorem}
###### Theorem
Two [[knot diagram]]s correspond to isotopic knots precisely if they can be connected by a sequence of applications of the three Reidemeister moves.
=--
The corresponding statement for [[links]] and link diagram is also true.

## References

* Reidemeister, _Knotentheorie_ , Ergebnisse der Mathematik (1932)
{#Reidemeister}


[[!redirects Reidemeister move]]
[[!redirects Reidemeister moves]]
