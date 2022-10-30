

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _model structure for Segal operads_  is a [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category]] of [[(∞,1)-operads]] regarding these as [[enriched (∞,1)-category|∞Grpd-enriched]] [[operads]].

It is the [[operad|operadic]] analog of the _[[model structure for Segal categories]]_: its [[fibrant objects]] are operadic analogs of [[Segal categories]].

## Definition

Write $\Omega$ for the [[tree category]], the [[site]] for [[dendroidal sets]].

### Segal operads

Write $\eta$ for the tree with a single edge and no vertices.
Write 

$$
  sdSet := [\Omega^{op}, sSet]
$$ 

for the category of [[simplicial presheaves]] on the tree category -- _simplicial dendroidal sets_ or _dendroidal simplicial sets_ (see [[model structure for complete dendroidal Segal spaces]] for more on this).

+-- {: .num_defn #InclusionOfSegalPreOperads}
###### Definition

A **Segal pre-operad** $X \in [\Omega^{op}, sSet]$ is a simplicial dendroidal set such that $X(\eta)$ is a [[discrete object|discrete]] [[simplicial set]] (a plain set regarded as a simplicially constant simplicial set). Write

$$
  SegalPreOperad \hookrightarrow [\Omega^{op}, sSet]
$$

for the [[full subcategory]] on the Segal pre-operads.

A **Segal operad** is a Segal pre-operad such that for every [[tree]] $T \in \Omega$ the [[powering]] 

$$
  X^{\Omega[T]} \to X^{Sp(T)}
  \in
  sSet
$$ 

of the [[spine]] inclusion $(Sp(T) \hookrightarrow T) \in$ [[dendroidal set|dSet]] into $X$ is an [[weak equivalence|acyclic]] [[Kan fibration]]. Write

$$
  SegalOperad \hookrightarrow SegalPreOperad
$$

for the [[full subcategory]] on the Segal operads.

A **Reedy-fibrant Segal operad** is a Segal operad which is moreover fibrant in the [[generalized Reedy model structure]] $[\Omega^{op}, sSet]_{gReedy}$.

=--

This is ([Cisinski-Moerdijk, def. 7.1, def. 8.1](#CisinskiMoerdijk)).

+-- {: .num_remark }
###### Remark

The definition of Segal pre-operads encodes a [[set]] of colors of an [[operad]], together with for each [[tree]] $T$ an [[∞-groupoid]] of operations in the operad of the shape of this tree  --- notably $\infty$-groupoids of $n$-ary operations if the tree is the $n$-corolla, $T = C_n$.

The condition on Segal operads encodes the existence of _composition_ of these operad operations by [[∞-anafunctors]]. See the discussion at _[[Segal category]]_ for more on this.

The Reedy fibrancy condition is mostly a technical convenience. 

=--

+-- {: .num_prop }
###### Obervation

The inclusion def. \ref{InclusionOfSegalPreOperads} has a [[left adjoint|left]] and [[right adjoint|right]] [[adjoint functors]]

$$
  sdSet 
  \stackrel{\overset{\gamma_!}{\to}}{\stackrel{\overset{\gamma^*}{\leftarrow}}{\underset{\gamma_*}{\to}}}
  SegalPreOperad
  \,.
$$

=--

+-- {: .proof}
###### Proof

One way to see the existence of the adjoints is to note that 
$SegalPreOperad$ is a [[category of presheaves]] over the [[site]] $S(\Omega)$ which is the [[localization]] of $\Omega \times \Delta$ at morphisms of the form $(-,Id_\eta)$, where $\eta$ is the tree with one edge and no vertex. Write

$$
  \gamma : \Delta \times \Omega \to S(\Omega)
$$

for the [[localization]] functor, then the inclusion of Segal pre-operads is the precomposition with this functor

$$
  \gamma^* : SegalPreOperad \simeq [S(\Omega)^{op}, sSet] \hookrightarrow [\Omega^{op}, sSet]
  \,.
$$

Therefore the left and right adjoint to $\gamma^*$ are given by left and right [[Kan extension]] along $\gamma$.

Explicitly, these adjoints are given as follows.

For $X \in [\Omega^{op}, sSet]$, the Segal pre-operad $\gamma_!(X)$ sends a tree $T$ 
either to $X(T)$, if $T$ is non-linear, hence if it admits no morphism to $\eta$, or else to the [[pushout]]

$$
  \array{
    X(\eta) &\to& X(T)
    \\
    \downarrow && \downarrow
    \\
    \pi_0 X(\eta) &\to& \gamma_!(X)(T)
  }
$$

in [[sSet]], where the top morphism is $X(T \to \eta)$ for the unique morphism to $\eta$.

In words, $\gamma_!(X)$ is obtained from $X$ precisely by contracting the simplicial set of colors to its set of connected components.

=--


### Special morphisms

We discuss morphisms between Segal pre-operads with special properties, which will appear in the model structure. 

+-- {: .num_defn #NormalMonomorphism}
###### Definition

Say a morphism $f$ in $SegalPreOperad$ is a **normal monomorphism** precisely if $\gamma^*(f)$ is a normal monomorphism (see [[generalized Reedy model structure]]),  which in turn is the case if it is simplicial-degreewise a normal morphisms of [[dendroidal sets]] (see there for details).

Correspondingly, a Segal pro-operad $X$ is called _normal_ if $\emptyset \to X$ is a normal monomorphism.

=--

+-- {: .num_defn #PreOperadAcyclicFibration}
###### Definition

A morphism in $SegalPreOperad$ is called an **acyclic fibration** precisely
if it has the [[right lifting property]] against all normal monomorphisms, def. \ref{NormalMonomorphism}.

=--

+-- {: .num_defn #SegalWeakEquivalence}
###### Definition

Say a morphism $f$ in $SegalPreOperad$ is a _Segal weak equivalence_ precisely if $\gamma^*(f)$ is a weak equivalence in the [[model structure for dendroidal complete Segal spaces]] $[\Omega^{op}m, sSet]_{gReedy \atop cSegal}$.

=--


+-- {: .num_defn #WeakEquivalencesAndFibrations}
###### Definition

Call a morphism in $SegalPreOperad$

* a weak equivalence precisely if it is a Segal weak equivalence, def. \ref{SegalWeakEquivalence};

* a cofibration precisely if it is a normal monomorphism, def. \ref{NormalMonomorphism}.

=--

Theorem \ref{ExistenceOfTheModelStructure} below asserts that this is indeed a model category struture whose fibrant objects are the Segal operads.


## Properties

### Of the various classes of morphisms

+-- {: .num_lemma }
###### Lemma

If $f : X \to Y$ in $[\Omega^{op}, sSet]$ is a normal monomorphism and 
$\pi_0 X(\eta) \to \pi_0 Y(\eta)$ is a monomorphism, then $\gamma_!(f)$
is normal in $SegalPreOperad$. 

=--

([Cis-Moer, lemma 7.4](#CisinskiMoerdijk)).

+-- {: .num_prop }
###### Proposition

The class of normal monomorphisms in $SegalPreOperad$ is 
[[cofibrantly generated model category|generated]] (under
[[pushout]], [[transfinite composition]] and [[retracts]]) by the set

$$  
  \{
     \gamma_!(\partial \Delta[n] \times \Omega[T]  \cup \Delta[n] \times \partial \Omega[T])
     \to
    \gamma_! (\Delta[n], \Omega[T])
  \}_{n \in \Delta, T \in \Omega, {\vert T\vert} \geq 1}
 \cup
  \{
    \emptyset \to \eta
  \}
$$

=--

([Cis-Moer, prop 7.5](#CisinskiMoerdijk)).


+-- {: .num_prop }
###### Proposition

Let $X \in [\Omega^{op}, sSet]_{gReedy \atop Segal}$ be fibrant. Then $\gamma_* X$ is a Reedy fibrant Segal operad. If $X$ is moreover fibrant in $[\Omega^{op}, sSet]_{gReedy \atop cSegal}$ then the [[unit of an adjunction|counit]] $\gamma^* \gamma* X \to X$ is a weak equivalence in $[\Omega^{op}, sSet]_{gReedy \atop cSegal}$.

=--

([Cis-Moer, prop 8.2](#CisinskiMoerdijk)).

+-- {: .num_lemma #AcyclicFibrationsAreIndeedWeakEquivalences}
###### Lemma

An acyclic fibration in $SegalPreOperad$, def. \ref{PreOperadAcyclicFibration}, is also a weak equivalence in $[\Omega^{op}, sSet]_{gReedy \atop Segal}$.

=--

([Cis-Moer, prop 8.12](#CisinskiMoerdijk)).

### Of the model structure itself

+-- {: .num_theorem #ExistenceOfTheModelStructure}
###### Theorem

The structures in  def. \ref{WeakEquivalencesAndFibrations} 
make the category $SegalPreOperad$ a [[model category]] which is

* [[cofibrantly generated model category|cofibrantly generated]];

* [[left proper model category|left proper]].

=--

This is ([Cis-Moer, theorem 8.13](#CisinskiMoerdijk)).

+-- {: .proof}
###### Proof

The existence of the cofibrantly generated model structure follows with _[Smith's theorem](combinatorial+model+category#SmithTheorem)_: by the discussion there it is sufficient to notice that 

1. the Segal equivalences are an accessibly embedded accessible full subcategory of the arrow category;

1. the acyclic cofibrations are closed under pushout and retract;

   (both of these because these morphisms come from the [[combinatorial model category]] $[\Omega^{op}, sSet]_{gReedy \atop cSegal}$)

1. the morphisms with right lifting against the normal monomorphisms are weak equivalences, by lemma \ref{AcyclicFibrationsAreIndeedWeakEquivalences}.


=--

### Relation to other model structures

We discuss the relation to various other model structures for operads. For an overview see _[[table - models for (infinity,1)-operads]]_.

#### To dendroidal complete Segal spaces

(...) [[model structure for dendroidal complete Segal spaces]]

## References

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal Segal spaces and infinity-operads_ ([arXiv:1010.4956](http://arxiv.org/abs/1010.4956))
 {#CisinskiMoerdijk}

[[!redirects Segal operad]]
[[!redirects Segal operads]]
