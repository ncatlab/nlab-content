
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

For $C$ a [[site]]n and $c \in C$ an [[object]], the [[over category]] $C/c$ may naturally be thought of as a generalization of the notion of [[category of open subsets]] of $c$ in the case of $C = $ [[Top]]: it's [[object]]s are probes of $c$ by arbitrary other objects of $C$.

The over-category naturally inherits the structure of a [[site]] itself -- this is called the _big site_ of $C$. The corresponding [[sheaf topos]] $Sh(C/c)$ is the [[topos]]-incarnation of the object $c$.


## Definition

Let $C$ be a category equipped with a [[pretopology]] $J$ (i.e. a [[site]]) and let $a$ be an object of $C$. The [[slice category]] $C/a$ inherits a pretopology by setting the covering families to be those collections of morphisms whose image under $C/a \to C$ form a covering family. This is then the **big site** of $a$.

In the special case that $C$ is some category of spaces with a terminal object $t$, then sheaves on the big site of $t$ form a [[gros topos]]. Hence the category of sheaves on the big site of $a$ generalize this idea.

## Related concepts

* [[small site]];

* **big site**


[[!redirects big site]]
[[!redirects big sites]]

[[!redirects gros site]]
[[!redirects gros sites]]

[[!redirects large site of an object in a site]]
[[!redirects large sites of objects in a site]]
[[!redirects large sites of objects in sites]]
