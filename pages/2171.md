
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

\linebreak

## Definitions and characterizations
 {#DefinitionsAndCharacterizations}

* *[As the fundamental group of a configuration space of points](#AsFundamentalGroupOfConfigurationSpace)*

* *[Via generators and relations](#ByGeneratorsAndRelations)*

* *[As mapping class group of a punctured disk](#AsMappingClassGroupOfAPuncturedDisk)*

* *[As automorphisms of a free group](#AsAutomorphismsOfAFreeGroup)*

#### As fundamental group of a configuration space of points
 {#AsFundamentalGroupOfConfigurationSpace}

Geometrically, one may understand the group of braids in $\mathbb{R}^3$ as the [[fundamental group]] of the [[configuration space of points]] in the [[plane]] $\mathbb{R}^2$ (traditionally regarded as the [[complex plane]] $\mathbb{C}$ in this context, though the [[complex structure]] plays no role in the definition of the braid group as such).

(originally due to [Hurwitz 1891, §II](#Hurwitz1891), then re-discovered/re-vived in [Fadell & Neuwirth 1962, p. 118](#FadellNeuwirth62), [Fox & Neuwirth 1962, §7](#FoxNeuwirth62), review includes [Birman 1975, §1](#Birman75), [Williams 2020, pp. 9](#Williams20))


\linebreak


**In the plane**

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

\linebreak

**In general surfaces or graphs**
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


#### By generators and relations
 {#ByGeneratorsAndRelations}

The braid group as  a [[finitely generated group]]:

\begin{definition}\label{ArtinPresentation}
**(Artin presentation)**
\linebreak

The **Artin braid group**, $Br({n+1})$, on $n+1$ strands is the [[finitely generated group]] given via [[generators and relations]] by:

* generators: 

  \[
    \label{ArtinGenerators}
    b_i\;\; i = 1, \ldots, n
  \]

* relations: 

  \[
    \label{ArtinRelations}
    \begin{array}{ccccc}
    \underset{
      i+1 \lt j    
    }{\forall}
    &\;&
     b_i \cdot b_j 
     &=&  
     b_j \cdot b_i
    \\
    \underset{
      1 \leq i \lt n    
    }{\forall}
    &&
    b_i \cdot b_{i+1} \cdot b_i 
    &=&
    b_{i+1} \cdot b_i \cdot b_{i+1}
    \end{array}
  \]

\end{definition}


([Artin 1925, (5)-(6)](#Artin25); [Artin 1947, (18)-(19)](#Artin47);
review in, e.g.:  [Fox & Neuwirth 1962, §7](#FoxNeuwirth62))




#### As mapping class group of punctured disk
 {#AsMappingClassGroupOfAPuncturedDisk}


The braid group $Br(n)$ may be alternatively described as the [[mapping class group]] of a 2-disk $D^2$ with $n$ punctures. 

(review includes [Birman 1975, §4](#Birman75), [González-Meneses 2011, §1.4](#González-Meneses11))

Concretely, consider 

1. $D^2 \setminus \{z_1, \cdots, z_n\}$ 

   denoting the [[complement]] of $n$ distinct points in the [[closed disk]] (with [[boundary]] the [[circle]]);

1. $Homeo^{\partial}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)$ 

   denoting the [[mapping space]] of [[automorphism|auto]]-[[homeomorphisms]] which restrict to the [[identity]] on the [[boundary]] [[circle]], regarding with its canonical [[group]] structure;

1. $Homeo^{\partial}_id\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)$ 

   denoting the [[subgroup]] which is the [[connected component]] of the [[identity]].

Then the [[mapping class group]] is 

$$
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big)
  \;\coloneqq\;
  Homeo^{\partial}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)
  \Big/
  Homeo^{\partial}_{id}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)
  \,.
$$

Now observe that 

1. for the case that $n = 0$ this group is [[trivial group|trivial]], by *[[Alexander's trick]]*. 

1. continuous extension yields an [[injection]]

   $$
     Homeo^{\partial}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)
     \xhookrightarrow{\phantom{-}\iota\phantom{-}}
     Homeo^{\partial}\big(D^2\big)
     \,.
   $$

Combining this implies that for every $[\phi] \,\in\, MCG\big(D^2 \setminus \{z_1, \cdots, z_n\}big)$ therese is an [[isotopy]] of $\iota[\phi] \to id$ under which the locations of the punctures trace out a braid (in the sense of a [[loop]] in the symmetrized [[configuration space of points]]). This construction zields a morphism

and this is [[isomorphism|isomorphic]] to the braid group

$$
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big)
  \xrightarrow{\;\;\sim\;\;}
  Br(n) 
  \,.
$$

which is an [[isomorphism]].





#### As automorphisms of a free group
 {#AsAutomorphismsOfAFreeGroup}

Since the [[fundamental group]] of $D^2 \setminus \{z_1, \cdots, z_n\}$ is [[generalized the|the]]  [[free group]] of $n$ generators, the MCG-presentation of the braid group ([above](#InTermsOfAutomorphismsOfFreeGroups)) induces a [[group homomorphism]] of the braid group into the [[automorphism group]] of a [[free group]], which turns out to be [[faithful representation|faithful]].

This presentation is due to [Artin 1925, §6](#Artin25), review includes [González-Meneses 2011, §1.6](#González-Meneses11), see also pointer in [Bardakov 2005, p.  2](#Bardakov05).


More in detail, since the [[homotopy type]] of this punctured disk is, evidently, that of the the [[wedge sum]] of $n$ [[circles]], it follows that its [[fundamental group]] is is the [[free group]] $F_n$ on $n$ generators:

$$
  \pi_1
  \big(
    D^2 \setminus \{z_1, \cdots, z_ n\}
  \big)
  \;\simeq\;
  \pi_1
  \big(
    \vee_n S^1
  \big)
  \;\simeq\;
  F_n
  \,.
$$ 

Now the [[functor|functoriality]] of $\pi_1 \,\colon\, Top^{\ast/} \longrightarrow Grp$ implies we have an induced homomorphism 

$$
  Aut
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\} 
  \big)
  \longrightarrow 
  Aut
  \Big(
    \pi_1\big(
      D^2 \setminus \{z_1, \cdots, z_n\} 
    \big)
  \Big) 
  \,\simeq\, 
  Aut(F_n)
  \,.
$$ 

If such an automorphism $\phi$ of $D^2 \setminus \{z_1, \cdots, z_n\} $ is [[isotopy|isotopic]] to the [[identity]], then of course $\pi_1(\phi)$ is trivial, which means that the above homomorphism factors through the [[quotient group]] known as the [[mapping class group]]:

$$
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big) 
  \,=\, 
  Aut
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big)/Aut_0
  \big(
     D^2 \setminus \{z_1, \cdots, z_n\}  
  \big)
$$ 

Therefore, the above gives a homomorphism of the following form, which turns out to be a [[monomorphism]]:

$$
  Br(n) 
    \,=\, 
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big) 
  \xhookrightarrow{\phantom{--}} 
  Aut(F_n)
$$ 

\begin{imagefromfile}
    "file_name": "BraidActingOnFundamentalGroup-Artin1925.jpg",
    "width": 440,
    "float": "right",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [Artin 1925](#Artin25)"
\end{imagefromfile}



Explicitly, the generator $yb_i$ (eq:ArtinGenerators) in the Artin presentation(Def. \ref{ArtinPresentation}) is mapped to the automorphism $\sigma_i$ on the free group on $n$ generators $t_1, \ldots, t_n$ which is given as follows:

$$
  \sigma_i(t_j)
  \,=\,
  \left\{
  \begin{array}{lcl}
    t_{i+1} & \vert & j = i
    \\  
    t_{i+1}^{-1} \cdot t_i \cdot t_{i+1}
    & \vert & 
    j = i + 1
    \\
    t_j &\vert& \text{otherwise.}
  \end{array}
  \right.
$$

([Artin 1925, (24)](#Artin25))

\begin{imagefromfile}
    "file_name": "BraidActingOnFundamentalGroup-Gonzalez2011.jpg",
    "width": 540,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [González-Meneses 2011](#González-Meneses11)"
\end{imagefromfile}




\linebreak

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

* [[parenthesized braid operad]]

[[!include chord diagrams and weight systems -- table]]


## References

### General

The braid group regarded as the [[fundamental group]] of a [[configuration space of points]] is considered (neither of them under these names, though) already in:

* {#Hurwitz1891} [[Adolf Hurwitz]], §II of: *&Uuml;ber Riemann'sche Flächen mit gegebenen Verzweigungspunkten*, Mathematische Annalen **39** (1891) 1–60 &lbrack;[doi:10.1007/BF01199469](https://doi.org/10.1007/BF01199469)&rbrack;

there regarded as [[group action|acting]] on [[Riemann surfaces]] forming [[branched covers]], by movement of the branch points.

The original articles dedicated to analysis of the braid group:

* {#Artin25} [[Emil Artin]], *Theorie der Zöpfe*, Abh. Math. Semin. Univ. Hambg. **4**  (1925) 47–72 &lbrack;[doi;10.1007/BF02950718](https://doi.org/10.1007/BF02950718)&rbrack;

  >(the braid group via generators & relations and via automorphisms of free groups)

* [[Wilhelm Magnus]], *Über Automorphismen von Fundamentalgruppen berandeter Flächen*, Mathematische Annalen **109** (1934) 617–646 &lbrack;[doi:10.1007/BF01449158](https://doi.org/10.1007/BF01449158)&rbrack;

  > (the braid group as a [[mapping class group]])
    
* {#Artin47} [[Emil Artin]], *Theory of Braids*, Annals of Mathematics, Second Series, **48** 1 (1947) 101-126 &lbrack;[doi:10.2307/1969218](https://doi.org/10.2307/1969218)&rbrack;

* [[Frederic Bohnenblust]], *The Algebraical Braid Group*, Annals of Mathematics Second Series **48** 1 (1947) 127-136 &lbrack;[doi:10.2307/1969219](https://doi.org/10.2307/1969219)&rbrack;

* [[Wei-Liang Chow]], *On the Algebraical Braid Group*, Annals of Mathematics Second Series, **49** 3 (1948) 654-658 &lbrack;[doi:10.2307/1969050](https://doi.org/10.2307/1969050)&rbrack;

Survey of the early history:

* [[Michael Friedman]], *Mathematical formalization and diagrammatic reasoning: the case study of the braid group between 1925 and 1950*, British Journal for the History of Mathematics **34** 1 (2019) 43-59 &lbrack;[doi:10.1080/17498430.2018.1533298](https://doi.org/10.1080/17498430.2018.1533298)&rbrack;

The understanding of the braid group as the [[fundamental group]] of a [[configuration space of points]] was re-discovered/re-vived (after [Hurwitz 1891](#Hurwitz1891)) in:

* {#FoxNeuwirth62} [[Ralph H. Fox]], [[Lee Neuwirth]], *The braid groups*, Math. Scand. **10** (1962) 119-126 $[$[doi:10.7146/math.scand.a-10518](https://doi.org/10.7146/math.scand.a-10518), [pdf](https://www.mscand.dk/article/view/10518/8539), [MR150755](http://www.ams.org/mathscinet-getitem?mr=150755)$]$

* {#FadellNeuwirth62} [[Edward Fadell]], [[Lee Neuwirth]], *Configuration spaces*, Math. Scand. __10__ (1962) 111-118 $[$[doi:10.7146/math.scand.a-10517](https://doi.org/10.7146/math.scand.a-10517), [MR141126](http://www.ams.org/mathscinet-getitem?mr=141126)$]$

Textbook accounts:

* {#Birman75} [[Joan S. Birman]], _Braids, links, and mapping class groups_, Princeton Univ Press (1975) &lbrack;[preview pdf](https://api.pageplace.de/preview/DT0400.9781400881420_A26691398/preview-9781400881420_A26691398.pdf)&rbrack;

* [[Christian Kassel]], [[Vladimir Turaev]], _Braid Groups_, GTM **247** Springer Heidelberg 2008 ([doi:10.1007/978-0-387-68548-9](https://link.springer.com/book/10.1007/978-0-387-68548-9), [webpage](http://irma.math.unistra.fr/~kassel/Braids-bk.html))

Further introduction and review:

* [[Joan S. Birman]], [[Anatoly Libgober]] (eds.) *Braids*, Contemporary Mathematics **78** (1988) &lbrack;[doi:10.1090/conm/078](http://dx.doi.org/10.1090/conm/078)&rbrack;

* Joshua Lieber, *Introduction to Braid Groups*, 2011 ([pdf](https://math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Lieber.pdf))

* {#González-Meneses11} Juan González-Meneses, *Basic results on braid groups*, Annales Mathématiques Blaise Pascal, Tome 18 (2011) no. 1, pp. 15-59 ([ambp:AMBP_2011__18_1_15_0](https://ambp.centre-mersenne.org/item/?id=AMBP_2011__18_1_15_0))

* Alexander I. Suciu, He Wang, *The pure braid groups and their relatives*,  Perspectives in Lie theory, 403-426, Springer INdAM series, vol. 19, Springer, Cham, 2017 ([arXiv:1602.05291](https://arxiv.org/abs/1602.05291))

* Dale Rolfsen, *New developments in the theory of Artin’s braid groups* ([pdf](https://personal.math.ubc.ca/~rolfsen/papers/newbraid/newbraid2.pdf))

* {#Williams20} [[Lucas Williams]], *Configuration Spaces for the Working Undergraduate*,  Rose-Hulman Undergraduate Mathematics Journal, **21** 1 (2020) Article 8. ([arXiv:1911.11186](https://arxiv.org/abs/1911.11186), [rhumj:vol21/iss1/8](https://scholar.rose-hulman.edu/rhumj/vol21/iss1/8))

On the braid representation on [[automorphism group|automorphisms]] of [[free groups]]:

* [[Lluís Bacardit]], [[Warren Dicks]], *Actions of the braid group, and new algebraic proofs of results of Dehornoy and Larue*, Groups Complexity Cryptology **1** (2009) 77-129 &lbrack;[arXiv:0705.0587](https://arxiv.org/abs/0705.0587), [doi;10.1515/GCC.2009.77](https://doi.org/10.1515/GCC.2009.77)&rbrack;

* {#Bardakov05} [[Valerij G. Bardakov]], *Extending representations of braid groups to the automorphism groups of free groups*, Journal of Knot Theory and Its Ramifications **14** 08 (2005) 1087-1098 &lbrack;[arXiv:math/0408330](https://arxiv.org/abs/math/0408330), [doi:10.1142/S0218216505004251](https://doi.org/10.1142/S0218216505004251)&rbrack;

* Tetsuya Ito, *Actions of the $n$-strand braid groups on the free group of rank n which are similar to the Artin representation*, Quart. J. Math **66** (2015) 563-581 &lbrack;[arXiv;1406.2411](https://arxiv.org/abs/1406.2411), [doi:10.1093/qmath/hau033](https://doi.org/10.1093/qmath/hau033)&rbrack;


See also:

* Wikipedia: _[Braid group](http://en.wikipedia.org/wiki/Braid_group)_

On the [[group homology]] and [[group cohomology]] of braid groups:

* [[Vladimir Vershinin]], *Homology of Braid Groups and their Generalizations*, Banach Center Publications (1998) **42** 1 421-446 ([pdf](https://hopf.math.purdue.edu/Vershinin/hobr.pdf), [dml:208821](https://eudml.org/doc/208821))

Relation of [[automorphism groups]] of the [[profinite completion]] of braid groups to the [[Grothendieck-Teichmüller group]]:

* [[Pierre Lochak]], [[Leila Schneps]], *The Grothendieck-Teichmüller group and automorphisms of braid groups*, in: *The Grothendieck Theory of Dessins d’Enfant*, Cambridge University Press (1994, 2011) &lbrack;[pdf](https://webusers.imj-prg.fr/~leila.schneps/Fls.pdf), [doi:10.1017/CBO9780511569302](https://doi.org/10.1017/CBO9780511569302)&rbrack;


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

