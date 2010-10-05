
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--



# Contents
* the following line creates the automatic table of contents
{: toc}

## Idea ##

A [[homotopy]] between two maps $f,g \colon X \to Y$ can be thought of as a path in the mapping space $Map(X,Y)$.  If, instead, one works with the space of [[embeddings]], one gets the notion of an **isotopy**.

Since, for arbitrary topological spaces, the mapping space $Map(X,Y)$ is not always well-defined as a topological space, defining a homotopy as a map $H \colon X \times I \to Y$ is the rigorous way of saying "$H$ is a path from $f$ to $g$ in the mapping space.".  Similarly, the proper definition of an isotopy as a map $H \colon X \times I \to Y$ with the property that $H(-,t) \colon X \to Y$ is always an embedding, is the rigorous way of saying "$H$ is a path from $f$ to $g$ in the embedding space.".

In some settings, even this is not strong enough.  In the notion of an **ambient isotopy**, one requires the path to extend to a path in the space of homeomorphisms of the ambient space.

## Definition ##

+-- {: .num_defn #isotopy}
###### Definition
Let $X$ and $Y$ be two [[topological spaces]].  Let $f,g \colon X \to Y$ be two [[embeddings]] of $X$ in to $Y$.  An **isotopy** from $f$ to $g$ is a [[continuous map]] $H \colon X \times [0,1] \to Y$ with the following properties:

1. $H(-,0) = f$
2. $H(-,1) = g$
3. $H(-,t)$ is an embedding of $X$ in to $Y$ for each $t \in [0,1]$.

Two maps for which there exists an isotopy are said to be **isotopic**.
=--

+-- {: .num_defn #amiso}
###### Definition
Let $X$ and $Y$ be two [[topological spaces]].  Let $f,g \colon X \to Y$ be two [[embeddings]] of $X$ in to $Y$.  An **ambient isotopy** from $f$ to $g$ is a [[continuous map]] $H \colon Y \times [0,1] \to Y$ with the following properties:

1. $H(-,0)$ is the identity on $Y$
2. $H(-,1) \circ f = g$
3. $H(-,t)$ is a self-homeomorphism of $Y$ for each $t \in [0,1]$.
=--


## Properties ##

The first two conditions on an isotopy $H$ imply that $H$ is a homotopy from $f$ to $g$.  Therefore the condition of being isotopic is stronger than that of being homotopic.  As the third condition applies level-wise, the proof that homotopy is an equivalence relation carries over to show that the same is true of isotopy.


## Examples ##

Isotopy is used where one wishes to study deformations of an object inside some ambient space that do not change the object itself.  An extremely important example of this is the theory of [[knots]] and [[links]] where, to prevent unknottings and unlinkings, there have to be some restrictions on the allowed movements.  These are usually encoded in terms of isotopies. It is unfortunately true, however, that a naive use of isotopy leads to strange results. If you use *continuous* isotopies then any two continuous embeddings of the circle into $S^3$ are isotopic, (basically since you just pull the knot tighter and tighter, (so the knotted bit gets smaller and smaller) and at the end you just put the 'unknot').  One way to handle this is to demand the isotopy to be [[piecewise linear]] (or [[smooth map|smooth]]), another is to work explicitly with ambient isotopy.

One of the beauties of isotopy of knots is that it can be realised very simply at the level of [[knot diagrams]]. Two knots are isotopic if their respective knot diagrams can be related using [[Reidemeister moves]]. (This is a formal theorem, but will be given elsewhere after some more development.)


## References ##
For isotopy in Knot Theory

 * R. H Crowell and R.H. Fox, Introduction to Knot Theory, Springer, Graduate Texts 57, 1963.

 * N.D. Gilbert and T. Porter, Knots and Surfaces, Oxford U.P., 1994.

[[!redirects isotopies]]
[[!redirects Isotopy]]
[[!redirects Isotopies]]
[[!redirects isotopic]]
[[!redirects Isotopic]]
[[!redirects ambient isotopy]]
[[!redirects Ambient Isotopy]]
[[!redirects Ambient isotopy]]
[[!redirects ambient isotopies]]
[[!redirects Ambient Isotopies]]
[[!redirects Ambient isotopies]]

