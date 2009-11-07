

#Contents#
* automatic table of contents goes here
{:toc}

## Definition ##

A **group** is a [[monoid]] in which every element has an [[inverse]].



##Delooping##

To some extent, a group "is" a [[groupoid]] with a single object, or more precisely a [[pointed object|pointed]] groupoid with a single object.

The [[delooping]] of a group $G$ is a [[groupoid]] $\mathbf{B} G$ with 

* $Obj(\mathbf{B}G) = \{\bullet\}$ 

* $Hom_{\mathbf{B}G}(\bullet, \bullet) = G$.

Since for $G, H$ two groups, [[functors]] $\mathbf{B}G \to \mathbf{B}H$ are canonically in bijection with group homomorphisms $G \to H$, this gives rise to the following statement:

Let [[Grpd]] be the 1-[[category]] whose objects are [[groupoids]] and whose [[morphisms]] are [[functors]] (discarding the [[natural transformations]]). Let [[Grp]] be the category of groups. Then the [[delooping]] functor

$$
  \mathbf{B} : Grp \to Grpd
$$

is a [[full and faithful functor]]. In terms of this functor we may regard groups as the full [[subcategory]] of groupoids on groupoids with a single object.

It is in this sense that a group really is a groupoid with a single object.

But notice that it is unnatural to think of [[Grpd]] as a 1-category. It is really a [[2-category]], namely the sub-2-category of [[Cat]] on groupoids.

And the category of groups is _not_ equivalent to the full sub-2-category of the 2-category of groupoids on one-object groupoids. 

The reason is that two functors:

$$
  \mathbf{B}f_1, \mathbf{B}f_2 : \mathbf{B}G \to \mathbf{B}H
$$ 

coming from two group homomorphisms $f_1, f_2 : G \to H$ are related by a [[natural transformation]] $\eta_h : f_1 \to f_2$ with single component $\eta_h : \bullet \mapsto h \in Mor(\mathbf{B} H)$ for each element $h \in H$ such that the homomorphisms $f_1$ and $f_2$ differ by the [[inner automorphism]] $Ad_h : H \to H$

$$
  (\eta_h : \mathbf{B}f_1 \to \mathbf{B}f_2)
  \Leftrightarrow 
  (f_2 = Ad_h \circ f_1)
  \,.
$$

To fix this, look at the category of [[pointed object|pointed]] groupoids with [[pointed functor|pointed functors]] and pointed natural transformations.  Between group homomorphisms as above, only identity transformations are pointed, so $Grp$ becomes a full sub-$2$-category of $Grpd_*$ (one that happens to be a $1$-[[1-category|category]]).  (Details may be found in the appendix to [[Lectures on n-Categories and Cohomology]] and should probably be added to [[pointed functor]] and maybe also [[k-tuply monoidal n-category]].)


## Internalization ##

A **[[group object]]** [[internalization|internal to]] a [[category]] $C$ with finite [[product|products]] is an object $G$ together with maps $mult:G\times G\to G$, $id:1\to G$, and $inv:G\to G$ such that various diagrams expressing associativity, unitality, and inverses commute.

Equivalently, it is a functor $C^{op}\to Grp$ whose underlying functor $C^{op} \to Set$ is [[representable functor|representable]].

For example, a group object in [[Diff]] is a [[Lie group]].  A group object in [[Top]] is a [[topological group]].  A group object in [[S-Sch]] is a S-group scheme.  And a group object in $CAlg^{op}$, where $CAlg$ is the category of commutative algebras, is a (commutative) [[Hopf algebra]].

A group object in [[Grp]] is the same thing as an abelian group (see [[Eckmann-Hilton argument]]), and a group object in [[Cat]] is the same thing as an [[internal category]] in [[Grp]], both being equivalent to the notion of [[crossed module]]. 

## Groups in higher categorical and homotopical contexts ##

Internalizing the notion of _group_ in [[higher category theory|higher categorical]] and [[homotopy theory|homotopical]] contexts yields various generalized notions. For instance

* a [[2-group]] is a group object in [[Grpd]]

* an [[n-group]] is a group object internal to [[n-groupoid]]s

* a [[loop space]] is a group object in [[Top]]

* generally there is a notion of [[groupoid object in an (infinity,1)-category|group object in an (infinity,1)-category]].

And the notion of [[loop space object]] and [[delooping]] makes sense (at least) in any [[(infinity,1)-category]].

Notice that the relation between group objects and deloopable objects becomes more subtle as one generalizes this way. For instance not every [[groupoid object in an (infinity,1)-category|group object in an (infinity,1)-category]] is [[delooping|deloopable]]. But every group object in an [[(infinity,1)-topos]] is.

## Weakened versions ##

<div style="float:left;margin:0 10px 10px 0;"><img src="http://math.ucr.edu/home/baez/centipede.jpg" alt="" width="208" height="150" /> &nbsp; &nbsp;</div>

Following the practice of [[centipede mathematics]], we can remove certain properties from the definition of group and see what we get:
* remove inverses to get [[monoids]], then remove the identity to get [[semigroups]];
* or remove associativity to get [[loop(algebra)|loops]], then remove the identity to get [[quasigroups]];
* or remove all of the above to get [[magma|magmas]];
* or instead allow (in a certain way) for the binary operation to be partial to get [[groupoids]], then remove inverses to get [[categories]], and then remove identities to get [[semicategory|semicategories]]
* etc.

[[!redirects groups]]