
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **Segal category** is one of the models for that of [[(∞,1)-category]]. 

It can be understood as modelling the notion of an [[SSet]]-[[enriched category|enrichment]] _up to [[coherence|coherent]] [[homotopy]]_ , i.e. a _weak_ enrichment. As such it is very similar to the notion of [[complete Segal space]].



## Definition

+-- {: .un_def}
###### Definition

A __Segal category__ is 

* a simplicial simplicial set ([[bisimplicial set]]) $X$

* such that $X_0$ (the set of points) is a discrete (= constant) simplicial set

* the morphisms

  $$ 
    \phi_k: X_k \to X_1 \times_{X_0} \cdots \times_{X_0} X_1 \;\;(k factors)
  $$

  induced by the face maps $X_{\{0,\cdots ,k\}} \to X_{\{i,i+1\}}$ for $0 \leq i \leq k-1$ are [[model structure on simplicial sets|weak equivalences of simplicial sets]] for $k \geq 2$.

=--

+-- {: .un_remark}
###### Remark

The object $X_1 \times_{X_0} X_1$ has the interpretation as the space of composable 1-[[morphism]]s in $X$. The weak equivalence $X_2 \to X_1 \times_{X_0} X_1 $ given by the above definition together with the remaining face map $\delta^1 : X_2 \to X_1$ provide an [[∞-anafunctor]]

$$
  \array{
    X_2 &\stackrel{\delta1}{\to}& X_1
    \\
    {}^{\mathllap{\simeq}}\downarrow
    \\
    X_1 \times_{X_0} X_1
  }
$$

that encodes the composition operation in the Segal category $X$. 

=--

## References

Segal categories were defined in 1974 (implicitly) by [[Graeme Segal]]. They were named Segal categories first by [[William Dwyer]], [[Daniel Kan]], [[Jeff Smith]] in 1989. 

An overview is on pages 164 to 169 of

* [[Andre Joyal]], _The theory of Quasi-Categories and its Applications_ notes from a lecture at [Simplicial Methods in Higher Categories](http://www.crm.cat/HigherCategories/)

A discussion with emphasis on the comparison of the various [[model category]] structures is in

* [[Julia Bergner]], _A survey of $(\infty, 1)$-categories_ ([arXiv](http://arxiv.org/abs/math.AT/0610239))



[[!redirects Segal categories]]

[[!redirects Segal groupoid]]
[[!redirects Segal groupoids]]