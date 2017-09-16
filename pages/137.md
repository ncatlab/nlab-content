#Definition#

An **epimorphism** in a [[category]] $C$ is a [[morphism]] 
$f : X \to Y$ 
such that it is sent by every contravariant [[hom-functor]] $Hom(-,Z)$ sends to an [[injection]]
$$
  \forall Z \in C : \;
  Hom(Y,Z) \stackrel{f^*}{\hookrightarrow} 
  Hom(X,Z)
  \,.
$$

In more elementary terms, $f: X \to Y$ is an epimorphism if, given any $g, h: Y \to Z$, $g = h$ if $f; g = f; h$:
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

An epimorphism in $C^{op}$ is a [[monomorphism]] in $C$.

#Remarks#

## Variations ##

There are a sequence of variations on the concept of epimorphism, from strongest to weakest:
>[[split epimorphism]], [[regular epimorphism]], [[strong epimorphism]], [[extremal epimorphism]], epimorphism.
In [[Set|the category of sets]], every epimorphism is regular (and even split if you believe the [[axiom of choice]]), so it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use.  

For example, in categories of sets with [[extra structure]], epimorphisms need not be surjective, but often the surjections correspond to a stronger notion of epimorphism. In [[algebraic category|algebraic categories]] (categories of algebra for a [[Lawvere theory]]), the morphisms whose underlying function is surjective are the regular epimorphisms.

