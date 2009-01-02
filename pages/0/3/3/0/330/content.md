#Idea# 

One striking difference between Set Theory and Category Theory is that, while [[object|objects]] of a [[category]] need not have any other structure, a [[set]] comes equipped with the notion of _element_, identifying other sets which belong to it.  Sometimes, a category turns out to possess a similar structure, designating certain [[morphism|morphisms]] as **global elements** of an object.

#Definition#

If a category $C$ has a [[terminal object]] $1$, a **global element** of another object $x$ is a morphism $1\to x$.  

For example:
* In [[Set]], global elements are just elements: a function from a one-element set into $x$ picks out a single element of $x$.
* In [[Cat]], global elements are objects: the terminal category $1$ is the [[discrete category]] with one object, and a [[functor]] from $1$ into a category $C$ singles out an object of $C$.
* In a [[topos]], a global element of the [[subobject classifier]] is called a [[truth value]].
* Working in a [[slice category]] $C/b$, a global element of the object $\pi: e\to b$ is a map into it from the terminal object $1_b:b\to b$; i.e. a right inverse for $\pi$.  In the context of bundles, a global element is thus called a *global section*.