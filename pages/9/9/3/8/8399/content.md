
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In [[physics]], the term _general covariance_ is meant to indicate the property of a [[physical system]] or [[model (in theoretical physics)]] whose [[configuration space|configurations]], [[action functional]] and [[equations of motion]] are all [[equivariance|equivariant]] under the [[action]] of the [[diffeomorphism group]] on the [[smooth manifold]] underlying the [[spacetime]] or the [[worldvolume]] of the system. Here "covariance" is as in "[[covariant tensor]]" another term for behaviour under diffeomorphisms.

The term _[[general relativity]]_ for [[Einstein]]-[[gravity]] originates in at least closely related ideas (see _[History and original formulation](#HistoryAndOriginalFormulation)_ below), and Einstein-gravity is the archtypical example of a generally covariant physical system: 

here, the [[configuration space]] of physical fields over a [[smooth manifold]] $\Sigma$ is not quite the space of [[Riemannian metrics]] on $\Sigma$ itself, but is the [[quotient]] $[\Sigma,\mathbf{Fields}]/\mathbf{Diff}(\Sigma)$ of this space by the [[action]] of the [[diffeomorphism group]] $\mathbf{Diff}(\Sigma)$: two Riemannian metrics $g_1$ and $g_2$ on $\Sigma$ represent the same field of [[gravity]] on $\Sigma$ if there is a [[diffeomorphism]] $f : \Sigma \stackrel{\simeq}{\to} \Sigma$ such that $g_2 = f^* g_1$.

Or rather, such a diffeomorphism is a [[gauge transformation]] between the two field configurations. The configuration space is not the naive [[quotient]] of fields by diffeomorphisms as above, but is the [[homotopy quotient]], or _[[action groupoid]]_, denoted $[\Sigma,\mathbf{Fields}]\sslash \mathbf{Diff}(\Sigma)$. In the physics literature this action groupoid is most familiar in its [[infinitesimal cohesion|infinitesimal approximation]], the corresponding [[Lie algebroid]], whose formal dual is a [[BRST complex]] whose degree-1 elements are accordingly called the _diffeomorphism ghosts_ (see there).

As with all [[gauge transformations]], they relate physical configurations which may be nominally different, but [[equivalence|equivalent]].
Therefore _general covariance_ is an instance of the general _[[principle of equivalence]]_ in mathematics which says that sensible statements about [[objects]] must respect the [[isomorphisms]] and more general [[equivalences]] between these objects. 

A physical system which is not generally covariant in this sense is hence one where the [[smooth manifold]] $\Sigma$ as above, underlying [[spacetime]]/[[worldvolume]] is not regarded as modelling an absolute physical system (such as the [[observable universe]] in gravity), but a [[subsystem]] that is equipped with ambient [[structure]] that [[spontaneous symmetry breaking|breaks]] the diffeomorphism symmetry. Notably systems like [[electromagnetism]] or [[Yang-Mills theory]] have traditionally been written in a non-generally covariant form describing gauge fields on a fixed gravitational background, as for instance the space inhabited by a particle accelerator. This ambient structure on the spacetime $\Sigma$ breaks its general diffeomorphism invariance and hence the effective resulting theory on this background is not generally covariant (a special case of the general phenomenon of [[spontaneous symmetry breaking]]). 

On the other hand, such a model consisting of background (e.g. the particle accelerator) and quantum fields propagating in it is ultimately to be understood as an approximation to a more encompassing model in which also the background is dynamical, and which is again generally covariant. Specific for electromagnetism and Yang-Mills theory this refined generally covariant model is known as _[[Einstein-Maxwell theory]]_ or more generally _[[Einstein-Yang-Mills theory]]_.

The idea of general covariance has a long and convoluted history and the literature witnesses plenty of disagreement about how to interpret and formalize it in technical detail ([Norton](#Norton)). Already early arguments by [[Einstein]] himself (e.g. the "[[hole paradox]]" ([Einstein-Grossmann](#EinsteinGrossmann))) show that the discussion has suffered from the beginning from lack of the basic [[category theory|category theoretic]] concept  of [[isomorphism]]  in the [[category]] [[Diff]] of [[smooth manifolds]]. Below in _[Formalization in homotopy type theory](#InHomotopyTypeTheory)_ we indicate a formalization of general covariance that is general, fundamental, and accurately reflects the role of the term in theoretical physics.


## History and original formulation
 {#HistoryAndOriginalFormulation}

> The question of general covariance of physical theories in space and time can be traced back to the famous debate between [[Gottfried Wilhelm Leibniz]] and [[Samuel Clarke]] (the latter assisted by Sir [[Isaac Newton]]) on the [[ontology|ontological]] status of space in the years 1715&#8211;1716 ([Alexander](#Alexander)), the central question being if space exists as a substance or as an absolute being and absolute motion is present (Clarke) or if it is constituted only in relation to co-existent things allowing for relativism in motions only (Leibniz). This kind of problems also played an important role when the general theory of relativity was being developed in the years around 1910. While [[Albert Einstein]] first characterized generally covariant field equations as inadmissible since they did not determine the [[Riemannian metric|metric field]] uniquely as shown in the hole argument ( _Lochbetrachtung_ ) in the appendix of ([Einstein-Grossmann](#EinsteinGrossmann)), he later accepted ([Einstein 1916](#Einstein1916)) that all [[physical laws]] had to be expressed by [[equations]] that are valid in all [[coordinate systems]], i. e., which are covariant (generally covariant) under arbitrary [[substitution|substitutions]]. 

>> _Die allgemeinen Naturgesetze sind durch Gleichungen auszudr&#252;cken, die f&#252;r alle Koordinatensysteme gelten, d. h. die beliebigen Substitutionen gegen&#252;ber kovariant (allgemein kovariant) sind._ ([Einstein 1916 p. 776](#Einstein1916))

> The hole argument was dismissed by the reasoning that it is not the [[spacetime]] [[Riemannian metric|metric]] that has to be fixed uniquely by the [[equations of motion|field equations]], but only the physical phenomena that occur in spacetime need to be given a unique expression with reference to any description of spacetime. All physical statements are given in terms of spacetime coincidences; [[measurement|measurements]] result in statements on meetings of material points of the measuring rods with other material points or in coincidences between watch hands and points on the clockface. The introduction of a reference system merely serves the easy description of the totality of all these coincidences (point-coincidence argument) ([Einstein 1916 p. 776f](#Einstein1916)).

> from ([Brunetti-Pormann-Ruzzi](#BrunettiPorrmannRuzzi))

## Modern formulation in differential geometry
 {#ModernFormulationInDifferentialGeometry}

We discuss the modern formulation of general covariance in [[differential geometry]].

### In gravity

Let $\Sigma \in $ [[SmoothMfd]] be a [[smooth manifold]]. Write $Riem(\Sigma)$ for the space of ([[pseudo-Riemannian metric|pseudo]]-)[[Riemannian metrics]] on $\Sigma$. For $f : \Sigma \to \Sigma$ a [[diffeomorphism]], there is a [[function]] $f^* : Riem(\Sigma) \to Riem(\Sigma)$ which sends a Riemannian metric to its pullback:

$$
  (f^*g)(v,w) \coloneqq g(f_* v, f_* w)
  \,, 
$$ 

where $f_* : T\Sigma \to T\Sigma$ is the canonical map induced on the [[tangent bundle]] (see at _[[derivative]]_).

Say that two metrics $g_1, g_2$ are [[gauge transformation|gauge equivalent]] if there is a diffeomorphism $f$ such that $g_2 = f^* g_1$.  This is an [[equivalence relation]]. Write $Riem(\Sigma)/Diff(\Sigma)$ for the corresponding set of [[equivalence classes]]. 

The statement of _general covariance_ is that the distinct configurations of the gravitational field form the set $Riem(\Sigma)/Diff(\Sigma)$. In particular, if $\Sigma$ is [[compact topological space|compact]], then the [[Einstein-Hilbert action]] functional which *a priori* is defined on $Riem(\Sigma)$ descends to $Riem(\Sigma)/Diff(\Sigma)$

$$
  S_{EH} : Riem(\Sigma)/Diff(\Sigma) \to \mathbb{R}
  \,.
$$

While this captures the idea of general covariance accurately, for further development of the theory of [[gravity]], however, the set $Riem(\Sigma)/Diff(\Sigma)$ needs to be refined. It is really equipped with the structure of a [[smooth space]] $\mathbf{Riem}(\Sigma)/\mathbf{Diff}(\Sigma)$ (in order to perform [[variational calculus]] and hence derive the [[equations of motion]] of the theory), and second it is to be refined to a [[smooth infinity-groupoid|smooth groupoid]] $\mathbf{Riem}(\Sigma)\sslash\mathbf{Diff}(\Sigma)$.

Finally, for setups that admit to introduce [[fermions]]/[[spinors]] into the model one needs to refine Riemannian metrics to [[vielbein]] fields/[[orthogonal structures]]. The fully refined generally covariance smooth configuration groupoid is then $[\Sigma, \mathbf{orth}]\sslash \mathbf{Diff}(\Sigma)$, discussed in more detail [below](#GravityInHoTT).


### Relation to the "principle of equivalence" in gravity
 {#RelationToPrincipleOfEquivalenceInGravity}

The _[[equivalence principle (physics)|principle of equivalence]]_ in [[general relativity]] is formally the statement that around every point in a ([[pseudo-Riemannian metric|pseudo]]-)[[Riemannian manifold]] one can find a [[coordinate system]] such that the [[Levi-Civita connection]] vanishes ("[[Riemann normal coordinates]]"), which means that to **first [[infinitesimal space|infinitesimal]] order** around that point particle dynamics subject to the force of gravity is equivalent to dynamics in [[Minkowski spacetime]] with vanishing field of gravity.

By the above, this is a special case of the principle of general covariance: for every field configuration $g$ and every given point there is a gauge equivalent field configuration $f^* g$ such that the "force of gravity" (the Levi-Civita connection) vanishes at that point.

It is via this relation that the physical "[[equivalence principle (physics)|principle of equivalence]]" relates to the mathematical _[[principle of equivalence]]_: this says that formulations need to respect the given notion of [[equivalence]]/[[gauge transformation]], and so

[[principle of equivalence]] in mathematics $\Rightarrow$ principle of general covariance $\Rightarrow$ principle of equivalence in physics .


### In other topological field theories



## Formalization in homotopy type theory
 {#InHomotopyTypeTheory}

We discuss here that general covariance in field theory has a natural formalization in [[homotopy type theory]], hence internal to any [[(∞,1)-topos]]. For exposition, background and further details on the discussion of [[classical field theory|classical]]/[[quantum field theory]] in this fashion see ([Schreiber, ESI lectures](#SchreiberLectures)) and ([Schreiber-Shulman](#SchreiberShulman)).

The same kind of construction yields important [[moduli stacks]], for instance the [[moduli stack of Riemann surfaces]], see [this remark](moduli+space+of+curves#InTermsOfTheHigherToposOfSmoothStacks) there.

### Informal introduction
 {#InformalIntroduction}
 
Let $\Sigma$ be a [[smooth manifold]] to be thought of as [[spacetime]].

Then the central idea of _general covariance_ is that for

$$
  i_1 \;\colon\; U \hookrightarrow \Sigma
$$

and 

$$
  i_2 \;\colon\; U \hookrightarrow \Sigma
$$

two [[subsets]]/[[submanifolds]], they should be regarded as [[equivalence|equivalent]] if there is a [[diffeomorphism]] $\phi \;\colon\; \Sigma \stackrel{}{\longrightarrow} \Sigma$ which takes one to the other, hence such that 
$i_2 = \phi^\ast i_1 \coloneqq\phi \circ i_1 $.

That this statement can be puzzling if one thinks of the case $U = \ast$ as being just a single point is the content of the historical "[[hole argument]] [[paradox]]". 

But with just a little bit of formalization the apparent paradox is resolved, because the above evidently just says that the "[[moduli space]]" for "subsets of spacetime" is not the manifold $\Sigma$ itself, but is rather a "[[moduli stack]]" namely the [[quotient stack]] $\Sigma //Diff(\Sigma)$ of $\Sigma$ by the [[action]] of the [[diffeomorphism group]].

Indeed, the technical term "[[quotient stack]]" is precisely defined by the condition that for $U$ of the shape of a [[disk]]/[[coordinate chart]], then two maps

$$
  i \;\colon\; U \hookrightarrow \Sigma \longrightarrow \Sigma \sslash Diff(\Sigma)
$$

to it are equivalent if (and only if) there is a diffeomorphism relating them, as above. 

So if in a generally covariant field theory spacetime is not actually the manifold $\Sigma$, but rather the quotient stack $\Sigma \sslash Diff(\Sigma)$, then also a [[field (physics)|field]] in this generally covariant field theory should be a field on that quotient stack, not on $\Sigma$ itself.

For $\mathbf{Fields}$ a [[moduli space]]/[[moduli stack]] of [[field (physics)|fields]], in a non-generally covariant field theory a field configuration is simply a map

$$
  \Phi \;\colon\; \Sigma \longrightarrow \mathbf{Fields}
$$

and accordingly the [[configuration space|space of all field configurations]] is the [[mapping space]] $[\Sigma, \mathbf{Fields}]$.

From this it is clear that for a generally covariant field theory we are instead to declare that the space of field configurations is

$$
  [\Sigma \sslash Diff(\Sigma), \;\mathbf{Fields}]
  \,.
$$

And it is at this point that [[homotopy type theory]]/[[(infinity,1)-topos theory|higher topos theory]] works a little wonder for us -- namely it provides proof -- and this is what is discussed below -- that

$$
  [\Sigma \sslash Diff(\Sigma),\; \mathbf{Fields}]
  \simeq
  [\Sigma,\; \mathbf{Fields}] \sslash Diff(\Sigma)
  \,.
$$

In words, the right hand side is the time-honored answer: two fields _on_ a spacetime manifold $\Sigma$, which are such that one goes over into the other when pulled back along a diffeomorphism, are [[gauge equivalence|gauge equivalent]]. This is the statement of general covariance, derived here, formally, from just the condition that any two shapes _in_ spacetime are to be equivalent if related by a diffeomorphism.

Here to read the above equivalence as a theorem, we have to read the left hand side, as it should, be "in the context of $Diff(\Sigma)$-actions". Such [[context]]-dependence is precisely what _[[dependent type theory|dependent]]_ [[homotopy type theory]] takes care of, and this is what the following technical statement deals with.





### Introduction in terms of type theory

A basic idea of traditional [[dependent type theory]] is of course that [[types]] $A$ may appear _in [[context]]_ of other types $\Gamma$. The traditional interpretation of such a dependent type

$$
  x : \Gamma \vdash A(x) : Type
$$

is that of a $\Gamma$-parameterized family or _[[bundle]]_ of types, whose [[fiber]] over $x \in \Gamma$ is $A(x)$.

But in [[homotopy type theory]], types are [[homotopy types]] and, hence so are the contexts. A [[type in context]] is now in general something more refined than just a family of types. It is really a family of types equipped with _[[equivariance]]_ structure with respect to the [[homotopy groups]] of the context type.

Hence in homotopy theory [[types in context]] generically satisfy an [[equivariance]]-principle.

Specifically, if the context type is [[n-connected object in an (infinity,1)-topos|connected]] and [[pointed object|pointed]], then it is equivalent to the [[delooping]] $\Gamma \simeq \mathbf{B}G$ of an [[∞-group]] $G$. One finds -- this is discussed at _[[∞-action]]_ -- that the [[context]] defined by the type $\mathbf{B}G$ is that of $G$-[[equivariance]]: every type in the context is a type in the original context, but now equipped with a $G$-[[∞-action]]. In a precise sense, the homotopy type theory of $G$-$\infty$-actions is equivalent to plain homotopy type theory _in [[context]]_ $\mathbf{B}G$.

In the following we discuss this for the case that $G$ is an [[automorphism ∞-group]] of a type $\Sigma$ which is regarded as representing [[spacetime]] or a [[worldvolume]]. We show that in this context the rules of homotopy type theory automatically induce the principle of general covariance and naturally produce configurations spaces of generally covariant field theories: for $\mathbf{Fields}$ a moduli object for the given fields, so that a field configuration is a function $\phi : \Sigma \to \mathbf{Fields}$, the configuration space of _covariant_ fields is the [[function type]] $(\Sigma \to \mathbf{Fields})$ but formed in the "general covariance context" $\mathbf{B}\mathbf{Aut}(\Sigma)$. When [[categorical semantics|interpreted]] in [[smooth infinity-groupoid|smooth models]], $\mathbf{Conf}$ is the smooth groupoid of field configurations and diffeomorphism gauge transformations acting on them, the [[Lie integration|Lie integrations]] of the [[BRST complex]] whose degree-1 elements are the _diffeomorphism ghosts_. 

More precisely, we show the following.

+-- {: .num_defn}
###### Definition

Consider in homotopy type theory two types 
$\vdash \Sigma, \mathbf{Fields} : Type$, to be called _spacetime_ and _field moduli_. Let 

$$
  \vdash \mathbf{B}\mathbf{Aut}(\Sigma) : Type
$$

be the image of the name of $\Sigma$, with essentially unique term

$$
  \vdash \Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)
  \,.
$$

Perform the canonical context extension of $\Sigma$ and trivial context extension of $\mathbf{Fields}$ to get types in context

$$
  \Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)
  \vdash 
  \Sigma : Type
$$

and 

$$
  \Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)
  \vdash 
  \mathbf{Fields} : Type
  \,.
$$

Form then the type of field moduli 

"$\mathbf{Conf} \coloneqq (\Sigma \to \mathbf{Fields})$"

*in this context*:

$$
  \mathbf{Conf} \coloneqq 
  \;\;\;\;\;
  \Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)
  \vdash (\Sigma \to \mathbf{Fields}) : Type
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The [[categorical semantics]] of $\mathbf{Conf}$ in the model [[Smooth∞Grpd]] of the homotopy type theory, and for $\Sigma \in$ [[SmoothMfd]] $\hookrightarrow Smooth \infty Grpd$, is given by the [[diffeological space|diffeological groupoid]] 

$$
  \mathbf{Conf} 
    = 
  [\Sigma, \mathbf{Fields}]\sslash \mathbf{Diff}(\Sigma)
$$

whose objects are field configurations on $\Sigma$ and whose morphisms are diffeomorphism gauge transformations between them. In particular the corresponding [[Lie algebroid]] is dual to the [[BRST complex]] of fields with diffeomorphism ghosts in degree 1.

=--

### The ambient theory

Write $\mathbf{H}$ for the ambient [[homotopy type theory]], or rather an [[categorical semantics|interpretation]] given by an [[(∞,1)-topos]].
For standard applications in [[physics]] we have $\mathbf{H} = $ [[Smooth∞Grpd]] or [[SmoothSuper∞Grpd]] or similar, but none of the following general discussion depends on a concrete choice for $\mathbf{H}$.

Pick once and for all an [[object]] 

$$
  \Sigma \in \mathbf{H}
$$
 
supposed to represent the [[space]] underlying [[spacetime]] or the [[worldvolume]] of a [[model (in theoretical physics)]], 

### The diffeomorphism group

Write 

$$
  \mathbf{Aut}(\Sigma) \in Grp(\mathbf{H})
$$ 

for the [[automorphism ∞-group]] of $\Sigma$. As discussed there, this is the [[loop space object]] of the  [[homotopy image]]-factorization of

$$
  * \stackrel{\vdash \Sigma}{\to} Type
  \,,
$$

hence the factorization by an  [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] followed by a [[monomorphism in an (infinity,1)-category|monomorphism]]:

$$
  * \stackrel{}{\to} \mathbf{B}\mathbf{Aut}(\Sigma) 
    \stackrel{}{\hookrightarrow} Type
  \,.
$$

In the standard [[categorical semantics|interpretation]] of the homotopy type theory in $\mathbf{H} = $ [[Smooth∞Grpd]] $\Sigma$ could be an ordinary [[smooth manifold]] or [[orbifold]], in particular, and then $\mathbf{Aut}(\Sigma) = \mathbf{\Diff}(\Sigma)$ is the [[diffeomorphism group]] of $\Sigma$, regarded as a [[diffeological space|diffeological]] [[group object]]. In view of this archetypical example we will in the following often say _[[diffeomorphism]]_ for short instead of _auto-equivalence in $\mathbf{H}$_ and similarly refer to $\mathbf{Aut}(\Sigma)$ loosely as the _diffeomorphism group_ of $\Sigma$. But even in the specifical model $\mathbf{H} = $ [[Smooth∞Grpd]]/[[SmoothSuper∞Grpd]], $\Sigma$ can be much more general than a [[smooth manifold]] or [[supermanifold]] or [[orbifold]]. 

### The context of general covariance

Write then $\mathbf{B} \mathbf{Aut}(\Sigma) \in \mathbf{H}$ for the [[delooping]] of the diffeomorphism group. The essentially unique [[term]] of this type is to be thought of as being $\Sigma$ itself, and so we 
write it as

$$
  \vdash \Sigma : \mathbf{B} \mathbf{Aut}(\Sigma)
  \,.
$$

By the discussion at _[[∞-action]]_, a [[type in context]] of $\mathbf{B}\mathbf{Aut}(\Sigma)$

$$
  \Sigma : \mathbf{B} \mathbf{Aut}(\Sigma) \vdash V(\Sigma)
$$

is a type $\vdash V : Type$ in the absolute context equipped with an $\mathbf{Aut}(\Sigma)$-[[∞-action]] $\rho : V \times \mathbf{Aut}(\Sigma) \to V$ on it. The [[dependent sum]] 

$$
  \vdash \sum_{\Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)} V(\Sigma) : Type 
  \,,
$$

which we also write

$$
  V \sslash \mathbf{Aut}(\Sigma)
  \coloneqq 
  \sum_{\Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)}
   V(\Sigma)
  \,,
$$

is the total space of the universal [[associated ∞-bundle|associated]] $V$-[[fiber ∞-bundle]]:

$$
  \array{
     V &\to& \sum_{\mathbf{B}\mathbf{Aut}(\Sigma)} V(\Sigma)
     \\
      && \downarrow^{\overline{\rho}}
     \\
      && \mathbf{B}\mathbf{Aut}(\Sigma)
  }
  \,.
$$

Hence the [[categorical semantics|interpretation]] of the context $\Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)$  is the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}\mathbf{Aut}(\Sigma)}$ and equivalently is the [[(∞,1)-topos]] of objects in $\mathbf{H}$ equipped with $G$-[[∞-actions]] and of $G$-[[equivariance|equivariant]] [[morphisms]] between them:

$$
  \mathbf{H}_{/\mathbf{B}\mathbf{Aut}(\Sigma)}
  \simeq
  Act_{\mathbf{H}}(\mathbf{Aut}(\Sigma))
  \,.
$$

Hence a [[type in context]] $\Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)$ is a "generally covariant type" with respect to $\Sigma$ in the sense that it transforms [[covariant functor|covariantly]] by equivalences under diffeomorphisms of $\Sigma$. In summary then

**Fact.** $\Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)$ _is the **[[context]] of general covariance** with respect to $\Sigma$. 

In the precise formal sense.

In particular, $\Sigma$ itself is canonically equipped with the defining action of $\mathbf{Aut}(\Sigma)$ on it, which [[syntax|syntactically]] we may write

$$
  \Sigma : \mathbf{B}\mathbf{Aut}(\Sigma) \vdash \Sigma : Type
$$

and which [[categorical semantics|semantically]] is exhibited by the universal  [[associated ∞-bundle|associated]] $\Sigma$-[[fiber ∞-bundle]]

$$
  \array{
    \Sigma &\to& \sum_{\Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)} \Sigma
    \\
    && \downarrow^{\overline{\rho_{\Sigma}}}
    \\
    && \mathbf{B} \mathbf{Aut}(\Sigma)
  }
  \,,
$$

given by the [[pullback]] of the [[universe]] $\widetilde Type \to Type$ along the defining [[monomorphism in an (infinity,1)-category|inclusion]] $\mathbf{B}\mathbf{Aut} \hookrightarrow Type$.

Here the total space 

$$
  \Sigma \sslash \mathbf{Aut}(\Sigma) 
  \coloneqq 
  \sum_{\Sigma : \mathbf{B}\mathbf{Aut}(\Sigma) } \Sigma
$$ 

is the [[homotopy quotient]] or [[action groupoid]] of $\Sigma$ by $\mathbf{Aut}(\Sigma)$. This is the type characterized by the fact that a [[function]] $f : U \to \Sigma \sslash \mathbf{Aut}(\Sigma)$ is a function to $\Sigma$ which is regarded as ([[gauge equivalence|gauge]]) [[equivalence|equivalent]] to another function to $\Sigma$ if both differ by postcomposition with a diffeomorphism of $\Sigma$.


### Generally covariant field configuration spaces

Let now

$$
  \mathbf{Fields} \in \mathbf{H}
$$ 

be an object that represents the [[moduli ∞-stack]] of field configurations on $\Sigma$ for some [[model (in theoretical physics)]] to be described. For instance for $G \in Grp(\mathbf{H})$ an [[∞-group]] and $\mathbf{H}$ a [[cohesive homotopy type theory]], we could have $\mathbf{Fields} = \mathbf{B}G_{conn}$ the moduli for a choice of $G$-[[connection on an ∞-bundle|principal ∞-connection]], being the moduli for $G$-([[higher gauge theory|higher]])[[gauge fields]]. For general $\mathbf{Fields} = X \in \mathbf{H}$ we may always regard $X$ as the [[target space]] of a [[sigma-model]].

Then the [[internal hom]] 

$$
  \mathbf{Fields}(\Sigma) \coloneqq [\Sigma, \mathbf{Fields}] \in \mathbf{H}
$$ 

hence the [[function type]]

$$
  \vdash \Sigma \to \mathbf{Fields} : Type
$$

is the _naive_ [[configuration space]] of the model. This is not generally covariant, precisely so by the above definition: it is not in the generally covariant context $\mathbf{H}_{/\mathbf{B} \mathbf{Aut}(\Sigma)}$.

But by the [[inverse image]] of the $\mathbf{B}\mathbf{Aut}(\Sigma)$-[[dependent product]] [[étale geometric morphism]]

$$
  \mathbf{H}_{/\mathbf{B}G}
  \stackrel{\overset{\sum_{\mathbf{B}\mathbf{Aut}(\Sigma)}}{\to}}{
  \stackrel{\overset{}{\leftarrow}}{\underset{\prod_{\mathbf{B}\mathbf{Aut}(\Sigma)}}{\to}}}
  \mathbf{H}
$$

which is [[context enlargement]] by $\mathbf{B}\mathbf{Aut}(\Sigma)$, 
the moduli type $\mathbf{Fields}$ is freely moved to the general covariant context, where it is regarded as equipped with the [trivial ∞-action](infinity-action#TrivialAction). Accordingly we will write just $\mathbf{Fields} \in \mathbf{H}_{/\mathbf{B}\mathbf{Aut}(\Sigma)}$ with that trivial action understood, which is justified by the precise syntactic expression for it:

$$
  \Sigma : \mathbf{B}\mathbf{Aut}(\Sigma) \vdash \mathbf{Fields} : Type
$$

We may then form the _configuration space of fields in the generally covariant context_ . As before, a field $\phi$ should be a function on $\Sigma$ with values in the moduli type of field configurations, but now we interpret this statement in the generally covariant context. Syntactically this simply means that a field is now a term in $\mathbf{B}\mathbf{Aut}(\Sigma)$-context

$$
  \Sigma : \mathbf{B}\mathbf{Aut}(\Sigma) 
  \vdash
  \phi : \Sigma \to \mathbf{Fields}
$$

and that accordingly the configuration space of fields is 

$$
  \Sigma : \mathbf{B}\mathbf{Aut}(\Sigma) 
  \vdash
  \Sigma \to \mathbf{Fields} : Type
  \,.
$$

The [[categorical semantics|semantics]] of this is the 
[[internal hom]] in the [[slice (∞,1)-topos]], the _[Internal hom of ∞-actions](infinity-action#CartesianClosedMonoidalStructure)_

$$
  \mathbf{Conf} 
    \coloneqq
  [\Sigma \sslash \mathbf{Aut}(\Sigma), \mathbf{Fields}]
  \in
  \mathbf{H}_{/\mathbf{Aut}(\Sigma)}
  \,,
$$

The central observation now is that discussed at _[∞-action -- Examples -- General covariance](infinity-action#GeneralCovariance)_:

$$
  \mathbf{Conf} \simeq [\Sigma,\mathbf{Fields}] \sslash \mathbf{Aut}(\Sigma)
$$

is the [[homotopy quotient]] of the naive fields $\in \mathbf{Fields}(\Sigma)$ by the action of the [[diffeomorphism group]], exhibiting a [[gauge equivalence]] between any two field configurations that differ after pullback along a diffeomorphism.

This is precisely as it should be for configuration space of generally covariant theories. We have found:

**Fact**. In terms of homotopy type theory, configuration spaces of a generally covariant theory over $\Sigma$ are precisely the ordinary configuration spaces of fields, but formed in the context $\mathbf{B}\mathbf{Aut}(\Sigma)$:

$$
  \mathbf{Conf} =_{def}
  \;\;\;\;\;\;
\Sigma : \mathbf{B}\mathbf{Aut}(\Sigma) \vdash (\Sigma \to \mathbf{Field}) : Type
  \,.
$$


### Generally covariant field of gravity
 {#GravityInHoTT}

We now spell out the example of ordinary [[Einstein]]-[[gravity]] in this language. Plenty of further examples work analogously.

For pure [[gravity]], we choose $\mathbf{H} = $ [[Smooth∞Grpd]] or $=$[[SynthDiff∞Grpd]].

If we denote by $D^n \in $ [[SynthDiff∞Grpd]] the first order [[infinitesimal object|infinitesimal neighbourhood]] of the origin in the [[Cartesian space]] $\mathbb{R}^n$, then 

$$
  GL(n) = \mathbf{Aut}(D^n)
$$ 

is the [[automorphism ∞-group]] of $D^n$. Accordingly we write the unique term of the [[delooping]] $\mathbf{B}GL(n)$ as

$$
  \vdash D^n : \mathbf{B}GL(n)
  \,.
$$



The fields of Einstein gravity are [[orthogonal structures]] ([[Riemannian metrics]]) on a [[smooth manifold]] $\Sigma \in $ [[SmoothMfd]] $\hookrightarrow \mathbf{H}$ of [[dimension]] $n$. 
As discussed at _[[orthogonal structure]]_ and _[[vielbein]]_, we are to regard $\Sigma$ in the [[context]] of the [[delooping]] of the [[general linear group]] $GL(n) \in Grp(\mathbf{H})$ via its [[tangent bundle]] $T \Sigma \to \Sigma$, by which we always mean here the $GL(n)$-[[principal bundle]] to which the tangent bundle is [[associated bundle|associated]].

By the discussion at _[[principal ∞-bundle]]_ this is modulated by a morphism

$$
  (\Sigma \stackrel{\vdash T \Sigma}{\to} \mathbf{B} GL(n))
  \in
  \mathbf{H}_{/\mathbf{B} GL(n)}
$$

to the [[delooping]] $\mathbf{B}GL(n)$ of $GL(n)$ (the [[moduli stack]] of $GL(n)$-[[principal bundles]]) in that we have a [[fiber sequence]]

$$
  \array{
    T \Sigma &\to& \Sigma
    \\
    && \downarrow^{\mathrlap{\vdash T \Sigma}}
    \\
    && \mathbf{B}GL(n) 
  }
$$

in $\mathbf{H}$. (A detailed exposition of this and the following, with further pointers, is in ([Schreiber, ESI lectures](#SchreiberLectures)).)

Therefore the [[syntax]] of the tangent bundle as a [[dependent type]] is

$$
  D^n : \mathbf{B}GL(n) \vdash T \Sigma(D^n) : Type
$$

and since $D^n$ is essentially unique we will notationally suppress it in the [[succedent]] on the right and just write


$$
  D^n : \mathbf{B}GL(n) \vdash T \Sigma : Type
  \,.
$$

Let then

$$
  (\mathbf{B} O(n) \stackrel{\mathbf{orth}}{\to} \mathbf{B} GL(n)) 
  \in 
  \mathbf{H}_{/\mathbf{B}GL(n)}
$$

be the [[delooping]] of the inclusion $O(n) \to GL(n)$ of the [[maximal compact subgroup]] of $GL(n)$, the [[orthogonal group]] $O(n)$, regarded as an [[object]] in the [[slice-(∞,1)-topos]] over $\mathbf{B}GL(n)$. Since this sits in the [[homotopy fiber sequence]]

$$
  \array{
    GL(n)/O(n) &\to& \mathbf{B}O(n)
    \\
    && \downarrow^{\mathrlap{orth}}  
    \\
    && \mathbf{B}GL(n)
  }
$$

with the [[coset]] [[smooth space]] $GL(n)/O(n)$, the [[syntax]] of this object is the [[dependent type]]

$$
  D^n : \mathbf{B}GL(n) \vdash GL(n)/O(n) : Type
  \,.
$$

In view of the [[equivalence of (∞,1)-categories]]

$$
  \mathbf{H}_{/\mathbf{B}GL(n)} \simeq Act_{\mathbf{H}}(GL(n))
$$

this expresses the canonical $GL(n)$-[[∞-action|action]] on the coset $GL(n)/O(n)$ (by mutliplication from the "other side").

The [[syntax]] of the [[moduli stack]] of [[vielbein]] fields /  [[Riemannian metrics]] on $\Sigma$ is

$$
  \vdash \prod_{D^n : \mathbf{B}GL(n)} T \Sigma \to GL(n)/O(n) : Type
  \,.
$$

This almost verbatim expresses the familiar statement:

> A [[vielbein]] on $\Sigma$ is a $GL(n)$-equivariant map from $T \Sigma$ to the coset $GL(n)/O(n)$.

The [[categorical semantics]] of such a [[vielbein]] $e$ is as a diagram

$$
  \array{
    \Sigma && \stackrel{}{\to}&& \mathbf{B}O(n)
    \\
    & \searrow &\swArrow_{e}& \swarrow_{\mathrlap{orth}}
    \\
    && \mathbf{B}GL(n)
  }
  \,.
$$

This in turn almost verbatim expresses the familar equivalent statement

> A vielbein is a [[reduction of the structure group]] of the $GL(n)$-[[principal bundle]] $T \Sigma$ along $O(n) \to GL(n)$.

This is still the naive space of fields, not yet generally covariant. So we next pass to the general covariant $\mathbf{B}\mathbf{Aut}(T\Sigma)$-[[context]] and form the correct generally covariant space of fields, being the [[type in context]] $\mathbf{B} \mathbf{Aut}(T \Sigma)$ given by

$$
  \mathbf{Conf}
  \coloneqq
  \vdash
   \prod_{D^n : \mathbf{B}GL(n)}
   \sum_{T\Sigma : \mathbf{B}\mathbf{Aut}(T\Sigma)}
   T \Sigma \to GL(n)/O(n)   : Type
  \,,
$$

which is the integrated [[BRST complex]] of Einstein gravity field configurations modulo diffeomorphism ghosts: the [[smooth infinity-groupoid|smooth groupoid]] whose 

* [[objects]] are [[vielbein]] fields $e$ on $X$;

* [[morphisms]] are

  1. orthogonal frame transformations of the fibers of the tangent bundle;

  1. general diffeomorphisms of the base $\Sigma$.

We unwind this a bit more. 

A slight subtlety in interpreting the above expression is that in 

$$
  D^n : \mathbf{B}GL(n) \vdash \mathbf{B}Aut(T \Sigma) : Type
$$

the [[automorphism ∞-group]] of the tangent bundle it to be formed in the [[context]] of $\mathbf{B}GL(n)$. By the discussion at _[[automorphism ∞-group]]_ the [[delooping]] $\mathbf{B}Aut(T \Sigma)$ is the [[∞-image]] of the name


$$
  (* \stackrel{}{\to} Type) \in \mathbf{H}_{/\mathbf{B}GL(n)}
$$

of $(\Sigma \to \mathbf{B}GL(n))$ in the slice. By the discussion at [slice-(∞,1)-topos -- Object classifier](over-%28infinity%2C1%29-topos#ObjectClassifier) the [[object classifier]] in the slice is the [[projection]] $(Type \times \mathbf{B}GL(n) \to \mathbf{B}GL(n))$. 

So the name and its pullback are given by a diagram of the form

$$
  \array{
    \Sigma &&\to&& \widehat{Type} \times \mathbf{B}GL(n)
    \\
    {}^{\mathllap{}}\downarrow &&\swArrow&& \downarrow
    \\
    \mathbf{B}GL(n) &&\stackrel{(\vdash \Sigma, id)}{\to}&& Type \times \mathbf{B}GL(n)
    \\ 
    & {}_{\mathllap{id}}\searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}GL(n)
  }
$$

in $\mathbf{H}$. Here the [[∞-image]] is directly read off to be the factorization in the third column of

$$
  \array{
    T \Sigma
    &\to&
    \Sigma 
     &\to&  
      (T \Sigma \sslash \mathbf{Aut}(T\Sigma)) \times \mathbf{B}GL(n)
     &\to& 
    \widehat{Type} \times \mathbf{B}GL(n)
    \\
    \downarrow 
    &&
    {}^{\mathllap{}}\downarrow && \downarrow
     && \downarrow
    \\
    * &\to& 
       \mathbf{B}GL(n) 
       &\stackrel{}{\to}& 
       \mathbf{B}\mathbf{Aut}(T \Sigma) \times \mathbf{B}GL(n)
       &\to& 
       Type \times \mathbf{B}GL(n)
    \\ 
    && & {}_{\mathllap{id}}\searrow &\swArrow& \swarrow
    \\
    && && \mathbf{B}GL(n)
  }
  \,,
$$

where each square and hence each rectangle is an [[(∞,1)-pullback]] in $\mathbf{H}$. This shows that the automorphism $\infty$-group of $T \Sigma$ in the context of $\mathbf{B}GL(n)$ is just the absolute automorphism $\infty$-group freely [[context extension|context extended]]. The [[categorical semantics]] of the [[dependent type]]

$$
  D^n \colon \mathbf{B}GL(n), T \Sigma \colon \mathbf{B}\mathbf{Aut}(T \Sigma)
  \vdash
  T \Sigma \colon Type
$$

is the third column from the left in the above diagram. This means that the dependent sum in 

$$
  \mathbf{Conf}
  \coloneqq
  \vdash
   \prod_{D^n : \mathbf{B}GL(n)}
   \sum_{T\Sigma : \mathbf{B}\mathbf{Aut}(T\Sigma)}
   T \Sigma \to GL(n)/O(n)   : Type
  \,,
$$

forms the internal hom in $\mathbf{H}_{/\mathbf{B}GL(n)}$ between the homotopy fiber of that third column formed in $\mathbf{H}_{/\mathbf{B}GL(n)}$, which is the second column (and therefore now does rememeber the $GL(n)$-action on $T \Sigma$) with $\mathbf{orth}$, rememeberting that the result has an $\mathbf{Aut}(T\Sigma)$-action by precomposition.





## References
 {#References}

### History
 {#ReferencesHistory}

The pre-history of the idea of general covariance is reviewed in 

* H. G. Alexander (ed.), _The Leibniz-Clarke Correspondence: Together With Extracts from Newton's Principia and Opticks_, Manchester University Press (1998)
 {#Alexander}

The original articles by Einstein on the idea of general covariance include his _Entwurf_ (sketch)

* [[Albert Einstein]], M. Grossmann, _Entwurf einer verallgemeinerten Relativit&#228;tstheorie und einer Theorie der Gravitation_ Zeitschrift f&#252;r Math. Phys. 62, 225&#8211;259 (1914)
 {#EinsteinGrossmann}

of the theory of [[gravity]] (where the notion of general covariance is still rejected) and then the full development of [[general relativity]]

* [[Albert Einstein]], _Die Grundlage der allgemeinen Relativit&#228;tstheorie. Ann. Phys. (Leipzig) 49, 769&#8211;822 (1916)
 {#Einstein1916}

where it is fully embraced.

An attempt at a fairly comprehensive review of the history of the idea of general covariance and its reception up to modern days is in

* J. D. Norton, _General covariance and the foundations of general relativity: eight decades of dispute_, Rep. Prog. Phys **56** (1993), ([original pdf](http://www.pitt.edu/~jdnorton/papers/decades.pdf), [reprint pdf](http://www.pitt.edu/~jdnorton/papers/decades_re-set.pdf))
 {#Norton}


### Formalizations of general covariance
 {#ReferencesFormalizations}

A formalization in the context of [[AQFT]] is proposed and discussed in 

* [[Klaus Fredenhagen]], [[Rudolf Haag]], _Generally covariant quantum field theory and scaling limits_,  Comm. Math. Phys. Volume 108, Number 1 (1987), 91-115. ([EUCLID](http://projecteuclid.org/euclid.cmp/1104116359))

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Rainer Verch]], _The generally covariant locality principle -- A new paradigm for local quantum physics_, Commun.Math.Phys.237:31-68,2003 ([math-ph/0112041](http://arxiv.org/abs/math-ph/0112041))

A review is in

* [[Romeo Brunetti]], Martin Porrmann, Giuseppe Ruzzi, _General Covariance in Algebraic Quantum Field Theory_ ([arXiv:math-ph/0512059](http://arxiv.org/abs/math-ph/0512059))
 {#BrunettiPorrmannRuzzi}

For more see the references at _[[AQFT on curved spacetimes]]_.

Via [[quotient stacks]] in [[BV-formalism]]:

* [[Filip Dul]]: *General Covariance from the Viewpoint of Stacks*,  Lett Math Phys **113** (2023) 30 &lbrack;[arXiv:2112.15473](https://arxiv.org/abs/2112.15473), [doi:10.1007/s11005-023-01653-3](https://doi.org/10.1007/s11005-023-01653-3)&rbrack;


### Formalization in homotopy type theory
 {#FormalizationInHomtopyTypeTheory}

Background and context for the above formalization of [[classical field theory|classical]]/[[quantum field theory]] in [[homotopy type theory]] see

* [[Urs Schreiber]], _[[twisted smooth cohomology in string theory]]_, Lectures at _[ESI program on K-theory and quantum fields](http://maths-old.anu.edu.au/esi/2012/)_ (2012)
 {#SchreiberLectures}

* [[Urs Schreiber]], [[Mike Shulman]], _[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]_ (2012)
 {#SchreiberShulman}

See also _[[higher category theory and physics]]_.