+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

A _directed topological space_ is a [[topological space]] $X$ in which there is some 'sense of direction'. This can happen in various different ways, and the level of the 'directedness' can be different in different situations, so there are several 'competing' ideas, but the beginning of a consensus on what the overarching idea is.

If one bases homotopy theory on the idea of a [[singular simplex]] or, more generally, a singular cell of any shape, then there is no way in which a 'sense of direction' can be encoded. If we have a path in a space, we can travel along it in either direction, from 0 to 1 or from 1 to 0.  From this perspective, a directed space is one in which not every singular cell $\Delta^n \to X$ (for $\Delta^n$ the standard topological [[simplex]]) is supposed to be _traversable_ in all directions, in some sense: instead, these $k$-dimensional _paths_ may have a _direction_.

As an example, one can base the 'sense of direction' on a closed [[preorder]] or [[partial order]] (that is, a [[pospace]]), so that the paths from the directed interval $[0,1]$ with the usual order to the space $X$ can only be 'traversed' in one direction. Another example which does not fit into this first type would be the directed circle.

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="90.218414"
   height="86.221573"
   id="svg2383"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="d-circle.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
  <defs
     id="defs2385">
    <marker
       inkscape:stockid="Arrow1Lstart"
       orient="90deg"
       refY="0"
       refX="0"
       id="Arrow1Lstart"
       style="overflow:visible">
      <path
         id="path3170"
         d="M 0,0 L 5,-5 L -12.5,0 L 5,5 L 0,0 z"
         style="fill-rule:evenodd;stroke:#000000;stroke-width:1pt;marker-start:none"
         transform="matrix(0.8,0,0,0.8,10,0)" />
    </marker>
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 372.04724 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_z="1052.3622 : 372.04724 : 1"
       inkscape:persp3d-origin="526.18109 : 248.03149 : 1"
       id="perspective2392" />
  </defs>
  <sodipodi:namedview
     inkscape:document-units="mm"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     inkscape:pageopacity="0.0"
     inkscape:pageshadow="2"
     inkscape:zoom="0.86831673"
     inkscape:cx="292.72913"
     inkscape:cy="256.93488"
     inkscape:current-layer="layer1"
     id="namedview2387"
     showgrid="false"
     inkscape:window-width="663"
     inkscape:window-height="701"
     inkscape:window-x="20"
     inkscape:window-y="22" />
  <metadata
     id="metadata2389">
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
     transform="translate(-393.3659,-193.1045)">
    <path
       style="fill:none;fill-opacity:1;fill-rule:evenodd;stroke:#000000;stroke-width:0.99921262;stroke-linecap:butt;stroke-linejoin:miter;marker:none;marker-start:url(#Arrow1Lstart);marker-mid:none;marker-end:none;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1;visibility:visible;display:inline;overflow:visible;enable-background:accumulate"
       d="M 479.08786,236.21529 C 479.08786,259.73666 459.99806,278.82647 436.47668,278.82647 C 412.95531,278.82647 393.86551,259.73666 393.86551,236.21529 C 393.86551,212.69392 412.95531,193.60411 436.47668,193.60411 C 459.99806,193.60411 479.08786,212.69392 479.08786,236.21529 z"
       id="path3164" />
  </g>
</svg>
In other words, a circle with direction determined by the anticlockwise sense. Again, it is easy to see that there are certain paths that respect the direction while others do not. 

So far, there exists a well-developed theory for a notion of _directed spaces_ $X$ where 1-dimensional paths given by maps $[0,1] \to X$ from the [[interval]] into the space are equipped with a direction. See in particular the book by [[Marco Grandis]] on [[Directed Algebraic Topology]] listed below. Another suggested notion for modelling directed spaces is that of _[framed spaces](#framed_spaces)_, which is tailored towards certain higher categorical applications.

Note that a directed space is like a generalised space; not every directed space need be a space in the traditional sense, in accordance with the [[red herring principle]]. As an instance of this, note that [[Marco Grandis]] in his book [[Directed Algebraic Topology]] handles the directed homotopy of small categories, and of cubical complexes, since this is useful for comparison an interpretation of directed homotopy 'invariants'.

Directed spaces are studied in [[directed homotopy theory]], a relatively young topic. In generalization of how a [[topological space]] has a [[fundamental groupoid]], a [[directed space]] has a [[fundamental category]].



### Homotopy-theoretic perspective

From a [[homotopy theory|homotopy theoretic]] perspective, one would wish that notions of directed spaces might serve to generalize the [[homotopy hypothesis]]—which identifies ordinary (undirected) [[topological space]]s with [[∞-groupoid]]s, i.e., with [[(∞,0)-category|(∞,0)-categories]]—to a more general context where [[(∞,0)-category|(∞,0)-categories]] are generalized to [[(∞,n)-category|(∞,r)-categories]] with $r \gt 0$.

An [[(∞,r)-category]] in this context might correspond to an **$r$-directed topological space**—one that comes equipped with a notion of orientation of its $k$-cells for $0 \leq k \leq r$, but is impartial on direction above that dimension.

If such a definition exists, it may need to use [[filtered topological space]]s instead of bare topological spaces.

Even in the absence of a homotopy-theoretic definition of $r$-directed spaces in this sense, from the perspective of [[homotopy theory]], one might take the standpoint of the [[homotopy hypothesis]] and _define_ a (nice) $r$-directed space to be an [[(∞,n)-category|(∞,r)-category]], just as it makes good sense and is nowadays common practice in [[algebraic topology]] to _define_ a nice [[topological space]] to be an [[∞-groupoid]].

See [[(n,r)-category]] for more on that.


## Variants

### $d$-Spaces

A **directed topological space** or **d-space** is pair $(X, d X)$ consisting of a [[topological space]] $X$ and a subset $d X \subset C(I,X)$ of continuous maps from the interval $I = [0,1]$ into $X$ -- called _directed paths_ or d-paths -- satisfying the following conditions:

1. (constant paths) every constant map $I\to X$ is directed,

2. (reparametrisation) $dX$ is closed under composition with increasing maps $I\to I$,

3. (concatenation) $dX$ is closed under path concatenation: if the d-paths $a, b$ are consecutive in $X$ $(a(1) = b(0))$, then their ordinary concatenation $a+b$ is also a d-path

$$(a+b)(t) = a(2t),\,\text{if}\, 0\le t\le \frac{1}{2},$$

$$(a+b)(t) = b(2t-1),\,\text{if}\, \frac{1}{2}\le t\le 1.$$

A **morphism of directed topological spaces**  $f : (X, d X)\to (Y , d Y)$ is a morphism of topological spaces $f: X \to Y$ which preserves directed paths, in that, for every $\gamma: I \to X$ in $d X$, the path $f_* \gamma : I \stackrel{\gamma}{\to} X \stackrel{f}{\to} Y$ is in $d Y$.

\begin{example} Basic examples of $d$-spaces include:

* The _standard directed interval_ is $I_d = ([0,1], d I)$ with $d I$ the set of all _monotonic_ continuous maps $[0,1] \to [0,1]$

* Any [[pospace]] $X$ gives rise to a d-space by taking the directed paths to be, well, directed paths, i.e., continuous order-preserving maps from $I_d$ to $X$.

Many other example can be found in the references.
\end{example}


### Streams

A different definition comes from [[Sanjeevi Krishnan]], _A Convenient Category of Locally Preordered Spaces_, Applied Categorical Structures, 2009, vol. 17, no 5, p. 445-466 ([arxiv](https://arxiv.org/abs/0709.3646)):

__Definition__ A **stream** is a tuple $X, \leq_{-}$, where $\leq_{-}$ assigns to each open subset $U \subset X$ a preorder $\leq_U$, such that:
$$\leq_{\bigcup_i U_i} = \bigvee_i \leq_{U_i}$$
Here, $U_i, i \in I$ is a collection of open sets, and $\bigvee$ is the pointwise *or* of relations.

_Remarks_

* Morally, a point in a stream is less or equal to another point if it is less or equal in any open set. The relation $\leq_X$ for the whole space does not hold much information.
* In the typical example of the clockwise oriented circle, each point is less or equal to every other one in the relation $\leq_{S^1}$; but for a contractible subset $U \subset S^1$, a point $x$ is less or equal than $y$ if $y$ can be reached from $x$ in a monotonous clockwise path.
* The defining equation of a stream can be thought of as a (co)sheaf condition, and there is indeed a cosheafification result.
* Every d-space gives rise to a stream.
* The category of streams has good properties. In particular, there is an further notion of compactly flowing streams_ extending the notion of compactly generated Hausdorff spaces, and indeed the forgetful functor creates limits and colimits.
* The category of compactly flowing streams is Cartesian closed.

### Framed spaces {#framed_spaces}

#### Motivation

Another way to endow spaces with directions is via [[frame of a vector space|framings]], i.e. choices of a "basis of the vector space of tangential directions at each point". Somewhat abstracting this idea, frames may also be thought about in terms of [[projection#in_linear_algebra|projections]], as the following remark motivates.

\begin{rmk} Let $V$ be an $n$-dimensional [[vector space]] with an [[inner product]] $g$. The following structures on $V$ are equivalent.

* An orthonormal frame of $V$, i.e. an ordered sequence of vectors $v_i$, $1 \leq i \leq n$, such that  $g(v_i,v_j)=\delta_{ij}$.
* A sequence of surjections $V_i \to V_{i-1}$, $1 \leq i \leq n$, where $V_i$ is an oriented $i$-dimensional vector space (and $V_n = V$).

The two structures are related by setting $v_i$ to be the unit vector spanning $\ker(V_i \to V_{i-1})$ such that $V_{i-1} \oplus v_i$ recovers the orientation of $V_i$ (note that all $V_i$ canonically embed in $V$ as the orthogonal complement of the kernel of the composite map $V \to V_i$).

In the absence of inner products, one cannot speak of orthonormal frames any longer. However, sequences of projections can still be defined, and may be regarded as playing the role of "metric-free orthonormal" frames. (A vaguely analogous line of thinking is that a [[Morse function]] $M \to \mathbb{R}$ provides useful "direction" information on $M$, e.g. for the construction of handlebodies, that is ultimately independent from any chosen metric on $M$.) Moreover, this approach offers room for generalization by varying the length of the projection sequence and the vector space dimensions.
\end{rmk}

\begin{example} The standard orthonormal frame of $n$-dimensional euclidean space $\mathbb{R}^n$ consists for the ordered sequence of vectors $e_1 = (1,0,...,0)$, $e_2 = (0,1,0,...,0)$, ..., $e_n = (0,...,0,1)$. By the previous remark, this orthonormal frame is equivalently described by the sequence of projections $\pi_i : \mathbb{R}^i = \mathbb{R}^{i-1} \times \mathbb{R} \to \mathbb{R}^{i-1}$ (each $\mathbb{R}^i$ being endowed with standard orientation).
\end{example}

When forgetting basepoints, then the previous remark and example equally apply to [[affine space|affine spaces]], now endowing each point in the space with a basis of frames. Using affine standard framed $\mathbb{R}^n$ (or rather [[compact]] [[contractible]] patches of it, that interact nicely with the projections, see below) as our "local models" for framed spaces one may define global framed spaces and their maps.

#### Definition

\begin{terminology} Inductively in $n \in \mathbb{N}$, an *$n$-framed patch* $U \subset \mathbb{R}^n$ is a non-empty subspace of $\mathbb{R}^n$ with the property that its projection $\pi_n(U)$ is an $(n-1)$-framed patch, such that $\pi_n : U \to \pi_n(U)$ has fibers $\pi^{-1}_n(x)$ of the form $[\gamma_-(u),\gamma_+(u)]$ for two continuous sections $\gamma_\pm : \pi_n(U) \to \pi_n(U) \times \mathbb{R}$. Given two $n$-framed patches $U$ and $V$, a *(partial) $n$-framed patch map* $F : U \to V$ is a (partial) continuous map which descends along $\pi_n$ to a (partial) $(n-1)$-framed patch map $F_{n-1} : \pi_n (U) \to \pi_n(V)$ such that mappings of fibers $F : \pi^{-1}_n(x) \to \pi^{-1}_n(F_{n-1}(x))$ are monotone.
\end{terminology}

Note that $n$-framed patches are [[compact]] and [[contractible]] spaces.

\begin{example} The standard example of an $n$-framed patch is the closed $n$-cube $\mathbf{I}^n = [-1,1]^n \subset \mathbb{R}^n$. However, in general $n$-framed patches need not be "$n$-dimensional": for instance, the $0$th slice $\{0\} \times \mathbf{I}^{n-1}$ of the $n$-cube is itself an $n$-framed patch, and so are the "$k$-directed intervals" $\mathbf{I}_k := \{0\}^{k-1} \times \mathbf{I} \times \{0\}^{n-k}$.
\end{example}

\begin{defn} Let $X$ be a topological space. Fix $n \in \mathbb{N}$.

* An *$n$-framed chart* $(U,\gamma)$ in $X$ is an embedding $\gamma : U \hookrightarrow \mathbb{R}^n$ of a subspace $U \subset X$ whose image $\im(\gamma)$ is an $n$-framed patch. 

* Two $n$-framed charts $(U,\gamma)$, $(V,\rho)$ in $X$ are *compatible* if  $\rho \circ \gamma^{-1}$ is a partial map of $n$-framed patches.

An **$n$-framed space** is a space $X$ endowed with an $n$-framing structure $\mathcal{A}$, which is an "atlas" of compatible $n$-framed charts $\{(U_i,\gamma_i)\}$ such that $U_i$ are a [[locally finite]] cover of $X$.
\end{defn}

\begin{rmk} The condition for covers to be locally finite is convenient as it describes the situation of locally finite [[cell complex|cell complexes]]. However, the condition could be replaced, and the definition generalized, in several ways. The above version of the definition should be considered a first approximation to a potentially more general notion of framed spaces.
\end{rmk}

Maps of framed spaces could be defined along the following lines.

\begin{defn} Given spaces with $n$-framing structure $(X,\mathcal{A}) \to (Y,\mathcal{B})$ then a **framed map** $F : X \to Y$ is a map such that for any charts $(U,\gamma) \in \mathcal{A}$ and $(V,\rho) \in \mathcal{B}$, $F$ yields a partial map $\rho \circ F \circ \gamma^{-1} : \mathrm{im}(\gamma) \to \mathrm{im}(\rho)$ of $n$-framed patches. 
\end{defn}

Framed spaces and framed maps are, in a sense, "very rigid" variants of directed spaces. Nonetheless, they are interesting to study as they turn out to have a rich [[framed combinatorial topology|combinatorial theory associated to them]]. This combinatorial counterpart is particular useful when translating between the topology of directed spaces and the combinatorics of higher categories: an example of this is the definition of [[manifold diagram|manifold diagrams]] in the language of framed spaces.

\begin{example} Realizations of [[geometric computad|geometric computads]] (resp. their functors) have the structure of framed spaces (resp. of framed maps), see [Dorn23](#Dorn23).
\end{example}

#### Comparison to $d$-spaces

\begin{rmk} One may want to define directed paths in an $n$-framed space as maps from "the framed interval" into that space: but, in fact, there are now $n$ different framed intervals, corresponding to the $n$ possible directions of $n$-framings. These are precisely modelled by the $n$-patches $\mathbf{I}_k$ mentioned in a previous example. Note, there is a framed bijection $\mathbf{I}_k \to \mathbf{I}_j$ if and only if $k \leq j$ (in particular, directions aren't interchangeable at all: analogously, note that in an [[n-category]] a $(n-k)$-morphisms can be (possibly degenerate) $(n-j)$-morphisms only if $k \leq j$). Given a framed space $(X,\mathcal{A})$, and defining $d_k X = \mathrm{Map}_{\mathrm{fr}}(\mathbf{I}_k, (X,\mathcal{A}))$, we thus obtain a filtration of directed paths:
\[
  d_n X \subset d_{n-1} X \subset ... \subset d_1 X \subset \Map(\mathbf{I},X)
\]
instead of a single path subset $dX \subset \Map(\mathbf{I},X)$, as required in the definition of $d$-spaces.
\end{rmk}

## Remarks

* If we can equip directed spaces with an internal hom, then a directed space with at least one directed path should be a strictly directed object in the category of directed spaces, with respect to the standard directed interval as the [[interval object]], while an ordinary topological space regarded as a directed space should be an [[undirected object]].

## Related concepts

* [[directed object]]

* [[directed homotopy theory]]

* [[directed homotopy type theory]]

## References

The above definition of $d$-spaces is from

* [[Marco Grandis]], _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))

This has now developed into a book

* [[Marco Grandis]], _[[Directed Algebraic Topology]], Models of non-reversible worlds_ , Cambridge University Press, 2009.

A discussion of reparameterization of directed paths in directed topological spaces is in

* Ulrich Fahrenberg and Martin Raussen, _Reparametrizations of Continuous Paths_ ([arXiv](http://arxiv.org/abs/0706.3560), ([blog](http://golem.ph.utexas.edu/category/2006/09/fahrenberg_and_raussen_on_cont.html)))

Further references are given in [[directed homotopy theory]].

* Emmanuel Haucourt, [_Streams, d-Spaces and Their Fundamental Categories_, Electronic Notes in Theoretical Computer Science, Volume 283, 15 June 2012, Pages 111-151](https://doi.org/10.1016/j.entcs.2012.05.008)

Some 'local combinatorial' aspects of framed spaces are discussed in:

* {#DornDouglas21} [[Christoph Dorn]] and [[Christopher Douglas]], _Framed combinatorial topology_, 2021 ([arXiv](https://arxiv.org/abs/2112.14700))

A global (higher-categorical) perspective on directed spaces is taken in:

* {#Dorn23} [[Christoph Dorn]], _Nine short stories about geometric higher categories_, 2023 ([pdf](https://cxdorn.github.io/assets/pdfs/nine-stories.pdf))

[[!redirects directed space]]
[[!redirects directed spaces]]

[[!redirects d-space]]
[[!redirects d-spaces]]
