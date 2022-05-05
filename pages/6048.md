
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The theory of [[11-dimensional supergravity]] contains a higher [[gauge field]] -- the [[supergravity C-field]] -- that naturally couples to higher electrically charged 2-[[branes]], [[membranes]] ([Bergshoeff-Sezgin-Townsend 87](#BergshoeffSezginTownsend87)). By _[[double dimensional reduction]]_, these turn into the [[superstrings]] of [[type IIA string theory]] ([Duff-Howe-Inami-Stelle 87](#DuffHoweInamiStelle87)). (See at _[[duality between M-theory and type IIA string theory]]_.)

When in ([Witten95](#Witten95)) it was argued that the 10-dimensional [[target space]] theories of the five types of [[string theory|superstring theories]] are all limiting cases of one single 11-dimensional target space theory that extends [[11-dimensional supergravity]] ([[M-theory]]), it was natural to guess that this supergravity membrane accordingly yields a 3-dimensional [[sigma-model]] that reduces in limiting cases to the [[string]] [[sigma-models]].

But there were two aspects that make this idea a little subtle, even at this vague level: first, there is no good theory of the [[quantization]] of the membrane [[sigma-model]], as opposed to the well understood quantum [[string]]. Secondly, that hypothetical "theory extending 11-dimensional supergravity" ("M-theory") has remained elusive enough that it is not clear in which sense the membrane would relate to it in a way analogous to how the string relates to its [[target space]] theories (which is fairly well understood).

Later, with the [[BFSS matrix model]] some people gained
more confidence in the idea, by identifying the corresponding degrees
of freedom in a special case ([Nicolai-Helling 98](#NicolaiHelling98), [Dasgupta-Nicolai-Plefka 02](#DasguptaNicolaiPlefka02)). See also at _[[membrane matrix model]]_. 

In a more modern perspective, the M2-brane [[worldvolume]] theory appears under _[AdS4-CFT3 duality](AdS-CFT#AdS4CFT3)_ as a [[holographic principle|holographic dual]] of a [[4-dimensional Chern-Simons theory]]. Indeed, its [[Green-Schwarz action functional]] is entirely controled by the [[super Lie algebra|super]]-[[Lie algebra cocycle|Lie algebra 4-cocycle]] of [[super Minkowski spacetime]] given by the [[brane scan]]. This exhibits the M2-brane worldvolume theory as a 3-dimensional [[higher dimensional WZW model]].

## Definition

There are two different incarnations of the M2-brane. On the one hand it is defined as a [[Green-Schwarz sigma model]] with [[target space]] a [[spacetime]] that is a solution to the [[equations of motion]] of [[11-dimensional supergravity]]. One would call this the "fundamental" M2 in analogy with the "fundamental string", if only there were an "M2-perturbation series" which however is essentially ruled out.

On the other hand the M2 also appears as a [[black brane]], hence as a solution to the [[equations of motion]] of [[11-dimensional supergravity]] with [[singularity]] that looks from outside like a charged 2 dimensional object. 

### As a Green-Schwarz sigma model

See at _[[Green-Schwarz sigma model]]_ and _[[brane scan]]_.

### As a black brane
 {#AsABlackBrane}

As a [[black brane]] solution to the [[equations of motion]] of [[11-dimensional supergravity]] the M2 is the [[spacetime]] $\mathbb{R}^{2,1} \times (\mathbb{R}^8-\{0\})$ with [[pseudo-Riemannian metric]] being

$$
  g = H^{-2/3} g_{\mathbb{R}^{2,1}} + H^{1/3}g_{\mathbb{R}^8-\{0\}}
$$

where 

$$
  H = \alpha + \frac{\beta}{r^6}
$$

for $(\alpha,\beta) \in \mathbb{R}^2 \setminus \{(0,0)\}$;

and the [[field strength]] of the [[supergravity C-field]] is 

$$
  F = d vol_{\mathbb{R}^{2,1}} \wedge \mathbf{d} H^{-1}
  \,.
$$

For $\alpha \beta \neq 0$ this is a 1/2 [[BPS state]] of 11d sugra.

In the above [[coordinates]] the metric is ill-defined at $r = - \beta^{1/6} \alpha$, but in fact it may be smoothly continued through this point ([Duff-Gibbons-Townsend 94, section 3](#DuffGibbonsTownsend94)), which is a [[event horizon]]. An actual singularity is at $r = 0$.


The [[near horizon geometry]] of this spacetime is the [[Freund-Rubin compactification]] [[anti de Sitter spacetime|AdS4]]$\times$[[7-sphere|S7]]. For more on this see at _[[AdS-CFT]]_.

[[!include black branes in supergravity -- table]]

{#BlackM2AtADESingularity} More generally, one may classify those solutions of [[11-dimensional supergravity]] of the form $AdS_4 \times X_7$ for some [[closed manifold]] $X_7$, that are at least 1/2 [[BPS states]]. One finds ([Medeiros-Figueroa 10](#MedeirosFigueroa10)) that all these are of the form $AdS_4 \times S^7/G_{ADE}$, where $S^7 / G_{ADE}$ is an [[orbifold]] of the [[7-sphere]] (a [[spherical space form]] in the smooth case, see [there](spherical+space+form#7DSphericalSpaceFormsWithSpinStructure)) by a [[finite subgroup of SU(2)]] $G_{ADE} \hookrightarrow SU(2)$, i.e. a finite group in the [[ADE-classification]]

[[!include ADE -- table]]

Here for $ 5 \leq \mathcal{N} \leq 8$-supersymmetry then the action of $G_{ADE}$ on $S^7$ is via the canonical action of $SU(2)$ as in the [[quaternionic Hopf fibration]] ([Medeiros-Figueroa 10](#MedeirosFigueroa10)), while for $\mathcal{N} = 4$ then there is an extra twist to the action  ([MFFGME 09](#MFFGME09)). See the table [below](#WorldvolumeTheory).



## Properties

### Worldvolume theory -- BLG and ABJM
 {#WorldvolumeTheory}

The [[worldvolume]] [[QFT]] of [[black brane|black]] M2-branes is a [[3d superconformal gauge field theory]]:

[[!include superconformal symmetry -- table]]

Specifically, [[worldvolume]] [[quantum field theory]] of M2-branes sitting at [[ADE singularities]] (as [above](#BlackM2AtADESingularity)) is supposed to be described by [[ABJM theory]] and, for the special case of $SU(2)$ gauge group, by the [[BLG model]]. See also at _[[gauge enhancement]]_.

[[!include 7d spherical space forms -- table]]



### AdS4-CFT3 duality

Under [[AdS-CFT duality]] the M2-brane is given by
_[AdS4-CFT3 duality](AdS-CFT#AdS4CFT3)_. ([Maldacena 97, section 3.2](#Maldacena97), [Klebanov-Torri 10](#KlebanovTorri10)).

## Related concepts

* [[membrane instanton]]

* [[triple membrane junction]]

* [[BLG model]], [[ABJM model]], [[membrane matrix model]]

* [[string theory]]

* [[11-dimensional supergravity]], [[M-theory]]

* [[string]], [[superstring]]

* [[D-brane]]

* [[M5-brane]], [[6d (2,0)-superconformal QFT]]

* [[M9-brane]]

* [[topological membrane]]

* [[supergravity Lie 3-algebra]], [[M-theory super Lie algebra]]

[[!include table of branes]]

## References

### As a fundamental brane

The [[Green-Schwarz sigma-model]]-type formulation of the supermembrane (as in the [[brane scan]]) first appears in 

* {#BergshoeffSezginTownsend87} [[Eric Bergshoeff]], [[Ergin Sezgin]], and [[Paul Townsend]], _Supermembranes and eleven-dimensional supergravity_, Phys. Lett. B189 (1987) 75&#8211;78. ([spire:248230](http://inspirehep.net/record/248230/))
  
and its [[quantization]] of the was explored in 

* {#DuffInamiPopeSezginStelle88} [[Mike Duff]], T. Inami, [[Christopher Pope]], [[Ergin Sezgin]],  [[Kellogg Stelle]], _Semiclassical Quantization of the Supermembrane_, Nucl.Phys. B297 (1988) 515-538 ([spire:247064](http://inspirehep.net/record/247064))

* [[Bernard de Wit]], [[Jens Hoppe]], [[Hermann Nicolai]], _On the Quantum Mechanics of Supermembranes_, Nucl. Phys. B305 (1988) 545. ([pdf](http://pubman.mpdl.mpg.de/pubman/item/escidoc:153408:1/component/escidoc:153407/353961.pdf), [[deWitHoppeNicolai88.pdf:file]])

* [[Bernard de Wit]], W. L&#252;scher, [[Hermann Nicolai]], _The supermembrane is unstable_, Nucl. Phys. B320 (1989) 135. 

* {#KabatTaylor97} Daniel Kabat, [[Washington Taylor]], section 2 of _Spherical membranes in Matrix theory_, Adv.Theor.Math.Phys.2:181-206,1998 ([arXiv:hep-th/9711078](https://arxiv.org/abs/hep-th/9711078)) 


The [[double dimensional reduction]] of the M2-brane to the [[Green-Schwarz superstring]] was observed in

* {#DuffHoweInamiStelle87} [[Michael Duff]], [[Paul Howe]], T. Inami, [[Kellogg Stelle]], _Superstrings in $D=10$ from Supermembranes in $D=11$_, Phys. Lett. B191 (1987) 70 and in [[Michael Duff]] (ed.) _[[The World in Eleven Dimensions]]_ 205-206 (1987) ([spire](http://inspirehep.net/record/245249))



The interpretation of the membrane as as an object related to [[string theory]], hence as the _M2-brane_ was proposed in 

* [[Paul Townsend]], _The eleven-dimensional supermembrane revisited_, Phys.Lett.B350:184-187, 1995 ([arXiv:hep-th/9501068](http://arxiv.org/abs/hep-th/9501068))

around the time when [[M-theory]] became accepted due to

* {#Witten95} [[Edward Witten]], _[[String Theory Dynamics In Various Dimensions]]_ ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))
 



The interpretation related to the [[BFSS matrix model]] of [[D0-branes]] is discussed in some detail in 

* {#NicolaiHelling98} [[Hermann Nicolai]], Robert Helling, _Supermembranes and M(atrix) Theory_, In _Trieste 1998, Nonperturbative aspects of strings, branes and supersymmetry_ 29-74 ([arXiv:hep-th/9809103](http://arxiv.org/abs/hep-th/9809103), [spire:476366](http://inspirehep.net/record/476366))
  
* {#DasguptaNicolaiPlefka02} Arundhati Dasgupta, [[Hermann Nicolai]], [[Jan Plefka]], _An Introduction to the Quantum Supermembrane_, Grav.Cosmol.8:1,2002; Rev.Mex.Fis.49S1:1-10, 2003 ([arXiv:hep-th/0201182](http://arxiv.org/abs/hep-th/0201182))

* [[Gijs van den Oord]], _On Matrix Regularisation of Supermembranes_, 2006 ([pdf](http://web.science.uu.nl/itf/Teaching/2006/vandenOord.pdf))


### As a black brane

The back membrane solution of [[11-dimensional supergravity]] was found in

* [[Mike Duff]], [[Kellogg Stelle]], _Multimembrane solutions of $D = 11$ supergravity_, Phys. Lett. B 253, 113 (1991) ([spire](http://inspirehep.net/record/299386?ln=en))

Its regularity throught the [[event horizon]] is due to

* {#DuffGibbonsTownsend94} [[Mike Duff]], [[Gary Gibbons]], [[Paul Townsend]], _Macroscopic superstrings as interpolating solitons_, Phys.Lett.B332:321-328,1994 ([arXiv:hep-th/9405124](https://arxiv.org/abs/hep-th/9405124))

The [[Horava-Witten theory|Horava-Witten]]-[[orientifold]] of the black M2, supposedly yielding the [[black brane|black]] [[heterotic string]] is discussed in

* {#LalakLukasOvrut97} Zygmunt Lalak, Andr&eacute; Lukas, [[Burt Ovrut]], _Soliton Solutions of M-theory on an Orbifold_, Phys. Lett. B425 (1998) 59-70 ([arXiv:hep-th/9709214](https://arxiv.org/abs/hep-th/9709214))

* {#Kashima00} Ken Kashima, _The M2-brane Solution of Heterotic M-theory with the Gauss-Bonnet $R^2$ terms_, Prog.Theor.Phys. 105 (2001) 301-321 ([arXiv:hep-th/0010286](https://arxiv.org/abs/hep-th/0010286))


Meanwhile [[AdS-CFT duality]] was recognized in 

* {#Maldacena97} [[Juan Maldacena]], _The Large N limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys. 2:231, 1998, [hep-th/9711200](http://arxiv.org/abs/hep-th/9711200); 
 
where a dual description of the [[worldvolume]] theory of M2-brane appears in section 3.2.  More on this is in 

* {#KlebanovTorri10} [[Igor Klebanov]], Giuseppe Torri, _M2-branes and AdS/CFT_, Int.J.Mod.Phys.A25:332-350,2010 ([arXiv:0909.1580](http://arxiv.org/abs/0909.1580))

An account of the history as of 1999 is in

* {#Duff99} [[Mike Duff]], chapter II of _[[The World in Eleven Dimensions]]: Supergravity, Supermembranes and M-theory_, IoP 1999 ([publisher](https://www.crcpress.com/The-World-in-Eleven-Dimensions-Supergravity-supermembranes-and-M-theory/Duff/9780750306720))

More recent review is in

* Georgios Linardopoulos, chapter 13 of _Classical Strings and Membranes in the AdS/CFT Correspondence_ ([pdf](http://users.uoa.gr/~glinardo/Thesis.pdf), [spire](https://inspirehep.net/record/1391031/))




 
A detailed discussion of this [[black brane]]-realization of the M2 and its relation to [[AdS-CFT]] is in 

* [[Gianguido Dall'Agata]], Davide FabbKri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl.Phys.B542:157-194, 1999 ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

The generalization of this to $\geq 1/2$ BPS sugra solutions of the form $AdS_4 \times X_7$ is due to

* {#MFFGME09} Paul de Medeiros, [[José Figueroa-O'Farrill]], [[Sunil Gadhia]], [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))

* {#MedeirosFigueroa10} Paul de Medeiros, [[José Figueroa-O'Farrill]], _Half-BPS M2-brane orbifolds_, Adv. Theor. Math. Phys. Volume 16, Number 5 (2012), 1349-1408. ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761), [Euclid](https://projecteuclid.org/euclid.atmp/1408561553))


Discussion of the history includes

* [[Mike Duff]], ([arXiv:1501.04098](http://arxiv.org/abs/1501.04098))

Other recent developments are discussed in 

* [[Paul Howe]], [[Ergin Sezgin]], _The supermembrane revisited_, ([arXiv:hep-th/0412245](http://arxiv.org/abs/hep-th/0412245))

* [[Igor Bandos]], [[Paul Townsend]], _SDiff Gauge Theory and the M2 Condensate_ ([arXiv:0808.1583](http://arxiv.org/abs/0808.1583))

* [[Jonathan Bagger]], [[Neil Lambert]], Sunil Mukhi, Constantinos Papageorgakis, _Multiple Membranes in M-theory_ ([arXiv:1203.3546](http://arxiv.org/abs/1203.3546))

* [[Nathan Berkovits]], _Towards Covariant Quantization of the Supermembrane_ ([arXiv:hep-th/0201151](http://arxiv.org/abs/hep-th/0201151))

Formulations of multiple M2-branes on top of each other are given by the _[[BLG model]]_ and the _[[ABJM model]]_. See there for more pointers. The relation of these to the above is discussed in section 3 of 

Discusson of [[boundary conditions]] in the ABJM model (for M2-branes ending on [[M5-branes]]) is in

* {#BermanThomson09} [[David Berman]], Daniel Thompson, _Membranes with a boundary_, Nucl.Phys.B820:503-533,2009 ([arXiv:0904.0241](http://arxiv.org/abs/0904.0241))

A kind of [[double dimensional reduction]] of the ABJM model to something related to [[type II superstrings]] and [[D1-branes]] is discussed in

* [[Horatiu Nastase]], Constantinos Papageorgakis, _Dimensional reduction of the ABJM model_,  JHEP 1103:094,2011 ([arXiv:1010.3808](http://arxiv.org/abs/1010.3808))

Discussion of the ABJM model in [[Horava-Witten theory]] and reducing to [[heterotic strings]] is in

* {#Lambert15} [[Neil Lambert]], _Heterotic M2-branes_ ([arXiv:1507.07931](http://arxiv.org/abs/1507.07931))


Discussion of general phenomena of [[M-branes]] in [[higher geometry]] and [[generalized cohomology]] is in 

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ (2010)

Discussion from the point of view of [[Green-Schwarz action functional]]-[[schreiber:∞-Wess-Zumino-Witten theory]] is in

* {#FSS2013} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ (2013)
 

### Dualities

The role of and the relation to [[duality in string theory]] of the membrane is discussed in the following articles.

Relation to [[T-duality]] is discussed in:

* J.G. Russo, _T-duality in M-theory and supermembranes_ ([arXiv:hep-th/9701188](http://arxiv.org/abs/hep-th/9701188))

* M.P. Garcia del Moral, J.M. Pena, A. Restuccia, _T-duality Invariance of the Supermembrane_ ([arXiv:1211.2434](http://arxiv.org/abs/1211.2434))

Relation to [[U-duality]] is discussed in:

* [[Martin Cederwall]], _M-branes on U-folds_ ([arXiv:0712.4287](http://arxiv.org/abs/0712.4287))

* M.P. Garcia del Moral, _Dualities as symmetries of the Supermembrane Theory_ ([arXiv](http://arxiv.org/abs/1211.6265))

* [pdf](http://streaming.ictp.trieste.it/preprints/P/97/044.pdf)

Discussion from the point of view of [[E11]]-[[U-duality]] and [[current algebra]] is in 

* [[Hirotaka Sugawara]], _Current Algebra Formulation of M-theory based on E11 Kac-Moody Algebra_, International Journal of Modern Physics A, Volume 32, Issue 05, 20 February 2017 ([arXiv:1701.06894](https://arxiv.org/abs/1701.06894))

* [[Shotaro Shiba]], [[Hirotaka Sugawara]], _M2- and M5-branes in E11 Current Algebra Formulation of M-theory_ ([arXiv:1709.07169](https://arxiv.org/abs/1709.07169))

[[!redirects M2-branes]]

[[!redirects M-theory membrane]]
[[!redirects M-theory membranes]]