In a rather general form, a __representation__ of a category $C$ in category $D$ is simply a [[functor]] $F\colon C \to D$.  Similarly, an __intertwiner__ between representations is simply a [[natural transformation]] between functors when they are being thought of as representations.

The term 'representation' is most often used when one or more of the following conditions apply:
*  $D$ is the category $k$-[[Vect]] of vector spaces over some [[field]] $k$; one then has a __$k$-linear representation__.
*  $C$ is the [[delooping]] of a [[group]]; one then has a __group representation__ in $D$.  Such a representation gives us a specific object $V$ of $D$; we say that we have a representation of $G$ on $V$.
*  $C$ is the [[free category]] on a [[quiver]]; one then has a __quiver representation__.

Part of classical [[representation theory]] is about representations of (topological, smooth etc.) groups on (topological) vector spaces, that is when the first two conditions apply. 

+-- {: .query}
I don\'t agree with this $D \coloneqq Aut(V)$ business.  A $k$-linear representation of a group $G$ is a functor from $\mathbf{B}G$ to $k Vect$, period.  Because $\mathbf{B}G$ has one object (or is pointed), we can pick out an object $V$ of $k Vect$, and it was remiss of me not to mention this (and the language '*on* $V$' vs '*in* $D$'.  But we usually don\'t want $D$ to actually *be* $Aut(V)$ instead of $k Vect$; when doing representation theory, we fix $G$ and fix $k$ (or fix $D$ in some other way), but we don\'t fix $V$.  ---Toby

If you look at the textbooks of representation of groups, then they start with representation of groups as homomorphisms of groups, that is just functors. Then they say, that usually the target groups are groups of automorphisms of some other objects. And at the end they say that one usually restricts just to linear automorphisms of linear objects when linearizing the general problematics to the linear one. Now the fact that in some special case there is a category which expresses the same fact does not extend to other symmetry objects, like for representations of vertex operator algebras, pseudotensor categories etc. I mean End(something) or Aut(something) is just inner end in some setup like in closed monoidal category, but there are symmetries in mathematics which have a notion of End of Aut for a single object but do not have good notion of category one level up which has inner homs leading to the same End or Aut. Conceptually actions are about endosymmetries or symmetries (automorphisms) being reducable to categorical ones but not necessarily, I think. In a way you say that you are sure that any symmetry of another object can be expressed internally in some sort of a higher category of such objects, what is to large extent true, but I am sure not for absolutely all examples.  

(for "on" terminology:) Ross Street uses monads in a 2-category and monads on a 1-category and I know of no objects in category theory. 

Another important thing is that the endomorphisms are by definitions often equipped with some additional (e.g. topological) structure which is not necessarily coming from some enrichement of the category of objects. --Zoran

(Zoran on word "classical representation" being just for groups: so the representations of associative algebras, Lie algebras, Leibniz algebras, topological groups, quivers, are not classical ??).
=--

There are also enriched, $k$-linear and other versions, hence one can talk about representations of [[Lie algebras]], [[vertex operator algebras]], etc. See also [[representation theory]]. 


[[!redirects representation]]
[[!redirects representations]]

[[!redirects intertwiner]]
[[!redirects intertwiners]]

[[!redirects linear representation]]
[[!redirects linear representations]]

[[!redirects group representation]]
[[!redirects group representations]]
[[!redirects representation of a group]]
[[!redirects representations of a group]]
[[!redirects representations of groups]]

[[!redirects quiver representation]]
[[!redirects quiver representations]]
[[!redirects representation of a quiver]]
[[!redirects representations of a quiver]]
[[!redirects representations of quivers]]
