This entry is about the properties and the characterization of the category $Sh(S)$ of [[sheaf|sheaves]] on a [[site]] $S$. Among other things it does give a definition and a characterization of the notion of [[sheaf]] itself, but for more on the traditional information on [[sheaf|sheaves]] see there. This entry here is to be compared with the entry [[(infinity,1)-category of (infinity,1)-sheaves]] of which it is the 1-categorical shadow.

#Contents#
* automatic table of contents goes here
{:toc}

#Definition#

Consider a [[site]] $S$, i.e. a [[category]] $S$ equipped with a [[Grothendieck topology]].  Think of this topology equivalently as encoded in a system of [[local isomorphism]]s (see there) on the [[presheaf]] category $PSh(S) := [S^{op}, Set]$.

Then

* a [[sheaf]] on $S$ is precisely a [[presheaf]] $F \in [S^{op}, Set]$ such that $Hom_{PSh(S)}(-, F)$ sends all [[local isomorphism]]s to [[isomorphism]]s;

* the category $Sh(S)$ of [[sheaf|sheaves]] on $S$ is the full [[subcategory]] of the category of $PSh(S)$ on sheaves;

* the [[stuff, structure, property|fully faithful forgetful]] inclusion functor $i : Sh(S) \hookrightarrow PSh(S)$ has an [[adjoint functor|left adjoint]] $\bar{(-)} : PSh(S) \to Sh(S)$ -- [[sheafification]] -- which is [[exact functor|exact]] -- hence the inclusion is a [[geometric morphism]].

* the functor $L := i \circ \bar{(-)}: PSh(S) \to PSh(S)$ whose [[image]] is $Sh(S)$ has the property that $L(A_1 \to A_2)$ is an [[isomorphism]] if and only if $A_1 \to A_2$ is a [[local isomorphism]];

* the category of sheaves is equivalent to the [[homotopy category]] of [[presheaf|presheaves]] with respect to weak equivalences given by [[local isomorphism]]
$$
  Sh(S) \simeq Ho_{PSh(S)}
  \,.
$$

* also the converse is true: for every [[exact functor|left exaxt]] functor $L : PSh(S) \to PSh(S)$ (preserving finite limits) which is [[adjoint functor|left adjoint]] to the inclusion of its image, there is a Grothendieck topology on $S$ such that the image of $L$ is the category of sheaves on $S$ with respect to that topology 


#Relation to topos theory#

Categories of sheaves are examples of [[category|categories]] that are [[topos]]es: they are the [[Grothendieck topos]]es.


#References#

For some standard references see the list of references at [[sheaf]] and [[topos]].

The characterization of $Sh(S)$ as the homotopy category of $PSh(S)$ with respect to local isomorphisms is emphasized at the beginning of the text

* B. To&#235;n, _Stacks and non-abelian cohomology_ ([web](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/index.html)) .

Details are in 

* Kashiwara-Schapira, [[Categories and Sheaves]] .

It's a bit odd that the full final statement does not seem to be stated there explicitly, but all the ingredients are discussed:

* exercise 16.7 shows that [[sheafification]] inverts precisely the [[local isomorphism]]s, so that in particular every [[local isomorphism]] between [[sheaf|sheaves]] is an [[isomorphism]];

* lemma 16.3.2 states that the unit of the [[adjoint functor|adjunction]] $Id_{PSh(S)} \rightarrow i \circ \bar{(-)} : PSh(S) \to PSh(S)$ is componentwise a [[local isomorphism]];

* using this corollary 7.2.2 says that $Sh(S) \simeq Ho_{PSh(S)}$ with the [[homotopy category]] $Ho_{PSh(S)}$ formed using [[local isomorphism]]s as weak equivalences.



The entirely analogous story in the wider context of [[(infinity,1)-category|(infinity,1)-categories]] is the central statement of

* [[Jacob Lurie]], [[Higher Topos Theory]] .

For more on this see [[(infinity,1)-category of (infinity,1)-sheaves]].

***

