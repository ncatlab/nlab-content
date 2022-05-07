
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

An __endomorphism__ of an [[object]] $x$ in a [[category]] $C$ is a [[morphism]] $f : x \to x$.  

An endomorphism that is also an [[isomorphism]] is called an [[automorphism]].


## Properties

Given an object $x$, the endomorphisms of $x$ form a [[monoid]] under [[composition]], the __endomorphism monoid__ of $x$:
$$
  End_C(x) = Hom_C(x,x)
,$$
which may be written $End(x)$ if the category $C$ is understood.  Up to equivalence, every monoid is an endomorphism monoid; see [[delooping]].

An endomorphism monoid is a special case of a monoid structure on an [[end]] construction. Let $d:D\to C$ be a diagram in $C$, where $C$ is a [[monoidal category]] (in the case above the monoidal structure is the [[cartesian product]] and $d$ is a constant diagram from the initial category). One defines $End(d)$ as an object in $C$, equipped with a natural transformation $a: End(d) \otimes d \to d$ which is universal in the sense that for all objects $Z \in C$, and any natural transformation $f: Z \otimes d \to d$ there exists a unique morphism $g: Z \to End(d)$ such $a \circ (g \otimes d) = f: Z \otimes d \to d$.

+-- {: .num_prop}
###### Proposition

If the universal object $(End(d),a)$ exists then there is a unique structure of an [[internalization|internal]] monoid $\mu: End(d) \otimes End(d) \to End(d)$, such that the map $a: End(d) \otimes d \to d$ is an [[action]]. 
=--

+-- {: .num_prop} 
###### Proposition 
In a [[cartesian monoidal category]] $C$, if an endomorphism monoid $End(c)$ for an object $c: 1 \to C$ exists and is [[commutative monoid|commutative]], then $c$ is a [[subterminal object]]. 
=-- 

+-- {: .proof} 
###### Proof 
Let $k: c \to End(c)$ correspond to first projection $\pi_1: c \times c \to c$. Then the composition 

$$c \times c \stackrel{k \times k}{\to} End(c) \times End(c) \stackrel{comp}{\to} End(c)$$ 

(where $comp$ denotes internal composition) may be computed to be $k \pi_1$, corresponding to first projection $\pi_1: c \times c \times c \to c$. Thus, assuming commutativity of $End(c)$ and letting $\sigma$ generally denote a symmetry map, consideration of the diagram 

$$\array{
c \times c & \stackrel{k \times k}{\to} & End(c) \times End(c) & \stackrel{comp}{\to} & End(c) \\ 
\mathllap{\sigma} \downarrow & & \mathllap{\sigma} \downarrow & & \downarrow \mathrlap{id} \\ 
c \times c & \stackrel{k \times k}{\to} & End(c) \times End(c) & \stackrel{comp}{\to} & End(c)
}$$ 

leads to the conclusion that $k \pi_1 = k \pi_1 \sigma$, or $\pi_1 = \pi_2: c \times c \times c \to c$. We easily conclude $\pi_1 = \pi_2: c \times c \to c$, which forces equality $f = g$ for any two maps $f, g: d \to c$, so that the unique map $!: c \to 1$ is a [[monomorphism]]. 
=-- 

## Related entries

* **endomorphism**, [[automorphism]]

* **endomorphism monoid**, [[endomorphism ring]]

* [[endomorphism operad]]

* [[endofunction]]

* [[endofunctor]]

* [[EI-category]]


[[!redirects endomorphism]]
[[!redirects endomorphisms]]

[[!redirects endomorphism monoid]]
[[!redirects endomorphism monoids]]
