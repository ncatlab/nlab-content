
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A pair 

$$
  (L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D
$$

of [[adjoint functor]]s between [[category|categories]] $C$ and $D$, is characterized by a [[natural isomorphism]]

$$ 
  C(L X,Y) \cong D(X,R Y) 
$$

of [[hom-set]]s for [[object]]s $X\in D$ and $Y\in C$.  Two [[morphism]]s 
$f:L X \to Y$ and $\tilde f : X \to R Y$ which correspond under this bijection are said to be **adjuncts** of each other.  That is, $\tilde f$ is the adjunct of $f$ and $f$ is the adjunct of $\tilde f$.

Sometimes people call $\tilde f$ the "adjoint" of $f$, and vice versa, but this is potentially confusing because it is the _functors_ $F$ and $G$ which are adjoint.  Other possible terms are _conjugate_ and [[mate]].

## Properties

Let $i_X : X \to R L X$ be the [[unit of an adjunction|unit of the adjunction]] and $\eta_X : L R X \to X$ the counit.

Then 

* the adjunct of $f : X \to R Y$ in $D$ is the composite

  $$
    \tilde f : L X \stackrel{L f}{\to} L R Y \stackrel{\eta_Y}{\to} Y
  $$

* the adjunct of $g : L X \to Y$ in $C$ is the composite

  $$  
    \tilde g : X \stackrel{i_X}{\to} R L X \stackrel{R g}{\to} R Y
  $$

## Related concepts

* [[adjunction]]

* [[zig-zag law]]/[[triangle identity]]

* [[unit of an adjunction]]

* **adjunct**

[[!redirects adjuncts]]