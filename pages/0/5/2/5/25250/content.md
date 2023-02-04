\tableofcontents

## Introduction

The purpose of this article is to explain how the general abstract techniques for computing [[sheaf cohomology]] described in articles like [[model structures on simplicial presheaves]] connect to the more traditional techniques for computing [[abelian sheaf cohomology]] such as injective resolutions, acyclic resolutions, Čech cohomology, Cartan and Leray theorems, etc.

## Model structures

Fix some [[site]] S such as Zariski, Nisnevich, etc., or one of the differential-geometric or complex-geometric sites.
We are interested in the category of [[chain complexes]] of [[sheaves]] or [[presheaves]] on S,
and how to compute [[abelian sheaf cohomology]] on S using [[model structures]] on these categories.

The following three [[model categories]] are [[Quillen equivalent]]:

1. The local [[projective model structure]] on [[chain complexes]] of [[presheaves]] of abelian groups.

2. The local [[injective model structure]] on chain complexes of presheaves of abelian groups;

3. The local [[injective model structure]] on chain complexes of sheaves of abelian groups;

For typical sites, it is not possible to construct a [[projective model structure]] or a local projective model structure on chain complexes of sheaves of abelian groups, which is often expressed by saying that the category of sheaves of abelian groups does not have enough [[projective objects]].

Here “local” means the same thing in all three cases: the class of [[weak equivalences]]
of these [[model structures]] is precisely the class of [[natural transformations]] of presheaves
that induce isomorphisms on sheaves of [[homology]] groups.
The latter can be computed as [[associated sheaves]] of presheaves of homology groups, which are computed objectwise on the site.

Furthermore, for a site with enough points (as is the case with the Zariski and Nisnevich site, as well as pretty much any site used in differential or complex geometry), the class of weak equivalences can also be described as the class of [[natural transformations]] of presheaves that at every point of the site induces a quasi-isomorphism of [[stalks]] at this point.

Next, if the site is [[hypercomplete]] (as is the case for any site with enough points), the following [[model categories]] are [[Quillen equivalent]] to each other and to the model categories 1-3),
in fact we have equalities 1=4, 2=5:

4\.  The [[projective model structure]] on chain complexes of presheaves of abelian groups left Bousfield localized at [[Čech nerves]] of covering families.

5\.  The [[injective model structure]] on chain complexes of presheaves of abelian groups left Bousfield localized at Čech nerves of covering families;

The [[model structures]] 1) and 2) can in general also be expressed as a [[left Bousfield localization]] of the projective/injective model structure on presheaves,
this time with respect to the (larger) class of [[hypercovers]],
or, equivalently, maps inducing isomorphisms on homology sheaves.
If the site is [[hypercomplete]], this process yields the same weak equivalence as in 4) and 5).

The model structure 3) is typically not a localization of a global model structure,
however, it can be easily constructed directly using, e.g., the [[Smith recognition theorem]].

There is an analogous statement in the setting of sheaves of abelian groups:
the category of sheaves of abelian groups is the [[category of fractions]], or, equivalently, [[reflective localization]],
of the category of presheaves of abelian groups with respect to the class of maps given by local isomorphisms of presheaves of abelian groups.
Left Bousfield localizations are precisely the homotopy coherent analogues of [[reflective localizations]].

To emphasize again: if the site has enough points, all three notions of a local weak equivalence:
isomorphisms on homology sheaves, stalkwise quasi-isomorphisms, and Čech-local weak equivalences coincide.
They are quite different from ordinary (objectwise) weak equivalences of presheaves, i.e., objectwise [[quasi-isomorphisms]].
(For sites that do not have enough points, such as the [[etale site]], it is important to distinguish [[Čech descent]] from [[hyperdescent]], which are quite different in general.)

The advantage of 4) and 5) is that [[fibrant objects]] are now easier to describe:
they are precisely [[fibrant objects]] in the original model structure (before a [[left Bousfield localization]]) that are local.
Here “local” amounts precisely to the homotopy coherent Čech descent property:
for any covering family in the site, the induced augmented cosimplicial diagram
exhibits its apex as the [[homotopy limit]] of the remaining cosimplicial diagram.
This is simply the homotopy coherent version of the usual gluing axiom for [[sheaves]] of abelian groups.

Any presheaf $F$ is weakly equivalent (in the localized model structure) to a local presheaf $L(F)$
via a (local) weak equivalence $F\to L(F)$, which is simply a homotopy coherent analogue of the [[associated sheaf]] map.
It is important not confuse the map $F\to L(F)$ with an entirely different map $F\to K(F)$
that is given by taking the [[associated sheaf]] of abelian groups of $F_n$ separately in every degree $n$.
The functor $K$ in fact gives a [[Quillen equivalence]] 2→3,
and in general has nothing to do with the functor $L$, which is related to the [[fibrant replacement]] functor in the model structures 1-5).

Indeed, the [[fibrant replacement]] functor in 1-5) can be computed by applying first $L$, then any [[fibrant replacement functor]] in the original (global) model structure.
For [[projective model structures]], the global fibrant replacement can be simply computed as the objectwise fibrant replacement,
which in the case of presheaves of chain complexes is a trivial operation, i.e., every presheaf of chain complexes is projectively fibrant.
For [[injective model structures]], the global fibrant replacement can be computed as the injective resolution.

The relevance of the [[fibrant replacement]] functor is explained by its relevance for computing the derived mapping chain complex of presheaves of chain complexes.
Recall that given [[presheaves]] $F$ and $G$ of chain complexes of abelian groups,
we can define the mapping chain complex $Map(F,G)$ using the usual formula with [[kernels]] (or [[equalizers]]).

What we really are interested in is the derived mapping chain complex $RMap(F,G)$,
which can be computed as $Map(Q F, R G)$, where $Q$ is a cofibrant replacement functor and $R$ is a fibrant replacement functor, in any of the [[model structures]] 1-5).
In the more traditional language, (the cohomology groups of) RMap are also known as the [[hypercohomology]] (groups) of $F$ with coefficients in $G$.

The derived mapping chain complex depends only on the class of [[weak equivalences]], not on the class of fibrations or cofibrations,
so in what follows we write $RMap_{local}(F,G)$ and $RMap_{global}(F,G)$ to distinguish the cases when we use local weak equivalence versus objectwise weak equivalences.

The fundamental relation between two chain complexes is
$$RMap_{local}(F,G) = RMap_{global}(F,L(G)),$$
where $G\to L(G)$ is the localization map described above.
In the [[injective model structure]] (local or not) all objects are cofibrant, so in this case we can take $Q=id$.
In the global [[projective model structure]], all objects are fibrant, so in this case we can take $R=id$.

For the local [[injective model structures]] 2, 3, 5 all objects are cofibrant, so $Q$ can be taken to be the identity functor,
whereas $R$ is (for example) the [[injective resolution]] functor.
In these cases, we obtain the fairly traditional recipe for computing [[abelian sheaf cohomology]]: replace the sheaf $F$ of coefficients by its fibrant replacement,
e.g., the injective resolution of $F$, then compute the ordinary mapping chain complex.

For the [[projective model structures]] 1, 4 fibrancy boils down to locality, i.e., the homotopy coherent descent condition, so $R=L$ is the homotopy coherent analogue of the [[associated sheaf]] functor,
whereas cofibrant objects are the same in the local and global model structure
and are degreewise [[retracts]] of [[coproducts]] of representables

Now the [[abelian sheaf cohomology]] of an object $X$ in the site with coefficients in a sheaf of abelian groups $F$ can be computed as follows.
First, convert $X$ to its representable presheaf of sets, then convert the resulting presheaf of sets into a presheaf of abelian groups
by applying the free abelian group functor objectwise.
We will abuse the language and continue to refer to such presheaves of abelian groups as representable presheaf.

In fact, the same technique continues to work for more general objects than objects of the site, e.g., for [[algebraic spaces]],
which can also be converted into presheaves of abelian groups by applying the free abelian group functor objectwise.
Now $X$ and $F$ are presheaves of abelian groups, which we can convert into presheaves of [[chain complexes]] by placing them in chain degree 0.
The $n$th [[sheaf cohomology]] group of $X$ with coefficients in $F$ is now simply the nth cohomology group of the [[chain complex]] $RMap(X,F)$.

## Traditional recipes for abelian sheaf cohomology

We can now easily recover all traditional recipes for computing [[abelian sheaf cohomology]]:

1.  In the model structure 1), we can replace F by its [[injective resolution]], which yields a local [[fibrant replacement]].
Since any object (including $X$) is cofibrant, we conclude by evaluating the mapping chain complex and taking its $n$th cohomology group.
In particular, if $X$ comes from a representable presheaf, then we can simply evaluate the [[injective resolution]] on $X$ and take its cohomology.

2.  We can also replace $F$ by its acyclic resolution $A$ via a map $F\to A$, which is a local weak equivalence.
Any acyclic resolution is a local object, but not necessarily a [[fibrant object]].
Thus, $RMap_{local}(X,F)$ can be computed as $RMap_{global}(X,A)$.
In typical applications, $X$ is representable, which means that $RMap(X,A)$ can be computed by evaluating $A$ on $X$,
which can be seen (for example) by switching to the [[projective model structure]], where $X$ is cofibrant and any object (including $A$) is fibrant.
This recovers the [[de Rham theorem]].

3.  In the model structure 3) we can fibrantly replace $F$ by taking its associated homotopy coherent sheaf $L(F)$.
Then we cofibrantly replace $X$ by taking the [[Čech nerve]] $\check C(U)$ of its covering family $U$.
Now $RMap(X,F)$ can be computed as $RMap(\check C(U),L(F))$, i.e., the Čech cohomology of $L(F)$.

4.  To recover Cartan's and Leray's theorems, first replace $X$ by $\check C(U)$
and compute
$$RMap(X,F) = RMap(\check C(U),F) = RMap(hocolim_n \check C(U)_n, F) = holim_n RMap(\check C(U)_n, F).$$
In the mapping chain complex on the right, the object $\check C(U)_n$ is a coproduct of representable presheaves
given by iterated [[fiber products]] of maps in the covering family $U$.
In particular, $RMap(\check C(U)_n, F)$ can be computed as the product of individual derived mapping chain complexes
from individual [[fiber products]] to $F$.
The conditions of Cartan's and Leray's theorems guarantee that these derived mapping chain complexes
can be simply computed by evaluating $F$ on the corresponding representable objects.
(Here we must emphasize that it is not necessary to replace $F$ by $L(F)$, since instead we computed the derived mapping chain complexes directly.)
Therefore, $RMap(\check C(U),F)$ can be computed as the [[total complex]] of the Čech bicomplex of $F$ with respect to $U$.

## Related concepts

* [[simplicial presheaf]], [[model structures on simplicial presheaves]]

* [[chain complex]], [[model structures on chain complexes]]

* [[abelian sheaf cohomology]]
