I'll try to work out some stuff here. If anything becomes interesting in the slightest, I hope to add a new page to the nLab collection. Any editorial angels who wish to help add, correct, comment, etc, please feel free.

My ultimate goal is to follow what others at the nLab are doing and reformulate it in a way I can understand (which usually means that I need to "discretize" everything). In particular, I would like to one day understand [[space and quantity]] and be able to understand how

$$discrete space \Longleftrightarrow discrete differential forms$$

works (if it does).

Clues:

* ["arrow theory"](http://golem.ph.utexas.edu/category/2007/05/the_first_edge_of_the_cube.html#c009337)

* [Wedge Product](http://golem.ph.utexas.edu/category/2007/09/arrowtheoretic_differential_th_3.html#c020832)

* [Arrow Fields](http://golem.ph.utexas.edu/category/2007/02/isham_on_quantization.html)

* [Arrow Category](http://unapologetic.wordpress.com/2007/05/23/arrow-categories/)

$$
\array{\arrayopts{\rowalign{center}}
O(\Delta^0) = & \{ 0\} \\
O(\Delta^1) = & \left\{ 0 \to 1\right\} \\
O(\Delta^2) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="6em" height="4em" viewBox="0 0 60 40">
 <defs>
  <marker id="svg295arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
  <marker id="svg296arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="4" markerHeight="2.5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
 </defs>
 <g font-size="10">
  <foreignObject x="25" y="-2" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
  <foreignObject x="0" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
  <foreignObject x="50" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
 </g>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M10,30 23, 15"/>
   <path d="M35,12 48, 27"/>
   <path d="M15,37 45, 37"/>
  </g>
  <g>
   <path stroke-width="3" d="M30,15 30,27" marker-end="url(#svg296arrowhead)"/>
   <path stroke="#FFF" d="M30,15 30,27"/>
  </g>
 </g>
</svg>
\end{svg}}
\right\}\\
O(\Delta^3) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="13em" height="5em" viewBox="0 0 130 50">
 <defs>
  <g id="myRect256">
   <g font-size="10">
    <foreignObject x="0" y="-3" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
    <foreignObject x="0" y="37" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
    <foreignObject x="40" y="-3" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
    <foreignObject x="40" y="37" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>3</mi></math></foreignObject>
   </g>
   <g fill="none" stroke="#000">
    <g marker-end="url(#svg295arrowhead)">
     <path d="M10,7 37, 7"/>
     <path d="M6,42 6, 17"/>
     <path d="M10,47 37, 47"/>
     <path d="M46,12 46, 37"/>
    </g>
   </g>
  </g>
 </defs>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myRect256" x="0" y="0"/>
 <g fill="none" stroke="#000">
  <path d="M11,43 38, 15" marker-end="url(#svg295arrowhead)"/>
  <g stroke-width="3" marker-end="url(#svg296arrowhead)">
   <path d="M12,12 20,20"/>
   <path d="M40,18 27,40"/>
  </g>
  <g stroke="#FFF">
   <path d="M12,12 20,20"/>
   <path d="M40,18 27,40"/>
  </g>
 </g>
 <g fill="none" stroke="#000">
   <path stroke-width="5" d="M55,25 72,25"/>
   <path stroke-width="3" stroke="#FFF" d="M55,25 72,25" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="1" d="M55,25 72,25"/>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myRect256" x="80" y="0"/>
 <g fill="none" stroke="#000">
  <path d="M92,12 118, 39" marker-end="url(#svg295arrowhead)"/>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M92,20 100,38"/>
    <path d="M120,12 113,19"/>
   </g>
   <g stroke="#FFF">
    <path d="M92,20 100,38"/>
    <path d="M120,12 113,19"/>
   </g>
  </g>
 </g>
</svg>
\end{svg}}\right\}\\
O(\Delta^4) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="28em" height="23em" viewBox="-35 0 245 230">
 <defs>
  <g id="myPent256">
   <g font-size="10">
    <foreignObject x="25" y="-2" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
    <foreignObject x="0" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
    <foreignObject x="50" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>3</mi></math></foreignObject>
    <foreignObject x="13" y="57" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
    <foreignObject x="38" y="57" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>4</mi></math></foreignObject>
   </g>
   <g fill="none" stroke="#000" marker-end="url(#svg295arrowhead)">
    <path d="M8,32 25,13"/>
    <path d="M35,10 52,28"/>
    <path d="M54,41 48,57"/>
    <path d="M24,67 36,67"/>
    <path d="M16,62 8,45"/>
   </g>
  </g>
 </defs>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="0" y="0"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M10,36 45,36"/>
   <path d="M22,60 47,41"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M31,12 31,26"/>
    <path d="M12,38 25,48"/>
    <path d="M45,48 35,60"/>
   </g>
   <g stroke="#FFF">
    <path d="M31,12 31,26"/>
    <path d="M12,38 25,48"/>
    <path d="M45,48 35,60"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="110" y="0"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M120,36 155,36"/>
   <path d="M122,41 147,60"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M141,12 141,26"/>
    <path d="M125,47 135,58"/>
    <path d="M162,38 145,48"/>
   </g>
   <g stroke="#FFF">
    <path d="M141,12 141,26"/>
    <path d="M125,47 135,58"/>
    <path d="M162,38 145,48"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="160" y="80"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M172,119 195,140"/>
   <path d="M194,98 201,138"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M175,127 185,138"/>
    <path d="M212,116 206,116"/>
    <path d="M189,98 184,121"/>
   </g>
   <g stroke="#FFF">
    <path d="M175,127 185,138"/>
    <path d="M212,116 206,116"/>
    <path d="M189,98 184,121"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="55" y="160"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M74,220 83,180"/>
   <path d="M87,178 96,218"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M86,187 86,216"/>
    <path d="M63,196 71,196"/>
    <path d="M107,196 99,196"/>
   </g>
   <g stroke="#FFF">
    <path d="M86,187 86,216"/>
    <path d="M63,196 71,196"/>
    <path d="M107,196 99,196"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="-50" y="80"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M-31,140 -22,100"/>
   <path d="M-29,143 -3,120"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M-40,116 -35,116"/>
    <path d="M-17,97 -17,123"/>
    <path d="M-5,128 -15,140"/>
   </g>
   <g stroke="#FFF">
    <path d="M-40,116 -35,116"/>
    <path d="M-17,97 -17,123"/>
    <path d="M-5,128 -15,140"/>
   </g>
  </g>
 </g>
 <g fill="none" stroke="#000">
  <g stroke-width="5">
   <path d="M60,35 100,35"/>
   <path d="M158,75 168,90"/>
   <path d="M118,190 168,155"/>
   <path d="M3,150 43,185"/>
   <path d="M-3,95 11,79"/>
  </g>
  <g stroke-width="3" stroke="#FFF" marker-end="url(#svg296arrowhead)">
    <path d="M158,75 168,90"/>
    <path d="M60,35 100,35"/>
    <path d="M118,190 168,155"/>
    <path d="M3,150 43,185"/>
    <path d="M-3,95 11,79"/>
  </g>
  <g stroke-width="1">
   <path d="M60,35 100,35"/>
   <path d="M158,75 168,90"/>
   <path d="M118,190 168,155"/>
   <path d="M3,150 43,185"/>
   <path d="M-3,95 11,79"/>
  </g>
 </g>
 <g fill="none" stroke="#000">
   <path stroke-width="7" d="M85,43 85,140"/>
   <path stroke-width="5" stroke="#FFF" d="M85,43 85,140" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="3" d="M85,43 85,140"/>
   <path stroke-width="1" stroke="#FFF" d="M85,43 85,140"/>
 </g>
</svg>
\end{svg}}
\right\}
}
$$


$$\begin{svg}

<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<!-- Created with Inkscape (http://www.inkscape.org/) -->
<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="744.09448819"
   height="1052.3622047"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="drawing.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape">
  <defs
     id="defs4">
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 526.18109 : 1"
       inkscape:vp_y="6.1230318e-14 : 1000 : 0"
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
     inkscape:zoom="0.35"
     inkscape:cx="375"
     inkscape:cy="566.73076"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="1920"
     inkscape:window-height="1180"
     inkscape:window-x="-8"
     inkscape:window-y="-8" />
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
     id="layer1">
    <g
       sodipodi:type="inkscape:box3d"
       style="fill:none;fill-rule:evenodd;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:round;stroke-opacity:1"
       id="g2383"
       inkscape:perspectiveID="#perspective10"
       inkscape:corner0="0.69112381 : 0.74475459 : 0 : 1"
       inkscape:corner7="0.15235871 : 0.61604454 : 0.25 : 1">
      <path
         sodipodi:type="inkscape:box3dside"
         id="path2395"
         style="fill:#e9e9ff;fill-rule:evenodd;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:round;stroke-opacity:1"
         inkscape:box3dsidetype="11"
         d="M 287.49885,232.86601 L 397.95158,120.17877 L 397.95158,211.95989 L 287.49885,299.17299 L 287.49885,232.86601 z" />
      <path
         sodipodi:type="inkscape:box3dside"
         id="path2385"
         style="fill:#353564;fill-rule:evenodd;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:round;stroke-opacity:1"
         inkscape:box3dsidetype="6"
         d="M 220,189.50504 L 220,265.61422 L 287.49885,299.17299 L 287.49885,232.86601 L 220,189.50504 z" />
      <path
         sodipodi:type="inkscape:box3dside"
         id="path2387"
         style="fill:#4d4d9f;fill-rule:evenodd;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:round;stroke-opacity:1"
         inkscape:box3dsidetype="5"
         d="M 220,189.50504 L 322.85714,32.098057 L 397.95158,120.17877 L 287.49885,232.86601 L 220,189.50504 z" />
      <path
         sodipodi:type="inkscape:box3dside"
         id="path2393"
         style="fill:#afafde;fill-rule:evenodd;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:round;stroke-opacity:1"
         inkscape:box3dsidetype="13"
         d="M 220,265.61422 L 322.85714,143.79075 L 397.95158,211.95989 L 287.49885,299.17299 L 220,265.61422 z" />
      <path
         sodipodi:type="inkscape:box3dside"
         id="path2391"
         style="fill:#d7d7ff;fill-rule:evenodd;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:round;stroke-opacity:1"
         inkscape:box3dsidetype="14"
         d="M 322.85714,32.098057 L 322.85714,143.79075 L 397.95158,211.95989 L 397.95158,120.17877 L 322.85714,32.098057 z" />
      <path
         sodipodi:type="inkscape:box3dside"
         id="path2389"
         style="fill:#8686bf;fill-rule:evenodd;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:round;stroke-opacity:1"
         inkscape:box3dsidetype="3"
         d="M 220,189.50504 L 322.85714,32.098057 L 322.85714,143.79075 L 220,265.61422 L 220,189.50504 z" />
    </g>
  </g>
</svg>


\end{svg}$$

**Warning: Under Construction**

##Discrete Smooth Spaces

My current motivation is to try to discretize the definition of a Frolicher space (from [Andrew Stacey's paper](http://arxiv.org/abs/0802.2225)).

***

###Definition (Frolicher) 

A Frolicher space is a triple $(X,C,F)$ where $X$ is a set, $C$ is a family of curves in $X$, i.e. a subset of $Map(R,X)$, and $F$ is a
family of functionals on $X$, i.e. a subset of $Map(X,R)$. 


The sets $C$ and $F$ have to satisfy the following compatibility condition: a curve $c: R\to X$ is in $C$ if and only if $fc\in C^\infty(R,R)$ for all functionals $f\in F$, and similarly a functional $f: X\to R$ is in
$F$ if and only if $fc\in C^\infty(R,R)$ for all curves $c: R\to X$.

***

I guess the first place to start is to define what I mean by a discrete space.

***

###Definition (Discrete Space)

Given a [[directed graph]] $G$, a discrete space is the [[DGA|graded differential algebra]] (DGA) 

$$\Omega(G) = \bigoplus_{r\ge 0} \Omega^r(G)$$

generated by $G$.

The space $\Omega^0(G)$ is spanned by the complete set of vertex projections

$$\{\pi_v:G_0\to G_0|v\in G_0\}$$

satisfying

\[\sum_{v\in G_0} \pi_v = 1.\]

The commutative product on $\Omega^0(G)$ is given simply by composition

\[\pi_v \pi_{v'} = \delta_{v,v'} \pi_v.\]

The space $\Omega^1(G)$ is spanned by elements 

$$\{\pi_e | e\in G_1\}$$

with right multiplication $\Omega^1(G)\times\Omega^0(G)\to\Omega^1(G)$ given by

\[\pi_e\pi_v = \delta_{t(e),v} \pi_e\]

and left multiplication $\Omega^0(G)\times\Omega^1(G)\to\Omega^1(G)$ given by

\[\pi_v\pi_e = \delta_{v,s(e)} \pi_e.\]

###Generating a Discrete Space

The derivation

$$d: \Omega^0(G)\to \Omega^1(G)$$

applied to vertex projections results in,

\[\sum_{v\in G_0} d\pi_v = 0\]

and

\[d(\pi_v \pi_{v'}) = (d \pi_v) \pi_{v'} + \pi_v (d \pi_{v'}) = \delta_{v,v'} d\pi_v,\]

which, in particular, provides the graded commutative relation

\[[\pi_v,d\pi_v] = d\pi_v.\]

Since $\{\pi_e|e\in G_1\}$ spans $\Omega^1(G)$, it follows that 

\[
\begin{aligned}
d\pi_v &= \sum_{e\in G_1} \alpha_e \pi_e, \alpha_e\in R \\
&= \sum_{e\in t^{-1}(v)} \alpha^{(t)}_e \pi_e + \sum_{e\in s^{-1}(v)} \alpha^{(s)}_e \pi_e\quad\text{from (3),(4), and (7),}
\end{aligned}
\]

which says $d\pi_v$ is a weighted sum of edges directed into $v$ and edges directed out of $v$.

Multiplying (6) by $\pi_v$ on the left and $\pi_{v'}$ on the right, results in

\[\pi_v (d\pi_{v'}) \pi_{v'} = (\delta_{v,v'} - 1) \pi_v (d\pi_v) \pi_{v'}\]

####Case: $v = v'$####

When $v = v'$, combining (8) and (9) gives

\[
\pi_v (d\pi_v) \pi_v 
= \sum_{e\in s^{-1}(v)\cap t^{-1}(v)} (\alpha^{(t)}_e + \alpha^{(s)}_e) \pi_e
= 0,\]

which implies that for loops

$$\alpha^{(s)}_e = -\alpha^{(t)}_e.$$

####Case: $v \ne v'$####

When $v \ne v'$, (8) gives

\[
\pi_v (d\pi_v) \pi_{v'} 
= \sum_{e\in s^{-1}(v)\cap t^{-1}(v')} \alpha^{(s)}_e \pi_e
\]

and

\[
\pi_v (d\pi_{v'}) \pi_{v'} 
= \sum_{e\in s^{-1}(v)\cap t^{-1}(v')} \alpha^{(t)}_e \pi_e
\]

which, when combined with (9), implies that

$$\alpha^{(s)}_e = -\alpha^{(t)}_e.$$

Therefore, (8) may be rewritten, in general, as 

\[
d\pi_v 
= \sum_{e\in t^{-1}(v)} \alpha_e \pi_e - \sum_{e\in s^{-1}(v)} \alpha_e \pi_e.
\]

and (12) may be rewritten as

\[
\pi_v (d\pi_{v'}) \pi_{v'} 
= \sum_{e\in s^{-1}(v)\cap t^{-1}(v')} \alpha_e \pi_e.
\]
+--{.query}

Question: This looks suspiciously like it could be related to a discrete Feynman integral to me, i.e. a weighted sum of paths connecting vertex $v$ and $v'$. Could it be that $\alpha_e$ is related to the Leinster measure?

=--

***

+--{.query}
Note: I just found that what I am trying to outline here is very closely related to this paper: [C* Algebras of Infinite Graphs](http://www.ams.org/proc/2000-128-08/S0002-9939-99-05378-2/S0002-9939-99-05378-2.pdf)
=--

+--{.query}
Note: The plot thickens. Reference tracking opened a floodgate. I'm trying to track down [Graphs, groupoids and Cuntz-Krieger algebras](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.38.93), but in the meantime came across [Fundamental groupoids of k-graphs](http://www.emis.de/journals/NYJM/j/2004/10-12.pdf). A $k$-graph seems to be a lot like a diamond complex.
=--

+--{.query}
Note: This looks like a very interesting and readable thesis: [$C^*$-algebras associated to higher-rank graphs](http://www.newcastle.edu.au/service/library/adt/uploads/approved/adt-NNCU20060327.122628/public/02whole.pdf)
=--

***

###Research Papers

[Discrete differential geometry on causal graphs](http://arxiv.org/abs/math-ph/0407005), with
Urs Schreiber (2004).

category: people