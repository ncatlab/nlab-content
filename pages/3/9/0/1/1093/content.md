
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

This entry is about the properties and the characterization of the category $Sh(S)$ of [[sheaf|sheaves]] on a [[site]] $S$ -- a [[Grothendieck topos]]. Among other things it does give a definition and a characterization of the notion of [[sheaf]] itself, but for more on the traditional information on [[sheaf|sheaves]] see there. 

## Definition

Consider a [[site]] $S$, i.e. a [[category]] $S$ equipped with a [[coverage]], a [[Grothendieck topology]].  Think of this topology equivalently as encoded in a system of [[local isomorphism]]s (see there) on the [[presheaf]] category $PSh(S) := [S^{op}, Set]$.

Then

* a [[sheaf]] on $S$ is precisely a [[presheaf]] $F \in [S^{op}, Set]$ such that $Hom_{PSh(S)}(-, F)$ sends all [[local isomorphism]]s to [[isomorphism]]s;

* the category $Sh(S)$ of [[sheaf|sheaves]] on $S$ is the full [[subcategory]] of the [[category of presheaves]] $PSh(S)$ on sheaves;

* the [[stuff, structure, property|fully faithful forgetful]] inclusion functor $i : Sh(S) \hookrightarrow PSh(S)$ has an [[adjoint functor|left adjoint]] $\bar{(-)} : PSh(S) \to Sh(S)$ -- [[sheafification]] -- which is [[exact functor|exact]] -- hence the inclusion is a [[geometric morphism]]:

  $$
    Sh(C) \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow} PSh(C)
    \,;
  $$

* the functor $L := i \circ \bar{(-)}: PSh(S) \to PSh(S)$ whose [[image]] is $Sh(S)$ has the property that $L(A_1 \to A_2)$ is an [[isomorphism]] if and only if $A_1 \to A_2$ is a [[local isomorphism]];

* the category of sheaves is equivalent to the [[homotopy category]] of the [[category with weak equivalences]] $PSh(C)$ with the weak equivalences given by $W = $[[local isomorphism]]s

$$
  Sh(S) \simeq Ho_{PSh(S)} = PSh(C)[local isomorphisms]^{-1}
  \,.
$$

* also the converse is true: for every [[exact functor|left exaxt]] functor $L : PSh(S) \to PSh(S)$ (preserving finite limits) which is [[adjoint functor|left adjoint]] to the inclusion of its image, there is a Grothendieck topology on $S$ such that the image of $L$ is the category of sheaves on $S$ with respect to that topology 

* Categories of sheaves are examples of [[category|categories]] that are [[topos]]es: they are the [[Grothendieck topos]]es characterized among all toposes as those satisfying [[Grothendieck topos|Giraud's axioms]].


In [[topos]]-theoretic language we therefore have that

+-- {: .standout}

[[Grothendieck topos|Sheaf toposes]] are precisely the [[geometric embedding|subtoposes]] of [[presheaf]] toposes.

=--

## Properties


Let $Sh(C)$ be a category of sheaves.

+-- {: .un_prop}
###### Proposition

A morphism $f : X \to Y$ is a [[monomorphism]] if it is a monomorphism of [[presheaves]], that is if for each $U \in C$ the [[function]] $f(U) : X(U) \to Y(U)$ is [[injective]].

=--


+-- {: .un_prop}
###### Proposition

A morphism $f : X \to Y$ in $Sh(C)$ is an [[epimorphism]] precisely if it is **locally surjective** in the sense that:

for all $U \in C$ there is a [[covering]] $\{p_i : U_i \to U\}_{i \in I}$ such that for all $i \in I$ and every element $y \in Y(U)$ the element $f(p_i)(y)$ is in the image of $f(U_i) : X(U_i) \to Y(U_i)$.


=--


## In higher category theory

The notion of _category of sheaves_ has analogs in [[higher category theory]].

For [[(∞,1)-category]] theory see [[(∞,1)-category of (∞,1)-sheaves]].



## References

For some standard references see the list of references at [[sheaf]] and [[topos]].

The characterization of sheaf toposes and Grothendieck topologiws in terms of left exact [[reflective subcategory|reflective subcategories]] of a presheaf category is in

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

where it is implied by the combination of Corollary VII 4.7 and theorem V.4.1.

The statement is also theorem A.4.4.8 in

* [[Peter Johnstone]], _[[Elephant|Sketches of an Elephant]]_ .



The characterization of $Sh(S)$ as the [[homotopy category]] of $PSh(S)$ with respect to local isomorphisms is emphasized at the beginning of the text

* [[Bertrand Toen]], _Stacks and non-abelian cohomology_ ([web](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/index.html)) .

Details are in 

* Kashiwara-Schapira, _[[Categories and Sheaves]]_ .

It's a bit odd that the full final statement does not seem to be stated there explicitly, but all the ingredients are discussed:

* exercise 16.7 shows that [[sheafification]] inverts precisely the [[local isomorphism]]s, so that in particular every [[local isomorphism]] between [[sheaf|sheaves]] is an [[isomorphism]];

* lemma 16.3.2 states that the unit of the [[adjoint functor|adjunction]] $Id_{PSh(S)} \rightarrow i \circ \bar{(-)} : PSh(S) \to PSh(S)$ is componentwise a [[local isomorphism]];

* using this corollary 7.2.2 says that $Sh(S) \simeq Ho_{PSh(S)}$ with the [[homotopy category]] $Ho_{PSh(S)}$ formed using [[local isomorphism]]s as weak equivalences.



The entirely analogous story in the wider context of [[(infinity,1)-category|(infinity,1)-categories]] is in

* [[Charles Rezk]], _Toposes and homotopy toposes_ ([pdf](http://www.math.uiuc.edu/~rezk/homotopy-topos-sketch.pdf))

and

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

For more on this see [[(∞,1)-category of (∞,1)-sheaves]] and [[models for ∞-stack (∞,1)-toposes]].


[[!redirects sheaf category]]
[[!redirects categories of sheaves]]
[[!redirects topos of sheaves]]
[[!redirects topoi of sheaves]]
[[!redirects toposes of sheaves]]
