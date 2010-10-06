
#Contents#
* automatic table of contents goes here
{:toc}

## Idea of some problems

**Proper homotopy theory** is both an old and a fairly new area of [[algebraic topology].
It deals with properties of non-[[compact space|compact]] [[topological space]]s, that cannot be detected using maps from [[simplex|simplices]] in these spaces, such as used in the [[fundamental infinity-groupoid|singular complex]]. 

Historically the subject is traced back to Kerekjarto's classification of non-compact surfaces in 1923, but its emergence as an important tool in geometric topology came with Larry Siebenmann's work in 1965.

Suppose $M$ is a _smooth_ [[manifold]] with boundary, $\partial M$, then $M\setminus \partial M$ is an open manifold. Now suppose someone gives us an open manifold $N$, is it possible to detect if there is a compact manifold $M$, with $M\setminus \partial \cong N$.  Siebenmann showed that certain conditions on the _ends_ of $N$ were necessary and that there were obstructions if the dimension of $M$ was greater than 5.

Its potential importance of proper homotopy, 
for example for physical applications, comes from the fact that the phenomena it studies include the limiting behaviour of the system.

##Intuitions

The basic hypothesis will be that $X$ will be a [[connected space|connected and locally connected]] compact [[Hausdorff space]. It will usually be $\sigma$-compact, i.e., there will be an increasing sequence, $\{K_n\}$, of compact subspaces with each $K_n$ in the interior of $K_{n+1}$ and such that 

$$X = \bigcup^\infty_{n=0}K_n,$$

These spaces will most often than not be locally finite [[simplicial complex]]es.

We will  be interested in the [[homotopy]] of such spaces 'out towards its ends' 


###Ends###

To illustrate the idea of the ends of a space $X$, we note that naively $\mathbb{R}$ has two ends, $\infty$ and $-\infty$, whilst $\mathbb{R}^2$ has only one as it is $S^2\setminus \{\infty\}$, (but that is vague!).

More exactly, consider the system of spaces

$$\varepsilon(X) = \{closure(X\setminus K) : K compact \subset X\},$$

This is an inverse system or [[pro-object]] in the category of spaces. Applying the connected component functor, $\pi_0$, to this system of spaces gives $\pi_0(X)$, and, classically, one takes the limit of this to get 

$$e(X) = lim \pi_0\varepsilon(X),$$
the _set of ends_ of $X$. In general, $e(X)$ would be given the [[inverse limit topology]], to preserve more of the information coming from its construction.  This space is the _space of (Freudenthal) ends of $X$_. It is a [[profinite space]].

####Examples####
* Let $X_8$ be the figure eight space, the one-point union of two circles, and let $X$ be its universal cover.  This is an infinite 'thorn bush'. It has infinitely many ends and 
$$e(X) \cong 2^{\aleph_0}.$$

* Let $M$ be a compact manifold and $X = M\setminus \partial M$, then
$e(X) \cong \pi_0(\partial M)$.

###Proper maps###
The assignment sending $X$ to $E(X)$ cannot be functorial on the category of spaces and _continuous_ maps, since the contracting map $\mathbb{R}\to \{0\}$ is continuous, $e(\mathbb{R})$ is $\{-\infty, \infty\}$, whilst $e(\{0\})$ is empty since $\{0\}$ is compact.
The problem is that continuity is really about inverse images (inverse image of open is open), but the inverse image mapping does not preserve compactness  (as in the example!).

####Definition (recall)####
A map $f:X\to Y$ is a [[proper map]] if for each subset $K$ compact in $Y$ then $f^{-1}(K)$ is compact in $X$.

###End spaces continued###
If $f:X\to Y$ is proper, then it induces a pro-morphism
$$\varepsilon(f) : \varepsilon(X)\to \varepsilon(Y)$$
and hence a _continuous map of the end spaces
$$e(f):e(X)\to e(Y),$$
and $e$ becomes a functor from some category $Proper$ of spaces and proper maps to $Stone$, the category of [[profinite space]]s / [[Stone space]]s.

###Proper homotopy###
+-- {: .un_proposition}
###### Proposition . 

For any space $X$, the natural inclusions of $X$ into $X \times I$, $e_i(x) = (x,i)$, $i = 0,1$ together with the projection maps from $X\times I$ to $X$, are proper maps.
=--
+-- {: .un_corollary}
###### Corollary
The category $Proper$ has a [[cylinder functor]].
=--

We call the corresponding notion of homotopy, 'proper homotopy'.
We get a 'Proper category' and an associated 'proper homotopy category', which we will denote $Ho(Proper)$. If we are restricting to $\sigma$-compact spaces we may write $Proper_\sigma$, and so on.

###Germs at $\infty$###
Although a proper map $f: X\to Y$ will induce a continuous $\varepsilon(f)$, on the end spaces, it is clear that $f$ does not need to be defined on the whole of $X$ for this to work, as $\varepsilon$ encodes behaviour 'out towards $\infty$'.  This leads to the notion of a 'germ at $\infty$'.

Suppose $X$ is locally compact Hausdorff and $A\subset X$. The inclusion $j: A\to X$ is 'cofinal' if the closure of $W\setminus A$ is compact.  Note that a cofinal inclusion is proper and induces an isomorphism $\varepsilon(A)\cong \varepsilon(X)$.  Let $\Sigma$ be the class of all cofinal inclusions in $Proper$ and let $Proper_\infty = Proper[\Sigma^{-1}]$, the category obtained by formally inverting the cofinal inclusions. 

####Definition#### 

This category is called the _proper category at $\infty$_.

Note that $(Proper,\Sigma)$ admits a [[calculus of fractions|calculus of right fractions]], so any morphism from $X$ to $Y$ in $Proper_\infty$ can be represented by a diagram 
$$X\stackrel{j}{\leftarrow} A \stackrel{f}{\rightarrow}Y,$$
with $j$ a cofinal inclusion, i.e., $f$ is defined on some 'neighbourhood of the end of $X$'.

Two such diagrams 
$$X\stackrel{j^{\prime}}{\leftarrow} A^{\prime} \stackrel{f^\prime}{\rightarrow}Y   and       X\stackrel{j^{\prime\prime}}{\leftarrow} A^{\prime\prime} \stackrel{f^{\prime\prime}}{\rightarrow}Y$$
represent the same germ if $f^\prime | A = f^{\prime\prime}|A$ for some cofinal subspace  $A$ with $A^\prime \cup A^{\prime\prime}\subset A$.


There is also a homotopy category $Ho(Proper_\infty)$

+--{.query}
The end space $e(X)$ is a Stone space so is $Max(R)$ for some Boolean algebra $R$ (Stone duality) In the 1960s someone (Goldman?) looked at a ring, $R$, of 'almost continuous functions' from $X$ to $\mathbb{Z}/2\mathbb{Z}$, that gave the right $e(X)$.  Can this idea help integrate better the ideas of proper homotopy etc. with modern methods of algebraic geometry?
=--
##Proper analogues of the fundamental group.##
The end space behaves a bit like a $\pi_0$ and usually spaces will have many ends, so are not 'connected at infinity'.  If we try to do a fundamental group or groupoid analogue, this means life will get more complicated.  We will try with the assumption of a space having a single end for simplicity!  We will also assume $X$ is $\sigma$-compact.

###First attempt###
We could try defining $\pi_1(\varepsilon(X))$ as a progroup, then taking its limit.  For this we would take $\{K_n\}$ an exhausting increasing sequence of compact subsets and setting $U_i = X\setminus K_i$, pick a base point $x_i$ in each $U_i$, and we will get groups $\pi_1(U_i,x_i)$.  We however need induced homomorphisms $\pi_1(U_{i+1},x_{i+1})\to \pi_1(U_i,x_i)$, and for this we have to choose an arc in $U_i$ from $x_{i+1}$ to $x_i$.  We can combine these to get a _base ray_, rather than a _base point_,  that is, we need a proper map, $\alpha : [0,\infty)\to X$.  With that we do get an inverse sequence of groups, but there are problems.  What is the dependence of the inverse system on the choice of $\alpha$?
<svg width="640" height="480" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink" se:nonce="86885">
 <g>
  <title>Layer 1</title>
  <use x="1203.639282" y="868.198853" transform="translate(100.832, 109.273) scale(1, 0.905592) translate(-100.832, -109.273) translate(100.832, 109.273) scale(1.27683, 1) translate(-100.832, -109.273) translate(480.129, 395.262) scale(1.24647, 1.25993) translate(-480.129, -395.262) translate(175.832, 168.273) scale(0.918502, 1.4277) translate(-175.832, -168.273) translate(175.832, 168.273) scale(0.904449, 0.691289) translate(-175.832, -168.273) translate(175.828, 168.273) scale(2.92331, 3.53877) translate(-175.828, -168.273) matrix(0.152039, 0, 0, 0.152039, 0, 0)" id="svg_86885_2" xlink:href="#svg_86885_1"/>
 </g>
 <defs>
  <symbol id="svg_86885_1" height="744.09448" width="1052.3622">
   <metadata id="metadata7">image/svg+xml</metadata>
   <g id="layer1">
    <path fill="#ffe6d5" fill-rule="evenodd" stroke="#000000" stroke-width="1px" marker-start="none" marker-mid="none" marker-end="none" stroke-miterlimit="4" stroke-dashoffset="0" transform="translate(-64.6405, 239.242)" d="m202.857147,254.094482a34.285709,61.42857 0 1 1 -68.571442,0a34.285709,61.42857 0 1 1 68.571442,0z" id="path2383"/>
    <path fill="none" fill-rule="evenodd" stroke="#000000" stroke-width="1px" id="path2387" d="m99.624733,432.649414c516.747887,-148.801788 516.747887,-148.801788 516.747887,-148.801788l1.352783,-1.352722"/>
    <path fill="none" fill-rule="evenodd" stroke="#000000" stroke-width="1px" id="path2389" d="m110.77491,553.753906l518.100639,-217.791656"/>
    <path fill="#fffdfe" fill-rule="evenodd" stroke="#000000" stroke-width="1px" marker-start="none" marker-mid="none" marker-end="none" stroke-miterlimit="4" stroke-dashoffset="0" transform="matrix(0.814331, 0, 0, 0.822406, 49.4903, 147.729)" d="m202.857147,254.094482a34.285709,61.42857 0 1 1 -68.571442,0a34.285709,61.42857 0 1 1 68.571442,0z" id="path2391"/>
    <path fill="#fffdfe" fill-rule="evenodd" stroke="#000000" stroke-width="1px" marker-start="none" marker-mid="none" marker-end="none" stroke-miterlimit="4" stroke-dashoffset="0" id="path3163" d="m202.857147,254.094482a34.285709,61.42857 0 1 1 -68.571442,0a34.285709,61.42857 0 1 1 68.571442,0z" transform="matrix(0.64873, 0, 0, 0.745549, 177.364, 142.388)"/>
    <path fill="#fffdfe" fill-rule="evenodd" stroke="#000000" stroke-width="1px" marker-start="none" marker-mid="none" marker-end="none" stroke-miterlimit="4" stroke-dashoffset="0" transform="matrix(0.676825, 0, 0, 0.687266, 257.281, 136.872)" d="m202.857147,254.094482a34.285709,61.42857 0 1 1 -68.571442,0a34.285709,61.42857 0 1 1 68.571442,0z" id="path3165"/>
    <path fill="#fffdfe" fill-rule="evenodd" stroke="#000000" stroke-width="1px" marker-start="none" marker-mid="none" marker-end="none" stroke-miterlimit="4" stroke-dashoffset="0" id="path3167" d="m202.857147,254.094482a34.285709,61.42857 0 1 1 -68.571442,0a34.285709,61.42857 0 1 1 68.571442,0z" transform="matrix(0.614871, 0, 0, 0.637115, 343.53, 131.201)"/>
    <path fill="#fffdfe" fill-rule="evenodd" stroke="#000000" stroke-width="1px" marker-start="none" marker-mid="none" marker-end="none" stroke-miterlimit="4" stroke-dashoffset="0" transform="matrix(0.566765, 0, 0, 0.586908, 423.618, 126.502)" d="m202.857147,254.094482a34.285709,61.42857 0 1 1 -68.571442,0a34.285709,61.42857 0 1 1 68.571442,0z" id="path3169"/>
    <path fill="#fffdfe" id="path3173" d="m-46.161949,467.045288l0,-198.002533l206.970024,0.0047l206.970032,0.004669l-2.484406,1.156708c-14.808228,6.894592 -21.974426,37.255829 -14.625671,61.965179c1.498749,5.039337 4.11319,10.318848 7.0336,14.203339c2.326538,3.094574 7.076477,6.694763 9.462433,7.171936c0.7323,0.146454 1.331451,0.413971 1.331451,0.594452c0,0.234344 -54.170319,16.075165 -73.22287,21.412292c-0.42099,0.11792 0.502686,-1.118256 2.052612,-2.74704c5.094696,-5.354034 9.188965,-15.432678 11.164307,-27.482635c1.157166,-7.059204 1.059723,-20.816772 -0.198212,-27.978638c-2.105103,-11.985046 -5.583221,-20.497711 -10.621399,-25.996002c-15.426971,-16.835815 -33.526337,4.953644 -33.511719,40.344025c0.005859,14.154419 2.261627,24.816406 7.285522,34.435211c3.178833,6.086212 7.049622,9.829559 11.841827,11.451874l2.265259,0.766846l-42.822235,12.315186c-23.552216,6.773376 -43.014847,12.31012 -43.25029,12.303925c-0.235428,-0.006195 0.662048,-1.16391 1.994415,-2.572693c6.005402,-6.349823 10.374054,-16.376343 12.614334,-28.951294c1.394638,-7.828339 1.396729,-21.45163 0.004471,-29.227173c-2.056427,-11.48468 -5.674393,-20.579041 -10.785599,-27.111389c-9.808899,-12.536194 -23.298584,-12.531433 -33.112885,0.011658c-16.640549,21.267365 -15.604706,66.781738 1.943268,85.385468c2.997681,3.17804 5.476471,4.898621 8.860687,6.150452l2.61261,0.966431l-4.047409,1.220459c-7.142929,2.15387 -77.11274,22.213165 -80.204086,22.993317c-8.860176,2.235962 -16.251457,9.356842 -21.896736,21.095612c-5.694199,11.840515 -8.361,24.73288 -8.361,40.420319c0,15.527374 2.740265,28.766754 8.373726,40.457062c7.523247,15.612 18.667213,23.374878 30.365898,21.152893c177.877182,-49.187134 361.230423,-126.223846 521.298721,-218.84021c0.006775,-0.328796 -0.235779,-0.597809 -0.538879,-0.597809c-0.303223,0 -108.792053,46.003479 -248.100983,104.568176c-139.308975,58.564697 -259.458694,108.509369 -259.984779,108.650055c-0.650909,0.174011 -0.212395,-0.523071 1.37249,-2.18158c3.228477,-3.37854 5.168472,-6.218262 7.896103,-11.55835c13.37738,-26.189575 11.800735,-66.417114 -3.505447,-89.440887c-4.48439,-6.745483 -11.014824,-11.980438 -16.744446,-13.42276l-2.928421,-0.737183l41.390076,-11.891388c22.764542,-6.540283 43.865112,-12.621002 46.890152,-13.512756c3.02504,-0.891754 99.188187,-28.594788 213.695908,-61.562286c115.294861,-33.194153 208.527771,-60.272858 208.939697,-60.684784c1.01709,-1.01712 0.347046,-2.100555 -0.732056,-1.183685c-0.653809,0.555481 -86.983948,25.697784 -88.233459,25.696564c-0.219604,-0.000183 0.462341,-0.979279 1.515503,-2.17572c1.053162,-1.196442 2.771667,-3.940491 3.818909,-6.0979c3.446716,-7.100372 5.015503,-14.813446 5.005005,-24.607605l-0.006775,-6.337036l118.545776,0l118.545837,0l0,198.002533l0,198.002502l-411.070435,0l-411.070457,0l0,-198.002502z"/>
    <path fill="none" fill-rule="evenodd" stroke="#000000" stroke-width="1px" id="path3195" d="m113.82753,434.17749l491.658432,-143.480072"/>
    <path fill="none" fill-rule="evenodd" stroke="#000000" stroke-width="1px" id="path3211" d="m272.612152,391.133484c154.001953,93.740295 154.001953,93.740295 154.001953,93.740295"/>
    <path fill="none" fill-rule="evenodd" stroke="#000000" stroke-width="1px" id="path3213" d="m486.875763,449.482025l-6.69574,-8.608795"/>
    <text font-size="16px" font-style="normal" font-weight="normal" text-anchor="start" fill="#000000" stroke-width="1px" font-family="Bitstream Vera Sans" id="text3215" y="501.135" x="401.744" xml:space="preserve">
     <tspan y="501.135" x="401.744" id="tspan3217">base ray</tspan>
    </text>
   </g>
  </symbol>
 </defs>
</svg>

Let $X$ be an infinite cylinder with an infinite string of circles attached via a proper ray $\alpha: [0,\infty) \to X$. 
The space has just one 'end' but you can choose different ways of going from $\pi_1(U_{i+1},x_{i+1})$ to $\pi_1(U_i,x_i)$ for fairly obvious choices of  base points such that the limit groups of the resulting two inverse systems are non-isomorphic! (In the survey listed below, this example is examined in detail, and one of the limits is a free group on one element, the other is trivial! Definitely non-isomorphic!)

This means that $lim \pi_1(\varepsilon(X))$ is not an invariant of the end. This phenomenon is linked to the fact that $\pi_1(\varepsilon(X))$ does not satisfy the [[Mittag-Leffler condition]] for either choice of the base rays.


###Waldhausen Boundary###

If $X$ and $Y$ are locally compact Hausdorff spaces, there is no obvious candidate for a space of proper maps from $X$ to $Y$, but one can form a simplicial set $\mathbb{P}(X,Y)$ with $\mathbb{P}(X,Y)_n = P(X\times \Delta^n,Y)$, which acts as if it was the singular complex of the mythical space of proper maps from $X$ to $Y$.

####Definition####
The **Waldhausen boundary** of $X$ is the simplicial set $\mathbb{P}([0,\infty),X)$.

There is an epimorphism from $\pi_0(\mathbb{P}([0,\infty),X))$ to $e(X)$.

*  In the example above of the cylinder with the string of circles attached, $\pi_0(\mathbb{P}([0,\infty),X))$,  is uncountable, and $\pi_1(\mathbb{P}([0,\infty),X))$ maps onto $lim S$.  

*  When $X$ has a single end and  $\pi_0(\varepsilon(X))$ is [[Mittag-Leffler condition|Mittag-Leffler]], then $\pi_0(\mathbb{P}([0,\infty),X))$, is a single point, i.e. all possible base rays are properly homotopic.


###Second attempt###
Even if we  did not have the above difficulty with the limit groups, we would still have the problem that, as the limit functor is not exact, the resulting limiting homotopy groups would not be that well behaved.  There would not be  any general long exact sequence results (just as with [[Čech homology]]). There is at least one possible replacement for those limiting homotopy groups, but first we note that is is not appropriate to base any such things at a point, rather we should be using a base ray as was discussed above.

##References##

Survey article:

* [[Tim Porter]], _Proper Homotopy Theory_,  in the _Handbook on Algebraic Topology_, Ed. I.M.James, Elsevier, 1995, p. 127-167,

Books:

* [[Hans-Joachim Baues|H. J. Baues]] and A. Quintero, _Infinite homotopy theory_, Volume 6 of K-monographs in mathematics,	Springer, 2001

* Bruce Hughes and Andrew Ranicki, _Ends of Complexes_, Cambridge Tracts in Mathematics (No. 123), C.U.P.

