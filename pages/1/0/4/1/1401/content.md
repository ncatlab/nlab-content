# Ananatural transformations
* table of contents
{: toc}


## Idea

Just as [[natural transformation|natural transformations]] go between [[functor|functors]], ananatural transformations go between [[anafunctor|anafunctors]].

Given two functors interpreted as anafunctors, the natural transformations and ananatural transformations between them are the same, so the term 'ananatural' is overkill; one only needs it to emphasise the ana-context and otherwise can just say 'natural'.  That is, a 'natural transformation' between anafunctors unambigously means an ananatural transformation.


## Definitions

Given two [[categories]] $C$ and $D$ and two anafunctors $F, G\colon C \to D$, let us interpret $F,G$ as [[spans]] $C \leftarrow \overline{F} \rightarrow D$ and $C \leftarrow \overline{G} \rightarrow D$ of [[strict functors]] (where each backwards-pointing arrow is strictly surjective and faithful; see the definition of [[anafunctor]]).  Form the [[strict 2-limit|strict]] $2$-[[pullback]] $P \coloneqq \overline{F} \times_C \overline{G}$ and consider the strict functors $P \to \overline{F} \to D$ and $P \to \overline{G} \to D$.  Then an ananatural transformation from $F$ to $G$ is simply a natural transformation between these two strict functors.


More explicitly, if $F,G$ are given by sets ${|F|}, {|G|}$ of specifications and additional maps (see the other definition of [[anafunctor]]), then an __ananatural transformation__ from $F$ to $G$ consists of a coherent family of morphisms of $D$ indexed by the elements of $|F|$ and $|G|$ with common values in $C$.  That is:

* for each object $x$ of $C$, each $F$-specification $s$ over $x$, and each $G$-specification $t$ over $x$, we have a morphism
$$ \eta_{s,t}(x)\colon F_s(x) \to G_t(x) $$
in $D$;

* for each morphism $f\colon x \to y$ in $C$, each pair of $F$-specifications $s,t$ over $x,y$, and each pair of $G$-specifications $u,v$ over $x,y$, the diagram
  $$ \array {
     F_s(x)                & \overset{\eta_{s,u}(x)}\rightarrow  & G_u(x) \\
     F_{s,t}(f) \downarrow &                                     & \downarrow F_{u,v}(f) \\
     F_t(y)                & \underset{\eta_{t,v}(y)}\rightarrow & G_v(y)
  } $$
  is a [[commutative square]].


Of course, an __ananatural isomorphism__ is an [[invertible morphism|invertible]] ananatural transformation.


## Composition

Just as natural transformations can be composed vertically to form the morphisms of a [[functor category]], so ananatural transformations can be composed vertically to form an anafunctor category.

Just as natural transformations can also be whiskered by functors and composed horizontally to make a [[strict 2-category]] $Str Cat$ of (strict) categories, (strict) functors and natural transformations, so ananatural transformations can also be whiskered by anafunctors and composed horizontally to make a [[bicategory]] $Cat_{ana}$ of (strict) categories, anafunctors and (ana)natural transformations.  Assuming the [[axiom of choice]], $Cat_{ana}$ is equivalent to $Str Cat$; without choice (and [[internalisation|internally]]), $Cat_{ana}$ has better properties than $Str Cat$ and we will usually identify the former with [[Cat]].


[[!redirects ananatural isomorphism]]