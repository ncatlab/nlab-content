
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _factorization lemma_ is a fundamental tool in [[categories of fibrant objects]] (dually: of cofibrant objects). It mimics the _factorization axioms_ in a [[model category]].

## Statement

Let $C$ be a [[category of fibrant objects]]. 

+-- {: .un_lemma}
###### Lemma

Every [[morphism]] $f : X \to Y$ in $C$ factors as

$$
  f : X \stackrel{i_\simeq}{\to} \hat X \stackrel{p}{\to} Y
  \,,
$$

where 

1. $i$ is the [[right inverse]] to a trivial fibration, hence in particular a weak equivalence;

1. $p$ is a fibration.
=--

+-- {: .proof}
###### Proof

Let $X \stackrel{\simeq}{\to} X^I \stackrel{(d_0,d_1)}{\to} X \times X$ be a [[path space object]] for $X$. Let $\hat X := Y^I \times_Y X$ be the [[pullback]] of $f$ along one of its legs, to get the diagram

$$
  \array{
     \hat X &\to& X
     \\
     \downarrow && \downarrow^{\mathrlap{f}}
     \\
     Y^I &\stackrel{d_1}{\to}& Y
     \\
     {}^{\mathllap{d_0}}\downarrow 
     \\
     Y
  }
  \,.
$$

With a little diagram gymnastics one shows that the composit vertical morphism is a fibration. Take this to be $p : \hat X \to Y$. 

Notice by the axioms of [[path space object]]s in a [[category of fibrant objects]] that $d_1 : Y^I \to Y$ is a trivial fibration. Since these are stable under pullback, also $\hat X \to X$ is a trivial fibration.

But, by the axioms, $Y^I \to Y$ has a right inverse $Y \to Y^I$. By the [[pullback]] property this induces a right inverse of $\hat X \to X$ fitting into a [[pasting]] diagram

$$
  \array{
     X &\to& \hat X &\to& X
     \\
     {}^{\mathrlap{f}}\downarrow && \downarrow && \downarrow^{\mathrlap{f}}
     \\
     Y &\to& Y^I &\stackrel{d_1}{\to}& Y
     \\
     & {}_{\mathllap{Id}}\searrow& {}^{\mathllap{d_0}}\downarrow 
     \\
     && Y
  }
  \,.
$$

That establishes the claim.
=--

## Corollaries

+-- {: .un_corollary}
###### Corollary
Let $F : C \to D$ be a functor from a [[category of fibrant objects]] to any [[category with weak equivalences]] that sends trivial fibrations to weak equivalences. Then this functor necessarily sends all weak equivalences to weak equivalences, hence is a [[homotopical functor]].
=--

+-- {: .proof}
###### Proof

If $f : X \to Y$ is a weak equivalence, then by 2-out-of-3 also the $p : \hat X \to Y$ from the above proof is a weak equivalence, hence a trivial fibration.

Apply the functor $F$ to the diagram of the above proof

$$
  \array{
     F(\hat X) &\to& F(X)
     \\
     \downarrow && \downarrow^{\mathrlap{F(f)}}
     \\
     F(Y^I) &\stackrel{F(d_1)}{\to}& F(Y)
     \\
     {}^{\mathllap{F(d_0)}}\downarrow 
     \\
     F(Y)
  }
  \,.
$$

By the assumption that $F$ preserves trivial fibrations we have that both horizontal morphisms as well as the total vertical morphism and the bottom vertical morphism are weak equivalences. By 2-out-of-3 it then follows that also the top left vertical morphism is a weak equivalence and then finally that $F(f)$ is.
=--

+-- {: .un_remark}
###### Remark
If $C$ is the full subcategory of fibrant objects in a [[model category]], then this corollary asserts that a [[Quillen adjunction|right Quillen functor]] $F$, which by its axioms is required only to preserve fibrations and trivial fibrations, preserves also weak equivalences between fibrant objects.
=--

## Examples

* For $G$ an [[∞-group]] object in $C$ with [[delooping]] $\mathbf{B}G$, applying the factorization lemma to the point inclusion $* \to \mathbf{B}G$ yields a morphism $* \stackrel{\simeq}{\to} \mathbf{E}G \stackrel{p}{\to} \mathbf{B}G$. This exhibits a [[universal principal ∞-bundle]] for $G$. 


## References

For instance page 4 of

* Kenneth Brown, _[[BrownAHT|Abstract Homotopy Theory and Generalized sheaf Cohomology]]_ .
