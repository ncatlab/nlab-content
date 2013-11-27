
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


### Characterization by reduction/infinitesimal shape
 {#CharacterizationByReductionModality}


+-- {: .num_defn #ReductionOnRings}
###### Definition

Write $CRing_{fin}$ for the [[category]] of [[finitely generated ring|finitely generated]] [[commutative rings]] and write $CRing_{fin}^{ext}$ for the category of [[infinitesimal ring extensions]].
Write

$$
  Red \;\colon\; CRing_{fin}^{ext} \longrightarrow CRing_{fin}
$$

for the [[functor]] which sends an [[infinitesimal ring extension]] to the underlying [[commutative ring]] (in the maximal case this sends a commutative ring to its [[reduced ring]], whence the name of the functor), and write

$$
  i \;\colon\; CRing_{fin} \hookrightarrow CRing_{fin}^{ext}
$$

for the [[full subcategory]] inclusion that regards a ring as the trivial infinitesimal extension over itself.

=--

+-- {: .num_prop #DifferentialCohesionModality}
###### Proposition

There is an [[adjoint triple]] of [[idempotent monad|idempotent]] [[comonad|co]]-[[monads]]

$$
  (Red \dashv \int_{inf} \dashv \flat_{inf}) \;\colon\; PSh((CRing_{fin}^{ext})^{op}) \longrightarrow PSh((CRing_{fin}^{ext})^{op})
$$

where the [[left adjoint]] [[comonad]] $Red$ is given on [[representable functor|representables]] by the [[reduced scheme|reduction]] functor of def. \ref{ReductionOnRings} (followed by the inclusion).

=--

This statement and the following prop. \ref{FormalEtalenessBydeRhamSpace} is a slight paraphrase of an observation due to ([Kontsevich-Rosenberg 04](Q-category#KontsevichRosenbergSpaces)).

+-- {: .proof}
###### Proof

The  functors from def. \ref{ReductionOnRings} form an 
[[adjoint pair]] $(Red \dashv i)$ because an extension element
can only map to an extension element; so for $\widehat R \to R$
an [[infinitesimal ring extension]] of $R = Red(\widehat R)$, 
and for $S$ a commutative ring with
$i(S) = (S \to S)$ its trivial extension, there is a [[natural isomorphism]]

$$
  Hom_{CRing_{fin}^{ext}}(\widehat R, i(S))
  \simeq
  Hom_{CRing_{fin}}(R,S)
  \,.
$$

This exhibits $CRing_{fin}$ as a [[reflective subcategory]]
of $CRing_{fin}^{ext}$.

$$
  (Red \dashv i)
   \;\colon\;
  CRing_{fin}
   \stackrel{\overset{Red}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  CRing_{fin}^{ext}
  \,.
$$

Via [[Kan extension]] this [[adjoint pair]] induces an [[adjoint quadruple]] of [[functors]] on [[categories of presheaves]]

$$
  PSh(CRing_{fin}^{op})
    \stackrel{\overset{i_!}{\hookrightarrow}}{\stackrel{\overset{i^\ast = Red_!}{\leftarrow}}{\stackrel{\overset{Red^\ast}{\hookrightarrow}}{\underset{Red_\ast}{\leftarrow}}}}
  PSh((CRing_{fin}^{ext})^{op})
  \,.
$$

The [[adjoint triple]] to be shown is obtained from composing these adjoints pairwise.

That $Red$ coincides with the reduction functor on representables is a standard property of [[left Kan extension]] (see [here](Kan+extension#LeftKanOnRepresentables) for details).

=--


+-- {: .num_remark }
###### Remark

These considerations make sense in the general abstract context of 
"[[differential cohesion]]" where the [[adjoint triple]] of prop. \ref{DifferentialCohesionModality} would be called:

([[reduction modality]] $\dashv$ [[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]]).

=--

Due to the [[full subcategory]] inclusion $i_!$ in the proof of prop. \ref{DifferentialCohesionModality} we may equivalently regard presheaves on $(CRing_{fin})^{op}$ (e.g. [[schemes]]) as presheaves on $(CRing_{fin}^{ext})^{op}$ (e.g. [[formal schemes]]). This is what we do implicitly in the following.

+-- {: .num_prop #FormalEtalenessBydeRhamSpace}
###### Proposition

A morphism $f \;\colon\; Spec A \to Spec R$ in $CRing_{fin}^{op} \hookrightarrow PSh(CRing_{fin}^{op})$ is 
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

Evaluated on $I \hookrightarrow R  \to R/I \in CRing_{fin}^{ext}$ any object, by the [[Yoneda lemma]] and the $(Red \dashv \int_{inf})$-[[adjunction]] the naturality square becomes

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

The basic stability property of [[étale morphisms]], which we need in the following, immediately follows from this characterization:

+-- {: .num_prop #ClosureForFormallyEtale}
###### Proposition

For $\stackrel{f}{\to} \stackrel{g}{\to}$ two composable morphisms, then

1. if $f$ and $g$ are both (formally) &#233;tale, then so is their composite $g \circ f$;

1. if $g$ and $ g\circ f$ are (formally) &#233;tale, then so is $f$;

1. the [[pullback]] of a (formally) &#233;tale morphism along any morphism is again (formally) &#233;tale.

=--

+-- {: .proof}
###### Proof

With prop. \ref{FormalEtalenessBydeRhamSpace} this is equivalently the 
statement of the [[pasting law]] for [[pullback]] diagrams.

=--



## Properties


### Relation to &#233;tale morphism

Formally &#233;tale morphisms of schemes which are in addition [[locally of finite presentation]] are equivalently [[étale morphisms of schemes]].

Relaxing this finiteness condition yields the notion of [[weakly étale morphisms]].

[[étale morphism of schemes|étale morphism]] $\Rightarrow$ [[pro-étale morphism of schemes|pro-étale morphism]] $\Rightarrow$ [[weakly étale morphism of schemes|weakly étale morphism]] $\Rightarrow$ [[formally étale morphism of schemes|formally étale morphism]]

## Related concepts

* [[formally unramified morphism]], [[formally smooth morphisms]]

* [[basics of étale cohomology]]

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