In a rather general form, a __representation__ of a category $C$ in category $D$ is simply a [[functor]] $F\colon C \to D$.  Similarly, an __intertwiner__ between representations is simply a [[natural transformation]] between functors when they are being thought of as representations.

The term 'representation' is most often used when one or more of the following conditions apply:
*  $D$ is the category $k$-[[Vect]] of vector spaces over some [[field]] $k$; one then has a __$k$-linear representation__.
*  $C$ is the [[delooping]] of a [[group]]; one then has a __group representation__ in $D$.  Such a representation gives us a specific object $V$ of $D$; we say that we have a representation of $G$ on $V$.
*  $C$ is the [[free category]] on a [[quiver]]; one then has a __quiver representation__.

Classical [[representation theory]] is about representations of groups on vector spaces, that is when the first two conditions apply.

+-- {: .query}
I don\'t agree with this $D \coloneqq Aut(V)$ business.  A $k$-linear representation of a group $G$ is a functor from $\mathbf{B}G$ to $k Vect$, period.  Because $\mathbf{B}G$ has one object (or is pointed), we can pick out an object $V$ of $k Vect$, and it was remiss of me not to mention this (and the language '*on* $V$' vs '*in* $D$'.  But we usually don\'t want $D$ to actually *be* $Aut(V)$ instead of $k Vect$; when doing representation theory, we fix $G$ and fix $k$ (or fix $D$ in some other way), but we don\'t fix $V$.  ---Toby
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
