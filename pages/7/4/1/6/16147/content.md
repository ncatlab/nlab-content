+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The [[action]] on a [[module]] over a [[monoid]] $A$ in a [[closed monoidal category]] $V$ may be equivalently encoded in terms of a $V$-[[enriched functor]] 
   
   $$
     \rho : \mathbf{B}A^{op} \to V
   $$ 

from the [[delooping]] one-object $V$-[[enriched category]] $\mathbf{B}A$, corresponding to $A$, to $V$ itself. 

   More generally it makes sense to replace $\mathbf{B}A$ by any $V$-[[enriched category]] $C$ -- regarded as the [[horizontal categorification]] of a monoid, a "monoid-oid" -- and think of a $V$-enriched presheaf $\rho : C \to V$ as a __module over the category__ $C$.

   From this perspective a $C$-$D$-[[bimodule]] is a $V$-[[enriched functor]] $C^{op}\times D \to V$, which is in this context known as a [[profunctor]] from $C$ to $D$. The notion of the [[bicategory]] $V Mod$ of $V$-enriched categories, $V$-profunctors between these and transformations between those is then a generalization of the category of monoids in $V$ and bimodules between them.

## Definition

Let $V$ be a [[closed monoidal category]]. Let $C$ be a $V$-[[enriched category]].

+-- {: .num_defn}
###### Definition
A **left module** over $V$ is a $V$-[[presheaf]] on $C$, i.e. a [[enriched functor|functor]] of $V$-[[enriched categories]]
  $$ M : C^{op} \longrightarrow V. $$
Dually a **right module** is a $V$-[[enriched functor]] $M : C \to V$.
=--

Let $C$ and $D$ be $V$-[[enriched categories]].

+-- {: .num_defn}
###### Definition
A $C$-$D$-**[[bimodule]]** is a $V$-[[enriched functor]]
  $$ C^{op} \otimes D \longrightarrow V, $$
i.e. a left $C \otimes D^{op}$-module.
=--

$C$-$D$-[[bimodules]] are also known as _[[profunctors]]_ or _[[distributor]]s_ from $C$ to $D$.

## Examples

### Modules over a ring

For $R$ a [[ring]], write $\mathbf{B}R$ for the [[Ab-enriched category]] with a single object and [[hom-object]] $R = \mathbf{B}R(\bullet, \bullet)$.

Then a left $R$-module $N$ is equivalently an [[Ab]]-[[enriched functor]]
$$   
  N : \mathbf{B}R^{op} \to Ab 
  \,.
$$

This makes manifest that the category $R$[[Mod]] is 
an [[Ab-enriched category]], namely the
[[Ab]]-[[enriched functor category]] 

$$
  R Mod \simeq [\mathbf{B}R,Ab]  
  \,.
$$

The right $R$-modules can be considered as $Ab$-functors $\mathbf{B}R\to Ab$. Then the usual [[tensor product of abelian groups]] $M\otimes N$ of left and right $R$-modules can be considered as a functor
  $$ \mathbf{B}R^{op}\otimes \mathbf{B}R\to Ab. $$
The [[coend]] $\int^R M\otimes N$ computes then to $M\otimes_R N$. 

### $G$-Sets
 {#GSetsAsPresheaves}

Classically the notion of module is always regarded internal to [[Ab]], so that a module is always an abelian group with extra structure. But noticing that such abelian ring modules are just enriched presheaves in [[Ab]]-[[enriched category theory]], it makes sense to consider enriched presheaves in general $V$-enriched category theory as a natural generalization of the notion of module.

For that generalization the case of [[Set]]-[[enriched category theory]] plays a special basic role:

a [[group]] $G$ (with no extra structure, i.e. just a [[set]] with group structure) is a monoid in [[Set]]. A module over $G$ in the sense of [[Set]]-[[enriched functor]] (just an ordinary [[functor]])

$$
  \mathbf{B}G \to Set
$$

is nothing but a **$G$-set**: a [[set]] equipped with a $G$-action.

$\mathbf{B}G$ is the [[small category]] that is the [[delooping]] [[groupoid]] of $G$, which has a single object and $Hom_{\mathbf{B}G}(\bullet,\bullet) = G$. The functor $\mathbf{B}G \to Set$ takes the single object to some set $S$ and takes each morphism $(\bullet \stackrel{g}{\to} \bullet)$ to an [[automorphism]] $\rho(g) : S \to S$ of that set, such that composition is respected. This is just a [[representation]] of $G$ on the set $S$.

Of course for this story to work, $G$ need not be a group, but could be any [[monoid]].

## Related concepts

* [[enriched presheaf category]]

## References

See the references at [[enriched category theory]] and [[profunctor]].

[[!redirects modules over an enriched category]]
[[!redirects module over enriched category]]
[[!redirects modules over enriched categories]]
[[!redirects enriched presheaf]]
[[!redirects enriched presheaves]]