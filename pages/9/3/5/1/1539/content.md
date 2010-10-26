
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A quasitopos is a particular kind of [[category]] that has properties similar to that of a [[topos]], but is not quite a [[topos]].  

Instead of the usual [[subobject classifier]], it has a classifier only for *[[strong monomorphism|strong]]* [[subobject]]s.

## Definition

+-- {: .un_defn}
###### Definition

A **quasitopos** is a [[finitely complete category|finitely complete]], [[finitely cocomplete category|finitely cocomplete]], [[locally cartesian closed category]] $E$ in which there exists an [[object]] $\Omega$ that classifies [[strong monomorphism|strong monomorphisms]]. 

=--

In particular, this means 

* Every finite [[limit]] and [[colimit]] exists;
* For each morphism $f: A \to B$, the [[base change|pullback functor]] between [[over category|slice quasitoposes]], 
$$f^*: E/B \to E/A,$$
admits a [[adjoint functor|right adjoint]]; 
* There is a map $t: 1 \to \Omega$ such that every [[strong monomorphism]] $i: A \to X$ occurs as the [[pullback]] of $t$ along some unique morphism $\chi_i: X \to \Omega$: 
$$\array{
A & \to & 1\\
i \downarrow & & \downarrow t\\
X & \overset{\chi_i}{\to} & \Omega
}$$

The object $\Omega$ above is sometimes called a **strong-subobject classifier**, since it classifies strong subobjects, but also sometimes called a **weak subobject classifier**, since it satisfies a weaker property than an ordinary [[subobject classifier]].

+-- {: .un_remark}
###### Remark

Equivalently, in addition to finite limits and colimits and local cartesian closure, one may ask only that there exists a classifier $t\colon 1\to\Omega$ as above for *some* class $\mathcal{M}$ of [[monomorphisms]] which contains the [[regular monomorphisms]] and is closed under composition and pullback.  It then follows that $\mathcal{M}$ is precisely the class of strong monics, and also equal to the class of regular monics.

=--


+-- {: .un_prop}
###### Definition/Proposition


Every [[full subcategory]] $SepPSh(C) \hookrightarrow PSh(C)$ of a [[category of presheaves]] over a [[site]] $C$ on the [[separated presheaves]]  is a quasitopos.  A category equivalent to such a separated presheaf category is called a **Grothendieck quasitopos**, by analogy with the notion of [[Grothendieck topos]].  

=--

## Properties

### General

+-- {: .un_lemma}
###### Lemma

In a quasitopos the [[pushout]] of a [[strong monomorphism]] is again a strong mono, and the resulting square is also a [[pullback]] square.

=--

This appears as [Elephant, lemma 2.6.2](#Elephant).

+-- {: .un_corollary}
###### Corollary

A quasitopos that is also a [[balanced category]] is a [[topos]].

=--

This is [Elephant, corollary 2.6.3](#Elephant).


+-- {: .un_lemma}
###### Lemma

A quasitopos has [[disjoint coproduct]]s precisely if the unique morphism $\emptyset \to *$ from the [[initial object]] to the [[terminal object]] is a [[strong monomorphism]].

=--

This is [Elephant, corollary 2.6.5](#Elephant).


+-- {: .un_def}
###### Definition


An [[object]] $C$ in a quasitopos is called **coarse** if for every [[bimorphism|monic epic]] morphism $f : A \to B$ every morphism $A \to C$ factors uniquely through $f$.

=--

So the coarse objects are those that see monic epic morphisms as [[isomorphism]]s, hence that do onot see the failure of the quasitopos to be a [[balanced category]].

+-- {: .un_prop}
###### Proposition


In a quasitopos $\mathcal{E}$ the [[full subcategory]]
on coarse objects is a [[topos]] and a [[reflective subcategory]]

$$
  Coarse(\mathcal{E}) \stackrel{\leftarrow}{\hookrightarrow} \mathcal{E}
  \,.
$$


=--

This is [Elephant, prop 2.6.12](#Elephant).

+-- {: .un_lemma}
###### Observation

If $\mathcal{E} \simeq SepPSh(C)$ is a Grothendieck quasitopos of [[separated presheaves]] on a [[site]] $C$, then $Coarse(\mathcal{E}) \simeq Sh(C)$ is the [[sheaf topos]] on $C$.

=--

This is in [Elephant, section A4.4](#Elephant).


### Characterization

There is a [[Giraud theorem]] characterizing Grothendieck quasitoposes:

+-- {: .un_theorem}
###### Theorem

Grothendieck quasitoposes are those quasitoposes which are [[locally small category|locally small]], [[cocomplete category|cocomplete]], and have a [[generating set]], or equivalently as the [[locally presentable categories]] which are locally cartesian closed and in which every *strong* [[congruence]] has a [[effective quotient]].

=--

see C2.2.13 of the ([Elephant](#Elephant))

### Extensivity and exactness

A topos is always [[extensive category|extensive]] and [[exact category|exact]], but this is not the case for quasitopoi.

A quasitopos is a [[coherent category]], since it has finite colimits which are stable under pullback (since it is locally cartesian closed), and so in particular its initial object is [[strict initial object|strict]], and it has finite coproducts which are pullback-stable, but they need not be disjoint: for objects $A$ and $B$, in the pullback
$$\array{P & \overset{}{\to} & B\\
  \downarrow && \downarrow\\
  A & \underset{}{\to} & A+B}$$
the object $P$ need not be initial.  This is easy to see from the fact that any Heyting category is a quasitopos, since then $A+B$ is the join $A\vee B$, and so the pullback is the meet $A\wedge B$, which is not in general the bottom element.

It is true, however, that such a $P$ is always a *quotient* of the initial object, i.e. the unique map $0\to P$ is epic.  If the map $0\to 1$ is strong monic, as it is in the "topological" examples, then $0$ can have no proper epimorphic images, and so coproducts are disjoint.  The converse also holds, since if coproducts are disjoint then $0\to 1$ is an equalizer of the two injections $1\rightrightarrows 1+1$.  A quasitopos with this property is sometimes called **solid**.

More generally, in any quasitopos $E$, we can factor $0\to 1$ into an epic followed by a strong monic, $0\to \bar{0} \to 1$.  One can prove that then the [[slice category]] $E/\bar{0}$ is a Heyting algebra (i.e. a posetal quasitopos), while the [[co-slice category]] $\bar{0}/E$ is a solid quasitopos, and moreover $E$ itself is recoverable via [[Artin gluing]] from a particular functor $E/\bar{0} \to \bar{0}/E$.  Thus, to a certain extent, the only interest in the theory of quasitoposes, above and beyond the theory of Heyting algebras, is in the solid ones.

By contrast, if a solid quasitopos is additionally [[exact category|exact]], and hence a [[pretopos]], then in particular it is [[balanced category|balanced]], which implies that it is in fact a topos.  One can prove, however, that a quasitopos is always *quasi-exact*, meaning that every *strong* [[congruence]] has an [[effective quotient]].


## Examples ##

* Any (elementary) [[topos]] is a quasitopos.  The first two properties are known, and in a topos every monomorphism is strong, so the ordinary subobject classifier works.

  Conversely, if a quasitopos is also a [[balanced category]], then it is also a topos. 

* Any [[Heyting algebra]] is a quasitopos.  This is in notable contrast to the case of topoi, since no nontrivial poset is a topos.  The crucial distinction is that every morphism in a poset is both monic and epic, but only the identities are strong monic or strong epic.

* The category of [[pseudotopological spaces]] is a quasitopos, as is the category of [[subsequential spaces]].  (The latter is Grothendieck, but not the former.)  The category of [[topological spaces]] fails only to be locally cartesian closed.  In such "topological" quasitopoi, the strong monics are the "subspace inclusions" (i.e. those monics whose source has the topology induced from the target), and the strong-subobject classifier is the two-point space with the indiscrete topology.  (In particular, we cannot demand any sort of [[separation axiom]] and still have a quasitopos.)

* The category of [[simplicial complex]]es is a quasitopos.

* The category of [[diffeological space]]s is a quasitopos.

* These are special cases of the general result: the category of [[concrete sheaves]] on a [[concrete site]] is a Grothendieck quasitopos. See [[local topos]].


## Related concept

* **quasitopos**

* [[(∞,1)-quasitopos]]


## References ## 

Original articles include

* J. Penon, _Quasi-topos_ , C.R. Acad. Sci. Paris, S&#233;r. A 276 (1973), 237&#8211;240.

* J. Penon, _Sur le quasi-topos_ , Cahiers Top. G&#233;om. Diff. 18 (1977), 181&#8211;218.

Standard textbook references are

*  Oswald Wyler, _Lecture Notes on Topoi and Quasitopoi_, World Scientific, 1991. 


* [[Peter Johnstone]], _[[Sketches of an Elephant]]_, 
{#Elephant}

Here quasitoposes are introduced in A2.6.

Quasi-toposes of [[concrete sheaves]] are considered in

* [[Eduardo Dubuc]], _Concrete quasitopoi_ , Lecture Notes in Math. 753 (1979), 239&#8211;254

* [[Eduardo Dubuc]], L. Espanol, _Quasitopoi over a base category_  ([arXiv:math.CT/0612727](http://arxiv.org/abs/math.CT/0612727))

A review is in

* [[John Baez]], [[Alex Hoffnung]], _Convenient categories of smooth spaces_, to appear, Trans. AMS, ([arXiv](http://arxiv.org/abs/0807.1704))


[[!redirects quasitopoi]]
[[!redirects quasitoposes]]
[[!redirects quasi-topos]]
[[!redirects quasi-topoi]]
[[!redirects quasi-toposes]]
[[!redirects quasi-exact category]]
[[!redirects strong-subobject classifier]]
[[!redirects weak subobject classifier]]
[[!redirects Grothendieck quasitopos]]
[[!redirects Grothendieck quasitoposes]]
[[!redirects Grothendieck quasitopoi]]

