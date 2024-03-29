
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn }
###### Definition

The **Sierpinski [[topos]]** is the [[arrow category]] of [[Set]]. 

Equivalently, this is the [[category of presheaves]] over the [[interval category]] $\Delta[1] := \mathbf{2} = \{0 \to 1\}$, or equivalently the [[category of sheaves]] over the [[Sierpinski space]] $Sierp$

$$
  Sh(Sierp) \simeq PSh(\Delta[1]) \simeq Set^{\Delta[1]}
  \,.
$$

Yet another description is that it is the [[Freyd cover]] of **Set**.

=--

+-- {: .num_defn}
###### Definition

Similarly, the **Sierpinski [[(∞,1)-topos]]** is the [[arrow (∞,1)-category]] $\infty Grpd^{\Delta[1]}$ of [[∞Grpd]]. 

Equivalently this is the [[(∞,1)-category of (∞,1)-presheaves]] on $\Delta[1]$ and equivalently the [[(∞,1)-category of (∞,1)-sheaves]] on $Sierp$:

$$
  Sh_{(\infty,1)}(Sierp)
  \simeq
  PSh_{(\infty,1)}(\Delta[1])
  \simeq
  \infty Grpd^{\Delta[1]}
  \,.
$$

=--

## Properties

### Presentation and Homotopy type theory

Being a [[(∞,1)-category of (∞,1)-functors]], the Sierpinski [[(∞,1)-topos]] is [[presentable (∞,1)-category|presented]] by any of the [[model structure on simplicial presheaves]]  $[\Delta[1], sSet]$.

Specifically the [[Reedy model structure]] of [[simplicial presheaves]] on the [[interval category]] $[\Delta[1], sSet]_{Reedy}$ provides a [[univalence|univalent]] model for [[homotopy type theory]] in the Sierpinski $(\infty,1)$-topos ([Shulman](#Shulman))

### Connectedness, locality, cohesion
 {#Cohesion}

We discuss the connectedness, locality and cohesion of the Sierpinski topos. We do so relative to an arbitrary [[base topos]]/[[base (∞,1)-topos]] $\mathbf{H}$, hence regard the [[global section geometric morphism]] 

$$
  \mathbf{H}^I \to \mathbf{H}
  \,.
$$

+-- {: .num_prop}
###### Proposition

The Sierpinski topos is a _[[cohesive topos]].

The Sierpinski $(\infty,1)$-topos is a [[cohesive (∞,1)-topos]].

$$
  (\Pi \dashv \Disc \dashv \Gamma \dashv coDisc)
  : 
  \mathbf{H}^I
  \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\leftarrow}}}}
  \mathbf{H}
  \,.
$$

=--

+-- {: .proof}
###### Proof

For the first statement, see the detailed discussion at _[[cohesive topos]]_ _[here](cohesive+topos#FamiliesOfSets)_.

For the second statement, see the discussion at _[[cohesive (∞,1)-topos]]_  _[here](cohesive+%28infinity%2C1%29-topos#CohesiveDiagramToposes)_.

=--

+-- {: .num_remark}
###### Remark

The fact that the Sierpienski $(\infty,1)$-topos is, therefore, in particular 

1. a [[locally ∞-connected (∞,1)-topos]];

1. an [[∞-connected (∞,1)-topos]];

1. a [[local (∞,1)-topos]]

all follow directly from the fact that it is the image, under [[localic reflection]], of the [[Sierpinski space]] (hence that it is [[n-localic (∞,1)-topos|0-localic]], its [[n-truncated|(-1)-truncation]] being the [[frame]] of opens of the Sierpinski space).

That space $Sierp$, in turn,

1. is a [[contractible topological space]];

1. a [[locally contractible topological space]].

1. has a [[focal point]]

which implies the corresponding three properties of the Sierpinski $\infty$-topos above.

=--

+-- {: .num_remark}
###### Remark

By the discussion at _[[cohesive (∞,1)-topos]]_ every such may be thought of as a _fat point_, the abstract _cohesive blob_. In this case, this fat point _is_ the Sierpinski space. This space can be thought of as being the abstract "point with open neighbourhood".

=--

+-- {: .num_remark}
###### Remark


Accordingly, the objects of the Sierpinski $(\infty,1)$-topos may be thought of as [[∞-groupoids]] (relative to $\mathbf{H}$) equipped with the notion of [[cohesive (∞,1)-topos|cohesion]] modeled on this: they are [[bundles]] $[P \to X]$ of [[∞-groupoids]] whose [[fibers]] are regarded as being [geometrically contractible](cohesive+%28infinity%2C1%29-topos+--+structures#Homotopy), in that

$$
  \Pi([P \to X]) \simeq X
$$

and so in particular

$$
  \Pi([Q \to *]) \simeq *
  \,.
$$

Hence these objects are [[discrete ∞-groupoids]] $X$, to each of whose points $ x : * \to X$ may be attached a contractible cohesive blob with inner structure given by the $\infty$-groupoid $P_x := P \times_X \{x\}$.

Accordingly, the _underlying_ $\infty$-groupoid of such a bundle $[P \to X]$ is the union

$$
  \Gamma([P \to X]) \simeq P
$$

of the discrete base space and the inner structure of the fibers.

The [[discrete object]] in the Sierpinski $(\infty,1)$-topos on an object $X \in \mathbf{H}$ is the bundle 

$$
  Disc(X) \simeq [X \stackrel{id}{\to} X]
$$ 

which is $X$ with "no cohesive blobs attached".

Finally the [[codiscrete object]] in the Sierpinski $(\infty,1)$-topos on an object $X \in \mathbf{H}$ is 

$$
  coDisc(X) \simeq [X \to *]
  \,,
$$ 

the structure where all of $X$ is regarded as one single contractible cohesive ball.

The $(\Pi \dashv Disc)$-[[unit |adjunction unit]] 

$$
  i :  id \to Disc \Pi
$$ 

on $[P \to X]$ is

$$
  \array{
    \mathllap{[}P &\to& X\mathrlap{]}
    \\
    \downarrow && \downarrow
    \\
    \mathllap{[}X &\to& X\mathrlap{]}
  }
  \,.
$$

The $(Disc  \dashv \Gamma)$-counit $ Disc \Gamma  \to id$ on $[P \to X]$ is

$$
  \array{
    \mathllap{[}P &\to& P\mathrlap{]}
    \\
    \downarrow && \downarrow
    \\
    \mathllap{[}P &\to& X\mathrlap{]}
  }
  \,.
$$


Hence the canonical [[natural transformation]]

$$
  \array{
    \Gamma && \to && \Pi
    \\
     & {}_{\mathllap{\Gamma(i)}}\searrow & & \nearrow_{\mathrlap{\simeq}}
     \\
     && \Gamma Disc \Pi
  }
$$

from "points to pieces" is on $[P \to X]$ simply the morphism $P \to X$ itself

$$
  (\Gamma \to \Pi)([P \to X]) = (P \to X)
  \,.
$$

Therefore

1. the [[full sub-(∞,1)-category]] on those objects in $\mathbf{H}^I$ for which "[pieces have points](cohesive%20%28infinity,1%29-topos#PiecesHavePoints)", hence those for which $\Gamma \to \Pi$ is an [[effective epimorphism in an (∞,1)-category|effective epimorphism]], is the $(\infty,1)$-category of effective epimorphisms in the ambient $(\infty,1)$-topos, hence the $(\infty,1)$-category of [[groupoid object in an (∞,1)-category|groupoid objects]] in the ambient $(\infty,1)$-topos;

1. the full sub-$(\infty,1)$-category on the objects with "[one point per piece](cohesive+topos#ObjectsWithOnePointPerCohesivePiece)" is the ambient $(\infty,1)$-topos itself.

=--

### Cohesive structures

We unwind what some of the canonical  [[cohesive (infinity,1)-topos -- structures|structures in a cohesive (∞,1)-topos]] are when realized in the Sierpinski $(\infty,1)$-topos.

A group object $\mathbf{B}[\hat G \to G]$ in $\mathbf{H}^I$ is a morphism in $\mathbf{H}$ of the form $ = \mathbf{B}\hat G \to \mathbf{B}G$.

The corresponding flat coefficient object $\mathbf{\flat} \mathbf{B}[\hat G \to G] \to \mathbf{B}[\hat G \to G]$ is

$$
  \array{
    \mathbf{\hat G} &\to& \mathbf{B} \hat G
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\hat G} &\to& \mathbf{G}
  }
  \,.
$$

Hence the corresponding de Rham coefficient object is

$$
  \mathbf{\flat}_{dR} \mathbf{B}[\hat G \to G]
  = 
  [* \to \mathbf{B}A]
  \,,
$$

where $A \to \hat G \to G$ exhibits $\hat G$ has an $\infty$-group extension of $G$ by $A$ in $\mathbf{H}$.

The corresponding Maurer-Cartan form 

$$
  [\hat G \to G] \to \mathbf{\flat}_{dR}\mathbf{B}[\hat G \to G]
$$

is 

$$
  \array{
    \hat G &\to& G
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}A
  }
$$

exhibiting the $A$-cocycle that classifies the extension $\hat G \to G$.





### Differential cohesion
 {#DifferentialCohesion}

The leftmost adjoint, $\Pi$, of the string of four adjoints exhibiting cohesion [above](#Cohesion) itself possesses a left adjoint, $X \mapsto [0 \to X]$. Taking this functor along with the leftmost three adjoints of this previous string yields a second quadruple adjunction which exhibits [[differential cohesion]]. 

For $\mathbf{H}$ any [[cohesive (∞,1)-topos]], we have the "Sierpinski $(\infty,1)$-topos relative to $\mathbf{H}$" given by the [[arrow category]] $\mathbf{H}^{\Delta[1]}$, whose [[geometric morphism]] to the [[base topos]] is the [[domain cofibration]]

$$
  \mathbf{H}^{\Delta[1]}
   \stackrel{\overset{const}{\hookleftarrow}}{\underset{dom}{\to}}
   \mathbf{H}
  \,.
$$

Conversely, we may think of $\mathbf{H}^{\Delta[1]}$ as being an "infinitesimal thickening" of $\mathbf{H}$, as formalized at _[[differential cohesion]]_, where we regard

$$
  (i_! \dashv i^* \dashv i_* \dashv i^!)
  : 
  \mathbf{H}
    \stackrel{\overset{\top_!}{\hookrightarrow}}{\stackrel{\overset{\top^*}{\leftarrow}}{\stackrel{\overset{const}{\hookrightarrow}}{\underset{\bot^*}{\leftarrow}}}}
  \mathbf{H}^{\Delta[1]}
$$

as exhibiting $\mathbf{H}^{\Delta[1]}$ as an infinitesimal cohesive neighbourhood of $\mathbf{H}$ (here $(\bot, \top) : \Delta[0] \coprod \Delta[0] \to \Delta[1]$ denotes the endpoint inclusions, following the notation [here](http://ncatlab.org/nlab/show/cohesive+%28infinity,1%29-topos#CohesiveDiagramToposes)).

(See also the corresponding examples at _[[Q-category]]_.)

+-- {: .num_prop #iInclusion}
###### Observation


We have for all $X \in \mathbf{H}$ that

$$
  i_!(X) \simeq [\emptyset \to X]
  \,.
$$

=--

+-- {: .proof}
###### Proof

For all $[A \to B]$ in $\mathbf{H}^{\Delta[1]}$ we have

$$
  \mathbf{H}(X, i^*[A \to B])
  \simeq
  \mathbf{H}(X, cod(A \to B))
  \simeq
  \mathbf{H}(X, B)
  \,,
$$

which is indeed naturally equivalent to

$$
  \mathbf{H}^{\Delta[1]}([\emptyset \to X], [A \to B])
  \,.
$$

=--

Therefore an object of $\mathbf{H}^{\Delta[1]}$ given by a morphism $[P \to X]$ in $\mathbf{H}$ is regarded by the differential cohesion $i : \mathbf{H} \hookrightarrow \mathbf{H}^{\Delta[1]}$ as being an infinitesimal thickening of $X$ by the fibers of $P$: where before we just had that the fibers of $P$ are "contractible cohesive thickenings" of the discrete object $X$, now $X$ is "discrete relative to $\mathbf{H}$" (hence not necessarily discrete in $\mathbf{H}$) and  the fibers are in addition regarded as being infinitesimal.

This is of course a very crude notion of infinitesimal extension. Notice for instance the following

+-- {: .num_prop}
###### Proposition

With respect to the above differential cohesion $i : \mathbf{H} \hookrightarrow \mathbf{H}^{\Delta[1]}$, every morphism in $\mathbf{H}$ is a [[formally étale morphism]].

=--

+-- {: .proof}
###### Proof

By definition, given a morphism $f : X \to Y$, it is formally &#233;tale precisely if 

$$
  \array{
    i_! X &\stackrel{i_! f}{\to}& i_! Y
    \\
    \downarrow && \downarrow
    \\
    i_* X &\stackrel{i_*}{\to}& i_* Y
  }
$$

is an [[(∞,1)-pullback]]. 


By prop. \ref{iInclusion} the above square diagram in $\mathbf{H}^{\Delta[1]}$ is

$$
  \array{
    [\emptyset \to X] &\to& [\emptyset \to Y]
    \\
    \downarrow && \downarrow
    \\
    [X \stackrel{id}{\to} X]
    &\to&
    [Y \stackrel{id}{\to} Y]
  }
  \,.
$$

Since $(\infty,1)$-pullbacks of $(\infty,1)$-presheaves are computed objectwise, this is an $(\infty,1)$-pullback in $\mathbf{H}^{\Delta[1]}$ precisely if the "back and front sides" 

$$
  \array{
    \emptyset &\to& \emptyset
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{f}{\to}& Y
  }
$$

and

$$
  \array{
    X &\stackrel{f}{\to}& Y
    \\
    \downarrow^{\mathrm{id}} && \downarrow^{\mathrm{id}}
    \\
    X &\stackrel{f}{\to}& Y
  }
$$

are $(\infty,1)$-pullbacks in $\mathbf{H}$. This is clearly always the case.

The adjunction $i_{!} \circ i^{\ast} \vdash i_{\ast} \circ i^{\ast}$ forms the [[Aufhebung]] of $\emptyset \vdash \ast$ for the Sierpinski topos.


=--

### As a classifying topos
 {#AsAClassifyingTopos}

The Sierpinski topos is the [[classifying topos]] for [[subterminal objects]] in [[toposes]] (see e.g. [Johnstone 77, p. 117](#Johnstone77)).

The generic subterminal inclusion in the Sierpinski topos is the unique inclusion of $[\emptyset \to \ast]$ into $[\ast  \to \ast]$.

The (non-full) inclusion

$$
  \Delta^1 = \{\ast \to S^0\} \longrightarrow FinSet^{\ast/} \hookrightarrow \infty Grpd_{fin}^{\ast/}
$$

induces via restriction and right [[Kan extension]] an [[essential geometric morphism|essential]] [[geometric morphism]]


$$
  \mathbf{H}^{\Delta^1} \stackrel{\longleftarrow}{\hookrightarrow}
  \mathbf{H}[X_\ast]
$$


of the Sierpinski topos into the [[classifying topos]] for [[pointed objects]], $\mathbf{H}[X_\ast]$. (This becomes a [[geometric embedding]] if we refined the Sierpinski topos of bundles to the topos of bundles with sections).

The pointed object in $\mathbf{H}^{\Delta^1}$ which is classified by this [[geometric morphism]] is $[\ast \to S^0]$ (with $S^0 = \ast \coprod \ast$ the [[0-sphere]]) with its canonical map from $[\ast \to \ast]$.

In summary, the generic subterminal object and the generic pointed object fit into a sequence of the form

$$
  \array{
     \emptyset &\hookrightarrow& \ast &\longrightarrow& \ast
     \\
     \downarrow && \downarrow && \downarrow
     \\
     \ast &\longrightarrow& \ast &\longrightarrow& S^0
  }
$$


###Cohomology

According to the general idea of [[cohomology]], for $\mathbf{H}$ an [[(∞,1)-topos]], and $X, A \in \mathbf{H}$ two [[objects]], cohomology classes of $X$ with coefficients in $A$ are the connected components 

$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
  \,.
$$

Cohomology in the Sierpinski $(\infty, 1)$-topos, $\mathbf{H}^{I}$, corresponds to [[relative cohomology]] in $\mathbf{H}$.

Indeed, let $i : Y \to X$ and $f : B \to A$ be two [[morphisms]] in $\mathbf{H}$. Then the **relative cohomology** of $X$ with coefficients in $A$ relative to these morphisms is the connected components of the $\infty$-groupoid of relative cocycles

$$
  H_{Y}^B(X,A) := \pi_0 \mathbf{H}^I(Y \stackrel{i}{\to} X\;,\; B \stackrel{f}{\to} A)
  \,.
$$

In terms of the [[codomain fibration]], $\mathbf{H}^I \to \mathbf{H}$, intrinsic cohomology can be considered as nonabelian [[twisted cohomology]] (see there).

## References

The Sierpinski topos is mentioned around remarks A2.1.12, B3.2.11 (p.83, p.387f) in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. I_, Oxford UP 2002.

See also

* {#Johnstone77} [[Peter Johnstone]], _Topos theory_, London Math. Soc. Monographs __10__, Acad. Press 1977, xxiii+367 pp.

The [[homotopy type theory]] of the Sierpinski $(\infty,1)$-topos is discussed in 

* {#Shulman} [[Mike Shulman]], _The univalence axiom for inverse diagrams_ ([arXiv:1203.3253](http://arxiv.org/abs/1203.3253)) 
 

Cohesion of the Sierpinski $\infty$-topos is discussed in section 2.2.4 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

[[!redirects Sierpinski (∞,1)-topos]]
[[!redirects Sierpinski (infinity,1)-topos]]
