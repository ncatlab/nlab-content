#Idea#

The **cube category** $\Box$ encodes one of the main [[geometric shapes for higher structures]]. It is also called the [[cubical category]], although that term can be ambiguous.

Its objects are the standard cellular  "$n$-[[cube|cubes]]", for $n \in \mathbb{N}$ and its morphisms are all possible ways of mapping cubes to each other.

#Definition#

+-- {: .un_defn}
###### Definition
The **cube category** is the initial strict [[monoidal category]] $(M, \otimes, I)$ equipped with an object $int$ together with two maps $i_0, i_1: I \to int$ and a map $p: int \to I$ such that $p i_0 = 1_I = p i_1$. 
=--

+--{.query}
Do we have a similar definiton of the [[globe category]]?

[[Todd Trimble|Todd]]: None that I know of; the globe category doesn't carry a monoidal structure. But it reminds me that we should create an entry for Joyal's category $\Theta$, used in his definition of weak $omega$-category, as this cleverly combines globes and simplices. 
=--

##Remarks##

* The cube category is used to define [[cubical set|cubical sets]].

* The object $int$ may be thought of as the "generic interval" and the monoidal unit $I$ as a point; $x^{\otimes n}$ thus becomes the combinatorial $n$-cube. Indeed, the [[cubical set]] represented by $I$ is the standard cubical 0-cube, while the cubical set represented by $int$ is the standard cubical 1-cube.

* An explicit description of the cube category by generators and relations is in section 2 of

  * Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega-Cat$_ ([web](http://crans.fol.nl/papers/thten.html), [ps](http://crans.fol.nl/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

* Among all [[geometric shapes for higher structures]] cubes are best suited for describing Gray-like [[tensor product|tensor products]] of higher structures: there is geometrically obvious way in which to combine the $n$-cube $[n]$ and the $m$-cube $[m]$ to the $(n+m)$-cube $[n] \otimes [m] := [n+m]$. This makes $\Box$ into a [[monoidal category]]. It also induces the canonical monoidal structure on [[cubical set|cubical sets]] and then on [[strict omega-category|strict omega-categories]]: the [[Crans-Gray tensor product]].

category: category