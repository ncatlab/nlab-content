Just as [[natural transformation|natural transformations]] go between [[functor|functors]], ananatural transformations go between [[anafunctor|anafunctors]].

Given two functors interpreted as anafunctors, the natural transformations and ananatural transformations between them are the same, so the term 'ananatural' is overkill; one only needs it to emphasise the ana-context and otherwise can just say 'natural'.  That is, a 'natural transformation' between anafunctors unambigously means an ananatural transformation.

Of course, an __ananatural isomorphism__ is an invertible ananatural transformation.


## Definition ##

Given two [[categories]] $C$ and $D$ and two anafunctors $F, G\colon C \to D$, let us interpret $F,G$ as [[spans]] $C \leftarrow {|F|} \rightarrow D$ and $C \leftarrow {|G|} \rightarrow D$ of [[strict functors]] (where each backwards-pointing arrow is strictly surjective and faithful; see [[anafunctor]]).  Form the [[strict 2-limit|strict]] $2$-[[pullback]] $P \coloneqq {|F|} \times_C {|G|}$ and consider the strict functors $P \to {|F|} \to D$ and $P \to {|G|} \to D$.  Then an ananatural transformation from $F$ to $G$ is simply a natural transformation between these two strict functors.

More explicitly, ...


[[!redirects ananatural isomorphism]]