
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
* table of contents
{:toc}

## Idea

A _non-Hausdorff topological space_ is a [[topological space]] which is not a _[[Hausdorff topological space]]_.

## Examples

Since the [[full subcategory]] of [[Hausdorff topological spaces]] inside the [[category of topological spaces]] is [[reflective subcategory|reflective]], all [[limits]] in [[Top]] of [[diagrams]] of Hausdorff spaces are again Hausdorff spaces, but for [[colimits]] this fails in general ("non-Hausdorff quotients", the colimit in the subcategory is given by applying [[Hausdorff reflection]] to the colimit formed in [[Top]]). 

Hence examples of non-Hausdorff spaces generically arise from forming [[quotient topological spaces]] of Hausdorff spaces:

+-- {: .num_example #RQuotientedByQ}
###### Example

Consider the [[real line]] $\mathbb{R}$ regarded
as the 1-dimensional [[Euclidean space]] with its [[metric topology]] 
and consider the [[equivalence relation]] $\sim$ on $\mathbb{R}$ which identifies two [[real numbers]] if they
differ by a [[rational number]]:

$$
  \left(
    x \sim y
  \right)
    \;\Leftrightarrow\;
  \left(
    \underset{p/q \in \mathbb{Q} \subset \mathbb{R}}{\exists}
      x = y + p/q
  \right)
  \,.
$$

Then the [[quotient topological space]]

$$
  \mathbb{R}/\mathbb{Q}
    \;\coloneqq\;
  \mathbb{R}/\sim
$$

is a [[codiscrete topological space]], hence in particular a 
not a Hausdorff space.

=--

+-- {: .num_example}
###### Example

The [[line with two origins]].

=--



[[!redirects non-Hausdorff topological spaces]]