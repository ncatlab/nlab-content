
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents goes here
{:toc}

## Idea

The _string 2-group_ is a [[smooth ∞-groupoid|smooth 2-group]]-refinement of the [[topological group]] called the [[string group]].


## Definition

The [[string group]] in [[Top]] is one step in the [[Whitehead tower]] of the [[orthogonal group]].

+-- {: .un_defn}
###### Definition

For $n \in \mathbb{N}$ let $Spin(n)$ denote the [[spin group]], regarded as a [[topological group]]. Write $B Spin(n) \in $ [[Top]] for its [[classifying space]] and 

$$
  \frac{1}{2}p_1 : B Spin(n) \to B^4 \mathbb{Z}
$$

for a representative of the [[characteristic class]] called the first fractional [[Pontryagin class]]. Its [[homotopy fiber]] in the [[(∞,1)-topos]] [[Top]] $\simeq$ [[∞Grpd]] is denoted $B String(n) := B O(n)\langle 7 \rangle$

$$
  \array{
     B String(n) &\to& * 
     \\
     \downarrow && \downarrow
     \\
     B Spin(n) &\stackrel{\frac{1}{2} p_1}{\to}& B^4 \mathbb{Z}
  }
  \,.
$$

The [[loop space]] 

$$
  String(n) := \Omega B String(n)
$$

is the [[∞-group]]-object in [[Top]] called the **[[string group]]**.

=--

Write now

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc)
   :
  Smooth\infty Grpd
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\leftarrow}}}}
  \infty Grpd
    \simeq 
  Top
$$

for the [[(∞,1)-topos]] [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s, regarded as a [[cohesive (∞,1)-topos]] over [[∞Grpd]]. 

+-- {: .un_prop}
###### Proposition

There is a lift through $\Pi$ of $\frac{1}{2} p_1$ to the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth first fractional Pontryagin class</a>

$$
  \frac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin(n) \to \mathbf{B}^3 U(1)
$$

in [[Smooth∞Grpd]], where

* $\mathbf{B}Spin$ is the [[delooping]] [[Lie groupoid]] of $Spin(n)$ regarded as a [[Lie group]] (see <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#LieGroups">Smooth ∞-groupoids -- Cohesive ∞-groups -- Lie groups</a>);

* $\mathbf{B}^3 U(1)$ is the three-fold delooping of the [[circle group]], regarded as a [[Lie group]] (see <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">Smooth ∞-groupoids -- Cohesive ∞-groups -- Circle Lie n-group</a>);

* $\frac{1}{2}\mathbf{p}_1$ is the image under [[Lie integration]] of the canonical [[Lie algebra cohomology|cocycle]]
  
  $$
    \mu = \langle -,[-,-]\rangle : \mathfrak{so}(n) \to b^2 \mathbb{R}
    \,.
  $$
    
  on the [[orthogonal Lie algebra]].

=--

This is shown in ([FSS](#FSS)).


+-- {: .un_defn}
###### Definition

Write $\mathbf{B}String(n)$ for the [[homotopy fiber]] of the smooth
first fractional Pontryagin class

$$
  \array{
    \mathbf{B}String &\to& * 
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}Spin &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}&
    \mathbf{B}^3 U(1)
  }
$$

in [[Smooth∞Grpd]]. Its [[loop space object]]

$$
  String(n) := \Omega \mathbf{B}String(n)
$$

is the [[∞-Lie group|smooth ∞-group]] called [[generalized the|the]] **smooth string 2-group**.


=--

## Properties

(...)

## Presentations

Several presentations of the string Lie 2-group are known.

### As an integration of the String Lie 2-algebra 

The string Lie 2-group is the result of applying [[Lie integration]] to the [[String Lie 2-algebra]] for the case that the Lie algebra 3-cocycle this is  normalized so that its image as a left-invariant 3-form on the [[spin group]] is the image in [[deRham cohomology]] of the generator of the degree [[integral cohomology]] group $H^3(Spin(n), \mathbb{Z}) \simeq \mathbb{Z}$.

([Henriques](#Henriques)).

### As a strict Lie 2-group

A realization of the string 2-group as a [[strict 2-group]] [[internalization|internal]] to [[diffeological space]]s was given in ([BCSS](#BCSS)).


This is one of three different (there should be more), weakly equivalent such [[strict 2-group]] [[internalization|internal]] to [[diffeological space]] models that are discussed in the (to date unpublished)

* [nactwist, section 5.2.3](http://www.math.uni-hamburg.de/home/schreiber/nactwist.pdf#page=91)

(This particular section, and its results, are joint work of [[Urs Schreiber]] and [[Danny Stevenson]]).

We have the following pattern of routes through [[Lie integration]]:

$$
  \array{
    StrLie \omega Grpd
    &&&&
    StrLie \omega Grpd
    &\stackrel{\simeq}{\leftarrow}&
    LieCrsdCmplx
    \\
    \uparrow^{\Pi_n S CE}
    &&&&
    \uparrow
    &&
    \uparrow^{\exp(-)}
    \\
    L_\infty Algebras
    &&
    \leftarrow&&
    Str L_\infty Algebras
    &\to&
    DiffCrsdCmplx
  }
$$

Here $StrLie \omega Grpd$ is [[strict omega-groupoid]]s internal to [[diffeological space]]s, $LieCrsCmplx$ is accordingly smooth [[crossed complex]]es , $L_\infty Algebra$ is all [[L-infinity algebra]]s and $Str L_\infty Algebra$ is _strict_ $L_\infty$-algebras. The vertical morphism on the right is term-wise ordinary [[Lie integration]]. The other vertical morphisms take an [[L-infinity algebra]], form the [[sheaf]] on [[Diff]] of flat [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid differential form]]s, and then take [[path n-groupoid]] $\Pi_n(-)$ of that. 

For the String-case this yields

$$
  \array{
    \Pi_2(\Omega^\bullet_{fl}(-,\mathfrak{so}_{\mu_3}))
    &\stackrel{\simeq}{\mapsto}&
    \mathbf{B} String_{Mick}
    &\stackrel{\simeq}{\mapsto}&
    \mathbf{B} String_{BCSS}
    &\leftarrow|&
    (\hat \Omega Spin \to P Spin)
    \\
    \uparrow &&&\nearrow& \uparrow  && \uparrow
    \\
    \mathfrak{so}_{\mu_3}
    &&\stackrel{\simeq}{\mapsto}&&
    \mathfrak{string}
    &\mapsto&
    (\hat \Omega \mathfrak{so} \to P \mathfrak{so})    
  }
  \,,
$$

where 

* $\mathfrak{so}_{\mu_3}$ denotes the weak, skeletal [[String Lie 2-algebra]]

* $\mathfrak{string}$ its equivalent strict version given by BCSS

* the diagonal morphism is the construction in BCSS.

* the strict 2-groupoid $\Pi_2(\Omega^\bullet_{fl}(-,\mathfrak{g}_{\mu_3}))$ has, notice, as morphism smooth paths in $Spin(n)$ that are composed by concatenation

* the 2-groupoid $\mathbf{B}String_{Mick}$ is a version of the String Lie 2-group that manifestly uses the [[Mickelsson cocycle]] (morphism are paths in $Spin(n)$ that are composed using the group product) 

* the 2-groupoid $\mathbf{B}String_{BCSS}$ is the version given in BCSS (morhisms again are paths in $Spin(n)$ that are composed using the group product).


### As a finite-dimensional weak Lie 2-group 

([Schommer-Pries](#Schommer-Pries))


## Related concepts

[[fivebrane 6-group]] $\to$ **string 2-group** $\to$ [[spin group]]


## References

A [[crossed module]] presentation of a topological realization of the string 2-group is implicit in 

* [[Stephan Stolz]], [[Peter Teichner]], _What is an elliptic object?_ ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.146.5463&rep=rep1&type=pdf))
{#StolzTeichner}

A realization of the string 2-group in [[∞-groupoid]]s [[internalization|internal to]] [[Banach space]]s by [[Lie integration]] of the skeletal version of the [[string Lie 2-algebra]] is in

* [[Andre Henriques]], _Integrating $L_\infty$-algebras_ ([arXiv:math/0603563](http://arxiv.org/abs/math/0603563))
{#Henriques}

A realization of the string 2-group in [[strict 2-group]]s internal to [[Frechet manifold]]s by  [[Lie integration]] of a [[strict Lie 2-algebra]] incarnation of the [[string Lie 2-algebra]] in in

* BCSS, _From loop groups to 2-groups_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#BCSS">web</a>)
{#BCSS}

A realization of the string 2-group as a [[2-group]] in finite-dimensional [[smooth manifold]]s in in

* [[Chris Schommer-Pries]], _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ ([arXiv:0911.2483](http://arxiv.org/abs/0911.2483))
{#Schommer-Pries}

A discussion as an [[∞-group]] object in [[Smooth∞Grpd]] and the realization of the smooth first fractional Pontryagin class is in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cech cocycles for differential characteristic classes_ ([web](http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#FSS))
{#FSS}

and in section 4.1 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_


[[!redirects String 2-group]]
[[!redirects String Lie 2-group]]
[[!redirects string Lie 2-group]]