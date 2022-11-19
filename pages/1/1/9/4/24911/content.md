
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category Theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--

\tableofcontents

## Idea

The [[internalization]] of the notion of [[class]] inside of any [[(2,1)-category]]. 

Might be better to define this inside of an [[(infinity,1)-category]] so that it admits models inside of [[homotopy type theory]] as [[embeddings]] $m:C \hookrightarrow \mathrm{Set}_U$, but I do not know how to do so.  

## Definition

Let $\mathcal{C}$ be an [[(2,1)-category]] with a [[terminal object]], [[interval object]], finite [[2-pullback|(2,1)-pullbacks]], and a $\kappa$-small [[discrete object classifier]] $\mathrm{Set}_\kappa \in \mathrm{Ob}(\mathcal{C})$ for [[cardinal number]] $\kappa$. 
An internal set $A$ is a [[morphism]] $A:\mathrm{Hom}(1, \mathrm{Set}_\kappa)$ from the [[terminal object]] $1 \in \mathrm{Ob}(\mathcal{C})$ to $\mathrm{Set}_\kappa$. A **class object relative to $\mathrm{Set}_\kappa$** in $\mathcal{C}$ is an [[object]] $C \in \mathrm{Ob}(\mathcal{C})$ with a [[monomorphism]] $m:C \hookrightarrow \mathrm{Set}_\kappa$. 

## Category of class objects

Given a [[(2,1)-category]] $\mathcal{C}$ with a [[terminal object]], [[interval object]], finite [[2-pullback|(2,1)-pullbacks]], and a $\kappa$-small [[discrete object classifier]] $\mathrm{Set}_\kappa \in \mathrm{Ob}(\mathcal{C})$ for [[cardinal number]] $\kappa$, one could define the **[[(2,1)-category]] of class objects** $\mathrm{Mono}(\mathrm{Set}_\kappa)$ as the category of [[monomorphisms]] into the $\kappa$-small discrete object classifier, whose morphisms preserve the monomorphism into $\mathrm{Set}_\kappa$: for every object $A \in \mathrm{Mono}(\mathrm{Set}_\kappa)$ with monomorphism $a:\mathrm{Hom}(A,\mathrm{Set}_\kappa)$ and $B \in \mathrm{Mono}(\mathrm{Set}_\kappa)$ with monomorphism $b:\mathrm{Hom}(B,\mathrm{Set}_\kappa)$ and morphism $f:\mathrm{Hom}(A, B)$, there is a [[natural isomorphism]] $i(a, b, f):\mathrm{id}_{\mathrm{Set}_\kappa} \circ a \cong b \circ f$. 

$$\array{& A & \overset{a}\hookrightarrow & \mathrm{Set}_\kappa & \\
          f & \downarrow & \cong\swArrow &\downarrow & \mathrm{id}_{\mathrm{Set}_\kappa}\\
          &B & \underset{b}\hookrightarrow& \mathrm{Set}_\kappa & \\
}$$

## See also

* [[discrete object classifier]]

* [[class]]

[[!redirects class objects]]

[[!redirects category of class objects]]
[[!redirects (2,1)-category of class objects]]
[[!redirects (n,1)-category of class objects]]
[[!redirects (infinity,1)-category of class objects]]