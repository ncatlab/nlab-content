+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

# Discrete objects
* table of contents
{: toc}

## Idea

A __discrete space__ is, in general, an object of a [[concrete category]] $Sp$ of spaces that is [[free functor|free]] on its own underlying set.  More generally, the notion can be applied relative to any [[forgetful functor]].

**Note:** *This page is about the "[[cohesive]]" or "[[topology|topological]]" notion of discreteness.  In [[2-category theory]] the term "discrete object" is also often used for [[n-truncated object|0-truncated objects]].  For this usage, see _[[discrete morphism]]_ instead.*

## Definition

A discrete space must, in particular, be a [[free object]] for the forgetful functor $U\colon Sp\to Set$, i.e. in the image of its [[adjoint functor|left adjoint]] $F: Set \to Sp$.  However, this is not sufficient for it to be free on its *own* underlying set; we must also require that the counit $F U X\to X$ be an [[isomorphism]].

Thus, we say that $U\colon Sp \to Set$ (or more generally, any functor) **has discrete spaces** or **discrete objects** if it has a [[fully faithful functor|fully faithful]] left adjoint.  This ensures that the functor
$$ Set \stackrel{F}\to Sp \stackrel{U}\to Set $$
is ([[natural isomorphism|naturally isomorphic]] to) the [[identity functor]] on [[Set]].  This is true, for example, if $Sp$ is [[Top]], [[Diff]], [[Loc]], etc.

Assuming that $U$ is [[faithful functor|faithful]] (as it is when $Sp$ is a concrete category), we can characterise a discrete space $X$ as one such that every function from $X$ to $Y$ (for $Y$ any space) is a morphism of spaces.  (More precisely, this means that every function from $U(X)$ to $U(Y)$ is the image under $U$ of a morphism from $X$ to $Y$.)

The dual notion is a [[codiscrete object]].


## Examples

### Discrete geometric spaces

The best known example is a discrete [[topological space]], that is one, $X$, in which all subsets of $X$ are [[open subset|open]] in the topology.  This is the [[discrete topology]] on $X$.  If $X$ is discrete in this sense, then its [[diagonal map]] $X \times X \to X$ is [[open map|open]]; the converse holds if $X$ satisfies the $T_0$ [[separation axiom]].

This same space serves as a discrete object in many subcategories and supercategories of $Top$, from [[convergence space]]s (where the only proper filter that converges to a point is the free ultrafilter at that point) to (say) paracompact Hausdorff spaces or [[Diff|manifolds]] (because a discrete topological space has those properties).

It is also [[sober space|sober]] and thus serves as a discrete [[locale]], whose corresponding [[frame]] is the [[power set]] of $X$; see [[CABA]].  (Note that [[Loc]] is not concrete over [[Set]].).  A locale is discrete if and only if $X \times X \to X$ is open and $X \to 1$ is also open.  A locale that satisfies the latter condition is called [[overt locale|overt]]; note that every locale is $T_0$ while every topological space is overt.  Moreover, in [[classical mathematics]], every locale is overt, but the notion is important when internalizing in [[toposes]].

A discrete [[uniform space]] $X$ has all [[reflexive relations]] as [[entourages]], or equivalently all [[covers]] as [[uniform cover]]s.  It is the only uniformity (on a given set) whose underlying topology is discrete.

Strictly speaking, there is no discrete [[metric space]] on any set with more than one element, because the forgetful functor has no left adjoint.  However, there is a discrete *extended* metric space, given by $d(x,y) = \infty$ whenever $x \ne y$.  More usually, the term 'discrete metric' is used when $d(x,y) = 1$ for $x \ne y$, which is discrete in the category of metric spaces of diameter at most $1$.  (Comparing the [[adjoint functor theorem]], the problem with $Met$ is that it generally lacks infinitary [[product]]s; in contrast, $Ext Met$ and $Met_1$ are [[complete category|complete]].)

In [[Abstract Stone Duality]], a space is called __discrete__ if the diagonal map $\delta: X \to X \times X$ is open, which corresponds to the existence of an [[equality]] relation on $X$; discrete spaces as described above correspond to discrete *overt* spaces in ASD.

### Local toposes

Any [[local topos]] has discrete and [[codiscrete object|codiscrete]] objects.  By definition, a local topos $\mathbf{H}$ comes with an [[adjoint triple]] of [[functors]]

$$
  \mathbf{H}
   \stackrel{\overset{Disc}{\hookleftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\hookleftarrow}}}
  \mathbf{B}
$$

to a [[base topos]] $\mathbf{B}$ (for instance [[Set]]), for which both $Disc$ and $Codisc$ are fully faithful.  Thus, a _discrete object_ is one in the [[essential image]] of the functor $Disc$.  Note that $\Gamma$ is not generally faithful in this case.

Even more generally, $\mathbf{H}$ may be a [[local (∞,1)-topos]]. For more on the discrete objects in such a context see _[[discrete ∞-groupoid]]_ .

Equivalently, this [[adjoint triple]] induces an [[adjoint pair]] of [[modalities]]

$$
  (\flat \dashv \sharp)
  \coloneqq
  ( Disc \Gamma \dashv coDisc \Gamma)
  \,,
$$

the _[[flat modality]]_ and the _[[sharp modality]]_. The discrete objects are precisely the [[modal types]] for the [[flat modality]]. The [[codiscrete objects]] are the modal types for the [[sharp modality]].

### Topological categories, fibrations, and final lifts

Every [[topological concrete category]] has discrete (and also codiscrete) spaces 

More generally, if $U$ is an [[opfibration]] and $Sp$ has an initial object preserved by $U$, then $Sp$ has discrete objects: the discrete object on $X$ can be obtained as $i_!(0)$ where $0$ is the initial object of $Sp$ and $i\colon \emptyset \to X$ is the unique map from the initial object in $Set$ (or whatever underlying category).  (Conversely, if $Sp$ has discrete objects and pushouts preserved by $U$, then $U$ is an opfibration.)

Discrete objects can also be characterized as [[final lifts]] for empty [[sinks]].

### In simplicial sets

The category [[sSet]] of [[simplicial sets]] is a [[local topos]] (in fact a [[cohesive topos]]). 

* A _discrete object_ in $sSet$ is precisely the [[nerve]] of a [[discrete groupoid]].

* A _[[codiscrete object]]_ in $sSet$ is precisely the [[nerve]] of a [[codiscrete groupoid]].


### Discrete cellular/categorical structures
 {#DiscreteCellularStructures]

Often one calls a cellular structure, such as those appearing in [[higher category theory]], _discrete_ if it is in the [[essential image]] of the inclusion of [[Set]].

For instance, one may speak of a _[[discrete category]]_ as a category that is equivalent (or, in some cases, isomorphic) to one which has only [[identity]] morphisms.  This concept has a generalization to a notion of [[discrete object in a 2-category]].

An alternative terminology for this use of "discrete" is _[[truncated object|0-truncated]]_, or more precisely (0,0)-truncated.  A discrete groupoid in this sense is a _[[homotopy n-type|homotopy 0-type]]_, or simply a [[h-level|0-type]].  This terminology may be preferable to "discrete" in this context, notably when one is dealing with higher categorical structures that are in addition equipped with geometric structure. For instance, when dealing with a [[topological category]] there is otherwise ambiguity in what it means to say that it is "discrete": it could either mean that its underlying topological spaces (of objects and of morphisms) are discrete spaces,  or it could mean that it has no nontrivial morphisms, but possibly a non-discrete topological space of objects.

+--{: .num_remark}
###### Remark
In some cases, the cellular notion of "discreteness" for higher categories can be seen as a special case of the *spatial* notion of discreteness --- often the 1-category of shapes will have a functor to sets for which the cellularly discrete objects are the discrete objects in the sense considered on this page.  For instance, this is the case for [[simplicial sets]], which form a [[local topos]] over [[Set]].  The discrete objects relative to this notion of cohesion are precisely the simplicial sets that are constant on a given ordinary set, hence those that are "discrete" in the cellular sense.
=--

### In $\infty$-toposes
 {#ExamplesInInfinityToposes}

The definition of discrete objects has the evident generalization from [[category theory]] to [[(∞,1)-category theory]]/[[homotopy theory]]. One noteworthy aspect of discrete objects in the context of homotopy theory is that there they are intimately related to the notion of _[[cohomology]]_.

For $\mathcal{X}$ an [[(∞,1)-sheaf (∞,1)-topos]] with [[global section]] [[geometric morphism]]

$$
  (\Delta \dashv \Gamma)
  \colon
  \mathcal{X}
  \stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}
 \infty Grpd
$$

then for $X \in \mathcal{X}$ any object and $A \in $ [[∞Grpd]] any object, one says that

$$
  H(X,A)
  \coloneqq
  \pi_0 \mathcal{X}(X,\Delta(A))
  \in
  Set
$$

is the [[cohomology]] of $X$ [[cohomology with constant coefficients|with (locally) constant coefficients]] in $A$. (Here on the right $\mathcal{X}(-,-)$ denotes the [[(∞,1)-categorical hom-space]].)

Now if $\mathcal{X}$ _has discrete objects_ in the sense that $\Delta \colon \infty Grpd \to \mathcal{X}$ is a [[full and faithful (∞,1)-functor]], then it follows immediately from the definitions that the cohomology of discrete objects with constant coefficients in $\mathcal{X}$ equals the cohomology in [[∞Grpd]], which is standard "[[nonabelian cohomology]]":

$$
  (\mathcal{X} \, has\, discrete\, objects)
  \Leftrightarrow 
  ( \forall_{S,A \in \infty Grpd} \mathcal{X}(\Delta S, \Delta A) \simeq \infty Grpd(S,A) )
  \,.
$$

Conversely: _the failure of the cohomology with constant coefficients of objects in the image of $\Delta$ to coincide with standard cohomology is a measure for $\Delta$ not respecting discrete objects.

For example the [[natural numbers object]] $\mathbf{N} \simeq \Delta \mathbb{N}$ in the [[(∞,1)-sheaf (∞,1)-topos]] over some [[topological spaces]] fails to be a discrete object. Accordingly in this case the natural numbers object can have nontrivial higher cohomology with constant coefficients, see for instance ([Blass 83](#Blass83), [Shulman 13](#Shulman13)).

## Related concepts

* **discrete space**

* [[discrete group]] 

* [[discrete groupoid]]

* [[discrete ∞-groupoid]]

* [[codiscrete space]], [[Freyd cover]]

[[!include cohesion - table]]

## References

* *Discreteness, concreteness, fibrations, and scones*: [blog post](http://golem.ph.utexas.edu/category/2011/11/discreteness_concreteness_fibr.html)

* [[Andreas Blass]], _Cohomology detects failures of the axiom of choice_, Trans. Amer. Math. Soc. 279 (1983), 257-269 ([web](http://www.ams.org/journals/tran/1983-279-01/S0002-9947-1983-0704615-7/))
 {#Blass83}

* [[Mike Shulman]], _Cohomology_ on the [[homotopy type theory]] blog [here](http://homotopytypetheory.org/2013/07/24/cohomology/)
 {#Shulman13}

[[!redirects discrete space]]
[[!redirects discrete spaces]]

[[!redirects discrete uniformity]]
[[!redirects discrete uniformities]]
[[!redirects discrete uniform structure]]
[[!redirects discrete uniform structures]]
[[!redirects discrete uniform space]]
[[!redirects discrete uniform spaces]]

[[!redirects discrete metric]]
[[!redirects discrete metrics]]
[[!redirects discrete metric space]]
[[!redirects discrete metric spaces]]
[[!redirects discrete extended metric]]
[[!redirects discrete extended metrics]]
[[!redirects discrete extended metric space]]
[[!redirects discrete extended metric spaces]]

[[!redirects discrete locale]]
[[!redirects discrete locales]]

[[!redirects discrete object]]
[[!redirects discrete objects]]

[[!redirects discrete]]
[[!redirects discreteness]]
