
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An $(n,1)$-topos is the [[(n,r)-category|(n,1)-category]] version of a [[topos]]: a collection of [[n-groupoid|(n-1)-groupoid]]-valued sheaves on an $(n,1)$-categorical site.

Notice that an [[∞-stack]] on an ordinary (1-categorical) [[site]] that takes values in [[∞-groupoid]]s which happen to by 0-[[truncated]], i.e. which happen to take values just in [[Set]] $\hookrightarrow$ [[∞Grpd]] is the same as an ordinary [[sheaf]] of sets.

This generalizes: every $(n,1)$-topos arises as the full [[sub-quasi-category|(∞,1)-subcategory]] on $(n-1)$-[[truncated]] objects in an [[(∞,1)-topos]] of $\infty$-stacks on an [[(n,1)-category]] site.



## Definition

Recall that

* a 1-[[Grothendieck topos]] is precisely a [[accessible functor|accessible]] [[geometric embedding]] into a [[category of presheaves]] $PSh(C)$ on some [[small category]] $C$

  $$
    Sh(C) \stackrel{\overset{lex}{\leftarrow}}{\hookrightarrow} PSh(C)
    \,.
  $$

* a [[(∞,1)-topos]] (of [[∞-stack]]s/[[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]]) is precisely a [[accessible (∞,1)-functor|accessible]] [[reflective (∞,1)-subcategory|geometric embedding]] into a [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$ on some small [[(∞,1)-category]] $C$:

  $$
    Sh_{(\infty,1)}(C)
    \stackrel{\overset{lex}{\leftarrow}}{\hookrightarrow}
    PSh_{(\infty,1)}(C)
    \,.
  $$

Accordingly now, 


+-- {: .un_defn}
###### Definition

An **$(n,1)$-topos** $\mathcal{X}$ is an accessible left exact [[localization of an (∞,1)-category|localization]] of the full [[sub-quasi-category|(∞,1)-subcategory]] $PSh_{\leq n-1}(C) \subset PSh_{(\infty,1)}(C)$ on $(n-1)$-[[truncated]] objects in an [[(∞,1)-category of (∞,1)-presheaves]] on a small [[(∞,1)-category]] $C$:

$$
  \mathcal{X}
   \stackrel{\overset{lex}{\leftarrow}}{\hookrightarrow}
   PSh_{\leq n-1}(C)
   \,.
$$

=--

This appears as [[Higher Topos Theory|HTT, def. 6.4.1.1]].

## Properties

For $\mathcal{T}_1$, $\mathcal{T}_2$ $(n,1)$-toposes for some $n$, write  

$$
  Func^{geom}(\mathcal{T}_1, \mathcal{T}_2)
  \subset 
  Func(\mathcal{T}_1, \mathcal{T}_2)
$$

for the full [[sub-quasi-category|sub (∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] on [[geometric morphism]]s.

Write $Topos_{(n,1)}$ for the $(\infty,1)$-category of $(n,1)$-toposes and geometric morphisms between them.

Recall that an $(n,1)$-topos $\mathcal{X}$ is [[n-localic (∞,1)-topos|m-localic]] for $m \leq n$ if for everey $(n,1)$-topos $\mathcal{Y}$ the restriction to the $(m-1)$-[[truncated|truncations]]

$$
  Func^{geom}(\mathcal{Y}, \mathcal{X})
  \to
  Func^{geom}(\tau_{m -1}\mathcal{Y}, \tau_{m-1}\mathcal{X})  
$$

is an [[equivalence of quasi-categories|equivalence of (∞,1)-categories]]. 

([[Higher Topos Theory|HTT, def. 6.4.5.8]]).

This is in particular the case for $\mathcal{X} = Sh_{(n,1)}(C)$ with $C$ a small [[(n,1)-category]] with finite limits.


+-- {: .un_prop}
###### Proposition

For any $0 \leq m \leq n \leq \infty$, $(m-1)$-truncation induces a [[localization of an (∞,1)-category|localization]]

$$
  Topos_{(m,1)} \stackrel{\overset{\tau_{m-1}}{\leftarrow}}{\hookrightarrow}
  Topos_{n,1}
$$

that identifies $Topos_{(m,1)}$ equivalently with the full subcategory of $m$-localic $(n,1)$-toposes.

=--

(This is [[Higher Topos Theory|6.4.5.7]] in view of the following remarks.)






## Examples

### $(2,1)$-Toposes

If $E$ is a (2,1)-topos in which every object is *covered* by a 0-[[truncated]] object, then $E$ is equivalent to the category of (2,1)-sheaves on a 1-site (rather than merely a (2,1)-site, as is the case for general (2,1)-topoi), and is thus canonically *associated* to a 1-topos, namely the category of 1-sheaves on that same 1-site.  And in fact, $E$ can be recovered from this 1-topos as the category of (2,1)-sheaves for its canonical topology.  

See [[michaelshulman:truncated 2-topos]] for more.



## References

Section 6.4 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

