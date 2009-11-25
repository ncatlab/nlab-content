
#Contents#
* automatic table of contents goes here
{:toc}

## Defintion ##

An **inverse** of a [[morphism]] $f : X \to Y$ in a [[category]] (or an element of a [[monoid]]) is another morphism $f^{-1} : Y \to X$ which is both a left-inverse (a [[retraction]]) as well as a right-inverse (a [[section]]) of $f$, in that 
$$
  f \circ f^{-1} : Y \to X \to Y 
$$
equals the [[identity morphism]] on $Y$ and
$$
  f^{-1} \circ f : X \to Y \to X 
$$
equals the [[identity morphism]] on $X$.


## Remarks ##

* A morphism which has an inverse is called an [[isomorphism]].

* The inverse $f^{-1}$ is unique if it exists.

* The inverse of an inverse morphism is the original morphism, $(f^{-1})^{-1} = f$.

* A category in which all morphisms have inverses is called a [[groupoid]].

* An amusing exercise is to show that if $f,g,h$ are morphisms such that $f\circ g,\; g\circ h$ are defined and are isomorphisms, then $f,g,h$ are all isomorphisms. 

  * This is a special case of the **2-out-of-6-property** which is satisfied by the _weak equivalences_ in any [[homotopical category]].

  * When this is applied to a  homotopy category such as $HTop$ it implies the construction of and formulae for certain homotopies. 


## Inverses in non-associative contexts ##

These can be a little more complicated; see [[quasigroup]] for some discussion of the one-object version.


[[!redirects inverse element]]
[[!redirects inverse morphism]]