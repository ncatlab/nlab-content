
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A __natural isomorphism__ $\eta\colon F \Rightarrow G$ between two [[functors]] $F$ and $G$

$$
  \array{
    &  \nearrow \searrow^{F}
    \\
    C &{}^{\simeq}\Downarrow^\eta& D
    \\
    & \searrow \nearrow_{G}
  }
$$

is equivalently

* a [[natural transformation]] with a two-sided [[inverse]];

* a natural transformation each of whose components $\eta_c : F(c) \to G(c)$ for all $c \in Obj(C)$ is an [[isomorphism]] in $D$;

* an [[isomorphism]] in the [[functor category]] $[C,D]$.

In this case, we say that $F$ and $G$ are __naturally isomorphic__. (Synonym: $F$ and $G$ are _isomorphic functors_; the naturality is understood when one says that two functors are isomorphic.)

Notably, especially in expositions and lectures, despite the third bullet point above, one does not need to define the concept of a [[functor category]] in order to define _isomorphic functors_. Authors sometimes make cautionary remarks about the category of all functors from $C$ to $D$ (cf. e.g. [Auslander (1971, p.9)](#Auslander1971)) 



If you want to speak of '[[the]]' functor satisfying certain conditions, then it should be unique up to unique natural isomorphism.

A natural isomorphism from a functor to itself is also called a _natural [[automorphism]]_.


## Some basic uses of isomorphic functors

### Defining the concept of equivalence of categories
 
A fundamental use of the concept of isomorphic functors is the usual definition of [[equivalent categories]] which involves functors isomorphic to [[identity functor|identity functors]].

### Re-defining isomorphism of objects in terms of isomorphism of functors

The [[Yoneda lemma]] implies that in any category $\mathcal{C}$, and for any objects $O$ and $O'$ of $\mathcal{C}$, the following are equivalent:

* $O$ and $O'$ are [[isomorphic]] in $\mathcal{C}$,

* the [[hom-functor|representable presheaves]] $\mathcal{C}(-,O)$ and $\mathcal{C}(-,O')$ are isomorphic functors,

* the [[hom-functor|representable copresheaves]] $\mathcal{C}(O,-)$ and $\mathcal{C}(O',-)$ are isomorphic functors.



## Related entries

* [[functor category]]

* [[limit]]

## References

* {#Auslander1971}[[M. Auslander]],  The representation dimension of artin algebras. 
Queen Mary College Mathematics Notes (1971) Republished in: Selected works of Maurice Auslander. American Mathematical Society (1999)




## Related concepts

* [[natural equivalence]]




[[!redirects isomorphic functors]]


[[!redirects natural isomorphism]]
[[!redirects natural isomorphisms]]
[[!redirects naturally isomorphic]]
[[!redirects isomorphic functor]]
[[!redirects isomorphic functor]]
[[!redirects naturally isomorphic functor]]
[[!redirects naturally isomorphic functors]]

[[!redirects natural automorphism]]
[[!redirects natural automorphisms]]
