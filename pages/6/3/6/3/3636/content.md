+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea of some problems

**Proper homotopy theory** is both an old and a fairly new area of [[algebraic topology]].
It deals with properties of non-[[compact space|compact]] [[topological space]]s, that cannot be detected using maps from [[simplex|simplices]] in these spaces, such as used in the [[fundamental infinity-groupoid|singular complex]]. 

Historically the subject is traced back to Kerekjarto's classification of non-compact surfaces in 1923, but its emergence as an important tool in geometric topology came with [[Larry Siebenmann]]'s work in 1965.

Suppose $M$ is a _smooth_ [[manifold]] with boundary, $\partial M$, then $M\setminus \partial M$ is an open manifold. Now suppose someone gives us an open manifold $N$, is it possible to detect if there is a compact manifold $M$, with $M\setminus \partial \cong N$.  Siebenmann showed that certain conditions on the _ends_ of $N$ were necessary and that there were obstructions if the dimension of $M$ was greater than 5.

Its potential importance of proper homotopy, 
for example for physical applications, comes from the fact that the phenomena it studies include the limiting behaviour of the system.


## Intuitions

The basic hypothesis will be that $X$ will be a [[connected space|connected and locally connected]] compact [[Hausdorff space]]. It will usually be **$\sigma$-compact**, i.e., there will be an increasing sequence, $\{K_n\}$, of compact subspaces with each $K_n$ in the interior of $K_{n+1}$ and such that 

$$X = \bigcup^\infty_{n=0}K_n,$$

These spaces will most often than not be locally finite [[simplicial complex]]es.

We will  be interested in the [[homotopy]] of such spaces 'out towards its ends' 


### Ends

To illustrate the idea of the [[end of a topological space|ends]] of a space $X$, we note that naively $\mathbb{R}$ has two ends, $\infty$ and $-\infty$, whilst $\mathbb{R}^2$ has only one as it is $S^2\setminus \{\infty\}$, (but that is vague!).

More exactly, consider the system of spaces

$$\varepsilon(X) = \{closure(X\setminus K) : K compact \subset X\},$$

This is an inverse system or [[pro-object]] in the category of spaces. Applying the connected component functor, $\pi_0$, to this system of spaces gives $\pi_0(X)$, and, classically, one takes the limit of this to get 

$$e(X) = lim \pi_0\varepsilon(X),$$
the _set of ends_ of $X$. In general, $e(X)$ would be given the [[inverse limit topology]], to preserve more of the information coming from its construction.  This space is the _space of (Freudenthal) ends of $X$_. It is a [[profinite space]].

#### Examples

* Let $X_8$ be the figure eight space, the one-point union of two circles, and let $X$ be its universal cover.  This is an infinite 'thorn bush'. It has infinitely many ends and 
$$e(X) \cong 2^{\aleph_0}.$$

* Let $M$ be a compact manifold and $X = M\setminus \partial M$, then
$e(X) \cong \pi_0(\partial M)$.


### Proper maps

The assignment sending $X$ to $e(X)$ cannot be functorial on the category of spaces and _continuous_ maps, since the contracting map $\mathbb{R}\to \{0\}$ is continuous, $e(\mathbb{R})$ is $\{-\infty, \infty\}$, whilst $e(\{0\})$ is empty since $\{0\}$ is compact.
The problem is that continuity is really about inverse images (inverse image of open is open), but the inverse image mapping does not preserve compactness  (as in the example!).
+-- {: .un_defn}
###### Definition (recall)
A map $f:X\to Y$ is a [[proper map]] if for each subset $K$ compact in $Y$ then $f^{-1}(K)$ is compact in $X$.
=--

### End spaces continued

If $f:X\to Y$ is proper, then it induces a pro-morphism
$$\varepsilon(f) : \varepsilon(X)\to \varepsilon(Y)$$
and hence a _continuous map of the end spaces
$$e(f):e(X)\to e(Y),$$
and $e$ becomes a functor from some category $Proper$ of spaces and proper maps to $Stone$, the category of [[profinite space]]s / [[Stone space]]s.


### Proper homotopy

+-- {: .un_prop}
###### Proposition

For any space $X$, the natural inclusions of $X$ into $X \times I$, $e_i(x) = (x,i)$, $i = 0,1$ together with the projection maps from $X\times I$ to $X$, are proper maps.
=--
+-- {: .un_cor}
###### Corollary
The category $Proper$ has a [[cylinder functor]].
=--

We call the corresponding notion of homotopy, 'proper homotopy'.
We get a 'Proper category' and an associated 'proper homotopy category', which we will denote $Ho(Proper)$. If we are restricting to $\sigma$-compact spaces we may write $Proper_\sigma$, and so on.


### Germs at $\infty$

Although a proper map $f: X\to Y$ will induce a continuous $\varepsilon(f)$, on the end spaces, it is clear that $f$ does not need to be defined on the whole of $X$ for this to work, as $\varepsilon$ encodes behaviour 'out towards $\infty$'.  This leads to the notion of a 'germ at $\infty$'.

Suppose $X$ is locally compact Hausdorff and $A\subset X$. The inclusion $j: A\to X$ is 'cofinal' if the closure of $X\setminus A$ is compact. 
Note that a cofinal inclusion is proper and induces an isomorphism $\varepsilon(A)\cong \varepsilon(X)$.  Let $\Sigma$ be the class of all cofinal inclusions in $Proper$ and let $Proper_\infty = Proper[\Sigma^{-1}]$, the category obtained by formally inverting the cofinal inclusions. 
+--{: .un_defn}
###### Definition
This category is called the _proper category at $\infty$_.
=--
Note that $(Proper,\Sigma)$ admits a [[calculus of fractions|calculus of right fractions]], so any morphism from $X$ to $Y$ in $Proper_\infty$ can be represented by a diagram 
$$X\stackrel{j}{\leftarrow} A \stackrel{f}{\rightarrow}Y,$$
with $j$ a cofinal inclusion, i.e., $f$ is defined on some 'neighbourhood of the end of $X$'.

Two such diagrams 
$$X\stackrel{j^{\prime}}{\leftarrow} A^{\prime} \stackrel{f^\prime}{\rightarrow}Y   and       X\stackrel{j^{\prime\prime}}{\leftarrow} A^{\prime\prime} \stackrel{f^{\prime\prime}}{\rightarrow}Y$$
represent the same germ if $f^\prime | A = f^{\prime\prime}|A$ for some cofinal subspace  $A$ with $A^\prime \cup A^{\prime\prime}\subset A$.


There is also a homotopy category $Ho(Proper_\infty)$

+-- {: .query}
The end space $e(X)$ is a Stone space so is $Max(R)$ for some Boolean algebra $R$ (Stone duality) In the 1960s someone (Goldman?) looked at a ring, $R$, of 'almost continuous functions' from $X$ to $\mathbb{Z}/2\mathbb{Z}$, that gave the right $e(X)$.  Can this idea help integrate better the ideas of proper homotopy etc. with modern methods of algebraic geometry?
=--


## Proper analogues of the fundamental group

The end space behaves a bit like a $\pi_0$ and usually spaces will have many ends, so are not 'connected at infinity'.  If we try to do a fundamental group or groupoid analogue, this means life will get more complicated.  We will try with the assumption of a space having a single end for simplicity!  We will also assume $X$ is $\sigma$-compact.


### First attempt

We could try defining $\pi_1(\varepsilon(X))$ as a progroup, then taking its limit.  For this we would take $\{K_n\}$ an exhausting increasing sequence of compact subsets and setting $U_i = X\setminus K_i$, pick a base point $x_i$ in each $U_i$, and we will get groups $\pi_1(U_i,x_i)$.  We however need induced homomorphisms $\pi_1(U_{i+1},x_{i+1})\to \pi_1(U_i,x_i)$, and for this we have to choose an arc in $U_i$ from $x_{i+1}$ to $x_i$.  We can combine these to get a _base ray_, rather than a _base point_,  that is, we need a proper map, $\alpha : [0,\infty)\to X$.  With that we do get an inverse sequence of groups, but there are problems.  What is the dependence of the inverse system on the choice of $\alpha$?

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="560.23041"
   height="312.2442"
   id="svg2406"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="cylinder.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
  <defs
     id="defs2408">
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 526.18109 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_z="744.09448 : 526.18109 : 1"
       inkscape:persp3d-origin="372.04724 : 350.78739 : 1"
       id="perspective2414" />
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
     inkscape:zoom="1.55625"
     inkscape:cx="762.19162"
     inkscape:cy="154.01741"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="1152"
     inkscape:window-height="701"
     inkscape:window-x="0"
     inkscape:window-y="22" />
  <metadata
     id="metadata2411">
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
     transform="translate(-79.884809,-93.576859)">
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:#cccccc;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path2383"
       sodipodi:cx="168.57143"
       sodipodi:cy="254.09448"
       sodipodi:rx="34.285713"
       sodipodi:ry="61.42857"
       d="M 202.85714,254.09448 A 34.285713,61.42857 0 1 1 134.28571,254.09448 A 34.285713,61.42857 0 1 1 202.85714,254.09448 z"
       transform="translate(-53.900904,89.798016)" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 110.36437,283.20569 C 627.11227,134.40393 627.11227,134.40393 627.11227,134.40393 L 628.46501,133.05119"
       id="path2387" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 121.51454,404.3102 L 639.61519,186.51853"
       id="path2389" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:#ffffff;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path2391"
       sodipodi:cx="168.57143"
       sodipodi:cy="254.09448"
       sodipodi:rx="34.285713"
       sodipodi:ry="61.42857"
       d="M 202.85714,254.09448 A 34.285713,61.42857 0 1 1 134.28571,254.09448 A 34.285713,61.42857 0 1 1 202.85714,254.09448 z"
       transform="matrix(0.8143313,0,0,0.8224064,60.410706,-1.7353843)" />
    <path
       transform="matrix(0.6487302,0,0,0.7455493,188.19371,-6.6397643)"
       d="M 202.85714,254.09448 A 34.285713,61.42857 0 1 1 134.28571,254.09448 A 34.285713,61.42857 0 1 1 202.85714,254.09448 z"
       sodipodi:ry="61.42857"
       sodipodi:rx="34.285713"
       sodipodi:cy="254.09448"
       sodipodi:cx="168.57143"
       id="path3163"
       style="opacity:1;fill:#fffdfe;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       sodipodi:type="arc" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:#fffdfe;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path3165"
       sodipodi:cx="168.57143"
       sodipodi:cy="254.09448"
       sodipodi:rx="34.285713"
       sodipodi:ry="61.42857"
       d="M 202.85714,254.09448 A 34.285713,61.42857 0 1 1 134.28571,254.09448 A 34.285713,61.42857 0 1 1 202.85714,254.09448 z"
       transform="matrix(0.676825,0,0,0.6872657,267.99957,-12.600074)" />
    <path
       transform="matrix(0.614871,0,0,-0.6371152,352.77903,305.95506)"
       d="M 202.85714,254.09448 A 34.285713,61.42857 0 1 1 134.28571,254.09448 A 34.285713,61.42857 0 1 1 202.85714,254.09448 z"
       sodipodi:ry="61.42857"
       sodipodi:rx="34.285713"
       sodipodi:cy="254.09448"
       sodipodi:cx="168.57143"
       id="path3167"
       style="opacity:1;fill:#fffdfe;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       sodipodi:type="arc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1.04990613px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 276.5261,236.44499 C 437.3288,335.40514 437.3288,335.40514 437.3288,335.40514"
       id="path3211"
       sodipodi:nodetypes="cc" />
    <text
       xml:space="preserve"
       style="font-size:16px;font-style:normal;font-variant:normal;font-weight:normal;font-stretch:normal;text-align:start;line-height:125%;writing-mode:lr-tb;text-anchor:start;fill:#000000;fill-opacity:1;stroke:none;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1;font-family:Bitstream Vera Sans;-inkscape-font-specification:Bitstream Vera Sans"
       x="412.48389"
       y="351.69116"
       id="text3215"
       sodipodi:linespacing="125%"><tspan
         sodipodi:role="line"
         id="tspan3217"
         x="412.48389"
         y="351.69116">base ray</tspan></text>
    <path
       transform="matrix(0.5637487,0,0,-0.5562563,430.14511,269.36854)"
       d="M 202.85714,254.09448 A 34.285713,61.42857 0 1 1 134.28571,254.09448 A 34.285713,61.42857 0 1 1 202.85714,254.09448 z"
       sodipodi:ry="61.42857"
       sodipodi:rx="34.285713"
       sodipodi:cy="254.09448"
       sodipodi:cx="168.57143"
       id="path2450"
       style="opacity:1;fill:#fffdfe;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       sodipodi:type="arc" />
  </g>
</svg>

Let $X$ be an infinite cylinder with an infinite string of circles attached via a proper ray $\alpha: [0,\infty) \to X$. 
The space has just one 'end' but you can choose different ways of going from $\pi_1(U_{i+1},x_{i+1})$ to $\pi_1(U_i,x_i)$ for fairly obvious choices of  base points such that the limit groups of the resulting two inverse systems are non-isomorphic! (In the survey listed below, this example is examined in detail, and one of the limits is a free group on one element, the other is trivial! Definitely non-isomorphic!)

This means that $lim \pi_1(\varepsilon(X))$ is not an invariant of the end. This phenomenon is linked to the fact that $\pi_1(\varepsilon(X))$ does not satisfy the [[Mittag-Leffler condition]] for either choice of the base rays.


### Waldhausen boundary

If $X$ and $Y$ are locally compact Hausdorff spaces, there is no obvious candidate for a space of proper maps from $X$ to $Y$, but one can form a simplicial set $\mathbb{P}(X,Y)$ with $\mathbb{P}(X,Y)_n = Proper(X\times \Delta^n,Y)$, which acts as if it was the _singular complex of the mythical space of proper maps from $X$ to $Y$_.
+-- {: .un_defn}
###### Definition
The **Waldhausen boundary** of $X$ is the simplicial set $\mathbb{P}([0,\infty),X)$.
=--
There is an epimorphism from $\pi_0(\mathbb{P}([0,\infty),X))$ to $e(X)$.

*  In the example above of the cylinder with the string of circles attached, $\pi_0(\mathbb{P}([0,\infty),X))$,  is uncountable, and $\pi_1(\mathbb{P}([0,\infty),X))$ maps onto $lim S$.  

*  When $X$ has a single end and  $\pi_0(\varepsilon(X))$ is [[Mittag-Leffler condition|Mittag-Leffler]], then $\pi_0(\mathbb{P}([0,\infty),X))$, is a single point, i.e. all possible base rays are properly homotopic.


### Second attempt

Even if we  did not have the above difficulty with the limit groups, we would still have the problem that, as the limit functor is not exact, the resulting limiting homotopy groups would not be that well behaved.  There would not be  any general long exact sequence results (just as with [[Čech homology]]). There is at least one possible replacement for those limiting homotopy groups, but first we note that it is not appropriate to base any such things at a point, rather we should be using a base ray as was discussed above.

One fairly obvious attempt to define a 'fundamental group' for $X$, based at a proper ray $\alpha: [0,\infty) \to X$, would be to note that $\alpha$ gives $\mathbb{P}([0,\infty),X)$ a base point so we could look at  $\pi_1(\mathbb{P}([0,\infty),X),\alpha)$ and more generally at $\pi_n(\mathbb{P}([0,\infty),X),\alpha)$, and we will denote these groups by $\underline{\underline{\pi}}_n(X,\alpha)$.

There are variants 'at infinity' of both the Waldhausen boundary and these groups, otained using germs instead of proper maps. These will be denoted with a $\infty$ as a super- or suffix on the above notation.


### Brown&#8211;Grossman homotopy groups

(Once over lightly here, more details at [[Brown-Grossman homotopy group]].)
In fact there is another different way of looking at these groups, which has a more geometric feel to it. Historically these groups were not the first successful attempt.  This was due to Ed Brown and uses strings of spheres.  These are examples of [[spherical objects]] and the resulting 'groups' (better thought of as '$\Pi_\mathcal{A}$-[[spherical object and Pi(A)-algebra|algebras]]') have a rich structure.  They are discussed at [[Brown-Grossman homotopy group]]s.  They do link with the above homotopy groups of the Waldhausen boundary, which are called the [[Steenrod homotopy group]]s, (for reasons that will be explained there). 


## References

Survey article:

* [[Tim Porter]], _Proper Homotopy Theory_,  in the _[[Handbook of Algebraic Topology]]_, Ed. I.M.James, Elsevier, 1995, p. 127-167,

Books:

* [[Hans-Joachim Baues|H. J. Baues]] and A. Quintero, _Infinite homotopy theory_, Volume 6 of K-monographs in mathematics,	Springer, 2001

* Bruce Hughes and Andrew Ranicki, _Ends of Complexes_, Cambridge Tracts in Mathematics (No. 123), C.U.P.


Lecture Notes:

*   [[D. A. Edwards]] and [[H. M. Hastings]], _&#268;ech and Steenrod Homotopy Theory with Applications,_ SLNM 542, Springer (1976).


[[!redirects proper homotopy theory]]
[[!redirects Proper Homotopy Theory]]

[[!redirects proper homotopy]]
[[!redirects proper homotopies]]
