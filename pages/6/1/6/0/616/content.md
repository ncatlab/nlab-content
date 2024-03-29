
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--




# Contents
* table of contents
{:toc}

##Idea##

Directed Homotopy Theory is a variant of [[homotopy theory]] which aims to study the properties of [[directed spaces]]. 

Much of the impetus for the theory  comes from work on modelling concurrent process. It can also be seen as a way of studying an 'evolving' space. 

The following examples illustrate the sort of problems that arise:



##Example##

The example uses two directed spaces that are slightly different and use a [[pospace]], i.e. a space with a closed partial order.
(Both these use a rectangle with order $(x,y)\leq (x\prime, y\prime)$ if and only if $|y\prime - y| \leq x\prime - x$, so the [[future cone]] of any point is a cone symmetric about a horizontal line through the point and with edges at $\pm 45$ degrees to that line.)

The two spaces are

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="354.90808"
   height="150.71417"
   id="svg3965"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="stream1.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
  <defs
     id="defs3967">
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 372.04724 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_z="1052.3622 : 372.04724 : 1"
       inkscape:persp3d-origin="526.18109 : 248.03149 : 1"
       id="perspective3974" />
  </defs>
  <sodipodi:namedview
     inkscape:document-units="mm"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     inkscape:pageopacity="0.0"
     inkscape:pageshadow="2"
     inkscape:zoom="6.9465337"
     inkscape:cx="108.93402"
     inkscape:cy="551.24942"
     inkscape:current-layer="layer1"
     id="namedview3969"
     showgrid="true"
     inkscape:window-width="663"
     inkscape:window-height="701"
     inkscape:window-x="193"
     inkscape:window-y="22">
    <inkscape:grid
       type="xygrid"
       id="grid4498"
       visible="true"
       enabled="true" />
  </sodipodi:namedview>
  <metadata
     id="metadata3971">
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
     transform="translate(-104.18767,-134.37018)">
    <rect
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:1.00695038;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       id="rect3976"
       width="315.54532"
       height="149.70721"
       x="120.92747"
       y="134.87366" />
    <rect
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:0.99921262;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       id="rect4500"
       width="32.280476"
       height="16.248646"
       x="187.71953"
       y="187.84584" />
    <rect
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:0.99921262;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       id="rect4502"
       width="79.464096"
       height="20.729763"
       x="233.78566"
       y="224.69875" />
    <path
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:0.99921262;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       d="M 436.2716,214.16797 C 436.2716,214.16797 296.6058,165.47445 231.57667,169.06112 C 198.23447,170.9001 121.43957,214.59261 121.43957,214.59261 C 121.43957,214.59261 250.50206,269.68742 299.52423,268.10333 C 348.5464,266.51924 436.2746,214.16797 436.2746,214.16797"
       id="path4546"
       sodipodi:nodetypes="csczc" />
    <path
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:0.99921262;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       d="M 121.24621,214.62091 C 121.24621,214.62091 166.92495,222.84942 190.98935,223.73593 C 235.02174,225.35804 300.14065,205.00314 335.15561,201.3008 C 370.17057,197.59846 389.15756,187.14562 436.23367,214.54781"
       sodipodi:nodetypes="cszs"
       id="path4642" />
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="441.18854"
       y="219.73613"
       id="text4557"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4559"
         x="441.18854"
         y="219.73613">p'</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="102.18962"
       y="220.64066"
       id="text4650"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4652"
         x="102.18962"
         y="220.64066">p</tspan></text>
  </g>
</svg>

 and 

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="356.50772"
   height="150.71417"
   id="svg3965"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="stream2.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
  <defs
     id="defs3967">
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 372.04724 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_z="1052.3622 : 372.04724 : 1"
       inkscape:persp3d-origin="526.18109 : 248.03149 : 1"
       id="perspective3974" />
  </defs>
  <sodipodi:namedview
     inkscape:document-units="mm"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     inkscape:pageopacity="0.0"
     inkscape:pageshadow="2"
     inkscape:zoom="1.4142136"
     inkscape:cx="109.51908"
     inkscape:cy="126.16914"
     inkscape:current-layer="layer1"
     id="namedview3969"
     showgrid="true"
     inkscape:window-width="663"
     inkscape:window-height="701"
     inkscape:window-x="68"
     inkscape:window-y="22"
     showguides="true"
     inkscape:guide-bbox="true">
    <inkscape:grid
       type="xygrid"
       id="grid4498"
       visible="true"
       enabled="true" />
    <sodipodi:guide
       orientation="1,0"
       position="26.162951,267.99347"
       id="guide4646" />
  </sodipodi:namedview>
  <metadata
     id="metadata3971">
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
     transform="translate(-106.23382,-134.37018)">
    <rect
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:1.00695038;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       id="rect3976"
       width="315.54532"
       height="149.70721"
       x="120.92747"
       y="134.87366" />
    <rect
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:0.99921262;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       id="rect4500"
       width="32.280476"
       height="16.248646"
       x="187.71953"
       y="187.84584" />
    <rect
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:0.94120514;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       id="rect4502"
       width="70.308876"
       height="20.787771"
       x="289.03604"
       y="215.45651" />
    <path
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:0.99921262;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       d="M 436.27309,204.51588 C 436.27309,204.51588 364.16987,261.49359 323.61464,256.94504 C 280.78609,252.14152 250.8776,179.28556 208.44929,171.72269 C 180.78105,166.79081 121.12721,204.09448 121.12721,204.09448 C 121.12721,204.09448 171.7167,233.20797 195.7811,234.09448 C 239.81349,235.71659 336.28282,191.30079 336.28282,191.30079 C 336.28282,191.30079 404.30024,157.22823 436.54654,204.44602"
       sodipodi:nodetypes="csscscs" />
    <path
       style="fill:none;fill-opacity:0.52999998;stroke:#000000;stroke-width:0.99921262;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       d="M 436.41281,204.09448 C 436.41281,204.09448 297.66314,154.892 232.63401,158.47867 C 199.29181,160.31765 121.05734,204.29807 121.05734,204.29807 C 121.05734,204.29807 251.5594,259.10496 300.58157,257.52087 C 349.60374,255.93678 436.31401,204.09448 436.31401,204.09448"
       id="path4546"
       sodipodi:nodetypes="csczc" />
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="104.23577"
       y="-202.34459"
       id="text4552"
       sodipodi:linespacing="125%"
       transform="scale(1,-1)"><tspan
         sodipodi:role="line"
         id="tspan4554"
         x="104.23577"
         y="-202.34459">b</tspan></text>
    <text
       xml:space="preserve"
       style="font-size:22px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="444.83432"
       y="214.36501"
       id="text4557"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan4559"
         x="444.83432"
         y="214.36501">p'</tspan></text>
  </g>
</svg>


In both the space is the rectangle with two smaller rectangles removed.  The position of the upper left small rectangle is the same in both, but that of the righthand lower rectangle is shifted slightly to the right in the second picture.  The directed homotopy classes of d-paths from $p$ to $p^\prime$ in the two cases are different. The crucial point is that in the second there is such a class that was impossible in the first example, yet the spaces are homeomorphic, so classically would be 'the same'. The subtlety is in the order.
 

### Problem

The first problem is to find a small model of such structures.  The [[fundamental category]] would be a model, but unlike with the [[fundamental groupoid]] in the non-directed case, it is not sufficient to take a 'base point' in each connected component.  That would ignore the order.

## Related concepts
 {#RelatedConcepts}

* [[directed homotopy type theory]]

* [[models for concurrency]];

* [[topological data analysis]] and [[persistent homology]];

* Models for mixed temporal-spatial [[modal logics]];

* [[causal sets]], discrete models for space time and [[causal models]] in Computer Science, Physics and Systems Biology;

* models for multi-agent systems, [[multimodal logics]]



## References

(See also under [[directed space]].)

Foundational work was done by [[Eric Goubault]] and his collaborators.

* [[Eric Goubault]], [[Some geometric perspectives in concurrency theory]].

Categorical aspects are looked at in

* [[Lisbeth Fajstrup]] and [[Jiří Rosický]], *A convenient category for directed homotopy*, TAC 21 no. 1, [online](http://www.tac.mta.ca/tac/volumes/21/1/21-01abs.html)

For more on this see also at _[[Delta-generated space]]_.

Applications to computer science are presented in

* [[Lisbeth Fajstrup]], [[Eric Goubault]], [[Emmanuel Haucourt]], [[Samuel Mimram]], [[Martin Raussen]], [[Directed Algebraic Topology and Concurrency]]

The fundamental category of a pospace is discussed in

* [[Lisbeth Fajstrup]], [[Eric Goubault]], [[Emmanuel Haucourt]], and  [[Martin Raussen]], Components of the fundamental category. Appl.Cat. Struct. Vol. 12, pp.81-108, 2004

and the possibility of an analogue of covering spaces in

* [[Lisbeth Fajstrup]],  Dicovering spaces. Algebraic topological methods in computer science (Stanford, CA, 2001). Homology Homotopy Appl. 5 (2003), no. 2, 1-17 
([HHA](http://www.intlpress.com/HHA/v5/n2/))


[[Philippe Gaucher]] ([[PPS]], Paris) has introduced an interesting related model, namely that of 'flows'.  These are, approximately, topological categories without identity arrows.  They are intended as another model of processes. One of his papers on this idea is at [Arxiv](http://arxiv.org/abs/math/0308054v1), published as 

*  [[Philippe Gaucher]], A model category for the homotopy theory of concurrency, Homology Homotopy and Applications, vol. 5 (1):p.549-599, 2003.



Marco Grandis' work on the area is listed amongst his publications at his ([homepage](http://www.dima.unige.it/~grandis/rec.public_grandis.html)). Such as 

* [[Marco Grandis]], Directed homotopy theory. I, Cah. Topol. G eom. Di  er. Cat eg. 44 (4) (2003) 281&#8211;316.

* [[Marco Grandis]], Directed homotopy theory. II. Homotopy constructs, Theory Appl. Categ. 10 (2002) No. 14, 369&#8211;391 (electronic).

* [[Marco Grandis]], The shape of a category up to directed homotopy, Theory Appl. Categ. 15 (2005/06) No. 4, 95&#8211;146 (electronic).

* [[Marco Grandis]], Modelling fundamental 2-categories for directed homotopy, Homology, Homotopy Appl. 8 (1) (2006) 31&#8211;70 (electronic)


* [[Marco Grandis]], _[[Directed Algebraic Topology]], Models of non-reversible worlds_ , Cambridge University Press, 2009.


 A websearch will find others.

Another approach to model category structures in this area is by Kahl, who uses a Baues type fibration category approach.

*  Thomas Kahl, Relative directed homotopy theory of partially ordered spaces,
Journal of Homotopy and Related Structures, Vol. 1(2006), No. 1, pp. 79-100,([JHRS](http://jhrs.rmi.acnet.ge/volumes/2006/n1a4/ )).

[[Krzysztof Worytkiewicz]] and [[Peter Bubenik]] have given a model category structure for local pospaces:

*  P. Bubenik and [[K. Worytkiewicz]], A model category structure for local po-spaces, Homology, Homotopy and Applications, Vol. 8 (2006), No. 1, pp.263-292. ([HHA](http://intlpress.com/HHA/v8/n1/a10/)).


Further related references are

* [[L. Fajstrup]], Loops, ditopology and deadlocks, Math. Structures Comput. Sci. 10 (4) (2000) 459&#8211;480, geometry and concurrency.

* [[L. Fajstrup]], [[M. Raussen]],  [[E. Goubault]], [[E. Haucourt]], Components of the fundamental category, Appl. Categ. Structures 12 (1) (2004) 81&#8211;108, homotopy
theory.

* [[L. Fajstrup]], Dihomotopy classes of dipaths in the geometric realization of a cubical set: from discrete to continuous and back again, in: R. Kopperman, M. B. Smyth, D. Spreen, J. Webster (Eds.), _Spatial Representation: Discrete vs. Continuous Computational Models_, no. 04351 in Dagstuhl Seminar Proceedings, IBFI, Schloss Dagstuhl, Germany, 2005.

* [[L. Fajstrup]], Dipaths and dihomotopies in a cubical complex, Adv. in Appl.
Math. 35 (2) (2005) 188&#8211;206.

* [[M. Raussen]], Deadlocks and dihomotopy in mutual exclusion models, in: R. Kopperman, M. B. Smyth, D. Spreen, J. Webster (Eds.), _Spatial
Representation: Discrete vs. Continuous Computational Models, no. 04351 in
Dagstuhl Seminar Proceedings_, IBFI, Schloss Dagstuhl, Germany, 2005.

* U. Fahrenberg, [[M. Raussen]], Reparametrizations of continuous paths, available
as [preprint R-2006-22](http://www.math.aau.dk/research/reports/2006.htm)  (2006).


* [[E. Goubault]], [[E. Haucourt]], Directed algebraic topology and concurrency, ([web](http://iml.univ-mrs.fr/lafont/Geocal/goubault2.pdf))
(2006).23

* [[E. Goubault]], [[Emmanuel Haucourt|E. Haucourt]], Components of the fundamental category, II,
technical reports, CEA, Saclay (2006).

* [[M. Raussen]], Invariants of directed spaces, available as preprint R-2006-28 ([web](http://bib.mathematics.dk/preprint.php?id=DMF-2006-08-002 ))(2006).



[[!redirects directed algebraic topology]]