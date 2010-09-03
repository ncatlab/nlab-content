
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

An **equalizer** is a [[limit]] 

<center><img src="http://latex.codecogs.com/gif.latex?
\xymatrix{
eq\ar[r]_{e} %26 x \ar@%3C.5ex%3E [r]^{f}\ar@%3C-.5ex%3E[r]_{g} %26 y
}" />
</center>


over a parallel pair i.e. of the [[diagram]] of the shape 

$$
  \left\lbrace
      x \stackrel{\overset{f}{\to}}{\underset{g}{\to}} y
  \right\rbrace
  \,.
$$

(See also [[fork]] diagram).

This means that for $f : x \to y$ and $g : x \to y$ two [[parallel morphisms]] in a [[category]] $C$, their equalizer is, if it exists

* an object $eq(f,g) \in C$;

* a morphism $eq(f,g) \to x$

* such that 

  * pulled back to $eq(f,g)$ both morphisms become [[equality|equal]]: $ (eq(f,g) \to x \stackrel{f}{\to} y) = (eq(f,g) \to x \stackrel{g}{\to} y) $
  * and $eq(f,g)$ is the [[universal property|universal object]] with this property.

The dual concept is that of [[coequalizer]].

## Examples

* In $C =$ [[Set]] the equalizer of two functions of sets is the subset of elements of $c$ on which both functions coincide.
$$
  eq(f,g)
  = 
  \left\{
     s \in c | 
     f(s) = g(s)
  \right\}
  \,.
$$

* For $C$ a category with [[zero object]] the equalizer of a morphism $f : c \to d$ with the corresponding [[zero morphism]] is the [[kernel]] of $f$.


[[!redirects equalizers]]
[[!redirects equaliser]]
[[!redirects equalisers]]