
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

An [[object]] $A$ in a [[category]] is a **retract** of an object $B$ if there are [[morphisms]] $i:A\to B$ and $r:B\to A$ such that $r \circ i = 1_A$.



In this situation, $r$ is a [[split epimorphism]] and $i$ is a [[split monomorphism]]; the composite $i \circ r$ is a [[split idempotent]].  Sometimes $r$ is called a [[retraction]] of $i$ and $i$ is called a [[section]] of $r$; these terms come from [[topology]].  The whole thing may also be called a **splitting** of $i$, $r$, or $i \circ r$.


## Properties

Retracts are clearly preserved by any functor. A split epimorphism $r; B \to A$ is the strongest of various notions of epimorphism (e.g., it is a regular epimorphism, in fact an absolute coequalizer, being the coequalizer of a pair $(e, 1_B)$ where $e = i \circ r: B \to B$ is idempotent). Dually, a split monomorphism is the strongest of various notions of monomorphism. 

If an object $B$ has the [[left lifting property]] against a morphism $X \to Y$, then so does every of its retracts $A \to B$:

$$
  \left(
  \array{
     && Y
     \\
     & {}^{\mathllap{\exists}}\nearrow& \downarrow
     \\
     A &\to& Y
  }
  \right)
  \;\;\;\;
  :=
  \;\;\;\;
  \left(    
  \array{
     && && &&  Y
     \\
     &&& {}^{\mathllap{\exists}}\nearrow& && \downarrow
     \\
     A &\to& B &\to& A &\to& Y
  }
  \right)
$$

## Examples

### Of simplices

The includion of standard topological [[horn]]s into the topological [[simplex]] $\Lambda^n_k \hookrightarrow \Delta^n$ is a retract in [[Top]]. 

### In arrow categories

In the theory of [[weak factorization systems]] and [[model category|model categories]], an important role is played by retracts in $C^{\mathbf{2}}$, the [[arrow category]] of $C$.  Explicitly spelled out in terms of the original category $C$, a morphism $f:X\to Y$ is a retract of a morphism $g:Z\to W$ if we have commutative squares
$$\array{X & \to & Z & \to & X\\
  f \downarrow  & & g \downarrow & & \downarrow f\\
  Y & \to & W & \to & Y}$$
such that the top and bottom rows compose to identities.

[[!redirects retracts]]

[[!redirects retraction]]
[[!redirects retractions]]