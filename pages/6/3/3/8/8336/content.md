
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The standard [[interval object]] in a [[category of chain complexes]] in $R$[[Mod]] is an "abelianization" of the standard simplicial interval, the 1-[[simplex]] and a model of the unit interval, $[0,1]$, with the evident cell decomposition.

## Definition

Let $R$ be some [[ring]] and let $\mathcal{A} = R$[[Mod]] be the [[abelian category]] of $R$-[[modules]]. Write $Ch_\bullet(\mathcal{A})$ for the corresponding [[category of chain complexes]].

+-- {: .num_defn}
###### Definition

The standard **interval object in chain complexes**

$$
  I_\bullet \in Ch_\bullet(\mathcal{A})
$$

is the [[normalized chain complex]] of the [[chain on a simplicial set|simplicial chains]] on the simplicial 1-[[simplex]]:

$$
  I_\bullet \coloneqq N_\bullet(C(\Delta[1]))
  \,.
$$

In components this means that

$$
  I_\bullet = 
  [
    \cdots \to 0 \to 0 \to R \stackrel{(id,-id)}{\to}
   R \oplus R
  ]
  \,.
$$

=--

## Properties

### Homotopies


+-- {: .num_prop}
###### Proposition

A [[homotopy]] with respect to $I_\bullet$ gives a 
[[chain homotopy]] and conversely. 

=--

See the entry on [[chain homotopy]]  for more details.



[[!redirects interval in chain complexes]]
[[!redirects intervals in chain complexes]]
