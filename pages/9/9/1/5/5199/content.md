

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

A **framed link** is a [[link]] where the [[circles]] forming the components are viewed as having a thickness, albeit an arbitrarily small thickness.
That is to say, instead of the components of the links being [[embedding of smooth manifolds|embedded]] circles, they are embedded solid [[tori]].

The thickening can be considered in one direction only which gives [[embedding of smooth manifolds|embedded]] [[ribbons]].  This is an equivalent definition which can be useful as it makes the distinction clearer between an embedding and the same embedding composed with, say, a [[Dehn twist]].

A [[link diagram]] can be made into a diagram of a framed links by giving it the **blackboard framing**: this views each segment of the link diagram as a ribbon lying on the "blackboard".



## Definition 

The precise notion of a framing on a link is perhaps most naturally given in terms of [[smooth manifold|smooth structures]] on [[manifolds]]. We'll start from there and later give other versions. 

### Framing

Let $M$ be an [[orientation|oriented]] [[3-manifold]], for example $S^3$. The [[tangent bundle]] $p: T M \to M$ is a bundle with [[structure group]] [[general linear group|$GL(3) = GL(\mathbb{R}^3)$]] which in fact admits a [[reduction of the structure group|reduction]] to $GL_+(3)$ (invertible [[linear transformations]] with [[positive number|positive]] [[determinant]]) since $M$ is oriented. A further reduction to the structure group [[SO(3)|$SO(3)$]] can be effected by a number of means, e.g., by equipping $M$ with a [[Riemannian metric]]. 

Now let 

$$
  L
  \;\colon\; 
  S^1 \sqcup \ldots \sqcup S^1 \hookrightarrow M
$$ 

be a smoothly embedded link (of oriented circles). The [[normal bundle]] of $L$ is the [[cokernel]] of the bundle inclusion 

$$T(S^1 \sqcup \ldots \sqcup S^1) \to L^\ast T M$$ 

(as bundles over $S^1 \sqcup \ldots \sqcup S^1$); it is naturally [[associated bundle|associated]] with a [[principal bundle|principal]] $SO(2)$-bundle. A *framing* of $L$ is simply a choice of [[section]] $\sigma$ of this principal $SO(2)$-bundle. It can be thought of as a smooth choice of unit normal vectors along points of the embedded link, and can be visualized as "ribbons", one for each component $S^1$, with one edge of the ribbon being that component. 

The $SO(2)$-bundle or circle bundle over each component $S^1$ can be seen as an embedded [[torus]] in $M$. The framing itself induces a diffeomorphism on this torus which takes an element $(\xi, p)$ over $p \in S^1$ to $(\sigma(p)\xi, p)$. 

### Framing number

However, it is often convenient to consider such framings, or rather their associated torus [[diffeomorphisms]], only up to [[isotopy]]. For each component $S^1$, the [[isotopy class]] is specified by an [[integer]] which gives the number of 360 degree clockwise rotations of the unit normal or clockwise twists of the ribbon as one traverses the component in the direction of its orientation. This is called the *framing number*.

If one regards the framed link as a ribbon link, then its framing number is the [[linking number]] of the two [[boundary of a manifold|boundaries]] of the [[ribbon]].

Thus an alternative way of describing a framing on an [[oriented link]] is by assigning an integer (framing number) to each link component.

\begin{definition}
\label{LinkingMatrix}
The *[[linking matrix]]* of a [[framed link]] is the [[square matrix]] indexed by the [[connected components]] of the link whose off-diagonal entries are the [[linking numbers]] and whose diagonal entries are the [[framing numbers]].
\end{definition}
(e.g. [Ohtsuki 2001 p 227](#Ohtsuki01))

Notice that the linking matrix is a [[symmetric matrix]].

## Examples

Framings of the [[trefoil knot]]:

\begin{imagefromfile}
    "file_name": "FramingsOfTrefoilKnot.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [CMNP 19](#CMNP19)"
\end{imagefromfile}


## Properties

### Reidemeister moves
 {#ReidemeisterMoves}

A pair of framed [[link diagrams]] corresponds to the same framed link iff they may be deformed into each other by diagram [[isotopies]] and the following versions of the [[Reidemeister moves]] (e.g. [Ohtsuki 2001 Thm. 1.8](#Ohtsuki01)): 

\begin{imagefromfile}
    "file_name": "FramedLinkReidemeister-240718.jpg",
    "width": 650,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Here (only) the first is different from the 1st [[Reidemeister move]] for ordinary [[links]]: Where the latter says that a "twist" in the link diagram may by removed (by "yanking" it straight), here for framed link this is no longer the case in general, but that a twist may cancel against the opposite twist:

[[!include modified Reidemeister move 1 - SVG]]




## Related entries

* [[framed braid]], [[plat closure]]

* [[surgery]], [[Dehn surgery]], [[Kirby calculus]]

* [[normal framing]]

* [[framed manifold]]

* [[oriented link]]

* [[linking number]]

* [[crossing number]]

* [[writhe]]

## References

Survey:

* Mohamed Elhamdadi, Mustafa Hajij, Kyle Istvan: *Framed Knots*, Math Intelligencer **42** (2020) 7–22 &lbrack;[doi:10.1007/s00283-020-09990-0](https://doi.org/10.1007/s00283-020-09990-0), [arXiv:1910.10257](https://arxiv.org/abs/1910.10257)&rbrack;

Textbooks:

* {#Ohtsuki01} [[Tomotada Ohtsuki]], pp. 15 in: *Quantum Invariants -- A Study of Knots, 3-Manifolds, and Their Sets*, World Scientific (2001) &lbrack;[doi:10.1142/4746](https://doi.org/10.1142/4746)&rbrack;


Lecture notes:

* Roland van der Veen: Def. 4 of: *A smooth introduction to knots*, lecture notes (2016) &lbrack;[pdf](https://www.julianlyczak.nl/seminar/knots2016-files/KnotesJan18.pdf), [[vdVeen-SmoothKnots.pdf:file]]&rbrack;

Vivid illustrations:

* Mustafa Hajij: *Framed knot* (2022) &lbrack;video:[YT](https://youtu.be/KxEBhD0C2Pw)&rbrack;

* Nadav Drukker, Elise Paznokas, Dominik Schrimpel: *Knitting Knots & the Framing Anomaly*, in: *Proceedings of Bridges 2022: Mathematics, Art, Music, Architecture, Culture*, Tessalations Publishing (2022) 245-252 &lbrack;[arXiv:2210.16677](https://arxiv.org/abs/2210.16677), [web](https://archive.bridgesmathart.org/2022/bridges2022-245.html#gsc.tab=0),  [pdf](https://archive.bridgesmathart.org/2022/bridges2022-245.pdf)&rbrack;

Discussion of framed links in the context of regularizing [[Wilson loop]] [[quantum observables]] in [[Chern-Simons theory]]:

* {#Witten89} [[Edward Witten]], pp  20 in: _Quantum Field Theory and the Jones Polynomial_, Commun. Math. Phys. **121** 3 (1989) 351-399. MR0990772 &lbrack;[doi:10.1007/BF01217730](https://doi.org/10.1007/BF01217730), 
[euclid:cmp/1104178138](http://projecteuclid.org/euclid.cmp/1104178138)&rbrack;

* {#CMNP19} Giancarlo Camilo, [[Dmitry Melnikov]], Fábio Novaes, Andrea Prudenziati: *Circuit Complexity of Knot States in Chern-Simons theory*, J. High Energ. Phys. **2019** 163 (2019) &lbrack;[arXiv:1903.10609](https://arxiv.org/abs/1903.10609), <a href="https://doi.org/10.1007/JHEP07(2019)163">doi:10.1007/JHEP07(2019)163</a>&rbrack;

* {#Grabovsky22} David Grabovsky: pp 22 in: *Chern–Simons Theory in a Knotshell* (2022) &lbrack;[pdf](https://web.physics.ucsb.edu/~davidgrabovsky/files-notes/CS%20and%20Knots.pdf), [[Grabovsky-CSTheory.pdf:file]]&rbrack;

See also:

* Jianhua Wang: *Framed and oriented links of codimension 2* &lbrack;[arXiv:math/0205300](https://arxiv.org/abs/math/0205300)&rbrack;



[[!redirects framed links]]
[[!redirects Framed link]]
[[!redirects Framed links]]
[[!redirects framed knot]]
[[!redirects framed knots]]
[[!redirects Framed knot]]
[[!redirects Framed knots]]

[[!redirects framing number]]
[[!redirects framing numbers]]

