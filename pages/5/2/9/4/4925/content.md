
# Colourability
* table of contents
{: toc}

## Idea

The colourability of a knot tells one information about its [[knot group]] yet has a simple, and visually attractive aspect that seems almost to avoid all mention of groups, presentations, etc., except at a fairly naive level.

The easiest form of colourability to examine is $3$-colourability. 


## $3$-colourability

+--{: .un_defn}
###### Definition
A [[knot diagram]] is _$3$-colourable_ if we can assign colours to its arcs such that

1. each arc is assigned one  colour;

1.  _exactly_ three colours are used in the assignment;

1. at each crossing, either all the arcs have the same colour, or arcs of all three colours meet in the crossing.

=--

+--{: .un_example}
###### Examples and non-examples

* The usual diagram for the trefoil knot is $3$-colourable. (Just do it! Each arc is given a separate colour and it works.)

* The [[figure-8 knot]] diagram

  +-- {: style="text align:center"}
  [[!include figure 8 knot - SVG]]
  =--

  is not $3$-colourable. (Try it!)

=--

+--{: .un_theorem}
######Theorem
$3$-colourability is a [[knot  invariant]].

=--

The proof is amusing to work out oneself. You have to show that if a knot diagram $D$ is $3$-colourable and you perform a [[Reidemeister move]] on it then the result is also $3$-colourable. The thing to note is that any arcs that leave the locality of the move must be coloured the same before and after the move is done. 

+--{: .un_note}
###### Notes
*  We can now use phrases such as 'the trefoil knot is $3$-colourable' as its validity does not depend on what diagram is used to represent it, (by the above and by [[Reidemeister moves|Reidemeister's theorem]].) 

* As the trefoil knot is $3$-colourable and the unknot is not, *non-trivial knots exist*.  Moreover, the trefoil is $3$-colourable and the figure $8$ is not, so these are different. We also get that the [[bridge number]] of the trefoil is $2$, as this provides the missing piece of the argument found in that entry.

=--

 There are two comments to make here.  First what does this all mean at a deeper topological level?  The other is : why stop at $3$? What about $n$-colourability? We will handle the second one first.

##$n$-colourability##
 Let $n$ be an integer - in practice $n = 1$ or 2 are not that interesting, so usually $n \geq 3$. Let $\mathbb{Z}_n$ be the additive group of integers modulo $n$. 

+--{: .un_defn}
###### Definition
An _$n$-colouring_ of a knot diagram, $D$, is an assignment to each arc of an element of $\mathbb{Z}_n$ in such a way that, at each crossing, the sum of the values assigned on the underpass arcs is twice that on the overpass, and such that in the assignment at least two elements of $\mathbb{Z}_n$ are used.

=--

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="89.928581"
   height="101.35714"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   version="1.0"
   sodipodi:docname="labelled-crossing.svg"
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
     inkscape:zoom="2.8"
     inkscape:cx="47.132334"
     inkscape:cy="42.148486"
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
     transform="translate(-116.28571,-149.30877)">
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 117.14286,149.80877 C 202.85714,258.3802 205.71429,249.80877 205.71429,249.80877"
       id="path2383" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 116.78571,250.16591 L 156.78571,206.23734"
       id="path2385" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 163.21429,200.8802 L 203.92857,153.02305"
       id="path2387" />
    <text
       xml:space="preserve"
       style="font-size:14px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Times New Roman;-inkscape-font-specification:Times New Roman"
       x="129.64285"
       y="222.66591"
       id="text2389"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan2391"
         x="129.64285"
         y="222.66591">a</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:14px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Times New Roman;-inkscape-font-specification:Times New Roman"
       x="176.42857"
       y="175.52306"
       id="text2393"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan2395"
         x="176.42857"
         y="175.52306">c</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:14px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Times New Roman;-inkscape-font-specification:Times New Roman"
       x="146.42857"
       y="178.73734"
       id="text2397"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan2399"
         x="146.42857"
         y="178.73734">b</tspan></text>
  </g>
</svg>

with $a+c \equiv_n 2b$.


What, of course, needs to be checked (left to 'the reader') is

* this notion is a generalisation of 3-colourability (i.e. coincides in the case of $n = 3$);

* $n$-colourability is preserved under [[Reidemeister moves]] so can be applied to a knot, not just to a knot diagram;

and then to find some examples of, say, 5-colourability. What knots are 5-colourable? Which $(2,k)$-[[torus knots]] are 5-colorable, and so on.  This is not important mathematically, but is quite fun and, in fact, does give insight and experience in working with the Reidemeister moves.

## Coloring by a quandle

There is an even more general notion of coloring a knot $K$ by the elements of a [[quandle]] $(Q,\rhd : Q \times Q \to Q)$.  Formally, a coloring of $K$ by $Q$ corresponds to a quandle homomorphism from the fundamental quandle $Q(K)$ of $K$ to $Q$.  Concretely, this says that at each crossing with arcs labelled $a$, $b$, and $c$ (as in the above diagram), the identity $c = a \rhd b$ must be respected.  In particular, $n$-coloring corresponds to coloring by the set $\mathbb{Z}_n$ equipped with the quandle operation $a \rhd b = 2b - a\,(mod\,n)$, known as the dihedral quandle.

## References

* [[Ralph Fox]], _A quick trip through Knot theory_ [pdf file]( (http://homepages.math.uic.edu/~kauffman/QuickTrip.pdf)

* Wikipedia articles on [tricolorability](http://en.wikipedia.org/wiki/Tricolorability) and [Fox n-coloring](http://en.wikipedia.org/wiki/Fox_n-coloring)

[[!redirects colorable knot]]
[[!redirects colorable knots]]
[[!redirects colourable knot]]
[[!redirects colourable knots]]

[[!redirects colorability]]
[[!redirects colourability]]

[[!redirects coloring knots]]
[[!redirects knot coloring]]
category: knot theory