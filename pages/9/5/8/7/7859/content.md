
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $R$ a [[ring]], the _Brauer group_ $Br(R)$ is the [[group]] of [[Morita equivalence]] classes of [[Azumaya algebras]] over $R$.

## Properties

### Relation to categories of modules
 {#RelationToCatsOfModules}

+-- {: .num_defn }
###### Definition


For $R$ a commutative [[ring]], let $Alg_R$ or $2Vect_R$ (see at [[2-vector space]]/[[2-module]]) be the [[2-category]] whose

* [[objects]] are $R$-[[associative algebra|algebras]];

* [[morphisms]] are [[bimodules]] over $R$-algebras;

* [[2-morphisms]] are bimodule homomorphisms.

=--

+-- {: .num_remark}
###### Remark

This may be understood as the 2-category of (generalized) [[2-vector bundles]] over $Spec R$, the [[Isbell duality|formally dual]] [[space]] whose [[function algebra]] is $R$. This is a [[braided monoidal category|braided monoidal 2-category]]. 

=--

+-- {: .num_defn}
###### Definition

Let 

$$
  \mathbf{Br}(R) \coloneqq Core(Alg_R)
$$

be its [[Picard 3-group]], hence the maximal [[infinity-group|3-group]] inside (which is hence a [[braided 3-group]]), the [[core]] on the invertible objects, hence the [[2-groupoid]] whose

* [[objects]] are algebras which are invertible up to [[Morita equivalence]] under tensor product;

* [[morphisms]] are [[Morita equivalences]]; 

* [[2-morphisms]] are invertible bimodule homomorphisms. 

=--

+-- {: .num_remark}
###### Remark

This may be understood as the 2-groupoid of (generalized) [[line 2-bundles]] over $Spec R$ (for instance [[holomorphic line 2-bundles]] in the case of [[higher complex analytic geometry]]), inside that of all [[2-vector bundles]].

=--

+-- {: .num_prop}
###### Proposition

The [[homotopy groups]] of $\mathbf{Br}(R)$ are the following:

* $\pi_0(\mathbf{Br}(R))$ is the Brauer group of $R$;

* $\pi_1(\mathbf{Br}(R))$ is the [[Picard group]] of $R$;

* $\pi_2(\mathbf{Br}(R))$ is the [[group of units]] of $R$.

=--

See for instance ([Street](#Street)).

+-- {: .num_example}
###### Example

Analogous statements hold for (non-commutative) [[superalgebras]], hence for $\mathbb{Z}_2$-[[graded algebras]]. See at _[superalgebra -- Picard 3-group, Brauer group](super+algebra#Picard2Groupoid)_.

=--


### Relation to &#233;tale cohomology
 {#RelationToEtaleCohomology}

The Brauer group of a [[ring]] $R$ is a [[torsion]] subgroup of the second [[etale cohomology]] group of $Spec R$ with values in the [[multiplicative group]] $\mathbb{G}_m$

$$
  Br(X) \hookrightarrow H^2_{et}(X, \mathbb{G}_m)
  \,.
$$

This was first stated in ([Grothendieck 68](#Grothendieck68)) (see also [Grothendieck 64, prop. 1.4](#Grothendieck64) and see at _[algebraic line n-bundle -- Properties](algebraic+line+n-bundle#Properties)_). Review discussion is in ([Milne, chapter IV](#Milne)). A detailed discussion in the context of [[nonabelian cohomology]] is in ([Giraud](#Giraud)).

A theorem stating conditions under which the Brauer group is precisely the [[torsion]] subgroup of $H^2_{et}(X, \mathbb{G}_m)$ is due to ([Gabber](#Gabber)), see also the review in ([de Jong](#deJong)). For more details and more literature on this see ([Bertuccioni](#Bertuccioni)).


This fits into the following pattern

* $H^0_{et}(R, \mathbb{G}_m) = R^\times$ ([[group of units]])

* $H^1_{et}(R, \mathbb{G}_m) = Pic(R)$ ([[Picard group]]: iso classes of invertible $R$-modules)

* $H^2_{et}(R, \mathbb{G}_m)_{tor} = Br(R)$ ([[Brauer group]]: [[Morita equivalence]] classes of [[Azumaya algebras]] over $R$) (the torsion equivalence classes of the [[Brauer stack]])

It is therefore natural to regard all of $H^2_{et}(R, \mathbb{G}_m)$ as the "actual" Brauer group. This has been called the "[[bigger Brauer group]]" ([Taylor 82](#Taylor82), [Caenepeel-Grandjean 98](#CaenepeelGrandjean98), [Heinloth-Sch&#246;er 08](#HeinlothSchoeer08)). The bigger Brauer group has actually traditionally been implicit already in the term "[[formal Brauer group]]", which is really the [[formal geometry]]-version of the bigger Brauer group.




### Relation to derived &#233;tale cohomology
 {#RelationToDerivedEtaleCohomology}

More generally, this works for $R$ a (connective) [[E-infinity ring]] 
(the following is due to [Antieau-Gepner 12](#AntieauGepner12), see [Haugseng 14](#Haugseng14) for more). 

Let $GL_1(R)$ be its [[infinity-group of units]]. 
If $R$ is [[connective spectrum|connective]], then the first [[Postnikov tower|Postnikov stage]] of the [[Picard group|Picard]] [[infinity-groupoid]]

$$
  Pic(R) \coloneqq Mod(R)^\times
$$

is
 
$$
  \array{
   \mathbf{B}_{et} GL_1(-) &\to& Pic(-)
   \\
   && \downarrow
   \\
   && \mathbb{Z}
  }
  \,,
$$

where the top morphism is the inclusion of locally free $R$-modules.

So $H^1_{et}(R, GL_1)$ is not equal to $\pi_0 Pic(R)$, but it is off only by $H^0_{et}(R, \mathbb{Z}) = \prod_{components of R} \mathbb{Z}$.

Let $Mod_R$ be the [[(infinity,1)-category]] of $R$-[[module spectra|modules]].

There is a notion of $Mod_R$-[[enriched (infinity,1)-category]], of "$R$-linear $(\infty,1)$-categories".

$Cat_R \coloneqq Mod_R$-modules in [[presentable (infinity,1)-categories]].

Forming module $(\infty,1)$-categories is then an [[(infinity,1)-functor]]

$$
  Alg_R \stackrel{Mod}{\to} Cat_R
$$

Write $Cat'_R \hookrightarrow Cat_R$ for the image of $Mod$.  Then define the [[Brauer group|Brauer]] [[infinity-group]] to be

$$
  Br(R) \coloneqq (Cat'_R)^\times
$$

One shows ([Antieau-Gepner 12](#AntieauGepner12)) that this is exactly the Azumaya $R$-algebras modulo Morita equivalence.

**Theorem** (B. Antieau, D. Gepner) 

1. For $R$ a connective $E_\infty$ ring, any Azumaya $R$-algebra $A$ is &#233;tale locally trivial: there is an [[etale topology|etale cover]] $R \to S$ such that $A \wedge_R S \stackrel{Morita \simeq}{\to} S$.

   (Think of this as saying that an Azumaya $R$-algebra is &#233;tale-locally a Matrix algebra, hence Morita-trivial: a "bundle of compact operators" presenting a (torsion) $GL_1(R)$-2-bundle).

1. $Br : CAlg_R^{\geq 0} \to Gpd_\infty$ is a sheaf for the [[etale cohomology]].

**Corollary** 

1. $Br$ is [[connected object in an (infinity,1)-topos|connected]]. Hence $Br \simeq \mathbf{B}_{et} \Omega Br $.

1. $\Omega Br \simeq Pic$, hence $Br \simeq \mathbf{B}_{et} Pic$

  
[[Postnikov tower]] for $GL_1(R)$:

$$
  for\; n \gt 0: \pi_n GL_1(S) \simeq \pi_n 
$$

hence for $R \to S$ &#233;tale

$$
  \pi_n S \simeq \pi_n R \otimes_{\pi_0 R} \pi_0 S
$$

This is a [[quasi-coherent sheaf]] on $\pi_0 R$ of the form $\tilde N$ (quasicoherent sheaf associated with a module), for $N$ an $\pi_0 R$-module. By vanishing theorem of higher cohomology for quasicoherent sheaves

$$
  H_{et}^1(\pi_0 R, \tilde N) = 0; for p \gt 0
$$

For every [[(infinity,1)-sheaf]] $G$ of [[infinity-groups]], there is a [[spectral sequence]]

$$
  H_{et}^p(\pi_0 R; \tilde \pi_q G) \Rightarrow \pi_{q-p} G(R)
$$

(the second argument on the left denotes the $qth$ Postnikov stage). From this one gets the following.

* $\tilde \pi_0 Br \simeq *$

* $\tilde \pi_1 Br \simeq \mathbb{Z}$;

* $\tilde \pi_2 Br \simeq \tilde \pi_1 Pic \simeq \pi_0 GL_1 \simeq \mathbb{G}_m$

* $\tilde \pi_n Br$ is quasicoherent for $n \gt 2$.

there is an [[exact sequence]]

$$
  0 \to 
  H_{et}^2(\pi_0 R, \mathbb{G}_m)
  \to \pi_0 Br(R)
  \to H_{et}^1(\pi_0 R, \mathbb{Z})
  \to 0
$$

(notice the inclusion $Br(\pi_0 R) \hookrightarrow H_{et}^2(\pi_0 R, \mathbb{G}_m)$)

this is [[split exact sequence|split exact]] and so computes $\pi_0 Br(R)$ for connective $R$.

Now some more on the case that $R$ is not connective. 

Suppose there exists $R \stackrel{\phi}{\to} S$ which is a faithful 
[[Galois extension]] for $G$ a [[finite group]].

**Examples** 

1. (real into complex [[K-theory spectrum]]) $KO \to KU$ (this is $\mathbb{Z}_2$) 

1. [[tmf]] $\to tmf(3)$

Give $R \to S$, have a [[fiber sequence]]

$$
  Gl_1(R/S) \stackrel{fib}{\to} GL_1(R) \to GL_1(S)
  \to 
  Pic(R/S) \stackrel{fib}{\to} Pic(R) \to Pic(S)
  \to
  Br(R/S) \stackrel{fib}{\to} Br(R) \to Br(S) \to \cdots
$$

**Theorem** (descent theorems) (Tyler Lawson, David Gepner) Given $G$-Galois extension $R \stackrel{\simeq}{\to} S^{hG}$ ([[homotopy fixed points]])

1. $Mod_R \stackrel{\simeq}{\to} Mod_S^{hG}$

1. $Alg_R \stackrel{\simeq}{\to} Alg_S^{hG}$

it follows that there is a homotopy fixed points spectral sequence

$$
  H^p(G, \pi_\bullet \Sigma^n GL_1(S))
  \Rightarrow
  \pi_{-n} GL_1(S)
$$


**Conjecture** The spectral sequence gives an Azumaya $KO$-algebra $Q$ which is a nontrivial element in $Br(KO)$ but becomes trivial in $Br(KU)$.

## Related concepts

* [[Brauer stack]]

* [[formal Brauer group]]

* [[group of units]]/[[multiplicative group]], [[Picard group]]

* [[Azumaya algebra]]

* [[Brauer ∞-group]]

[[!include moduli of higher lines -- table]]



## References

Brauer groups are named after [[Richard Brauer]].

Original discussion includes

* {#Grothendieck64} [[Alexander Grothendieck]], _Le groupe de Brauer: II. Th&#233;ories cohomologiques_. S&#233;minaire Bourbaki, 9 (1964-1966), Exp. No. 297, 21 p. ([Numdam](http://www.numdam.org/item?id=SB_1964-1966__9__287_0))

* {#Grothendieck68} [[Alexandre Grothendieck]], _Le groupe de Brauer_, _Dix expos&#233;s sur la cohomologie des sch&#233;mas_, Masson and North-Holland, Paris and Amsterdam, (1968), pp. 46&#8211;66.


An introduction is in

* Pete Clark, _On the Brauer group_  (2003) ([pdf](http://math.uga.edu/~pete/trivial2003.pdf))


See also

* [[John Duskin]], _The Azumaya complex of a commutative ring_, in: Categorical algebra and its applications (Louvain-La-Neuve, 1987), 107&#8211;117, Lecture Notes in Math. __1348__, Springer 1988. 

* {#Street} [[Ross Street]], _Descent_, Oberwolfach preprint (sec. 5, _Brauer groups_) [pdf](http://www.math.mq.edu.au/~street/Descent.pdf); _Some combinatorial aspects of descent theory_, Applied categorical structures __12__ (2004) 537-576, [math.CT/0303175](http://arxiv.org/abs/math/0303175) (sec. 12, _Brauer groups_)
 

The relation to [[cohomology]]/[[etale cohomology]] is discussed in

* [[James Milne]], _&#201;tale cohomology_, Princeton Mathematical Series, vol. 33, Princeton University Press, Princeton, New Jersey (1980)
 {#Milne}

* [[Jean Giraud]], _Cohomologie non abelienne_, Die Grundlehren der mathematischen Wissenschaften, vol. 179, Springer-Verlag, Berlin, 1971.
 {#Giraud}

* [[Ofer Gabber]], _Some theorems on Azumaya algebras_, Ph. D. Thesis, Harvard University, 1978, Groupe de Brauer, Lecture Notes in Mathematics, vol. 844, Springer-Verlag, Berlin, 1981, pp. 129&#8211;209.

* [[Aise Johan de Jong]], _A result of Gabber_ ([pdf](http://www.math.columbia.edu/~dejong/papers/2-gabber.pdf))
 {#deJong}
  
* Inta Bertuccioni, _Brauer groups and cohomology_, Archiv der Mathematik, vol. 84 Number 5 (2005)
 {#Bertuccioni}

Brauer groups of [[superalgebras]] are discussed in 

* [[C. T. C. Wall]], _Graded Brauer groups_, J. Reine Angew. Math. 213 (1963/1964), 187-199. 

* [[Pierre Deligne]], _Notes on spinors_ in _[[Quantum Fields and Strings]]_

* [[Peter Donovan]], [[Max Karoubi]], _Graded Brauer groups and K-theory with local coefficients_, Publications Math. IHES 38 (1970), 5-25 ([pdf](http://www.math.jussieu.fr/~karoubi/Donavan.K.pdf))

Refinement to [[stable homotopy theory]] and [[Brauer ∞-groups]] is discussed in 

* {#Szymik11} [[Markus Szymik]], _Brauer spaces for commutative rings and structured ring spectra_ ([arXiv:1110.2956](http://arxiv.org/abs/1110.2956))

* {#BakerRichterSzymik12} [[Andrew Baker]], [[Birgit Richter]], [[Markus Szymik]], _Brauer groups for commutative $\mathbb{S}$-algebras_, J. Pure Appl. Algebra 216 (2012) 2361&#8211;2376 ([arXiv:1005.5370](http://arxiv.org/abs/1005.5370))

Unification of all this in a theory of [[(infinity,n)-modules]] is in

* {#Haugseng14} [[Rune Haugseng]], _The higher Morita category of $E_n$-algebras_ ([arXiv:1412.8459](http://arxiv.org/abs/1412.8459))

The "bigger Brauer group" is discussed in 

* {#Taylor82} J. Taylor, _A bigger Brauer group_ Pacific J. Math. 103 (1982), 163-203 ([projecteuclid](https://projecteuclid.org/euclid.pjm/1102724219))

* {#CaenepeelGrandjean98} S. Caenepeel, F. Grandjean, _A note on Taylor's Brauer group_. Pacific J. Math. 186 (1998), 13-27

* {#HeinlothSchoeer08} [[Jochen Heinloth]], Stefan Schr&#246;er, _The bigger Brauer group and twisted sheaves_ ([arXiv:0803.3563](http://arxiv.org/abs/0803.3563))

See also

* [[Jochen Heinloth]], [[Marc Levine]], Stefan Scr&#246;er, _Forschungsseminar: Brauer groups and Artin stack_, 07 ([pdf](https://www.uni-due.de/~mat903/sem/brauer.pdf))

The observation that passing to [[derived algebraic geometry]] makes also the non-torsion elements in $H^2_{et}(-,\mathbb{G}_m)$ be represented by (derived) [[Azumaya algebras]] is due to

* {#Toen10} [[Bertrand Toën]], _Derived Azumaya algebras and generators for twisted derived categories_ ([arXiv:1002.2599](http://arxiv.org/abs/1002.2599))


Related MO discussion includes 

* [Brauer groups and K-theory](http://mathoverflow.net/questions/87345/brauer-groups-and-k-theory)

Systematic discussion of Brauer groups in [[derived algebraic geometry]] is in 

* {#AntieauGepner12} [[Benjamin Antieau]], [[David Gepner]], _Brauer groups and &#233;tale cohomology in derived algebraic geometry_, Geom. Topol. 18 (2014) 1149-1244 ([arXiv:1210.0290](http://arxiv.org/abs/1210.0290))

For the Brauer-Picard 2-group of a tensor category, see

* [[Alexei Davydov]], [[Dmitri Nikshych]], _Braided Picard groups and graded extensions of braided tensor categories_, ([arXiv:2006.08022](https://arxiv.org/abs/2006.08022))

[[!redirects Brauer groups]]

[[!redirects bigger Brauer group]]
[[!redirects bigger Brauer groups]]