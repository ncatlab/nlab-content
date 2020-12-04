

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



> The way I first visualized a K-group was as a group of "classes of objects" of an abelian (or more generally, additive) category, such as coherent sheaves on an algebraic variety, or vector bundles, etc. I would presumably have called this group $C(X)$ ($X$ being a variety or any other kind of "space"), $C$ the initial letter of 'class', but my past in functional analysis may have prevented this, as $C(X)$ designates also the space of continuous functions on $X$ (when $X$ is a topological space). Thus, I reverted to $K$ instead of $C$, since my mother tongue is German, Class = Klasse (in German), and the sounds corresponding to $C$ and $K$ are the same.

> ([[Alexander Grothendieck]], as quoted in [Courtney 04](topological+K-theory#Courtney04), citing: A. Bak, _Editorial_, K-theory 1 (1987), 1)



## Idea ##

Given a [[stable (∞,1)-category]] $C$, its naive [[decategorification]] (its set of objects modulo the relation of [[equivalence]]) naturally inherits the structure of an abelian [[monoid]] from the [[biproducts]] in $C$.  That is, we define $[a]+[b] = [a\oplus b]$.  We can then further pass to the [[Grothendieck group]], adding formal additive inverses to get an abelian [[group]].

Note that such a biproduct sits in a [[split exact sequence|split]] (co)[[fibration sequence]] $a\to a\oplus b \to b$.  Often we would like to obtain an analogous additivity result for *arbitrary* (co)fibration sequences (a.k.a. [[distinguished triangles]]).  This requires imposing the [[generators and relations|relation]] $[c] = [a] + [b]$ for any fibration sequence $a\to c\to b$, thereby passing to a quotient abelian group called $K_0(C)$, the **K-group** or [[Grothendieck group]] of $C$; see the latter entry for more details.

The "K" is chosen by Grothendieck for the German word _Klasse_ for "class". The K-group of $C$ is the group of equivalence classes of $C$: it is a group due to the existence of a notion of exact sequences in $C$.

K-theory starts with the study of these K-groups and their higher analogues $K_n(C)$, collectively denoted $K(C)$. Sometimes the K-groups themselves are called "K-theory". One would say for instance: "$K(C)$ is the K-theory of $C$."

More generally, there is a [[symmetric monoidal (infinity,1)-category|symmetric groupal ∞-groupoid]] $\mathbf{K}(C)$  -- i.e. a connective [[spectrum]] -- in between the [[decategorification]] from $C$ to $K(C)$, for which $K_0(C)$ is the set of [[simplicial homotopy group|connected components]]

$$
  C \mapsto \mathbf{K}(C) \to \pi_0 \mathbf{K}(C) = K_0(C)
  \,.
$$

and more generally $K_n(C) = \pi_n \mathbf{K}(C)$.

In nice cases this is the degree 0 part of a non-connective [[spectrum]] which is then the **K-theory spectrum** of $C$.
This is also called the **Waldhausen K-theory** of $C$.



## Special cases and models ##

Much of the literature on K-theory discusses constructions that _model_ the above abstract setup in terms of [[model category|model categories]], or just their [[homotopy category|homotopy categories]], often of the [[derived category|derived catgeories]] type and then often expressed in terms of the [[abelian category]] or more generally [[Quillen exact category]] from which the derived category is derived.

Only a subset of the structure on a [[model category]] is necessary in order to conveniently extract the K-groups of the [[presentable (infinity,1)-category|presented]] [[stable (∞,1)-category]]. For that reason the axioms of a [[Waldhausen category]] have been devised to provide just the necessary convenient prerequisites to compute the K-groups of the [[(∞,1)-category]] [[presentable (infinity,1)-category|presented]] by the underlying [[homotopical category]].

* In particular, the K-group associated to the [[stable (∞,1)-category]] $Ch^b(A)$ of _bounded_ [[chain complex]]es in an [[abelian category]] or [[exact category]] $A$ is often called the K-group of $A$ itself and just denoted

  $$
    K(A) := K(Ch^b(A))
    \,.
  $$

  Most explicit constructions of K-theory spectra start with the data of an [[exact category]], such as notably Quillen's [[Q-construction]] and the [[Waldhausen S-construction]].

* In particular if the exact category $A$ is that of [[vector bundle]]s on a [[topological space]] $X$

  $$
    A = VectBund(X)
  $$

  the corresponding K-group is degree 0 [[topological K-theory]]. This was the original of the notion and the term K-theory.

## Definition ##

Recall that given a [[(∞,1)-category]] $C$, we may regard it as a [[complete Segal space]] $C_{\bullet,\bullet}$, a [[bisimplicial object|bisimplicial set]]. For instance if $C$ is originally given as a [[quasicategory]] then

$$
  C_{\bullet,\bullet} : [n],[m] \mapsto
  Core(Func(\Delta^n,C))_{m}
  \,,
$$

where $Core(Func(\Delta^n,C))$ denotes the maximal [[Kan complex]] inside the [[(∞,1)-category of (∞,1)-functors]] from $\Delta^n$ to $C$.

+-- {: .num_defn #Gap}
###### Definition 

For $\mathcal{C}$ an [[(∞,1)-category]] and $n \in \mathbb{N}$, write $Gap(\Delta^n, \mathcal{C})$ for the full sub-$\infty$-category on $Func(Arr(\Delta^n),\mathcal{C} )$ on those objects $F$ for which

* the [[diagonal]] $F(n,n)$ is inhabited by [[zero objects]], for all $n$;

* all [[diagrams]] of the form

  $$
    \array{
      F(i,j) &\to& F(i,k)
      \\
      \downarrow && \downarrow
      \\
      F(j,j) &\to& F(j,k)
    }
  $$

  is an [[(∞,1)-pushout]].

=--

+-- {: .num_defn}
###### Definition 

Let $C$ be a [[stable (∞,1)-category]]. Then its **Waldhausen K-theory** 

$$
  \mathbf{K}(C) := \underset{\rightarrow}{\lim}_n Core(Gap(C^{\Delta^n}))
$$

is the [[geometric realization of simplicial topological spaces|geometric realization]] of/[[homotopy colimit]] of the degreewise [[core]] of the  $Gap$, def. \ref{Gap},  of the corresponding [[complete Segal space]] (as a simplicial diagram of $\infty$-groupoids).

=--

This is [remark 11.4](http://arxiv.org/PS_cache/math/pdf/0608/0608228v5.pdf#page=43) in [[stable (infinity,1)-category|StCat]]. See also [Blumberg-Gepner-Tabuada, section 7](#BGT).

This construction is also conjectured in the last section of Toen-Vezzosi's _A remark on K-theory_ .

+-- {: .num_remark}
###### Remark

In the case that $C$ is the [[simplicial localization]] of a [[Waldhausen category]] $\bar C$ the explicit way to obtain this is the [[Waldhausen S-construction]].

=--

+-- {: .num_remark}
###### Remark

It should be true that with this definition we have an isomorphism of groups

$$
  K(C) \simeq \pi_0 \mathbf{K}(C)
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

This Waldhausen/hocolim-construction gives the _connective_ K-theory, taking values in [[connective spectra]]. The [[universal construction|universal]] completion to functor that sends [[homotopy cofibers]] of [[stable (infinity,1)-categories]] to homotopy cofibers of spectra is the corresponding unconnective $\mathbb{K}$-functor.

=--

There is a universal characterization of the construction of the $\mathbb{K}$-theory spectrum of a stable $(\infty,1)$-category $A$:

there is an $(\infty,1)$-functor

$$
  U : (\infty,1)StabCat \to N
$$

to a stable $(\infty,1)$-category which is universal with the property that it respects colimits and exact sequences in a suitable way. Given any stable $(\infty,1)$-category $A$, its (connective or non-connective, depending on details) algebraic K-theory spectrum is the hom-object

$$
  K(A) \simeq Hom(U(Sp), U(A))
  \,,
$$

where $Sp$ denotes the stable $(\infty,1)$-category of compact [[spectra]]. ([BGT](#BGT))


## Related entries ##
 
* [[Grothendieck group]]

* [[K-theory spectrum]]

* [[topological K-theory]]

  * [[fiber integration in K-theory]]

* [[Tate K-theory]]

* [[K-orientation]]

* [[algebraic K-theory]]

  * [[K-theory of a permutative category]]

  * [[K-theory of a bipermutative category]]

  * [[differential algebraic K-theory]]

  * [[noncommutative motive]]

* [[Waldhausen K-theory of a dg-category]]

* [[groupoid K-theory]]

* [[operator K-theory]]

  * [[equivariant operator K-theory]]

  * [[KK-theory]]

  * [[E-theory]]

* [[equivariant K-theory]]

* [[Karoubi K-theory]]

* [[Morava K-theory]]

* [[L-theory]]


* [[twisted K-theory]]

* [[differential K-theory]]

* [[K-theory and physics]]


## References ##

It was in 

* [[Bertrand Toen]], Gabriele Vezzosi, _A remark on K-theory and $S$-categories_ ([arXiv](http://arxiv.org/PS_cache/math/pdf/0210/0210125v2.pdf)).

that it was proven that the the [[Waldhausen S-construction]] of the [[K-theory spectrum]] depends precisely on the [[simplicial localization]] of the [[Waldhausen category]], i.e. of the [[(∞,1)-category]] that it presents.

In view of this remark 11.4 in

* [[Jacob Lurie]], [[stable (infinity,1)-category|Stable ∞-Categories]] .

interprets the construction of the K-theory spectrum as a natural operation of 
[[stable (infinity,1)-category|stable (∞,1)-categories]], as described above.

The universal property of the $(\infty,1)$-categorical definition is studied in 

* {#BGT} [[Andrew Blumberg]], [[David Gepner]], [[Goncalo Tabuada]], _A universal characterization of higher algebraic K-theory_ ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282)).
 




The standard constructions of K-theory spectra from [[Quillen exact categories]] are discussed in detail in chapter 1 of

* [[Eric Friedlander]], [[Daniel Grayson]], _Handbook of K-theory_, Springer Verlag .

A useful introduction to the definition and computation of K-groups (with a little on K-spectra) is

* Charles Weibel, _The K-book: An introduction to algebraic K-theory_ ([web](http://www.math.rutgers.edu/~weibel/Kbook.html))

[[!redirects Waldhausen K-theory]]
