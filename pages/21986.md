+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Integers object
* table of contents
{: toc}

## Idea

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[set|sets]].  

An **integers object** [[internalization|internal to]] a topos is an [[object]] that behaves in that topos like the set $\mathbb{Z}$ of [[integers]] does in [[Set]].

## Definition

### In a topos or cartesian closed category {#CCC}

An **integers object** in a [[topos]] (or any [[cartesian closed category]]) $E$ with [[terminal object]] $1$ is 

* an [[object]] $\mathbb{Z}$ in $E$ 

* equipped with 
  
  * a [[morphism]] $z:1 \to \mathbb{Z}$ from the [[terminal object]] $1$;

  * [[morphism]]s $s, p : \mathbb{Z} \to \mathbb{Z}$ (successor and predecessor), such that $s \circ p = p \circ s = id_\mathbb{Z}$;

* such that for every other object $A$ with morphisms $z_A : 1 \to A$ and $s_A, p_A : A \to A$ such that $s_A \circ p_A = p_A \circ s_A = id_A$, there is a unique morphism $u : \mathbb{Z} \to A$ such that $u \circ z = z_A$, $u \circ s = s_A \circ u$, and $u \circ p = p_A \circ u$. 

By the [[universal property]], the integers object is unique up to [[isomorphism]]. 

Every integers object is a [[natural numbers object]] in two different ways, as the triples $(\mathbb{Z},z:1\rightarrow\mathbb{Z},s:1\rightarrow\mathbb{Z})$ and $(\mathbb{Z},z:1\rightarrow\mathbb{Z},p:1\rightarrow\mathbb{Z})$. There is a nontrivial isomorphism $-:\mathbb{Z}\rightarrow\mathbb{Z}$ between the two natural numbers objects $(\mathbb{Z},z:1\rightarrow\mathbb{Z},s:1\rightarrow\mathbb{Z})$ and $(\mathbb{Z},z:1\rightarrow\mathbb{Z},p:1\rightarrow\mathbb{Z})$, such that $- \circ z = z$, $s \circ - = - \circ p$, and $p \circ - = - \circ s$, which corresponds to negation in [[Set]].  

## Related concepts

* [[integers]]

* [[natural numbers object]]




[[!redirects integers object]]
[[!redirects integers objects]]
[[!redirects integer object]]
[[!redirects integer objects]]