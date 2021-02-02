
> This entry is about a variant of the concept of [[cohesive (∞,1)-topos]]. The definition here expresses an intuition not unrelated to that at [[infinitesimally cohesive (∞,1)-presheaf on E-∞ rings]] but the definitions are unrelated and apply in somewhat disjoint contexts.


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

A [[cohesive (∞,1)-topos]] is _infinitesimal cohesive_ if all its objects behave as though built from [[infinitesimally thickened points|infinitesimally thickened]] [[geometrically discrete ∞-groupoids]] in that they all have "precisely one point in each cohesive piece". 

(There is an evident version of an infinitesimally cohesive 1-topos. In ([Lawvere 07, def. 1](#Lawvere07)) such is referred to as a "[[quality type]]". A hint of this seems to be also in ([Lawvere 91, p. 9](#Lawvere91))).


## Definition

+-- {: .num_remark #InfinitesimalCohesion}
###### Remark

A [[cohesive (∞,1)-topos]] $\mathbf{H}$ with its [[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]] denoted $&#643; \dashv \flat \dashv \sharp$ is _infinitesimal cohesive_ if the canonical [points-to-pieces transform](cohesive+topos#CanonicalComparison) is an [[equivalence]]

$$
  \flat \stackrel{\simeq}{\longrightarrow} &#643;
  \,.
$$


=--

+-- {: .num_remark }
###### Remark

The underlying [[adjoint triple]] $\Pi \dashv Disc \dashv \Gamma$ in the case of infinitesimal cohesion is an [[ambidextrous adjunction]]. Such a [[localization of a category|localization]] is called a "quintessential localization" in ([Johnstone 96](#Johnstone96)).

=--

## Examples



Given an [[(∞,1)-site]] with a [[zero object]], then the [[(∞,1)-presheaf (∞,1)-topos]] over it is infinitesimally cohesive. This class of examples contains the following ones.

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
 {#FormalModuliProblems}

[[synthetic differential ∞-groupoids]] are cohesive over generalized [[formal moduli problems]]/[[L-∞ algebras]] (generalized meaning without the condition of vanishing on the point and of without the condition of being [[cohesive (∞,1)-presheaf on E-∞ rings|infinitesimally cohesive sheaves in Lurie's sense]]) which in turn are infinitesimally cohesive over [[geometrically discrete ∞-groupoids]].

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

See also at _[[differential cohesion and idelic structure]]_.

### Goodwillie-tangent cohesion
 {#GoodwillieTangentCohesion}

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

* [[differential cohesion and idelic structure]]

## References

The notion of infinitesimal cohesion appears under the name "quality type" in def. 1 of 

* [[William Lawvere]], _Axiomatic cohesion_, Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
 {#Lawvere07}

An earlier hint of the same notion seems to be that on the bottom of p. 9 in 

* [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ (1991)
 {#Lawvere91} 

The above examples of infinitesimal cohesion appear in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ (2013)

Localization by an [[ambidextrous adjunction]] is also discussed in 

* {#Johnstone96} [[Peter Johnstone]], _Remarks on quintessential and persistent localizations_, Theory and Applications of Categories, Vol. 2, No. 8, 1996, pp. 90&#8211;99 ([TAC](http://www.tac.mta.ca/tac/volumes/1996/n8/2-08abs.html))

[[!redirects infinitesimal cohesive (infinity,1)-toposes]]
[[!redirects infinitesimal cohesive (infinity,1)-topoi]]

[[!redirects infinitesimal cohesion]]
[[!redirects infinitesimally cohesive]]

[[!redirects infinitesimal cohesive (∞,1)-topos]]
[[!redirects infinitesimal cohesive (∞,1)-toposes]]
[[!redirects infinitesimal cohesive (∞,1)-topoi]]
