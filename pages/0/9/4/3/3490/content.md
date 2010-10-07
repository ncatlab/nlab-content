
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The analog of the notion of [[subcategory]] for [[(∞,1)-categories]].

## Definition

Say that an [[equivalence of quasi-categories|equivalence of (∞,1)-categories]] $D \stackrel{\simeq}{\to} C$ exhibits $D$ as a **0-subcategory** of $C$.

Then define recursively, for $n \in \mathbb{N}$: 

an **$n$-subcategory** of an $(\infty,1)$-category $D$ for $n \geq 1$ is an [[(∞,1)-functor]]

$$
  F : D \to C
$$

such that for all objects $x,y \in D$ the component-$(\infty,1)$-functor on the [[hom-object in a quasi-category|hom-objects]] 

$$
  F_{x,y} : Hom_D(x,y) \to Hom_C(F(x), F(y))
$$

exhibits an $(n-1)$-subcategory.

## Special cases

### 1-Subcategory / full subcategory

A **full subcategory** is a 1-subcategory, exhibited by a [[full and faithful (∞,1)-functor]]. 

#### For $sSet$-enriched and quasi-categories

Let $C$ and $D$ be incarnated specifically as [[model structure on sSet-categories|fibrant]] [[simplicially enriched categories]]. Then for $F : D \to C$ a full and faithful $(\infty,1)$-functor, choose in each preimage $F^{-1}(c)$ for each object $c \in C$ a representative, and let $C'$ be the full [[sSet]]-[[enriched category|enriched]] [[subcategory]] on these representatives.

Then the evident projection functor $D \stackrel{\simeq}{\to} D'$ is manifestly an [[equivalence of quasi-categories|equivalence]] and the original $F : D \to C$ factors as

$$
  F : D \stackrel{\simeq}{\to} D' \hookrightarrow C
  \,,
$$

where the second morphism is an ordinary inclusion of objects and hom-complexes.

#### Reflective sub-$(\infty,1)$-categories

If the $(\infty,1)$-functor $F : D \to C$ has a left [[adjoint (∞,1)-functor]] $L : C \to D$, then $F$ is full and faithful and hence exhibits a 1-subcategory precisely if the counit

$$  
  L \circ F \stackrel{}{\to} Id_D
$$

is an [[equivalence in a quasi-category|equivalence]] of [[(∞,1)-functor]]s. (See also [[Higher Topos Theory|HTT, p. 308]]).

In this case $D$ is a [[reflective (∞,1)-subcategory]].

### 2-Subcategory

#### For $sSet$-enriched and quasi-categories

Let the $(\infty,1)$-categories $C$ and $D$ concretely be incarnated as [[model structure on sSet-categories|fibrant]] [[simplicially enriched categories]].

Write $h C := Ho(C)$ and $h D := Ho(D)$ for the corresponding [[homotopy category of an (∞,1)-category]] (hom-wise the connected components of the corresponding [[simplicially enriched category]]).

Let $h D \to h C$ be a [[faithful functor]]. Then if we have a [[pullback]] in [[sSet]]-[[Cat]]

$$
  \array{
    D &\to& C
    \\
    \downarrow && \downarrow
    \\
    h D &\to& h C
  }
$$

$D$ is a 2-sub-$(\infty,1)$-category of $C$. 
This pullback manifestly produces the simplicially enriched category whose

* objects are those of $h D$;

* hom-complexes are precisely the unions of those connected components of the hom-complexes of $C$ whose equivalence class is present in $h D$.

Therefore the inclusion functor $D \to C$ is on each hom-complex a [[full and faithful (∞,1)-functor]]. Hence this identifies $D$ as a 2-subcategory of $C$.

If $h D \to h C$ is an inclusion on objects (which is a bit [[evil]] to say) then this is the definition of subcategory of an $(\infty,1)$-category that appears in [[Higher Topos Theory|HTT, section 1.2.11]].


#### As 2-subobjects {#2Subobjects}

Let $core(Set_*) \to core(Set)$ be the 2-subobject classifier in the [[(∞,1)-topos]] [[∞Grpd]]. Then
for $C \in \infty Grpd$ a 1-subobject is classified by an $\infty$-functor
$C \to Set$. This factors through the homotopy category of $C$ as $C \to h C \to Set$. Since $Set_* \to Set$ is the universal faithful functor, the pullback

$$
  \array{
    Q &\to& Set_*
    \\
    \downarrow && \downarrow
    \\
    h C &\to& Set
  }
$$

gives an ordinary subcategory of $h C$. This means that the total pullback $D \to C$

$$
  \array{
    D &\to& h D &\to& Set_*
    \\
    \downarrow && \downarrow && \downarrow
    \\
    C &\to& h C &\to& Set
  }
$$

gives a 2-sub-$(\infty,1)$-category $K$ of $X$ (where both happen to be $\infty$-groupoids) here.




## References

What we call a 2-subcategory of an $(\infty,1)$-category appears in  section 1.2.11 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects sub-quasi-category]]

[[!redirects sub-quasicategory]]
[[!redirects subquasicategory]]

[[!redirects sub-(∞,1)-category]]
[[!redirects sub-(infinity,1)-category]]

[[!redirects sub-quasi-categories]]
[[!redirects sub-quasicategories]]
[[!redirects subquasicategories]]

[[!redirects sub-(∞,1)-categories]]
[[!redirects sub-(infinity,1)-categories]]