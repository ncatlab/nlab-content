+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Yoneda lemma for higher categories
#### $(\infty,n)$-Category theory
+--{: .hide}
=--
=--
=--


# Contents#
* table of contents
{: toc}


## Idea

The statement (not yet proved in general) of the Yoneda Lemma for higher categories should be the direct extension of the [[Yoneda lemma]] for [[categories]] and [[(infinity,1)-categories]] to the setting of other [[higher categories]].

## Yoneda embedding 
 {#YonedaEmbedding}

+-- {: .num_defn }
###### Definition

For $C$ an [[(∞,n)-category]] and $PSh(C)\coloneqq Func(C^\op, (\infty,(n-1)) Cat)$ its [[(∞,n)-category of (∞,n)-presheaves]], the **$(\infty,n)$-Yoneda embedding** is the [[(∞,n)-functor]]

$$
  y : C \to PSh(C)
$$


given by $y(X) : U \mapsto C(U,X)$.

=--



## Properties

### Yoneda lemma

+-- {: .num_prop }
###### Proposition
**$(\infty,n)$-Yoneda embedding**

Let $C$ be an [[(∞,n)-category]] and $PSh(C)$ be the corresponding [[(∞,n)-category of (∞,n)-presheaves]]. Then the canonical [[(∞,n)-functor]]

$$
  Y : C \to PSh(C) 
$$

is a [[full and faithful (∞,n)-functor]].

=--

+-- {: .num_prop }
###### Proposition
**$(\infty,n)$-Yoneda theorem**

For $C$ a small $(\infty,n)$-category and $F : C^{op} \to (\infty,(n-1)) Cat$ an $(\infty,n)$-functor, the composite

$$
  C^{op} \to PSh_{(\infty,1)}(C)^{op} \stackrel{Hom(-,F)}{\to}
  (\infty,(n-1)) Cat$$

is equivalent to $F$.

=--

### Preservation of limits


+-- {: .num_prop }
###### Proposition

The $(\infty,n)$-Yoneda embedding $y : C \to PSh(C)$ preserves all [[(∞,n)-limit]]s that exist in $C$.

=--
