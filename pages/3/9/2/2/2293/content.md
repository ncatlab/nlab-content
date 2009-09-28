<div class="rightHandSide toc">
[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]
</div>

#Contents#

* automatic table of conteents goes here
{:toc}

+-- {: .query}

[[Zoran Skoda]]: I worked very hard on parts of this entry and the bibliography. It was a TEXT, planned and created with this in mind. Now it has very arbitrary table of contents on the right hand side. Why not having simple one single LINK to the higher geometry contents page and who subscribes to it can follow it. If something is created as a TEXT it should be respected and not made into web-noise with content free table of links or adevrtisements. I support creating tabels of links and myself have done several of them. But if some page is already created and matured as a TEXT and hours are put into this, I do not like hijacking it for mixing it with table of contents. Lets have just link to toc, who likes it can folow it, and the look and size of the page does not change. Specially for printing. If I do a contribution in a format which I like, then up to additions, enw paragraphs, minor chanes, comments, linguistics corrections and alike by improvers and intelligent colleagues, I expect it to stay with some form-preserving features as an asset to a future, as a piece of work which I will find here after 30 years in traceably similar form. If you guys plan to change to nlabXP and nlabVista and so on in future, unlike LaTeX which was having similar ouput in 1990 as it has today, then it is not my choice and it makes me unhappy.

=--


# Idea #

The term __derived algebraic geometry__ is used in two closely related but logically different notions: 

1. as the part of the geometry of schemes captured cohomologically (by the [[derived category]] of [[coherent seaf|coherent sheaves]]), which presents the kind of data very close to the interests of the classical Italian school and 

1. as the derived [[moduli space]]s, which extend or replace the usual [[moduli space]]s. 

## derived categories of sheaves on a space ##

In the early works of the Russian school (Kapranov, Bondal, Orlov, [[Kontsevich]]) it meant, replacing a [[variety]] by the [[derived category]] of [[coherent sheaves]] (or [[quasicoherent sheaves]] on that variety, or [[dg-category]] (or [[A-infinity category]]) [[enhanced triangulated category|enhancements]] thereof. There are also [[noncommutative algebraic geometry|noncommutative deformations]] of such derived categories and analogues like the categories corresponding to the so-called [[Landau-Ginzburg model]]s. Therefore **noncommutative derived geometry** (and even noncommutative motives). 

Notice that the [[derived category]] of coherent sheaves on a variety does _not_ remember all the structure of the original variety hence derived geometry loses often some information (sometimes not); thus derived algebraic geometry is sometimes easier than nonderived. 

## derived noncommutative geometry: derived structure sheaves ##

On the other hand there is a closely related effort to include sheaves of commutative [[dg-algebra]]s as [[structure sheaf|structure sheaves]] (dg-schemes of Kapranov, Ciocan-Fontaine, and [[Kontsevich]]) and more generally to allow [[higher category theory|higher categorical]] [[structured (infinity,1)-topos|structured spaces]] of algebraic type, generalizing [[algebraic stack]]s, [[scheme]]s and [[algebraic space]]s. This is a [[higher category theory|higher categorical]] version of [[algebraic geometry]]: its [[vertical categorification]] is also called derived algebraic geometry. Notice that in that sense, there is no loss of information in a passage from a scheme to its natural extension to a derived scheme. 

This second school has been, after the original ideas of Deligne, Drinfel'd and Kontsevich advanced by [[Carlos Simpson]] (who introduced also basic prerequisited like algebraic and geometric [[infinity-stack|n-stack]]s), and later [[Bertrand Toen]] and coworkers. One of the main motivations for both variants of derived alegbraic geometry is to develop a satisfactory deformation theory and on its basis the theory of [[moduli stack]]s in [[algebraic geometry]] beyond the few examples which work in classical language of algebraic spaces and algebraic 1-stacks. 

Sometimes, but not always getting rid of limitations coming from 1-categorical truncations removes nonsmoothness, but the expectations in that directions (hidden smoothness principle) failed in generality expected at the beginning. The construction of the derived moduli spaces relies, similarly to the classical moduli theory in algebraic geometry, on the infinitesimal case -- the [[deformation theory]] (cf. [[cotangent complex]]).

## "derived" in the second sense versus "$\infty$-"

The adjective "derived" means pretty much the same as the "$\infty$-" in [[∞-category]]. It stems from the use of "derived" as in [[derived category]] and [[derived functor]]. But incidentally, derived algebraic geometry is honestly [[higher category theory|higher catgeorical]], whereas derived categories and derived functors are really more like 1-categorical shadows of higher categorical structures, as described in detail at [[homotopy category]].

There is no really systematic rule to the use of the word "derived" here. For instance [[derived stack]] has become the standard term for the general version of the notion of [[∞-stack]], but [[Higher Topos Theory]] is not called "derived topos theory".

> [[Urs Schreiber]]: personally I'd think that "derived algebraic geometry" is therefore a misnomer. But who am I to stop that train? :-)
_Zoran_: this paragraph is entirely wrong, hence your repenting it. There are two generalizations needed to come from schemes to algebraic geometry: deriving on the left and deriving on the right. The deriving on the left corresponds to take higher algebraic stacks,say in terms of fibrant objects in certain model category of simplicial presheaves. The deriving on the left means taking the fibre products of schemes in certain derived way as well (amounting to taking the left derived functors of the tensor product on the algebra level), but the model structures here take the flxibility of dg algebras in the source of the simplicial presheaf picture; this takes care of nontransersality. Thus derived stack is not only higher stack, it is also derived on the other side. 

 
## relation to higher algebra ##

Where ordinary [[algebraic geometry]] uses [[algebra]] to describe [[geometry]], derived algebraic geometry uses [[higher algebra]]. Where ordinary algebraic geometry uses [[scheme]]s modeled on [[commutative ring]]s, derived algebraic geometry uses [[structured (∞,1)-topos]]es modeled on [[E-∞ ring]]s .


#Definitions#

## derived noncommutative geometry: stable $(\infty,1)$-categories ##

> details to be inserted here and harmonized with [[derived noncommutative geometry]]:

> Basic idea is to _identify_ [[triangulated category|triangulated]] [[dg-category|dg-categories]], [[A-infinity category|categories]] and other models for [[stable (∞,1)-category|stable (∞,1)-categories]] with generalized "derived" spaces and to describe morphism between them in terms of [[geometric morphism]]s between these categories. It might be noteworthy that a (accessible) stable $(\infty,1)$-category is much like a (Grothendieck) [[(∞,1)-topos]]. See the definition below.

## structured $(\infty,1)$-toposes ##

In

* [[Jacob Lurie]], [[Structured Spaces]] 

a definition of [[derived algebraic scheme]] and [[derived Deligne-Mumford stack]] is given in the wider context of [[generalized scheme]]s realized as locally affine [[structured (∞,1)-topos]]es.

See these links for more details.

+-- {: .num_remark}
###### Remark (derived scheme are $(\infty,1)$-toposes)

This definition is based on the observation that it is a deficiency of the ordinary defintion of [[scheme]] to demand that underlying a scheme is a [[topological space]] and that a better definition is obtained by demanding it to have an underlying [[locale]]. But a [[locale]] is a [[0-topos]]. This motivates then the definition of a [[generalized scheme]] as a (locally affine, [[structured (infinity,1)-topos|structured]]) [[(∞,1)-topos]]. 

=--


# Examples #

##Homological mirror symmetry##

Homological mirror symmetry is one of the main motivations and statements of the derived algebraic geometry of the first kind.

* Maxim Kontsevich, _Homological algebra of mirror symmetry_,   Proceedings of the International Congress of Mathematicians, Vol. 1, 2 (Z&#252;rich, 1994),  120--139, Birkh&#228;user, Basel, 1995.

* Maxim Kontsevich, Yan Soibelman, _Homological mirror symmetry and torus fibrations_, in Symplectic geometry and mirror symmetry (Seoul, 2000),  203--263, World Sci. Publ., River Edge, NJ, 2001. 

## elliptic cohomology ##

More recent big success of derived algebraic geometry of the second kind was [[elliptic cohomology]] and the construction and study of the [[tmf]] [[spectrum]] as a certain derived moduli  "of derived elliptic curves". This construction of moduli space is based on earlier Lurie result (not available in full) in which Lurie has proved an analogue of the Artin's representability theorem from the algebraic geometry of Grothendieck school. For more on that see

* [[Jacob Lurie]], [[A Survey of Elliptic Cohomology]]

# References #

A prediction of derived moduli spaces is spelled out (in a bit different language) in

* M. Kontsevich, _Enumeration of rational curves via torus actions_. The moduli space of curves (Texel Island, 1994), 335--368, Progr. Math. __129__, Birkh&#228;user 1995. MR1363062 (97d:14077), [hep-th/9405035](http://arxiv.org/abs/hep-th/9405035).

An early variant, the _dg-schemes), were used to construct some derived moduli spaces for the first time in the works of Kapranov and Ciocan-Fontanine:

* M. Kapranov, _Injective resolutions of BG and derived moduli spaces of local systems_,  J. Pure Appl. Algebra  155  (2001),  no. 2-3, 167--179; [math/alg-geom/9710027](http://arxiv.org/abs/alg-geom/9710027), MR1801413 (2002b:18017)

* I. Ciocan-Fontanine, M. Kapranov, _Derived Hilbert scheme_ [math.AG/0005155](http://arxiv.org/abs/math/0005155), _Derived Quot scheme_, [math.AG/9905174](http://arxiv.org/abs/math/9905174)

A survey of derived category apsect of the algebraic geometry and related physics (mirror symmetry, Landau-Ginzburg models) is

* A. N. Kapustin, D. O. Orlov, _Lectures on mirror symmetry, derived categories, and D-branes_ (Russian. Russian summary) Uspekhi Mat. Nauk 59 (2004), no. 5(359), 101--134; translation in
Russian Math. Surveys 59 (2004), no. 5, 907--940 

A major case when derived geometry in the first sense gives full information is given by a reconstruction theorem of Bondal-Orlov:

* A. I. Bondal, D. O. Orlov, _Reconstruction of a variety from the derived category and groups of autoequivalences_, Compos. Math. 125 (2001), 327&#8211;344 [doi:10.1023/A:1002470302976](http://dx.doi.org/10.1023/A:1002470302976)

* A. I. Bondal, D. O. Orlov, "Derived categories of coherent sheaves", Proc. Internat. Congress of Mathematicians (Beijing, 2002)

The higher stacks and algebraic stacks were pioneered by ideas of Simpson's school. Here is one of the first successes, used later by Toen et al.:

* Andr&#233; Hirschowitz, Carlos Simpson, _Descente pour les n-champs (Descent for n-stacks)_, [math/9807049](http://arxiv.org/abs/math/9807049)

Then the major systematic work is

* Bertrand To&#235;n, Gabriele Vezzosi, _From HAG to DAG: derived moduli stacks_, in Axiomatic, enriched and motivic homotopy theory, 173--216,
NATO Sci. Ser. II Math. Phys. Chem., 131, Kluwer Acad. Publ., Dordrecht, 2004, [math.AG/0210407](http://arxiv.org/abs/math/0210407).

The theory of derived algebraic geometry in the second sense is given yet another general framework in 

* [[Jacob Lurie]], _[[structured (∞,1)-topos|Structured Spaces]] 

which merges the structural theory developed in

* [[Jacob Lurie]], [[Higher Topos Theory]]


with the theory developed in

* [[Jacob Lurie]], _Noncommutative algebra_, _Commutative algebra_ (see [[higher algebra]]).
 
A part of (derived) algebraic geometry in the framework of $A_\infty$-category can be found in

* L.Katzarkov, M.Kontsevich, T.Pantev, _Hodge theoretic aspects of mirror symmetry_ [arxiv:0806.0107](http://arxiv.org/abs/0806.0107)

and a bit earlier treatise on formal (infinitesimal in the sense of [[formal schemes]]) aspect as used in the [[deformation theory]] is in

* M. Kontsevich, Y. Soibelman, _Notes on A-infinity algebras, A-infinity categories and non-commutative geometry. I_, [math.AG/0606241](http://arxiv.org/abs/math/0606241)

This formal aspect is supposedly related to the infinitesimal picture of the moduli stacks considered by Toen et al. and it generalizes more classical approaches to the [[deformation theory]] like Illusie's [[cotangent complex ]] (cf. also smooth obstruction theory of Fantechi-Behrend). See also motivic aspects in

* Maxim Kontsevich, Yan Soibelman, _Stability structures, motivic Donaldson-Thomas invariants and cluster transformations_, [arXiv:0811.2435](http://arxiv.org/abs/0811.2435)

The relations to tropical and symplectic geometry are in recent Kontsevich's talk at 2009 Arbeitstagung:

* M. Kontsevich, Mathematische Arbeitstagung 2009, _Symplectic geometry of homological algebra_, preprint MPIM2009-40a, [pdf](http://www.mpim-bonn.mpg.de/preprints/send?bid=4024)