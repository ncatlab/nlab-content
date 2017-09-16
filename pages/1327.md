#Idea#


The _associahedra_ or _Stasheff polytopes_ $\{K_n\}$ are [[topological space]]s that naturally arrange themselves into an topological [[operad]] that resolves the standard associative operad: an [[A-infinity-operad]]. 

The vertices of $K_n$ correspond to ways in which one can bracket a product of $n$ variables. The edges correspond to rebracketings, the faces relate different sequences of rebracketings that lead to the same result, and so on.

The associahedra were introduced by Jim Stasheff in order to describe [[topological space]]s equipped with a multiplication operation that is associative up to every higher coherent homotopy. 

#Definition#

Here is the rough idea, copied, for the moment, verbatim from Markl94 [p. 26] (http://arxiv.org/PS_cache/hep-th/pdf/9411/9411208v1.pdf#page=26) (for more details see references below):

For $n \geq 2$ the **associahedron** $K_n$ is an $(n-2)$-dimensional polyhedron whose $i$-dimensional cells are, for $0 \leq i \leq n-2$, indexed by all (meaningful) insertions of $(n-i-2)$ pairs of brackets between $n$ independent indeterminants, with suitably defined incidence maps.

#Illustrations#

* **$K_4$** The fourth associahedron $K_4$ is the pentagon which expresses the different ways a product of four elements may be bracketed


+--{: style="text-align:center"}
<svg xmlns="http://www.w3.org/2000/svg" width="30em" height="20em" viewBox="0 0 480 320">
 <desc>Pentagon Identity</desc>
 <defs>
  <marker id="svg295arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
 </defs>
 <g font-size="16" markdown="1">
  <foreignObject x="180"  y="0" width="120" height="20">$(w\otimes x)\otimes(y\otimes z)$</foreignObject>
  <foreignObject x="0"  y="120" width="120" height="20">$((w\otimes x)\otimes y)\otimes z$</foreignObject>
  <foreignObject x="360"  y="120" width="120" height="20">$w\otimes (x\otimes(y\otimes z))$</foreignObject>
  <foreignObject x="60"  y="300" width="120" height="20">$(w\otimes (x\otimes y))\otimes z$</foreignObject>
  <foreignObject x="320"  y="300" width="120" height="20">$w\otimes ((x\otimes y)\otimes z)$</foreignObject>
  <foreignObject x="80"  y="50" width="60" height="24">$a_{w\otimes x,y,z}$</foreignObject>
  <foreignObject x="350"  y="50" width="60" height="24">$a_{w,x,y\otimes z}$</foreignObject>
  <foreignObject x="10"  y="210" width="70" height="24">$a_{w,x,y}\otimes 1_{z}$</foreignObject>
  <foreignObject x="410"  y="210" width="70" height="24">$1_w\otimes a_{x,y,z}$</foreignObject>
  <foreignObject x="215"  y="290" width="60" height="24">$ a_{w,x\otimes y,z}$</foreignObject>
 </g>
 <g fill="none" stroke="#000" stroke-width="1.5" marker-end="url(#svg295arrowhead)">
   <line x1="70" y1="120" x2="230" y2="25"/>
   <line x1="250" y1="25" x2="410" y2="120"/>
   <line x1="60" y1="140" x2="110" y2="300"/>
   <line x1="370" y1="300" x2="420" y2="150"/>
   <line x1="180" y1="315" x2="310" y2="315"/>
 </g>
</svg>
=--  

One can also think of this as the top-level structure of the 4th [[oriental]]. This controls in particular the _pentagon identity_ in the definition of [[monoidal category]], as dicussed there.

* **$K_5$** is the [dual polyhedron](http://en.wikipedia.org/wiki/Dual_polyhedron) to the [triaugmented triangular prism](http://en.wikipedia.org/wiki/Triaugmented_triangular_prism) 

+--{: style="text-align:center"}
<img src="http://upload.wikimedia.org/wikipedia/commons/thumb/c/c6/Polytope_K3.svg/180px-Polytope_K3.svg.png" alt="">
=--

  A template which can be cut out and assembled into a $K_5$ can be found [here](http://cheng.staff.shef.ac.uk/cutout/).

* Rotatable illustrations of some Stasheff polyhedra can be found at 

  * [Les polytopes de Stasheff](http://math.univ-lyon1.fr/~chapoton/stasheff.html)

  * This is part of a larger website [Petites pages sur divers sujets](http://math.univ-lyon1.fr/~chapoton/petitespages.html) which contains illusrations of other polyedra, too.




#References#

The original article that defines associahedra and in which the operad $K$ that gives $A(\infty)$-topological spaces is implicit is

* Stasheff, _Homotopy associative H-spaces I_, _II_, Trans. Amerk. Math. Soc. 108 (1963), 275-312

A textbook discussion (slightly modified) is in section 1.6 of the book

* Martin Markl, Steve Shnider, Jim Stasheff, _Operads in Algebra, Topology and Physics_ ([web](http://books.google.de/books?id=fMhZjT9lQo0C&pg=PA56&lpg=PA56&dq=Stasheff+associahedra&source=bl&ots=ZuGXjT4zbp&sig=V-taGG2LHS0msHK-PTxmUXXCvEY&hl=de#PPP1,M1))

