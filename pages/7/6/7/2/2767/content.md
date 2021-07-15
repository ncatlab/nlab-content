
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **constant functor** $\Delta d: C\to D$ is a [[functor]] that maps each [[object]] of the [[category]] $C$ to a fixed object $d\in D$ and each morphism of $C$ to the identity morphism of that fixed object. 

(The notation $\Delta d$ is suggested by the fact that if $d: 1 \to D$ names an object $d$ of $D$, then the composite 

$$1 \stackrel{d}{\to} D \stackrel{\Delta}{\to} D^C$$ 

names a functor $\Delta d: C \to D$ which is the constant functor at $d$. Here $\Delta: D \to D^C$ denotes a [[diagonal functor]].) 

Viewing $D \cong [1,D]$, it is possible to see that $\Delta$ is a base change of the functor categories $D^1$ and $D^C$, given the functor $!_C: C \to 1$.


More generally, we may say that a functor $F:C\to D$ is **essentially constant** if it is [[naturally isomorphic]] to a constant functor.

## Properties

Note that a constant functor can be expressed as the composite
$$C \stackrel{!}{\to} 1 \stackrel{[d]}{\to} D.$$ 
Here $1$ is a [[terminal category]] (exactly one object and exactly one morphism, namely the identity), and $[d]$ denotes the unique functor from $1$ with $F(\bullet) = d$ and $F(Id_\bullet) = Id_d$.  It follows that $F:C\to D$ is essentially constant if and only if it factors through $1$ up to isomorphism.

If $C$ has at least one object, then there is a [[codescent object]]
$$ C\times C\times C \underoverset{\to}{\to}{\to} C\times C \rightrightarrows C \to 1. $$
Therefore, in this case a functor $F:C\to D$ is essentially constant if and only if we have a natural isomorphism between the two composites $C\times C \rightrightarrows C \xrightarrow{F} D$ (i.e. isomorphisms $F(c_1)\cong F(c_2)$ natural in $c_1,c_2\in C$) that satisfies a [[cocycle condition]].  This is a categorified version of the statement that a [[function]] with inhabited domain is a [[constant function]] if and only if the images of any two elements are equal.  Just as in that case, there is a distinction in the trivial case: the [[identity functor]] of the [[empty category]] satisfies this weaker condition, but is not essentially constant because there is no object for it to be constant at.

## Examples

* For $F$ any functor, a [[natural transformation]]

  $\Delta_d \Rightarrow F$ 

  from a constant functor into $F$ is precisely a [[cone]] over $F$. Similarly a natural transformation
  
  $F \Rightarrow \Delta_d$

  is a [[cocone]].

## Related concepts

* [[constant presheaf]], [[locally constant sheaf]] 
* [[diagonal functor]]
* [[constant morphism]], [[constant function]]

[[!redirects constant functors]]
[[!redirects essentially constant functor]]
[[!redirects essentially constant functors]]

[[!redirects constant diagram]]
[[!redirects constant diagrams]]
