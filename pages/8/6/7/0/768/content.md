A **classifying space** for some sort of data refers to a space (or a more general object), usually written $\mathcal{B}(data)$, such that maps $X\to \mathcal{B}(data)$ correspond to data over $X$.

The classical example is the classifying space $\mathcal{B}G$ of a [[group]] $G$, which has the property that there is a bijection between [[homotopy]] classes of maps $X\to \mathcal{B}G$ and isomorphism classes of $G$-[[bundle|bundles]] over $X$.  (In fact, one can jack this up to an equivalence of [[groupoid|groupoids]] or $\infty$-[[infinity-groupoid|groupoids]].)  Various improvements of this are possible which classify bundles with extra structure or [[fibration|fibrations]].

Categorically, the corresponding statement is that [[Grothendieck fibration]]s over a [[category]] $X$ correspond to [[pseudofunctor]]s $X^{op}\to Cat$.  Thus $Cat$ is the "classifying space for categories."  Similarly, discrete fibrations over $X$ correspond to [[functor]]s $X^{op}\to Set$.

To see the connection between the two, consider the case when $X$ is a groupoid and we restrict the fibers of the fibration to be isomorphic to a given set $F$.   Then the functor $X^{op}\to Set$ must land in the subcategory of $Set$ consisting of just the [[automorphism]]s of $F$, which is the one-object groupoid corresponding to the [[automorphism group]] $Aut(F)$.  If we further restrict the automorphisms appearing to preserve some given structure on $F$, so that they lie in some smaller group $G$, then the "classifying space" will be the one-object groupoid corresponding to $G$.  Under the [[homotopy hypothesis]], groupoids correspond to [[homotopy 1-type]]s, and the one-object groupoid of a group $G$ corresponds precisely to the usual topological classifying space $\mathcal{B}G$ (in fact, this is one _construction_ of $\mathcal{B}G$).  For this reason, $\mathbf{B}G$ is often used to denote that one-object groupoid; see the [[delooping hypothesis]] and the discussion at [[category algebra]].

The phrase "classifying space" is also sometimes used for the realization of the nerve of any category, although it is more complicated to say what exactly this space "classifies."  (One answer is "torsors modulo concordance.")


# Classifying spaces for crossed complexes

The notion of classifying space should be regarded in general terms as giving a functor 

$$  \mathcal{B} :(algebraic data) \to (topological data).$$

Composition with a forgetful functor $U: (topological data) \to (topological spaces) $ gives a [[classifying space]]. In such cases one would also like a homotopically defined functor 

$$ \Xi: (topological data) \to (algebraic data) $$

such that 

1. $\Xi \circ \mathcal{B}$ is equivalent to the identity; 

1. $\Xi$ preserves certain colimits (Generalised [[van Kampen theorem]]) allowing some calculation;

1. there are notions of homotopy for both types of data leading to a bijection of homotopy classes for some $X$ 

$$[X,U\mathcal{B}C] \cong [\Xi X_*, C].$$

This happens for the algebraic data of crossed complexes and the topological data of filtered spaces, when $X$ is a CW-complex, and $\Xi$ is the fundamental crossed complex of a filtered space. Thus in this case the classifying space does classify homotopy classes of maps, and more work is needed to sort out the data over $X$ which this classifies (gerbes?). 

However $\mathcal{B}C$ is in this case defined by a nerve construction which generalises that for groupoids, and can also be applied to topological crossed crossed complexes, giving a simplicial space. 

+--{: .query}
[[Mike Shulman|Mike]]: I don't really get any intuition from that.  There might be lots of functors from "algebraic data" to "topological data" but it seems to me that only particular sorts of them deserve the name "classifying space."  Can you say more specifically what sorts of functors you have in mind, and relate it to the more basic ideas that I am familiar with?  What do these classifying spaces classify?

[[Ronnie Brown|Ronnie]] What I am trying to characterise is that higher categories carry structure such as a filtration by lower dimensional higher categories, or, for multiple structures, a multiple filtration. Thus one expects a classifying space to inherit this extra structure. Conversely, the construction of an infinity-groupoid from a space might depend on this extra structure. 

So I spent 9 years trying to construct a _strict_ homotopy double groupoid of a space, yet Philip Higgins and I did this overnight in 1974 when we tried the simplest relative example we could think of: take homotopy classes of maps from a square to $X$ which take the edges to a subspace $X_1$ and the vertices to a base point $x_0$. Then the filtered case took another 4 years or so to complete. 

Then Loday constructed a [[cat-n-group]] from an n-cube of spaces, published in 1982. Its multi-nerve  is an $(n+1)$-simplicial set, whose realisation is $(n+1)$-filtered. 

A strict homotopy double groupoid of a Hausdorff space has been constructed but this needs a subtle notion of [[thin element|thin]] homotopy.

Of course the filtration for a group is not so apparent, but it is more clear that  [[groupoid]]s  carry structure in dimension 0 and 1, and hence are useful for representing non connected homotopy 1-types, and their identifications in dimension 0, as explained in the first edition (1968) of my Topology book.   

The intuition for the [[higher homotopy van Kampen theorem]] is that you need _structure in all  dimensions from 0 to n _to get colimit theorems in dimension n, because in homotopy, low dimensional identifications, even in dimension 0,  usually effect high dimensional homotopy information. In effect, the [[higher homotopy van Kampen theorem]] is about gluing [[homotopy n-type]]s. 

_Mike_: Thanks, that is helpful.
=--

Some such constructions arise from generalisations of the [[Dold-Kan correspondence]], with values in [[simplicial set]]s. For example, from a [[crossed complex]] $C$ one obtains a simplicial  set $Nerve(C)$ which in dimension $n$ is $Crs(\Pi(\Delta^n_*),C)$. The geometric realisation $\mathcal{B}C$ of this is canonically filtered by the skeleta of $C$, so $\mathcal{B}$ is really a functor to [[filtered space]]s. This ties in with the functor $\Pi$ which goes in the opposite direction. But note that there is a different filtration of the space $\mathcal{B}C$ since it is a CW-complex, and so $\Pi$ of this filtration gives a free crossed complex. 

Special cases of crossed complexes are [[groupoid]]s, and so we get the classifying space of a groupoid; and similarly of a [[crossed module]]. 

A crossed module is equivalent to a category object in groups, and so a nerve of this can be constructed as a bisimplicial set. The geometric realisation of this is naturally bifiltered, in several ways!

In considering what is desirable for a [[fundamental infinity-groupoid]] one should bring the notion of classifying space, and its inherited structure, into account. 
# Classifying spaces for simplicial groups

The W-bar construction which gives the classifying space functor for simplicial groups and simplicially enriched groupoids is given in the entry on [[simplicial group|simplicial groups]].  It provides a good example of the above as the W-bar functor is right adjoint to the [[Dwyer-Kan loop groupoid]] functor and induces an equivalence of homotopy categories between that of simplicial sets and that of simplicially enriched groupoids.
The simplicial sets here are playing the role of 'topological data'.

#Moduli spaces#

The notion of **[[moduli space]]** is closely related to that of classifying space, but has some subtle differences. See there for more on this.
