


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesion
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In a context of [[differential cohesion]] the _infinitesimal shape modality_ or _&#233;tale modality_ $\& $ characterizes [[coreduced objects]]. It is itself the [[right adjoint]] in an [[adjoint modality]] with the [[reduction modality]] and the [[left adjoint]] in an [[adjoint modality]] with the [[infinitesimal flat modality]].

## Definition

A context of [[differential cohesion]] is determined by the existence of an [[adjoint triple]] of  [[modalities]]

$$
  \Re \dashv \Im \dashv \&
  \,,
$$

where $\Re$ and $\&$ are [[idempotent monad|idempotent]] [[comonads]] and $\Im $ is an [[idempotent monad]].

Here $\Im $ is the **infinitesimal shape modality**. The [[reflective subcategory]] that it defines is that of [[coreduced objects]].

## Properties

### Relation for formally &#233;tale morphisms

The [[modal types]] of $\Im $ in the context of some $X$, i.e. those $(Y\to X) \in \mathbf{H}_{/Y}$ for which the naturality square of the $\Im $-[[unit of a monad|unit]] 

$$
  \array{
     X &\longrightarrow& \Im X
     \\
     \downarrow && \downarrow
     \\
     Y &\longrightarrow& \Im Y
  }
$$
 
is a ([[homotopy pullback|homotopy]]) [[pullback]] square, are the [[formally étale morphisms]] $Y \to X$.

### Relation to de Rham spaces

For $X$ a [[geometric homotopy type]], the result of applying the infinitesimal shape modality yields a type $ \Im X$ which has the interpretation of the [[de Rham space]] of $X$. See there for more.

### Relation to jet bundles

For $E$ a [[dependent type]] on $X$, its [[dependent product]] along the [[unit of a monad|unit]] of the infinitesimal shape modality has the interpretation of the [[jet type]] $j(E)$. See there for more.

### Relation to crystalline cohomology

The [[cohomology]] of $\Im X$ has the interpretation of [[crystalline cohomology]] of $X$. See there for more.

## Related concepts


[[!include cohesion - table]]
