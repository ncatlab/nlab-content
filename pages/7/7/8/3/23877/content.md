
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Congruences
* table of contents
{: toc}

## Definitions

+-- {: .num_defn #Definition}
###### Definition

In a [[finitely complete category]] $C$, a **preordered object** $X$ is an object with an [[internal relation|internal]] [[preorder]] on $X$: a [[subobject]] of the product $R\stackrel{(p_1,p_2)}\hookrightarrow X \times X$ equipped with the following [[morphisms]]: 

* internal [[reflexive relation|reflexivity]]: $r \colon X \to R$ which is a [[section]] both of $p_1$ and of $p_2$, i.e., $p_1 r = p_2 r = 1_X$;

* internal [[transitive relation|transitivity]]: $t: R \times_X R \to R$ which factors the left/right projection map $R \times_X R \to X \times X$ through $R$, i.e., the following diagram commutes
  $$\array{
    && R \\  
    & {}^{\mathllap{t}}\nearrow & \downarrow \\
    R \times_X R & \stackrel{(p_1 q_1,p_2 q_2)}\rightarrow & X \times X
  }
  $$
where $q_1$ and $q_2$ are the projections defined by the [[pullback | pullback diagram]]
  $$\array{
    R \times_X R & \stackrel{q_2}\rightarrow & R
    \\
    \downarrow^{\mathrlap{q_1}} && \downarrow^{\mathrlap{p_1}}
    \\
    R & \stackrel{p_2}\rightarrow & X
  }
  $$
=--

+-- {: .num_remark}
###### Remark

Since $i$ is a [[monomorphism]], the maps $r$, $s$, and $t$ are necessarily unique if they exist.

=--

+-- {: .num_remark}
###### Remark

Equivalently, a preordered object $X$ is an [[internal category]] with $X$ the object of [[objects]], such that the (source,target)-map is a [[monomorphism]].

=--

+-- {: .num_remark}
###### Remark

We can equivalently define an internal preorder $R$ as (a representing object of) a representable sub-presheaf of $\hom(-, X \times X)$ so that for each object $Y$, the composite of $R(Y) \hookrightarrow \hom(Y, X \times X) \cong \hom(Y, X) \times \hom(Y, X)$ exhibits $R(Y)$ as an preorder on the set $\hom(Y, X)$. The upshot of this definition is that it makes sense even when $C$ is not finitely complete.

=--

## See also 

* [[preorder]]
* [[congruence]]
* [[cartesian monoidal preordered object]]

[[!redirects preordered objects]]
[[!redirects internal preorder]]
[[!redirects internal preorders]]
[[!redirects internal pre-order]]
[[!redirects internal pre-orders]]