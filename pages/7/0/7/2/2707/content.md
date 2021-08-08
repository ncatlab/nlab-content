
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

[[!redirects motives]]


# Contents
* table of contents
{: toc}

## Idea

> In order to express this kinship of these different cohomological theories, I formulated the notion of "motive" associated to an algebraic variety. By this term I want to suggest that it is the "common motive" (or "common reason") behind this multitude of cohomological invariants attached to an algebraic variety, or indeed, behind all cohomological invariants that are a priori possible. ([[Grothendieck]], [[Récoltes et Semailles]])

The similarity of the behaviour of various [[cohomologies]] of [[algebraic variety|varieties]] over a [[field]] suggests that there is a universal one among them with values in an intermediate [[abelian category]], called the _[[category]] of motives_. The idea is that to every variety $X$ is associated a motive $M(X)$, such that every good [[cohomology theory]] factors through the functor $M$. (Here not every motive is supposed to be the image of a single variety.)

One distinguishes a theory of [[pure motives]] for smooth projective varieties from a more general theory of [[mixed motives]] for arbitrary smooth varieties.
So far, pure motives and mixed motives have only been defined conditionally. However there are several equivalent definitions of a [[triangulated category|triangulated]] [[tensor category]] which has all conjectured structural properties of the derived category of mixed motives (except for the t-structure which would make it a derived category).

[[Grothendieck]]'s original realization of this idea is the [[category of Chow motives]], which is a certain abelianization and completion of a [[category of spans]] of [[smooth variety|smooth]] [[projective varieties]]. Later a more [[homotopy theory|homotopy-theoretic]] version was given, the [[Voevodsky motives]] or _derived motives_, see [below](#DerivedMotives), which subsume the Chow motives faithfully. More generally still, there are definitions for _[[noncommutative motives]]_ obtained by passing to [[noncommutative algebraic geometry]]. Finally, the construction principle of motives can also be adapted to other flavors of [[geometry]]. For instance in [[noncommutative topology]] the role of the category of [[noncommutative motives]] is played by [[KK-theory]]. 

Constructions of motives often depend on whether we work in prime [[characteristic]]s or in characteristic zero. Part of the formalism involves more general [[schemes]] than varieties. 

Another crucial idea leading to motives is that the various cohomology theories lead to the same pieces of information; therefore there is a symmetry related to this, which is of [[Galois theory]] nature. For example, over the [[complex numbers]] one can compare the [[Betti cohomology]] and [[de Rham cohomology]] "realizations". Thus one has a  [[motivic Galois group]], and as usually with representations one has a [[tensor category]] structure which is also [[rigid monoidal category|rigid]]. Thus one has in fact an [[abelian category|abelian]] [[tensor category]] of motives. [[Tannakian reconstruction]] plays a major role; for pure motives we have neutral [[Tannakian category|Tannakian categories]], and for mixed motives we have mixed Tannakian categories. Functions on the [[torsor]] of the isomorphism between "realizations" correspond to the matrices of [[period]]s in [[Hodge theory]]. 

$L$-functions (and $\zeta$-functions in particular) of varieties are also invariants of their motives. The [[Langlands program]] indirectly involves motives; in particular its essential part can be expressed as a general modularity conjecture relating $L$-functions to automorphic functions. Most of the deep properties of [[elliptic curve]]s are of motivic nature, and in particular a major step of the proof of [[Fermat's last theorem]] by Wiles and Taylor can be interpreted as a proof of a special case of the modularity conjecture (for elliptic curves). 


## Constructions of the abelian category of mixed motives {#AbelianMotives}

There is no generally accepted construction of a $\mathbb{Q}$-linear [[abelian category]] of mixed motives, and its existence remains conjectural. However, there exist candidate and conditional constructions which are useful in practice.

Note that "the" abelian category of mixed motives depends on choosing a base [[scheme]] $S$, and one speaks of motives (or _motivic sheaves_) over $S$. Traditionally, $S$ is the spectrum of a [[field]], often of characteristic zero.


### Nori motives

[[Madhav Nori]] has an approach to the theory of motives based on a peculiar kind of Tannakian reconstruction, the so called _[[Nori's Tannakian theorem]]_. Nori's construction unconditionally produces a $\mathbb{Q}$-[[Tannakian category]] of mixed motives over any sub[[field]] of $\mathbb{C}$.

### Deligne motives

[[Pierre Deligne]] gave a definition of a category of mixed motives over [[number fields]] as compatible systems of realizations, essentially bundling together all the structure that mixed motives should give rise to. This approach automatically yields a $\mathbb{Q}$-[[Tannakian category]] of mixed motives with all the desired realization functors (Betti, $l$-adic, de Rham, and crystalline). See [Deligne](#DeligneP1) for details.


### As the heart of a t-structure on the derived category of mixed motives

[[Pierre Deligne|Deligne]] first suggested that it might be easier to define the [[derived category]] $DM(S,\mathbb{Q})$ of the hypothetical abelian category of mixed motives. Once this is done, one can in principle recover the abelian category as the heart of a [[t-structure]] on $DM(S,\mathbb{Q})$. It is now well-understood what the [[triangulated category]] $DM(S,\mathbb{Q})$ is over any base [[scheme]] ([see below](#DerivedMotives)). The hypothetical t-structure on $DM(S,\mathbb{Q})$ whose heart is the abelian category of mixed motives over $S$ is called the **motivic t-structure**.

Beilinson proved that, over fields of characteristic zero, the existence of the motivic t-structure implies the [[standard conjectures on algebraic cycles]] (see [Beilinson](#Beilinson10)), and Bondarko proved that it implies the existence of motivic t-structures for more general schemes (see [Bondarko](#Bondarko13)).

While the derived category of mixed motives can also be defined with integral rather than rational coefficients, Voevodksy observed that the derived category of integral motives cannot have a motivic t-structure ([Voevodsky, Prop. 4.3.8](#TriCatMixMot)). Thus, the _abelian_ category of motives always refers to motives with rational coefficients.

### References

* [[Alexander Beilinson]], _Remarks on Grothendieck's standard conjectures_, 2010, ([arXiv](http://arxiv.org/abs/1006.1116))
{#Beilinson10}

* [[Mikhail Bondarko]], _Mixed motivic sheaves (and weights for them) exist if 'ordinary' mixed motives do_, 2013, ([arXiv](http://arxiv.org/abs/1105.0420))
{#Bondarko13}

* [[Pierre Deligne]], _Le groupe fondamental de la droite projective moins trois points_, ([pdf](http://publications.ias.edu/sites/default/files/61_LeGroupeFondamentalDroite.pdf))
{#DeligneP1}

* [[Vladimir Voevodsky]], _Triangulated categories of motives over a field_, ([K-theory](http://www.math.uiuc.edu/K-theory/0074/))
{#TriCatMixMot}


## Constructions of the derived category of mixed motives {#DerivedMotives}

The [[derived category]] of the hypothetical abelian category of mixed motives has been unconditionally defined over any [[Noetherian scheme]]. The first definition was proposed by Voevodsky in the mid 1990s. Since then, several other definitions were formulated: one by Morel, one by Ayoub, and one by Cisinski and D&#233;glise. The latter three are equivalent and support a full-fledged formalism of [[six operations]]. However, they are only known to be equivalent to Voevodsky's definition over [[excellent scheme|excellent]] and [[geometrically unibranch scheme|geometrically unibranch]] schemes.

On the other hand, Voevodsky's definition is the only one among these four which also makes sense with integral coefficients rather than rational coefficients. Recently, Spitzweck proposed a definition of the category of integral motives over general base schemes which also supports a formalism of [[six operations]]. It is known to agree with Voevodsky's definition for [[fields]] of characteristic zero. Rationally, however, it agrees with the Morel/Ayoub/Cisinski-D&#233;glise definition over any base scheme.


### As homotopy invariant Nisnevich sheaves with transfers (Voevodsky motives)
 {#VoevodskyMotives}

Associated to a [[Noetherian scheme]] $S$ there is an [[additive category]] $SmCor_S$ of "finite" [[correspondences]] of [[schemes]], whose

* [[objects]] are smooth schemes of finite type over $S$;

* [[morphism]]s $SmCor_S(X,Y)$ are the abelian group of cycles on the [[fiber product]] $X \times_S Y$ that are "universally integral relative to $X$" and each of whose components are finite and and surjective over $X$.

See at _[[pure motive]]_ for more (see also [MaVoWe, Appendix 1A](#MaVoWe)). Associating to a morphism of schemes its graph defines a [[faithful functor]] $Sm/S\hookrightarrow SmCor_S$.

An **(∞,1)-[[presheaf with transfers]]** on the category $Sm/S$ of smooth schemes of finite type is an [[(∞,1)-presheaf]] on $SmCor_S$ which transforms finite sums into finite (∞,1)-products (and hence take values in connective [[chain complexes]]).

The (∞,1)-category $DM^{eff}_{\geq 0}(S)$ is a certain reflexive [[localization]] of the (∞,1)-category of presheaves with transfers: it consists of those presheaves with transfers whose underlying presheaves on $Sm/S$ are [[(∞,1)-sheaves]] for the [[Nisnevich topology]] and are [[A1-homotopy theory|A1-homotopy invariant]]. 

The **Tate motive** $\mathbb{Z}(1)[2]$ is the image of the pointed scheme $(\mathbb{P}^1,\infty)$ in $DM^{eff}_{\geq 0}(S)$.

+-- {: .num_defn}
###### Definition
The stable (∞,1)-category of (integral) motives $DM(S)$ is the [[stabilization]] of $DM^{eff}_{\geq 0}(S)$ at the Tate motive $\mathbb{Z}(1)[2]$.
=--

The (∞,1)-category $DM(S)$ is a [[stable (∞,1)-category|stable]], [[symmetric monoidal (∞,1)-category|symmetric monoidal]], and [[locally presentable (∞,1)-category|locally presentable]] (∞,1)-category which is [[enriched category|enriched]] in [[chain complexes]]. It is slightly larger than the category $DM^-(S)$ defined in [MaVoWe, p. 110](#MaVoWe) which is not cocomplete.

_Voevodsky's cancellation theorem_ states that the canonical functor $DM^{eff}_{\geq 0}(S)\to DM(S)$ is [[fully faithful]] if $S$ is a [[perfect field]].

### As rational stable motivic homotopy types with trivial action of the Hopf element (Morel motives)

Let $\epsilon : \mathbb{G}_m\wedge \mathbb{G}_m\to \mathbb{G}_m\wedge \mathbb{G}_m$ be the transposition. In the [[stable motivic homotopy category]] $SH(S)$ this becomes an endomorphism of the motivic sphere spectrum $S^0$ such that $\epsilon^2=1$. Rationally (or even away from 2), we obtain a pair of idempotent elements

$$ \frac{1+\epsilon}{2}, \quad \frac{1-\epsilon}{2} $$

which induce a splitting $SH(S)_{\mathbb{Q}}\simeq SH(S)_{\mathbb{Q}_+}\times SH(S)_{\mathbb{Q}_-}$.

+-- {: .num_defn}
###### Definition
$SH(S)_{\mathbb{Q}_+}$ is the stable $(\infty,1)$-category of _Morel motives_.
=--

In other words, a Morel motive is a rational stable motivic homotopy type on which $\epsilon$ acts as $-1$.

The *Hopf element* $\eta\in \pi_{1,1}(S^0)$ is the stabilization of the algebraic [[Hopf fibration]] $\mathbb{A}^2-0\to\mathbb{P}^1$ over $S$. Morel motives can also be characterized as those rational stable motivic homotopy types that are acted on trivially by the Hopf element.

We have $\epsilon=-1$ if and only if $-1$ is a sum of squares in all the residue fields of $S$, in which case $SH(S)_{\mathbb{Q}}= SH(S)_{\mathbb{Q}_+}$. Thus, the other summand $SH(S)_{\mathbb{Q}_-}$ only appears over [[formally real field]]s. It is called the category of _Witt motives_.


### As homotopy invariant &#233;tale sheaves without transfers (Ayoub motives)

According to Ayoub, the stable $(\infty,1)$-category of motives over a scheme $S$ can be constructed in the same way as the stable motivic homotopy category $SH(S)$, with two variations:

* Instead of the [[Nisnevich topology]] on the category of smooth $S$-schemes, use the [[étale topology]]
* Instead of [[(∞,1)-sheaves]] of [[∞-groupoids]], use (∞,1)-sheaves of connective [[chain complexes]] of $\mathbb{Q}$-[[vector spaces]].

The resulting (∞,1)-category is denoted $DA^{\mathrm{et}}(S,\mathbb{Q})$. Its objects are thus $\mathbb{P}^1$-spectra of $\mathbb{A}^1$-invariant &#233;tale [[(∞,1)-sheaves]] with values in connective rational [[chain complexes]].

### As modules over a summand of rational homotopy invariant algebraic K-theory (Beilinson motives)

This definition is due to Cisinski and D&#233;glise. The rationalization of the homotopy invariant [[algebraic K-theory]] spectrum $KGL\in SH(S)$ splits as a direct sum

$$ KGL_{\mathbb{Q}} = \bigoplus_{n\in\mathbb{Z}} \Sigma_T^n H_B $$

for some $E_\infty$ rational motivic ring spectrum $H_B\in SH(S)$.

+-- {: .num_defn}
###### Definition
The stable $(\infty,1)$-category of _Beilinson motives_ is the $(\infty,1)$-category of [[module]]s over $H_B$. Equivalently, it is the full subcategory of $SH(S)_{\mathbb{Q}}$ consisting of $H_B$-local objects.
=--


Cisinski and D&#233;glise have shown that $H_B$ is exactly the $+$-summand $S^0_{\mathbb{Q}_+}$ of the rational motivic sphere spectrum, and hence that a Beilinson motive is the same thing as a Morel motive. They have also shown that Beilinson/Morel motives are equivalent to Ayoub motives. Finally, they have shown that Beilinson motives are equivalent to rational Voevodsky motives $DM(S,\mathbb{Q})$ when $S$ is [[excellent scheme|excellent]] and [[geometrically unibranch scheme|geometrically unibranch]]. Over such schemes, all four definitions of the derived category of mixed motives are therefore equivalent.

### As modules over a spectrum representing motivic cohomology over $Spec \mathbb{Z}$ (Spitzweck motives)

One idea to define a category of integral motives with a formalism of [[six operations]] is to first define an $E_\infty$ motivic ring spectrum $M_{\mathbb{Z}}\in SH(Spec \mathbb{Z})$. If $f: S\to Spec \mathbb{Z}$ is any scheme, we obtain an $E_\infty$-algebra $M_S = f^\ast(M_{\mathbb{Z}})$ in $SH(S)$. The categories of modules over $M_S$ for varying $S$ then inherit a complete formalism of six operations from $SH$.

Spitweck defined such an $E_\infty$-algebra $M_{\mathbb{Z}}$ such that

* if $S$ is smooth over a [[Dedekind domain]], $M_S$ represents [[motivic cohomology|Bloch-Levine motivic cohomology]],
* if $S$ is smooth over a field, $M_S$ is equivalent to Voevodsky's motivic Eilenberg&#8211;Mac Lane spectrum $H\mathbb{Z}$,
* $M_{\mathbb{Z}}\otimes\mathbb{Q}$ is the Beilinson motive $H_B$.

The stable $(\infty,1)$-category of $M_S$-modules is thus a well-behaved candidate for a derived category of integral motives, but it is only known to agree with Voevodsky's definition when $S$ is a field of characteristic zero (by [Rondigs-Ostvaer, Theorem 5.5](#RO08)).

## Variations and extensions

Correspondences are interesting in [[noncommutative geometry]] of the [[operator algebra]] flavour. For example, KK-groups are in fact themselves sort of correspondences; Connes and Skandalis had an early reference very much paralleling some ideas from the algebraic world. More recently, motives in the operator algebraic setup have been approached by Connes, Marcolli and others. 

In derived [[noncommutative algebraic geometry]] based on $A_\infty$-categories, Kontsevich proposed a theory of [[noncommutative motive]]s. There is now already a more general setup (than Kontsevich's) due Cisinski and Tabuada (see Refs.).

In [[birational geometry]], Bruno Kahn defined the appropriate version. In [[rigid analytic geometry]], $A^1$-homotopy theory is replaced by $B^1$-homotopy theory and the appropriate analogue of the Voevodsky's category of mixed motives has been constructed; the construction follows the same basic pattern. 

## Relation to other fields

### Relation to physics

Motivic structures show up in [[quantum field theory]], for instance

* [[motivic multiple zeta values]] in [[scattering amplitudes]]

* the [[motivic Galois group|motivic]] [[cosmic Galois group]] in [[renormalization]].

The [[path integral as a pull-push transform|pull-push quantization]] in [[Gromov-Witten theory]] is naturally understood as a "[[motivic quantization]]" in terms of [[Chow motives]] of [[Deligne-Mumford stacks]] ([Behrend-Manin 95](#BehrendManin95)).


### Relation to KK-theory

See at _[[KK-theory]]_ in the section _[As an analog of motives in noncommutative topology](http://ncatlab.org/nlab/show/KK-theory#AsAnAnalogOfMotives)_.


## Related concepts

* [[pure motive]], [[mixed motive]], [[Voevodsky motive]], [[Nori motive]], [[Chow motive]]

* [[K-motive]], [[noncommutative motive]]

* [[presheaf with transfer]]

* [[motivic homotopy theory]]

* [[motivic cohomology]]

* [[zeta function]], [[motivic multiple zeta values]]

* [[Hodge theory]]

* [[motivic function]]

* [[motivic Donaldson-Thomas invariant]]

* [[Fourier-Mukai transform]]

* See also at _[KK-theory -- Relation to motives](KK-theory#AsAnAnalogOfMotives)_.

* [[motives in physics]]


## References

### General

A brief exposition is in 

* [[Barry Mazur]], _What is... a Motive?_, Notices of the AMS, volume 51, Number 10, 2004 ([pdf](http://www.ams.org/notices/200410/what-is.pdf))

A review is also in chapter I of

* [[Alain Connes]], [[Matilde Marcolli]], _[[Noncommutative Geometry, Quantum Fields and Motives]]_

Lectures include

* {#Levine06} [[Marc Levine]], _Six lectures on motives_, lectures at _ICTP Workshop on K-theory and Motives_ 2006 ([[LevineMotiveLecture.pdf:file]])

The definition of Voevodsky motives can be found in

* [[Carlo Mazza]], [[Vladimir Voevodsky]], [[Charles Weibel]], _Lectures in motivic cohomology_ ([web](http://math.rutgers.edu/~weibel/motiviclectures.html) [pdf](http://www.claymath.org/library/monographs/cmim02.pdf))
{#MaVoWe}

Voevodsky's formalization of motives was sketched in 

* [[Pierre Deligne]], _Voevodsky lectures on cross functors,
Fall 2001. ([pdf](http://mat.uab.cat/~kock/tmp/delnotes01.pdf))
 {#Deligne}

and worked out in detail in 

* [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique (I)_, Ast&#233;risque, vol. 314, Soc. Math. France, 2007.

  _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique (II)_, Ast&#233;risque, vol. 315, Soc. Math. France, 2007.
 {#Ayoub}

the definition of Ayoub motives in

* [[Joseph Ayoub]], _La r&#233;alisation &#233;tale et les op&#233;rations de Grothendieck_ ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/Realisation-Etale.pdf))

For the definition of Beilinson and Morel motives, the equivalences of the various definitions, and the formalism of six operations, see

* [[Denis-Charles Cisinski]], [[Frédéric Déglise]], _Triangulated categories of mixed motives_ ([arXiv](http://arxiv.org/abs/0912.2110))
{#CD12}

The fact that $DM(k)$ is equivalent to the category of $H(\mathbb{Z})$-modules if $\mathrm{char}(k)=0$ is proved in

* [[Oliver Röndigs]], [[Paul Arne Østvær]], _Modules over motivic cohomology_ ([pdf](http://www.math.uni-bielefeld.de/~oroendig/MZfinal.pdf))
{#RO08}

Spitzweck's definition of a motivic cohomology spectrum over $Spec \mathbb{Z}$ is in

* [[Markus Spitzweck]], _A commutative P^1-spectrum representing motivic cohomology over Dedekind domains I_ ([arXiv](http://arxiv.org/abs/1207.4078))

A summary of the axioms and of the main theorems is in the introduction of

* [[Denis-Charles Cisinski]], [[Frédéric Déglise]], _Triangulated categories of mixed motives_, [arxiv/0912.2110](http://arxiv.org/abs/0912.2110)
 {#CisinskiDeglise}

An outline of the big picture can be found in the introduction to

* [[Dmitri Kaledin]], _Motivic structures in non-commutative geometry_, [arxiv/1003.3210](http://arxiv.org/abs/1003.3210)

Some pretty useful comments on motives are at this MathOverflow thead:

* [What's the "Yoga of Motives?"](http://mathoverflow.net/questions/2146/whats-the-yoga-of-motives/2230#2230)

See also the blog post

* [[David Speyer]], _Motive-ating the Weil conjecture proof_ ([blog](http://sbseminar.wordpress.com/2010/06/10/motive-ating-the-weil-conjecture-proof/))

A formal discussion of motives can be found in [lecture 14](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=121) of

* [[Carlo Mazza]], [[Vladimir Voevodsky]] and [[Charles Weibel]], _Lectures in motivic cohomology_ ([web](http://math.rutgers.edu/~weibel/motiviclectures.html) [pdf](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf))

There is also

*  James S. Milne, _[Motives -- Grothendieck's Dream](http://www.jmilne.org/math/xnotes/MOT.pdf)_

*  [[Minhyong Kim]], _[Classical Motives: Motivic $L$-functions](http://www.ucl.ac.uk/~ucahmki/ihes3.pdf)_

* Bruno Kahn, [pdf slides](http://www.aimath.org/WWN/motivesdessins/PaloAlto1.pdf) on pure motives

* Florence Lecomte, Nathalie Wach, _R&#233;alisations des complexes motiviques de Voevodsky_, [arxiv:0911.5611](http://de.arxiv.org/abs/0911.5611)

* [[Marc Levine]], _Smooth motives_, [arxiv:0807.2265](http://arxiv.org/abs/0807.2265)

* [[Marc Levine]], _Mixed motives_, Math. Surveys and Monographs __57__, Amer. Math. Soc.  1998, free [pdf](http://www.ams.org/online_bks/surv57/surv57.pdf)

For a noncommutative analogue to the theory of motives, see [[noncommutative motives]].

Some other aspects

* M.V. Bondarko, _Weight structures vs. $t$-structures; weight filtrations, spectral sequences, and complexes (for motives and in general)_, [arxiv/0704.4003](http://arxiv.org/abs/0704.4003)
* [[Yuri Manin]], _Motives and quantum cohomology_, talk at Colloque Grothendieck, [video](http://www.dailymotion.com/video/x8juco_colloque-grothendieck-yuri-manin_tech)

Motives from the point of view of Grothendieck topoi are studied in 

* [[Olivia Caramello]], _Motivic toposes, [arxiv/1507.06271](http://arxiv.org/abs/1507.06271)

### Relation to Hodge theory

Explicit discussion of the relation to [[Hodge theory]] is in 

* [[Chris Peters]], _Tata Lectures on Motivic Aspects of Hodge Theory_ ([pdf](http://www-fourier.ujf-grenoble.fr/~peters/motivic.f/Tatalects.pdf))

### Relation KK-theory and bivariant K-theory, K-motives
 {#RelationToKKTheory}

Relation of [[motivic cohomology]] to [[bivariant algebraic K-theory]] (see also at _[[KK-theory]]_) is discussed in 

* [[Alain Connes]], [[Caterina Consani]], [[Matilde Marcolli]], _Noncommutative geometry and motives: the thermodynamics of endomotives_ ([arXiv:math/0512138](http://arxiv.org/abs/math/0512138))
 {#ConnesConsaniMarcolli05}

* [[Guillermo Cortiñas]], [[Andreas Thom]], _Bivariant algebraic K-theory_. J. Reine Angew. Math. 510 (2007), 71&#8211;124. ([arXiv:math/0603531](http://arxiv.org/abs/math/0603531))

* [[Grigory Garkusha]], Ivan Panin, _K-motives of algebraic varieties_ ([arXiv:1108.0375](http://arxiv.org/abs/1108.0375))

* [[Grigory Garkusha]], _Algebraic Kasparov K-theory. II_ ([arXiv:1206.0178](http://arxiv.org/abs/1206.0178))

See also at _[KK-theory -- Relation to motives](http://ncatlab.org/nlab/show/KK-theory#AsAnAnalogOfMotives)_.

For a collection of literature see also paragraph 1.5 in 

* [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _A universal characterization of higher algebraic K-theory_ ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282))

(in the context of [[noncommutative motives]]).

### In physics

* A. Rej, [[Matilde Marcolli]], _Motives, an introductory survey for physicists_ ([pdf](http://www.its.caltech.edu/~matilde/ObiMotivesSurveyFinal.pdf))

See also at _[[motivic multiple zeta values]]_.

That the [[path integral as a pull-push transform|pull-push quantization]] in [[Gromov-Witten theory]] is naturally understood as a "[[motivic quantization]]" in terms of [[Chow motives]] of [[Deligne-Mumford stacks]] was suggested in

* [[Kai Behrend]], [[Yuri Manin]], _Stacks of Stable Maps and Gromov-Witten Invariants_ ([arXiv:alg-geom/9506023](http://arxiv.org/abs/alg-geom/9506023))
 {#BehrendManin95}

Further investigation of these stacky Chow motives then appears in 

* [[Bertrand Toën]], _On motives for Deligne-Mumford stacks_, International Mathematics Research Notices 2000, 17 (2000) 909-928 ([arXiv:math/0006160](http://arxiv.org/abs/math/0006160), [web](http://hal.archives-ouvertes.fr/hal-00773027), [pdf](http://hal.archives-ouvertes.fr/docs/00/77/30/27/PDF/motdm.pdf))
 {#Toen00}

* [[Utsav Choudhury]], _Motives of Deligne-Mumford Stacks_ ([arXiv:1109.5288](http://arxiv.org/abs/1109.5288))

For more see at _[[motives in physics]]_.


category: algebraic geometry
[[!redirects motif]]
[[!redirects motive]]
[[!redirects motives]]
[[!redirects category of motives]]
[[!redirects categories of motives]]
[[!redirects derived category of motives]]
[[!redirects derived category of mixed motives]]
[[!redirects motivic]]