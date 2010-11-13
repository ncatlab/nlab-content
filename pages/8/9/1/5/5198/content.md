+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--
#Contents#
* automatic table of contents goes here
{:toc}

## Idea: use a string of spheres not just one!

Within the context of [[proper homotopy theory]], what might be the analogues of the classical homotopy groups?  We might hope that &#268;ech style homotopy groups would work, but they don't, or rather, 'not exactly'!

Given a locally compact and $\sigma$-compact space $X$, and with a base ray $* : [0,\infty) \to X$, with end $\varepsilon(X)$, the &#268;ech homotopy groups of $\varepsilon(X)$ relative to $*$ are defined by $lim \pi_n(\varepsilon(X))$.  These 'make sense' but do not behave well, since the limit will destroy exactness in situations where we would hope for, and expect, long exact sequences. The problem is related to the fact that, depending how you view this, we are using just one sphere, or alternatively an infinite sequence of unrelated spheres. 

E.M. Brown (1974) suggested a different construction based on an infinite string of spheres and this helps reveal extra structure that helps:

##Strings of spheres
+--{: .un_defn}
######Definition######
Let $\underline{S}^n = ([0,\infty) \cup \bigcup_{k=0}^\infty(S^n \times \{k\})/(k\sim (\underline{1},k)$. This is called a **string of $n$-spheres.**
=--
This, of course, means that $\underline{S}^n $ is defined as a pushout
 
<img src="http://latex.codecogs.com/gif.latex?\xymatrix{\mathbb{N}\ar[r]\ar[d]%26[0,\infty)\ar[d]\\S^n\times\mathbb{N}\ar[r]%26\underline{S}^n}"/>

For the string of circles, it looks something like this:

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="743.85675"
   height="124.42857"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   version="1.0"
   sodipodi:docname="string-of-circles.svg"
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
     inkscape:zoom="1"
     inkscape:cx="423.63484"
     inkscape:cy="571.95397"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="true"
     inkscape:window-width="1152"
     inkscape:window-height="701"
     inkscape:window-x="0"
     inkscape:window-y="22">
    <inkscape:grid
       type="xygrid"
       id="grid3157"
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
     transform="translate(-86.642857,-160.16591)">
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#050803;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path2383"
       sodipodi:cx="108.57143"
       sodipodi:cy="225.52306"
       sodipodi:rx="22.857143"
       sodipodi:ry="61.42857"
       d="M 131.42857,225.52306 A 22.857143,61.42857 0 1 1 85.714283,225.52306 A 22.857143,61.42857 0 1 1 131.42857,225.52306 z"
       transform="translate(1.4285736,-2.8571434)" />
    <path
       style="fill:none;stroke:#050803;stroke-width:0.99921262;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 110,284.09448 L 710,284.09448"
       id="path3159" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#050803;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path3161"
       sodipodi:cx="108.57143"
       sodipodi:cy="225.52306"
       sodipodi:rx="22.857143"
       sodipodi:ry="61.42857"
       d="M 131.42857,225.52306 A 22.857143,61.42857 0 1 1 85.714283,225.52306 A 22.857143,61.42857 0 1 1 131.42857,225.52306 z"
       transform="matrix(1,0,0,-1,111.42857,448.18897)" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#050803;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path3163"
       sodipodi:cx="108.57143"
       sodipodi:cy="225.52306"
       sodipodi:rx="22.857143"
       sodipodi:ry="61.42857"
       d="M 131.42857,225.52306 A 22.857143,61.42857 0 1 1 85.714283,225.52306 A 22.857143,61.42857 0 1 1 131.42857,225.52306 z"
       transform="translate(213.42857,-2.8571434)" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#050803;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path3165"
       sodipodi:cx="108.57143"
       sodipodi:cy="225.52306"
       sodipodi:rx="22.857143"
       sodipodi:ry="61.42857"
       d="M 131.42857,225.52306 A 22.857143,61.42857 0 1 1 85.714283,225.52306 A 22.857143,61.42857 0 1 1 131.42857,225.52306 z"
       transform="translate(313.57143,-3.4285736)" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#050803;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path3167"
       sodipodi:cx="108.57143"
       sodipodi:cy="225.52306"
       sodipodi:rx="22.857143"
       sodipodi:ry="61.42857"
       d="M 131.42857,225.52306 A 22.857143,61.42857 0 1 1 85.714283,225.52306 A 22.857143,61.42857 0 1 1 131.42857,225.52306 z"
       transform="translate(411.28572,-3.4285736)" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#050803;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path3169"
       sodipodi:cx="108.57143"
       sodipodi:cy="225.52306"
       sodipodi:rx="22.857143"
       sodipodi:ry="61.42857"
       d="M 131.42857,225.52306 A 22.857143,61.42857 0 1 1 85.714283,225.52306 A 22.857143,61.42857 0 1 1 131.42857,225.52306 z"
       transform="translate(1.4285736,-2.8571434)" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#050803;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path3171"
       sodipodi:cx="108.57143"
       sodipodi:cy="225.52306"
       sodipodi:rx="22.857143"
       sodipodi:ry="61.42857"
       d="M 131.42857,225.52306 A 22.857143,61.42857 0 1 1 85.714283,225.52306 A 22.857143,61.42857 0 1 1 131.42857,225.52306 z"
       transform="translate(1.4285736,-2.8571434)" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#050803;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path3173"
       sodipodi:cx="108.57143"
       sodipodi:cy="225.52306"
       sodipodi:rx="22.857143"
       sodipodi:ry="61.42857"
       d="M 131.42857,225.52306 A 22.857143,61.42857 0 1 1 85.714283,225.52306 A 22.857143,61.42857 0 1 1 131.42857,225.52306 z"
       transform="matrix(1,0,0,-1,512.57143,447.61754)" />
    <path
       style="fill:none;stroke:#050803;stroke-width:0.99921262;stroke-miterlimit:4;stroke-dasharray:5.99527574, 0.99921262;stroke-dashoffset:0;stroke-opacity:1"
       d="M 720,284.09448 L 830,284.09448"
       id="path3175" />
    <path
       sodipodi:type="arc"
       style="opacity:1;fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#050803;stroke-width:1;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:none;marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:4, 1;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       id="path3177"
       sodipodi:cx="108.57143"
       sodipodi:cy="225.52306"
       sodipodi:rx="22.857143"
       sodipodi:ry="61.42857"
       d="M 131.42857,225.52306 A 22.857143,61.42857 0 1 1 85.714283,225.52306 A 22.857143,61.42857 0 1 1 131.42857,225.52306 z"
       transform="matrix(1,0,0,-1,604.28572,447.61754)" />
  </g>
</svg>


###Properties###
1. $\varepsilon(\underline{S}^n)$ is a pro-space isomorphic to an $\mathbb{N}$-indexed one with $k^{th}$ level, $\bigvee_{j\geq k}S^n_j$, where each $S^n_j$ is a copy of $S^n$.  The structural/ bonding maps from the $(k+1)^{st}$ level to the $k^{th$ level are the obvious inclusions.

1. The space $\underline{S}^n$ is, of course, considered as being based at the ray (given by the right vertical map in the pushout square).

1. The space $\underline{S}^n$ is a [[spherical object]] and the family $\mathcal{A} = \{\underline{S}^n\}^\infty_{n=0}$ defines a theory.

##The Brown-Grossman homotopy groups##
+--{: .un_defn}
######Definition######
The $n^{th}$ _Brown-Grossman homotopy group_ of $(X,*)$ is given by the  group of based proper homotopy classes of based proper maps from $\underline{S}^n$ to $(X,*)$;

$$\underline{\pi}_n(X,*) = Ho(Proper)(\underline{S}^n, (X,*)).$$
=--


###Properties###
1. As was pointed out above, the $\underline{S}^n$ are cogroups so the $\underline{\pi}_n(X,*)$ are groups, which are abelian for $n\geq 2$.

1. In fact the $\underline{\pi}_n(X,*)$ form a $\Pi_\mathcal{A}$-[[spherical object|algebra]] for $\mathcal{A}$ as above.  Not only are there the sort of morphisms in $\Pi_\mathcal{A}$ that will induce analogues of [[Whitehead products]], [[composition operations]] etc. but there are other interesting morphisms there, for instance: 

1. There is a proper **shift map** $S: \underline{S}^n\to \underline{S}^n$, which  shifts all the spheres one place to the right.   This induces, by composition, a morphism $S^*(X): \underline{\pi}_n(X,*)\to \underline{\pi}_n(X,*)$. This means that each individual $\underline{\pi}_n(X,*)$ has more structure than simply being a group.

##The variant 'at the end'##
###The Brown-Grossman homotopy groups at $\infty$###
+--{: .un_defn}
######Definition######
The $n^{th}$ _Brown-Grossman homotopy group of $(X,*)$ at $\infty$_ is given by the  group of based germ homotopy classes of based proper germs from $\underline{S}^n$ to $(X,*)$;

$$\underline{\pi}^\infty_n(X,*) = Ho(Proper_\infty)(\underline{S}^n, (X,*)).$$
=--
With this description, it is clear that $\underline{\pi}^\infty_n$ is functorial on base rayed spaces and that it only depends on the choice of the class of $*$ within $e(X)$ (cf. [[proper homotopy theory]]).

##A proper Whitehead theorem##
There are several different types of generalisation of Whitehead's theorem to the proper homotopy setting.  The following is due to Ed Brown (1974):
+--{: .un_thm}
######Theorem######
**(Brown, 1974)**
Let $K$, $L$ be finite dimensional connected locally finite [[simplicial complexes]], then a proper map $f : K \to L$ is a proper homotopy equivalence if, and only if:

1. $e(f) : e(K)\to e(L)$ is a homeomorphism;

1. for each $n$ $\pi_n(f) : \pi_n(K,*(0))\to \pi_n(L,f(*(0)))$ is an isomorphism;

1. for each $n$, and for each base ray, $*$, in $K$, $\underline{\pi}^\infty_n(K,*)\to \underline{\pi}^\infty_n(L,f(*))$ is an isomorphism.

=--
If one removes the condition of finite dimensionality, the result no longer holds. (There is an error in Brown's subsequent reasoning in the quoted paper, for which one needs to consult Edwards and Hastings, (1976).)

##Brown's $\mathcal{P}$-functor##
It would be useful to have a construction of the groups $\underline{\pi}^\infty_n(X,*)$ from the [[pro-group]] $\pi_n(\varepsilon(X),*(k))$. Such a construction was given by Brown in the same article (1974).  (An alternative construction due to Grossman will be discussed in a separate entry.)

Let $\underline{G} = \{G_n,p^m_n\}$ be an inverse sequence of groups (aka _tower of groups_), that is a pro-group that is indexed by the ordered set of positive integers. We assume $G_0=1$. Consider all sequences $\{g_{k(n)}\}$ with $g_{k(n)} \in G_{k(n)}$, where $k(n)$ is a sequence of natural numbers such that $k(n)\to \infty$ as $n\to \infty$. Given two such sequences $\{g_{k(n)}\}$ and $\{g\prime_{l(n)}\}$, we say they are equivalent if there is a third sequence $m(n)$, $m(n)\to \infty$ as $n \to \infty$, with $m(n)\leq min(k(n),l(n)))$ and $p^{k(n)}_{m(n)}(g_{k(n)}) =  p^{l(n)}_{m(n)}(g\prime_{l(n)})$.  We let $\,mathcal{P}(\underline{G})$ be the set of equivalence classes.

* This has a natural group structure;

* If $X = \bigcup_n K_n$, $U_n = X- K_n$, and $* : [0,\infty) \to X$ is chosen so that $*[n,\infty)\subset U_n$, then setting $G_n = \pi_k(U_n,*(n))$ with $G_n\to G_{n-1}$ induced by the inclusion of $U_n$ into $U_{n-1}$ and the change of base point along $*([n-1,n])$, then $\underline{\pi}^\infty_n(X,*) \cong \mathcal{P}(\underline{G}).$

* For any tower of groups, $\underline{G}$ there is an action of the group $F = \underline{\pi}_1(\underline{S}^1,[0,\infty)$ on $\mathcal{P}(\underline{G})$.

* (Chipman) Let $\underline{G}$, $\underline{H}$ be towers of finitely generated groups, then $\underline{G}$ is isomorphic to $\underline{H}$ if, and only if, there is an isomorphism from $\mathcal{P}(\underline{G})$ to $\mathcal{P}(\underline{H})$ commuting with the operation of $F$.  (What is remarkable here is that initially no morphism between $\underline{G}$ and $\underline{H}$ is given.  It is constructed from the ones on the images under $\mathcal{P}$.






##References##
 General references include: the survey article:

* [[Tim Porter]], _Proper Homotopy Theory_,  in the _Handbook on Algebraic Topology_, Ed. I.M.James, Elsevier, 1995, p. 127-167,

and for a slightly different approach:

* [[Hans-Joachim Baues|Hans Baues]] and Antonio Quintero, _Infinite homotopy theory_, Volume 6 of K-monographs in mathematics,	Springer, 2001

A specific reference for the Brown Whitehead theorem is 

*  E. M. Brown, _Proper homotopy theory in simplicial complexes,_ Topology Conference (Virginia Polytechnic Institute and State University, Dickmann and Fletcher, eds.) SLNM 375, Springer (1974), pp. 41-46,

and further 

*  D. A. Edwards and H. M. Hastings, _&#268;ech and Steenrod Homotopy Theory with Applications,_ SLNM 542, Springer (1976).

[[!redirects Brown-Grossman homotopy groups]]