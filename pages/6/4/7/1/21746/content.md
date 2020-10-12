
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Homotopy Theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

[[!redirects Natural homotopy]]
[[!redirects Natural Homotopy]]

#Contents#
* table of contents
{:toc}

##Idea

Viewing [[topos|toposes]] as generalized spaces, **natural homotopy** is an [[equivalence relation]] between [[geometric morphism|geometric morphisms]] generalizing the [[homotopy|homotopy relation]] between [[continuous map|continuous maps]].

This relation is "natural" in the metaphorical sense of being the most "basic" such relation and in the metonymical sense of being defined via [[natural transformation|natural transformations]].

The correspondance between [[geometric theory|geometric theories]] and (classifying) [[Grothendieck topos|Grothendieck toposes]] then induces an [[equivalence relation]] between theories finer than [[Morita equivalence]] that affords to define "homotopy theoretical" concepts for [[logic]], e.g. contractability of a [[theory]].

## Definition

+-- {: .num_defn }
###### Definition

Given two [[Grothendieck toposes]] $\mathcal{E},\mathcal{F}$, let $[\mathcal{E},\mathcal{F}]$ denote the class of [[connected category|connected components]] of their [[hom-category]] $Hom(\mathcal{E},\mathcal{F})$ in the [[2-category]] $GrTop$. Two [[geometric morphism|geometric morphisms]] $f,g:\mathcal{E}\to\mathcal{F}$ are called _naturally homotopic_ , denoted $f\sim g$, if $[f]=[g]$, or in other words, if there exists a zigzag of [[natural transformation|natural transformations]] $f^*\leftarrow\cdot\rightarrow\cdot \dots\cdot\leftarrow\cdot\rightarrow g^*$.

=--

**Remark.**
Under the identification $Hom(\mathcal{E},Set(\mathbb{T}))\cong \mathbb{T}-Mod(\mathcal{E})$ natural homotopy corresponds to an equivalence relation $\sim$ on $\mathbb{T}$-models in $\mathcal{E}$ given by zigzags of model homomorphisms.

## Properties and some homotopic concepts

Using the Godement calculus of [[natural transformation|natural transformations]] an induction over the number of zigzags $\cdot\leftarrow\cdot\rightarrow\cdot$ shows that $f\sim f'$ implies $h\circ f\circ k\sim h\circ f'\circ k$. From this it follows that for composable geometric morphisms $f\sim f'$, $g\sim g'$ implies $f\circ g\sim f'\circ g'$.

In particular, one can define a (partial) composition $[f]\circ[g]$ on natural homotopy equivalence classes via the composition of the representatives $[f\circ g]$. In this way, one obtains a [[homotopy category]] $\mathbf{Ho}(GrTop)$ with objects the Grothendieck toposes and morphisms the natural homotopy equivalence classes of geometric morphisms.

+-- {: .num_defn }
###### Definition
A geometric morphism $f:\mathcal{E}\to\mathcal{F}$ is called a _(natural) homotopy equivalence_ if there exists a geometric morphism $g:\mathcal{F}\to\mathcal{E}$ such that $f\circ g\sim id_{\mathcal{F}}$ and $g\circ f\sim id_{\mathcal{E}}$. In that case, $\mathcal{F}$ and $\mathcal{E}$ are said to be of the same _(natural) homotopy type_.
=--

Homotopy equivalences are closed under composition hence "being of the same homotopy type" is an equivalence relation on toposes. Toposes having the same homotopy type as $Set$, the "point" in $GrTop$, deserve to be singled out:

+-- {: .num_defn }
###### Definition
A Grothendieck topos $Set(\mathbb{T})\;$, respectively the [[geometric theory]] $\mathbb{T}$ it [[classifying topos|classifies]], is called _(naturally) contractible_ , if there exists a "constant" geometric morphism $c:Set(\mathbb{T})\to Set(\mathbb{T})$ i.e. one factoring through $Set$ as $Set(\mathbb{T})\overset{!}{\to}Set\overset{\bar{c}}{\to}Set(\mathbb{T})\;$, such that $c\sim id_{Set(\mathbb{T})}\;$.
=--

In other words, a topos is contractible if its identity map is homotopic to a constant map and a geometric theory $\mathbb{T}$ is contractible iff its classifying topos $Set(\mathbb{T})$ is. 

Notice incidentally, that this requires by definition the existence of a [[point of a topos|point]] of $Set(\mathbb{T})$, or in other words, the existence of a "classical" i.e. $Set$-based $\mathbb{T}$-model. In particular, since there exist ([[Boolean topos|Boolean]]) [[point of a topos#toposes without points|toposes without points]] there exist (Boolean) geometric theories that are not contractible.

The correspondance between geometric theories and Grothendieck toposes together with the correspondance between their models and geometric morphisms similarly affords the transposition of other homotopic concepts to the realm of geometric logic.

Let us take a closer look at constant endomorphisms $c$ of $Set(\mathbb{T})\;$:

$$
Set(\mathbb{T})\overset{!}{\to}Set\overset{\bar{c}}{\to}Set(\mathbb{T})\;.
$$

Here $\bar{c}$ classifies a $\mathbb{T}$-model in $Set$ whereas $!$ classifies a model (which is unique up to isomorphism since $Set$ is [[terminal object|terminal]]) of some theory $\mathbb{S}$ classified by $Set$ whence $c$ classifies a $\mathbb{T}$-model that carries a $\mathbb{S}$-model structure as well.

Now, the [[inverse image functor|inverse image part]] of $!$ is $\Delta\;$, the [[constant sheaf|constant sheaf functor]]. Objects in the range of $\Delta$ are traditionally called "constant" whence we can think of the contractability $id_{Set(\mathbb{T})}\sim c$ of $\mathbb{T}$ as expressing the "almost constancy" of the generic model $\mathbf{M}_\mathbb{T}\sim \Delta(\bar{c}^*(\mathbf{M}_\mathbb{T}))$ i.e. as a structural similarity between $\mathbf{M}_\mathbb{T}$ and a constant $\mathbb{T}$-model.

## Example

Let $Set(\mathbb{D}_\infty)$ be the [[Schanuel topos]] that classifies the [[theory of infinite decidable objects|theory $\mathbb{D}_\infty$ of infinite decidable objects]] and $\mathbf{D}_\infty$ the generic infinite [[decidable object]].

+-- {: .num_prop }
###### Proposition (Joyal-Wraith)
$Set(\mathbb{D}_\infty)\;$, respectively the theory $\mathbb{D}_\infty\;$, are naturally contractible.
=--

**Proof.**

We argue on the logical side: $Set$ classifies the theory $\mathbb{S}$ of initial successor algebras whose models are [[natural number object|natural number objects]] (cf. the example section at [[geometric theory]]). But by generalities (that can be found e.g. in [[Handbook of Categorical Algebra|Borceux vol.3]]) a natural number object is both infinite and decidable and certainly the familiar set $\mathbb{N}$ of [[natural number|natural numbers]] in Set is.

Accordingly, we take $\bar{c}$ as the map that classifies $\mathbb{N}=\bar{c}^*(\mathbf{D}_\infty)$ as a model of $\mathbb{D}_\infty$ in Set. Then $!=\Delta\dashv\Gamma$ classifies $\Delta(\mathbb{N})$ as a model of $\mathbb{S}$ in $Set(\mathbb{D}_\infty)$ and the composite $\bar{c}\circ !$ classifies $\Delta(\mathbb{N})=\Delta(\bar{c}^*(\mathbf{D}_\infty))$ as a model of $\mathbb{D}_\infty$ in $Set(\mathbb{D})$.

Whence it suffices to exhibit a zigzag of homomorphisms in $\mathbb{D}_\infty-Mod(Set(\mathbb{D}_\infty))$ between the natural numbers object $\Delta(\mathbb{N})$ and the generic model $\mathbf{D}_\infty$ but the coproduct $\Delta(\mathbb{N})+\mathbf{D}_\infty$ is both infinite and decidable, hence in $\mathbb{D}_\infty-Mod(Set(\mathbb{D}_\infty))\;$, and the respective inclusions $\Delta(\mathbb{N})\rightarrow \Delta(\mathbb{N})+\mathbf{D}_\infty\leftarrow \mathbf{D}_\infty$ yield the desired zigzag of homomorphisms.$\qed$


## Topos homotopy via path spaces

The [[Sierpinski topos]] $Set^2$ is a connected, locally connected and local topos. As a result of [[Artin gluing]] along $Set\overset{id}{\to}Set$ it has two [[point of a topos|topos points]] (corresponding to the two points of the underlying [[Sierpinski space]]). It is [[exponentiable topos|exponentiable]] and, given a topos $\mathcal{E}$, we can accordingly view the exponential $\mathcal{E}^{Set^2}$ as a path space for $\mathcal{E}$ with respect to the abstract [[interval object]] $Set^2$.

(Cf. Beke [2000](#B00), p.11f)

## Related entries

* [[homotopy theory]]

* [[theory of model homomorphisms]]

* [[Sierpinski topos]]

* [[Eilenberg-Mac Lane space]]

* [[theory of presheaf type]]

## References

The concept originates with

* {#JW84}[[André Joyal]], [[Gavin Wraith]], _Eilenberg-Mac Lane Toposes and Cohomology_ , pp.117-131 in Cont. Math. **92** AMS 1984.

* {#W83}[[Gavin Wraith]], _Toposes and simplicial sets: the cohomological connection_ , pp.281-290 in _Category theoretic methods in geometry_ , no.**35** Aarhus Univ. Var. Publ. Ser. 1983.

An overview of homotopy theory done in this "toposophical" context is

* {#B00}[[Tibor Beke]], _Homotopoi_ , ms. University of Massachusetts Lowell (2000). ([dvi](http://faculty.uml.edu/tbeke/topos.dvi))

The following paper explores the topos of sheaves on the unit interval as abstract interval object

* {#MW86} [[Ieke Moerdijk]], [[Gavin Wraith]], _Connected locally connected toposes are path-connected_ , Trans. AMS **295** no.2 (1986) pp.849-859.

A proof of the homotopy equivalence of certain _petit_ and _gros_ toposes can be found on p.415f in

* {#MM94}[[Saunders Mac Lane]], [[Ieke Moerdijk]], _Sheaves in Geometry and Logic_ , Springer Heidelberg 1994.

A good source for the classical cohomology theory of toposes is chapter 8 of

* {#J77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York (1977). (Also available as Dover Reprint, Mineola 2014)
