+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Enriched category theory
+-- {: .hide}
[[!include enriched category theory contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[homotopy type theory]], [[types]] represent [[infinity-groupoids|$\infty$-groupoids]], so there should be something similar to [[enriched (infinity,1)-category|enriched]] $\infty$-groupoids in homotopy type theory. 

## Definition

Let $C$ be the [[subtype]] of [[types]] in a [[type universe]] $\mathcal{U}$ which satisfy a certain [[predicate]] $P$: for all types $T:C$, there is a [[term]] $p:P(T)$.

Then a type $T$ is *$C$-enriched* if for all terms $a:T$ and $b:T$, there is a [[dependent type|dependent]] term $p(a,b):P(a = b)$, where $a = b$ is the [[identity type]] of $a$ and $b$ in $T$. 

## Examples

* One could define [[Ab|$Ab$]]-enriched types, which are types whose identity types are all [[abelian groups]] (usually defined with a predicate $isAbelianGroup$). 

* Similarly, [[sets]] are [[Prop|$Prop$]]-enriched types, and [[homotopy n-type|$n$-types]] are $(n - 1)$Type-enriched types. 

## Categorical semantics

Under the [[relation between type theory and category theory]], enriched types should correspond to [[enriched (infinity,1)-category|enriched]] [[infinity-groupoids|$\infty$-groupoids]] in [[higher category theory]]. 

## See also

* [[enriched category]]
* [[enriched (infinity,1)-category]]

[[!redirects enriched types]]
