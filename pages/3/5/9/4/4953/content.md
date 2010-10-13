# Contents
* automatic table of contents goes here
{:toc}


##Idea##
When discussing [[language|languages]], say, in the theory of [[finite automata]], the usual starting point is a set, $\Sigma$, of symbols, which is taken to be the _alphabet_ for the language.  The next step is to form the [[free monoid]], $\Sigma^*$, on the alphabet, and then a language is simply a subset of $\Sigma^*$, and these can be used in a number of situations to describe the workings of a 'system', the symbols being used to represent certain operations or actions of the system, and the words in $\Sigma^*$ thus corresponding to sequences of operations. Usually the system will not allow arbitrary sequences of operations to be performed, and so the system determines a language, namely the allowable execution sequences. Describing the language, helps describe and determine the overall 'system'.

If the system being studied has some concurrency in it, so that certain of the operations are (causally) independent of each other, then one way of modelling such a system is to use a _Mazurkiewicz) trace alphabet_, that is one in which the independence is explicitly taken into consideration.



+--{: . un-definition}
##Definition##
A _(Mazurkiewicz) trace alphabet_ is a pair $(\Sigma, I)$ where $\Sigma$ is a (usually finite) set of _actions_ and $I \subseteq \Sigma \times \Sigma$ is an _irreflexive_ and _symmetric_ relation.
=--
The relation $I$ is usually referred to as *independence*.  Its complement $D = (\Sigma \times \Sigma) - I$ is called the _dependency_ relation.  It will be reflexive and symmetric. (Such a sense of 'dependency relation' is interpreted in a related but slightly different way from that in the use of [dependency graphs](http://en.wikipedia.org/wiki/Dependency_graph) in project planning.)

+--{: . un-example}
##Example##

Consider the following 'dependency diagram, with some vertices (states) and labelled edges (actions):

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="442.42856"
   height="203.85713"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   version="1.0"
   sodipodi:docname="dependency.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape">
  <defs
     id="defs4">
    <marker
       inkscape:stockid="Arrow2Lend"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow2Lend"
       style="overflow:visible">
      <path
         id="path3189"
         style="font-size:12px;fill-rule:evenodd;stroke-width:0.625;stroke-linejoin:round"
         d="M 8.7185878,4.0337352 L -2.2072895,0.016013256 L 8.7185884,-4.0017078 C 6.97309,-1.6296469 6.9831476,1.6157441 8.7185878,4.0337352 z"
         transform="matrix(-1.1,0,0,-1.1,-1.1,0)" />
    </marker>
    <marker
       inkscape:stockid="Arrow2Lstart"
       orient="auto"
       refY="0"
       refX="0"
       id="Arrow2Lstart"
       style="overflow:visible">
      <path
         id="path3186"
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
     inkscape:zoom="0.78209877"
     inkscape:cx="302.21784"
     inkscape:cy="362.85714"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="663"
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
     transform="translate(-125.21429,-227.8802)">
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:#ff0000;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path2383"
       sodipodi:cx="132.85715"
       sodipodi:cy="368.38019"
       sodipodi:rx="7.1428571"
       sodipodi:ry="7.1428571"
       d="M 140,368.38019 A 7.1428571,7.1428571 0 1 1 125.71429,368.38019 A 7.1428571,7.1428571 0 1 1 140,368.38019 z" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:#ff0000;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path2385"
       sodipodi:cx="132.85715"
       sodipodi:cy="368.38019"
       sodipodi:rx="7.1428571"
       sodipodi:ry="7.1428571"
       d="M 140,368.38019 A 7.1428571,7.1428571 0 1 1 125.71429,368.38019 A 7.1428571,7.1428571 0 1 1 140,368.38019 z"
       transform="translate(178.57142,-69.999991)" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:#ff0000;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path2387"
       sodipodi:cx="132.85715"
       sodipodi:cy="368.38019"
       sodipodi:rx="7.1428571"
       sodipodi:ry="7.1428571"
       d="M 140,368.38019 A 7.1428571,7.1428571 0 1 1 125.71429,368.38019 A 7.1428571,7.1428571 0 1 1 140,368.38019 z"
       transform="translate(352.85714,-132.85713)" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:#ff0000;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path2389"
       sodipodi:cx="132.85715"
       sodipodi:cy="368.38019"
       sodipodi:rx="7.1428571"
       sodipodi:ry="7.1428571"
       d="M 140,368.38019 A 7.1428571,7.1428571 0 1 1 125.71429,368.38019 A 7.1428571,7.1428571 0 1 1 140,368.38019 z"
       transform="translate(247.14285,55.714294)" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:#ff0000;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path2391"
       sodipodi:cx="132.85715"
       sodipodi:cy="368.38019"
       sodipodi:rx="7.1428571"
       sodipodi:ry="7.1428571"
       d="M 140,368.38019 A 7.1428571,7.1428571 0 1 1 125.71429,368.38019 A 7.1428571,7.1428571 0 1 1 140,368.38019 z"
       transform="translate(427.14285,-18.57142)" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1.03311849px;stroke-linecap:butt;stroke-linejoin:miter;marker-end:url(#Arrow2Lend);stroke-opacity:1"
       d="M 138.10653,368.16632 L 306.81601,301.71168"
       id="path2393"
       sodipodi:nodetypes="cc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker-end:url(#Arrow2Lend);stroke-opacity:1"
       d="M 314.53829,305.80099 L 377.19022,418.31875"
       id="path4468"
       sodipodi:nodetypes="cc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker-end:url(#Arrow2Lend);stroke-opacity:1"
       d="M 490.98659,240.59184 L 553.63852,342.88072"
       id="path4470"
       sodipodi:nodetypes="cc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker-end:url(#Arrow2Lend);stroke-opacity:1"
       d="M 388.96776,416.7701 L 553.90857,355.39678"
       id="path4472"
       sodipodi:nodetypes="cc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker-end:url(#Arrow2Lend);stroke-opacity:1"
       d="M 317.36556,296.58067 L 482.30637,235.20735"
       id="path4474"
       sodipodi:nodetypes="cc" />
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="203.29913"
       y="327.26733"
       id="text4496"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4498"
         x="203.29913"
         y="327.26733">a</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="388.69772"
       y="256.94373"
       id="text4500"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4502"
         x="388.69772"
         y="256.94373">b</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="314.53827"
       y="383.52621"
       id="text4504"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4506"
         x="314.53827"
         y="383.52621">c</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="475.64325"
       y="425.72037"
       id="text4508"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4510"
         x="475.64325"
         y="425.72037">d</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="538.29517"
       y="288.909"
       id="text4512"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4514"
         x="538.29517"
         y="288.909">e</tspan></text>
  </g>
</svg>

(arrow go from left to right but are not showing up ...  bother!)

We take $\Sigma = \{ a,b,c,d,e\}$ and note that, starting at the left, $b$ depends on $a$ (written $a\lt b$, since we cannot start action $b$ until action $a$ has been completed. This gives a labelled [[poset]].

 Here the first information to encode in $D$ is the poset structure of dependency

$$\{(a,a),(a,b),(a,c),(a,d),(a,e),(b,b),(b,d), etc.\},$$

then symmetrise this, and take the complement to get 

$$I = \{(b,c),(c,b),(d,e),(e,d),(b,e), (e,b), (c,d),(d,c)\}.$$

Note this encoding does not involve the relationship given by adjacency, and hence ignore if an 'execution sequence' is 'allowable' (i.e., realistic) so $(c,d)$ is in $I$ even though we could not first 'do' $c$ and then 'do' $d$ (unless of course $b$ had already been done).

The language ([[trace language]]) corresponding to the model will be a subset of the [[trace monoid]] of the trace alphabet $(\Sigma, I)$ given here.  It will encode allowable execution sequences  but also will consider the allowable sequences ( _traces_ ) $abcde$, $acbde$, $abdce$, $acebd$ etc. to be identified.

=----
##Reference

*  A Mazurkiewicz, _Trace theory_ in 'Advances in Petri Nets', volume 255 of LNCS, Springer (1987).


[[!redirects trace alphabets]]
[[!redirects Mazurkiewicz trace alphabet]]