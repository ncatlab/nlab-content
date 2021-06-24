
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _braid group_ $Br(n)$ is the [[group]] whose elements are [[isotopy]] classes of $n$ [[dimension|1-dimensional]] _braids_ running vertically in 3-dimensional [[Cartesian space]], the group operation being their concatenation.

Here a _braid_ with $n$ strands is thought of as $n$ pieces of string joining $n$ points at the top of the diagram with $n$-points at the bottom.



<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="169.27875"
   height="252.11273"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="3-braid.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
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
     inkscape:zoom="0.7"
     inkscape:cx="375"
     inkscape:cy="708.93575"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="640"
     inkscape:window-height="701"
     inkscape:window-x="0"
     inkscape:window-y="22">
    <inkscape:grid
       type="xygrid"
       id="grid2385"
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
     transform="translate(-116.64286,-131.85007)">
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.80512744px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 188.32014,243.16382 L 285.40892,298.64313 L 285.51904,383.56023 M 117.04542,132.25263 L 118.97101,201.55434 L 160.58048,229.294"
       id="path2383"
       sodipodi:nodetypes="cccccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.69349128px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 202.18997,132.20522 L 202.18997,215.42417 L 118.97101,298.64313 L 118.97101,381.86208"
       id="path2387" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.69349128px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 285.40892,215.42417 L 235.87382,262.97786 M 226.95752,274.86628 L 202.18997,298.64313 L 202.18997,381.86208 M 285.40892,132.20522 L 285.40892,215.42417"
       id="path2389"
       sodipodi:nodetypes="ccccccc" />
  </g>
</svg>


(This is a picture of a 3-strand braid.) 

We can transform / 'isotope' these braid diagrams just as we can transform [[knot diagrams]], again using [[Reidemeister moves]]. The 'isotopy' classes of braid diagrams form a group in which the composition is obtained by putting one diagram above another. 

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="162.66582"
   height="336.51199"
   id="svg2481"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="composition.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
  <defs
     id="defs2483">
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 526.18109 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_z="744.09448 : 526.18109 : 1"
       inkscape:persp3d-origin="372.04724 : 350.78739 : 1"
       id="perspective2489" />
    <inkscape:perspective
       id="perspective10"
       inkscape:persp3d-origin="372.04724 : 350.78739 : 1"
       inkscape:vp_z="744.09448 : 526.18109 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_x="0 : 526.18109 : 1"
       sodipodi:type="inkscape:persp3d" />
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
     inkscape:zoom="0.98994949"
     inkscape:cx="250.30935"
     inkscape:cy="631.41075"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="640"
     inkscape:window-height="701"
     inkscape:window-x="93"
     inkscape:window-y="22">
    <inkscape:grid
       type="xygrid"
       id="grid2557"
       visible="true"
       enabled="true" />
  </sodipodi:namedview>
  <metadata
     id="metadata2486">
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
     transform="translate(-117.83419,-176.3502)">
    <g
       transform="matrix(0.9585536,0,0,0.6593193,5.9599101,89.473516)"
       id="g2552"
       inkscape:label="Layer 1">
      <path
         sodipodi:nodetypes="cccccc"
         id="path2383"
         d="M 188.32014,243.16382 L 285.40892,298.64313 L 285.51904,383.56023 M 117.04542,132.25263 L 118.97101,201.55434 L 160.58048,229.294"
         style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.80512744px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1" />
      <path
         id="path2387"
         d="M 202.18997,132.20522 L 202.18997,215.42417 L 118.97101,298.64313 L 118.97101,381.86208"
         style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.69349128px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1" />
      <path
         sodipodi:nodetypes="ccccccc"
         id="path2389"
         d="M 285.40892,215.42417 L 235.87382,262.97786 M 226.95752,274.86628 L 202.18997,298.64313 L 202.18997,381.86208 M 285.40892,132.20522 L 285.40892,215.42417"
         style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.69349128px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1" />
    </g>
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 120,342.36218 L 120,382.36218 L 200,472.36218 L 200,512.36218"
       id="path2559" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 200,382.36218 L 168.98985,425.39264 M 156.96954,437.41295 L 120,472.36218 L 120,512.36218 M 200,342.36218 L 200,382.36218"
       id="path2561"
       sodipodi:nodetypes="ccccccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:1px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 280,342.36218 L 280,512.36218"
       id="path2563" />
  </g>
</svg>

The identity consists of $n$ vertical strings, so the inverse is obtained by turning a diagram upside down:

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="169.27875"
   height="252.11273"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="3-braid-inverse.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
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
     inkscape:zoom="0.7"
     inkscape:cx="141.43554"
     inkscape:cy="44.033213"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="640"
     inkscape:window-height="701"
     inkscape:window-x="0"
     inkscape:window-y="22">
    <inkscape:grid
       type="xygrid"
       id="grid2385"
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
     transform="translate(-116.64286,-131.85007)">
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.80512744px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 188.32014,272.64904 L 285.40892,217.16973 L 285.51904,132.25263 M 117.04542,383.56023 L 118.97101,314.25852 L 160.58048,286.51886"
       id="path2383"
       sodipodi:nodetypes="cccccc" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.69349128px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 202.18997,383.60764 L 202.18997,300.38869 L 118.97101,217.16973 L 118.97101,133.95078"
       id="path2387" />
    <path
       style="fill:none;fill-rule:evenodd;stroke:#000000;stroke-width:0.69349128px;stroke-linecap:butt;stroke-linejoin:miter;stroke-opacity:1"
       d="M 285.40892,300.38869 L 235.87382,252.835 M 226.95752,240.94658 L 202.18997,217.16973 L 202.18997,133.95078 M 285.40892,383.60764 L 285.40892,300.38869"
       id="path2389"
       sodipodi:nodetypes="ccccccc" />
  </g>
</svg>

This is the inverse of the first 3-braid we saw. 


There are useful [[group presentations]] of the braid groups.   We will return later to the interpretation of the [[generators and relations]] in terms of diagrams. 

## Definition

### Geometric definition 
 {#GeometricDefinition}

#### Ordinary braid group

Geometrically, one may understand the group of braids in $\mathbb{R}^3$ as the [[fundamental group]] of the [[configuration space of points]] in the [[plane]] $\mathbb{R}^2$ (traditionally regarded as the [[complex plane]] $\mathbb{C}$ in this context, though the [[complex structure]] plays no role in the definition of the braid group).

We say this in more detail:

Let $C_n \hookrightarrow \mathbb{C}^n$ denote the space of [[configuration space of points|configurations of n ordered  points]] in the [[complex plane]], whose elements are those [[n-tuples]] $(z_1, \ldots, z_n)$ such that $z_i \neq z_j$ whenever $i \neq j$. In other words, $C_n$ is the [[complement]] of the [[fat diagonal]]:

$$
  C_n 
    \;\coloneqq\; 
  \mathbb{C}^n \setminus \mathbf{\Delta}^n_{\mathbb{C}}
  \,.
$$


The [[symmetric group]] $S_n$ [[group action|acts]] on $C_n$ by [[permutation|permuting]] coordinates. Let:

* $C_n/S_n$  denote the [[quotient]] by this group action, hence the [[orbit]] space (the space of $n$-element subsets of $\mathbb{C}$ if one likes), 

* $[z_1, \ldots, z_n]$ denote the image of $(z_1, \ldots, z_n)$ under the quotient [[coprojection]] $\pi \colon C_n \to C_n/S_n$ (i.e. its the [[equivalence class]]). 

We understand $p = (1, 2, \ldots, n)$ as the basepoint for $C_n$, and $[p] = [1, 2, \ldots n]$ as the basepoint for the [[configuration space of unordered points]] $C_n/S_n$, making it a [[pointed topological space]].

+-- {: .num_defn} 
###### Definition 

The _braid group_ is the [[fundamental group]] of the [[configuration space of unordered points|configuration space of n unordered points]]:

$$
  Br(n) 
    \;\coloneqq\; 
  \pi_1
  \big(
    C_n/S_n, [p]
  \big)
$$

The _pure braid group_  is the [[fundamental group]] of the [[configuration space of ordered points|configuration space of n ordered points]]: 

$$
  PBr(n)
    \;\coloneqq\;
  \pi_1
  \big(
    C_n, p 
  \big)
  \,.
$$

=-- 

Evidently a braid $\beta$ is represented by a path $\alpha: I \to C_n/S_n$ with $\alpha(0) = [p] = \alpha(1)$. Such a path may be uniquely lifted through the [[covering]] projection $\pi: C_n \to C_n/S_n$ to a path $\tilde{\alpha}$ such that $\tilde{\alpha}(0) = p$. The end of the path $\tilde{\alpha}(1)$ has the same underlying subset as $p$ but with coordinates permuted: $\tilde{\alpha}(1) = (\sigma(1), \sigma(2), \ldots, \sigma(n))$. Thus the braid $\beta$ is exhibited by $n$ non-intersecting strands, each one connecting an $i$ to $\sigma(i)$, and we have a map $\beta \mapsto \sigma$ appearing as the quotient map of an exact sequence 

$$1 \to PBr(n) \to Br(n) \to Sym(n) \to 1$$ 

which is part of a [[long exact sequence of homotopy groups|long exact homotopy sequence]] corresponding to the [[fibration]] $\pi \colon C_n \to C_n/S_n$. 

#### For general topological base spaces
 {#ForMoreGeneralTopologicalSpaces}

Since the notion of a [[configuration space of points]] makes sense for points in any [[topological space]], not necessarily the [[plane]] $\mathbb{R}^2$, the [above](#GeometricDefinition) geometric definition has an immediate generalization:

For $\Sigma$ any [[surface]], the [[fundamental group]] of the (ordered) [[configuration space of points]] in $\Sigma$ may be regarded as generalized (pure) braid group.
These *surface braid groups are of interest in [[3d topological field theory]] and in particular in [[topological quantum computation]] where it models [[non-abelian anyons]].


Yet more generally, one may consider the fundamental group of the configuration space of points of any topological space $X$.

For example for $X$ a 1-dimensional [[CW-complex]], hence an ([[undirected graph|undirected]]) [[graph]], one speaks of *graph braid groups* (e.g. [Farley & Sabalka 2009](#FarleySabalka2009)).

> The following should maybe not be here in the Definition-section, but in some Properties- or Examples-section, or maybe in a dedicated entry on *[[graph braid groups]]*:

It has been shown ([An & Maciazek 2006](#AnMaciazek2006), using discrete [[Morse theory]] and combinatorial analysis of small graphs) that graph braid groups are generated by particular particle moves with the following description:

1. Star-type generators: exchanges of particle pairs on vertices of the particular graph

2. loop type generators: circular moves of a single particle around a simple cycle of the graph

\linebreak


### Group-theoretic definition

#### Artin presentation

The **Artin braid group**, $Br({n+1})$, defined using $n+1$ strands is a [[group]] given by 

* generators: $y_i$, $i = 1, \ldots, n$;

* relations: 

  * $r_{i,j} \equiv y_i y_j y_i^{-1} y_j^{-1}$ for $i+1 \lt j$

  * $r_{i,i+1}\equiv y_i y_{i+1} y_i y_{i+1}^{-1} y_i^{-1} y_{i+1}^{-1}$ for $1 \leq i \lt n$. 

#### In terms of automorphisms on free groups 

The braid group $Br(n)$ may be alternatively described as the [[mapping class group]] of a 2-disk $D^2$ with $n$ punctures (call it $X_n$). Meanwhile, the [[fundamental group]] $\pi_1(X_n)$ (with basepoint on the boundary) is a [[free group]] $F_n$ on $n$ generators; the functoriality of $\pi_1$ implies we have an induced homomorphism 

$$Aut(X_n) \to Aut(\pi_1(X_n)) = Aut(F_n).$$ 

If an automorphism $\phi: X_n \to X_n$ is isotopic to the identity, then of course $\pi_1(\phi)$ is trivial, and so the homomorphism factors through the quotient $MCG(X_n) = Aut(X_n)/Aut_0(X)$, so we get a homomorphism 

$$Br(n) = MCG(X_n) \to Aut(F_n)$$ 

and this turns out to be an injection. 

Explicitly, the generator $y_i$ used in the Artin presentation above is mapped to the automorphism $\sigma_i$ on the free group on $n$ generators $x_1, \ldots, x_n$ defined by 

$$\sigma_i(x_i) = x_{i+1}, \sigma_i(x_{i+1}) = x_{i+1}^{-1} x_i x_{i+1}, \; \else\; \sigma(x_j) = x_j.$$ 

## Properties

### Relation to moduli space of monopoles

+-- {: .num_prop #ModuliSpaceOfkMonopolesStablyWeakHomotopyEquivbalentToClassifyingSpaceOfBraids}
###### Proposition
**([[moduli space of monopoles]] is [[stable weak homotopy equivalence|stably weak homotopy equivalent]] to [[classifying space]] of [[braid group]])**

For $k \in \mathbb{N}$ there is a [[stable weak homotopy equivalence]] between the [[moduli space of k monopoles]] (eq:ModuliSpaceOfkInstantons) and the [[classifying space]] of the [[braid group]] $Br({2k})$ on $2 k$ strands:

$$
  \Sigma^\infty \mathcal{M}_k
  \;\simeq\;
  \Sigma^\infty Br({2k})
$$

=--

([Cohen-Cohen-Mann-Milgram 91](#CohenCohenMannMilgram91))


## Examples
 {#Examples}

The first few examples of the braid group $Br(n)$ for low values of $n$:

\begin{example}
The group $Br(1)$ has no generators and no relations, so is the [[trivial group]]:
$$
  Br(1) \;\simeq\; 1  
  \,.
$$

\end{example}

\begin{example}
The group $Br(2)$ has one generator and no relations, so is the infinite cyclic group of [[integers]]:
$$
  Br(2) \;\simeq\; \mathbb{Z}
  \,.
$$
\end{example}


\begin{example}\label{TheBraidgroupBr3}
The group $Br(3)$ (we will simplify notation writing $u = y_1$, $v = y_2$)
has presentation 

$$
  Br(3)
  \;\simeq\;
  \mathcal{P} 
  \coloneqq 
  \big( 
     u,v : r \equiv u v u v^{-1} u^{-1} v^{-1}
  \big).
$$

This is also known as the "trefoil [[knot group]]", i.e., the [[fundamental group]] of the [[complement]] of a [[trefoil knot]]. 
\end{example}

\begin{example}
The group $Br(4)$ (simplifying notation as [before](#TheBraidgroupBr3)) has generators $u,v,w$ and relations:

 *  $r_u \equiv  v w v w^{-1} v^{-1} w^{-1}$,
 *  $r_v \equiv  u w u^{-1} w^{-1}$,
 *  $r_w \equiv  u v u v^{-1} u^{-1} v^{-1}$.

\end{example}

\begin{example}\label{HurwitzBraidGroup}
The **Hurwitz braid group** (or **sphere braid group**) is the [surface braid group](#ForMoreGeneralTopologicalSpaces) for $\Sigma$ the [[2-sphere]] $S^2$.  Algebraically, the Hurwitz braid group $H_{n+1}$ has all of the generators and relations of the Artin braid group $Br({n+1})$, plus one additional relation:

$$ 
  y_1 y_2 \dots y_{n-1} y_n^2 y_{n-1}\dots y_2 y_1
$$
\end{example}


## Related entries

* [[braid representation]]

* [[braid group statistics]]

  [[anyons]], [[quantum Hall effect]]

  [[topological quantum computation]]

* [braid group cryptography](cryptography#BraidGroupCryptographyReferences)

* [[braid category]]

* [[infinitesimal braid relation]]

* [[loop braid group]]

[[!include chord diagrams and weight systems -- table]]


## References

### General

Classical references:

* [[Joan S. Birman]], _Braids, links, and mapping class groups_, Princeton Univ Press, 1974.

* [[R. H. Fox]], L. Neuwirth, _The braid groups_, Math. Scand. __10__ (1962) pp.119-126. [pdf](http://www.mscand.dk/article.php?id=1624), [MR150755](http://www.ams.org/mathscinet-getitem?mr=150755)

Textbook accounts:

* [[Christian Kassel]], [[Vladimir Turaev]], _Braid Groups_, GTM **247** Springer Heidelberg 2008 ([doi:10.1007/978-0-387-68548-9](https://link.springer.com/book/10.1007/978-0-387-68548-9), [webpage](http://irma.math.unistra.fr/~kassel/Braids-bk.html))

See also:

* Wikipedia: _[Braid group](http://en.wikipedia.org/wiki/Braid_group)_

* Joshua Lieber, *Introduction to Braid Groups*, 2011 ([pdf](https://math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Lieber.pdf))

* Juan González-Meneses, *Basic results on braid groups*, Annales Mathématiques Blaise Pascal, Tome 18 (2011) no. 1, pp. 15-59 ([ambp:AMBP_2011__18_1_15_0](https://ambp.centre-mersenne.org/item/?id=AMBP_2011__18_1_15_0))

* Alexander I. Suciu, He Wang, *The pure braid groups and their relatives*,  Perspectives in Lie theory, 403-426, Springer INdAM series, vol. 19, Springer, Cham, 2017 ([arXiv:1602.05291](https://arxiv.org/abs/1602.05291))


On the [[group homology]] and [[group cohomology]] of braid groups:

* [[Vladimir Vershinin]], *Homology of Braid Groups and their Generalizations*, Banach Center Publications (1998) **42** 1 421-446 ([pdf](https://hopf.math.purdue.edu/Vershinin/hobr.pdf), [dml:208821](https://eudml.org/doc/208821))

For orderings of the braid group see

* [[Patrick Dehornoy]], _Braid groups and left distributive operations_ , Transactions AMS **345** no.1 (1994) pp.115&#8211;150.

* H. Langmaack, _Verbandstheoretische Einbettung von Klassen unwesentlich verschiedener Ableitungen in die Zopfgruppe_ , Computing **7** no.3-4 (1971) pp.293-310.

On geometric presentations of braid groups:

* An, Byung Hee and Maciazek, Tomasz, Geometric Presentations of Braid Groups for Particles on a Graph, Communications in Mathematical Physics (2021) volume 384, pp. 1109-1140,(http://dx.doi.org/10.1007/s00220-021-04095-x)  


[[!include braid group representations -- references]]



### Graph braid groups
  {#ReferencesGraphBraidGroups}

* {#FarleySabalka2009} Daniel Farley, Lucas Sabalka, *Presentations of Graph Braid Groups* ([arXiv:0907.2730](https://arxiv.org/abs/0907.2730))

* Ki Hyoung Ko, Hyo Won Park,  *Characteristics of graph braid groups* ([arXiv:1101.2648](https://arxiv.org/abs/1101.2648))

* {#AnMaciazek2006} Byung Hee An, Tomasz Maciazek, *Geometric presentations of braid groups for particles on a graph* ([arXiv:2006.15256](https://arxiv.org/abs/2006.15256))



### Relation to moduli space of monopoles

On [[moduli spaces of monopoles]] related to [[braid groups]]:

* [[Fred Cohen]], [[Ralph Cohen]], B. M. Mann, R. J. Milgram, _The topology of rational functions and divisors of surfaces_, Acta Math (1991) 166: 163 ([doi:10.1007/BF02398886](https://doi.org/10.1007/BF02398886))

* [[Ralph Cohen]], John D. S. Jones  _Monopoles, braid groups, and the Dirac operator_, Comm. Math. Phys. Volume 158, Number 2 (1993), 241-266 ([euclid:cmp/1104254240](https://projecteuclid.org/euclid.cmp/1104254240))



[[!include braid group cryptography -- references]]


category: knot theory

[[!redirects braid groups]]

[[!redirects braid]]
[[!redirects braids]]

[[!redirects pure braid]]
[[!redirects pure braids]]

[[!redirects pure braid group]]
[[!redirects pure braid groups]]


[[!redirects Artin braid group]]
[[!redirects Hurwitz braid group]]

[[!redirects surface braid group]]
[[!redirects surface braid groups]]

