
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Big sites
* table of contents
{: toc}

## Idea

For $C$ a [[site]] and $c \in C$ an [[object]], the [[slice category]] $C/c$ may naturally be thought of as a generalization of the notion of [[category of open subsets]] of $c$ in the case of $C = $ [[Top]]: its [[object]]s are probes of $c$ by arbitrary other objects of $C$.

The over-category naturally inherits the structure of a [[site]] itself -- this is called the _big site_ of $C$. The corresponding [[sheaf topos]] $Sh(C/c)$ is the [[topos]]-incarnation of the object $c$.


## Definition

Let $C$ be a category equipped with a [[pretopology]] $J$ (i.e. a [[site]]) and let $a$ be an object of $C$. The [[slice category]] $C/a$ inherits a pretopology by setting the covering families to be those collections of morphisms whose image under $C/a \to C$ form a covering family. This is then the **big site** of $a$.

In the special case that $C$ is some category of spaces with a terminal object $t$, then sheaves on the big site of $t$ form a [[gros topos]]. Hence the category of sheaves on the big site of $a$ generalize this idea.

## Examples
 {#Examples}

* For $C$ the category of ([[affine scheme|affine]]) [[schemes]], with one of its [[Grothendieck topologies]], notably the [[etale topology]] or [[Zariski topology]], for $X$ a [[scheme]], $Sch/S$ is traditionally called _the [[étale site]] of $X$_ or _the [[Zariski site]] of $X$_. See for instance ([[The Stacks Project|The Stacks project, def. 38.27.3]]).

## Related concepts

* [[little site]]



[[!redirects big site]]
[[!redirects big sites]]

[[!redirects gros site]]
[[!redirects gros sites]]

[[!redirects slice site]]
[[!redirects slice sites]]


[[!redirects large site of an object in a site]]
[[!redirects large sites of objects in a site]]
[[!redirects large sites of objects in sites]]


