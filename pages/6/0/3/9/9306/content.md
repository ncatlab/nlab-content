
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Small objects
+--{: .hide}
[[!include compact object - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### Local definition as functors on Artinian objects

+-- {: .num_defn }
###### Definition

Given a [[deformation context]] $(\mathcal{Y}, \{E_\alpha\}_\alpha)$, the [[(∞,1)-category]] of **formal moduli problems** over it is the full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-presheaves]] over $\mathcal{Y}^{inf}$

$$
  Moduli^\mathcal{Y}
  \hookrightarrow
  [\mathcal{Y}^{inf}, \infty Grpd]
$$

on those [[(∞,1)-functors]] $X \colon \mathcal{Y}^{inf} \to \infty Grpd$ such that

1. over the [[terminal object]] they are [[contractible]]: $X(*) \simeq *$ (hence they are [[anti-reduced object|anti-reduced]]);

1. they preserve [[(∞,1)-pullbacks]] of small morphisms (are [[cohesive ∞-presheaf on E-∞ rings|infinitesimally cohesive]])

=--

([Lurie, Def. 1.1.14 with Def. 1.1.8](#Lurie))


+-- {: .num_remark }
###### Remark

This means that a "formal deformation problem" is a [[space]] in [[higher geometry]] whose geometric structure is detected by the "test spaces" in $\mathcal{Y}^{op}$ in a way that respects gluing ([[descent]]) in $\mathcal{Y}^{op}$ as given by [[(∞,1)-pullbacks]] there. The first condition requires that there is an essentially unique such probe by the point, hence that these higher geometric space has essentially a single global point. This is the condition that reflects the infinitesimal nature of the deformation problem.

=--

+-- {: .num_remark }
###### Remark

The clause about pullbacks is what makes the behaviour at arbitrary infinitesimal order be all controlled by that at first order, see [Calaque-Grivaux 18, top of p. 8](#CalaqueGrivaux18).

This ability to understand deformations order-by-order is related to the existence of a good obstruction theory. Indeed, evaluating a formal moduli problem $X$ on a pullback diagram defining an elementary morphism exhibits $X(\Omega^{\infty - n}E)$ as an obstruction space.


=--


## Properties

### Relation to $L_\infty$-algebras
  {#RelationToLInfinityAlgebras}

For $k$ a [[field]] of [[characteristic]] 0, write
write $CAlg_k^{sm} \hookrightarrow CAlg_k$ for the [[(∞,1)-category]] of [[Artin ring|Artinian]] connective [[E-∞ algebras]] over $k$, or equivalently that of "small" commutative [[dg-algebras]] over $k$.

The smallness condition implies connectivity ([Lurie, prop. 1.1.11 (1)](#Lurie)), hence that the [[homotopy group]] of these [[E-∞ algebras]] vanish in negative degree. Notice that for the dg-algebras this means that the [[chain homology]] vanishes in negative degree _if_ the differential is taken to have degree -1 (see [Porta 13, def. 3.1.14](#Porta13) for emphasis). This is the natural condition for the function algebra in [[derived geometry]]. Here these small $E_\infty$/dg-algebras are to be thought of as function algebras on "derived [[infinitesimally thickened points]]".


+-- {: .num_theorem }
###### Theorem

There is an [[equivalence of (∞,1)-categories]]

$$
  L_\infty Alg_k \stackrel{\simeq}{\to} Moduli^{CAlg^{sm}_k}
$$

with that of [[L-∞ algebras]].

=--

In this form this is ([Lurie, theorem 0.0.13](#Lurie)), originally proved as ([Pridham, theorem 2.30 and proposition 4.42](#Pridham)).
See at _[[model structure for L-∞ algebras]]_ for various other incarnations of this equivalence.



### Relation to Lie differentiation

+-- {: .num_prop }
###### Proposition

Given a [[deformation context]] $\mathcal{Y}$, the restricted [[(∞,1)-Yoneda embedding]] gives an [[(∞,1)-functor]]

$$
  Lie \colon \mathcal{Y} \to Moduli^{\mathcal{Y}}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

For $Y \in \mathcal{Y}^{op}$, the object $Lie(Y)$ represents the _[[formal geometry|formal neighbourhood]]_ of the basepoint of $Y$ as seen by the infinitesimally thickened points dual to the $\{E_\alpha\}$.

Hence we may call this the operaton of **[[Lie differentiation]]** of spaces in $\mathcal{Y}^{op}$ around their given base point.

=--

## Related concepts

* [[moduli problem]]

* [[model structure for L-∞ algebras]]

* [[sheaf of L-∞ algebras]]

* [[synthetic differential geometry]]

* [[synthetic differential ∞-groupoid]]

## References

* {#Pridham} [[Jonathan Pridham]], _Unifying derived deformation theories_, Adv. Math. 224 (2010), no.3, 772-826 ([arXiv:0705.0344](http://arxiv.org/abs/0705.0344))

* {#Lurie} [[Jacob Lurie]], _[[Formal moduli problems]]_

* [[Jacob Lurie]], _Moduli problems for ring spectra_ ICM 2010 proceedings contribution [pdf](http://www.math.harvard.edu/~lurie/papers/moduli.pdf)

* {#Porta13} [[Mauro Porta]], _Derived formal moduli problems_, master thesis 2013, [pdf](http://algant.eu/documents/theses/porta.pdf).

* {#CalaqueGrivaux18} Damien Calaque, Julien Grivaux, _Formal moduli problems and formal derived stacks_ ([arXiv:1802.09556](https://arxiv.org/abs/1802.09556))

* Arjen Baarsma: *Deformation problems and $L_\infty$-algebras of Fréchet type*, PhD thesis, Utrecht University (2019) &lbrack;[dspace:1874/386311](https://dspace.library.uu.nl/handle/1874/386311), [pdf](https://webspace.science.uu.nl/~caval101/homepage/Students_files/BaarsmaPhD.pdf)&rbrack;

* Brice Le Grignou, Victor Roca i Lucio: *A new approach to formal moduli problems* &lbrack;[arXiv:2306.07227](https://arxiv.org/abs/2306.07227)&rbrack;


The correspondence between formal moduli problems and [[dg-Lie algebras]] is extended to [[positive characteristic]] in

* {#BrantnerMathew19} [[Lukas Brantner]], [[Akhil Mathew]], _Deformation Theory and Partition Lie Algebras_, arXiv:[1904.07352](https://arxiv.org/abs/1904.07352)



[[!redirects formal moduli problems]]