
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

This entry means to indicate a generalization of the notion of [[adjoint functors]] from [[category theory]] to [[2-category theory]], but specialized to the case of [[strict 2-categories]].

Notice that [[strict 2-categories]] may be understood as [[Cat]]-[[enriched categories]], for [[Cat]] understood as the *[[1-category]]* of [[small categories|small]] [[strict categories]] with [[functors]] between them and equipped with its [[cartesian monoidal category|cartesian monoidal]]-[[structure]] (via forming [[product categories]]). 

In this sense the respective notion of adjoint 2-functors between strict 2-categories is that of *[[Cat]]-[[enriched adjoint functors]]*, which (by the discussion there) is equivalently that of [[adjunctions]] in the [[2-category]][[VCat|$\mathcal{V}Cat$]], for $\mathcal{C} = $ [[Cat]].

The following indicates what this means in more explicit detail.

## Definition

Given a [[pair]] of [[strict 2-functors]] between [[strict 2-categories]]

$$
  F 
    \,\colon\, 
  A \rightleftarrows C
    \,\colon\,
  U
$$

a *strict 2-adjunction* between them is, equivalently:

* for each [[pair]] of [[objects]] $a \in A$, $c\in C$, a [[natural isomorphism]] of [[strict categories|strict]] [[hom-categories]] 
 
  $$
    C\big(F(a), c\big) \,\cong\, A\big(a, U(c)\big)
  $$  

  which is [[strict 2-natural transformation|strict 2-natural]] in $a$ and $c$;

* a pair of [[strict 2-natural transformation|strict 2-natural transformations]] of 2-functors: 

   1. [[adjunction unit]] $\; \eta \colon Id_A \to U F$, 

   1. [[adjunction counit]] $\; \epsilon \colon F U \to Id_B$, 


  satisfying the [[triangle identities]] strictly.  


## Related concepts

For more general notions of *2-adjunctions*, involving [[weak 2-categories]], [[weak 2-functors]], and/or weak 2-natural transformations; see at *[[2-adjunction]]*.

[[!redirects strict adjoint 2-functors]]

[[!redirects strict 2-adjunction]]
[[!redirects strict 2-adjunctions]]




