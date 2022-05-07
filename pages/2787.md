
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Finitely generated objects
* table of contents
{: toc}

## Definition in arbitrary categories

Let $C$ be a [[locally small category]] that admits [[filtered colimits]] of monomorphisms. Then an [[object]] $X \in C$ is __finitely generated__ if the [[corepresentable functor]]

$$
  Hom_C(X,-) : C \to Set
$$

[[preserved limit|preserves]] these [[filtered colimits]] of monomorphisms.  This means that for every [[filtered category]] $D$ and every functor $F : D \to C$ such that $F(f)$ is a monomorphism for each morphism $f$ of $D$, the canonical morphism

$$
  \underset{\to_d}{\lim} C(X,F(d)) \stackrel{\simeq}{\to} 
  C(X, \underset{\to_d}{\lim} F(d))
$$

is an [[isomorphism]].

## Definition in concrete categories

An object $A$ of a [[concrete category]] $C$ is __finitely generated__ if it is a [[quotient object]] (in the sense of a [[regular epimorphism]]) of some [[free object]] $F$ in $C$, where $F$ is free on a [[finite set]].

The object $A$ is __finitely presented__ if it is the [[coequalizer]] of a [[parallel pair]] $R \rightrightarrows F$ such that $R$ is also free on a finite set.

## Examples

* A set $X$ is a finitely generated object in [[Sets]] iff it is [[finite set|(Kuratowski-)finite]]. For this to hold constructively, [[filtered categories]] (appearing in the definition of _[[filtered colimit]]_) have to be understood as categories admitting cocones of every _Bishop-finite_ diagram.

*  For $R$ a [[ring]], an $R$-[[module]] $N$ is a [[finitely generated module]] if it is a [[quotient]] of a [[free module]] with a finite [[basis of a free module|basis]].

* [[finitely generated group]]

## Related concepts

* [[finitely presentable object]]

* [[generators and relations]]


## References

The general definition is in [[Locally Presentable and Accessible Categories]], definition 1.67.

[[!redirects finitely generated object]]
[[!redirects finitely generated objects]]
[[!redirects finitely generated]]

[[!redirects finitely presented object]]
[[!redirects finitely presented objects]]
[[!redirects finitely presented]]