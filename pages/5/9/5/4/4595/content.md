
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _stacked cover_ is a [[cover]] of a [[topological space]] which is indexed by a cover of another topological space, such that the product cover is a cover of the product space.


## Definition

+-- {: .un_defn}
###### Definition

Let $A,B$ be [[topological space]]s and $\mathcal{U}$ a [[numerable cover]] of $A$. Then a [[cover]] of the [[product]] space $A \times B$ is called a **stacked cover** of $A\times B$ over $\mathcal{U}$ -- denoted $\mathcal{U} \times \mathcal{S}$ -- , if there exists a [[function]] $\mathcal{S}$ -- called the **stacking function** -- which assignes to each set $U \in \mathcal{U}$ a cover $\mathcal{S}U$ of $B$, such that $\mathcal{U} \times\mathcal{S}$ consists of all the sets $U \times V$ with $V \in \mathcal{S}U$.

=--

## Properties

### General

+-- {: .un_prop}
###### Proposition

A stacked cover is itself a [[numerable cover]].

=--

### Stacked covers of products with the interval {#OfProductsWithInterval}

In this section  we let $B = [0,1]$ the standard [[interval]] and consider properties of stacked covers of spaces of the form $A \times [0,1]$.

+-- {: .un_prop}
###### Proposition

For $A$ a [[topological space]] and $\mathcal{W}$ a [[numerable cover]] of $A \times [0,1]$ there exists a refinement of $\mathcal{W}$ to a stacked cover $\mathcal{U} \times \mathcal{S}$ of $A \times [0,1]$ of the form

$$
  \{U_i \times [\frac{k-1}{r_i}, \frac{k+1}{r_i}] | r_i,k \in \mathbb{N}, 1 \leq k \leq r_i-1\}
  \,.
$$


=--


## References

Section A.2.17 of

* [[Albrecht Dold]], _Lectures on algebraic topology_ , Spring Verlag (1980)

[[!redirects stacked covers]]
[[!redirects stacked covering]]
[[!redirects stacked coverings]]
