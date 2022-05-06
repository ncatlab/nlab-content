[[!redirects decorated cospans]]
# Decorated cospan

* table of contents
{: toc}

## Idea
Decorated cospans are a convenient formalism to deal with open networks, i.e. networks were some nodes are interpreted to be 'inputs' and some other to be 'outputs'. In fact, a natural way to do such labelling is to specify some function assigning the set of inputs to those nodes in the network tasked with receiving them, and analogously, a function assigning to outputs those nodes which provide them. This is, morally, a [[cospan]]: the network is the vertex, and inputs and outputs are the feet. However, the two things sit in 'different categories': e.g., inputs and outputs may be sets of wires and sockets, while the network has a more complicated description. Nevertheless, the network is just a set of nodes with more information attached, namely the way those nodes are connected. The key insight here is that to specify inputs/outputs of the network, we don't really care about this additional information. Hence we can use a 'cospan of nodes' (formally, a cospan in [[FinSet]]), and deal with the network structure later, as a _decoration_.

Surprisingly, this formalism naturally captures also other operations such as sequential and parallel composition of networks.

## Definition

### Categories of cospans
In a category $\mathbf C$ with finite colimits (or even just [[pushout|pushouts]]) [[cospans]] can be composed in a natural way. In fact, given $x \to s \leftarrow y$ and $y \to t \leftarrow z$, we get a new cospan $x \to p \leftarrow z$ by taking a pushout in the middle:
$$
  \array{
     &&&& s +_y t 
     \\& 
    &&
      {}^{p_s}\nearrow
      && \nwarrow^{p_t}
    \\
     && s &&&& t
      \\
      & {}^{f}\nearrow
      && \nwarrow^{g}
       &
       & {}^{h}\nearrow
      && \nwarrow^{i}
     \\
     x
     &&&&
     y
     &&&&
     z
  }
$$

Therefore cospans form a compositional structure: a category $\mathrm{Cospan}(\mathbf C)$ where objects are the same of $\mathbf C$ but morphisms from $x$ to $y$ are replaced by cospans with feet $x$ and $y$. Since the pushout we choose to form the composite of two cospans is, in general, unique only up to unique isomorphism, we actually need to define a $2$-category. Morphisms of cospans $(x \to p \leftarrow y) \Rightarrow (x \to q \leftarrow y)$ are given by any $\mathbf C$-morphism $\eta : p \to q$ making the following commute

$$
  \array{
    && p
    \\
    & {}^{f}\nearrow && \nwarrow^{g}
    \\
    x &&\downarrow^\eta&& z
    \\
    & {}_{f'}\searrow
    && \swarrow_{g'}
    \\
    && q
  }
$$

It is also customary to ignore the $2$-structure and simply work with $\mathrm{Cospan}(\mathbf C)$ as a $1$-category whose morphisms are _isomorphism classes_ of cospans.

### Categories of decorated cospans
+-- {: .un_defn #DecoratedCospanCategory}
###### Definition
([B. Fong 2015](#BrendanFong2015))
Let $\mathbf C$ be a [[finitely cocomplete category|category with finite colimits]], and
$$
(F, \phi): (\mathbf C, +) \to (\mathbf D, \otimes)
$$
be a [[lax monoidal functor]]. A **decorated cospan**, or more precisely an **$F$-decorated cospan**, is a pair $(x \overset{i}\to n \overset{o}\leftarrow y,\, 1 \overset{s}\to Fn)$. We shall call the element $1 \overset{s}\to Fn$ the **decoration** of the decorated cospan. A morphism of decorated cospans
$$
f : (x \overset{i}\to n \overset{o}\leftarrow y,\, 1 \overset{s}\to Fn) \to (x \overset{i}\to n' \overset{o}\leftarrow y,\, 1 \overset{s'}\to Fn')
$$
is a morphism of cospans such that the following commutes:
$$
\array{
 && Fn\\
 & \nearrow^s\\
 1 & & \downarrow^{Ff}\\
 & \searrow^{s'}\\
 && Fn'
}
$$
=--

+-- {: .un_def}
###### Definition
Given a cospan $x \to n \leftarrow y$ in $\mathbf C$, the **empty decoration on $n$** is the unique map
$$
1 \overset{\phi_1}\longrightarrow F\varnothing \overset{F!}\longrightarrow Fn
$$
where $\varnothing$ is [[initial object|inital]] in $\mathbf C$ and $!$ denotes the universal morphism from such object.
=--

+-- {: .num_prop}
###### Proposition
([B. Fong 2015](#BrendanFong2015))
There is a category $F\mathrm{Cospan}$ of $F$-decorated cospans, with objects the objects of $\mathbf C$ and morphisms isomorphism classes of $F$-decorated cospans. Composition in this category is given by the class of the pushout of two representatives:
$$
  \array{
     &&&& n +_y m
     \\& 
    &&
      {}^{j_n}\nearrow
      && \nwarrow^{j_m}
    \\
     && n &&&& m
      \\
      & {}^{i_x}\nearrow
      && \nwarrow^{o_y}
       &
       & {}^{i_y}\nearrow
      && \nwarrow^{o_z}
     \\
     x
     &&&&
     y
     &&&&
     z
  }
$$

along with the decoration

$$
1 \overset{\lambda^{-1}}\longrightarrow 1 \otimes 1 \overset{s \otimes s'}\longrightarrow Fn \otimes Fm \overset{\phi_{n,m}}\longrightarrow F(n+m) \overset{F[j_n,j_m]}\longrightarrow F(n +_y m).
$$

where $1 \overset{s}\to Fn$ and $1 \overset{s'}\to Fm$ are decorations of the first and second cospan, respectively.
=--
+-- {: .proof}
###### Proof
The identity morphism of an object $x$ in $F\mathrm{Cospan}$ is simply $x \overset{\mathrm{id}}\to x \overset{\mathrm{id}}\leftarrow x$ equipped with the empty decoration on $x$. The check that all relevant axioms are satisfied can be found in ([B. Fong 2015, Appendix A](#BrendanFong2015))
=--

+-- {: .un_remark}
###### Remark
The composition of decorations is the key construction of the decorated cospans formalisms. In fact, returning to the analogy with open networks, it constructs the composite network of a given 'link' of two networks. Hence the compositional structures of the cospans is leveraged to describe the compositional structure of a richer structure.
=--

+-- {: .un_remark}
###### Remark
Notice that the empty decoration gives a canonical way to decorate any cospan on $\mathbf C$. Indeed, it can be shown this defines a wide functor $\mathrm{Cospan}(\mathbf C) \embedsin F\mathrm{Cospan}$, as the composition of two empty-decorated cospans is again empty-decorated.
=--

### The monoidal and hypergraph structures
In the presence of a braiding on $\mathbf D$ (the 'decorating category'), the category of decorated cospans becomes not just [[symmetric monoidal category|symmetric monoidal]], but a full-blown [[hypergraph category]].

+-- {: .num_theorem}
###### Theorem
([B. Fong, 2015](#BrendanFong2015))
Let $\mathbf C$ be a category with finite colimts, $(\mathbf D, \otimes)$ a [[braided monoidal category]] and $(F, \phi) : (\mathbf C, +) \to (\mathbf D, \otimes)$ a lax braided monoidal functor. Then we may equip $F\mathrm{Cospan}$ with a symmetric monoidal and hypergraph structure, such that there is a [[wide subcategory|wide embedding]] of hypergraph categories
$$
\mathrm{Cospan}(\mathbf C) \embedsin F\mathrm{Cospan}.
$$
=--
+-- {: .proof}
###### Proof
We define the monoidal product of objects $x$ and $y$ of $F\mathrm{Cospan}$ to be their coproduct $x+y$ in $\mathbf C$, and defined the monoidal product of decorated cospans $(x \overset{i}\to n \overset{o}\leftarrow y, 1 \overset{s}\to Fn)$ and $(x \overset{i}\to n' \overset{o}\leftarrow y, 1 \overset{s'}\to Fn')$ to be
$$
  \array{
     && n + n'
      \\
      & {}^{i_x + i_{x'}}\nearrow
      && \nwarrow^{o_y + o_{y'}} &&,&& 1 \overset{\lambda^{-1}}\longrightarrow 1 \otimes 1 \overset{s \otimes s'}\longrightarrow Fn \otimes Fn' \overset{\phi_{n,n'}}\longrightarrow F(n+n')
     \\
     x+x'
     &&&&
     y+y'
  }
$$
The braiding in $\mathbf D$ can be now used to show this product is indeed functorial. Finally, we choose associator, unitors and braiding to be the images of those in $\mathrm{Cospan}(\mathbf C)$. The necessary checks are done in  ([B. Fong 2015, Appendix A](#BrendanFong2015)).

The hypergraph structure is defined by equipping each object $x \in F\mathrm{Cospan}$ with the image of the special commutative [[Frobenius algebra|Frobenius monoid]] specified by the hypergraph structure of $\mathrm{Cospan}(\mathbf C)$. The fact that the 'empty-decoration' embedding is an hypergraph functor is evident.
=--

If the monoidal unit of $(\mathbf D, \otimes)$ is the initial object, then each object admits only a decoration --- the empty one. This implies $\mathrm{Cospan}(\mathbf C)$ and $1_{\mathbf C}\mathrm{Cospan}$ are isomorphic as hypergraph categories.

## Examples

## Related concepts
* [[cospan]]
* [[structured cospan]]
* [[hypergraph category]]

## References ##

Decorated cospans were first defined by Brendan Fong:

* {#BrendanFong2015} [[Brendan Fong]], _Decorated Cospans_, ([arXiv:1502.00872](http://arxiv.org/abs/1502.00872)).
