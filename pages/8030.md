
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[physics]], _moduli stabilization_ refers to the problem of rendering [[Kaluza-Klein compactifications]] stable.

A [[Kaluza-Klein compactification]] is a [[model (physics)|model]] of [[gravity]] where [[spacetime]] is assumed to be a higher dimensional [[fiber bundle]], with [[compact topological space|compact]] [[fibers]] of tiny extension, such that the resulting physics looks effectively lower-dimensional, but inheriting extra [[field (physics)|fields]]. Namely the size and shape of the compactified extra dimension is encoded in the [[Riemannian metric]], hence in the field of gravity, hence are themselves dynamical fields. Since these fields parameterize the [[moduli space]] of the KK-compactification, they are called _[[moduli fields]]_. 

The problem of _moduli stabilization_ is the problem of identifying mechanisms or conditions that ensure that as these fields dynamically evolve, the compact spatial dimensions remain stably so, neither opening up nor collapsing. For [[phenomenology|phenomenologically]] realistic KK-compactifications the compact volume has to stably be a tiny but finite value ("volume stabilization").


Equivalently, since fast varying moduli appear as light or massless [[particles]] in the low-dimensional [[effective field theory]] which would show up in accelerator [[experiments]] (such as the [[LHC]]) but don't, the problem is to identify mechanisms or conditions that would render these moduli fields massive.


### For pure vacuum gravity compactifications
 {#ForPureVacuumGravity}

In pure [[classical field theory|classical]] [[gravity]] KK-compactifications have been suggested ([Penrose 03, section 10.3](#Penrose03)) to generically be unstable due to the [[Penrose-Hawking singularity theorem]]. 

But a rigorous analysis in [Anderson-Blue-Wyatt-Yau 20](#AndersonBlueWyattYau20) claims to show that, in contrast, even vacuum spacetimes are stable under KK-compactification (for $\geq 10$-dimensions with a [[Killing spinor]] on the [[compact topological space|compact]] [[fiber]] and for [[Schwarzschild spacetime|Schwarzschild]]-asymptotics).



### For Freund-Rubin flux compactifications
 {#FluxCompactfications}



If in addition to pure [[gravity]] extra [[gauge fields]] or [[higher gauge field]] beyond pure gravity are admitted in the higher dimensions, then stable compactifications may exist if there is "magnetic [[flux]]" in the compact fiber spaces. These are called _[[Freund-Rubin compactifications]]_, or _[[flux compactifications]]_. 

A well-studied example is 6-dimensional [[Einstein-Maxwell theory]] with magnetic [[flux]] on a 2-dimensional [[fiber]] spaces over a 4-dimensional base space ([Freund-Rubin 80](#FreundRubin80), [RDSS 83](#RDSS83)).

(On the other hand, Freund-Rubin compactifications usually have fibers the site of the curvature radius of the base, and hence not "small".)

Similarly, in [[string theory]] it is argued that the extra fields and further string theoretic effects may stabilize the compact dimensions, namely a combination of [[flux compactification]] and [[non-perturbative effect|non-perturbative]] [[brane]] effects ([Acharya 02](#Acharya02), [KKLT 03](#KKLT03)). However, these arguments typically focus on fluctuations that preserve given [[special holonomy]] ([[supersymmetry and Calabi-Yau manifolds|Calabi-Yau 3-folds]] in type II or [[M-theory on G2-manifolds|G2-manifolds in M-theory]]). There is also a more generic argument for volume compactification by string winding modes ("[[Brandenberger-Vafa mechanism]]" [Brandenberger-Vafa 89](#BrandenbergerVafa89), [Watson-Brandenberger 03](#WatsonBrandenberger03)) and the claim ([Kim-Nishimura-Tsuchiya 12](#KimNishimuraTsuchiya12)) that in the non-perturbative [[IKKT model]] computer simulations show a spontaneous stable compactification to 3+1 dimensions.

### For string theory compactifications

The issue of stabilization of compact dimensions arises notably in [[string theory]] [[Kaluza-Klein compactifications]]. 

In the context of [[type II string theory]] one way to design the [[model (in theoretical physics)|model]] such that the moduli fields are massive is to consider the case where [[higher gauge field|higher]] [[background gauge fields]] [[vacuum expectation value|vacuum expectation values]] (VEVs) $F_p$ are present on the compactification space.  Since these fields are characterized by their higher [[field strength]]/[[curvature]] forms which are referred to as "[[flux]]" terms in physics, these models are called **[[flux compactification]]** models ([KKLT 03](#KKLT03)).

Because the standard [[kinetic action]] term

$$
  S_{kin} \propto \int F_p \wedge \star_g F_p
$$

couples the flux VEV to the metric $g$ (via the [[Hodge star operator]]) and hence to the moduli, it generically induces an effective [[potential energy]] for these, which may stabilize them (when including [[non-perturbative effects]]).

Similarly in [[M-theory on G2-manifolds]] the 4-form flux of the [[supergravity C-field]] leads to potentials for the moduli, which is argued to generically stabilize them ([Acharya 02](#Acharya02)).

Since for these flux compactifications only the [[periods]] of the form fields on the compact space matter, under a bunch of further assumptions on the nature of the compactification, one can reduce the number of possible such compactifications to a combinatorial problem. The resulting space of possibilities is also known  as the _[[landscape of string theory vacua]]_.

\linebreak

A widely studied but non-rigorous scenario of moduli stabilization in string theory is due to ([KKLT 03](#KKLT03)). More recently, the assumptions of the KKLT scenario have been called into question ([Danielsson-Van Riet 18](#de+Sitter++spacetime#DanielssonVanRiet18), see also at [[swampland conjectures]]):

The moduli stabilization in ([KKLT 03](#KKLT03)) was (informally) argued in two steps. First, all moduli were stabilized at a fixed minimum with a negative [[cosmological constant]]. This was achieved by combining [[flux compactification|fluxes]] with [[non-perturbative effects]]. Second, the minimum was lifted to a metastable vacuum with a positive cosmological constant. This was accomplished by adding anti D-branes and using previous results, obtained in ([Kachru-Pearson-Verlinde 01](#KachruPearsonVerlinde01)), that the flux-anti D-brane system can form a metastable bound state with positive energy. In ([KKLT 03](#KKLT03)) it was also shown that one can fine tune various parameters to make the value of the [[cosmological constant]] consistent with the observed amount of [[dark energy]].

## Related concepts

* [[flux compactification]]

* [[G2-MSSM]]

* [[landscape of string theory vacua]]

* [String Theory FAQ -- Do the extra dimensions lead to instability of 4 dimensional spacetime?](string+theory+FAQ#StabilityOfKKCompactification)

## References

### In pure gravity

The problem of generic in-stability of moduli of pure gravity KK-compactifications is highlighted in

* {#Penrose03} [[Roger Penrose]], section 10.3 in _On the stability of extra space dimensions_ in Gibbons, Shellard, Rankin (eds.) _The Future of Theoretical Physics and Cosmology_, Cambridge (2003) ([spire:608935](https://inspirehep.net/record/608935))

A rigorous [[proof]] that, in contrast, even vacuum spacetimes are stable under KK-compactification is claimed (for $\geq 10$-dimensions with a [[Killing spinor]] on the [[compact topological space|compact]] [[fiber]] and for [[Schwarzschild spacetime|Schwarzschild]]-asymptotics) in

* {#AndersonBlueWyattYau20} [[Lars Andersson]], [[Pieter Blue]], [[Zoe Wyatt]], [[Shing-Tung Yau]], _Global stability of spacetimes with supersymmetric compactifications_ ([arXiv:2006.00824](https://arxiv.org/abs/2006.00824))

### Freund-Rubin flux compactifications
 {#ReferencesFreundRubinCompactificationo}

[[Freund-Rubin compactification|Freund-Rubin]] [[flux compactifications]] are due to

A class of stable compactifications of 6d Einstein-Maxwell theory down to four dimensions is due to

* {#FreundRubin80} [[Peter Freund]] and M. A. Rubin, _Dynamics Of Dimensional Reduction_, Phys. Lett. B 97, 233 (1980) (<a href="https://doi.org/10.1016/0370-2693(80)90590-0">doi:10.1016/0370-2693(80)90590-0</a>, [spire:154579](http://inspirehep.net/record/154579))

and the special case of compactifications of 6d Einstein-Maxwell theory to 4d is in

*  {#RDSS83} S. Randjbar-Daemi, [[Abdus Salam]] and J. A. Strathdee, _Spontaneous Compactification In Six-Dimensional Einstein-Maxwell Theory_, Nucl. Phys. B 214, 491 (1983) (<a href="https://doi.org/10.1016/0550-3213(83)90247-X">doi:10.1016/0550-3213(83)90247-X</a>, [spire:182427](https://inspirehep.net/record/182427/))

Further discussion of these models as toy models for [[flux compactifications]] in [[string theory]] is in

* {#DouglasKachru07} [[Michael Douglas]], [[Shamit Kachru]], section II.D.1 of _Flux compactification_, Rev. Mod. Phys. 79, 733 (2007) ([arXiv:hep-th/0610102](https://arxiv.org/abs/hep-th/0610102))

* [[Frederik Denef]], [[Michael Douglas]], [[Shamit Kachru]], _Physics of String Flux Compactifications_, Ann. Rev. Nucl. Part. Sci. 57:119-144, 2007, [arXiv:hep-th/0701050](https://arxiv.org/abs/hep-th/0701050)


### In string theory


#### In type II string theory

A generic argument for stabilization of compact dimensions in [[type II string theory]] via string winding modes at the self-[[T-duality]] radius is the [[Brandenberger-Vafa mechanism]], see e.g.

* {#BrandenbergerVafa89} [[Robert Brandenberger]], [[Cumrun Vafa]], _Superstrings In The Early Universe_, Nucl. Phys. B 316, 391  (1989) ([spire](http://inspirehep.net/record/263348))


* {#WatsonBrandenberger03} Scott Watson, [[Robert Brandenberger]], _Stabilization of Extra Dimensions at Tree Level_, JCAP 0311 (2003) 008 ([arXiv:hep-th/0307044](http://arxiv.org/abs/hep-th/0307044))

* [[Brian Greene]], Daniel Kabat, Stefanos Marnerides, _On three dimensions as the preferred dimensionality of space via the Brandenberger-Vafa mechanism_,   10.1103/PhysRevD.88.043527  ([arXiv:1212.2115](http://arxiv.org/abs/1212.2115))

Discussion of moduli stabilization via [[flux compactification]] of and [[non-perturbative effects]] in [[type II string theory]]/[[F-theory]] originates with the influential article ("KKLT")

* {#KKLT03} [[Shamit Kachru]], [[Renata Kallosh]], [[Andrei Linde]], [[Sandip  Trivedi]], _de Sitter Vacua in String Theory_, Phys. Rev. D68:046005, 2003 ([arXiv:hep-th/0301240](http://arxiv.org/abs/hep-th/0301240))

which led to a little burst of discussion of the [[landscape of string theory vacua]]. The analysis there relies on 

* {#KachruPearsonVerlinde01} [[Shamit Kachru]], J. Pearson, [[Herman Verlinde]], _Brane/Flux Annihilation and the String Dual of a Non-Supersymmetric Field Theory_, JHEP 0206 (2002) 021 ([arXiv:hep-th/0112197](http://arxiv.org/abs/hep-th/0112197))

Further developments include

* [[Frederik Denef]], [[Michael Douglas]], Bogdan Florea, Antonella Grassi, [[Shamit Kachru]], _Fixing All Moduli in a Simple F-Theory Compactification_, Adv.Theor.Math.Phys.9:861-929, 2005 ([arXiv:hep-th/0503124](http://arxiv.org/abs/hep-th/0503124))

* [[Vijay Balasubramanian]], Per Berglund, [[Joseph Conlon]], [[Fernando Quevedo]], _Systematics of Moduli Stabilisation in Calabi-Yau Flux Compactifications_,  JHEP 0503:007,2005 ([arXiv:hep-th/0502058](http://arxiv.org/abs/hep-th/0502058))

A variant via K&#228;hler uplifting is

* [[Alexander Westphal]], _de Sitter String Vacua from K&#228;hler Uplifting_, JHEP 0703:102,2007 ([arXiv:hep-th/0611332](https://arxiv.org/abs/hep-th/0611332))

Review includes

* [[Renata Kallosh]], _Stabilization of moduli in string theory_, lectures 2005 ([part I pdf ](http://web.stanford.edu/~rkallosh/Talks/LectureI.pdf), [part II pdf ](http://web.stanford.edu/~rkallosh/Talks/LectureII.pdf))

* [[Joseph Conlon]], _Moduli Stabilisation and Applications in IIB String Theory_, Fortsch.Phys.55:287-422,2007 ([arXiv:hep-th/0611039](http://arxiv.org/abs/hep-th/0611039))

* Sibasish Banerjee, _Calabi-Yau compactification of type II string theories_ ([arXiv:1609.04454](http://arxiv.org/abs/1609.04454))


Analogous discussion in [[type IIA string theory]] includes ([Acharya 02](#Acharya02)) and

* Oliver DeWolfe, Alexander Giryavets, [[Shamit Kachru]], [[Washington Taylor]], _Type IIA Moduli Stabilization_ ([arXiv:hep-th/0505160](http://arxiv.org/abs/hep-th/0505160))


Discussion of volume stabilization of compact dimensions in the context of [[cosmic inflation]] is in

* Jonathan P. Hsu, [[Renata Kallosh]], _Volume Stabilization and the Origin of the Inflaton Shift Symmetry in String Theory_, JHEP 0404 (2004) 042 ([arXiv:hep-th/0402047](http://arxiv.org/abs/hep-th/0402047))



In 

* {#KimNishimuraTsuchiya12} S.-W. Kim, J. Nishimura, and A. Tsuchiya, _Expanding (3+1)-dimensional universe from a Lorentzian matrix model for superstring theory in (9+1)-dimensions_, Phys. Rev. Lett. 108, 011601 (2012), ([arXiv:1108.1540](https://arxiv.org/abs/1108.1540)).

* S.-W. Kim, J. Nishimura, and A. Tsuchiya, _Late time behaviors of the expanding universe in the IIB matrix model_, JHEP 10, 147 (2012), ([arXiv:1208.0711](https://arxiv.org/abs/1208.0711)).

it is claimed that computer simulation shows that the [[IKKT matrix model]] description of, supposedly, non-perturbative type II string theory exhibits spontanous decompactification of 3+1 large dimensions, with the other 6 remaining tiny.


#### In M-theory
 {#ReferencesInMTheory}

Discussion of moduli stabilization in [[M-theory on G2-manifolds]] for stabilization via "[[flux]]" (non-vanishing bosonic  [[field strength]] of the [[supergravity C-field]]) is in

* {#Acharya02} [[Bobby Acharya]], _A Moduli Fixing Mechanism in M theory_ ([arXiv:hep-th/0212294](http://arxiv.org/abs/hep-th/0212294))

and [[moduli stabilization]] for fluxless compactifications via [[nonperturbative effects]], claimed to be sufficient and necessary to solve the [[hierarchy problem]], is discussed in

* {#AcharyaBobkovKaneKumarVaman06} [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Diana Vaman, _An M theory Solution to the Hierarchy Problem_, Phys.Rev.Lett.97:191601,2006 ([arXiv:hep-th/0606262](http://arxiv.org/abs/hep-th/0606262))

* {#AcharyaBobkovKaneKumarShao07} [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Jing Shao, _Explaining the Electroweak Scale and Stabilizing Moduli in M Theory_, Phys.Rev.D76:126010,2007 ([arXiv:hep-th/0701034](http://arxiv.org/abs/hep-th/0701034))

* {#AcharyaKumarBobbkovKaneShaoWatson08} [[Bobby Acharya]], [[Piyush Kumar]], Konstantin Bobkov, [[Gordon Kane]], Jing Shao, Scott Watson, _Non-thermal Dark Matter and the Moduli Problem in String Frameworks_,JHEP 0806:064,2008 ([arXiv:0804.0863](http://arxiv.org/abs/0804.0863))

and specifically for the [[G2-MSSM]] in

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Jing Shao, _The $G_2$-MSSM - An $M$ Theory motivated model of Particle Physics_ ([arXiv:0801.0478](http://arxiv.org/abs/0801.0478))

Discussion of moduli stabilization in [[M-theory on 8-manifolds]] for the [[product manifold]] of two [[K3]]s:

* [[Paul Aspinwall]], [[Renata Kallosh]], _Fixing All Moduli for M-Theory on $K3 \times K3$_, JHEP 0510:001, 2005 ([arXiv:hep-th/0506014](https://arxiv.org/abs/hep-th/0506014))



#### In heterotic string theory

Discussion of moduli stabilization in [[heterotic string theory]] includes

* {#BuchbinderOvrut04} [[Evgeny Buchbinder]], [[Burt Ovrut]], _Vacuum Stability in Heterotic M-Theory_, Phys.Rev. D69 (2004) 086010 ([arXiv:hep-th/0310112](http://arxiv.org/abs/hep-th/0310112))

* [[Sergei Gukov]], [[Shamit Kachru]], Xiao Liu, Liam McAllister, _Heterotic Moduli Stabilization with Fractional Chern-Simons Invariants_,  	Phys.Rev.D69:086008,2004 ([arXiv:hep-th/0310159](http://arxiv.org/abs/hep-th/0310159))



[[!redirects moduli stabilizations]]

[[!redirects Brandenberger-Vafa mechanism]]
[[!redirects Brandenberger-Vafa mechanisms]]
