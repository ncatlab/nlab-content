
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

A quasitopos is a particular kind of [[category]] that has properties similar to that of a [[topos]], but is not quite a [[topos]]. A major difference is that it need not be [[balanced category|balanced]]: a [[morphism]] that is both [[monomorphism|monic]] and [[epimorphism|epic]] is not necessarily invertible. A quasitopos that is balanced is a topos.

Instead of the usual [[subobject classifier]], it has a classifier only for *[[strong monomorphism|strong]]* [[subobject]]s. It satisfies the uniqueness, but not the existence, part of the sheaf axioms ([[Elephant]] A2.6).

Note that some of the literature definitions use the notion of a [[regular monomorphism]].  Since every regular monomorphism is as strong one, this article only uses  [[strong monomorphism]].

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

Equivalently, in addition to finite limits and colimits and local cartesian closure, one may ask only that there exists a classifier $t\colon 1\to\Omega$ as above for *some* class $\mathcal{M}$ of [[monomorphisms]] which contains the [[regular monomorphisms]] and is closed under composition and pullback.  From this one can show that every morphism factors as an epimorphism followed by a regular monomorphism (see [Wyler, proposition 12.5](#Wyler)).  It then follows that every strong monomorphism is regular, and therefore $\mathcal{M}$ is precisely the class of strong monomorphisms.

=--


+-- {: .un_prop}
###### Definition/Proposition

Let $C$ be a category with two [[Grothendieck topologies]] $J$ and $K$ such that $J\subseteq K$.  The [[full subcategory]] $BiSep(C,J,K) \hookrightarrow PSh(C)$ of the [[category of presheaves]] over $C$ consisting of the [[sheaves]] for $J$ that are also [[separated presheaves|separated]] for $K$ is a quasitopos.  A category equivalent to such a category is called a **Grothendieck quasitopos**, by analogy with the notion of [[Grothendieck topos]].

=--

In particular, this includes the category of separated presheaves on a given site (if we take $J$ to be the trivial topology), and also includes all Grothendieck toposes (if we take $K=J$). 

Equivalently, a Grothendieck quasitopos is a category of the form $Sep_k(\mathbf{E})$, the category of $k$-separated objects for a [[Lawvere-Tierney topology]] $k$ on a Grothendieck topos $\mathbf{E}$. 

## Properties

### General

+-- {: .num_lemma #PushoutOfStrongMonos}
###### Lemma
**(pushout of strong monos)

In a quasitopos the [[pushout]] of a [[strong monomorphism]] is again a strong mono, and the resulting square is also a [[pullback]] square.

=--

This appears as [Elephant, Lemma A.2.6.2](#Elephant), using the synonym _cocover_ for _strong monomorphism_. Since a [[topos]] is a quasitopos in which all monomorphisms are strong, this implies that the pushout of a mono in a topos is again a mono and that the resulting square is a pullback. Together with the fact that colimits are universal in a topos, this implies that a topos is an [[adhesive category]]. 

+-- {: .num_corollary}
###### Corollary

A quasitopos that is also a [[balanced category]] is a [[topos]].

=--

This is [Elephant, corollary 2.6.3](#Elephant).


+-- {: .num_lemma}
###### Lemma

A quasitopos has [[disjoint coproduct]]s precisely if the unique morphism $\emptyset \to *$ from the [[initial object]] to the [[terminal object]] is a [[strong monomorphism]].

=--

This is [Elephant, corollary 2.6.5](#Elephant).


+-- {: .num_defn}
###### Definition


An [[object]] $C$ in a quasitopos is called **coarse** if for every [[bimorphism|monic epic]] morphism $f : A \to B$ every morphism $A \to C$ factors uniquely through $f$.

=--

So the coarse objects are those that see monic epic morphisms as [[isomorphism]]s, hence that do not see the failure of the quasitopos to be a [[balanced category]].

+-- {: .num_prop}
###### Proposition


In a quasitopos $\mathcal{E}$ the [[full subcategory]]
on coarse objects is a [[topos]] and a [[reflective subcategory]]

$$
  Coarse(\mathcal{E}) \stackrel{\leftarrow}{\hookrightarrow} \mathcal{E}
  \,.
$$


=--

This is [Elephant, prop 2.6.12](#Elephant).

+-- {: .num_lemma}
###### Lemma

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


### Internal logic

Like a topos, a quasitopos has an [[internal logic]], for which the usual choice is to represent propositions by *strong* subobjects.  The resulting internal logic fails to satisfy the [[function comprehension principle]], forcing one to distinguish between [[functions]] and [[anafunctions]].


## Examples ##

* Any (elementary) [[topos]] is a quasitopos.  The first two properties are known, and in a topos every monomorphism is strong, so the ordinary subobject classifier works.

  Conversely, if a quasitopos is also a [[balanced category]], then it is also a topos. 

* Any [[Heyting algebra]] is a quasitopos.  This is in notable contrast to the case of topoi, since no nontrivial poset is a topos.  The crucial distinction is that every morphism in a poset is both monic and epic, but only the identities are strong monic or strong epic.

* The category of [[pseudotopological spaces]] is a quasitopos, as is the category of [[subsequential spaces]].  (The latter is Grothendieck, but not the former.)  The category of [[topological spaces]] fails only to be locally cartesian closed.  In such "topological" quasitopoi, the strong monics are the "subspace inclusions" (i.e. those monics whose source has the topology induced from the target), and the strong-subobject classifier is the two-point space with the indiscrete topology.  (In particular, we cannot demand any sort of [[separation axiom]] and still have a quasitopos.)

* The category of [[marked simplicial set]]s.

* A category of [[concrete sheaves]] on a [[concrete site]] is a Grothendieck quasitopos. See [[local topos]]. 

  This includes the following examples:

  * The category of [[simplicial complex|simplicial complexes]].

  * The category of [[diffeological space|diffeological spaces]]. 

* {#exampsep} The following examples are categories of separated presheaves for the $\neg\neg$-topology on various presheaf toposes: 

  * {#mono} The category [[M-category#def|Mono]] of [[monomorphisms]] between sets (as presheaves on the [[interval category]] - the [[Sierpinski topos]]).  

  * {#endorel} The category [[relation#endorel|EndoRel or Bin]] of sets equipped with a [[relation]] (as presheaves on [[Quiv]]
    $$G_1 = (0 \stackrel{\overset{s}{\to}}{\underset{t}{\to}} 1),$$ 
    a truncation of the [[globular category]]).  

  * {#endoref} The category of sets equipped with a reflexive relation (as presheaves on a truncated reflexive globular category). 

  * {#endosym} The category of sets equipped with a symmetric relation (as presheaves on the full subcategory of finite sets and injections consisting of just the objects $1$, $2$). 

  * {#endorefsym} The category of sets equipped with a reflexive symmetric relation (as presheaves on the full subcategory of finite sets consisting of just the objects $1$, $2$). See [[category of simple graphs]]. 


* The category of [[bornological set|bornological sets]]. 

* The category of assemblies of a [[partial combinatory algebra]]. 

* The category of Spanier's [[quasi-topological space|quasi-topological spaces]], the category of concrete sheaves on the site consisting of compact Hausdorff spaces with the finite covering topology. See [Dubuc-Espanol](#DE). 

## Related concept

* **quasitopos**

* [[(∞,1)-quasitopos]]


## References ## 

Original articles include

* [[Jacques Penon]], _Quasi-topos_ , C.R. Acad. Sci. Paris **276** S&#233;rie A (1973) pp.237&#8211;240. ([gallica](http://gallica.bnf.fr/ark:/12148/bpt6k6217213f/f251.image))

* [[Jacques Penon]], _Sur le quasi-topos_ , Cahiers Top. G&#233;om. Diff. 18 (1977), 181&#8211;218.

Textbook accounts:

* {#Wyler} Oswald Wyler, _Lecture Notes on Topoi and Quasitopoi_ , World Scientific Singapore 1991.

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_, Oxford UP 2002.
{#Elephant} (section A2.6)

* [[Jiří Adámek]], [[Horst Herrlich]], [[George Strecker]], *Abstract and Concrete Categories*, Wiley 1990, reprinted as: Reprints in Theory and Applications of Categories, No. 17 (2006) pp. 1-507 ([tac:tr17](http://www.tac.mta.ca/tac/reprints/articles/17/tr17abs.html))

Quasi-toposes of [[concrete sheaves]] are considered in

* [[Eduardo Dubuc]], _Concrete quasitopoi_ , Lecture Notes in Math. 753 (1979), 239&#8211;254

* {#DE} [[Eduardo Dubuc]], [[Luis Español]], _Quasitopoi over a base category_  ([arXiv:math.CT/0612727](http://arxiv.org/abs/math.CT/0612727))


A review is in

* [[John Baez]], [[Alex Hoffnung]], _Convenient categories of smooth spaces_, to appear, Trans. AMS, ([arXiv](http://arxiv.org/abs/0807.1704))

More generally, quasi-[[sheaf toposes]] are discussed in

* [[Richard Garner]], [[Stephen Lack]], _Grothendieck quasitoposes_ , arXiv:1106.5331 (2012). ([abstract](http://arxiv.org/abs/1106.5331))
 {#GarnerLack}



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

