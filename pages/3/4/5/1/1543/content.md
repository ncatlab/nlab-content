
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

For $G$ a [[group]] ([[internalization|internal]] to some [[category]], traditionally that of [[topological spaces]]) and $X$ some other object, a _$G$-principal bundle_  over $X$ -- also called a $G$-[[torsor]] over $X$ -- is a [[bundle]] $P \to X$ equipped with a $G$-[[action]] $\rho : P \times G \to P$ on $P$ over $X$, such that 

* the action is _principal_ meaning that 

  * the canonical morphism $(p_1, \rho) :  P \times G \to P \times_X P$ is an [[isomorphism]], which in turn means that the action is _free_ and _transitive_ over $X$, hence that each [[fiber]] of $P \to X$ looks like $G$ once we choose a base point;

  and / or / equivalently (depending on technical details, see below)

  * $P \to X$ is isomorphic to the [[quotient]] map $P \to P/G$.

and usually it is required that

* the bundle is _locally trivial_ in that there is a [[cover]] $\phi : U \to X$ and an isomorphism of $G$-actions between the [[pullback]] $\phi^* P$ and the _trivial $G$-principal bundle_ $U \times G \to U$ over $U$.

A central property of $G$-principal bundles over $X$ is that they are a geometric model of the degree-1 [[nonabelian cohomology]] of $X$ with coefficients in $G$. More precisely (subject to some technical details discussed below) there is a [[natural isomorphism]]

$$
  H^1(X, G) \simeq G Bund(X)/{\sim}
$$

between the degree-1 $G$-[[cohomology]] of $X$ and the [[isomorphism classes]] of $G$-principal bundles over $X$. 

The "naturality" of this relation is more pronounced when one refines it from cohomology to [[cocycle]] [[groupoids]]. This is discussed below in [some section](#SomeSection),


## Definition

We discuss first the definition of principal bundles

* [In the category of topological spaces](#InTopologicalSpaces)

This is historically and traditionally the default setup. But the theory exists in and is usefully regarded from a more abstract perspective, which, most naturally, is that of a [[(2,1)-topos]]. This we introduce and discuss in detail in

* [In an (2,1)-topos](#InA2Topos).

Finally in 

* [Other internalizations](#OtherInternalizations)

we discuss how the traditional setup and many other contexts are recovered from and illuminated by that abstract perspective.


### In the category of topological spaces
 {#InTopologicalSpaces}

#### As principal actions

Let $G$ be a [[topological group]] and $X$ a [[topological space]].

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

#### As quotient maps
 {#AsQuotients}

A central property of the above definition of principal bundle is

+-- {: .num_prop}
###### Proposition

If $P \to X$ is a $G$-principal bundle, then it is [[isomorphism|isomorphic]] to the [[quotient]] projection 
$P \to P/G \simeq X$.

=--

Some authors (e.g. [Husem&#246;ller](#Husemoeller)) take this to be the _definition_ of  "principal bundle" (requiring the action to be free and continuous) and explicitly speak of "locally trivial principal bundle" if the local triviality condition is added. This notion (quotient map of a free continuous action) is called a _Cartan principal bundle_ in ([Palais](#Palais)), referring to ([Serre, 1949-1950](#Serre)).




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


### In a $(2,1)$-topos
 {#InA2Topos}

(...)


#### In terms of fiber sequences

This indicates the more fundamental way to _define_ $G$-principal bundles in the first place:
 
Recall (from [[fiber sequence]]) that for every [[group]] there is the the one-object [[groupoid]] $\mathbf{B}G$. Under the [[Yoneda embedding]] this [[representable functor|represents]] a [[simplicial presheaf|prestack]]. Write $\bar{\mathbf{B}G}$ for the corresponding [[stack]] obtained by [[(infinity,1)-sheafification|stackification]]. This is our $G Bund(-)$

$$
  G Bund(-) = \bar{\mathbf{B} G}(-)
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

The homotopy pullback here is conveniently and traditionally computed as an ordinary pullback of a [[fibration|fibrant replacement]] of the pullback diagram. The canonical such fibrant replacement is obtained by replacing ${*} \to \mathbf{B}G$ by $\mathbf{E}G \to \mathbf{B}G$, with $\mathbf{E}G$ an object [[weak equivalence|weakly equivalent]] to the point, called the **$G$-[[universal principal bundle]]**. 

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

So every $G$-principal bundle $P \to X$ is the pullback along a classifying map $X \to \mathbf{B}G$ (in the right $(\infty,1)$-categorical context, otherwise a span such as an [[anafunctor]]) of the $G$-[[universal principal bundle]].

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

where all squares formed by the lowest horizontal morphisms are [[homotopy pullback]] squares, by construction, and where the remaining horizontal morphisms in the top row are induced by the universal property of the [[homotopy pullback]] and the morphisms downstairs.

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



#### Unwinding the abstract description

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

### Other internalizations
 {#Other internalizations}


## Examples

### Hopf fibration

A standard example of a nontrivial [[circle group]]-principal bundle -- a [[circle bundle]] -- is the [[Hopf fibration]] $S^3 \to S^2$, which has the structure of an $S^1$-principal bundle in [[topological space]]s.

### Pullbacks of universal bundles

Generally, if we accept that we have a large supply of continuous maps between [[topological spaces]], we obtain a $G$-principal bundle $f^* \mathcal{E}G \to X$ on a space $X$ for each continuous map $f : X \to \mathcal{B}G$ to the [[classifying space]] of $G$, by [[pullback]] of the [[generalized universal bundle|universal bundle]] $\mathcal{E}G \to \mathcal{B}G$ along $f$.



### Quotients by Lie group actions
 {#QuotientsByLieGroupActions}


We consider [[topological group]] [[actions]] $G$ on $P$ where $G$ is equipped with the structure of a [[Lie group]].

+-- {: .num_theorem #PalaisTheorem}
###### Theorem

Let $P$ be a [[completely regular topological space]] and let $G$ be a [[Lie group]] equipped with a free [[action]] on $P$. Then the [[quotient]] map $P \to P/G$
is a $G$-principal bundle -- in that it is locally trivial  -- precisely if the division map

$$
 P \times_{P/G} P \to G
$$

is a [[continuous function]].

=--

This is ([Palais, theorem 4.1](#Palais)).

### Coset spaces
 {#CosetSpaces}

We discuss principal bundles of the form $P \to P/G$ for $G \hookrightarrow P$ a [[subgroup]] of a [[topological group]].

+-- {: .num_prop }
###### Proposition

If $P$ is a [[topological group]] and $G \hookrightarrow P$
a closed [[Lie group|Lie]] subgroup, then the quotient map
$P \to P/G$ is a locally trivial $G$-principal bundle.

=--

This is a corollary of theorem \ref{PalaisTheorem} ([Palais](#Palais)).

Examples where $P \to P/G$ is **not** locally trivial re in 
[Karube](#Karube). See also ([Mostert](#Mostert)).


+-- {: .num_example }
###### Example


Let $P$ be the [[product]] of infinitly many [[circles]], and let $G$ is the product of their [[order]] 2 subgroups. This cannot have local  [[section]] because $P$ is [[locally connected topological space|locally connected]] and $G$ is not. Therefore $P$ is not even locally [[homeomorphism|homeomorphic]] to $(P / G) \times G$. 

=--


## Higher generalizations

In [[higher category theory]] the notion of principal bundle has various [[vertical categorification]]s. See

* [[principal 2-bundle]]

* [[gerbe]]

* [[principal ∞-bundle]]


## Gauge theory

In [[physics]], principal bundles [[connection on a bundle|with connection]] and their higher categorical analogs model [[gauge field]]s. 

In fact, the history of the development of the theory of principal bundles and [[gauge theory]] is closely related. In the early 1930s Dirac and Hopf independently introduced $U(1)$-principal bundles: Dirac, somewhat implicitly, in his study of the [[electromagnetic field]] as a background for [[quantum mechanics]], Hopf in terms of the fibration named after him. However, from there it took apparently many years for the first publication to appear that explicitly states that these two considerations are aspects of the same phenomenon.


## Related concepts

* **principal bundle** / [[torsor]] / [[groupoid principal bundle]] / [[associated bundle]]
  
  [[universal principal bundle]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[2-gerbe]] /  [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]] / [[∞-gerbe]]

  [[universal principal ∞-bundle]]

* [[n-vector bundle]]

## References

### General

An original reference on the notion of a principal bundle as a quotient map by a free continuous action of a topological group is 

* [[Jean-Pierre Serre]], _Seminar Cartan_ 1949-1950
 {#Serre}

A standard textbook is

* [[Dale Husemöller]], _Fiber bundles_ 
 {#Husemoeller}

A classical reference for smooth principal bundles is for instance

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)

### Examples

Detailed discussion of topological quotients of groups $G \to G/H$ as principal $H$-bundles is in 

* [[Richard Palais]], _On the existence of slices for actions of non-compact Lie groups_, _Annals of mathematics vol 73 no 2 (1961) _ ([pdf](http://vmm.math.uci.edu/ExistenceOfSlices.pdf))
 {#Palais}

Explicit examples and counter examples of coset principal bundles are discussed in 

* Takashi Karube, _On the local cross-sections in locally compact groups_, J. Math. Soc. Japan 10 (1958) 343&#8211;347 ([Euclid](http://projecteuclid.org/euclid.jmsj/1261148669))
 {#Karube}

* Paul Mostert, _Local cross sections  in locally compact groups_ ([pdf](http://www.pages.drexel.edu/~gln22/Local%20Cross%20Sections%20in%20Locally%20Compact%20Groups.pdf))
 {#Mostert}

### Automorphism groups

The [[automorphism groups]] of principal bundles are discussed for instance in 

* M.C. Abbati, R. Cirelli, A. Mania, _The Lie group of automorphisms of a principal bundle_ ([pdf](http://www.mat.univie.ac.at/~michor/AutomorphismPrincipleBundle.pdf))


[[!redirects principal bundles]]
[[!redirects principal fiber bundle]]
[[!redirects principal fiber bundles]]
[[!redirects principal fibre bundle]]
[[!redirects principal fibre bundles]]