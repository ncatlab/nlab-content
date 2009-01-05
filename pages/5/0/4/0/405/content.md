#Idea#

The **cube category** $\Box$ encodes one of the main [[geometric shapes for higher structures]].

Its objects are the standard "$n$-cubes", for $n \in \mathbb{N}$ and its morphisms are all possible ways of mapping cubes to each other.

#Definition#

A precise definition of the cube category by generators and relations can be found in section 2 of

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega-Cat$_ ([web](http://crans.fol.nl/papers/thten.html), [ps](http://crans.fol.nl/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

Alternatively, the cubical category can be defined as the initial strict monoidal category $(M, \otimes, I)$ equipped with an object $x$ together with two maps $i_0, i_1: I \to x$ and a map $p: x \to I$ such that $p i_0 = 1_I = p i_1$. (The object $x$ may be thought of as the "generic interval" and the monoidal unit $I$ as a point; $x^{\otimes n}$ thus becomes the combinatorial $n$-cube.) 

This is similar to how the (augmented) simplicial category $\Delta$ may be described as the initial strict monoidal category equipped with a monoid. This style of definition also opens up the possibility of using string diagrams to visualize the structure of $\Box$ and $\Delta$. 
 
The cube category is used to define [[cubical set|cubical sets]].

##Remarks##

Among all [[geometric shapes for higher structures]] cubes are best suited for describing Gray-like [[tensor product|tensor products]] of higher structures: there is geometrically obvious way in which to combine the $n$-cube $[n]$ and the $m$-cube $[m]$ to the $(n+m)$-cube $[n] \otimes [m] := [n+m]$. This makes $\Box$ into a [[monoidal category]]. It also induces the canonical monoidal structure on [[cubical set|cubical sets]] and then on [[strict omega-category|strict omega-categories]].

category: category