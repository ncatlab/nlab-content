
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

* **principal bundle** / [[torsor]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]]

***


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

For $G$ a [[group]], a $G$-principal [[bundle]] over a space $X$ is another space $P$ sitting over $X$ by a map $P \to X$ such together with an [[action]] of $G$ on the space $P$, such that each fiber $P_x$ of $P$ over any $x \in X$ is a $G$-[[torsor]], so it looks like $G$ once we identify one of the elements of $P_x$ with the identity element in $G$. 

## Definition

Let $G$ be a ([[group object|topological, smooth, ?]]) [[group]] and $X$ a ([[topological space|topological]], [[manifold|smooth]], ...) space.


### Ordinary definition

The **trivial $G$-principal bundle** on $X$ is the space $G \times X$ with the projection map $X \times G \to X$ and the action of $G$ on $X \times G$ by (say, right) multiplication of $G$ on itself.

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


#### The stack of principal bundles

The [[groupoid]] of $G$-principal bundles on $X$ is denoted 

$$
  G Bund(X)
  \,.
$$

Since $G$-bundles pull back, this extends to a [[pseudofunctor]]

$$
  G Bund(-) : Sp^{op} \to Grpd
  \,.
$$

The local construction of $G$-principal bundles above ensures precisely that this satisfies [[descent]] and is hence a [[stack]].


### In terms of fiber sequences 

This indicates the more fundamental way to _define_ $G$-principal bundles in the first place:
 
Recall that for every [[group]] there is the the one-object [[groupoid]] $\mathbf{B}G$. Under the [[Yoneda embedding]] this [[representable functor|represents]] a [[simplicial presheaf|prestack]]. Write $\bar{\mathbf{B}G}$ for the corresponding [[stack]] obtained by [[(infinity,1)-sheafification|stackification]]. This is our $G Bund(-)$

$$
  G Bund(-) = \bar{\mathbf{B} G}
  \,.
$$

This perspective in turn is by [[category theory|general abstract nonsense]] equivalent to the following useful description:

Let $H$ be the suitable [[(∞,1)-topos]] internal to which one looks at $G$-principal bundles. For instance for topological bundles this would be [[Top]]. For smooth bundles it would be the [[(∞,1)-category of (∞,1)-sheaves]] on [[Diff]], etc. 

Then every element in $G Bund(X) \simeq \bar{\mathbf{B} G}(X)$ is given by a morphism in $H(X,\mathbf{B}G)$, which may be thought of as an [[anafunctor]] to $\mathbf{B}G$ from the (categorially) [[discrete category]] $X$; the $G$-principal bundle from the beginning of the above definition is just the [[homotopy limit|homotopy pullback]] of the [[point]] along this map, i.e. the [[fibration sequence|homotopy fiber]] of $X \to \mathbf{B}G$:

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

This diagram, incidentally, directly tells us about another important property of $G$-principal bundles: they all canonically trivialize when pulled back to their own total space $P$.

This is what the homotopy commutativity of the above homotopy pullback diagram says: the cocycle $X \to \mathbf{B}G$ pulled back to the bundle $P \to X$ that it classifies becomes $P \to X \to \mathbf{B}G$, which is homotopic to the trivial cocycle (the one that factors through the [[point]]) on $P$.

The homotopy pullback here is conveniently and traditionally computed as an ordinary pullback of a [[fibration|fibrant replacement]] of the pullback diagram. The canonical such fibrant replacement is obtained by replacing ${*} \to \mathbf{B}G$ by $\mathbf{E}G \to \mathbf{B}G$, with $\mathbf{E}G$ an object [[weak equivalence|weakly equivalent]] to the point, called the **universal $G$-principal bundle**. Details on how this fibrant replacement works are in the example section of [[homotopy limit]] and of [[generalized universal bundle]].

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

So every $G$-principal bundle $P \to X$ is the pullback along a classifying map $X \to \mathbf{B}G$ (in the right $(\infty,1)$-categorical context, otherwise a span such as an [[anafunctor]]) of the universal $G$-principal bundle.

#### The $G$-action from the homotopy pullback


Given the definition of the bundle $P$ in terms of a [[homotopy pullback]] of ${*} \to \mathbf{B}G$ we re-obtain the $G$-[[action]] on $P$ as follows 
(with an eye towards its generalization to [[principal ∞-bundles]]).



Let 

$$
  \cdots G \times G \stackrel{\stackrel{d_2}{\to}}{\stackrel{\stackrel{d_1}{\to}}{\stackrel{d_0}{\to}}}
  G \stackrel{\stackrel{d_1}{\to}}{\stackrel{d_0}{\to}}
  {*}
  \to 
  \mathbf{B}G
$$

be the [[quotient object|effective]] [[groupoid object in an (∞,1)-category]] that exhibits the [[delooping]] $\mathbf{B}G$ of $G$.

Form the [[homotopy pullback]] of the classifying morphism $X \to \mathbf{B}G$ along the $d_0$-[[simplicial object|face maps]] of this diagram. This yields a diagram

$$
  \array{
    \cdots
    &
     P \times G \times G
    &
    \stackrel{\to}{\stackrel{\to}{\to}}
    &
     P \times G
    &
    \stackrel{\to}{\to}
    &
    P
    &
    \stackrel{}{\to}
    &
    X
    \\
    & \downarrow
    &&
    \downarrow
    &&
    \downarrow
    &&
    \downarrow
    \\
    \cdots
    &
     G \times G
    &
    \stackrel{\to}{\stackrel{\to}{\to}}
    &
     G
    &
    \stackrel{\to}{\to}
    &
    {*}
    &
    \stackrel{}{\to}
    &
    \mathbf{B}G
  }
$$

where all squares formed by the lowest horizontal morphisms are [[homotopy pullback]] squares, by construction, and where the remaining horizontal morphisms in the top row are induced by the universal property of the homotopy pullback and the morphisms downstairs.

The claim is that 

* the top row encodes the [[action]] of $G$ on $P$
  in that the action is the morphism indicated $\rho$ in
  $$
   \cdots
   \stackrel{\to}{\stackrel{\to}{\to}}
   P \times G 
    \stackrel{\stackrel{\rho}{\to}}{\stackrel{p_1}{\to}}
   P
   \to X
  $$

* and it exhibits $P \times G^{\times (n-1)}$ as the [[groupoid object in an (∞,1)-category]] being the [[?ech nerve]] of $P \to X$:

  $$
  \array{
    \cdots
    &
     P \times_X P \times_X P
    &
    \stackrel{\to}{\stackrel{\to}{\to}}
    &
     P \times_X P
    &
    \stackrel{\to}{\to}
    &
    P
    &
    \stackrel{}{\to}
    &
    X
    \\
    & \uparrow^{\simeq}
    &&
    \uparrow^{\simeq}
    &&
    \uparrow^{\simeq}
    &&
    \uparrow^{\simeq}
    \\
    \cdots
    &
     P \times G \times G
    &
    \stackrel{\to}{\stackrel{\to}{\to}}
    &
     P \times G
    &
    \stackrel{\stackrel{\rho}{\to}}{\to}
    &
    P
    &
    \stackrel{}{\to}
    &
    X
    \\
    & \downarrow
    &&
    \downarrow
    &&
    \downarrow
    &&
    \downarrow
    \\
    \cdots
    &
     G \times G
    &
    \stackrel{\to}{\stackrel{\to}{\to}}
    &
     G
    &
    \stackrel{\to}{\to}
    &
    {*}
    &
    \stackrel{}{\to}
    &
    \mathbf{B}G
  }
  $$

Here the second statement in particular encodes the familiar way to formulate **principality of the action** $\rho$, in that it says that

$$
  P \times G \stackrel{p_1 \times \rho}{\to} P \times_X P
$$

is an [[isomorphism]].

We now unwrap the first statement in gory detail to make clear that this abstract nonsense does reproduce the familiar definition of the action of $G$ on $P$.



#### Unwinding this abstract nonsense

We now rederive the [[action]] $\rho$ of $G$ on $P$ given just the classifying map $X \to \mathbf{B} G$ by spelling out the details implied by the above nonsense.

Whatever the precise context is (topological, smooth, etc.) we may assume that we are at least in a [[category of fibrant objects]]. Then the classifying morphism $X \to \mathbf{B}G$ is represented by an [[anafunctor]], namely a cocycle

$$
  \array{
    C(U) &\stackrel{g}{\to} & \mathbf{B}G
    \\
    \downarrow^{\in W \cap F}
    \\
    X
  }
$$

in [[?ech cohomology]] coming from some [[cover]] $\{U_i \to X\}$ of $X$.

The [[?ech nerve]] $C(U)$ has

* objects = $\{(x,i) | x \in U_i\}$

* morphisms = $\{ (x,i) \stackrel{}{\to} (x,j) | x \in U_{i j}\}$ .

The [[functor]] $g : C(U) \to \mathbf{B}G$ sends

$$
  g : ((x,i) \to (x,j)) \mapsto (\bullet \stackrel{g_{i j}(x)}{\to}\bullet )
$$

for $g_{i j} \in Functions(U_{i j}, G)$ as described in detail at [[?ech cohomology]].

With $\mathbf{E}G = \{g \stackrel{h}{\to} g h | g,h \in G \}$ the fibrant replacement of the point, which we shall find it helpful to think of as given by

* objects = $\left\{
      \array{
         && \bullet
         \\
         & {}^g\swarrow
         \\
         \bullet
      }
    \right\}
  $

* morphisms = $\left\{
      \array{
         && \bullet
         \\
         & {}^g\swarrow && \searrow^{g' = g h}
         \\
         \bullet &&\stackrel{h}{\to}&& \bullet
      }
    \right\}
  $


we compute the [[homotopy pullback]] as the 
homotopy fiber product given by the ordinary [[pullback]] (see [[category of fibrant objects]] for details)

$$
  \array{
    P &\to& \mathbf{E}G
    \\
    \downarrow && \downarrow
    \\
    C(U) &\stackrel{g}{\to}&
    \mathbf{B}G
  }
  \,.
$$


So we read off that $P$ is the [[groupoid]] with

* objects = 
  $$
   \left\{
   \array{
     && \bullet
     \\
     & {}^{g}\swarrow
     \\
     \bullet
     \\
     (x,i)
   }
   \right\}
  $$

* morphisms =
  $$
   \left\{
   \array{
     && \bullet
     \\
     & {}^{g}\swarrow && \searrow^{g'}
     \\
     \bullet &&\stackrel{g_{i j }(x)}{\to}&& \bullet
     \\
     (x,i) &&\stackrel{}{\to}&& (x,j)
   }
   \right\}   
  $$

With $P$ determined as an ordinary pullback of a replacement it is convenient for the following to realize it in turn as the pullback-up-to-2-cell in

$$
  \array{
   P &\to& {*}
   \\
   \downarrow &\Downarrow^{\eta_P}& \downarrow
   \\
   C(U) &\to& \mathbf{B}G
  }
 \,.
$$
  
  
A moment reflection shows that the component of the [[natural transformation]] $\eta_P$ here is

$$
  \eta_P : 
  \left(
     \array{
     && \bullet
     \\
     & {}^{g}\swarrow
     \\
     \bullet
     \\
     (x,i)
   }
  \right)
  \;\;\;
  \mapsto
  \;\;\;
  (\bullet \stackrel{g}{\to}\bullet)
$$
   
  At the same time recall from the discussion at [[delooping]] that the component of the transformation $\eta_G$ in

$$
  \array{
   G &\to& {*}
  \\
  \downarrow &\Downarrow^{\eta_G}& \downarrow
   \\
   {*} &\to& \mathbf{B}G
  }
$$

is

$$
  \eta_G : g \mapsto (\bullet \stackrel{g}{\to} \bullet)
  \,.
$$
  

Taken together this shows that  the universal morphism $P \times G \to P$ induced from the commutativity of

$$
 \array{
  &&&& P \times G
  \\
  && & \swarrow && \searrow
  \\
  && P &&&& G
  \\
  & \swarrow && \searrow && \swarrow && \searrow 
  \\
  C(U) &&\Downarrow^{\eta_P}&& {*} &&\Downarrow^{\eta_G}&& {*}
  \\
  &&\searrow&& \downarrow && \swarrow
  \\
  &&&& \mathbf{B}G
 }  
$$

and from the [[homotopy pullback]] property of

$$
  \array{
   P &\to& {*}
   \\
   \downarrow &\Downarrow^{\eta_P}& \downarrow
   \\
   C(U) &\to& \mathbf{B}G
  }
$$

is simply given by the composition of these two component maps

$$
  P  \times G  \to P :
  \left(
  \left(
     \array{
     && \bullet
     \\
     & {}^{g}\swarrow
     \\
     \bullet
     \\
     (x,i)
   }
  \right)
  \,,
  \array{
    \bullet
    \\
    \downarrow^{g'}
    \\
    \bullet
  }
  \right)
  \; \;\; \;
  \mapsto
  \; \;\; \;
  \left(
     \array{
     && \bullet
     \\
     && \downarrow^{g'}
     \\
     && \bullet
     \\
     & {}^{g}\swarrow
     \\
     \bullet
     \\
     (x,i)
   }
  \right)
  \,.
$$

But this is manifestly the right (being both: from the right and correct :-) [[action]] $\rho : P \times G \to G$ of $G$ on $P$.


## Examples

A standard example of a nontrivial [[circle group]]-principal bundle -- a [[circle bundle]] -- is the [[Hopf fibration]] $S^3 \to S^2$, which has the structure of an $S^1$-principal bundle in [[topological space]]s.

Generally, if we accept that we have a large supply of conttinuous maps between [[topological space]]s, we obtain a $G$-principal bundle $f^* \mathcal{E}G \to X$ on a space $X$ for each continuous map $f : X \to \mathcal{B}G$ to the [[classifying space]] of $G$, by [[pullback]] of the [[generalized universal bundle|universal bundle]] $\mathcal{E}G \to \mathcal{B}G$ along $f$.


## Higher generalizations

In [[higher category theory]] the notion of principal bundle has various [[vertical categorification]]s. See

* [[principal 2-bundle]]

* [[gerbe]]

* [[principal ∞-bundle]]


## Gauge theory

In [[physics]], principal bundles [[connection on a bundle|with connection]] and their higher categorical analogs model [[gauge field]]s. 

In fact, the history of the development of the theory of principal bundles and [[gauge theory]] is closely related. In the early 1930s Dirac and Hopf independently introduced $U(1)$-principal bundles: Dirac, somewhat implicitly, in his study of the [[electromagnetic field]] as a background for [[quantum mechanics]], Hopf in terms of the fibration named after him. However, from there it took apparently many years for the first publication to appear that explicitly states that these two considerations are aspects of the same phenomenon.



[[!redirects principal bundles]]
[[!redirects principal fiber bundle]]
[[!redirects principal fiber bundles]]
[[!redirects principal fibre bundle]]
[[!redirects principal fibre bundles]]