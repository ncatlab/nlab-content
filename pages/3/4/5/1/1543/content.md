#Idea#

For $G$ a group, a $G$-principal bundle over a space $X$ is another space $P$ sitting over $X$ by a map $P \to X$ such together with an [[action]] of $G$ on the space $P$, such that each fiber $P_x$ of $P$ over any $x \in X$ looks like $G$ once we identify one of the elements of $P_x$ with the identity element in $G$. 

#Definition#

Let $G$ a (topological, smooth, ...) [[group]] and $X$ a ([[topological space|topological]], smooth, ...) space.

The **trivial $G$-principal bundle** on $X$ is the space $G \times X$ with the projectoin map $X \times G \to X$ and the action of $G$ on $X \times G$ by right multiplication of $G$ on itself.

A $G$-**principal bundle** on $X$ is a space $P \to X$ equipped with an [[action]] of $G$ on $P$ such that there is a [[cover]] $Y \to X$ and a $G$-equivariant isomorphism of the [[pullback]] of $P$ to the cover with the trivial $G$-bundle on the cover

$$
  \array{
    Y \times G& \stackrel{\simeq_G}{\leftarrow}
     & P|_Y &\to& P
    \\ 
    &&\downarrow && \downarrow
    \\
    &&Y &\to& X
  }
$$

The [[groupoid]] of $G$-principal bundles on $X$ is denoted 

$$
  G Bund(X)
  \,.
$$

Since $G$-bundle pull back, this extends to a [[pseudofunctor]]

$$
  G Bund(-) : Spaces^{op} \to Groupoids
  \,.
$$

The local construction of $G$-principal bundles above ensures precisely that this satisfies [[descent]] and is hence a [[stack]].

This indicates the more fundamental way to _define_ $G$-principal bundles in the first place:
 
recall that for every [[group]] there is the the one-object [[groupoid]] $\mathbf{B}G$. Under the [[Yoneda embedding]] this [[representable functor|represents]] a [[simplicial presheaf|prestack]]. Write $\bar{\mathbf{B}G}$ for the corresponding [[stack]] obtained by [[(infinity,1)-sheafification|stackification]]. This is our $G Bund(-)$

$$
  G Bund(-) = \bar{\mathbf{B} G}
  \,.
$$

This perspective in turn is by general abstract nonsense equivalent to the following useful description:

Let $H$ be the suitable [[(infinity,1)-topos]] internal to which one looks at $G$-principal bundles. For instance for topological bundles this would be [[Top]]. For smooth bundles it would be the [[(infinity,1)-category of (infinity,1)-sheaves]] on [[Diff]], etc. 

Then every element in $G Bund(X) \simeq \bar{\mathbf{B} G}(X)$ is given by a morphism in $H(X,\mathbf{B}G)$ (sometimes called an [[anafunctor]]) and the $G$-principal bundle from the beginning of the above definition is just the [[homotopy limit|homotopy pullback]] of the [[point]] along this map

$$
  \array{
     P &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     X &\to& \mathbf{B} G
  }
  \,.
$$

This diagram, incidentally, directly tells us about another important property of $G$-principal bundles: they all canonically trivialize when pulled back to its own total space $P$.

This is what the homotopy commutativity of the above homotopy pullback diagram says: the cocycle $X \to \mathbf{B}G$ pulled back to the bundle $P \to X$ that it classifies becomes $P \to X \to \mathbf{B}G$ which is homotopic to the trivial cocycle (the one that factors through the [[point]]) on $P$.

The homotopy pullback here is conveniently and traditionally computed as an ordinary pullback of a fibrant replacement of the pullback diagram. The canonical such fibrant replacement is obtained by replacing ${*} \to \mathbf{B}G$ by $\mathbf{E}G \to \mathbf{B}G$, with $\mathbf{E}G$ an object weakly equivalent to the point, called the **universal $G$-principal bundle**. Details on how this fibrant replacement works are in the example section of [[homotopy limit]] and of [[generalized universal bundle]].

With that the above homotopy pullback is computed as the ordinary [[pullback]]

$$
  \array{
     P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     X &\to& \mathbf{B} G
  }
$$

So every $G$-principal bundle $P \to X$ is the pullback along a classifying map $X \to \mathbf{B}G$ (in the right $(\infinity,1)$-categorical context, otherwise a span such as an [[anafunctor]]) of the universal $G$-principal bundle.