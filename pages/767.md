Often [[site]]s are required to be [[small category|small categories]].  If not, there are complications.

Many of the good properties of [[sheaf|sheaves]] depend on such smallness.  To begin with, even the category of sheaves may have to be extra-large, but there are other issues, such as:

* the existence of [[sheafification]],
* the existence of [[colimit|colimits]] in the category of sheaves,
* [[cartesian closed category|cartesian closedness]] of the category of sheaves, and
* the category of sheaves being a [[topos]].

However, for many purposes it is desirable to consider the notion of sheaves on large sites.  In some cases, sheaves on a large site can be identified with sheaves on some small full sub-site.  For example, if $C$ is a [[Grothendieck topos]] with its [[subcanonical coverage|canonical coverage]], then every sheaf on $C$ is representable, so $C\simeq Sh(C)$; thus $Sh(C)$ is equivalent to the category of sheaves on some small site (a defining site for $C$ itself).

On the other hand, one sometimes wants to consider sheaves on [[large category|large categories]] such as [[Top]] or [[Diff]], which are certainly not Grothendieck toposes.  One way to deal with this is to consider [[full subcategory|full subcategories]] of these large categories on objects whose size is bounded by some large (in the non-technical sense) [[cardinal number]] $\kappa$.  In an extreme case, $\kappa$ could be an [[inaccessible cardinal]].  The idea is that for sheaves and in particular for any [[homotopy theory]] of sheaves the choice of these cardinality bounds is "inessential."

See for instance [p. 2](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=2) of Jardine, [Fields Lectuere: Simplicial presheaves](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf) where this issue arises in the study of [[simplicial presheaf|simplicial presheaves]] and the [[model structure on simplicial presheaves]].

+-- {: .query}
Can any of you size-issue experts help to clarify this?

_Mike_: I wish.  I added some stuff, but I still don't really understand this business.  In particular I don't really know what is meant by "inessential."  It certainly seems unlikely that you would  get _equivalent_ homotopy theories, but it does seem likely that you would get similar behavior no matter where you draw the line.  And if all you care about is, say, having a good category of sheaves in which you can embed any _particular_ space or manifold you happen to care about, then that may be good enough.  But I don't really know what the goal is of considering such large sites.
=--


[[!redirects large sheaf]]
[[!redirects sheaves on large sites]]