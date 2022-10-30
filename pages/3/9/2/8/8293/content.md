
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A pure subobject is a [[monomorphism]] $A \rightarrowtail B$ -- hence a [[subobject]] $A$ of some [[object]] $B$ in some [[category]] -- such that any sufficiently small system of [[equations]] involving constants in $A$ that admits a solution in $B$ also admits a solution in $A$. This generalises the classical notions of 'pure group' and 'pure submodule'.

## Definition

Let $\kappa$ be a regular [[cardinal]]. A **$\kappa$-pure morphism** in a [[category]] $\mathcal{C}$ is a morphism $f : A \to B$ with the following extension property:

* Given any morphisms $f' : A' \to B'$, $a : A' \to A$,  $b : B' \to B$ in $\mathcal{C}$, if both $A'$ and $B'$ are $\kappa$-[[compact object|compact]] and $f \circ a = b \circ f'$, 

  $$
    \array{
      A' &\stackrel{a}{\to}& A
      \\
      \downarrow^{\mathrlap{f'}} && \downarrow^{\mathrlap{f}}
      \\
      B' &\stackrel{b}{\to}& B
    }
    \,,
  $$

  then there exists a (not necessarily unique) morphism $\bar{a} : B' \to A$ in $\mathcal{C}$ such that $a = \bar{a} \circ f$.

A **$\kappa$-pure subobject** is a $\kappa$-pure monomorphism.


## Examples

* A [[retract]] is a $\kappa$-pure subobject in any category, for any $\kappa$.

* Conversely, any $\kappa$-pure subobject in [[Set]] is a retract. 

* If $A$ is an [[injective]] [[module]] and $B$ is any module containing $A$ as a submodule, then the inclusion $A \hookrightarrow B$ is $\kappa$-pure. (This can be checked directly without recourse to the fact that any injective submodule is a retract!)

* The torsion subgroup of any [[abelian group]] is a $\kappa$-pure subgroup, since it is a filtered colimit of [[direct sum|direct summands]]. (See below.)


## Properties
 {#Properties}

+-- {: .num_lemma}
###### Lemma

In any category:

* The class of $\kappa$-pure morphisms is closed under composition.

* If $g \circ f$ is a $\kappa$-pure morphism, then so is $f$.

* If $\kappa' \ge \kappa$, then any $\kappa$-pure morphism is also $\kappa'$-pure.

=--

+-- {: .num_prop }
###### Proposition

In a $\kappa$-[[accessible category]], any $\kappa$-pure morphism is necessarily monic.

=--

This is [LPAC, Prop. 2.29](#AdamekRosicky).

+-- {: .num_prop }
###### Proposition

If $\mathcal{C}$ is a $\kappa$-accessible category, then $\kappa$-pure subobjects in $\mathcal{C}$ are closed under $\kappa$-[[filtered limit|filtered colimits]] in the [[arrow category]] $Arr (\mathcal{C})$.

If $\mathcal{C}$ is a $\kappa$-accessible category with [[pushout|pushouts]], then any $\kappa$-pure subobject in $\mathcal{C}$ is a $\kappa$-filtered colimit in $Arr (\mathcal{C})$ of retracts in $\mathcal{C}$.

=--

This is [LPAC, Prop. 2.30](#AdamekRosicky).


+-- {: .num_prop }
###### Proposition

In a $\kappa$-accessible category, every $\kappa$-pure morphism is a [[regular monomorphism]].

=--

This is [LPAC, Prop. 2.31](#AdamekRosicky).

## Applications


+-- {: .num_theorem }
###### Theorem

Let $\mathcal{C}$ be a $\kappa$-accessible category, and let $\mathcal{D}$ be a full subcategory of $\mathcal{C}$ that is closed under $\kappa$-filtered colimits for some regular cardinal $\kappa$. Then, $\mathcal{D}$ is a $\mu$-accessible category for some regular cardinal $\mu$ sharply larger than $\kappa$ if and only if $\mathcal{D}$ is closed under $\kappa$-pure subobjects in $\mathcal{C}$.

In particular, a category $\mathcal{D}$ is accessible if and only if there is a fully faithful functor $R : \mathcal{D} \to Set^{\mathcal{A}}$ where $\mathcal{A}$ is small, $R$ [[created limit|creates]] colimits for all $\kappa$-filtered diagrams, and $\mathcal{D}$ is closed under $\kappa$-pure subobjects in $Set^{\mathcal{A}}$.

=--

This is [LPAC, Cor. 2.36](#AdamekRosicky).

## References 


* [LPAC] [[Jiri Adamek]], [[Jiri Rosicky]], _[[Locally presentable and accessible categories]]_
 {#AdamekRosicky}


[[!redirects pure morphism]]
[[!redirects pure monomorphism]]

[[!redirects pure subobjects]]
[[!redirects pure morphisms]]
[[!redirects pure monomorphisms]]