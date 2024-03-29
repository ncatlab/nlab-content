
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
* table of contents
{:toc}

## Idea

A _geometric transformation_ is a [[morphism]] between [[geometric morphism]]s between [[topos]]es: a [[2-morphism]] in the [[2-category]] [[Topos]].


## Definition

For

$$
  f = (f^* \dashv f_*) : \mathcal{E} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} \mathcal{F}
$$

and

$$
  g = (g^* \dashv g_*) : \mathcal{E} \stackrel{\overset{g^*}{\leftarrow}}{\underset{g_*}{\to}} \mathcal{F}
$$

two [[geometric morphism]]s, a **geometric transformation** 

$$
  \eta : f \Rightarrow g
$$

is a [[natural transformation]] between the [[inverse image]] functors

$$
  f^* \Rightarrow g^*
  \,.
$$

By [[mate]]-calculus, these are in bijection to natural transformations of the [[direct image]] functors

$$
  g_* \Rightarrow f_*
  \,.
$$

## References

Section A4.1 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

[[!redirects geometric transformations]]