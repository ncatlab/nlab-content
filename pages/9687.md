
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+-- {: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Confinement (e.g [Espiru 94](#Espiru94)) is the (expected) phenomenon in [[Yang-Mills theory]]/[[QCD]] that [[quark]]-excitations must form [[bound state|bound states]] which are neutral under the color charge -- such as the [[hadron|hadrons]] ([[proton|protons]], [[neutron|neutrons]]) and [[meson|mesons]].

Confinement is a [[non-perturbative effect]] (e.g [Espiru 94](#Espiru94)).

## Possible realizations

### In $\mathcal{N}=2$ super Yang-Mills theory via Seiberg-Wittern theory

While confinement in plain [[Yang-Mills theory]] is still waiting for mathematical formalization and [[proof]] (see [Jaffe-Witten](#JaffeWitten)), there is a variant of [[Yang-Mills theory]] with more [[symmetry]] where the phenomenon has been demonstrated, namely in [[N=2 D=4 super Yang-Mills theory]] ([Seiberg-Witten 94](#SeibergWitten94)).

### In $\mathcal{N} = 1$ super Yang-Mills theory via M-theory on $G_2$-manifolds
 {#ForN1SYMViaMTheoryOnG2Manifolds}

An idea for a strategy towards a proof of confinement in [[N=1 D=4 super Yang-Mills theory]] via two different but conjecturally equivalent realizations as [[M-theory on G2-manifolds]] has been given in [Atiyah-Witten 01, section 6](#AtiyahWitten01), review is in [Acharya-Gukov 04, section 5.3](#AcharyaGukov04).

The idea here is to consider a [[KK-compactification]] of [[M-theory]] on [[fibers]] which are [[G2-manifolds]] that locally around a special point 
are of the form

$$
  X_{1,\Gamma} 
  \;\coloneqq\;
  \big( S^3 / \Gamma \big) \times Cone\big(S^3\big)
  \phantom{AA}
  \text{or}
  \phantom{AA}
  X_{2,\Gamma} 
  \;\coloneqq\;
  S^3 \times Cone\big(S^3/\Gamma\big)
$$

where 

* $\Gamma$ is a [[finite subgroup of SU(2)]] that [[action|acts]] canonically by left-multiplication on $S^3 \simeq $ [[SU(2)]];

* $Cone(\cdots)$ denotes the [[metric cone]] construction.

This means that $X_{1,\Gamma}$ is a [[smooth manifold]], but $X_{2,\Gamma}$, as soon as $\Gamma$ is not the [[trivial group]], $\Gamma \neq 1$, is an [[orbifold]] with an [[ADE singularity]].

Now the lore of [[M-theory on G2-manifolds]] predicts that [[KK-compactification]]

1.  on $X_{1,\Gamma}$ yields a 4d theory without massless fields (since there are no massless modes on the [[covering space]] $S^3$ of $X_{1,\Gamma}$)

1. on the [[ADE-singularity]] $X_{2,\Gamma}$ yields [[non-abelian group|non-abelian]] [[Yang-Mills theory]] in 4d coupled to [[chiral fermions]].

So in the first case a [[mass gap]] is manifest, while non-abelian gauge theory is not visible, while in the second case it is the other way around.

But is there were an argument that [[M-theory on G2-manifolds]] is in fact equivalent for compactification both on $X_{1,\Gamma}$ and on $X_{2,\Gamma}$. To the extent that this is true, it looks like an argument that could demonstrate confinement in non-abelian 4d gauge theory.

This approach is suggested in [Atiyah-Witten 01, pages 84-85](#AtiyahWitten01). An argument that this equivalence is indeed the case is then provided in sections 6.1-6.4, based on an argument in [Atiyah-Maldacena-Vafa 00](#AtiyahMaldacenaVafa00) 

## Related concepts

* [[asymptotic freedom]]
* [[quantization of Yang-Mills theory]]

## References

### In Yang-Mills theory
 {#ReferencesInYangMillsTheory}

#### General

Introductions and surveys include

* Wikipedia, _[Color confinement](http://en.wikipedia.org/wiki/Color_confinement)_

* {#Espiru94} D. Espriu, section 7 of _Perturbative QCD_ ([arXiv:hep-ph/9410287](http://arxiv.org/abs/hep-ph/9410287))

A formulation of confinement as an open problem of mathematical physics, together with many references, is in 

* {#JaffeWitten} [[Arthur Jaffe]], [[Edward Witten]], _Quantum Yang-Mills theory_ ([pdf](http://www.claymath.org/millennium/Yang-Mills_Theory/yangmills.pdf))
 

Other technical reviews include

* G. M. Prosperi, _Confinement and bound states in QCD_ ([arXiv:hep-ph/0202186](http://arxiv.org/abs/hep-ph/0202186))

#### Via monopole condensation
 {#ViaMonopoleCondensation}

An original suggestion that confinement in [[Yang-Mills theory]] may be understood via [[monopole]] [[condensate|condensation]] as a dual [[Meissner effect]] is due to 

* {#Hooft75} [[Gerard 't Hooft]], in Proceed.of the Europ.Phys.Soc. 1975, ed.by A.Zichichi (Editrice Compositori, Bologna, 1976), p.1225.

* {#Mandelstam76} S. Mandelstam, Phys.Rep. 23C (1976) 145;

(That this is indeed the case has not yet been demonstarted for plain Yang-Mills theory, but it was later shown for [[N=2 D=4 super Yang-Mills theory]] in ([Seiberg-Witten 94](#SeibergWitten94)). What this does or does not imply for the case of [[QCD]] is discussed in ([Yung 00](#Yung00)) ).


The relation to [[QCD instantons]]/[[monopole|monopoles]] in the [[QCD vacuum]] is discussed in section III D of 

* {#SchaeferShuryak} T. Schaefer, E. Shuryak, _Instantons in QCD_, Rev. Mod. Phys.70:323-426,1998 ([arXiv:hep-ph/9610451](http://arxiv.org/abs/hep-ph/9610451))
 

For further developments see

* _Dimensional Transmutation by Monopole Condensation in QCD_ ([arXiv:1206.6936](http://arxiv.org/abs/1206.6936))

### Interacting field vacuum

Discussion of confinement as a result of the [[interacting vacuum]] includes

* {#Rafelski90} [[Johann Rafelski]], _Vacuum structure -- An Essay_, in pages 1-29 of H. Fried, Berndt Müller (eds.) _Vacuum Structure in Intense Fields_, Plenum Press 1990 ([GBooks](https://books.google.de/books?id=5uXcBwAAQBAJ&pg=PA14&lpg=PA14&dq=confinement+%22interacting+vacuum%22&source=bl&ots=xPGYJ-JOc-&sig=AoYbqWQeNRMg6hMSRZjJ3nzq8B0&hl=en&sa=X&ved=0ahUKEwjIgK68-tnYAhVCESwKHThMDykQ6AEIKTAA#v=onepage&q=confinement%20%22interacting%20vacuum%22&f=false))

See also

* {#Simonov18} Yu. A. Simonov, _What is the confinement mechanism in QCD?_ ([arXiv:1804.08946](https://arxiv.org/abs/1804.08946))

### In super-Yang-Mills theory
 {#ReferencesInSuperYangMillsTheory}

Confinement in [[N=2 D=4 super Yang-Mills theory]] by a version of the monopole condensation of ([t Hooft 75](#Hooft75), [Mandelstam 76](#Mandelstam76)) was demonstrated in

* {#SeibergWitten94} [[Nathan Seiberg]], [[Edward Witten]], _Monopole Condensation, And Confinement In N=2 Supersymmetric Yang-Mills Theory_,  	Nucl.Phys.B426:19-52,1994; Erratum-ibid.B430:485-486,1994 ([arXiv:hep-th/9407087](http://arxiv.org/abs/hep-th/9407087))

* {#SeibergWitten94b} [[Nathan Seiberg]], [[Edward Witten]], _Monopoles, Duality and Chiral Symmetry Breaking in N=2 Supersymmetric QCD_,  	Nucl.Phys.B431:484-550,1994 ([arXiv:hep-th/9408099](http://arxiv.org/abs/hep-th/9408099))
  
Reviews with discussion of the impact on confinement in plain YM include

* {#Yung00} Alexei Yung, _What Do We Learn about Confinement from the Seiberg-Witten Theory_ ([arXiv:hep-th/0005088](http://arxiv.org/abs/hep-th/0005088))

### Under the AdS/CFT correspondence

Discussion in the context of the [[AdS-CFT correspondence]] is in

* [[David Berman]], Maulik K. Parikh, _Confinement and the AdS/CFT Correspondence_, Phys.Lett. B483 (2000) 271-276 ([arXiv:hep-th/0002031](https://arxiv.org/abs/hep-th/0002031))

* Henrique Boschi Filho, _AdS/QCD and confinement_, Seminar at the _Workshop on Strongly Coupled QCD: The confinement problem_, November 2011 ([pdf](http://www.if.ufrj.br/~boschi/pesquisa/seminarios/AdS_QCD_Confinement_UERJ_2011.pdf))

### In M-theory on $G_2$-manifolds

An idea for how to demonstrate confinement in models of [[M-theory on G2-manifolds]] is given in 

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]], section 6 of  _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

based on 

* {#AtiyahMaldacenaVafa00} [[Michael Atiyah]], [[Juan Maldacena]], [[Cumrun Vafa]], _An M-theory Flop as a Large N Duality_, J.Math.Phys.42:3209-3220, 2001 ([arXiv:hep-th/0011256](https://arxiv.org/abs/hep-th/0011256))

See also 

* [[Bobby Acharya]], _Confining Strings from $G_2$-holonomy spacetimes_ ([arXiv:hep-th/0101206](https://arxiv.org/abs/hep-th/0101206))

For review see

* {#AcharyaGukov04} [[Bobby Acharya]], [[Sergei Gukov]], section 5.3 of _M theory and Singularities of Exceptional Holonomy Manifolds_, Phys.Rept.392:121-189,2004 ([arXiv:hep-th/0409191](https://arxiv.org/abs/hep-th/0409191))


[[!redirects confinement]]
[[!redirects color confinement]]
[[!redirects colour confinement]]