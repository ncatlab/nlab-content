
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The *simplicial identities* encode the relationships between the face and degeneracy maps in a [[simplicial object]], in particular, in a [[simplicial set]].

## Definition

The **simplicial identities** are the duals to the _simplicial relations_  of coface and codegeneracy maps described at [[simplex category]]:

* $ d_i d_j  = d_{j-1}d_i$ if $i \lt j$,

* $d_i s_j$ can be written as
   *  $s_{j-1}d_i$  if  $i \lt j$,
   *  $id$    if   $i = j$ or   $j+1$,
   *  $s_j d_{i-1}$  if $i \gt j+1$,

* $s_i s_j  = s_j s_{i-1}$ if   $i \gt j$.

Here, the $d_i$ are the _face maps_ and the $s_i$ are the _degeneracy maps_.

[[!redirects simplicial identity]]