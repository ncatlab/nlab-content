An **epimorphism** (in a given category) is any morphism that every contravariant [[hom-functor]] sends to an [[injection]]. In more elementary terms, $f: X \to Y$ is an epimorphism if, given any $g, h: Y \to Z$, $g = h$ if $f; g = f; h$:
$$\array{
  &              & Y \\
  & \nearrow_{f} &   & \searrow^{g} \\
X &              &   &              & Z \\
  & \searrow^{f} &   & \nearrow_{h} \\
  &              & Y \\
} \quad\quad \Rightarrow \quad\quad \array{
X & \rightarrow^{f} & Y & \rightrightarrows^g_h & Z \\
}$$

+--{.query}
Can anybody make this look nicer? Preferably with curved arrows in the right-hand diagram? And maybe even with little vertical equals signs to show how the diagrams commute? I can do it in XYpic, but that\'s not supported by iTeX.
=--

There are a sequence of variations on the concept of epimorphism, from strongest to weakest:
>[[split epimorphism]], [[regular epimorphism]], [[strong epimorphism]], [[extremal epimorphism]], epimorphism.
In [[Set|the category of sets]], every epimorphism is regular (and even split if you believe the [[axiom of choice]]), so it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use.  

For example, in categories of sets with structure, epimorphisms need not be surjective: in the category of monoids, the inclusion $\mathbb{N}\hookrightarrow\mathbb{Z}$ is an epimorphism.  In general, in [[algebraic category|algebraic categories]] (categories of algebra for a [[Lawvere theory]]), the morphisms whose underlying function is surjective are the regular epimorphisms.