
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
* the following line creates the automatic table of contents
{: toc}

## Idea ##

A **link** is a generalisation of a [[knot]] where one is allowed more than one component.  Many [[knot invariants]] extend to [[link invariants]] and for many such invariants, one needs to know this extension to compute it even for a knot.  Thus the study of links and knots is inextricably intertwined.

## Basics ##

+-- {: .num_defn #link}
###### Definition
A **link** is an [[embedding]] of a finite number of copies of the [[circle]].  The embedding is usually taken in $\mathbb{R}^3$, or its [[one-point compactification]], $S^3$.
=--

It is possible to generalise this to more varied sources and targets.

Links can be studied in a number of ways depending on the notion of equivalence that is used.  Coming from knot theory, one considers equivalence up to [[isotopy]]; that is, two links are equivalent if there is a homotopy between them which is an embedding for all times.  A weaker notion was consider by [Milnor](#jmLinkGroups) wherein the components of the link are allowed to pass through themselves, but not through other components.  That is, when restricted to each component it must be an immersion for all times, and the images of the components must always be disjoint.


## Examples ##

#### The Hopf Link ####

This is perhaps the simplest non-trivial link, consisting of two components linked once.

<svg width="334" height="218" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="50131">
 <g>
  <title>Layer 1</title>
  <path fill="none" stroke="#ff00dc" stroke-width="12" d="m212,206.957031c1.5,-64.5 -56.75,-102.75 -105,-103.5c-48.25,-0.75 -97.5,37 -101,97.5" id="svg_50131_4" transform="rotate(-180, 109.014, 155.201)"/>
  <circle fill="none" stroke="#32ff00" stroke-width="12" cx="225" cy="108.957031" r="102.957031" id="svg_50131_2"/>
  <path fill="none" stroke="#ff00dc" stroke-width="12" d="m212,109.957031c1.5,-64.5 -56.75,-102.75 -105,-103.5c-48.25,-0.75 -97.5,37 -101,97.5" id="svg_50131_3"/>
 </g>
</svg>

#### The Borromean Links ####

It is possible to link together $n$ circles in such a way that removing any one makes the others fall apart.  The simplest such configuration is the Borromean Links.

<svg width="311" height="303" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="26799">
 <g>
  <title>Layer 1</title>
  <path id="svg_26799_5" transform="rotate(151.088, 228.857, 239.417)" d="m128.856506,289.932281c0.666992,-60.332993 50,-102.333282 101,-100.999985c51,1.333008 98,41.666992 99,100.999985" stroke-width="12" stroke="#004cff" fill="none"/>
  <path transform="rotate(146.692, 132.899, 239.497)" id="svg_26799_3" d="m32.898575,290.01297c0.667007,-60.333008 50,-102.333313 101,-101.000015c51.000015,1.333008 98.000015,41.667007 99.000015,101.000015" stroke-width="11" stroke="#ff0000" fill="none"/>
  <path id="svg_26799_4" transform="rotate(148.192, 178.059, 148.126)" d="m78.059052,198.642181c0.666992,-60.333008 50,-102.333298 101,-101c51,1.333008 98,41.666992 99,101" stroke-width="12" stroke="#22ba00" fill="none"/>
  <path transform="rotate(-28.912, 181.026, 153.005)" id="svg_26799_7" d="m81.026367,203.520721c0.666992,-60.332993 50,-102.33329 101,-100.999992c51,1.333008 98,41.667 99,100.999992" stroke-width="12" stroke="#004cff" fill="none"/>
  <path transform="rotate(-33.3083, 77.9843, 155.925)" id="svg_26799_2" d="m-22.01577,206.440155c0.666672,-60.333328 50,-102.333328 100.999992,-101c51,1.333328 98,41.666672 99,101" stroke-width="11" stroke="#ff0000" fill="none"/>
  <path transform="rotate(-31.8084, 125.824, 63.2953)" id="svg_26799_6" d="m25.823822,113.810913c0.666992,-60.332993 50,-102.333296 101,-100.999998c51,1.333 98,41.667006 99,100.999998" stroke-width="12" stroke="#22ba00" fill="none"/>
 </g>
</svg>

#### The Whitehead Link ####

This is an example of a link that shows the difference between the two notions of equivalence.  If the links are only allowed to move by isotopies, then the two components are linked.  However, if a link is allowed to pass through itself, then they can be unlinked.

<svg width="570" height="425" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="15824">
 <g>
  <title>Layer 1</title>
  <path transform="rotate(180, 407.508, 178.539)" id="svg_15824_16" d="m252.014862,137.203003c-1.166687,64 59.916992,118 128.375,102c34.229004,-8 84.802032,-81 108.859039,-106c24.057983,-24.999992 41.598999,-24.999992 73.765991,5" stroke-width="12" stroke="#ff9400" fill="none"/>
  <path id="svg_15824_13" d="m6.027344,221.222137c-1.166702,-79.766586 36.916992,-126.069641 114.375,-124.127991c77.458008,1.94165 78.291992,75.620697 116.625,107.620697" stroke-width="12" stroke="#ff9400" fill="none"/>
  <circle id="svg_15824_19" r="202.714844" cy="212.714844" cx="281.027344" stroke-width="20" stroke="#ffffff" fill="none"/>
  <circle id="svg_15824_18" r="202.714844" cy="212.714844" cx="280.027344" stroke-width="12" stroke="#ff00f6" fill="none"/>
  <rect id="svg_15824_20" height="20" width="52" y="312.714845" x="84.027344" stroke-width="0" stroke="#ff9400" fill="#ffffff"/>
  <path id="svg_15824_12" d="m6.027344,217.714844c-1.166664,64 59.916672,118 128.375,102c34.229172,-8 88.802094,-87 112.859375,-112c24.057281,-25 43.598969,-17 69.765625,12" stroke-width="12" stroke="#ff9400" fill="none"/>
  <rect id="svg_15824_21" height="20" width="52" y="328.714845" x="412.027344" stroke-width="0" stroke="#ff9400" fill="#ffffff"/>
  <path transform="rotate(180, 446.51, 276.961)" id="svg_15824_17" d="m330.018829,338.553772c-1.166687,-79.765991 45.916992,-125.069305 123.374969,-123.127701c77.458008,1.941696 78.291992,75.620682 109.625,105.620682" stroke-width="12" stroke="#ff9400" fill="none"/>
 </g>
</svg>

#### Brunnian Links ####

A _Brunnian link_ is a non-trivial link which has the property that the removal of any of its components results in an unlink.  The Borromean rings above are an example of a Brunnian link.  Whether or not the Hopf link is will hopefully be decided by the answers to [this MO question](http://mathoverflow.net/questions/40724/is-the-hopf-link-a-brunnian-link).



## References ##

* Milnor, J. (1954). Link groups. _Ann. of Math. (2)_, _59_, 177&ndash;195. [MR](http://www.ams.org/mathscinet-getitem?mr=71020){: #jmLinkGroups}

[[!redirects Link]]
[[!redirects links]]
[[!redirects Links]]
