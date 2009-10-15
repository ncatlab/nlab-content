

#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The _string 2-group_ is a _smooth_ [[2-group]] incarnation of the [[topological group]] called the [[string group]].

## motivation from quantum physics ##

Since, by definition, the topological [[string group]] has vanishing third [[homotopy group]], it cannot be a (finite dimensional) [[Lie group]] (because these all have $\pi_3 = \mathbb{Z}$). However, for various applications it is necessary to have a smooth model of the [[string group]]. The string 2-group provides this.

This is best understood by comparison with the situation one step down in the [[Whitehead tower]] of $O(n)$: using the [[spin group]] instead of the string group. A priori the [[spin group]] is defined as the [[topological group]] that is the [[universal cover]] of the [[special orthogonal group]]. This alone is sufficient to talk about [[spin structure]] of an [[orientation|oriented]] $n$-dimensional [[manifold]] $X$: this is a lift of the classifying map $X \to \mathcal{B} SO(n)$ -- a morphism of [[topological space]]s -- of the [[tangent bundle]] $T X $ of $X$ through the projection $\mathcal{B} Spin(n) \to \mathcal{B} SO(n)$.

And this can be said entirely within [[Top]]. In [[quantum physics]], the existence of such a lift is necessary in order for [[spinning particle]]s to have a consistent _kinematics_ on $X$. However, the _dynamics_ of such spinning particles is encoded by a richer structure: 

the [[spin group]] naturally has the structure not just of a [[topological group]] but of a [[Lie group]]. This means that a [[spin structure]] on $X$ may be exhibited by a _smooth_ $Spin(n)$-[[principal bundle]]. Being a smooth bundle for a [[Lie group]], there is a notion of [[connection on a bundle]]. The choice of such refines the [[nonabelian cohomology]] class given by the [[spin structure]] $X \to \mathcal{B} Spin(n)$ to a class in [[schreiber:differential nonabelian cohomology|differential nonabelian cohomology]].

Such a differential refinement of topological [[nonabelian cohomology]] is what the string 2-group admits and which the plain [[string group]] in the form of a  [[topological group]] does not admit:

The _kinematics_ of the "spinning string" called the [[heterotic string]] requires that the [[spin structure]] $X \to \mathcal{B} Spin(n)$ lifts to a [[string structure]] $X \to \mathcal{B} String(n)$, again so far just as a lift in [[Top]].

Such a lift classifies a topological [[string group]]-[[principal bundle]] on $X$. But the _dynamics_ of the string is determined by a differential refinement of this [[nonabelian cohomology]] class (aspects of this are described at [[schreiber:twisted differential String- and Fivebrane structures]]): it is given by a _smooth_ $String(n)$-[[schreiber:principal 2-bundle with connection|principal 2-bundle with connection]].

In order to make sense of this one needs an incarnation and refinement of the topological [[string group]] inside an [[(infinity,1)-topos]] of [[Lie infinity-groupoid]]s. This is what the string 2-group accomplishes.
 
## as an integration of the String Lie 2-algebra ##

The string Lie 2-group is the result of applying [[Lie integration]] to the [[String Lie 2-algebra]] for the case that the Lie algebra 3-cocycle this is defined by is normalized such that its image as a left-invariant 3-form on the [[spin group]] is the image in [[deRham cohomology]] of the generator of the degree [[integral cohomology]] group $H^3(Spin(n), \mathbb{Z}) \simeq \mathbb{Z}$.

...

## in terms of Whitehead towers in a smooth $(\infty,1)$-topos ##

+-- {: .query}

[[Urs Schreiber]]: the following should be the right general-nonsense point of view, but strictly speaking I haven't fully provided complete proof of this perspective, just evidence. See the technical discussion further below.

=--

Just as the [[topological group|topological]] [[string group]] is the element above the  [[spin group]] in the [[Whitehead tower]] of $O(n)$ inside the [[(∞,1)-topos]] [[Top]] -- in terms of [[delooping]]s

$$
 (
  \cdots
  \to
  \mathcal{B} String(n)
  \to 
  \mathcal{B} Spin(n)
  \to \mathcal{B}SO(n) \to \mathcal{B}O(n)
  )
  \in Top
  \,,
$$

so the **string 2-group** is the [[Whitehead tower]] element above $Spin(n)$, but now regarded in an [[(∞,1)-topos]] $\mathbf{H}$ of smooth [[∞-groupoid]]s. In terms of [[delooping]]s:

$$
 (
  \cdots
  \to
  \mathbf{B} String(n)
  \to 
  \mathbf{B} Spin(n)
  \to 
  \mathbf{B}SO(n) 
  \to 
  \mathbf{B}O(n)
  )
  \in \mathbf{H}
  \,.
$$


It is in $\mathbf{H}$ the [[homotopy fiber]] of the morphism

$$
  \frac{1}{2}p_1
  :
  \mathbf{B} Spin(n)
  \stackrel{}{\to}
  \mathbf{B}^3 U(1)
$$

that is the smooth [[group cohomology|group cocycle]] that integrates the normalized canonical [[Lie algebra cohomology|Lie algebra 3-cocycle]] $\mu_3 \in CE(\mathfrak{so}(n))$.

**Remark.** Notice that in the existing literature the smooth [[group cohomology|group cocycles]] of a [[Lie group]] are _defined_ to be simplicial morphisms out of 

$$
  (\cdots  G\times G\stackrel{\stackrel{\to}{\to}}{\to}G\stackrel{\to}{\to}{*})
  \,.
$$

With that definition, $\frac{1}{2}p_1$ does _not exist_ as a smooth cocycle. But, while that definition is copied verbatim from the correct definition in [[Top]], it is **not the right general definition** for smooth [[group cohomology]]. Instead, the right definition is given by  the [[category theory|general nonsense]] of [[cohomology]] in an [[(infinity,1)-topos]] $\mathbf{H}$:
 a smooth [[group cohomology|group cocycle]] on the [[Lie group]] $G$ is a morphism out of its [[delooping]] but regarded in $\mathbf{H}$. This $\mathbf{H}$ in turn is [[models for infinity-stack (infinity,1)-toposes|modeled]] by [[simplicial presheaves]] which for the present purposes we may assume to be [[simplicial object|simplicial]] [[diffeological space]]s. But in that context there are considerably "bigger" resolutions of $\mathbf{B}G$ than the one above. (In fact the one above is just $\mathbf{B}G$ in $\mathbf{H}$ itself). The 3-cocycle $\frac{1}{2}p_1$ is a morphism out of one of these bigger resolutions. More on that below.

...

So the string 2-group is a smooth [[2-group]] incarnation of...

# Constructions #

There are various equivalent constructions that should eventually be described here in detail. For the time being this here is very incomplete and -- notably -- biased. But it should improve eventally.

## as a weak Lie 2-group ##

... Henriques...

## as a strict Lie 2-group ##

A realization of the string 2-group as a [[strict 2-group]] [[internalization|internal]] to [[diffeological space]]s was given in 

* Baez, Crans, Schreiber, Stevenson, ([arXiv]())

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


## as a finite-dimensional weak Lie 2-group ##

...Schommer-Pries ...


## by co-killing of homotopy groups in the smooth $(\infty,1)$-topos ##

...The smooth version of $\frac{1}{2}p_1 : \mathbf{B}Spin(n) \to \mathbf{B}^3 R//Z$ is constructed as follows.

Use the [[models for infinity-stack (infinity,1)-toposes|model]] given by the [[model structure on simplicial presheaves]] on [[Diff]] or similar. All [[simplicial presheaf|simplicial presheaves]] appearing are actually simplicial [[concrete sheaf|concrete sheaves]] hence simplicial [[diffeological space]]s.

The cocycle is a span in this context out of an acyclic fibration over $\mathbf{B}Spin(n)$ (an [[anafunctor]])

$$
  \array{
    \mathbf{B}Q
    &\stackrel{f}{\to}&
    \mathbf{B}^3 R/Z
    \\
    \downarrow^{\simeq}
    \\
    \mathbf{B}Spin(n)
  }
  \,.
$$

The resolution $\mathbf{B}Q$ may be chosen as follows: 1-cells are smooth paths in $Spin(n)$ starting at the neutral element, 2-cells smooth 2-[[simplex]]es in $Spin(n)$, 3-cells homotopy classes of smooth 3-[[simplex]]es. All other cells are degenerate. The projection to $\mathbf{B}Spin(n)$ takes paths to their endpoint. Because $\pi_2(Spin(n)) = 0$ this is indeed a weak equivalence.

Then let $\mu_3 \in \Omega^3(Spin(n))$ be the above-mentioned de-Rham representative of the generator of $H^3(Spin(n), \mathbb{Z}) \simeq \mathbb{Z}$.  The morphism $f$ in the above reads in 3-simplices $[\phi : \Delta^3_{Diff} \to Spin(n)]$ and sends them to

$$
  \int_{\Delta^3_{Diff}} \phi^* \mu_3
  \;\;
  \in R/Z
  \,.
$$

This is well defined because $\mu_3$ has integral periods. 

That defines the smooth version of the cocycle. Notice how $Q$ is a considerably "bigger" resolution of $Spin(n)$ than the familiar bar resolution, which doesn't work here in the smooth case, as mentioned above.

Then using this the smooth string 2-group is defined abstractly as the [[homotopy fiber]]

$$ 
  \array{
     \mathbf{B} String &\to&  {*}
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}Q &\stackrel{f}{\to}& \mathbf{B}^3 R/Z
     \\
     \downarrow^{\simeq}
     \\
     \mathbf{B}Spin(n)
  }
  \,.
$$

Of course actually constructing this [[homotopy pullback]] (which is defined only up to weak equivalence of course) amounts to constructing one of the above models, or similar.

#References#

* Henriques

* BCSS

* Schommer-Pries

* ...

[[!redirects String 2-group]]
[[!redirects String Lie 2-group]]
[[!redirects string Lie 2-group]]