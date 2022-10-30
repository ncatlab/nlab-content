
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Content#
* table of contents
{:toc}

## Idea

In a context of [[differential cohesion]] a [[reduction modality]] exhibits an inclusion of its [[modal types]] -- the [[reduced objects]]. Essentially the corresponding inclusion of the [[anti-modal types]] is exhibited by an induced [[modal operator]], the _relative flat modality_ $\flat^{rel}$.

Where the plain [[flat modality]] $\flat$ sends any object $X$ to the type $\flat X$ of its [[global points]], the relative flat modality instead sends it to the type $\flat^{rel} X$ of all [[infinitesimal disks]] (i.e. the [[infinitesimal neighbourhoods]] of all global points) in $X$.

See also at _[[differential cohesion and idelic structure]]_.

## Definition

+-- {: .num_defn #InducedRelativeShapeAndFlat}
###### Definition

Given [[differential cohesion]], 

$$
  \array{
     \Re &\dashv& \Im &\dashv& \&
     \\
     && \vee && \vee
     \\
     && &#643; &\dashv& \flat &\dashv& \sharp
  }
$$

define operations $&#643;^{rel}$ and $\flat^{rel}$ by

$$
  &#643;^{rel} X \coloneqq (&#643; X) \underset{\Re X}{\coprod} X
$$

$$
  \flat^{rel} X \coloneqq (\flat X) \underset{\Im}{\times} X
  \,.
$$

Hence $&#643;^{rel} X$ makes a [[homotopy pushout]] square

$$
  \array{
    \Re X &\longrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    &#643; X &\longrightarrow& &#643;^{rel} X
  }
$$

and $\flat^{rel}$  makes a [[homotopy pullback]] square

$$
  \array{
    \flat^{rel} X &\longrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    \flat X &\longrightarrow& \Im X
  }
  \,.
$$

We call $&#643;^{rel}$ the _relative shape modality_ and $\flat^{rel}$ the _relative flat modality_.

=--

## Properties

+-- {: .num_prop}
###### Proposition

The relative shape and flat modalities of def. \ref{InducedRelativeShapeAndFlat}

1. form an [[adjoint pair]] $(&#643;^{rel} \dashv \flat^{rel})$;

1. whose (co-)[[modal types]] are precisely the properly infinitesimal types, hence those for which $\flat \to \Im$ is an [[equivalence]];

1. $&#643;^{rel}$ preserves the [[terminal object]].

=--

It follows that when $\flat^{rel}$ has a further [[right adjoint]] $\sharp^{rel}$ with equivalent [[modal types]] containing the [[codiscrete object|codiscrete types]], then this defines a [[level of a topos|level]]

$$
  \array{
     \flat^{rel} &\dashv& \sharp^{rel}
     \\
     \vee && \vee
     \\
     \flat &\dashv& \sharp
     \\
     \vee && \vee 
     \\
     \emptyset &\dashv& \ast
  }
$$

hence an intermediate subtopos 
$\infty Grpd \hookrightarrow \mathbf{H}_{infinitesimal}\hookrightarrow \mathbf{H}_{th}$ which is [[infinitesimal cohesion|infinitesimally cohesive]].

This happens notably for the model of [[formal smooth ∞-groupoids]] and all its variants such as formal [[complex analytic ∞-groupoids]] etc. But in this case $(\flat^{rel} \dashv \sharp^{rel})$ does not provide  [[Aufhebung]] for $(\flat \dashv \sharp)$.

(...)

+-- {: .num_prop #CounitOfFlatRelIsFormallyEtale}
###### Proposition

The [[counit of a comonad|counit]] of the relative flat modality is a [[formally étale morphism]].


=--

[[!redirects relative shape modality]]
[[!redirects relative sharp modality]]