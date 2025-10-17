> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak




***

\tableofcontents

## From Complete QFT to Higher Topos Ontology, and back

Why care about higher category and topos theory in physics. 

Physics mindset: Care about understanding the world. Embrace the foundational math that naturally comes with it; disregard mathematics as sport or as end in itself.


### The Millennium Problem of Physics

Glory and misery of contemporary QFT: Perturbation theory. Works wonders as far as it goes; but goes only infinitesimally far.

Mathematically, perturbation theory is the geometry of *infinitesimal* spaces. Highly restrictive and of dubious predictivity (non-convergence...), but amenable to traditional algebra and analysis (formal power series).

The Millennium Problem of Physics: Complete QFT. Non-perturbative and globally defined. As in the slogan: "M-theory is (going to be) the completion of 11D SuGra". 

Traditionally lacking: Any concept of what such complete theories would actually be. 

Requires differential geometry of global field spaces, beyond the infinitesimal. But field spaces are generically not even infinite-dimensional manifolds, thus outside the scope of traditional diff geo textbooks. 

Underappreciated show stopper right there: Even basic notions that would be needed are traditionally missing. (Like: What is non-perturbative global BV-BRST??)


### Toposes for the Geometry of Physics 

Claim: Cohesive Higher Topos Theory is the missing globally complete Geometry of Physics.

Just like Riemannian geometry is the languge of gravity, or differential forms is the language of electromagnetic fields, or group/representation theory is the language of symmetry. You can do without, but you won't get very far.

Topos means "place". Where physics may *take place*.

First of all, a topos is a *category of generalized spaces*:

* a collection of "objects" $X$ --- the spaces

* a collection of "morphisms" $X \xrightarrow{f} Y$ --- the  maps

* a composition operation $(-) \circ (-)$ on composable morphisms, which is associative and unital.

\begin{tikzcd}
  & 
  Y
  \ar[dr, "{ g } "]
  \ar[d, equals, shorten=5pt]
  \\
  X 
  \ar[ur, "{ f }"]
  \ar[rr, "{ g \circ f }"{swap}]
  &{}&
  Z
\end{tikzcd}

Specifically, a (Grothendieck) topos is a category of such generalized spaces which are characterized by how they are *probed* by a given collection of probe spaces.

A rather physics-style operational notion: Instead of traditionally defining space as a set of points with  extra structure and properties, for a topos a space $X$ is defined by the system of sets of maps $U \to X$ of probe spaces $U$ into it.


Previous champion of toposes for physics: William Lawvere. Started out working on continuum mechanics. Went from asking "what is a vector field, really?" to laying foundations for topos theory, in order to speak about "Toposes of Laws of Motion" (technical term: synthetic differential geometry). A language for differential equations on generalized (field) spaces.

Great start, but for modern physics we need to go further.

### Higher Toposes for Generalized Symmetry

Beyond classical continuum mechanics, there is, of course

* gauge fields

* topological charges

* orbifolding (symmetry protection) 

and last not least:

* quantum states. 

Adjoining these to the picture brings in *higher topos theory*, also: *geometric homotopy theory*.

| geometry of physics | topos theory |
|---------|-------|
| gauge principle | higher homotopy |

A higher topos is where higher gauge field theory may take place.

In a higher topos, for every higher ("categorical") gauge group $G$ there is a *moduli space* (moduli stack) $\mathbf{B}G$ such that for every space(time) $X$: 

* a map $X \xrightarrow{ \vdash P } \mathbf{B}G$ is equivalently a $G$-principal bundle on $X$ (a charge sector of $G$-gauge fields)

* a homotopy between these is equivalently a gauge transformation.

\begin{tikzcd}
  X
  \ar[rr, bend left=30, "{ \vdash P }"{description, name=s}]
  \ar[rr, bend right=30, "{ \vdash P' }"{description, name=t}]
  \ar[from=s, to=t, Rightarrow]
  &&
  \mathbf{B}G
\end{tikzcd}

* a higher homotopy is equivalently a higher gauge transformation.

\begin{tikzcd}
  X
  \ar[rr, bend left=30, "{ \vdash P }"{description, name=s}]
  \ar[rr, bend right=30, "{ \vdash P' }"{description, name=t}]
  \ar[from=s, to=t, bend left=50, Rightarrow]
  \ar[from=s, to=t, bend right=50, Rightarrow]
  &
    \Rightarrow
  &
  \mathbf{B}G
\end{tikzcd}

* and so on.

In a precise sense, $\mathbf{B}G$ is the groupoid with a single object carrying $G$-worth of symmetries:

\begin{tikzcd}[sep=0pt]
  \mathbf{B}G
  =
  \Big\{
  &
  \ast
  \ar[
    in=60,
    out=180-60,
    looseness=4,
    shift right=3pt,
    "{ \,\mathclap{g}\, }"{description}
  ]
  &
  \Big\vert
  & 
  g \in G
  \Big\}
\end{tikzcd}

Generally, the spaces in a higher topos are like geometric *sets with gauge symmetries* (like orbifolds):

* in addition to elements $x$

* they contain gauge transformations 

\begin{tikzcd}
  x 
    \ar[r, "{ \sim }"] 
    &
  y
\end{tikzcd}

* and higher gauge-of-gauge transformations

\begin{tikzcd}[
  sep=35pt
]
  & y
  \ar[dr, "{ \sim }"{sloped}]
  \ar[
    d,
    Rightarrow,
    shorten=10pt
  ]
  \\
  x
  \ar[ur, "{ \sim }"{sloped}]
  \ar[rr, "{ \sim }"{swap, sloped}]
  &
    {}
  &
  z
\end{tikzcd}


### Gros Toposes for Generalized Geometry 

Recall that every topos is a category of geometric spaces of *some* sort. (Defined by the nature of the given probe spaces.)

But many toposes (including those traditionally highlighted in introductions to the topic, unfortunately) are just categories of *covering spaces of a fixed space $X$*. These are clearly too small a scenery for general physics, in fact they are technically called: *petit toposes*. 

Other toposes are categories of *all* generalized spaces exhibiting a given notion of geometry (differential, infinitesimal, analytic, super, ... etc.). These are called *gros toposes*. These are potentially geometries of physics.

Here the probe spaces are generalized *charts*.

\begin{imagefromfile}
    "file_name": "GeneralizedCharts.png",
    "width": 850,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


### Cohesive $\infty$-Toposes for Higher Gauge Fields

Thus to ask: What types of gros higher toposes are actual geometries of physics? 

These must contain 

* besides *concrete* spaces (physical spacetime) 

also 

* *superspaces* (of fermionic fields) 

as well as 

* *moduli* spaces of *gauge* fields.

These *geometric qualities* of spaces turn out to be witnessed by special higher toposes called *cohesive*.

These are higher toposes realizing a progression of "adjoint idempotent monads".

Prime example:

* **shape** 

  for every space $X$ there is its *path infinity-groupoid* $\esh X$: 

  $n$-morphisms are $n$-dimensional paths in $X$

  original space includes as the constant path $X \xrightarrow{\eta^{\esh}} \esh X$


* **points**

  for every moduli space $\mathbf{A}$ there is a its underlying groupoid of points $\flat \mathbf{A}$

  devoid of their cohesion / path-connection

  includes back into the original space $\flat \mathbf{A} \xrightarrow{\epsilon^{\flat}} \mathbf{A}$

These two aspects of spaces (shape/points) are *dual opposites* to each other:

There is an *adjunction*

$$
  shape \dashv points
$$

namely a natural bijection of maps, like this:

$$
  \begin{array}{rccc}
    & \esh X &\xrightarrow{ \nabla }& \mathbf{B}G
    \\
    \Leftrightarrow &
    X &\xrightarrow{}& \flat \mathbf{B}G
  \end{array}
$$

But maps $\esh X \xrightarrow{ \nabla } \mathbf{B}G$ encode *parallel transport* in the underlying $G$-bundle $X \xrightarrow{\eta^{\esh}} \esh X \xrightarrow{\nabla} \mathbf{B}G$. This is the same as a *flat connection* on $P$, a gauge field.

The adjunction above says that a flat connection on a $G$-principal bundle is equivalent to a reduction of its structure group to the underlying discrete group. This is a theorem of gauge theory. But here it is part of the BIOS of cohesive higher toposes.




### Hard Metaphysics

Every topos is also a language of formal logic (namely of the laws that govern its geometry of physics).
In this logic, the cohesive modalities are a progression of resolution of oppositions.

From this logical perspective these neatly matches idealistic ontology ("objective logic").

So, in asking for fundamental physics we end up asking about natural foundations of mathematics. 

Seems only natural: That the most fundamental physics involves the most fundamental math.

Hegel [said](https://ncatlab.org/nlab/show/Phenomenology+of+Spirit#Vorrede5) his aim to bring philosophy closer to a form of science. The philosophy in question here is ontology, hence metaphysics (as in the old *natural philosophy*). 

Hence to make *metaphysics* a hard science. 

Hegel's *idealism* refers to the aim that basic *qualities of being* (like *shape* and *points*, above) be *systematically derivable* from first principles ("objective logic": a logic of how objective reality comes into being). To see how they are hard-coded in the BIOS of reality.

Hence to make *metaphysics* a mathematical since.

Lawvere observed that *modal topos theory* (my paraphrase) provides this "objective logic".


### The Exceptional within the General Abstract 

Two facets: The general abstract and the exceptional particular.
Eg. Category of groups is general abstract. In there we find the exceptional groups.

Similarly: Solid cohesive toposes accommodate all supergeometry. In there 11D supergravity with its 5-brane is an exceptional structure.

And in higher cohesive topos, 11D supergravity does find a global completion. Shown in the topological sector...







