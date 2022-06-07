
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Structured cospan
* table of contents
{: toc}

## Idea
 {#Idea}

The notion of a *structured cospan* is a modification of the concept of *[[decorated cospans]]*, introduced to provide an improved definition of [[isomorphism classes]] of decorated cospans. 

To better understand this motivation, notice that the decoration of the [[target]] of an [[isomorphism]] of [[decorated cospans]] is completely determined by the decoration of the source and the chosen isomorphism of vertices.

More clearly, let
$$
  \array{
     && c && &&&&&& F(c)\\
     & {}^{i}\nearrow && \nwarrow^{o} &&&&&& {}^d\nearrow\\
     a && \downarrow^f && b &&&& 1 & & \downarrow^{F(f)} \\
     & {}^{i'}\searrow && \swarrow^{o'}  &&&&&& {}^{d'}\searrow \\
     && c' &&&&&&&& F(c')
  }
$$
be an isomorphism of decorated cospans, where $d$ and $d'$ are the decorations of the source and the target, respectively (i.e., the 'top' and the 'bottom' cospan in the left diagram, respectively). Then, since the right diagram sits in $\mathbf{Set}$, it commutes on the nose. Thus the decoration $d'$ is already determined by the data of bijection $c \to c'$, together with the decoration on the source.

Therefore, this definition of isomorphism means we are lacking a degree of freedom, namely the freedom to specify an isomorphism for the decorations as well. For example, when open graphs are treated with decorated cospans, the decoration $d$ of a cospan $a \to c \leftarrow b$ is a [[directed graph]] with $c$ as vertex set. An isomorphism of such decorated cospans simply renames the source and target of each edge in $d$. However, isomorphism of directed graphs can be more than just relabeling of the vertices; hence we end up distinguishing open graphs merely by frivolous details like the specific names we give to edges.

Decorated cospans solve this problem by moving the cospans to the 'decorating category', meaning that the data of an isomorphism of cospans now is an arrow between the decorations. In the example of open graphs, we now have to specify an isomorphism of quivers $d \to d'$ instead of getting this from the (poorer) isomorphism of their vertices.

## Definition
+-- {: .un_def}
Let $\mathbf A$ be a category admitting finite coproducts, $\mathbf X$ a category admitting finite colimits and $L : \mathbf A \to \mathbf X$ a functor preserving finite coproducts. Then the [[symmetric monoidal category|symmetric monoidal]] [[double category]] of **structured cospans** over $L$ is the category $_L\mathrm{Csp}(\mathbf X)$ which has

* objects given by objects of $\mathbf A$,
* vertical 1-morphisms given by morphisms of $\mathbf A$
* horizontal 1-morphisms given by structured cospans:
$$
  \array{
     && x
      \\
      & {}^{i}\nearrow
      && \nwarrow^{o}
     \\
     L(a)
     &&&&
     L(b)
  }
$$
which are composed through the obvious pushout,
* 2-morphisms given by commutative diagrams of the form
$$
  \array{
     L(a) & \leftarrow^i & x & \rightarrow^o & L(b)\\
     \downarrow^{L(f)} & & \downarrow^h & & \downarrow^{L(g)}\\
     L(a') & \leftarrow^{i'} & x' & \rightarrow^{o'} & L(b')\\
  }
$$
which are composed horizontally in the obvious way.
=--

A **structured cospan** is then a ($1$-)morphism in such a category, that is, a cospan in $\mathbf X$ with the additional data of the functor $L$ and the two preimages of the feet.

## Examples
* By taking $L : \mathbf{Set} \to \mathbf{Graph}$ to be the *discrete graph functor*, i.e. the functor assigning to a set $V$ the edgeless graph with vertex set $V$, we get a category $_L\mathrm{Csp}(\mathbf{Graph})$ which models open graphs.

## Related concepts
* [[cospan]]
* [[decorated cospan]]
* [[hypergraph category]]

## References ##
Structured cospan categories were invented by [[John C. Baez]], [[Kenny Courser]], and [[Christina Vasilakopoulou]]. An introductory talk was given by Courser at the 4th Symposium on Compositional Structures:

* [[John C. Baez]], [[Kenny Courser]], _Structured cospans_, Theory and Applications of Categories **35** 48 (2020) 1771-1822 $[$[arXiv:1911.04630](https://arxiv.org/abs/1911.04630), [tac:35-48](http://www.tac.mta.ca/tac/volumes/35/48/35-48abs.html)$]$

* [[John C. Baez]], [[Kenny Courser]], *Structured cospans* talk notes (2019) ([pdf](http://math.ucr.edu/home/baez/SYCO4/courser_syco4.pdf))


[[!redirects structured cospans]]
