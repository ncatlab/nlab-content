
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[quotient group]] $\mathbb{Q}/\mathbb{Z}$ of the additive [[abelian group]] of [[rational numbers]] by its [[subgroup]] of [[integers]].

It is also the [[coequalizer]] of the [[identity function]] of the rational numbers and the function $x \mapsto x + 1$ on the rational numbers:

$$
\mathbb{Q}\underoverset{\quad x \mapsto x + 1 \quad}{\mathrm{id}_{\mathbb{Q}}}{\rightrightarrows}\mathbb{Q} \to \mathbb{Q}/\mathbb{Z}
$$

## Properties

### Relation to cyclic groups

For each [[natural number]] $n \in \mathbb{N}$ the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$ is a [[subgroup]]

$$
  \array{
    \mathbb{Z}/n\mathbb{Z} 
    &\overset{\;\;\;\;\;\;}{\hookrightarrow}&
    \mathbb{Q}/\mathbb{Z}
    \\
    [k]
    &\mapsto&
    [k/n]
  }
$$

In fact $\mathbb{Q}/\mathbb{Z}$ is the [[filtered colimit]] of a [[diagram]] of cyclic groups and [[inclusions]] between them. In more detail, whenever $m|n$, multiplication by $n/m$ induces an inclusion 

$$\mathbb{Z}/m\mathbb{Z} \hookrightarrow \mathbb{Z}/n\mathbb{Z}$$ 

and this gives a [[functor]] to [[abelian groups]] from the [[lattice]] of [[natural numbers]] ordered by divisibility. The [[colimit]] of this functor is the [[abelian group]] $\mathbb{Q}/\mathbb{Z}$. 

### Relation to Prüfer groups

For each [[prime number|prime]] $p$ the $p$-[[Prüfer group]] $\mathbb{Z}[1/p]/\mathbb{Z}$, similarly formed as the colimit of groups $\mathbb{Z}/p^k\mathbb{Z}$ and inclusions between them, embeds in $\mathbb{Q}/\mathbb{Z}$. Furthermore, it follows from the [[Chinese remainder theorem]] that the induced map 

$$\bigoplus_p \mathbb{Z}[1/p]/\mathbb{Z} \to \mathbb{Q}/\mathbb{Z}$$ 

is an [[isomorphism]]. 

### Relation to the circle group

We have a canonical [[subgroup]] inclusion into the [[circle group]]: If the latter is identified as the canonical subgroup $U(1) \;\subset\; \mathbb{C}^\times $ in the [[group of units]] of the [[complex numbers]], this inclusion is given by

$$
  \array{
    \mathbb{Q}/\mathbb{Z}
    &\overset{\;\;\;\;\;\;}{\hookrightarrow}&
    U(1)
    \\
    [q] &\mapsto& \exp\big( 2\pi\mathrm{i} q\big)
    \,.
  }
$$ 

From this point of view, $\mathbb{Q}/\mathbb{Z}$ is the [[torsion subgroup]] of [[U(1)]], whose elements are precisely the [[roots of unity]]. 

### Further properties 

* The group $\mathbb{Q}/\mathbb{Z}$ is an [[injective object]] in the [[category]] [[Ab]] of [[abelian groups]]. 

* It is also a [[cogenerator]] in the category of abelian groups. 

  Proof: let $A$ be an abelian group. It suffices to check that for every $a \in A$ there exists $f: A \to \mathbb{Q}/\mathbb{Z}$ such that $f(a) \neq 0$. But if $\langle a \rangle$ is the cyclic subgroup generated by $a$, then it is easy to find a map $g: \langle a \rangle \to \mathbb{Q}/\mathbb{Z}$ such that $g(a) \neq 0$, and then we can extend $g$ to a map $f: A \to \mathbb{Q}/\mathbb{Z}$ using injectivity of $\mathbb{Q}/\mathbb{Z}$. 

This means every abelian group embeds into an [[injective object|injective]] abelian group, 

$$A \to \prod_{f: A \to \mathbb{Q}/\mathbb{Z}} \mathbb{Q}/\mathbb{Z},$$ 

and into an [[algebraic dual|algebraic double dual]], $A \hookrightarrow \hom(\hom(A, \mathbb{Q}/\mathbb{Z}), \mathbb{Q}/\mathbb{Z})$. The algebraic double dual of $\mathbb{Z}$ is its [[profinite completion]] 

$$\prod_{p} \mathbb{Z}_p$$ 

where $\mathbb{Z}_p$ is the group of $p$-[[p-adic number|adic integers]] (this is connected with the direct sum decomposition of $\mathbb{Q}/\mathbb{Z}$ into [[Prüfer group|Prüfer]] $p$-groups). 

* For any [[ring]] $R$, its [[algebraic dual]] $\hom(R, \mathbb{Q}/\mathbb{Z})$, equipped with the left $R$-module structure defined by $r \cdot f: s \mapsto f(s r)$, is an injective cogenerator in the category of left $R$-modules. This follows easily from the corresponding property for $\mathbb{Q}/\mathbb{Z}$. 


## Related concepts

* [[cyclic group]], [[multiplicative group of integers modulo n]]

* [[Prüfer group]], [[root of unity]]

* [[Brown-Comenetz duality]]

* [[e-invariant]]

