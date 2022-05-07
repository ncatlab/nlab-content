
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
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

  * the [[shear map]] $(p_1, \rho) \colon  P \times G \to P \times_X P$ is an [[isomorphism]], which in turn means that the action is _[[free action|free]]_ and _[[transitive action|transitive]]_ over $X$, hence that each [[fiber]] of $P \to X$ looks like $G$ once we choose a base point;

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

We discuss here principal bundles in the context [[Top]] of [[topological spaces]]. So the group $G$ here is a _[[topological group]]_. 

This is the original and oldest branch of the theory. There is a modern established default of the definition, but many slight but crucial variants exists in the literature and are relevant in applications. We start with the modern default notion and then look into its variants.

$\,$

Let $G$ be a [[topological group]].

+-- {: .num_defn #TrivialTopologicalPrincipalBundle}
###### Definition

The **trivial $G$-principal bundle** on a [[topological space]] $X$ is the [[product]] space $X \times G$ equipped with 

* the [[projection]] map $p_1 : X \times G \to X$ ;

* the [[action]] of $G$ on $X \times G$ by right multiplication of $G$ on itself.

=--

+-- {: .num_defn}
###### Definition

A $G$-**principal bundle** over a [[topological space]] $X$ is a topological space $P$ equipped with

* a [[continuous function]] $p : P \to X$;

* an [[action]] $\rho : P \times G \to P$ of $G$ on $P$ over $X$, hence fitting into a [[coequalizer|coequalizing]] [[diagram]]

  $$
    \array{
      P \times G
      \\
      {}^{\mathllap{p_1}} \downarrow \downarrow^{\mathrlap{\rho}}
      \\
      P
      \\
      \downarrow^{\mathrlap{p}}
      \\
      X
    }
  $$

such that this is _locally trivial_ in the sense that

* there exists a [[cover]] $U \to X$  and a [[continuous map]] $P|_U \to U \times G$ from the [[pullback]] of $P$ to the cover to the trivial $G$-pricipal bundle on the cover, 
def. \ref{TrivialTopologicalPrincipalBundle}, which is an [[isomorphism]] of $G$-[[actions]] over $U$

$$
  \array{
    U \times G& \stackrel{\simeq_G}{\leftarrow}
     & P|_Y &\to& P
    \\ 
    &{}_{\mathllap{p_1}}\searrow&\downarrow && \downarrow^{\mathrlap{p}}
    \\
    &&U &\to& X
  }
  \,.
$$

=--

In the [references](#References) listed below, this appears for instance as ([Mitchell, section 2](#Mitchell), ...)

A central property of the above definition of principal bundle is

+-- {: .num_prop}
###### Proposition

For $P \to X$ a $G$-principal bundle, it is naturally [[isomorphism|isomorphic]] to the [[quotient]] projection 
$P \to P/G \simeq X$ of the $G$-[[action]].

=--

\begin{remark}\label{CartanPrincipalBundles}
**(Cartan principal bundles)**

Historically this quotient property of a free continuous action was sometimes taken as the very definition of "principal bundle" without requiring [[local triviality]], e. g. in ([Cartan, 1949-1950](#Cartan)), where this perspective is attributed to [[Henri Cartan]]. A standard modern textbook following this tradition is ([Husem&#246;ller](#Husemoeller)).

Therefore in order to avoid ambiguous terminology in the following, we will now follow ([Palais 61, Def. 1.1.2](#Palais61)) and refer to this alternative definition of principal bundle as that of _Cartan principal bundle_:

\end{remark}

+-- {: .num_defn}
###### Definition

Let $G$ be a [[locally compact topological group]] and $P$ a [[completely regular topological space]] equipped with a [[continuous function]] [[action]] $\rho : P \times G \to P$. 
If $G$ acts _[[free action|freely]]_ on $P$, (no element $g \in G$ except the neutral element has any fixed points in $P$ under the action) then the [[coprojection]] 

$$
  P \to P/G =: X
$$

to the [[quotient topology|topological quotient]] is called a **$G$-principal bundle in the wide sense**. If furthermore the division map

$$
  P \times_X P \to G
$$

is a [[continuous function]], then this is called a **Cartan principal bundle** ([Palais 61, around theorem 1.1.3](#Palais61)), following ([Cartan](#Cartan)).

(...)

=--





### In a $(2,1)$-topos
 {#InA2Topos}

It is no surprise that there is a good theory of principal bundles internal to every [[topos]]. However, it turns out that the most "natural home" of the theory is the [[higher category theory|higher category theoretic]] context of a _[[(2,1)-topos]]_ $\mathbf{H}$. This we discuss now, and then relate it to the traditional notion and to various other generalizations. More along these lines is at _[[geometry of physics -- principal bundles]]_.

Notably the existence of [[universal principal bundles]] finds its fundamental "explanation" here, where they are seen to be but a presentation of the construction of the [[homotopy fiber]] functor, which establishes the [[equivalence of categories|equivalence of groupoids]]

$$
  \mathbf{H}(X, \mathbf{B}G) \stackrel{\simeq}{\to} G Bund(X)
  \,,
$$

where on the left we have the [[groupoid]] of [[cocycles]] with coefficients in the internal [[delooping]] $\mathbf{B}G$ of the [[group object in an (infinity,1)-category|group object]] $G$: the [[moduli stack]] of $G$-principal bundles.

In this context, all of the non-natural aspects of the traditional theory of principal bundles disappear, for instance 

* _every_ $G$-principal bundle is locally trivial in a $(2,1)$-topos $\mathbf{H}$;

* accordingly there is no mismatch between the various definitions anymore as in the context of topological spaces: the condition of principality becomes equivalent to the quotient space condition.

Moreover, all these fact are fairly direct consequences simply of the [[Giraud axioms]] that characterize [[(2,1)-toposes]] in the first place.

Conversely, the traditional theory nicely naturally embeds into a [[(2,1)-topos]] -- for instance that of [[(2,1)-sheaves]] over the [[site]] [[Top]] (or rather some [[small site|small]] [[dense subsite]]   thereof) -- and the higher topos theory helps to study it there. 

The failure of various definitions to match in the traditonal context becomes the fact that the [[colimits]] involved get "corrected" to [[homotopy colimits]] after embedding into a [[(2,1)-topos]]. For instance if an $G$-[[action]] on some object $P$ is not suitably free, then the $(2,1)$-topos theory still produces a healthy principal bundle by replacing the base space by a base [[groupoid]]/[[stack]]. In fact, this way _every_ action becomes principal over its [[homotopy colimit|homotopy quotient]]. Notably the trivial $G$-action on the [[terminal object]] $*$ becomes principal over the [[action groupoid]] $*//G$ and the resulting $G$-principal bundle is nothing but the [[universal principal bundle|universal]] one.

As the notation suggests, thus formulating the theory in [[(2,1)-topos]] theory immediately generalizes it to [[(∞,1)-topos theory]]. This is discussed at _[[principal ∞-bundle]]_.

(...)

> The following is old material collected from elsewhere that is going to be rearranged....

#### In terms of fiber sequences

This indicates the more fundamental way to _define_ $G$-principal bundles in the first place:
 
Recall (from [[fiber sequence]]) that for every [[group]] there is the one-object [[groupoid]] $\mathbf{B}G$. Under the [[Yoneda embedding]] this [[representable functor|represents]] a [[simplicial presheaf|prestack]]. Write $\bar{\mathbf{B}G}$ for the corresponding [[stack]] obtained by [[(infinity,1)-sheafification|stackification]]. This is our $G Bund(-)$

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
  \cdots G \times G \stackrel{\stackrel{d_2}{\longrightarrow}}{\stackrel{\stackrel{d_1}{\longrightarrow}}{\stackrel{d_0}{\longrightarrow}}}
  G \stackrel{\stackrel{d_1}{\longrightarrow}}{\stackrel{d_0}{\longrightarrow}}
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
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
    &
     P \times G
    &
    \stackrel{\longrightarrow}{\longrightarrow}
    &
    P
    &
    \stackrel{}{\longrightarrow}
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
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
    &
     G
    &
    \stackrel{\longrightarrow}{\longrightarrow}
    &
    {*}
    &
    \stackrel{}{\longrightarrow}
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
   \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
   P \times G 
    \stackrel{\stackrel{\rho}{\longrightarrow}}{\stackrel{p_1}{\longrightarrow}}
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
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
    &
     P \times_X P
    &
    \stackrel{\longrightarrow}{\longrightarrow}
    &
    P
    &
    \stackrel{}{\longrightarrow}
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
    \stackrel{\to}{\stackrel{\longrightarrow}{\longrightarrow}}
    &
     P \times G
    &
    \stackrel{\stackrel{\rho}{\longrightarrow}}{\longrightarrow}
    &
    P
    &
    \stackrel{}{\longrightarrow}
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
    \stackrel{\to}{\stackrel{\longrightarrow}{\longrightarrow}}
    &
     G
    &
    \stackrel{\longrightarrow}{\longrightarrow}
    &
    {*}
    &
    \stackrel{}{\longrightarrow}
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
 {#UnwindingTheAbstractDefinition}

We now rederive the [[action]] $\rho$ of $G$ on $P$ given just the classifying map $X \to \mathbf{B} G$ by spelling out the details implied by the above abstract description.

Whatever the precise context is (topological, smooth, etc.) we may assume that we are at least in a [[category of fibrant objects]]. Then the classifying morphism $X \to \mathbf{B}G$ is represented by an [[anafunctor]], namely a cocycle

$$
  \array{
    C(U) &\stackrel{g}{\to} & \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\in W \cap F}}
    \\
    X
  }
$$

in [[?ech cohomology]] coming from some [[cover]] $\{U_i \to X\}$ of $X$.

The [[?ech nerve]] $C(U)$ has

* objects = $\{(x,i) | x \in U_i\}$

* morphisms = $\{ (x,i) \stackrel{}{\longrightarrow} (x,j) | x \in U_{i j}\}$ .

The [[functor]] $g : C(U) \to \mathbf{B}G$ sends

$$
  g : ((x,i) \to (x,j)) \mapsto (\bullet \stackrel{g_{i j}(x)}{\longrightarrow}\bullet )
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
         \bullet &&\stackrel{h}{\longrightarrow}&& \bullet
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
    C(U) &\stackrel{g}{\longrightarrow}&
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

We discuss here aspects of formulating a theory of principal bundles in contexts different from those already discussed above.

(...)

#### Higher generalizations

In [[higher category theory]] the notion of principal bundle has various [[vertical categorification]]s. See

* [[principal 2-bundle]], [[bundle gerbe]]

* [[principal ∞-bundle]]


## Properties

### Gauge groupoid

For $P \to X$ a $G$-principal bundle, 
its **[[Atiyah Lie groupoid]]** is

$$
  ((P \times P)/G
    \stackrel{\stackrel{p\circ p_1}{\to}}{\underset{p \circ p_2}{\to}}
    X
  )
$$

with the evident composition operation.

The principal bundle $P \to X$ is recovered from its 
Atiyah Lie groupoid, up to isomorphism, as the source fiber over
any point.

This is a classical statement due to Ehresmann ... .
See for instance ([Androulidakis](#Androulidakis)).


## Examples

### Hopf fibration

A standard example of a nontrivial [[circle group]]-principal bundle -- a [[circle bundle]] -- is the [[Hopf fibration]] $S^3 \to S^2$, which has the structure of an $S^1$-principal bundle in [[topological space]]s.

### Pullbacks of universal bundles

Generally, if we accept that we have a large supply of continuous maps between [[topological spaces]], we obtain a $G$-principal bundle $f^* \mathcal{E}G \to X$ on a space $X$ for each continuous map $f : X \to \mathcal{B}G$ to the [[classifying space]] of $G$, by [[pullback]] of the [[generalized universal bundle|universal bundle]] $\mathcal{E}G \to \mathcal{B}G$ along $f$.



### Quotients by Lie group actions
 {#QuotientsByLieGroupActions}


We consider [[actions]] by [[topological groups]] and [[Lie groups]].

+-- {: .num_prop #QuotientProjectionForCompactLieGroupActingFreelyOnManifoldIsPrincipa}
###### Proposition

For $X$ a [[smooth manifold]] and $G$ a [[compact Lie group]] equipped with a [[free action|free]] smooth [[action]] on $X$, then the [[quotient]] [[projection]]

$$
  X \longrightarrow X/G
$$

is a $G$-[[principal bundle]] (hence in particular a [[Serre fibration]]).

=--

This is originally due to ([Gleason 50](#Gleason50)). See e.g. ([Cohen, theorem 1.3](#Cohen))




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

### Coset projections
 {#CosetSpaces}

We discuss principal bundles of the form $P \to P/G$ for $G \hookrightarrow P$ a [[subgroup]] of a [[topological group]], hence with base space a [[coset]] space.

+-- {: .num_prop #QuotientProjectionForCompactLieSubgroupIsPrincipal}
###### Proposition

For $G$ a [[Lie group]] and $H \subset G$ a [[compact Lie group|compact]] [[subgroup]], then the [[coset]] [[quotient]] [[projection]]

$$
  G \longrightarrow G/H
$$

is an $H$-[[principal bundle]] (hence in particular a [[Serre fibration]]).  

=--

This is a direct corollary of prop. \ref{QuotientProjectionForCompactLieGroupActingFreelyOnManifoldIsPrincipa}.
Originally this statement is due to ([Samelson 41](#Samelson41)). 

+-- {: .num_prop #ProjectionOfCosetsIsFiberBundleForClosedSubgroupsOfCompactLieGroup}
###### Proposition

For $G$ a [[compact Lie group]] and $K \subset H \subset G$ [[closed subspace|closed]] [[subgroups]], then the [[projection]] map

$$
  p \;\colon\; G/K \longrightarrow G/H
$$

is a locally trivial $H/K$-[[fiber bundle]] (hence in particular a [[Serre fibration]]).

=--

+-- {: .proof}
###### Proof

Observe that the projection map in question is equivalently

$$
  G \times_H (H/K) \longrightarrow G/H
  \,,
$$

(where on the left we form the [[Cartesian product]] and then divide out the [[diagonal action]] by $H$). This exhibits it as the $H/K$-[[fiber bundle]] [[associated bundle|associated]] to the $H$-[[principal bundle]] of corollary \ref{QuotientProjectionForCompactLieSubgroupIsPrincipal}.

=--



+-- {: .num_prop }
###### Proposition

If $P$ is a [[topological group]] and $G \hookrightarrow P$
a closed [[Lie group|Lie]] subgroup, then the quotient map
$P \to P/G$ is a locally trivial $G$-principal bundle.

=--

This is a corollary of theorem \ref{PalaisTheorem} ([Palais 61](#Palais61)).



Examples where $P \to P/G$ is **not** locally trivial are in 
([Karube](#Karube)), see also ([Mostert](#Mostert)):

+-- {: .num_example }
###### Example (counter example)

Let $P$ be the [[product]] of infinitely many [[circles]], and let $G$ be the product of their [[order]] 2 [[subgroups]]. This cannot have local  [[section]] because $P$ is [[locally connected topological space|locally connected]] and $G$ is not. Therefore $P$ is not even locally [[homeomorphism|homeomorphic]] to $(P / G) \times G$. 

=--



## Gauge theory

In [[physics]], principal bundles [[connection on a bundle|with connection]] and their higher categorical analogs model [[gauge fields]]. See at _[[fiber bundles in physics]]_.

In fact, the history of the development of the theory of principal bundles and [[gauge theory]] is closely related. In the early 1930s Dirac and Hopf independently introduced $U(1)$-principal bundles: Dirac, somewhat implicitly, in his study of the [[electromagnetic field]] as a background for [[quantum mechanics]], Hopf in terms of the fibration named after him. However, from there it took apparently many years for the first publication to appear that explicitly states that these two considerations are aspects of the same phenomenon.


## Related concepts

* **([[formally principal bundle|formally]]) principal bundle** / ([[pseudo-torsor|pseudo]]-)[[torsor]] / [[groupoid principal bundle]] / [[associated bundle]]
  
  * [[universal principal bundle]]

  * [[caloron correspondence]]

  * [[Galois cover]]

  * [[bibundle]]

  * [[groupoid principal bundle]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[2-gerbe]] /  [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]] / [[∞-gerbe]]

  [[universal principal ∞-bundle]]
* [[noncommutative principal bundle]]

* [[n-vector bundle]]


[[!include gauge field - table]]


* [[horizontal differential form]]

* [[basic differential form]]

* [[equivariant de Rham cohomology]]

## References
 {#References}

### General

An original reference on the notion of a principal bundle as a quotient map by a free continuous action of a topological group is 

* {#Cartan} _S&#233;minaire [[Henri Cartan]]_ 1949-1950 *Topologie algébrique* ([numdam:SHC_1948-1949__1](http://www.numdam.org/volume/SHC_1948-1949__1))
  

some of which is recollected in ([Palais 61](#Palais61)).

Further textbooks include

* {#Steenrod51} [[Norman Steenrod]], section I.7 of _The topology of fibre bundles_, Princeton Mathematical Series 14, Princeton Univ. Press, 1951 ([jstor:j.ctt1bpm9t5](https://www.jstor.org/stable/j.ctt1bpm9t5))

* {#Husemoeller} [[Dale Husemöller]], _Fiber bundles_, Springer (1994) ([doi:10.1007/978-1-4757-2261-1](https://doi.org/10.1007/978-1-4757-2261-1))
 
* [[Dale Husemoeller]], [[Michael Joachim]], [[Branislav Jurco]], [[Martin Schottenloher]], _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Lecture Notes in Physics, Springer 2008 ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726corr1.pdf))

* [[Ralph Cohen]], _The topology of fiber bundles_, Stanford University (2017) ([pdf](http://math.stanford.edu/~ralph/fiber.pdf), [OMN:201707.110706](https://www.ams.org/open-math-notes/omn-view-listing?listingId=110706))


With an eye towards application in [[mathematical physics]]:

* [[Mikio Nakahara]], Chapter 9 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)

* [[Gerd Rudolph]], [[Matthias Schmidt]], Section 1.1: *Differential Geometry and Mathematical Physics Part II. Fibre Bundles, Topology and Gauge Fields*, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))

For principal bundles in the smooth context see most textbooks on _[[differential geometry]]_, for instance

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)

also around section 3.1 of 

* {#Moerdijk} [[Ieke Moerdijk]], _On the classification of regular Lie groupoids_ ([pdf](http://igitur-archive.library.uu.nl/math/2007-0201-202453/moerdijk_02_on_the_classification.pdf))

Questions related to the existence [[slice theorem|slices]] of [[topological G-spaces]], of sections of $G$-bundles and conditions for [[proper map|properness]] of some related maps are treated in 

* {#Palais61} [[Richard Palais]], _On the Existence of Slices for Actions of Non-Compact Lie Groups_, Annals of Mathematics
Second Series, Vol. 73, No. 2 (Mar., 1961), pp. 295-323 ([jstor:1970335](https://www.jstor.org/stable/1970335), [doi:10.2307/1970335](https://doi.org/10.2307/1970335), [pdf](http://vmm.math.uci.edu/ExistenceOfSlices.pdf))


 
Lecture notes on principal bundles include

* {#Mitchell}  Stephen A. Mitchell, _Notes on principal bundles and classifying spaces_, 2011 ([pdf](https://sites.math.washington.edu/~mitchell/Notes/prin.pdf), [[MitchellPrincipalBundles.pdf:file]])


* {#Cohen} R. Cohen, _Topology of fiber bundles_, Lecture notes ([pdf](http://math.stanford.edu/~ralph/fiber.pdf))

### In general categories

* [[Anders Kock]], _Fibre bundles in general categories_, Journal of Pure and Applied Algebra 56(3):233-245, 1989; _Generalized fibre bundles_, in: Categorical Algebra and its Applications, Lecture Notes in Mathematics 1348, pp 194-207 (2006)
* C. Townsend, _Principal bundles as Frobenius adjunctions with application to geometric morphisms_, Math. Proc. Camb. Phil. Soc. 159(03) (2015), 433-444 [pdf](http://www.christophertownsend.org/Documents/Principal.pdf)

* [[Tomasz Brzezinski]], _On synthetic interpretation of quantum principal bundles_, AJSE D - Mathematics 35(1D): 13-27, 2010 [arxiv:0912.0213](http://uk.arxiv.org/abs/0912.0213)

### In relation to Lie groupoids
 {#ReferencesInRelationToLieGroupoids}

Discussion of [[Atiyah Lie groupoids]] associated to principal bundles and the reconstruction of principal bundles from their Atiyah Lie groupoids is due to 

* Ehresmann, ...

Further discussion along these lines is for instance in 

* [[Iakovos Androulidakis]], _Classification of extensions of principal bundles and transitive Lie groupoids with prescribed kernel and cokernel_ ([arXiv:math/0402007](http://arxiv.org/abs/math/0402007))
 {#Androulidakis}

### Examples

Discussion of topological quotients of groups $G \to G/H$ as principal $H$-bundles is in 

* {#Gleason50} [[Andrew Gleason]], _Spaces with a compact Lie group of transformations_, Proc. of A.M.S 1, (1950), 35 - 43.

* [Palais 61](#Palais61) 

Explicit examples and counter examples of coset principal bundles are discussed in 

* Takashi Karube, _On the local cross-sections in locally compact groups_, J. Math. Soc. Japan 10 (1958) 343&#8211;347 ([Euclid](http://projecteuclid.org/euclid.jmsj/1261148669))
 {#Karube}

* Paul Mostert, _Local cross sections  in locally compact groups_ ([pdf](http://www.pages.drexel.edu/~gln22/Local%20Cross%20Sections%20in%20Locally%20Compact%20Groups.pdf))
 {#Mostert}

Relations between classes of continuous and of smooth principal bundles are discussed in

* Christoph M&#252;ller, [[Christoph Wockel]], _Equivalences of smooth and continuous principal bundles with infinite-dimensional structure groups_, Advances in Geometry. Volume 9, Issue 4, Pages 605&#8211;626 (2009)

### Extensions
 {#ReferencesExtensions}

Extensions of principal bundles are discussed for instance in

* [[Kirill Mackenzie]], _On extensions of principal bundles_, Annals of Global Analysis and Geometry Volume 6, Number 2 (1988),

* I. Androulidakis, _Classification of extensions of principal bundles and transitive Lie groupoids with prescribed kernel and cokernel_, J. Math. Phys. 45, 3995 (2004); ([pdf](http://users.uoa.gr/~iandroul/A-gpdextnclass.pdf))


### Automorphism groups

The [[automorphism groups]] of principal bundles are discussed for instance in 

* M.C. Abbati, R. Cirelli, A. Mania, P. Michor _The Lie group of automorphisms of a principal bundle_ 1989 JGP **6** 215 ([pdf](http://www.mat.univie.ac.at/~michor/AutomorphismPrincipleBundle.pdf), [doi](http://dx.doi.org/10.1016/0393-0440%2889%2990015-6))



[[!redirects principal bundles]]
[[!redirects principal fiber bundle]]
[[!redirects principal fiber bundles]]
[[!redirects principal fibre bundle]]
[[!redirects principal fibre bundles]]