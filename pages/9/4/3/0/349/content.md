#Idea#

A _Grothendieck topology_ on a category is a choice of morphisms in that category which are regarded as [[cover|covers]].

A category equipped with a Grothendieck topology is a [[site]].

#Definition#

+-- {: .un_defn}
###### Definition
A _Grothendieck topology_ $J$ on a category $C$ assigns to each object $c$ a collection of [[sieve|sieves]] on $c$ which are called _covering sieves_, satisfying the following axioms: 

*  If $F$ is a [[sieve]] that covers $c$ and $g: d \to c$ is any morphism, then the pullback sieve $g^* F$ covers $d$. 

* The maximal [[sieve]] $id: \hom(-, c) \hookrightarrow \hom(-, c)$ is always a covering sieve; 

* Two [[sieve|sieves]] $F, G$ of $c$ cover $c$ if and only if their intersection $F \cap G$ covers $c$. (Here the saturation condition is important.) 

* If $F$ is a sieve on $c$ such that the sieve 
    $\bigcup_d \{g: d \to c| g^* F \; covers \; d\}$
    is a covering sieve of $c$, then $F$ itself covers $c$. 
=--

The set of covering sieves of an object $c$ is denoted $J(c)$, and the first axiom guarantees that we have a functor $J: C^{op} \to Set$. 

## Comparison with Lawvere-Tierney topologies ##

There is a beautifully compact and elegant description of Grothendieck topologies by means of [[Lawvere-Tierney topology|Lawvere-Tierney topologies]]: 

Grothendieck topologies as described above are special cases: a Grothendieck topology on $C$ is equivalent to a [[Lawvere-Tierney topology]] on the presheaf topos $Set^{C^{op}}$. We proceed to unpack this equivalence. 

In the first place, we need to understand the subobject classifier in $E = Set^{C^{op}}$. But according to the definition, $\Omega$ is simply the representing object for the functor 

$$Sub: E^{op} \to Set$$ 

which takes an object $F$ of $E$ to the collection of subobjects of $F$, $Sub(F)$. In other words, $Sub(F) \cong \hom_E(F, \Omega)$. Applied to $F = \hom_C(-, c)$, we have then 

$$Sub(\hom_C(-, c)) \cong \hom_{Set^{C^{op}}}(\hom_C(-, c), \Omega) \stackrel{Yoneda}{\cong} \Omega(c)$$ 

In other words, we find that the functor $\Omega: C^{op} \to Set$ is defined by 

$$\Omega(c) = \{sieves on c\}$$ 

Next, if $J$ is a Grothendieck topology on $C$, then the collection of $J$-covering sieves on $c$ [which we denoted by $J(c)$] is a subcollection of all sieves on $c$, and so we have an inclusion 

$$J(c) \hookrightarrow \Omega(c)$$ 

and this inclusion is natural in $c$, by virtue of the first axiom on covering sieves. Thus we have a subobject

$$J \hookrightarrow \Omega$$ 

and again, by definition of subobject classifier, this subobject corresponds to a uniquely determined element 

$$j \in \hom_E(\Omega, \Omega)$$ 

which is just the Lawvere-Tierney operator $j: \Omega \to \Omega$. 

The other axioms for covering sieves translate neatly into properties of $j$. 

...

---
One reason for introducing topologies is that one wants a coequalizer $\coprod Spec (A_{ij}) \to Spec(A_i) \to X$
This doesn't exist in Aff, and the thing you get in presheaves does not behave as it should. Therefore need to take the presheaf coequalizer and sheafify it. Problem: It is not obvious which topology to take - the canonical topology is hard to get your hands on.



&lt;http://mathoverflow.net/questions/71893/cohomological-dimension-for-coarser-finer-topologies>

[de Jong on comparing topologies](http://math.columbia.edu/~dejong/wordpress/?p=1297)

There are lots of insights on Grothendieck topologies in general, and h and qfh in particular, in Voevodsky's thesis. I think Homology of schemes I is essentially an improved version of the thesis.

As pointed out by Peter, and also indicated by Voevodsky, one can think of a Grothendieck topology as something corresponding to fixing some colimits which should be preserved under the Yoneda embedding. Some explanation: Take a colimit diagram in the small cat, embed it under Yoneda, might get a new colimit, and a map from the new to the old. Localize by making these maps isomorphisms. Peter thinks: Every left exact localization should correspond to a Groth top.

See Anel factorization systems, and Lurie's discussion on localization, for two alternative ways of thinking of Groth topologies.

Remark: As seen for example in Toen, some topologies can be defined formally, while others need some real AG input.

Voevodsky: Homotopy theory of simplicial sheaves in cd topologies. Discusses two approaches to model structures on simplicial sheaves, Jardine-Joyal being very general, and Brown-Gersten more managable with better finiteness properties (finitely generated), but working only on certain sites associated to "cd-structures". Notions of complete, bounded and regular cd-structure.

See also the various pages on different types of sheaf cohomology.

See also [[Sheaf theory]] and similar entries under S.

References:

Shatz article, for cohomological dimension.

[nLab](http://ncatlab.org/nlab/show/Grothendieck+topology), see also [sieve](http://ncatlab.org/nlab/show/sieve)

&lt;http://nlab.mathforge.org/nlab/show/Grothendieck+pretopology>

&lt;http://ncatlab.org/nlab/show/Verdier+site>

&lt;http://mathoverflow.net/questions/9571/canonical-topology-on-the-category-of-schemes>

See Toen Essen talk section 4.3 and later, for the right way of defining Grothendieck tops on model categories, taking into account the model structure.

For abstract defs of flat, smooth and etale morphisms, see Toen Barcelona lectures.

Toen and Vaquie: Under Spec Z. Some notes: Idea: Relative alg geom. Think of commutative monoids in a symm monoidal cat C as models for affine schemes relative to C. If there is a reasonable symmetric monoidal functor from C to Z-modules, get a base change functor, and a notion of scheme under Spec(Z). Homotopical version of this requires C to have a model structure. Now have flat and Zariski topology. Can make sense of schemes: a functor with a Zariski covering. Stuff about toric varieties and GL. Brave new AG over the sphere spectrum, and the spectrum with one element. Digression: Flat and Zariski ok. For etale (and maybe hence Nisnevich), Peter Arndt said there might be three ways of doing it: by a lifting property, by factorization systems (Anel), or by mimicking something Deitmar does for monoids, see Peter's thesis in progress, and see also the notion of formally etale.

---


A Grothendieck topology is a standard tool for constructing cohomology theories in algebraic geometry. See [Wikipedia page](http://en.wikipedia.org/wiki/Grothendieck_topology) for basic definitions: sieves, covering families, subcanonical topology, presheaf and sheaf with values in a category with products. More serious references include Tamme: Etale cohomology, Artin lecture notes (el), and SGA4.

Grothendieck topologies are used to define various kinds of [[Sheaf cohomology]]

A morphism of topologies $T \\\\\\\\to T\\\\\\\'$ is a functor on the underlying categories which take covering families to covering families and \\\\\\\"commutes with fiber products\\\\\\\".

Here is something about the [primitive topology](http://www.math.uiuc.edu/K-theory/0214) by Walker.

de Jong on [Comparing topologies](http://math.columbia.edu/~dejong/wordpress/?p=1297)

##Examples

&lt;http://mathoverflow.net/questions/74549/a-bestiary-of-topologies-on-sch>

###The big and small Zariski site
[Wikipedia](http://en.wikipedia.org/wiki/Grothendieck_topology)

###The big and small Nisnevich site
[Wikipedia](http://en.wikipedia.org/wiki/Grothendieck_topology)

###The big and small &#233;tale site
[Wikipedia](http://en.wikipedia.org/wiki/Grothendieck_topology)

&lt;http://mathoverflow.net/questions/52404/locally-constant-sheaves-for-the-etale-topology-lack-of-intuition-about-etale-l>

###The separated &#233;tale site
Objects are required to be separated, &#233;tale, and of finite type, rather than just the last two. Cohomology is canonically IMic to &#233;tale cohomology, but and advantage is that if $X$ is separated, Noetherian and regular, and $V \\\\\\\\to X$ is an object, then $V$ is also separated, Noetherian and regular. Ref: Jardine, Generalized &#233;tale cohomology, p. 278.

###Lisse-etale
&lt;http://mathoverflow.net/questions/53563/why-is-lack-of-functoriality-of-the-lisse-etale-topology-specific-to-the-lisse-et>

###The big and small fppf site
[Wikipedia](http://en.wikipedia.org/wiki/Flat_topology)

###The big and small fpqc site
[Wikipedia](http://en.wikipedia.org/wiki/Flat_topology)

&lt;http://mathoverflow.net/questions/39211/open-faithfully-flat-morphisms-are-fpqc>

###The qfh topology


###The h topology

###Geisser\\\\\\\'s eh topology
Kahn in K-theory handbook says something about base change thm between &#233;tale and cdh topology, see page 384 bottom.

###The cdh topology
We want to talk about singular schemes which admit resolutions by smooth schemes. For this purpose we introduce the cdh topology on $Sch/k$ (schemes of finite type over $k$). This is the minimal Grothendieck topology for which Nisnevich coverings are coverings, and also proper surjective morphisms of the following type: $W \\\\\\\\coprod U_1 \\\\\\\\to U$ where $U_1 \\\\\\\\to U$ is a closed embedding and $p^{-1}(U-U_1) \\\\\\\\to (U-U_1)$ is an isomorphism.

See also [[cdh-cohomology]]

###Examples in FGA?

###The canonical topology
On any category (with products, I guess), we can define the canonical topology, by taking as coverings the collection of all families $\\\\\\\\{U_i \\\\\\\\to U \\\\\\\\}$ of universal [[Effective epimorphism|effective epimorphisms]]. On this topology, every presheaf of sets is a sheaf, and it is the finest topology with this property.

###The perfect site
See Milne: Arithmetic duality theorems

###The smooth site
Milne again.

###The positive topology
See Schmidt

###The canonical topology
Def by all representables being sheaves?

###The alteration topology with variants
See Gabber\\\\\\\'s abstract from IHES talk 2009

###The cohomological descent topology
See Hodge III

###Syntomic topology
See [[Syntomic cohomology]]

###The Zink site
See &lt;http://www.ams.org/mathscinet-getitem?mr=1803955>

###More Voevodsky stuff
Thesis, p 35: The p-topology and f-topology, coverings given by proper (resp finite) surjective families of morphisms.

nLab page on [[nlab:Grothendieck topology]]
