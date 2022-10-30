
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--

# Discrete spaces
* table of contents
{: toc}

## Idea

A __discrete space__ is, in general, an object of a [[concrete category]] $Sp$ of spaces that is [[free functor|free]] on its underlying set.  

Every [[topological concrete category]] has discrete spaces ([[discrete objects]]); so do many other categories, such as [[Diff]] and [[Hausdorff space|Haus Top]].  Non-concrete categories of spaces, such as [[Loc]], usually also have discrete spaces; the concept makes sense as long as there is a given [[forgetful functor]] from $Sp$ to [[Set]].

The dual notion is that of a [[codiscrete space]].

More generally, any [[local topos]] is a context in which it makes sense to ask if an object is discrete or [[codiscrete object|codiscrete]].

By definition, a local topos $\mathbf{H}$ comes with an [[adjoint triple]] of [[functors]]

$$
  \mathbf{H}
   \stackrel{\overset{Disc}{\hookleftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\hookleftarrow}}}
  \mathbf{B}
$$

to a [[base topos]] $\mathbf{B}$ (for instance [[Set]]). And a _discrete object_ is one in the [[essential image]] of the functor $Disc$.

Even more generally, $\mathbf{H}$ may be a [[local (∞,1)-topos]]. For more on the discrete objects in such a context see _[[discrete ∞-groupoid]]_ .

Often one also calls objects in [[higher category theory]] _discrete_ if they are in the essential image of the embedding of [[sets]] into the higher categorical context. This can typically be understood as a special case of discreteness in the above sense.

## Definition

We want the functor
$$ Set \stackrel{F}\to Sp \stackrel{U}\to Set $$
to be ([[natural isomorphism|naturally isomorphic]] to) the [[identity functor]] on [[Set]], where $F: Set \to Sp$ is [[adjoint functor|left adjoint]] to the [[forgetful functor]] $U: Sp \to Set$.  (This is true, for example, if $Sp$ is [[Top]], [[Diff]], [[Loc]], etc.)

Assuming that $U$ is [[faithful functor|faithful]] (as it should be when $Sp$ is a concrete category), we can characterise a discrete space $X$ as one such that every function from $X$ to $Y$ (for $Y$ any space) is a morphism of spaces.  (More precisely, this means that every function from $U(X)$ to $U(Y)$ is the image under $U$ of a morphism from $X$ to $Y$.)

A [[topological space]] is discrete in the sense above only if the [[diagonal map]] $X \times X \to X$ is [[open map|open]]; the converse holds if $X$ satisfies the $T_0$ [[separation axiom]].  In [[locale]] theory, the condition that a locale is discrete may be split into two parts: that $X \times X \to X$ is open and that $X \to 1$ is open.  A locale that satisfies the latter condition is called [[overt locale|overt]]; note that every locale is $T_0$ while every topological space is overt.  In [[Abstract Stone Duality]], a space is called __discrete__ if $X \times X \to X$ is open, which corresponds to the existence of an [[equality]] relation on $X$; discrete spaces as described above correspond to discrete *overt* spaces in ASD.


## Examples

### Discrete geometric spaces

The best known example is a discrete [[topological space]], that is one, $X$, in which all subsets of $X$ are [[open subset|open]] in the topology. This is the [[discrete topology]] on $X$.  

This same space serves as a discrete object in many subcategories and supercategories of $Top$, from [[convergence space]]s (where the only proper filter that converges to a point is the free ultrafilter at that point) to (say) paracompact Hausdorff spaces (because a discrete topological space has those properties).  It is also [[sober space|sober]] and thus serves as a discrete [[locale]], whose corresponding [[frame]] is the [[power set]] of $X$; see [[CABA]].

A discrete [[uniform space]] $X$ has all [[reflexive relations]] as [[entourages]], or equivalently all [[covers]] as [[uniform cover]]s.  It is the only uniformity (on a given set) whose underlying topology is discrete.

Strictly speaking, there is no discrete [[metric space]] on any set with more than one element, because the forgetful functor has no left adjoint.  However, there is a discrete *extended* metric space, given by $d(x,y) = \infty$ whenever $x \ne y$.  More usually, the term 'discrete metric' is used when $d(x,y) = 1$ for $x \ne y$, which is discrete in the category of metric spaces of diameter at most $1$.  (Comparing the [[adjoint functor theorem]], the problem with $Met$ is that it generally lacks infinitary [[product]]s; in contrast, $Ext Met$ and $Met_1$ are [[complete category|complete]].)

A general axiomatization of the notion of space is as an object in a [[cohesive topos]]. This comes by definition with an underlying-set-functor (or similar) and a [[left adjoint]] that produces discrete cohesive structure. See there for details.

### Discrete cellular/categorical structures
 {#DiscreteCellularStructures]

Often one calls a cellular structure such as appeariun in [[higher category theory]] _discrete_ if it is in the [[essential image]] of the inclusion of [[sets]].

For instance one may speak of a _[[discrete category]]_ as a category that is equivalent to one which has only [[identity]] morphisms. This concept has a generalization to a notion of [[discrete object in a 2-category]]. 

At least if the categories in question here are in fact [[groupoids]], alternative terminology for this use of "discrete" is _[[0-truncated]]_. A discrete groupoid in this sense is a _[[homotopy n-type|homotopy 0-type]]_, or simply a [[h-level|0-type]].

This terminology may be preferrable over "discrete" in this context, notably when one is dealing with higher cellular structures that are in addition equipped with geometric structure. For instance when dealing with a [[topological category]] there is otherwise ambiguity in what it means to say that it is "discrete": it could either mean that its underlying topological spaces (of objects and of morphisms) are discrete spaces,  or it could mean that it is no nontrivial morphisms, but possibly a non-discrete topological space of objects.

On the other hand, typically the cellular notion of "discreteness" is a special case of the spatial notion. For instance the [[category]] [[sSet]] of [[simplicial sets]] is canonically a [[cohesive topos]] (as discussed in the examples there) and hence in particular a [[local topos]] over [[Set]]. The discrete objects relative to this notion of cohesion are precisely the simplicial sets that are constant on a given ordinary set, hence those that are "discrete" in the cellular sense.



## Related concepts

* **discrete space**

* [[discrete group]] 

* [[discrete groupoid]]

* [[discrete ∞-groupoid]]



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
