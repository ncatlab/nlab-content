

> This entry is a sub-chapter of _[[geometry of physics]]_. See there for background

> The following is effectively a derivation of, and an introduction to, [[classical mechanics]] by studying [[correspondences]] in what is called (as we will explain) the _[[slice topos]] over the [[moduli stack]] of [[prequantum line bundles]]_. One such correspondence in this slice topos is precisely a _[[prequantized Lagrangian correspondence]]_ and the reader looking for just these should skip ahead to the section _[The classical action functional prequantizes Lagrangian correspondences](#TheClassicalActionFunctionalPrequantizesHamiltonianCorrespondences)_. But for completeness and to introduce the technology used here, we start with introducing also more basic concepts, such as [[phase space]] etc.


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Classical Mechanics via Prequantum Correspondences#
* table of contents
{:toc}


## Model Layer
 {#ModelLayer}


Here we discuss the notion of _prequantized Lagrangian correspondences_ and how it serves to embed traditional [[classical mechanics]] in its formulation as [[Hamiltonian mechanics]] and [[Lagrangian mechanics]] into the general context of [[local prequantum field theory]] and its [[motivic quantization]].

A traditional notion is that of a plain _[[Lagrangian correspondence]]_, which is a [[Lagrangian submanifold]] of the [[Cartesian product]] of a [[symplectic manifold]] and another one, with opposite [[symplectic structure]]. As discussed there, plain [[Lagrangian correspondences]] naturally generalize [[symplectomorphisms]] -- hence transformations between [[phase spaces]] in [[physics]] -- via [[correspondences]] of [[symplectic manifolds]].

But in [[prequantum field theory]] proper, and in particular with an eye towards [[geometric quantization]], one considers the [[prequantization]] of these symplectic manifolds by lifting them to [[prequantum circle bundles]] with [[principal connection]]. The notion of _prequantized Lagrangian correspondence_ is the refinement of that of plain [[Lagrangian correspondence]] which does properly respect and reflect this [[prequantization]] information: a prequantized Lagrangian correspondence is a [[Lagrangian subspace]] as before, but now equipped with an explicit [[gauge transformation]] between the pullbacks of the two [[prequantum circle bundles]] to the correspondence space.

We discuss below how the concept of prequantized Lagrangian correspondences neatly induces and unifies ingredients and aspects of [[classical mechanics]], notably the [[Hamiltonian mechanics]] of [[symplectic manifolds]] and the [[Lagrangian mechanics]] of [[action functionals]] associated to it via the [[Legendre transform]]. Specifically, below in _[The classical action prequantizes Hamiltonian correspondences](#TheClassicalActionFunctionalPrequantizesHamiltonianCorrespondences)_ we see that prequantized Lagrangian correspondences are [[diagrams]] which schematically express this data as follows:

$$
  \array{
    && {{space\,of} \atop {trajectories}}
    \\
    & {}^{\mathllap{{initial}\atop {values}}}\swarrow && \searrow^{\mathrlap{{Hamiltonian} \atop {evolution}}}
    \\
    phase\,space_{in} && \swArrow_{{action} \atop {functional}} && phase \,space_{out}
    \\
    & {}_{\mathllap{{prequantum}\atop {bundle}_{in}}}\searrow 
    && 
    \swarrow_{\mathrlap{{prequantum} \atop {bundle}_{out}}}
    \\
    && {{2\text{-}group} \atop {of\,phases}}
  }
  \,.
$$

This describes a [[diagram]] in what is called the [[slice topos]] of [[smooth sets]] over the [[moduli stack]] of [[prequantum circle bundles]]. Once formulated this way, there is an evident refinement to [[moduli infinity-stack|higher moduli stacks]] of [[prequantum n-bundles]].

For $n = 2$ we show how the notion of prequantized Lagrangian correspondence is -- still naturally in the context of [[local prequantum field theory]] -- further refined from the context of [[symplectic manifolds]] to that of [[Poisson manifolds]]. Specifically, this is obtained by realizing that prequantized Lagrangian correspondences are really naturally to be regarded as correspondences-of-correspondences in a [[higher category of correspondences|2-category of correspondences]], where now the new lower-order correspondences are instead [[boundary field theories]] for a [[2d Chern-Simons theory]] (a non-perturbative [[Poisson sigma-model]]).  


### Phase spaces and symplectic manifolds
 {#PhaseSpaceAndSymplecticManifolds}

Given a [[physical system]], one says that its _[[phase space]]_ is the
space of its possible ("classical") histories or _[[trajectories]]_. 
The first two of [[Newton's laws of motion]] say that [[trajectories]] of [[physical systems]] are (typically) determined by [[differential equations]] of  _second_ order, and therefore these spaces of trajectories are (typically) equivalent to initial value data of 0th and of 1st derivatives. In [[physics]] this data (or rather its linear dual) is referred to as the _[[canonical coordinates]]_ and the _[[canonical momenta]]_, respectively, traditionally denoted by the symbols "$q$" and "$p$". 
But being [[coordinates]], these are actually far from being canonical in the mathematical sense; all that has invariant meaning is, locally, the surface element $\mathbf{d}p \wedge \mathbf{d}q$ spanned by a change of coordinates and momenta.

So far this says that a physical phase space is mathematically formalized
by a sufficiently [[smooth manifold]] $X$ which is equipped with a closed
and non-degenerate [[differential 2-form]] $\omega  \in \Omega^2_{\mathrm{cl}}(X)$, hence by a [[symplectic manifold]] $(X,\omega)$.


The non-degeneracy of a symplectic form encodes the special property
(as we will make explicit below)
that (time) evolution of coordinates and momenta is uniquely
induced by an [[action functional]]/[[Hamiltonian]] generating the evolution. This is however famously not the case for systems with _[[gauge equivalences]]_, hence such systems which have configurations that are nominally different but nevertheless physically equivalent. Presence of such  gauge equivalences is not the exception,
but the rule for physical systems, and therefore we want to include this case.

In the presence of gauge equivalences, the phase space form
$\omega$ is still a closed differential 2-form, it just need not be 
non-degenerate anymore. While in such a case the pair $(X,\omega)$
could just be called a _smooth manifold equipped with a closed differential 2-form}_, it is traditional to call this a 
_[[pre-symplectic manifold]]_ in order to amplify the indented use as a model for phase spaces. (Some authors demand that a pre-symplectic form be a closed form with constant
rank, but here this technical condition will not be relevant and will not be considered.)




+-- {: .num_example #CanonicalR2PhaseSpace}
###### Example

The [[sigma-model]] describing the propagation of a [[particle]] on the [[real line]] $\mathbb{R}$ has as [[phase space]] the [[plane]] $\mathbb{R}^2 = T^\ast \mathbb{R}$ and as [[symplectic form]] its canonical [[volume form]]. Traditionally the two canonical [[coordinate functions]] on this phase space are denoted $q,p \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}$ (called the "[[canonical coordinate]]" and the "[[canonical momentum]]", respectively), and in terms of these the symplectic form in this example is $\omega = \mathbf{d} q \wedge \mathbf{d} p$.

=--

When dealing with spaces $X$ that are equipped with extra structure, such as  $\omega \in \Omega^2_{\mathrm{cl}}(X)$, then it is useful to have 
a _universal [[moduli space]]_ for these structures, and this will be central for our developments here. 
So we need a "[[smooth set]]" $\mathbf{\Omega}^2_{\mathrm{cl}}$ of sorts, characterized by the property that  there is a [[natural bijection]] between smooth closed differential  2-forms $\omega \in \Omega^2_{\mathrm{cl}}(X)$ and [[smooth maps]]
$
    X \longrightarrow \mathbf{\Omega}^2_{\mathrm{cl}}
$.
Of course such a universal moduli spaces of closed 2-forms does not exist in the  [[category]] of [[smooth manifolds]]. But it does exist canonically if we  slightly generalize the notion of "smooth set" suitably. 

+-- {: .num_defn}
###### Definition

A _[[smooth set]]_ or _smooth 0-type_ $X$ is 

1. an assignment to each $n \in \mathbb{N}$ of a  set, to be written $X(\mathbb{R}^n)$ and to be called the  _set of smooth maps from $\mathbb{R}^n$ into $X$_,

1. an assignment to each ordinary smooth function $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ between Cartesian spaces of  a function of sets $X(f) : X(\mathbb{R}^{n_2}) \to X(\mathbb{R}^{n_1})$, to be called the _pullback of smooth functions into $X$ along $f$_;

such that

1. this assignment respects composition of smooth functions;

1. this assignment respects the [[covering]] of [[Cartesian spaces]] by [[open disks]]: for every [[good open cover]] $\{\mathbb{R}^n \simeq U_i \hookrightarrow \mathbb{R}^n\}_i$, the set $X(\mathbb{R}^n)$ of smooth functions out of $\mathbb{R}^n$ into $X$ is in natural bijection with the set $\left\{ (\phi_i)_i \in \prod_i X(U_i) \;|\;  \forall_{i,j}\; \phi_i|_{U_{i} \cap U_j}   = \phi_j|_{U_{i} \cap U_j} \right\}$ of tuples of smooth functions out of the patches of the cover which agree on all intersections of two patches.

=--

For more on this see at _[[geometry of physics]]_ in the section _[Smooth sets](geometry%20of%20physics#SmoothSpaces)_.

While the formulation of this definition is designed to make transparent its geometric meaning, of course equivalently but more abstractly this says the following:

+-- {: .num_defn #SheavesOnCartSp}
###### Definition

 Write [[CartSp]] for the [[category]] of [[Cartesian spaces]] with 
[[smooth functions]] between them, and consider it as a [[site]] by equipping it with the [[coverage]] of [[good open covers]]. 
A _[[smooth set]]_ or _smooth 0-type_ is a [[sheaf]] on this site. 
The _[[topos]] of smooth 0-types_ is the [[category of sheaves]]
  $$
    \mathrm{Smooth}0\mathrm{Type} \coloneqq \mathrm{Sh}(\mathrm{CartSp})
	\,.
  $$

=--

In the following we will abbreviate the notation to
$$
  \mathbf{H} \coloneqq \mathrm{Smooth}0\mathrm{Type}
  \,.
$$


The topos of prop. \ref{SheavesOnCartSp} also has another site of definition.

+-- {: .num_prop #Smooth0TypeIsSheavesOnSmoothMfd}
###### Proposition

Write $SmoothMfd$ for the [[category]] of [[smooth manifolds]] regarded as a [[site]] with the standard [[Grothendieck topology]] of [[open covers]]. There is an [[equivalence of categories]]

$$
  Sh(SmoothMfd) \simeq \mathrm{Smooth}0\mathrm{Type}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The canonical inclusion $CartSp\hookrightarrow SmoothMfd$ is readily seen to be a [[dense subsite]]. (This is just the statement that -- by definition -- every smooth manifold may be covered by Cartesian spaces.) The statement hence follows by the [[comparison lemma]]. 

=--

For the discussion of presymplectic manifolds, we need the following two 
examples.

+-- {: .num_example}
###### Example

  Every smooth manifold $X \in \mathrm{SmoothManifold}$ becomes
  a smooth 0-type by the assignment 
  $$
    X \;\colon\; n \mapsto C^\infty(\mathbb{R}^n, X)
	\,.
  $$
  This construction extends to a [[full subcategory|full embedding]]
  of [[smooth manifolds]] into [[smooth sets]]
  $$
    SmoothManifold
    \hookrightarrow
    \mathbf{H}
  $$

=--

+-- {: .proof}
###### Proof

This follows via prop. \ref{Smooth0TypeIsSheavesOnSmoothMfd} by the [[Yoneda lemma]].

=--


+-- {: .num_example #SmoothSetOfDifferentialPForms}
###### Example

For $p \in \mathbb{N}$, write $\mathbf{\Omega}^p_{\mathrm{cl}}$
for the [[smooth set]] whose $n$-dimensional plots are
smooth [[differential p-forms]] on $\mathbb{R}^n$:

$$
  \mathbf{\Omega}^p_{\mathrm{cl}} 
  \colon 
  \mathbb{R}^n \mapsto \Omega^p_{\mathrm{cl}}(\mathbb{R}^n)
$$

and which sends a [[smooth function]] $f \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ to the [[pullback of differential forms]] along this map

$$
  \array{
     \mathbb{R}^{n_1}
     &\mapsto&
     \Omega^p_cl(\mathbb{R}^{n_1})
     \\
     \downarrow^{\mathrlap{f}} && \uparrow^{\mathrlap{f^\ast}}
     \\
     \mathbb{R}^{n_2}
     &\mapsto&
     \Omega^p_cl(\mathbb{R}^{n_2})
  }
  \,.
$$

=--

For more on this example see at _[[geometry of physics]]_ in the section _[Differential forms](geometry%20of%20physics#DifferentialForms)_.


This solves the [[moduli problem]] for closed smooth differential forms:


+-- {: .num_prop #PresymplecticFormsAsMapsIntoASmoothSpace}
###### Proposition

For $p \in \mathbb{N}$
and $X \in SmoothManifold \hookrightarrow Smooth0Type$, 
there is a [[natural bijection]]
$$
  \mathbf{H}(X,\mathbf{\Omega}^p_{\mathrm{cl}})
  \simeq
  \Omega^p_{\mathrm{cl}}(X)
$$

between morphisms (of smooth sets)

$$
  X \longrightarrow \Omega^2_{cl}
$$

and smooth closed 2-forms 

$$
  \omega \in \Omega^2_{cl}(X)
$$

on $X$.

=--

+-- {: .proof}
###### Proof

This follows via prop. \ref{Smooth0TypeIsSheavesOnSmoothMfd} by the [[Yoneda lemma]].

=--

So a [[presymplectic manifold]] $(X,\omega)$ is equivalently a map of smooth sets of the form
$$
  \omega \;\colon\;
    X \longrightarrow \mathbf{\Omega}^2_{\mathrm{cl}}
  \,.
$$

### Canonical transformations and symplectomorphisms
 {#CanonicalTransformations}

An [[equivalence]] between two [[phase spaces]], hence a re-expression
of the "[[canonical coordinates]]" and "[[canonical momenta]]", is called a 
_[[canonical transformation]]_ in [[physics]]. Mathematically this is
a _[[symplectomorphism]]_.

+-- {: .num_defn}
###### Definition

Given two [[symplectic manifolds]] $(X_1, \omega_1)$ and $(X_2, \omega_2)$ (which might be two copies of one single symplectic manifold), a _[[symplectomorphism]]_ between them

$$
  f \;\colon\; (X_1, \omega_1) \longrightarrow (X_2, \omega_2)
$$

is a [[diffeomorphism]]

$$
  f \;\colon\; X_1 \longrightarrow X_2
$$

of the underlying [[smooth manifolds]], such that the [[pullback of differential forms|pullback]] of the second [[symplectic form]] along $f$ equals the first, 

$$
  f^\ast \omega_2 = \omega_1
  \,.
$$

=--


The above formulation of pre-symplectic manifolds as maps into a [[moduli space]] of closed [[differential 2-forms]] yields the following formulation of symplectomorphisms,  which is very simple in itself, 
but contains in it the seed of an important phenomenon:


+-- {: .num_prop #Symplectomorphism}
###### Proposition

A [[symplectomorphism]] $f \colon (X_1, \omega_2) \longrightarrow (X_2, \omega_2)$ as above is, under the identification of prop. \ref{PresymplecticFormsAsMapsIntoASmoothSpace}, equivalently a [[commuting diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    X_1 && \stackrel{f}{\longrightarrow}&& X_2
    \\
    & {}_{\mathllap{\omega_1}}\searrow && \swarrow_{\mathrlap{\omega_2}}
    \\
    && \Omega^2_{cl}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is the [[natural transformation|naturality]] of the [[Yoneda lemma]]:

By prop. \ref{PresymplecticFormsAsMapsIntoASmoothSpace} the identification of $\omega_i \in \Omega^2_{cl}(X_i)$ with $\omega_i \colon X \to \Omega^2_{cl}$ is via the [[natural equivalence]]

$$
  Hom_{Smooth0Type}(X,\mathbf{\Omega}^2_{cl})
  \stackrel{\simeq}{\longrightarrow}
  \Omega^2_{cl}(X)
  \,.
$$

This being natural means that for every morphism $X_1 \stackrel{f}{\longrightarrow} X_2$ there is a [[commuting diagram]] of the form

$$
  \array{
      Hom(X_2,\mathbf{\Omega}^2_{cl})
      &\stackrel{\simeq}{\longrightarrow}&
      \Omega^2_{cl}(X_2)
      \\
      \downarrow^{\mathrlap{(-) \circ f}}
      &&
      \downarrow^{\mathrlap{f^\ast}}
      \\
      Hom(X_1,\mathbf{\Omega}^2_{cl})
      &\stackrel{\simeq}{\longrightarrow}&
      \Omega^2_{cl}(X_1)  
  }
$$

where on the left we have the pre-[[composition]] operation on morphisms and on the right we have, by example \ref{SmoothSetOfDifferentialPForms}, the [[pullback of differential forms]].

Consider then the element 

$$
  (X_2 \stackrel{\omega_2}{\to} \mathbf{\Omega}^2_{cl})
  \in
  Hom(X_2,\mathbf{\Omega}^2_{cl})
$$

in the top left set in this diagram. Sending it along the top and right maps yields the [[pullback of differential forms]] $f^\ast \omega_2 \in \Omega^2_{cl}(X_1)$. On the other hand, sending it along the left and bottom maps yields the differential form represented by the composite morphism $(X_1 \stackrel{f}{\to} X_2 \stackrel{\omega_1}{\to}\mathbf{\Omega}^2_{cl})$. Commutativity of the above naturality diagram means that these two elements of $\Omega^2_{cl}(X_1)$ coincide. This is the claim to be proven.

=--

Situations like this are naturally interpreted in a _[[slice topos]]_:

+-- {: .num_defn #TheSliceTopos}
###### Definition

For $A \in \mathbf{H}$ any [[smooth set]],
  the _[[slice topos]]_  $\mathbf{H}_{/A}$ is the [[category]] whose
  [[objects]] are objects $X \in \mathbf{H}$ equipped with [[maps]]
  $X \to A$, and whose [[morphisms]] are [[commuting diagrams]] in $\mathbf{H}$
  of the form
  $$
    \array{
      X &&\longrightarrow&& Y
      \\
      & \searrow && \swarrow
      \\
      && A
    }
  $$

=--

+-- {: .num_defn}
###### Definition


Write $\mathrm{SymplManifold}$ for the [[category]] with
[[symplectic manifold|presymplectic]] [[smooth manifolds]] as [[objects]] and 
[[symplectomorphisms]], def. \ref{Symplectomorphism}, betwen them as [[morphisms]]

=--


+-- {: .num_prop #SymplecticManifoldsAsObjectsInSliceOverModuliOf2Forms}
###### Proposition


The construction of prop. \ref{PresymplecticFormsAsMapsIntoASmoothSpace} 
which sends a smooth symplectic manifold $(X,\omega)$ to the
classifying morphism of smooth sets 
$(X \stackrel{\omega}{\longrightarrow}\mathbf{\Omega}^2_{cl})$
regarded as an object in the [[slice topos]],
def. \ref{TheSliceTopos}
constitutes a [[full and faithful functor]]

$$
  SymplManifold 
   \hookrightarrow 
   Smooth0Type_{/\mathbf{\Omega}^2_{\mathrm{cl}}}
$$

of pre-symplectic manifolds with symplectomorphisms between them into 
the slice topos of smooth sets over the smooth moduli space of
closed differential 2-forms.

=--

+-- {: .proof}
###### Proof

By prop. \ref{Symplectomorphism}.

=--

### Trajectories and Lagrangian correspondences
 {#TrajectoriesAndLagrangianCorrespondences}

A [[symplectomorphism]] clearly puts two [[symplectic manifolds]] "in _[[relation]]_" to each other. But it does so also in the formal sense of [[relations]] in mathematics. Recall:

+-- {: .num_defn}
###### Definition

For $X,Y \in $ [[Set]] two [[sets]], a [[relation]] $R$ between [[elements]] of $X$ and [[elements]] of $Y$ is a [[subset]] of the [[Cartesian product]] set 

$$
  R \hookrightarrow X \times Y
  \,.
$$

More generally, for $X, Y \in \mathbf{H}$ two [[objects]] of a [[topos]] (such as the topos of [[smooth sets]]), then a [[relation]] $R$ between them is a [[subobject]] of their [[Cartesian product]]

$$
  R \hookrightarrow X \times Y
  \,.
$$

=--

In particular any [[function]] induces the [[relation]] "$y$ is the image of $x$":

+-- {: .num_example #FunctionsAsCorrespondences}
###### Example

For $f \;\colon\; X \longrightarrow Y$ a [[function]], its _induced relation_ is the [[relation]] which is exhibited by the [[graph of a function|graph]] of $f$

$$
  graph(f) 
    \coloneqq 
  \left\{
    (x,y) \in X \times Y \;|\; f(x) = y
  \right\}
$$

canonically regarded as a subobject 

$$
  graph(f) \hookrightarrow X \times Y
  \,.
$$

=--

Hence in the context of classical mechanics, in particular any [[symplectomorphism]] $f \;\colon\; (X_1, \omega_1) \longrightarrow (X_2, \omega_2)$ induces the relation 

$$
  graph(f) \hookrightarrow X_1 \times X_2
  \,.
$$

Since we are going to think of $f$ as a kind of "physical process", it is useful to think of the [[smooth set]] $graph(f)$ here as the _space of [[trajectories]]_ of that process. To make this clearer, notice that we may equivalently rewrite every [[relation]] $R \hookrightarrow X \times Y$ as a [[diagram]] of the following form:

$$
  \array{
     && R
      \\
     & {}^{\mathllap{i_X}}\swarrow && \searrow^{\mathrlap{i_Y}}
    \\
    X && && Y
  }
  \;\;
  = 
  \;\;
  \array{
     && R
     \\
     && \downarrow
     \\
     && X \times Y
      \\
     & {}^{\mathllap{p_X}}\swarrow && \searrow^{\mathrlap{p_Y}}
    \\
    X && && Y
  }
$$

reflecting the fact that every [[element]] $(x \sim y) \in R$ defines an element $x = i_X(x \sim y) \in X$ and an element $y = i_Y(x \sim y) \in Y$. 

Then if we think of $R = graph(f)$ we may read the relation as "there is a trajectory from an incoming configuration $x_1$ to an outgoing configuration $x_2$"

$$
  \array{
    && graph(f)
    \\
    & {}^{\mathllap{incoming}}\swarrow && \searrow^{\mathrlap{outgoing}}
    \\
    X_1 && && X_2
  }
  \,.
$$

Notice here that the defining property of a relation as a [[subset]]/[[subobject]] translates into the property of [[classical physics]] that there is _at most one trajectory_ from some incoming configuration $x_1$ to some outgoing trajectory $x_2$ (for a fixed parameter time interval at least, we will formulate this precisely in the next section when we genuinely consider Hamiltonian correspondences).

In a more general context one could consider there to be several such trajectories, and even a whole smooth set of such trajectories between given incoming and outgoing configurations. Each such trajectory would "relate" $x_1$ to $x_2$, but each in a possible different way. We can also say that each trajectory makes $x_1$ _correspond_ to $x_2$ in a different way, and that is the mathematical term usually used:

+-- {: .num_defn #CorrespondencesAndEquivalences}
###### Defininition

For $X, Y \in \mathbf{H}$ two spaces, a [[correspondence]] between them is a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
     && Z
     \\
     & \swarrow && \searrow
    \\
    X && && Y
  }
$$

with no further restrictions. 
Here $Z$ is also called the _[[correspondence space]]_. 


An [[equivalence]] between two such correspondences is
an equivalence $Z_1 \stackrel{\simeq}{\to}Z_2$
that gives a [[commuting diagram]] of the form


$$
  \array{
     && Z_1
     \\
    & {}^{}\swarrow && \searrow^{}
    \\
    X &&\downarrow^{\mathrlap{\simeq}} && Y
    \\
    & {}_{}\nwarrow && \nearrow_{}
    \\
    && Z_2
  }
$$

Correspondences between $X$ any $Y$ with such equivalences between them form a _[[groupoid]]_. (See at _[[geometry of physics]]_ the section _[Essence of gauge theory: Groupoids and basic homotopy 1-type theory](geometry%20of%20physics#GroupoidsAndBasicHomotopy1TypeTheory)_ for more on this.) Hence we write

$$
  Corr\left(\mathbf{H}\right)(X,Y) \in Grpd
  \,.
$$



=--

+-- {: .num_example #EquivalenceOfCorrespndencesInducedByFunction}
###### Example


The correspondence induced by the
[[graph of a function]]  $f \colon X \to Y$ 
as in example \ref{FunctionsAsCorrespondences} is
equivalent, in the sense of def. \ref{CorrespondencesAndEquivalences}, 
to the correspondence

$$
  \array{
    && X
    \\
    & {}^{\mathllap{id}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    X && && Y
  }
  \,.
$$

The equivalence 


$$
  \array{
     && X
     \\
    & {}^{\mathllap{id}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    X &&\downarrow^{\mathrlap{\simeq}} && Y
    \\
    & {}_{\mathllap{i_X}}\nwarrow && \nearrow_{\mathrlap{i_Y}}
    \\
    && graph(f)
  }
$$

is induced by

$$
  X \stackrel{\simeq}{\longrightarrow} graph(f)
$$
$$
  x \mapsto (x,f(x))
$$


=--


Moreover, if we think of correspondences as modelling spaces of [[trajectories]], then it is clear that their should be a notion of [[composition]]:

+-- {: .num_defn}
###### Definition

Given two consecutive correspondences, then their 
_composite_ is the correspondence obtained by forming the
[[fiber product]] of the two coincident morphisms:

$$
  \left(
  \array{    
    && Y_1 &&&& Y_2
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    X_1 && && X_2 && && X_3 
  }
  \right)
  \;\;\;\;
  \mapsto 
  \;\;\;\;
  \left(
  \array{    
    && Y_1 \circ_{X_2} Y_2 
    \\
    & \swarrow && \searrow 
    \\
    X_1 && && X_3 
  }
  \right)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark


Heuristically, the composite space of trajectories $Y_1 \circ_{X_2} Y_2$ should consist precisely of those pairs of trajectories $( f, g ) \in Y_1  \times Y_2$ such that the endpoint of $f$ is the starting point of $g$. The space with this property is precisely the _[[fiber product]]_ of $Y_1$ with $Y_2$ over $X_2$, denoted $Y_1 \underset{X_2}{\times} Y_2$ (also called the [[pullback]] of $Y_2 \longrightarrow X_2$ along $Y_1 \longrightarrow X_2$ and then abbreviated $(pb)$):


$$
  \left(
  \array{    
    && Y_1 \circ_{X_2} Y_2 
    \\
    & \swarrow && \searrow 
    \\
    X_1 && && X_3 
  }
  \right)
  \;\;\;
  =
  \;\;\;
  \left(
  \array{  
     && && Z_1 \underset{Y}{\times} Z_2
     \\
      && & \swarrow && \searrow
      \\
      && Z_1 && (pb) && Z_2
      \\
     & \swarrow && \searrow && \swarrow && \searrow
    \\
    X && && Y && && Z
  }
  \right)
  \,.
$$ 

Hence given a [[topos]] $\mathbf{H}$, [[correspondences]] between its objects form a [[category]] which [[composition]] the [[fiber product]] operation, where however the collection of [[morphisms]] between any two objects is not just a [[set]], but is a [[groupoid]] (the groupoid of correspondences between two given objects and [[equivalences]] between them).

=--

One says that correspondences form a _[[(2,1)-category]]_ 

$$
  Corr(\mathbf{H}) \in (2,1)Cat
  \,.
$$

But for most purposes here, the reader unwilling to enter [[higher category theory]] can, to good approximation, pretend that correspondences form an ordinary [[category]].

One reason for formalizing this notion of correspondences so much in the present context that it is useful now to apply it not just to the ambient [[topos]] $\mathbf{H}$ of [[smooth sets]], but also to its [[slice topos]] $\mathbf{H}_{/\mathbf{\Omega}_{cl}^2}$ over the universal [[moduli space]] of closed [[differential 2-forms]].

To see how this is useful in the present context, notice the following basic observation:

+-- {: .num_defn}
###### Definition

Given a [[symplectic manifold]] $(X,\omega)$, then a [[submanifold]] 

$$
  L \hookrightarrow X
$$ 

is called 

* an _[[isotropic submanifold]]_ if $\omega|_{L}= 0$;

* a _[[Lagrangian submanifold]]_ if in addition $L$ has [[dimension]] $dim(L) = dim(X)/2$.

=--

+-- {: .num_prop}
###### Proposition

Let $f \colon X_1 \to X_2$ be a [[smooth function]] between [[smooth manifolds]] and let

$$
  \array{
     && graph(f)
     \\
     && \downarrow
     \\
     && X_1 \times X_2
     \\
     & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
    X_1 && && X_2
  }
$$

be the induced [[correspondence]]. If $\omega_1$ and $\omega_2$ are [[symplectic forms]] on $X_1$ and $X_2$, respectively, then $p_1^\ast \omega_1 - p_2^\ast \omega_2$ is a pre-symplectic form on $X_1 \times X_2$, and $f$ is a [[symplectomorphism]] precisely if $graph(f) \hookrightarrow X_1 \times X_2$ is a [[Lagrangian submanifold]].

=--

To capture this phenomenon, one traditionally sets:

+-- {: .num_defn #LagrangianCorrespondence}
###### Definition

For $(X_1,\omega_1)$ and $(X_2,\omega_2)$ two [[symplectic manifolds]] (not necessarily of the same [[dimension]]), an _isotropic correspondence_ or  _[[Lagrangian correspondence]]_ between them is a [[correspondence]] of the underlying [[manifolds]]

$$
  \array{
     && R
     \\
     && \downarrow
     \\
     && X_1 \times X_2
     \\
     & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
    X_1 && && X_2
  }
$$

such that the [[correspondence space]] $R \hookrightarrow X_1 \times X_2$ is an  [[isotropic submanifold]] or [[Lagrangian submanifold]], respectively of the product symplectic manifold given by

$$
  (X_1 \times X_2 , p_1^\ast \omega_1 - p_2^\ast \omega_2)
  \,.
$$

=--


+-- {: .num_prop #IsotropicCorrespondenceDiagrammatically}
###### Proposition

Under the identification of prop. \ref{PresymplecticFormsAsMapsIntoASmoothSpace}, 
isotropic correspondences as in def. \ref{LagrangianCorrespondence} are equivalent to diagrams of [[smooth sets]] of the form

$$
  \array{
    && R
    \\
    & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
    \\
    X_1 && \swArrow_= && X_2
    \\
    & {}_{\mathllap{\omega_1}}\searrow && \swarrow_{\mathrlap{\omega_2}}
    \\
   && \Omega^2_{cl}
  }
  \,.
$$

This in turn is equivalent to being a [[correspondence]] in the [[slice topos]] $\mathbf{H}_{/\Omega^2_{cl}}$, def. \ref{TheSliceTopos}, under the identification of prop. \ref{SymplecticManifoldsAsObjectsInSliceOverModuliOf2Forms}.


=--

+-- {: .proof}
###### Proof

By prop. \ref{Symplectomorphism} the commutativity of this diagram says precisely that on $R$ we have

$$
  p_1^\ast \omega_1 = p_2^\ast \omega_2
$$

hence 

$$
  p_1^\ast \omega_1 - p_2^\ast \omega_2 = 0
  \,.
$$

=--

Therefore we have:

+-- {: .num_prop}
###### Proposition

For $(X_1, \omega_2)$ and $(X_2, \omega_2)$ two [[symplectic manifolds]], there is a [[full subcategory|full embedding]]

$$
  LagrangianCorrespondences\left(\left(X_1,\omega_1\right), \left(X_2, \omega_2\right)\right)
  \hookrightarrow
  Corr\left(\mathbf{H}_{/\mathbf{\Omega}^2_{cl}}\right)\left(\left(X_1,\omega_1\right), \left(X_2, \omega_2\right)\right)
$$

of the Lagrangian correspondences into the space of correspondences between the two manifolds as objects in the [[slice topos]] over the universal moduli space of closed differential 2-forms.

=--

+-- {: .num_example}
###### Example

The [[graph of a function]] $f \colon X_1\to X_2$ between [[symplectic manifold]] $(X_i, \omega_i)$ is a [[Lagrangian correspondence]] precisely if $f$ is a [[symplectomorphism]].

=--

+-- {: .proof}
###### Proof

Under the identification of 

$$
  \array{
     && graph(f)
     \\
     & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
     X_1 && && X_2
  }
$$

=--




### Hamiltonian (time evolution) trajectories and Hamiltonian correspondences
 {#TheClassicalActionFunctionalPrequantizesHamiltonianCorrespondences}

An important class of [[symplectomorphisms]] are the following

+-- {: .num_defn #HamiltonianCorrespondence} 
###### Definition

Let $(X,\omega)$ be a [[symplectic manifold]]. The induced [[Poisson bracket]] 
$\{-,-\}$ takes a [[smooth function]] $H \in C^\infty(X)$ (the "[[Hamiltonian]]") to the [[derivation]] $\{H,-\}$ on $C^\infty(X)$. This is equivalently a [[vector field]] $v_H \in \Gamma T X$, the corresponding [[Hamiltonian vector field]].

A [[Hamiltonian symplectomorphisms]] from a [[symplectic manifold]] $(X,\omega)$ to itself, is a [[symplectomorphism]] $X \to X$ which is 
the [[flow]] of a [[Hamiltonian vector field]] 
for some parameter "time" $t \in \mathbb{R}$

$$
  \exp( t \{H,-\}) \;\colon\; (X,\omega) \longrightarrow (X,\omega)
  \,.
$$ 

We call a [[Lagrangian correspondence]], def. \ref{LagrangianCorrespondence}, induced from [[Hamiltonian symplectomorphisms]] a _Hamiltonian correspondences_.

=--


+-- {: .num_remark #HamiltonianCorrespondencesAreSpacesOfTrajectories}
###### Remark

Under the interpretation of [[correspondences]] as spaces of [[trajectories]] as in example \ref{FunctionsAsCorrespondences}, 
the [[smooth set|smooth]] [[correspondence space]] of a
Hamiltonian correspondence is naturally identified with the space of
_classical [[trajectories]]_ of the [[Hamiltonian mechanics|Hamiltonian]] [[dynamics]] of $H$

$$
  Fields_{traj}^{class}(t) = graph\left( \exp(t\{H,-\}) \right)
$$


in that 

1. every point in the space corresponds uniquely to a [[trajectory]] of parameter time length $t$ characterized as satisfying the [[equations of motion]] as given by [[Hamilton's equations]] for $H$;

1. the two projection maps to $X$ send a trajectory to its initial and to its final configuration, respectively.

=--

+-- {: .num_remark}
###### Remark

Forming Hamiltonian correspondences consitutes a [[functor]] from 1-dimensional [[cobordisms]] with [[Riemannian structure]] to the [[category of correspondences]] in the [[slice topos]]:

$$
  \exp((-)\{H,-\}) \;\colon\; Bord^{Riem}_1 \longrightarrow Corr_1(\mathbf{H}_{/\Omega^2})
$$

since for all ("time") parameter valued $t_1, t_2 \in \mathbb{R}$ 
we have a [[composition]] (by [[fiber product]]) of [[correspondences]] exhibited
by the following [[pasting diagram]]:

$$
  \array{
    &&&& graph\left(\exp\left(\left(t_1+t_2\right)\right) \left\{H,-\right\} \right)
    \\
    && & \swarrow && \searrow
    \\
    && graph\left(\exp\left(t_1\right)\left\{H,-\right\}\right) 
    && (pb) && graph\left(\exp\left(t_2 \left\{H,-\right\}\right)\right)
    \\
    & \swarrow && \searrow & & \swarrow && \searrow
    \\
    X && && X && && X
    \\
    & \searrow &&& \downarrow &&& \swarrow
    \\
    &&&& \Omega^2_{cl}
  }
  \,.
$$

=--

### The kinetic action and Planck's constant
 {#KineticAction}


To naturally see why there would be any [[Hamiltonian]]
associated to a (to some) [[symplectomorphism]] in the first place, 
we step back and consider _local trivializations_ or _local potentials_
for [[symplectic forms]]. Doing so turns out to give rise to what
in physics is called the [[kinetic action]], what in 
the context of [[geometric quantization]] is called [[prequantization]]
and what in [[mathematics]] is called lifting to _[[differential cohomology]]_. All these concepts arise directly from the following simple consideration.

Given a [[pre-symplectic form]] $\omega \in \Omega^2_{\mathrm{cl}}(X) $, 
by the [[Poincaré lemma]] there is a [[good open cover]] $\{U_i \hookrightarrow X\}_i$
such that one can find smooth [[differential 1-forms]] $\theta_i \in \Omega^1(U_i)$ such that these are local trivializations/potentials
for the [[symplectic form]] on each patch $U_i$ of the cover:

$$
  \mathbf{d}\theta_i = \omega_{|U_i}
  \,.
$$

Physically such a 1-form is (up to a factor of 2) a choice 
of _[[kinetic energy]] [[density]]_ called a _[[kinetic Lagrangian]]_ 
$L_{\mathrm{kin}}$ (below in example \ref{StandardPrequantizationOfStandardR2PhaseSpace} we connect this statement to a maybe more familiar formla): 

$$
  \theta_i = 2 L_{\mathrm{kin}, i}
  \,.
$$

+-- {: .num_example #StandardPrequantizationOfStandardR2PhaseSpace}
###### Example

Consider the [[phase space]] $(\mathbb{R}^2, \; \omega = \mathbf{d} q \wedge \mathbf{d} p)$ 
of example \ref{CanonicalR2PhaseSpace}. Since $\mathbb{R}^2$ is a [[contractible topological space]] we consider the trivial [[covering]] ($\mathbb{R}^2$ covering itself) since this is already a [[good covering]] in this case. Then all the $\{g_{i j}\}$ are trivial and the data of a [[prequantization]] consists simply of a choise of 1-form $\theta \in \Omega^1(\mathbb{R}^2)$ such that 

$$
  \mathbf{d}\theta = \mathbf{d}q \wedge \mathbf{d}p
  \,.
$$

A standard such choice is 

$$
  \theta = - p \wedge \mathbf{d}q
  \,.
$$

Then given a [[trajectory]] $\gamma \colon [0,1] \longrightarrow X$ which satisfies [[Hamilton's equation]] for a standard [[kinetic energy]] term, then $(p \mathbf{d}q)(\dot\gamma)$ is this [[kinetic energy]] of the [[particle]] which traces out this [[trajectory]].

=--

Given a path $\gamma : [0,1] \to X$ in phase space, its 
_[[kinetic action]]_ $S_{\mathrm{kin}}$ 
is supposed to be the integral of $L_{\mathrm{kin}}$
along this trajectory. In order to make sense of this in the generality where there is no globally defined $\theta$,
there need to be functions $g_{i j} \in C^\infty(U_i \cap U_j, \mathbb{R})$ for each double intersection of patches of the cover,
such that these the local $\theta$'s differ on these double
intersection only by the total [[derivative]] 
([[de Rham cohomology|de Rham]] [[differential]] $\mathbf{d}$ ) of these functions:

$$
  \theta_j|_{U_j} - \theta_i|_{U_i} = \mathbf{d}g_{i j}
  \,.
$$

One then finds (from the theory of [[Cech cohomology]]) that if on triple intersections these functions satisfy

$$
  g_{ij} + g_{j k} = g_{i k}
$$

then there is a well defined action functional

$$
  S_{\mathrm{kin}}(\gamma) \in \mathbb{R}
$$

obtained by dividing $\gamma$ into small pieces that each map to a single
patch $U_i$, integrating $\theta_i$ along this piece, and adding the 
contribution of $g_{i j}$ at the point where one switches from using
$\theta_i$ to using $\theta_j$. Technically this is called the [[holonomy]] or [[parallel transport]] of the $(\mathbb{R},+)$-[[principal connection]] which is defined by the data $(\{\theta_i\}, \{g_{i j}\} )$.

However, requiring this condition on triple overlaps as an equation between $\mathbb{R}$-valued functions makes the local patch structure trivial: if this is possible then one can in fact already find a single $\theta \in \Omega^1(X)$ and functions $h_i \in C^\infty(U_i, \mathbb{R})$ such that  $\theta_i = \theta|_{U_i} + \mathbf{d}h_i$. This has the superficially pleasant effect that the action is 
simply the integral against this globally defined 1-form, 
$S_{\mathrm{kin}} = \int_{[0,1]} \gamma^\ast L_{\mathrm{kin}}$, but it also means that the pre-symplectic form $\omega$ is exact, which is 
not the case in many important examples.
(In more abstract terms what this is saying is that every 
$(\mathbb{R},+)$-[[principal bundle]] over a manifolds is trivializable.)

On the other hand, what really matters in [[prequantum field theory|prequantum]] [[physics]] is not the [[action functional]]
$S_{\mathrm{kin}} \in \mathbb{R}$ itself, 
but the _exponentiated_ action 

$$
  \exp\left( \tfrac{i}{\hbar} S \right) \in \mathbb{R}/(2\pi \hbar)\cdot\mathbb{Z}
  \,,
$$

which takes values in the [[quotient]] of the additive group of [[real numbers]] by [[integer|integral]] multiples of [[Planck's constant]] $2\pi \hbar$.

In more detail, consider the canonical inclusion

$$
  \mathbb{Z} \hookrightarrow \mathbb{R}
$$

of the [[integers]] as an addiditve [[subgroup]] of the [[real numbers]]. Strictly speaking what appears in [[physics]] is the [[real line]] on which a [[unit]] is chosen as part of the identification of mathematical formalism with physical reality, one should really consider _all_ possible additive group homomorphisms $\mathbb{Z}\to \mathbb{R}$. These are parameterized by 

$$
  h \in (\mathbb{R}- \{0\}) \hookrightarrow \mathbb{R}
$$

$$
  (-)\cdot h \;\colon\; \mathbb{Z} \longrightarrow \mathbb{R}
$$

and this "physical [[unit]]" $h$ is what is called _Planck's constant_. 

In particular the induced [[circle group]] is identified as the [[quotient]] of $\mathbb{R}$ by $h \mathbb{Z}$, in this sense

$$
  U(1) \simeq \mathbb{R}/h \mathbb{Z}
$$

and under this identification its [[quotient]] map is expressed in terms of the [[exponential function]] $\exp \colon z \mapsto  \sum_{k = 0}^\infty \frac{z^k}{k!} \in \mathbb{C}$ as

$$
  \exp(2 \pi \tfrac{i}{h}(-))
  =
  \exp(\tfrac{i}{\hbar} (-)) \;\colon\; \mathbb{R} \longrightarrow U(1)
  \,,
$$

where

$$
  \hbar \coloneqq h/2\pi
  \,.
$$

The resulting [[short exact sequence]] is the real [[exponential exact sequence]]

$$
  0 \to \mathbb{Z} \longrightarrow \mathbb{R} \stackrel{\exp(\tfrac{i}{\hbar}(-))}{\longrightarrow} U(1) \to 0
  \,.
$$

This is the source of the ubiquity of the expression  $\exp(\tfrac{i}{\hbar} (-))$ in [[quantum physics]], say in the [[path integral]], where the exponentiated [[action functional]] appears as $\exp(\tfrac{i}{\hbar} S)$.



### Pre-Quantization and Differential cohomology
 {#Prequantization}

By the above discussion, for the exponentiated
kinetic action functional to be well defined, one only needs that the equation
$g_{i j} + g_{j k} = g_{i k}$ on triple intersection holds modulo addition of an integral multiple of [[Planck's constant]] $h = 2\pi \hbar$. 

If this is the case, then one says that the data 
$(\{\theta_i\}, \{g_{i j}\})$ defines 
equivalently

* a $U(1)$-[[principal connection]];

* a degree-2 cocycle in [[ordinary differential cohomology]] 

on $X$, with _[[curvature]]_ the given symplectic 2-form $\omega$.

Such data is called a _[[pre-quantization]]_ of the symplectic manifold 
$(X,\omega)$. Since it is the exponentiated action functional
$\exp(\frac{i}{\hbar} S)$ that enters the quantization of the 
given mechanical system (for instance as the integrand of a 
[[path integral]]),
the [[prequantization]] of a symplectic manifold is indeed precisely
the data necessary before quantization.



Therefore, in the spirit of the above discussion of pre-symplectic structures,
we would like to refine the smooth moduli space of closed 
differential 2-forms to a moduli space of prequantized differential 
2-forms. 

Again this does naturally exist if only we allow for a good notion of
"space". An additional phenomenon to be taken care of now is that
while pre-symplectic forms are either equal or not, their
pre-quantizations can be different and yet be _[[equivalence|equivalent]]_:

because there is still a remaining freedom to change this data without
changing the exponentiated action along a _closed_ path:
we say that a choice of functions 
$h_i \in C^\infty(U_i, \mathbb{R}/(2\pi\hbar)\mathbb{Z})$
defines an equivalence between 
$(\{\theta_i\}, \{g_{i j}\})$ and $(\{\tilde \theta_i\}, \{\tilde g_{i j}\})$
if $\tilde \theta_i - \theta_i = \mathbf{d}h_i$
and $\tilde g_{i j} - g_{i j} = h_j - h_i$.

This means that the space of prequantizations of $(X,\omega)$
is similar to an _[[orbifold]]_: it has points which are connected by 
gauge equivalences: there is a _[[groupoid]]_ of pre-quantum structures
on a manifold $X$. 

In just the same way then that above we found a [[smooth set|smooth]] [[moduli space]] $\mathbf{\Omega}^2_{cl}$ of closed differential 2-forms, one can find a [[smooth groupoid]] (for more on this see at _[[geometry of physics]]_ the section _[Smooth homotopy types](geometry%20of%20physics#SmoothnGroupoids)_ ), which we denote 

$$
  \mathbf{B}U(1)_{\mathrm{conn}}
  \in 
  \mathbf{H}
$$

+-- {: .num_prop #PrequantumGaugeTransformation}
###### Proposition

The [[smooth groupoid]] $\mathbf{B}U(1)_{\mathrm{conn}}$ is _characterized_ as follows, 

1. For $X$ a [[smooth manifold]], maps 

   $$
     \nabla \colon X \longrightarrow \mathbf{B}U(1)_{conn}
   $$ 

   are equivalent to the above prequantum data $(\{\theta_i\}, \{g_{i j}\})$ on $X$;

1. for $\nabla_1, \nabla_2 \colon X \longrightarrow \mathbf{B}U(1)_{conn}$ two such maps, [[homotopies]] 

   $$
     \array{
       & \nearrow \searrow^{\mathrlap{\nabla_1}}
       \\
       X & \Downarrow & \mathbf{B}U(1)_{conn}
       \\
       & \searrow \nearrow_{\mathrlap{\nabla_2}}
     }
   $$

   between these are equivalent to the above [[gauge transformations]] $(\{h_i\})$ between this data

$$
  (\theta_2)_i - (\theta_1)_i = \mathbf{d} \tfrac{\hbar}{i} log (h_i)
  \,.
$$

=--

+-- {: .num_prop #UniverselCurvatureMap}
###### Proposition

There is a universal [[curvature]] map, a morphism of [[smooth groupoids]]

$$
  F
  \;\colon\;
   \mathbf{B}U(1)_{\mathrm{conn}}
     \longrightarrow
   \mathbf{\Omega}^2_{\mathrm{cl}}
$$

which is such that for $\nabla \colon X \longrightarrow \mathbf{B}U(1)_{conn}$ a $U(1)$-[[principal connection]], the composite

$$
  F_\nabla \;\colon\;
  X 
    \stackrel{\nabla}{\longrightarrow}
  \mathbf{B}U(1)_{conn}
    \stackrel{F_{(-)}}{\longrightarrow}
  \mathbf{\Omega}^2_{cl}
$$

is its [[curvature]] 2-form. 

=--

Hence this is the map that sends $(\{\theta_i\}, \{g_{i j}\})$ to $\omega$ with $\omega|_{U_i} = \mathbf{d}\theta_i$.

Therefore:

+-- {: .num_defn #Prequantization}
###### Definition


A _[[prequantization]]_ of a [[symplectic manifold]] $(X,\omega)$ is -- if it exists -- a choice of [[circle group]]-[[principal connection]] $\nabla$ on $X$ whose [[curvature]] 2-form is the given [[symplectic form]]

$$
  F_\nabla = \omega
  \,.
$$

=--

In terms of the classifying morphism of differential forms as in prop. \ref{PresymplecticFormsAsMapsIntoASmoothSpace} this reads as follows.

+-- {: .num_prop #PrequantizationByLiftingClassifyingMap}
###### Proposition

Given a [[presymplectic manifold]] $(X,\omega)$, regarded equivalently as an object $(X \stackrel{\omega}{\longrightarrow} \mathbf{\Omega}^2_{cl}) \in \mathbf{H}_{/\mathbf{\Omega}^2_{cl}}$ by prop. \ref{SymplecticManifoldsAsObjectsInSliceOverModuliOf2Forms}, then a
**[[prequantization]]** of $(X,\omega)$, def. \ref{Prequantization}, is equivalently a choice of lift $\nabla$ in

$$
  \array{
    X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}U(1)_{conn}
    \\
    & {}_{\mathllap{\omega}}\searrow & \downarrow^{\mathrlap{F_{(-)}}}
    \\
    && \mathbf{\Omega}^2_{cl}
  }
  \,.
$$

=--

Phrased this way, there is an evident concept of prequantization of Lagrangian correspondences:

+-- {: .num_defn #PrequantizedLagrangianCorrespondence}
###### Definition

Given prequantized symplectic manifolds $(X_i,\nabla_i)$ as in prop. \ref{PrequantizationByLiftingClassifyingMap}, and given a Lagrangian correspondence
as in prop. \ref{IsotropicCorrespondenceDiagrammatically}, then
a prequantization of this correspondence is a lift of the 
whole diagram through the universal curvature map of prop. \ref{UniverselCurvatureMap}:

$$
  \array{
    && Z
    \\
    & \swarrow && \searrow
    \\
    X_1 && && X_2
    \\
    & {}_{\mathllap{\omega_1}}\searrow && \swarrow_{\mathrlap{\omega_2}} 
    \\
    && \mathbf{\Omega}^2_{cl}
  }
  \;\;\;\;
    \mapsto
  \;\;\;\;
  \array{
    && Z
    \\
    & \swarrow && \searrow
    \\
    X_1 && \swArrow_{\simeq} && X_2
    \\
    & {}_{\mathllap{\nabla_1}}\searrow && \swarrow_{\mathrlap{\nabla_2}} 
    \\
    && \mathbf{B}U(1)_{conn}
    \\
    && \downarrow^{\mathrlap{F}}
    \\
    && \mathbf{\Omega}^2_{cl}
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This means in words that a prequantized Lagrangian correspondence is a [[prequantization]] of the in- and out-going [[symplectic manifolds]] together with a choice of [[equivalence]]/[[gauge transformation]]
between the two [[prequantum circle bundles]] pulled back to the 
[[correspondences]] space.

=--

+-- {: .num_remark}
###### Remark

By [[duality]] in the [[symmetric monoidal (infinity,1)-category|smmetric monoidal]] [[(infinity,n)-category of correspondences|(2,1)-category of correspondences]], a prequantized Lagragian correspondence is equivalently a [[diagram]] of the form

$$
  \array{
    && Y
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && X_1 \times X_2
    \\
    & \searrow && \swarrow_{\mathrlap{\nabla_2- \nabla}}
    \\
    \\
    && \mathbf{B}U(1)_{conn}
  }
$$

hence a trivialization of the product of one prequantum bundle with the negative (the inverse under tensor product) of the other, on the correspondence space.


=--




### Hamiltonian flows, the Legendre transform and the Hamilton-Jacobi action
 {#HamiltonianTrajectoriesAndPrequantizedLagrangianCorrespondences}



+-- {: .num_prop #HamiltonianTransformationIsPrequantizedByTheExponentiatedAction}
###### Proposition

Consider the [[phase space]] $(\mathbb{R}^2, \; \omega = \mathbf{d} q \wedge \mathbf{d} p)$ 
of example \ref{CanonicalR2PhaseSpace} equipped with its canonical [[prequantization]] by $\theta = p \, \mathbf{d}q$ from example \ref{StandardPrequantizationOfStandardR2PhaseSpace}, 

Then smooth 1-parameter flows of this data via prequantized correspondences, def. \ref{PrequantizedLagrangianCorrespondence},

$$
  t
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{       
    X && \stackrel{f_t}{\longrightarrow} && X
    \\
    & {}_{\mathllap{\theta}} \searrow 
    & \swArrow_{ F_t } & \swarrow_{\mathrlap{\theta}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
$$

are in bijection with 
smooth functions $H \colon \mathbb{R}^2 \longrightarrow \mathbb{R}$.

This bijection works by regarding $H$ as a [[Hamiltonian]], def. \ref{HamiltonianCorrespondence}, and assigning the [[flow]] $f_t = \exp(t \{H,-\})$ of its [[Hamiltonian vector field]]

$$
  t
  \;\;
  \mapsto
  \;\;
  \array{       
    X && \stackrel{\exp(t \{H,-\})}{\longrightarrow} && X
    \\
    & {}_{\mathllap{\theta}} \searrow 
    & \swArrow_{\exp( \tfrac{i}{\hbar} S_t  )} & \swarrow_{\mathrlap{\theta}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \,,
$$

where the prequantization is given by

* $S_t \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}$ is the [[Hamilton-Jacobi action]] of the classical [[trajectories]] induced by $H$,

* which is the [[integral]] $S_t = \int_{0}^t L \, d t$ of the [[Lagrangian]] $L \,d t$ induced by $H$,

* which is the [[Legendre transform]] of the [[Hamiltonian]]

  $$
    L \coloneqq p \frac{\partial H}{\partial p} - H \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}
    \,. 
  $$


=--



+-- {: .proof}
###### Proof

By prop. \ref{PrequantumGaugeTransformation} the prequantum filler of the diagram is given by a function $F_t =\exp(\tfrac{i}{\hbar} S_t)$ satisfying

$$
  f_t^\ast \theta - \theta = -\mathbf{d}S_t
  \,.
$$

By standard [[Lie theory]] a smooth such 1-parameter flow is fixed by its [[derivative]] by $t$. For the above equation this yields

$$
  \mathcal{L}_v \theta = -\mathbf{d}L
$$

where 

1. $v \in \Gamma(T X)$ is the [[vector field]] of the [[flow]] $t\mapsto f_t$;

1. $\mathcal{L}_v$ is the [[Lie derivative]] along $v$;

1. $L \coloneqq \frac{\partial S}{\partial t}$.

By [[Cartan's magic formula]] this equation is equivalent to

$$
  \iota_v \omega = -\mathbf{d}L - \mathbf{d} \iota_v \theta
  \,.
$$

This is the symplectic form of [[Hamilton's equations]] for $v$ and says that

$$
  H 
  \coloneqq 
  - L - \iota_v \theta 
$$

is a [[Hamiltonian]] that makes $v$ a [[Hamiltonian vector field]]. The correction term is

$$
  \begin{aligned}
    \iota_v  \theta 
    &= 
    \iota_v ( p \, \mathbf{d}q )
    \\
    & = p \partial_v q
    \\ 
  \end{aligned}
  \,.
$$

But since $v$ is Hamiltonian, this is given by one component of [[Hamilton's equations]] $\iota_v (\mathbf{d}p \wedge \mathbf{d}q) = \mathbf{d}H$ saying that 
$\partial_v q = \frac{\partial H}{\partial p}$.

Hence in summary the flow is Hamiltonian and the pre-quntum filler is the choice of Hamiltonian $H$ specified by

$$
  \frac{\partial S}{\partial t}
  = 
  L
  = 
  p \frac{\partial H}{\partial p}  - H 
  \,.
$$

=--

+-- {: .num_remark}
###### Remark


In particular, this induces a [[functor]]

$$
  \exp(\tfrac{i}{\hbar} S)
  \;\colon\;
  Bord_1^{Riem} 
    \longrightarrow 
  Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}})
  \,.
$$


In summary,  prop. \ref{HamiltonianTransformationIsPrequantizedByTheExponentiatedAction} 
and remark \ref{HamiltonianCorrespondencesAreSpacesOfTrajectories}
say that a prequantized Lagrangian correspondence is conceptually of the following form

$$
  \array{
    && {{space\,of} \atop {trajectories}}
    \\
    & {}^{\mathllap{{initial}\atop {values}}}\swarrow && \searrow^{\mathrlap{{Hamiltonian} \atop {evolution}}}
    \\
    phase\,space_{in} && \swArrow_{{action} \atop {functional}} && phase \,space_{out}
    \\
    & {}_{\mathllap{{prequantum}\atop {bundle}_{in}}}\searrow 
    && 
    \swarrow_{\mathrlap{{prequantum} \atop {bundle}_{out}}}
    \\
    && {{2-group} \atop {of\,phases}}
  }
  \,.
$$

=--


+-- {: .num_remark }
###### Remark

The proof of prop. \ref{HamiltonianTransformationIsPrequantizedByTheExponentiatedAction} recovers, from general abstract input, precisely all the ingredients known in physics as _[[canonical transformations]]_.


The proposition says that the slice topos $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$
unifies [[classical mechanics]] in its two incarnations as
[[Hamiltonian mechanics]] and as [[Lagrangian mechanics]], where the relation between the two via the [[Legendre transform]] is exhibited by the [[homotopies]] that fill diagrams in the slice topos over $\mathbf{B}U(1)_{conn}$.

[[!include Hamiltonian and Lagrangian -- table]]

=--



### Heisenberg group and Poisson bracket

Above we have interpreted [[maps]] $f \colon X \to Y$ as [[correspondences]]
between $X$ and $Y$ by taking the [[correspondence space]] to be the 
[[graph of a function|graph]] of $f$. There is also another natural way
to regard maps as correspondences: we may simply take $X$ as the correspondence
space, take the left map out of it to be the identity and the right map 
to be $f$ itself:

$$
  \left(
    X \stackrel{f}{\longrightarrow} Y
  \right)
  \;\;  
    \mapsto
  \;\;
  \left(
    \array{
       && X
       \\
       & {}^{\mathllap{id}}\swarrow && \searrow^{\mathrlap{f}}
       \\
      X && && Y
    }
  \right)
  \,.
$$

Consider now those correspondences which are [[equivalences]] ([[isomorphisms]])
in the [[category of correspondences]] $Corr_1(\mathbf{H})$. If we forget
the [[smooth structure]] on everything and consider just correspondences
of the underlying [[sets]], hence $Corr_1(Set)$, then it is easy to see
that under the [[cardinality]] map correspondences are given by [[matrices]]
with [[cardinality]] entries and [[composition]] of correspondence 
by [[fiber product]] induces [[matrix multiplication]]. 

Therefore for a correspondence to be an equivalence-transformation it has
to be of the form above, induced by a direct [[map]], which in 
addition is an [[equivalence]] $f \colon X \stackrel{\simeq}{\longrightarrow} Y$.

+-- {: .num_prop}
###### Proposition

Let $(X,\omega)$ be a [[symplectic manifold]] and choose any 
[[prequantization]] $(L,\nabla)$, thought of, via remark \ref{PrequantizationIsLiftThroughCurvatureBaseChange}, as an object in the [[slice (infinity,1)-topos|slice (2,1)-topos]],
$\nabla \in \mathbf{H}_{/\mathbf{B}U(1)_{conn}}$. Then

* the [[automorphism group]] of $\nabla$ in the [[category of correspondences]] $Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}})$ is what is called the _[[quantomorphism group]]_;

* its [[Lie algebra]] is the [[Poisson bracket]] Lie algebra of $(X,\omega)$.

=--

See ([hgp 13](#FiorenzaRogersSchreiber13a))

For some reason, the [[quantomorphism group]] which is the [[Lie integration]] of the [[Poisson bracket]] is less famous than the [[Heisenberg group]] that sits inside it:

+-- {: .num_remark}
###### Remark

Suppose that $(X,\omega)$ itself has the structure of a [[group]] (for instance if $(X,\omega)$ is a [[symplectic vector space]] such as $(\mathbb{R}^{2n}, \sum_i p_i \mathbf{d}q^i)$ ), then the [[subgroup]] of the [[quantomorphism group]] whose underlying [[diffeomorphisms]] are given by the action of $X$ is the _[[Heisenberg group]]_ of $X$.

=--

### Hamiltonian actions and moment maps 

For $G$ a [[Lie group]], a [[Hamiltonian action]] of $G$ on $(X,\omega)$ is equivalently an action by prequantized Lagrangian correspondences, hence a group [[homomorphism]]

$$
  G \longrightarrow \mathbf{Aut}_\nabla(Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}}))
  \,.
$$

The [[Lie differentiation]] of this is the corresponding [[moment map]].

See ([hgp 13](#FiorenzaRogersSchreiber13a))



## Semantic Layer
 {#SemanticsLayer}

We now discuss the above constructions more abstractly in [[cohesive topos|cohesive]] [[topos theory]].


> under construction



given $V$ then the [[delooping]] $\mathbf{B} \mathbf{Aut}(V)$ of its [[automorphism group]] $\mathbf{Aut}(V)$ is the [[1-image]] factorization of the name $\ast \stackrel{\vdash V}{\longrightarrow} Type$ of $V$

$$
  \ast \stackrel{}{\longrightarrow} \mathbf{B}\mathbf{Aut}(V)
  \hookrightarrow Type
  \,.
$$

for the slice over $\mathbf{B}U(1)_{conn}$ this needs to be subjected to [[differential concretification]]

(...)

## Syntactic Layer
 {#SyntacticLayer}

We now discuss the above constructions yet more abstractly in [[homotopy type theory]].

(...)

prequantization is lift through [[dependent sum]] along the universal [[curvature]] map of prop. \ref{UniverselCurvatureMap}

$$
  \underset{F_{(-)}}{\sum}
   \;\colon\;
  \mathbf{H}_{/\mathbf{B}U(1)_{conn}}
   \longrightarrow
  \mathbf{H}_{/\mathbf{\Omega}^2_{cl}}
$$

(...)

## References

As far as it is not covered by traditional material, the above discussion is taken from

* {#FiorenzaRogersSchreiber13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_
 
* [[Urs Schreiber]], _[[schreiber:Classical field theory via Cohesive homotopy types]]_


For more and related references see there and see at _[[motivic quantization]]_.

[[!redirects prequantized Lagrangian correspondences]]

[[!redirects prequantum Lagrangian correspondence]]
[[!redirects prequantum Lagrangian correspondences]]