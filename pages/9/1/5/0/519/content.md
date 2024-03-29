
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
$f:L X \to Y$ and $g : X \to R Y$ which correspond under this bijection are said to be **adjuncts** of each other.  That is, $g$ is the (right-)adjunct of $f$, and $f$ is the (left-)adjunct of $g$.  Sometimes one writes $g = f^\sharp$ and $f = g^\flat$, as in musical notation.

Sometimes people call $\tilde f$ the "adjoint" of $f$, and vice versa, but this is potentially confusing because it is the _functors_ $F$ and $G$ which are adjoint.  Other possible terms are _conjugate_, _transpose_, and [[mate]].

## Properties

+-- {: .num_prop #AdjunctionCoUnitGiveesAllAdjuncts}
###### Proposition
**(adjuncts in terms of adjunction (co-)unit)**


Let $\eta_X \colon X \to R L X$ be the [[unit of an adjunction|unit of the adjunction]] and $\epsilon_X \colon L R X \to X$ the [[counit of an adjunction|counit]].

Then 

* the adjunct of $f \colon X \to R Y$ in $D$ is the composite

  $$
    \tilde f 
      \colon 
    L X 
     \overset{L f}{\longrightarrow} 
    L R Y 
     \overset{\epsilon_Y}{\longrightarrow} 
    Y
  $$

* the adjunct of $g \colon L X \to Y$ in $C$ is the composite

  $$  
    \tilde g 
      \colon 
    X 
      \stackrel{\eta_X}{\longrightarrow} 
    R L X 
      \overset{R g}{\longrightarrow} 
    R Y
    \,.
  $$

=--

For proof see [this Prop.](adjoint+functor#GeneralAdjunctsInTermsOfAdjunctionUnitCounit) at *[[adjoint functor]]*.

## Examples

* The process of [[currying]] is an instance of passage to adjuncts, specialized to the tensor-hom adjunction of a [[closed monoidal category]].


## Related concepts

* [[adjunction]]

* [[zig-zag law]]/[[triangle identity]]

* [[unit of an adjunction]]

* [[mate]] 

* **adjunct**

## References

* [[Categories Work]], second edition, p. 81

* [[Category Theory in Context]], p. 116, 124.

[[!redirects adjuncts]]