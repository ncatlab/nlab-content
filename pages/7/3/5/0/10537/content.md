
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[cohesive (∞,1)-topos]] is _infinitesimal cohesive_ if all its objects behave like built from [[infinitesimally thickened points|infinitesimally thickened]] [[geometrically discrete ∞-groupoids]] in that they all have "precisely one point in each cohesive neighbourhood". By the discussion at _[[cohesive topos]]_ ([here](cohesive%20topos#FurtherAxioms)) the formal version of this statement  is that the [[shape modality]] $&#643;$ (which sends a [[cohesive homotopy type]] to its "pieces") and the [[flat modality]] $\flat$ (which sends a [[cohesive homotopy type]] to its "points") are [[natural equivalence|naturally equivalent]], which implies that in particular the canonical [[natural transformation]] $\flat \longrightarrow &#643;$ is an [[equivalence]].

(There is an evident version of an infinitesimally cohesive 1-topos. In ([Lawvere 07, def. 1](#Lawvere07)) such is referred to as a "quality type".)


## Definition

A [[cohesive (∞,1)-topos]] $\mathbf{H}$ with its [[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]] denoted $(\Pi \dashv \flat \dashv \sharp))$
is _infinitesimal cohesive_ if

$$
  \Pi \simeq \flat \simeq \sharp
  \,.
$$

Equivalently this means that the [[left adjoint]] to the [[inverse image]] inclusion of the [[base (∞,1)-topos]] is equivalent to the [[global section]] [[direct image]]. 


## Properties

(...)



## Examples

### Super $\infty$-groupoids

[[super ∞-groupoids]] are infinitesimally cohesive over [[geometrically discrete ∞-groupoids]], while [[smooth super ∞-groupoids]] are cohesive over [[super ∞-groupoids]] and [[differential cohesion|differentially cohesive]] over [[smooth ∞-groupoids]]

$$
  \array{
    cohesion &&
    SmoothSuper\infty Grpds 
    &\stackrel{\overset{\Pi^s}{\longrightarrow}}{\stackrel{\overset{Disc^s}{\leftrightarrow}}{\stackrel{\overset{\Gamma^s}{\longrightarrow}}{\underset{coDisc^s}{\leftarrow}}}}&
   Super \infty Grpds
    \\
    &&{}^{\mathllap{Disc_{inf}}}\uparrow \downarrow^{\mathrlap{\Pi_{inf}}}
    && 
    {}^{\mathllap{Disc_{inf}}}\uparrow \downarrow^{\mathrlap{\Pi_{inf}}}
    \\
    cohesion && 
    Smooth \infty Grpds
    &\stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftrightarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}&
    \infty Grpds
    \\
    \\
    && diff.\;cohesion && inf.\;cohesion
  }
$$

### Formal moduli problems/ strong homotopy Lie algebras

[[synthetic differential ∞-groupoids]] are cohesive over
[[formal moduli problems]]/[[L-∞ algebras]] which in turn are infinitesimally cohesive over [[geometrically discrete ∞-groupoids]].

$$
  \array{
    cohesion
    &&
    SynthDiff\infty Grpds 
    &\stackrel{\overset{\Pi^i}{\longrightarrow}}{\stackrel{\overset{Disc^i}{\leftrightarrow}}{\stackrel{\overset{\Gamma^i}{\longrightarrow}}{\underset{coDisc^i}{\leftarrow}}}}&
   L_\infty Alg^{op}_{gen}
    \\
    &&{}^{\mathllap{Disc_{inf}}}\uparrow \downarrow^{\mathrlap{\Pi_{inf}}}
    && 
    {}^{\mathllap{Disc_{inf}}}\uparrow \downarrow^{\mathrlap{\Pi_{inf}}}
    \\
    cohesion && Smooth \infty Grpds
    &\stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftrightarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}&
    \infty Grpds
    \\
     && diff.\;cohesion && inf.\;cohesion
  }
$$


### Goodwillie-tangent cohesion

A [[tangent (∞,1)-topos]] $T \mathbf{H}$ is infinitesimally cohesive over $\mathbf{H}$:

$$
  \array{
    && Stab(\mathbf{H})
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
    &
    Stab(\infty Grpd) \simeq Spectra
    \\
    && \simeq && \simeq
    \\
    && T_\ast \mathbf{H} && T_\ast \infty Grpd
    \\
    && \downarrow^{\mathrlap{incl}} && \downarrow^{\mathrlap{incl}}
    \\
    \mathbf{H}
    &\stackrel{\overset{d}{\longrightarrow}}{\underset{\Omega^\infty \circ tot}{\leftarrow}}&
    T \mathbf{H}
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
  &
  T \infty Grpd
  \\
  &&
  {}^{\mathllap{base}}\downarrow \uparrow^{\mathrlap{0}} 
  && 
  {}^{\mathllap{base}}\downarrow \uparrow^{\mathrlap{0}} 
  \\
  &&
    \mathbf{H}
    &
    \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  &
  \infty Grpd
  }
  \,.
$$


## Related concepts

* [[differential cohesion]]

## References

The notion of infinitesimal cohesion appears under the name "quality type" in def. 1 of 

* [[Bill Lawvere]], _Axiomatic cohesion_, Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
 {#Lawvere07}

The above examples of infinitesimal cohesion appear in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ (2013)


[[!redirects infinitesimal cohesion]]
[[!redirects infinitesimally cohesive]]
[[!redirects infinitesimal cohesive (∞,1)-topos]]