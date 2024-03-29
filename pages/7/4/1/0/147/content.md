
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea 

A _site_  is a [[locally presentable category|presentation]] of a [[sheaf topos]] as a structure [[free cocompletion|freely generated under colimits]] from a category, subject to the relation that certain [[covering]] colimits are preserved.

As such, sites generalise [[topological spaces]] and [[locales]], which present [[localic topos|localic]] sheaf toposes.  More precisely, sites generalise and [[categorify]] [[posites]], which present localic toposes but also present locales themselves in a decategorified manner.

In technical terms, a _site_ is a [[small category]] equipped with a [[coverage]] or [[Grothendieck topology]]. The [[category of sheaves]] over a site is a [[sheaf topos]] and the site is a _site of definition_ for this topos.


## Definition 

+-- {: .num_defn #Site}
###### Definition

A _site_ $(C,J)$ is a [[category]] $C$ equipped with a [[coverage]] $J$.

For $\mathcal{E}$ a topos equipped with an [[equivalence of categories]]

$$
  \mathcal{E} \simeq Sh(C,J)
$$

to the [[sheaf topos]] over a site, one says that $(C,J)$ is a **site of definition** for $\mathcal{E}$.

=--

Some classes of sites have their special names

+-- {: .num_defn #TypesOfSites}
###### Definition

A site is called

* a [[small site]], [[large site]], _essentially small site_ if the underlying category is a [[small category]], [[large category]], [[essentially small category]], respectively;

* a **[[cartesian site]]** if the underlying category is [[finitely complete category|finitely complete]] (which the [[Elephant]] calls a [[cartesian category]]);

* a **[[standard site]]** if it is a cartesian site equipped with a [[subcanonical coverage]].

=--

The term [[standard site]] appears in ([Johnstone, example A2.1.11](#Johnstone)).


+-- {: .num_remark #SmallAndLarge}
###### Remark

Often a site is required to be a [[small category]]. But also [[large site]]s play a role.

=--

+-- {: .num_remark #CoveragesAndTopologies}
###### Remark

Every [[coverage]] induces a [[Grothendieck topology]]. Often sites are defined to be categories equipped with a Grothendieck topology. Some constructions and properties are more elegantly handled with coverages, some with Grothendieck topologies.

Notice that there are many equivalent ways to define a [[Grothendieck topology]], for instance in terms of a system of [[local isomorphisms]], or in terms of a system of [[dense monomorphisms]] in the [[category of presheaves]] $PSh(S)$.

=--

+-- {: .num_defn}
###### Definition

For $(C,J)$ a site, we write $Sh_J(C)$ for the
[[category of sheaves]] on $C$ with respect to the [[coverage]] $J$.

=--


## Properties


### Morita equivalent sites

Many inequivalent sites may have equivalent [[sheaf topos]]es.

+-- {: .num_prop }
###### Proposition

Every [[sheaf topos]] has a [standard site](#TypesOfSites) of definition.

=--

This appears as ([Johnstone, theorem C2.2.8 (iii)](#Johnstone)).

+-- {: .num_remark }
###### Remark

By [this corollary](classifying+topos#SheafToposesAreClassifyingForTheirTheoryOfLocalAlgegras) at _[[classifying topos]]_ this means that every sheaf topos is the [[classifying topos]] for some [[theory]] of [[local algebras]].

=--


### Subcanonical sites

+-- {: .num_prop #CharacterizationOfSubcanonicalSites}
###### Proposition

For $\mathcal{E}$ a [[sheaf topos]], the [[essentially small category|essentially small]] sites of definition $(\mathcal{C}, J)$ of $\mathcal{E}$ such that $J$ is a [[subcanonical coverage]] are precisely the [[full subcategories]] on [[generating families]] of objects equipped with the coverages induced from the [[canonical coverage]] of $\mathcal{E}$.

=--

This appears as ([Johnstone, prop. C2.2.16](#Johnstone)).



## Examples


### Classes of sites

* Every [[frame]] is canonically a site, where $U$ is covered by $\{U_i\}$ precisely if it is their [[join]].
  
  A subclass of examples is the [[category of open subsets]] of a [[topological space]].

  This are examples of [[posite]]s/[[(0,1)-site]].

* Various categories come with canonical structures of sites on them:

  * For every category $C$ there is its [[canonical coverage]].

  * On every [[regular category]] there is its [[regular coverage]].

  * On every [[coherent category]] there is its [[coherent coverage]].

  * Generalizing the previous two examples, on an [[∞-ary regular category]] there is a $\kappa$-canonical coverage.

  If the category in question is the [[syntactic category]] of a [[theory]], the corresponding site is the [[syntactic site]].

* For every site there is the corresponding [[double negation topology]] that forces the sheaf topos to a [[Boolean topos]].

Other classes of sites are listed in the following.

* [[big site]] 

* [[dense sub-site]]

* [[large site]], [[essentially small site]]

* [[concrete site]]

* [[locally connected site]] / [[locally ∞-connected site]]

  * [[connected site]] / [[∞-connected site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / [[∞-local site]]

* [[cohesive site]], [[∞-cohesive site]]

* [[atomic site]]

### Specific sites

* Sites for [[big topos]]es defining notions of [[higher geometry|geometry]] are:

  * The sites that define the [[higher geometry|geometry]] called [[differential geometry]] are [[CartSp]]${}_{smooth}$, [[SmoothMfd]], etc, equipped with the [[open cover]] [[coverage]]. Or more generally [[smooth loci]] etc.

  * The sites that induce [[topological geometry]] are small versions of [[Top]] equipped with the [[open cover]] [[coverage]].

  * The sites that induce the [[higher geometry]] modeled on [[Euclidean topology]] are the large site of [[paracompact manifold]]s and its [[dense sub-site]] [[CartSp]]${}_{top}$.

* The sites that define the [[higher geometry|geometry]] called [[algebraic geometry]] are site structures on categories of formal duals of [[commutative ring]]s or commutative [[associative algebra]]s

  * [[fpqc-site]] $\to$ [[fppf-site]] $\to$ [[syntomic site]] $\to$ [[étale site]] $\to$ [[Nisnevich site]] $\to$ [[Zariski site]]

    [[crystalline site]]


## Related concepts

* [[posite]]

* **site**

  * [[internal site]]
  * [[∞-ary site]]

* [[2-site]], [[(2,1)-site]]

* [[(∞,1)-site]]

  * [[model site]], [[simplicial site]]

* [[morphism of sites]], [[covering lifting property]]


## References 

In 

* [[Peter Johnstone]], _[[Elephant|Sketches of an Elephant]]_

sites are discussed in section C2.1.

[[!redirects sites]]

[[!redirects 1-site]]
[[!redirects (1,1)-site]]
[[!redirects 1-sites]]
[[!redirects (1,1)-sites]]
