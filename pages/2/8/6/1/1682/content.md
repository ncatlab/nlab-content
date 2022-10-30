
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[generalized (Eilenberg-Steenrod) cohomology]] theory/[[spectrum]] called $tmf$ -- for _[[topological modular forms]]_ -- is in a precise sense the union of all [[elliptic cohomology theories]]/[[elliptic spectra]] ([Hopkins 94](#Hopkins94)). 

More precisely, $tmf$  is the [[homotopy limit]] in [[E-∞ rings]] of the [[elliptic spectra]] of all [[elliptic cohomology]] theories, parameterized over the [[moduli stack of elliptic curves]] $\mathcal{M}_{ell}$. That such a parameterization exists, coherently, in the first place is due to the [[Goerss-Hopkins-Miller theorem]]. In the language of [[derived algebraic geometry]] this refines the [[commutative ring]]-valued [[structure sheaf]] $\mathcal{O}$ of the [[moduli stack of elliptic curves]] to an [[E-∞ ring]]-valued sheaf $\mathcal{O}^{top}$, making $(\mathcal{M}_{ell}, \mathcal{O}^{top})$ a [[spectral Deligne-Mumford stack]], and $tmf$ is the [[E-∞ ring]] of [[global sections]] of that structure sheaf ([[A Survey of Elliptic Cohomology|Lurie]]).

The construction of $tmf$ has motivation from [[physics]] ([[string theory]]) and from [[chromatic homotopy theory]]: 

1. **from [[string theory]].** Associating to a [[space]], roughly, the [[partition function]] of the [[spinning string]]/[[superstring]] [[sigma-model]] with that space as [[target space|target]] [[spacetime]] defines a [[genus]] known as the _[[Witten genus]]_, with [[coefficients]] in ordinary [[modular forms]]. Now, the interesting genera typically appear as the values on [[homotopy groups]] (the [[decategorification]]) of [[orientation in generalized cohomology|orientations]] of [[multiplicative cohomology theories]]; for instance the [[A-hat genus]], which is the [[partition function]] of the [[spinning particle]]/[[superparticle]] is a shadow of the [[Atiyah-Bott-Shapiro orientation|Atiyah-Bott-Shapiro]] [[Spin structure]]-orientation of the [[KO]] spectrum. Therefore an obvious question is which spectrum lifts this classical statement from point [[particles]] to [[strings]]. The spectrum $tmf$ solves this: there is a [[String structure]] [[string orientation of tmf|orientation of tmf]] such that on homotopy groups it reduces to the [[Witten genus]] of the [[superstring]] ([Ando-Hopkins-Rezk 10](#AndoHopkinsRezk10)).

   Mathematically this means for instance that $tmf$-cohomology classes help to detect elements in the [[String structure|string]] [[cobordism ring]]. Physically it means that the small aspect of [[string theory]] which is captured by the [[Witten genus]] is realized more deeply as part of fundamental mathematics ([[chromatic homotopy theory|chromatic]] [[stable homotopy theory]], see the next point) and specifically of [[elliptic cohomology]]. Since the full mathematical structure of [[string theory]] is still under investigation, this might point the way:

   > A properly developed theory of elliptic cohomology is likely to shed some light on what [[string theory]] really means. ([Witten 87, very last sentence](#Witten87))



1. **from [[chromatic homotopy theory]].** The [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[stable (∞,1)-category|stable]] [[(∞,1)-category of spectra]] ([[finite spectra]]) has its [[prime spectrum of a symmetric monoidal stable (∞,1)-category|prime spectrum]] parameterized by [[prime numbers]] $p$ and [[Morava K-theory]] spectra $K(n)$ at these primes, for natural numbers $n$. The level $n$ here is called the _[[chromatic level]]_. In some sense the part of this prime spectrum at chromatic level 0 is [[ordinary cohomology]] and that at level 1 is [[topological K-theory]]. Therefore an obvious question is what the part at level 2 would be, and in some sense the answer is $tmf$. (This point of view has been particularly amplified in the review ([Mazel-Gee 13](#MazelGee13)) of the writeup of the construction in ([Behrens 13](#Behrens13)), which in turn is based on unpublished results based on ([Hopkins 02](#Hopkins02))). For purposes of [[stable homotopy theory]] this means for instance that $tmf$ provides new tools for computing more [[homotopy groups of spheres]] via an [[Adams-Novikov spectral sequence]].


## Definition 

Write 

* $\mathcal{M}_{cub}$ for the [[moduli stack of curves]] for [[cubic curves]];

* $\mathcal{M}_{ell}$ for the [[moduli stack of elliptic curves]];

* $\mathcal{M}_{\overline{ell}}$ for its [[Deligne-Mumford compactification]] obtained by adding the [[nodal cubic curve]].

(Here $\mathcal{M}_{cub}$ is obatined by furthermor adding also the [[cuspidal cubic curve]], hence we have canonical maps $\mathcal{M}_{ell}\to \mathcal{M}_{\overline{ell}}\to \mathcal{M}_{cusp} \to \mathcal{M}_{FG}$).

The [[Goerss-Hopkins-Miller theorem]] equips these three moduli stacks with [[E-∞ ring]]-valued [[structure sheaves]] $\mathcal{O}^{top}$ (and by [[A Survey of Elliptic Cohomology|Lurie (Survey)]] that makes them into [[spectral Deligne-Mumford stacks]] which are moduli spaces for [[derived elliptic curves]] etc.)

The _$tmf$-spectrum_ is defined to be the $E_\infty$-ring of [[global sections]] of $\mathcal{O}^{op}$ (in the sense of [[derived algebraic geometry]], hence the [[homotopy limit]] of $\mathcal{O}^{top}$ over the [[etale site]] of $\mathcal{M}$). More precisely one sets

* $TMF \coloneqq \Gamma(\mathcal{M}_{ell}, \mathcal{O}^{top})$;

* $Tmf \coloneqq \Gamma(\mathcal{M}_{\overline{ell}}, \mathcal{O}^{top})$;

* $tmf \coloneqq$ the [[connective cover]] of $Tmf$ (also $\simeq \Gamma(\mathcal{M}_{\overline{cub}}, \mathcal{O}^{top})$ ([Hill-Lawson 13, p. 2](#HillLawson13}) (?)).

##Constructions


### Decomposition via Arithmetic fracture squares
 {#DecomopositionViaArithmeticSquares}

We survey here some aspects of the explicit construction in ([Behrens 13](#Behrens13)), a review is also in ([Mazel-Gee 13](#MazelGee13)),

The basic strategy here is to use [[arithmetic squares]] in order to decompose the problem into smaller more manageable pieces.

Write $\overline{\mathcal{M}_{ell}}$ for the compactified [[moduli stack of elliptic curves]]. In there one finds the pieces

$$
  \array{
    \overline{\mathcal{M}_{ell}} 
    &\stackrel{\iota_{p}}{\leftarrow}& 
    (\overline{\mathcal{M}_{ell}})_p
    \\
    {}^{\mathllap{\iota_{\mathbb{Q}}}}\uparrow
    \\
    (\overline{\mathcal{M}_{ell}})_{\mathbb{Q}}
  }
$$

given by [[rationalization]]  

$$
  (\overline{\mathcal{M}_{ell}})_{\mathbb{Q}}
  = 
  \overline{\mathcal{M}_{ell}}
  \underset{Spec(\mathbb{Z})}{\times}
  Spec(\mathbb{Q})
$$ 

(hence this is the moduli of [elliptic curves over the rational numbers](elliptic+curve#OverTheRationalNumbers))
and by [[p-completion]] 

$$
  (\overline{\mathcal{M}_{ell}})_p
  =
  (\overline{\mathcal{M}_{ell}})
  \underset{Spec(\mathbb{Z})}{\times}
  Spf(\mathbb{Z}_p)
$$

for any [[prime number]] $p$, where $\mathbb{Z}_p$ denotes the [[p-adic integers]] and $Spf(-)$ the [[formal spectrum]]. (Hence this is the moduli  of [elliptic curves over p-adic integers](elliptic+curve#OverpAdics)).



This induces the [[arithmetic square]] decomposition which realizes $\mathcal{O}^{top}$ as the [[homotopy fiber product]] in 

$$
  \array{
    \mathcal{O}^{top} &\to& \prod_p (\iota_p)_\ast \mathcal{O}^{top}_p
    \\
    \downarrow && \downarrow^{\mathrlap{L_{\mathbb{Q}}}}
    \\
    (\iota_{\mathbb{Q}})_\ast \mathcal{O}^{top}_{\mathbb{Q}}
    &\stackrel{\alpha_{arith}}{\to}&
    \left(
     \prod_p (\iota_p)_\ast \mathcal{O}^{top}_p
    \right)_{\mathbb{Q}}
  }
$$

Here $\mathcal{O}^{top}_{\mathbb{Q}}$ can be obtained directly, and to obtain $\mathcal{O}^{top}_p$ one uses in turn another [[fracture square]], now decomposing via [[K(n)-localization]] into $K(1)$-local and $K(2)$-local pieces.

(...)

### Stacks from spectra

There is a way to "construct" the tmf-spectrum as the [[E-∞ ring]] of [[global section]]s of a [[structured (∞,1)-topos]] whose underlying space is essentially the [[moduli stack]] of [[elliptic curve]]s. We sketch some main ideas of this construction.

#### The context -- derived geometry over formal duals of $E_\infty$-rings

The discussion happens in the context of [[derived geometry]] in the [[(∞,1)-topos]] $\mathbf{H}$ over a [[small (∞,1)-category|small]] version of the [[(∞,1)-site]] of formal duals of [[E-∞ ring]]s ([[ring spectra]]). This is equipped with some [[subcanonical coverage]]. For $R \in E_\infty Ring$ we write $Spec R$ for its image under the [[(∞,1)-Yoneda embedding]] $(E_\infty Ring)^{op} \hookrightarrow \mathbf{H}$.

+-- {: .un_lemma}
###### Observation

The [[terminal object in an (∞,1)-category|terminal object]] in $\mathbf{H}$ is the formal dual of the [[sphere spectrum]]

$$
  * \simeq Spec(\mathbb{S})
  \,.
$$

=--

Because the sphere spectrum is the [[initial object]] in $E_\infty Ring$.

#### Coverings by the Thom spectrum

The crucial input for the entire construction is the following statement.



The idea is that the formal dual of the [[complex cobordism cohomology|complex cobordism]] [[Thom spectrum]] $M U$ is in a suitable sense a covering

$$
  Spec M U \to  Spec \mathbb{S}
$$

of the [[terminal object]] in $\mathbf{H}$. (See at _[Adams spectral sequence -- As derived descent](Adams%20spectral%20sequence#DefinitionInHigherAlgebra)_)


This means that $Spec M U$ plays the role of a [[cover]] of the point. This allows to do some computations with ring spectra _locally on the cover $Spec M U$_ . Since $M U^*$ is the [[Lazard ring]], this explains why [[formal group law]]s show up all over the place.

To see this, first notice that the problem of realizing $R = tmf$ or any other ring spectrum as the ring of global sections on something has a _tautological solution_ : almost by definition (see [[generalized scheme]]) there is an $E_\infty$-ring valued [[structure sheaf]] $\mathcal{O}Spec(R)$ on $Spec R$ and its global sections is $R$. So we have in particular

$$
  tmf \simeq \mathcal{O}(Spec(tmf))
  \,.
$$ 

In order to get a less tautological and more insightful characterization, the strategy is now to pass on the right to the $Spec M U$-cover by forming the [[(∞,1)-pullback]]

$$
  \array{
    Spec(tmf) \times Spec(M U) &\to& Spec(tmf)
    \\
    \downarrow && \downarrow
    \\
    Spec(M U) &\to& * \simeq Spec(\mathbb{S})
  }
  \,.
$$

The resulting [[Cech nerve]] is a [[groupoid object in an (∞,1)-category]] given by

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spec(tmf) \times Spec(MU) \times Spec(MU) \stackrel{\to}{\to} Spec(tmf) \times Spec(MU)
$$

which by formal duality is

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spec (tmf \wedge MU \wedge MU) \stackrel{\to}{\to} Spec ( tmf \wedge MU)

$$

where the [[smash product]] $\wedge$ of ring spectra over the [[sphere spectrum]] $\mathbb{S}$ is the [[tensor product]] operation on function algebras formally dual to forming products of spaces.



As a [[groupoid object in an (∞,1)-category|groupoid object]] this is still equivalent to just $Spec(tmf)$.


#### Decategorification: the ordinary moduli stack of elliptic curves

To simplify this we take a drastic step and apply a lot of [[decategorification]]: by applying the [[homotopy group]] [[(∞,1)-functor]] to all the $E_\infty$-rings involved these are sent to graded ordinary [[ring]]s $\pi_*(tmf)$, $\pi_*(M U)$ etc. The result is an ordinary [[simplicial object|simplicial]] [[scheme]]

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spec (\pi_*(tmf \wedge M U \wedge  M U)) \stackrel{\to}{\to} Spec ( \pi_*(tmf \wedge M U))
  \,,
$$

which remembers the fact that its structure rings are graded by being equipped with an [[action]] of the multiplicative group $\mathbb{G} = \mathbb{A}^\times$ (see [[line object]]).

This general Ansatz is discussed in ([Hopkins](#Hopkins)).

This simplicial scheme, which is degreewise the formal dual of a graded ring of [[generalized (Eilenberg-Steenrod) cohomology|generalized homology]]-groups one can show is in fact a [[groupoid]], hence a [[stack]]: effectively the [[moduli stack of elliptic curves]]. $\mathcal{M}_{ell}$. See ([Henriques](#HenriquesModuli)).


In fact if in this construction one replaced $Spec tmf$ by the point, one obtains the simplicial scheme

$$
  \cdots \stackrel{\to}{\stackrel{\to}{\to}} Spec (\pi_*(M U \wedge M U)) \stackrel{\to}{\to} Spec ( \pi_*(M U))
$$

which one finds is the [[moduli stack  of formal group laws]] $\mathcal{M}_{fg}$.



#### Explicit computation of homotopy groups by a spectral sequence

Now, a priori these underived stacks remember little about the original [[derived scheme]]s $Spec tmf$ etc. They may not even carry any $E_\infty$-ring valued structure sheaf anymore (though some of them do). 

If they do carry an $E_\infty$-ring valued structure sheaf $\mathcal{O}$, one can compute the homotopy groups of its global sections by a [[spectral sequence]]

$$
  H^p(\mathcal{M}_{ell}, \pi_q(\mathcal{O}))
  \Rightarrow
  \pi_{p+q} \mathcal{O}(\mathcal{M}_{ell})
  \,.
$$

But it turns out that even if the derived structure sheaf does not exist, this spectral sequence may still converge and may still compute the homotopy groups of the ring spectrum that one started with. This gives one way to compute the homotopy groups of $tmf$. 

For the case of $tmf$ one finds that the homotopy sheaves $\pi_q(\mathcal{O}(\mathcal{M}_{ell}))$ are simple: they vanish in odd degree and are [[tensor power]]s $\omega^{\otimes k}$ of the canonical line bundle $\omega$ in even degree $2 k$, where the fiber of $\omega$ over an [[elliptic curve]] is the [[tangent space]] of that curve at its identity element. A [[section]] of $\omega^{\otimes k}$ is a [[modular form]] of weight $k$. So the whole problem of computing the homotopy groups of $tmf$ boils down to computing the [[abelian sheaf cohomology]] of the moduli stack of elliptic curves with coefficients in these abelian groups of modular forms --- and then examining the resulting spectral sequence.

This can be done quite explicitly in terms of a long but fairly elementary computation  in ordinary algebra. A detailed discussion of this computation is in ([Henriques](#Henriques))

### With Level structure
 {#WithLevelStructure}

The [[moduli stack of elliptic curves]] has covers by that of [[elliptic curves with level structure]] $\Gamma$. Under some conditions these covers inherit derived structure sheaves $\mathcal{O}^{top}$ and hence induce spectra of "topological forms with level structure", $tmf(\Gamma)$ ([Mahowald-Rezk 09](#MahowaldRezk09)). For more on this see at _[[modular equivariant elliptic cohomology]]_.

For instance $tmf_0(2)$ (for the [[congruence subgroup]] which preserves an NS-R [[spin structure]] on elliptic curves over the complex numbers) is the [[elliptic spectrum]] $Ell$ of ([Landweber-Ravenel-Stong 93](#spin+orientation+of+Ochanine+elliptic+cohomology#LandweberRavenelStong93)), see at _[[tmf0(2)]]_.

Discussion of level structure also governs the relation of tmf to K-theory, see at _[Maps to K-theory and Tate K-theory](#MapToTateKTheory)_. 

## Properties

### Homotopy groups
 {#HomotopyGroups}

The first few [[homotopy groups]] of $tmf$ are ([Hopkins 02, section 4.3](#Hopkins02))


| $k$ |  0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 |
|-----|----|---|---|---|---|---|---|---|---|----|----|----|----|----|----|
| $\pi_k(tmf)$ | $\mathbb{Z}$ | $\mathbb{Z}/2\mathbb{Z}$ | $\mathbb{Z}/2\mathbb{Z}$ | $\mathbb{Z}/24\mathbb{Z}$ | 0 | 0 | $\mathbb{Z}/2\mathbb{Z}$ | 0 | $\mathbb{Z}\oplus \mathbb{Z}/2\mathbb{Z}$ | $(\mathbb{Z}/2\mathbb{Z})^2$ | $\mathbb{Z}/6\mathbb{Z}$ | 0 | $\mathbb{Z}$ | $\mathbb{Z}/3\mathbb{Z}$ | $\mathbb{Z}/2\mathbb{Z}$ | $\mathbb{Z}/2\mathbb{Z}$ |

### Boardman homomorphism
 {#BoardmanHomomorphism}

Write $\mathbb{S}$ for the [[sphere spectrum]] and [[tmf]] for the [[connective spectrum]] of [[topological modular forms]].
Since [[tmf]] is an [[E-∞ ring|E-∞]][[ring spectrum]], there is an essentially unique homomorphism of [[E-∞ ring|E-∞]][[ring spectra]]

$$
  \mathbb{S}
  \overset{e_{tmf}}{\longrightarrow}
  tmf
  \,.
$$

Regarded as a morphism of [[generalized homology]]-theories, this is also called the [[Hurewicz homomorphism]], or rather the [[Boardman homomorphism]] for $tmf$


+-- {: .num_prop #BoardmanHomomorphismInTmfIs6Connected}
###### Proposition
**(Boardman homomorphism in $tmf$ is 6-connected)**

The [[Boardman homomorphism in tmf]]

$$
  \mathbb{S}
  \overset{e_{tmf}}{\longrightarrow}
  tmf
$$

induces an [[isomorphism]] on [[stable homotopy groups]] 
(hence from the [[stable homotopy groups of spheres]]), up to degree 6:

$$
  \pi_{\bullet \leq 6}(\mathbb{S})
  \underoverset{\simeq}{\pi_{\bullet \leq 6}(e_{tmf})}{\longrightarrow}
  \pi_{\bullet\leq 6}(tmf)
  \,.
$$


=--

([Hopkins 02, Prop. 4.6](#Hopkins02), [DFHH 14, Ch. 13](#DFHH14))




### Inclusion of circle 2-bundles 
 {#InclusionOfCircle2Bundles}


Write $B^2 U(1) \simeq K(\mathbb{Z},3)$ for the [[abelian ∞-group]] whose underlying [[homotopy type]] is the [[classifying space]] for [[circle 2-bundle]]. Write $\mathbb{S}[B^2 U(1)]$ for its [[∞-group ∞-ring]]. 


+-- {: .num_prop}
###### Proposition

There is a canonical homomorphism of [[E-∞ rings]]

$$
  \mathbb{S}[B^2 U(1)] \to tmf
  \,.
$$

=--

See ([Ando-Blumberg-Gepner 10, section 8](#ABG10)).

+-- {: .num_remark}
###### Remark

This means that every [[circle 2-bundle]] ($U(1)$-[[bundle gerbe]]) given by a modulating map $\chi \colon X \to B^2 U(1)$ determines a class represented by

$$
  X \stackrel{\chi}{\to} B^2 U(1) \to \mathbb{S}[B^2 U(1)] \to tmf
$$

in the $tmf$-[[generalized cohomology]] of its base space $X$.

=--


### Maps to K-theory and to Tate K-theory
 {#MapToTateKTheory}


The inclusion of the compactification point (representing the [[nodal curve]] but being itself the [[cusp]] of $\mathcal{M}_{\overline{ell}}$) into the [[Deligne-Mumford compactification|compactified]] [[moduli stack of elliptic curves]] $\mathcal{M}_{\overline{ell}}$ is equivalently the inclusion of the [[moduli stack of 1-dimensional tori]] $\mathcal{M}_{1dtori} = \mathcal{M}_{\mathbb{G}_m}$ ([Lawson-Naumann 12, Appendix A](#LawsonNaumann12))

$$
  \mathcal{M}_{\mathbb{G}_m}
  \simeq \mathbf{B}\mathbb{Z}_2
 \longrightarrow 
  \mathcal{M}_{\overline{ell}}
  \to
  \mathcal{M}_{FG}
$$

and pullback of [[global sections]] of [[Goerss-Hopkins-Miller-Lurie theorem]]-wise $E_\infty$-ring valued structure sheaves yields maps

$$
  KO \longleftarrow \longleftarrow \mathbb{S}
$$


exhibiting [[KO]] $= \Gamma(\mathcal{M}_{\mathbb{G}_m}, \mathcal{O}^{top})$.

At least after [[localization of a ring|2-localization]] the canonical [[double cover]] of the compactification of $\mathcal{M}_{\mathbb{G}_m} \simeq \mathbf{B}\mathbb{Z}_2$ similarly yields under $\Gamma(-,\mathcal{O}^{top})$ the inclusion of $ko$ as the $\mathbb{Z}_2$-[[homotopy fixed points]] of $ku$ (see at _[[KR-theory]]_ for more on this)

$$
  \array{
    ku_{(2)}
    \\
    \uparrow
    \\
    ko_{(2)}
  }  
$$

and combined with the above this comes with maps from $tmf$ by restriction along the inclusion of the [[nodal curve]] [[cusp]] as

$$
  \array{
    ku_{(2)} & \longleftarrow & tmf_1(3)_{(2)}
    \\
    \uparrow && \uparrow
    \\
    ko_{(2)} & \longleftarrow & tmf_{(2)}
  }  
  \,,
$$

([Lawson-Naumann 12, theorem 1.2](#LawsonNaumann12)), where $tmf_1(3)$ denotes [[topological modular forms]] with [[level structure on an elliptic curve|level-3 structure]] ([Mahowald-Rezk 09](#MahowaldRezk09)).


Moreover, including not just the nodal curve cusp but its [[formal neighbourhood]], which is the [[Tate curve]], there is analogously a canonical map of $E_\infty$-rings

$$
  tmf \longrightarrow KO[ [ q ] ]
$$

to [[Tate K-theory]] (this is originally asserted in [Ando-Hopkins-Strickland 01](#AndoHopkinsStrickland01), details are in [Hill-Lawson 13, appendix A](#HillLawson13)).

### Witten genus and string orientation

The $tmf$-[[spectrum]] is the codomain of the [[Witten genus]], or rather of its refinements to the [[string orientation of tmf]] with value in [[topological modular forms]]

$$ 
   \sigma : M String \to tmf
  \,.
$$

The original Witten genus is the value of the composite of this with the [map to Tate K-theory](#MapToTateKTheory) on [[homotopy groups]]. ([Ando-Hopkins-Rezk 10](#AndoHopkinsRezk10))



### Chromatic filtration

[[!include chromatic tower examples - table]]

### Anderson self-duality

The [[spectrum]] $Tmf$ is self-dual under [[Anderson duality]], more precisley $Tmf[1/2]$ is Anderson-dual to $\Sigma^{21} Tmf[1/2]$ ([Stojanoska 11, theorem 13.1](#Stojanoska11))


### Modular equivariant versions

See at _[[modular equivariant elliptic cohomology]]_
and at _[[Tmf(n)]]_.



## Related concepts

* [[taf]]

[[!include moduli stack of curves -- table]]

## References ##

The idea of a [[generalized cohomology theory]] with [[coefficients]] the ring of [[topological modular forms]] providing a home for the refined [[Witten genus]] of

* {#Witten87a} [[Edward Witten]],  _Elliptic Genera And Quantum Field Theory_, Commun. Math. Phys. 109 525 (1987) ([euclid.cmp/1104117076](http://projecteuclid.org/euclid.cmp/1104117076), [pdf](https://people.maths.ox.ac.uk/beem/papers/elliptic_genus_witten.pdf))

and produced as a [[homotopy limit]] of [[elliptic cohomology]] theories over the [[moduli stack of elliptic curves]] was originally announced, as joint work with [[Mark Mahowald]] and [[Haynes Miller]], in 

* {#Hopkins94} [[Michael Hopkins]], section 9 of _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([[Hopkins_TopModFormsAtICM.pdf:file]], [doi:10.1007/978-3-0348-9078-6_49](https://doi.org/10.1007/978-3-0348-9078-6_49))

(There the spectrum was still called "$eo_2$" instead of "$tmf$".) The details of the definition then appeared in


* {#Hopkins02} [[Michael Hopkins]], section 4 of _Algebraic topology and modular forms_, Proceedings of the ICM, Beijing 2002, vol. 1, 283--309 ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397))

A central tool that goes into the construction is the [[Goerss-Hopkins-Miller theorem]], see there for references on that.

Textbook account:

* {#DFHH14} [[Christopher Douglas]], [[John Francis]], [[André Henriques]], [[Michael Hill]] (eds.), _Topological Modular Forms_, Mathematical Surveys and Monographs Volume 201, AMS 2014  ([ISBN:978-1-4704-1884-7](https://bookstore.ams.org/surv-201))


Expositions include

* {#MazelGee13} [[Aaron Mazel-Gee]], _You could've invented $tmf$_, April 2013 ([pdf slides](http://math.berkeley.edu/~aaron/writing/ustars-tmf-beamer.pdf), [notes pdf](http://math.berkeley.edu/~aaron/writing/tmf-seminar-talk.pdf))

* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology]]_

See also

* [[Chris Douglas]], [[André Henriques]], _Topological modular forms and conformal nets_, in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:1103.4187](https://arxiv.org/abs/1103.4187), [doi:10.1090/pspum/083](https://doi.org/10.1090/pspum/083))

An actual detailed account of the construction of $tmf$ (via decomposition by [[arithmetic squares]]) is spelled out in

* {#Behrens13} [[Mark Behrens]], _Notes on the construction of $tmf$_, 2013 ([pdf](http://math.mit.edu/~mbehrens/papers/buildTMF.pdf))

A complete account of the computation of the homotopy groups of $tmf$ (following previous unpublished computations) is in 

* [[Tilman Bauer]], _Computation of the homotopy groups of the spectrum $tmf$_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/eo2ss.pdf))

A survey of how this works is in

* [[Akhil Mathew]], _The homotopy groups of $TMF$_ ([pdf](http://math.uchicago.edu/~amathew/tmfhomotopy.pdf))

  (This presents as an instructive much simpler but analogous case the construction of [[KO]] in analogy to the construction of $tmf$, more details on this are in [Mathew 13, section 3](#Mathew13).)

and course notes that go through the construction of tmf and the computation of its homotopy groups are here:

*  _Talbot workshop on TMF_ ([web](http://math.mit.edu/conferences/talbot/2007/tmfproc/))

   * {#Hopkins} [[Mike Hopkins]] (talk notes by [[Michael Hill]]), _Stacks and complex oriented cohomology theories_ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter08/MikesTalk1.pdf))
    

   * {#Henriques} [[André Henriques]], _The homotopy groups of tmf_ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter16/TmfHomotopy.pdf))
     

   * {#HenriquesModuli} [[André Henriques]], _The moduli stack of elliptic curves_   ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter04/henriques.pdf))     

The non-connective version of this is discussed in

* [[Johan Konter]], _The homotopy groups of the spectrum Tmf_ ([arXiv:1212.3656](http://arxiv.org/abs/1212.3656))


Supplementary material graphically displaying parts of these intricate computations is in 

* [[André Henriques]],

  the graded ring $tmf^\ast(pt)$ ([pdf](http://www.staff.science.uu.nl/~henri105/PDF/TmfRing.pdf));

  the [[spectral sequence]] used to compute it ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/henriques-tmfSS.pdf));

  whose $E_2$-page is $Ext_{A(2)}(\mathbb{F}_2, \mathbb{F}_2)$ where $A(2)$ is displayed here: [pdf](http://www.staff.science.uu.nl/~henri105/PDF/A2.pdf);

  the spectral sequence that computes $Tmf^\ast(pt)$ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/EllipticSpectralSequence.pdf))


The $\mathbb{Z}_2$-[[homology]] of $tmf$ is discussed in 

* {#Mathew13} [[Akhil Mathew]], _The homology of $tmf$_ ([arXiv:1305.6100](http://arxiv.org/abs/1305.6100))

The refinement of the [[Witten genus]] to a morphism of [[E-∞ rings]] to $tmf$, hence the [[string orientation of tmf]] is due to 

* [[Michael Hopkins]], _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

* {#AndoHopkinsStrickland01} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], _Elliptic spectra, the Witten genus and the theorem of the cube_, Invent. Math. 146 (2001) 595&#8211;687 MR1869850


* [[Michael Hopkins]], _Algebraic topology and modular forms_, Proceedings of the ICM, Beijing 2002, vol. 1, 283--309 ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397))

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Michael Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

see also remark 1.4 of

* [[Paul Goerss]], _Topological modular forms (after Hopkins, Miller and Lurie)_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.5130v1.pdf)).

and for more on the [[sigma-orientation]] see

* [[Matthew Ando]], _The sigma orientation for analytic circle-equivariant elliptic cohomology_, Geom. Topol. 7 (2003) 91-153 ([arXiv:math/0201092](http://arxiv.org/abs/math/0201092))



Discussion of [[twisted cohomology]]  with [[coefficients]] in $tmf$
is in 

* {#ABG10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], section 8 of _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 

Topological modular forms with _[[level N-structure]]_ -- $tmf(N)$ -- is discussed in 

* {#MahowaldRezk09} [[Mark Mahowald]] [[Charles Rezk]], _Topological modular forms of level 3_, Pure Appl. Math. Quar. 5 (2009) 853-872 ([pdf](http://www.math.uiuc.edu/~rezk/tmf3-paper-final.pdf))

* {#DavisMahowald10} [[Donald Davis]], [[Mark Mahowald]], _Connective versions of $TMF(3)$_ ([arXiv:1005.3752](http://arxiv.org/abs/1005.3752))


* {#Stojanoska11} [[Vesna Stojanoska]], Duality for Topological Modular Forms ([arXiv:1105.3968](http://arxiv.org/abs/1105.3968))


* {#LawsonNaumann12} [[Tyler Lawson]], [[Niko Naumann]], _Strictly commutative realizations of diagrams over the Steenrod algebra and topological modular forms at the prime 2_, Int. Math. Res. Not. (2013) ([arXiv:1203.1696](http://arxiv.org/abs/1203.1696))

* {#HillLawson13} [[Michael Hill]], [[Tyler Lawson]], _Topological modular forms with level structure_, Inventiones mathematicae volume 203, pages 359–416 (2016) ([arXiv:1312.7394](http://arxiv.org/abs/1312.7394), [doi:10.1007/s00222-015-0589-5](https://doi.org/10.1007/s00222-015-0589-5))

  > (with [[level structure on an elliptic curve|level structure]])

The self-[[Anderson duality]] of $tmf$ is discussed in ([Stojanoska 11](#Stojanoska11)).

On equivariant topological modular forms (on [[equivariant elliptic cohomology]]):

* [[David Gepner]], [[Lennart Meier]], _On equivariant topological modular forms_, ([arXiv:2004.10254](https://arxiv.org/abs/2004.10254))

On the [[Boardman homomorphism]] (generalized [[Hurewicz homomorphism]]) to [[tmf]]:

* [[Mark Behrens]], [[Mark Mahowald]], J.D. Quigley, _The 2-primary Hurewicz image of $tmf$_ ([arXiv:2011.08956](https://arxiv.org/abs/2011.08956))




[[!redirects Tmf]]
[[!redirects TMF]]


[[!redirects tmf spectrum]]