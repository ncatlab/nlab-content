
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _string 2-group_ is a [[Lie infinity-groupoid|Lie 2-group]]-refinement of the [[topological group]] called the [[string group]].

The topological string group is the [[homotopy fiber]] in [[Top]] of the first fractional [[Pontryagin class]] $\frac{1}{2}p_1 : \mathcal{B}Spin \to \mathbf{B}^4 \mathbb{Z}$. The string 2-group is the homotopy fiber in [[?LieGrpd]] of the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth first fractional Pontryagin class</a>  $\frac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)$.

### Motivation from quantum physics

Since, by definition, the topological [[string group]] has vanishing third [[homotopy group]], it cannot be a (finite dimensional) [[Lie group]] (because these all have nontrivial $\pi_3$ as soon as they are nonabelian). However, for various applications it is necessary to have a smooth model of the [[string group]]. The string 2-group provides this.

This is best understood by comparison with the situation one step down in the [[Whitehead tower]] of $O(n)$: using the [[spin group]] instead of the string group. A priori the [[spin group]] is defined as the [[topological group]] that is the [[universal cover]] of the [[special orthogonal group]]. This alone is sufficient to talk about [[spin structure]] of an [[orientation|oriented]] $n$-dimensional [[manifold]] $X$: this is a lift of the classifying map $X \to \mathcal{B} SO(n)$ -- a morphism of [[topological space]]s -- of the [[tangent bundle]] $T X $ of $X$ through the projection $\mathcal{B} Spin(n) \to \mathcal{B} SO(n)$.

And this can be said entirely within [[Top]]. In [[quantum physics]], the existence of such a lift is necessary in order for [[spin|spinning]] particles to have a consistent _kinematics_ on $X$. However, the _dynamics_ of such spinning particles is encoded by a richer structure: 

the [[spin group]] naturally has the structure not just of a [[topological group]] but of a [[Lie group]]. This means that a [[spin structure]] on $X$ may be exhibited by a _smooth_ $Spin(n)$-[[principal bundle]]. Being a smooth bundle for a [[Lie group]], there is a notion of [[connection on a bundle]]. The choice of such refines the [[nonabelian cohomology]] class given by the [[spin structure]] $X \to \mathcal{B} Spin(n)$ to a class in [[schreiber:differential nonabelian cohomology|differential nonabelian cohomology]].

Such a differential refinement of topological [[nonabelian cohomology]] is what the string 2-group admits and which the plain [[string group]] in the form of a  [[topological group]] does not admit:

The _kinematics_ of the "spinning string" called the [[heterotic string]] requires that the [[spin structure]] $X \to \mathcal{B} Spin(n)$ lifts to a [[string structure]] $X \to \mathcal{B} String(n)$, again so far just as a lift in [[Top]].

Such a lift classifies a topological [[string group]]-[[principal bundle]] on $X$. But the _dynamics_ of the string is determined by a differential refinement of this [[nonabelian cohomology]] class (aspects of this are described at [[schreiber:twisted differential String- and Fivebrane structures]]): it is given by a _smooth_ $String(n)$-[[schreiber:principal 2-bundle with connection|principal 2-bundle with connection]].

In order to make sense of this one needs an incarnation and refinement of the topological [[string group]] inside an [[(infinity,1)-topos]] of [[Lie infinity-groupoid]]s. This is what the string 2-group accomplishes.



## Definition

Let $\mathfrak{g} = \mathfrak{so}$ be the [[orthogonal Lie algebra]] and $\mu = \langle  . , [-,-]\rangle\in CE(\mathfrak{so})$ the canonical cocycle in [[Lie algebra cohomology]] corresponding to the [[Killing form]] [[invariant polynomial]], normalized such that its continuation to a left-invariant 3-form on the [[spin group]] represents the image in deRham cohomology of a generator of the [[integral cohomology]] group $H^3(Spin,\mathbb{Z}) \simeq \mathbb{Z}$.

Then by <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfCocycles">integration of Lie algebra cocycles</a> we get a morphism

$$
  \frac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)
$$

in the [[(∞,1)-topos]] [[?LieGrpd]]. 

Concretely, in terms of the [[model structure on simplicial presheaves]] over the [[site]] [[CartSp]], this is given as follows: the 3-[[coskeleton]] $\mathbf{cosk}_3 \exp(\mathfrak{g})$ of the [[simplicial presheaf]]

$$
  \exp(\mathfrak{g}) : (U,[n]) \mapsto Hom_{dgAlg}(CW(\mathfrak{g}), C^\infty(U)\otimes\Omega^\bullet(\Delta^n))
$$

is an equivalent [[resolution]] of $\mathbf{B}G := \{G \stackrel{\to}{\to} *\}$, and the cocycle $\frac{1}{2}\mathbf{p}_1$ is given by the [[anafunctor]]

$$
  \array{
    &&\mathbf{cosk}_3 \ing_{\Delta^\bullet}\exp(\mu) &\stackrel{\exp(\mu)}{\to}&
    \mathbf{B}^3 \mathbb{R}/\mathbb{Z}
    \\
    &&\downarrow^{\mathrlap{\simeq}}
    \\
    && \mathbf{B}G
  }
$$

where the top horizontal morphism sends a 3-morphism $C^\infty(U)\otimes\Omega^\bullet(\Delta) \leftarrow CE(\mathfrak{g})$ to the composite $C^\infty(U)\otimes\Omega^\bullet(\Delta) \stackrel{\leftarrow}{\leftarrow} CE(\mathfrak{g}) \leftarrow CE(b^2 \mathbb{R}) : \mu(A)$, regards that as a $U$-family of 3-forms and performs [[fiber integration]] over the 3-simplex, regarding the result modulo $\mathbb{Z}$.

+-- {: .un_defn}
###### Definition

The delooping of the string Lie 2-group is the [[homotopy fiber]] 

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

in [[?LieGrpd]].

=--


+-- {: .un_remark}
###### Remark

By the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfCocycles">theorem on geometric realization</a> $|-| : \infty LieGrpd \stackrel{\Pi}{\to} \infty Grpd \stackrel{\simeq}{\to} Top$ it follows that the geometric realizaton of $\mathbf{B}String$ is $\mathcal{B}String$, the homotopy fiber in [[Top]] of

$$
  \array{
    \mathcal{B}String &\to& * 
    \\
    \downarrow && \downarrow
    \\
    \mathcal{B}Spin &\stackrel{\frac{1}{2}{p}_1}{\to}&
    \mathcal{B}^4 \mathbb{Z}
  }
  \,.
$$


=--



## Models

There are various equivalent constructions that should eventually be described here in detail. For the time being this here is very incomplete and -- notably -- biased. But it should improve eventally.

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




## References

* [[Andre Henriques]], _Integrating $L_\infty$-algebras_ ([arXiv:math/0603563](http://arxiv.org/abs/math/0603563))
{#Henriques}

* BCSS, _From loop groups to 2-groups_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#BCSS">web</a>)
{#BCSS}

* [[Chris Schommer-Pries]], _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ ([arXiv:0911.2483](http://arxiv.org/abs/0911.2483))
{#Schommer-Pries}


[[!redirects String 2-group]]
[[!redirects String Lie 2-group]]
[[!redirects string Lie 2-group]]