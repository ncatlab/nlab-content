
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Manifolds and Cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
#### Functorial Quantum Field Theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

$n$-Dimensional [[manifolds]] (possibly and usually equipped with certain structure, notably for instance with [[orientation]], [[framing]]-structure or more general [[G-structure]]) should naturally form an [[(∞,n)-category]] of [[extended cobordisms]] whose

* [[objects]] are 0-dimensional (oriented) manifolds (disjoint unions of (oriented) points);

* 1-[[morphisms]] are (oriented) [[cobordisms]] between disjoint unions of (oriented) points;

* 2-morphisms are cobordisms between 1-dimensional cobordisms

* etc.

* (n+1)-morphisms are _diffeomorphisms_ between $n$-dimensional cobordisms;

* (n+2)-morphisms are smooth homotopies of these;

* etc.

The $(\infinity,n)$-category of cobordisms is the subject of the [[cobordism hypothesis]].


## Definition

### As an $n$-fold complete Segal space

Here is an outline of the idea of the definition of 
$Bord_{(\infty,n)}$ as given in ([Lurie](#LurieQFT)) where the main point, apart from the [[(∞,n)-category]] machinery in the background, is definition 2.2.9.

The idea is to start with thinking of $n$-dimensional cobordisms as forming something like an [[n-fold category]] by simply saying that the collection of composites of cobordisms is given by big cobordisms with markings on them, indicating where we think of them as being composed.

Let's first do this for composition in one direction, as in an ordinary 1-category of $n$-dimensional cobordisms.

consider a [[manifold]] $X \hookrightarrow V \times \mathbb{R}$ embedded in a [[vector space]] of the form $V \times \mathbb{R}$. We can think of this as a manifold canonically equipped with a coordinate function $\phi : X \hookrightarrow V \times \mathbb{R} \to \mathbb{R}$ that measures the "height" or maybe better the "length" of the embedded manifold. 

We can pick a bunch of numbers $\{t_j \in \mathbb{R}\}$ and think of these as marking a bunch of slices of $X$, the preimages $\phi^{-1}(t_j)$. We can think of these slices as being the $(n-1)$-dimensional boundary manifolds at which a sequence of manifolds have been glued together to produce $X$. 

> (there is an obvious picture to be drawn and uploaded here, maybe somebody finds the time and energy)

In this way an embedded manifold $X \hookrightarrow V \times \mathbb{R} $ and a set of $k$-numbers $\{t_i\}$ may represent an element in the space of sequences of composable cobordisms. To make this work as expected, the markings on $X$ may not be too irregular, so we should impose some conditions on what qualifies as a marked manifold. The precise statement is given further below.

The collection of these tuples, consisting of an embedded manifold $X \hookrightarrow V \times \mathbb{R}$ and a collection of $k$ numbers $\{t_i \in \mathbb{R}\}$ naturally form a [[simplicial set]], which is like the [[nerve]] of the 1-category of $n$-dimensional cobordisms under composition in one direction.

To generalize this from just a 1-categorical structure to an $n$-categorical structure, we simply take a manifold $X$ as before, but now draw markings on it in $n$ transversal directions, thereby putting a kind of grid on it that subdivides the manifold into cubical slices. A manifold with such subdivision on it may then be regarded as giving an element in the space of $n$-dimensional pasting diagrams in an $n$-fold category.

To formalize this more general case, we embed $X$ not just into a $V \times \mathbb{R}$, but a $V \times \mathbb{R}^n$. This then provides us with $n$ different coordinate functions $\phi_i : X \hookrightarrow V \times \mathbb{R}^n \stackrel{p_i}{\to} \mathbb{R}$ on $X$, each running along one of the directions in which we may think of $X$ as having been glued from smaller manifolds.

A collection of markings indicating such gluing is now a collection of numbers $\{t_j^1\}, \;\{t_j^2\}, \; \cdots \{t_j^n\}$, one for each of these directions.

For each direction this yields a [[simplicial set]] of such structures, to be thought of as the [[nerve]] of the category of cobordisms under composition in one of these directions. Taken together this is an $n$-fold simplicial set

$$
  \Delta^{op} \times \Delta^{op} \times \cdots \times \Delta^{op}
  \to Set
$$

which is like the nerve of an $n$-fold category of cobordisms. 

When suitable regularity conditions are imposed on this data, there is naturally a [[topology]] on each of these sets of embedded marked cobordisms, that makes this into an $n$-fold simplicial [[topological space]]

$$
  \Delta^{op} \times \Delta^{op} \times \cdots \times \Delta^{op}
  \to Top
  \,.
$$

To get rid of the dependence of this construction on $V$, we can let $V$ "grow arbitrarily large" by taking the [[colimit]] of the above $n$-fold cosimplicial spaces as $V$ ranges over the finite dimensional subspaces of $\mathbb{R}^\infty$.

The resulting $n$-fold simplicial topological space obtained by this colimit then is essentially the [[(∞,n)-category]] $Bord_n$ that we are after. It turns out that it actually is an $n$-fold Segal space. We just formally _complete_ it to an [[n-fold complete Segal space]]

$$
  Bord_n : (\Delta^{op})^n \to Top
  \,.
$$

This, then, is a model for the [[(∞,n)-category]] of extended $n$-dimensional cobordisms.

### As a blob $n$-category

There is a definition of a [[blob n-category]] of $n$-cobordisms. See there for more details.

## Examples

### $Bord_2^{fr}$
 {#Framed2Bordisms}

Some comments on 2-[[framed manifold|framed]] 2-cobordisms.

Consider the pictures in ([Schommer-Pries 13, figure 5](#SchommerPries13)).

<svg width="640" height="480" xmlns="http://www.w3.org/2000/svg" xmlns:svg="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink" se:nonce="7480">
 <g>
  <title>Layer 1</title>
  <use id="svg_7480_62" xlink:href="#svg_7480_61" transform="matrix(0.930341, 0, 0, 1.0136, -84.7055, -144.561)" y="0" x="0"/>
  <g id="svg_7480_63"/>
 </g>
 <defs>
  <symbol xmlns:svg="http://www.w3.org/2000/svg" xmlns="http://www.w3.org/2000/svg" id="svg_7480_61">
   <defs>
    <marker orient="auto" refY="0" refX="0" id="svg_7480_46">
     <path id="svg_7480_60" d="m0,0l5,-5l-17.5,5l17.5,5l-5,-5z" transform="scale(0.2) rotate(180) translate(6,0)" stroke-width="1.0pt" stroke="#000000" fill-rule="evenodd"/>
    </marker>
    <marker orient="auto" refY="0" refX="0" id="svg_7480_47">
     <path id="svg_7480_59" d="m-2.5,-1c0,2.76 -2.24,5 -5,5c-2.76,0 -5,-2.24 -5,-5c0,-2.76 2.24,-5 5,-5c2.76,0 5,2.24 5,5z" transform="scale(0.4) translate(7.4, 1)" stroke-width="1.0pt" stroke="#000000" fill-rule="evenodd"/>
    </marker>
   </defs>
   <metadata id="svg_7480_54">image/svg+xml</metadata>
   <g id="svg_7480_3">
    <g id="svg_7480_50" transform="translate(-12,101)">
     <path d="m199.964645,94.862167a24.964653,23.464651 0 1 1 -49.929306,0a24.964653,23.464651 0 1 1 49.929306,0z" id="svg_7480_53" stroke-dashoffset="0" stroke-dasharray="1.868, 1.868" stroke-miterlimit="4" stroke-width="0.934" stroke="#000000" fill-opacity="0" fill="#ffffff"/>
     <rect y="94.81481" x="175.18947" height="23.08421" width="8.23158" id="svg_7480_52" stroke-dashoffset="0" stroke-opacity="0" stroke-miterlimit="4" stroke="#000000" fill="#808080"/>
     <path id="svg_7480_51" d="m175,94.362183l0,22" marker-end="url(#svg_7480_46)" marker-mid="none" marker-start="url(#svg_7480_47)" stroke-miterlimit="4" stroke-width="2" stroke="#000000" fill="none"/>
    </g>
    <g id="svg_7480_44" transform="matrix(-1,0,0,1,435.2421,100.07368)">
     <path id="svg_7480_49" d="m199.964645,94.862167c0,12.959183 -11.177048,23.464653 -24.964645,23.464653c-13.787598,0 -24.964661,-10.50547 -24.964661,-23.464653c0,-12.959167 11.177063,-23.464653 24.964661,-23.464653c13.787598,0 24.964645,10.505486 24.964645,23.464653z" stroke-dashoffset="0" stroke-dasharray="1.868, 1.868" stroke-miterlimit="4" stroke-width="0.934" stroke="#000000" fill-opacity="0" fill="#ffffff"/>
     <rect id="svg_7480_48" width="8.23158" height="23.08421" x="175.18947" y="94.81481" stroke-dashoffset="0" stroke-opacity="0" stroke-miterlimit="4" stroke="#000000" fill="#808080"/>
     <path d="m175,94.362183l0,22" id="svg_7480_45" marker-end="url(#svg_7480_46)" marker-mid="none" marker-start="url(#svg_7480_47)" stroke-miterlimit="4" stroke-width="2" stroke="#000000" fill="none"/>
    </g>
    <g id="svg_7480_41" transform="translate(-14,63)">
     <path d="m365,129.290497a39,-39 0 0 1 78,0" id="svg_7480_43" marker-mid="none" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.5" stroke="#000000" fill="#808080"/>
     <path d="m370.690063,129.258896a33.369053,-33.569511 0 0 1 66.738129,0" id="svg_7480_42" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.5" stroke="#ffffff" fill="#ffffff"/>
    </g>
    <g id="svg_7480_38" transform="translate(-31,59)">
     <path id="svg_7480_40" d="m498,162.290482a39,39 0 0 1 78,0" marker-mid="none" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.5" stroke="#808080" fill="#808080"/>
     <path id="svg_7480_39" d="m503.690094,162.322098a33.369053,33.569511 0 0 1 66.738068,0" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.4998" stroke="#000000" fill="#ffffff"/>
    </g>
    <g id="svg_7480_35" transform="translate(27,5)">
     <path id="svg_7480_37" d="m86,358.290497a39,39 0 0 1 78,0" marker-mid="none" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.5" stroke="#000000" fill="#808080"/>
     <path id="svg_7480_36" d="m91.690086,358.322083a33.369053,33.569511 0 0 1 66.738106,0" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.5" stroke="#ffffff" fill="#ffffff"/>
    </g>
    <g id="svg_7480_32" transform="translate(-9,4)">
     <path d="m328,354.362183a36,36 0 1 1 -72,0a36,36 0 1 1 72,0z" id="svg_7480_34" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.414" stroke="#000000" fill="#808080"/>
     <path d="m323,354.862183a31.5,31.5 0 1 1 -63,0a31.5,31.5 0 1 1 63,0z" id="svg_7480_33" stroke-dashoffset="0" stroke-opacity="0" stroke-miterlimit="4" stroke-width="1.414" stroke="#000000" fill="#c0c0c0"/>
    </g>
    <g id="svg_7480_25">
     <rect y="309.36218" x="372.52603" height="105" width="78.78863" id="svg_7480_31" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.44958" stroke="#000000" fill="#808080"/>
     <rect y="313.36218" x="377.32037" height="101" width="69.67963" id="svg_7480_30" stroke-dashoffset="0" stroke-opacity="0" stroke-miterlimit="4" stroke-width="1.51841" stroke="#000000" fill="#c0c0c0"/>
     <path id="svg_7480_29" d="m373,305.290497a39,-39 0 0 1 78,0" marker-mid="none" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.5" stroke="#000000" fill="#808080"/>
     <path id="svg_7480_28" d="m378.690063,305.258881a33.369053,-33.569511 0 0 1 66.738129,0" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.5" stroke="#ffffff" fill="#ffffff"/>
     <path d="m373,414.290497a39,39 0 0 1 78,0" id="svg_7480_27" marker-mid="none" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.5" stroke="#000000" fill="#808080"/>
     <path d="m378.525238,415.168091a33.369053,33.569511 0 0 1 66.738098,0" id="svg_7480_26" stroke-dashoffset="0" stroke-miterlimit="4" stroke-width="1.5" stroke="#ffffff" fill="#ffffff"/>
    </g>
    <g id="svg_7480_22" transform="translate(-75,21)">
     <path d="m582.086975,292.202759c0,56.055511 24.304321,26.768127 24.304321,58.768127c0,32 42.562134,26.206329 43.217407,6.072449c0.132996,-4.085205 0.519775,-19.290985 0.681152,-30.927521c0.463806,-33.434784 -42.666626,-28.594208 -43.666626,-6.594208c-0.048645,32.260468 -27.985168,19.793762 -26,54.072449c0.463745,17.608704 -0.231934,18.536255 -0.231934,18.536255" id="svg_7480_24" stroke-miterlimit="4" stroke-width="3" stroke="#808080" fill="none"/>
     <path id="svg_7480_23" d="m580,293.362183c0.231873,54.432312 25.231873,27.695648 25,59c-0.237,31.999115 45.911865,24.546478 46,7c0.045715,-9.102478 0.681152,-20.217407 0.913025,-31.855072c0.776978,-38.992249 -45.913025,-31.144928 -46.913025,-9.144928c-0.048584,32.260468 -27.985168,20.721313 -26,55c0,19 0,19 0,19" stroke-width="1px" stroke="#000000" fill="none"/>
    </g>
    <text xml:space="preserve" x="126" y="236.36218" id="svg_7480_20" font-family="Bitstream Vera Sans" fill="#000000" font-weight="normal" font-style="normal" font-size="16px">
     <tspan id="svg_7480_21" x="126" y="236.36218">positive point</tspan>
    </text>
    <text xml:space="preserve" x="186" y="271.36218" id="svg_7480_18" font-family="Bitstream Vera Sans" fill="#000000" font-weight="normal" font-style="normal" font-size="16px">
     <tspan id="svg_7480_19" x="186" y="271.36218">negative point</tspan>
    </text>
    <text xml:space="preserve" x="352" y="270.36218" id="svg_7480_16" font-family="Bitstream Vera Sans" fill="#000000" font-weight="normal" font-style="normal" font-size="16px">
     <tspan x="352" y="270.36218" id="svg_7480_17">ev: pt+ u pt- -> 0</tspan>
    </text>
    <text xml:space="preserve" x="569" y="248.36218" id="svg_7480_14" font-family="Bitstream Vera Sans" fill="#000000" font-weight="normal" font-style="normal" font-size="16px">
     <tspan id="svg_7480_15" x="569" y="248.36218">coev</tspan>
    </text>
    <text xml:space="preserve" x="131" y="406.36218" id="svg_7480_12" font-family="Bitstream Vera Sans" fill="#000000" font-weight="normal" font-style="normal" font-size="16px">
     <tspan id="svg_7480_13" x="131" y="406.36218">ev^R</tspan>
    </text>
    <text xml:space="preserve" x="269" y="440.36218" id="svg_7480_9" font-family="Bitstream Vera Sans" fill="#000000" font-weight="normal" font-style="normal" font-size="16px">
     <tspan id="svg_7480_11" x="269" y="440.36218">&#949;</tspan>
     <tspan x="269" y="460.36218" id="svg_7480_10"/>
    </text>
    <text xml:space="preserve" x="405" y="441.36218" id="svg_7480_6" font-family="Bitstream Vera Sans" fill="#000000" font-weight="normal" font-style="normal" font-size="16px">
     <tspan id="svg_7480_8" x="405" y="441.36218">&#951;</tspan>
     <tspan x="405" y="461.36218" id="svg_7480_7"/>
    </text>
    <text xml:space="preserve" x="482" y="433.36218" id="svg_7480_4" font-family="Bitstream Vera Sans" fill="#000000" font-weight="normal" font-style="normal" font-size="16px">
     <tspan x="482" y="433.36218" id="svg_7480_5">Serre automorphism</tspan>
    </text>
   </g>
   <g id="svg_7480_2"/>
  </symbol>
 </defs>
</svg>

> Somebody should produce pictures like this here...
>> Well, it worked in the preview; a little help?

Let $\gamma$ be a 1-dimensional manifold of the form of the interval $[0,1]$. A 2-[[framing]] of $\gamma$ is a trivialization of $T\gamma \oplus \mathbb{R}$. Let $\{1\} \subset \mathbb{R}$ be the canonical [[basis]] of $\mathbb{R}$. If we think of the plane $\mathbb{R}^2$ as equipped with its canonical 2-framing, then a 2-framing of $\gamma$ is induced by embedding $\gamma$ into the plane and shading one of its two sides. This identifies at each point  $x \in \gamma$ the tangent space to $\gamma$ at that point with the tangent vector to the embedding of $\gamma$ as a vector in $\mathbb{R}^2$ and identifies $1\in \mathbb{R}$ with the vector in $\mathbb{R}^2$ orthogonal to this tangent vector and pointing into the shaded region.

This shows that if $\gamma$ is regarded with its two endpoints both as incoming or both as outgoing, then the induced 2-framing of these endpoints is opposite to each other. This way such an arc is a morphism from the union of the "positive point" and the "negative point" to the empty 0-manifold, hence is a unit/counit exhibiting these as [[dual objects]].




## Properties 
 {#Properties}

### Adjoints

$Bord_n$ is an [[(∞,n)-category with all adjoints]].

### Relation to Thom spectrum

For $n \to \infty$ we have that $Bord_{(\infty,\infty)}$ is the [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[∞-groupoid]] ($\simeq$ [[infinite loop space]]) $\Omega^\infty M O$ that underlies the [[Thom spectrum]].

Its [[homotopy group]]s are the [[cobordism ring]]s

$$
  \pi_n Bord_{(\infty,\infty)} \simeq \Omega_n
  \,.
$$

Therefore a symmetric monoidal  $\infty$-functor

$$
  Bord_{(\infty,\infty)} \to S
$$

to some symmetric monoidal $\infty$-groupoid $S$ is a [[genus]].

## Related concepts

* [[cobordism]], [[extended cobordism]]

* [[category of cobordisms]]

* **(∞,n)-category of cobordisms**

* [[cobordism hypothesis]]


## References

### General

A specific realization of this idea in terms of [[(∞,n)-category]] modeled as [[n-fold complete Segal space]] is in (definition 2.2.9, page 36)

*  {#LurieQFT} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

* [[Jacob Lurie]], [Video Stream](http://www.youtube.com/watch?v=Bo8GNfN-Xn4)

In that article a proof of the [[cobordism hypothesis]] is indicated. A review is in 

* [[Julie Bergner]], _Models for $(\infty,n)$-Categories and the Cobordism Hypothesis_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Available [on the arxiv](http://arxiv.org/abs/1011.0110). 

Other discussions of higher categories of cobordisms are

* [[Marco Grandis]], _[[Cospans in Algebraic Topology]]_

* [[Eugenia Cheng]] and [[Nick Gurski]], _Toward an $n$-category of cobordisms_ , Theory and Applications of Categories 18 (2007), 274-302. ([tac](http://www.tac.mta.ca/tac/volumes/18/10/18-10abs.html))


### In dimension 2

A detailed construction of the [[(n,r)-category|(2,2)-category]] of 2-dimensional cobordisms is

* [[Chris Schommer-Pries]], _[[2-category of 2-dimensional cobordisms]]_.

* {#SchommerPries13} [[Chris Schommer-Pries]], _Dualizability in Low-Dimensional Higher Category Theory_ ([arXiv:1308.3574](http://arxiv.org/abs/1308.3574))

### In dimension 3

* [[Bruce Bartlett]], [[Christopher Douglas]], [[Christopher Schommer-Pries]], [[Jamie Vicary]], _Extended 3-dimensional bordism as the theory of modular objects_ ([arXiv:1411.0945](http://arxiv.org/abs/1411.0945))

### In dimension $\infty$

For a discussion of the relation of $Bord_{(\infty,\infty)}$ to the [[Thom spectrum]] and the [[cobordism ring]] see also

* [[John Francis]], _Cobordisms_ (notes by [[Owen Gwilliam]]) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))



[[!redirects (∞,n)-category of cobordisms]]

[[!redirects (∞,n)-categories of cobordisms]]
[[!redirects (infinity,n)-categories of cobordisms]]

