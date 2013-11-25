
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of [[formally étale morphism]] between [[schemes]].

## Definition

We first state the traditional 

* _[Explicit definition in components](#ExplicitlyInComponents)_

Then we give the abstract

* _[Characterization by reduction/infinitesimal shape/de Rham Space](#CharacterizationByReductionModality)_

### Explicitly in components
 {#ExplicitlyInComponents}

+-- {: .num_defn #ExplicitDefinition}
###### Definition

A [[morphism]] of [[commutative rings]] $R \hookrightarrow A$
is called _formally &#233;tale_ if for every ring $B$ and for every [[nilpotent ideal]] $I \subset B$ and for every [[commuting diagram]] of the form

$$
  \array{
    B/I &\leftarrow& A
    \\
    \uparrow && \uparrow
    \\
    B &\leftarrow& R
  }
$$

there is a unique diagonal morphism

$$
  \array{
    B/I &\leftarrow& A
    \\
    \uparrow &\swarrow& \uparrow
    \\
    B &\leftarrow& R
  }
$$

that makes both triangles commute.

=--

(e.g. [Stacks Project 57.9, 57.12](#StackProject))

By [[Isbell duality|formal duality]] and [[sheafification|locality]] this yields a notion of formally &#233;tale morphisms of [[affine varieties]] and of [[schemes]].


### Characterization by reduction/infinitesimal shape/de Rham Space
 {#CharacterizationByReductionModality}

+-- {: .num_defn }
###### Definition

Write [[CRing]] for the [[category]] of [[commutative rings]].
Write $Sh(CRing)$ for the [[category of sheaves]] ([[presheaves]], [[(infinity,1)-presheaves]]) over $CRing$.
 
=--

+-- {: .num_defn #ReductionOnRings}
###### Definition

Write

$$
  Red \;\colon\; CRing \longrightarrow CRing
$$

for the [[functor]] which sends a [[commutative ring]] $R$ to its [[reduced scheme|reduced ring]] $R/I$, where $I$ is the [[nilradical]].

=--

+-- {: .num_prop #DifferentialCohesionModality}
###### Proposition

There is an [[adjoint triple]] of [[idempotent monad|idempotent]] [[comonad|co]]-[[monads]]

$$
  (Red \dashv \int_{inf} \dashv \flat_{inf}) \;\colon\; PSh(CRing) \longrightarrow PSh(CRing)
$$

where the [[left adjoint]] [[comonad]] $Red$ is given on [[representable functor|representables]] by the [[reduced scheme|reduction]] functor of def. \ref{ReductionOnRings}.

=--

This is for the most part probably [[folklore]]. It is observed more or less explicitly for instance in the unpublished notes/preprints ([Simpson-Teleman 97](#SimpsonTeleman97), [Kontsevich-Rosenberg 04](#KontsevichRosenberg04)). More discussion of how to extract the above from these references is at _[[Q-category]]_.

+-- {: .num_remark }
###### Remark

Here $\int_{inf}$ sends a [[scheme]] to its [[de Rham space]].

=--


+-- {: .num_remark }
###### Remark

Since in terms of the [[internal logic|internal]] [[type theory]] of the [[topos]] $Sh(CRing)$ an [[idempotent monad|idempotent]] ([[comonad|co]]-)[[monad]] is a _[[modality]]_, the operators in prop. \ref{DifferentialCohesionModality} may be thought of as (co-)modalities. We may call them, respectively 

[[reduction modality]] $\dashv$ [[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]].

The collection of these we say equips $Sh(CRing)$ with _[[differential cohesion]]_.

=--

+-- {: .num_prop }
###### Proposition

A morphism $f \;\colon\; Spec A \to Spec R$ in $CRing^{op} \hookrightarrow Sh(CRing)$ is 
formally &#233;tale, def. \ref{ExplicitDefinition}, precisely if it is $\int_{inf}$-[[modal type|modal]] relative $Spec R$, hence if the [[natural transformation|naturality square]] of the [[infinitesimal shape modality]]-[[unit of a monad|unit]] 

$$
  \array{
    Spec A &\longrightarrow& \int_{inf} Spec A
    \\
    \downarrow && \downarrow
    \\
    Spec R &\longrightarrow& \int_{inf} Spec R
  }
$$

is a [[pullback]] square.

=--

+-- {: .proof}
###### Proof

Evaluated on $B \in CRing$ any object, by the [[Yoneda lemma]] and the $(Red \dashv $\int_{inf}$)$-[[adjunction]], the naturality square becomes

$$
  \array{
    CRing(A,B) &\longrightarrow& CRing(A,B/I)
    \\
    \downarrow && \downarrow
    \\
    CRing(R,B) &\longrightarrow& CRing(R,B/I)
  }
  \,.
$$

in [[Set]]. Chasing elements through this shows that this is a [[pullback]] precisely if the condition in def. \ref{ExplicitDefinition} holds.

=--

## Properties


### Relation to &#233;tale morphism

Formally &#233;tale morphisms of schemes which are in addition [[locally of finite presentation]] are equivalently [[étale morphisms of schemes]].

Relaxing this finiteness condition yields the notion of [[weakly étale morphisms]].

[[étale morphism of schemes|étale morphism]] $\Rightarrow$ [[pro-étale morphism of schemes|pro-étale morphism]] $\Rightarrow$ [[weakly étale morphism of schemes|weakly étale morphism]] $\Rightarrow$ [[formally étale morphism of schemes|formally étale morphism]]

## References

The traditional formulation is for instance in 

* [[The Stacks Project]], _[57.9. Formally smooth, &#233;tale, unramified transformations](http://stacks.math.columbia.edu/tag/04G3)_ _[57.12. Formally &#233;tale morphisms](http://stacks.math.columbia.edu/tag/04GB)_
 {#StackProject}

The  characterization via a ([[reduction modality]] $\dashv$ [[infinitesimal shape modality]]) is more or less explicit in

* [[Carlos Simpson]], [[Constantin Teleman]], _de Rham Theorem for $\infty$-stacks_ 1997 ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))
 {#SimpsonTeleman97}

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], section 4 of _Noncommutative spaces_, preprint MPI-2004-35 ([[KontsevichRosenbergNCSpaces.pdf:file]], [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 {#KontsevichRosenberg04}

The formalization as [[differential cohesion]] is discussed in 

* [[Urs Schreiber]], sections 3.5, 3.10 of _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

[[!redirects formally étale morphisms of schemes]]

[[!redirects formally etale morphism of schemes]]
[[!redirects formally etale morphisms of schemes]]