[[!redirects (infinity,n)-category of spans]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _$(\infty,n)$-category of correspondences_ in [[∞-groupoid]] is an [[(∞,n)-category]] whose

* [[objects]] are [[∞-groupoids]];


* [[morphism]]s $X \to Y$ are [[correspondences]] 

  $$
    \array{
      && Z
      \\
      & \swarrow && \searrow
      \\
      X &&&& Y
    }
  $$

  in [[∞Grpd]]

* [[2-morphisms]] are correspondences of correspondences

  $$
    \array{
      && Z
      \\
      & \swarrow &\uparrow& \searrow
      \\
      X &&Q&& Y
      \\
      & \nwarrow &\downarrow& \nearrow
      \\
      && Z'
    }
  $$

  (where the triangular sub-[[diagram]]s are filled with [[2-morphism]]s in [[∞Grpd]] which we do not display here)

* and so on up to [[k-morphism|n-morphism]]s

* $k \gt n$-morphisms are equivalences of order $(k-n)$ of higher correspondences.

Using the symmetric monoidal structure on [[∞Grpd]] this becomes a [[symmetric monoidal (∞,n)-category]].

More generally, for $C$ some [[symmetric monoidal (∞,n)-category]], there is a symmetric monoidal $(\infty,n)$-category of correspondences over $C$, whose

* [[object]]s are [[∞-groupoid]]s $X$ equipped with an [[(∞,n)-functor]] $X \to C$;

* [[morphism]]s $X \to Y$ are [[correspondences]] in [[(∞,1)Cat]] over $C$

  $$
    \array{
      && Z
      \\
      & \swarrow && \searrow
      \\
      X &&\swArrow&& Y
      \\
      & \searrow && \swarrow
      \\
      && C
    }
  $$

* and so on.

Even more generally one can allow the [[∞-groupoid]]s $X, Y, \cdots$ to be [[(∞,n)-categories]] themselves.

## Definition
 {#Definition}

### Direct definition

The [[(∞,2)-category]] of correspondences in [[∞Grpd]] is discussed in some detail in ([Dyckerhoff-Kapranov 12, section 10](#DyckerhoffKapranov12)).
A sketch of the definition for all $n$ was given in ([Lurie, page 57](#Lurie)). A fully detailed version of this definition is in ([Haugseng 14](#Haugseng14)).


### Definition via coalgebras
 {#DefinitionViaCoalgebras}

In ([BenZvi-Nadler 13, remark 1.17](#BenZviNadler13)) it is observed that 

$$
  Corr_n(\mathbf{H}) \simeq E_n Alg_b(\mathbf{H}^{op})
$$

is equivalently the [[(∞,n)-category]] of [[En-algebras]] and [[(∞,1)-bimodules]] between them in the [[opposite (∞,1)-category]] of $\mathbf{H}$ (since every object in a cartesian category is uniquely a [[coalgebra]] by its [[diagonal]] map).

(This immediately implies that every object in $Corr_n(\mathbf{H})$ is a self-[[fully dualizable object]].)

To see how this works, consider $X \in \mathbf{H}$ any object regarded as a coalgebra in $\mathbf{H}$ via its [[diagonal map]]. Then a [[comodule]] $E$ over it is a [[co-action]]

$$
  E \to E \times X
$$

and hence is canonically given by just a map $E \to X$. 

Then for 

$$
  \array{
    && E_1 &&&& E_2
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    X && && Y && && Z
  }
$$

two consecutive correspondences, now interpreted as two bi-comodules, their [[tensor product]] of comodules over $Y$ as a coalgebra is the limit over

$$
  E_1 \times E_2
  \stackrel{\to}{\to}
  E_1 \times Y \times E_2
  \stackrel{\to}{\stackrel{\to}{\to}}
  ...
$$

This is indeed the fiber product

$$
  E_1 \underset{Y}{\times} E_2 \stackrel{(p_1, p_2)}{\to} E_1 \times E_2
$$

as it should be for the composition of [[correspondences]].

### With the phased tensor product
 {#PhasedTensorProduct}

+-- {: .num_defn #InSliceWithPhasedTensorProduct}
###### Proposition


For $\mathbf{H}$ an [[(∞,1)-topos]] and $\mathcal{C} \in Cat_{(\infty,n)}(\mathbf{H})$ a [[symmetric monoidal (∞,n)-category|symmetric monoidal]] [[internal (∞,n)-category]] then there is a [[symmetric monoidal (∞,n)-category]]

$$
  Corr_n(\mathbf{H}_{/\mathcal{C}})^\otimes \in SymmMon (\infty,n)Cat
$$

whose [[k-morphisms]] are $k$-fold correspondence in $\mathbf{H}$ over $k$-fold correspondences in $\mathcal{C}$, and whose monoidal structure is given by

$$
  \left[
    \array{
      X_1
      \\
      \downarrow^{\mathrlap{\mathbf{L}_1}}
      \\
      \mathcal{C}_0
    }
  \right]
  \otimes
  \left[
    \array{
      X_2
      \\
      \downarrow^{\mathrlap{\mathbf{L}_2}}
      \\
      \mathcal{C}_0
    }
  \right]
  \coloneqq
  \left[
    \array{
      X_1 \times X_2
      \\
      \downarrow^{\mathrlap{(\mathbf{L}_1, \mathbf{L}_2)}}
      \\
      \mathcal{C}_0 \times \mathcal{C}_0
      \\
      \downarrow^{\mathrlap{\otimes_{\mathcal{C}}}}
      \\
      \mathcal{C}_0
    }
  \right]  
  \,.
$$

=--

This is ([Haugseng 14, def. 4.6, corollary 7.5](#Haugseng14))

+-- {: .num_remark}
###### Remark

If $\mathcal{C}_0$ is (or is regarded as) a [[moduli stack]] for some kind of bundles forming a [[linear homotopy type theory]] over $\mathbf{H}$, then the phased tensor product is what is also called the _[[external tensor product]]_.

=--

+-- {: .num_example}
###### Example

Examples of phased tensor products include

* the [Cauchy product of species](species#HoTTCauchyProduct);

* some [[external tensor products]] in [[indexed monoidal categories]];

=--

## Properties
 {#Properties}

### Full dualizability
 {#FullDualizability}

+-- {: .num_prop #CorrnGrpdHasDuals}
###### Proposition

$Corr_n(\infty Grpd)$ is a [[symmetric monoidal (∞,n)-category|symmetric monoidal]] [[(∞,n)-category with duals]]. 

More generally, if $\mathcal{C}$ is a symmetric monoidal $(\infty,n)$-category with 
duals, then so is $Corr_n(\infty Grpd,\mathcal{C})^\otimes$ equipped with the 
phased tensor product of prop. \ref{InSliceWithPhasedTensorProduct}.

In particular every object in these is a [[fully dualizable object]].

=--

This appears as ([Lurie, remark 3.2.3](#Lurie)). A proof is written down in ([Haugseng 14, corollary 6.6](#Haugseng14)).

+-- {: .num_conjecture }
###### Conjecture


The canonical $O(n)$-[[∞-action]] on $Corr_n(\infty Grpd)$ induced via prop. \ref{CorrnGrpdHasDuals} by the [[cobordism hypothesis]] (see there at _[the canonical O(n)-action](cobordism+hypothesis#TheCanonicalOnAction)_) is trivial.

=--

This statement appears in  ([Lurie, below remark 3.2.3](#Lurie)) without formal proof. It is reproduced as [Haugseng 14, conjecture 1.3](#Haugseng14))]).





More generally:

+-- {: .num_prop }
###### Proposition

For $\mathbf{H}$ an [[(∞,1)-topos]], then $Corr_n(\mathbf{H})$
is an [[(∞,n)-category with duals]].

And generally, for $\mathcal{C} \in SymmMon (\infty,n)Cat(\mathbf{H})$ a [[symmetric monoidal (∞,n)-category]] [[internal (∞,n)-category|internal]] to $\mathbf{C}$, then $Corr_n(\mathbf{H}_{/\mathbf{C}})$ equipped with the phased tensor product of prop. \ref{InSliceWithPhasedTensorProduct} is an [[(∞,n)-category with duals]]

=--

([Haugseng 14, cor. 7.8](#Haugseng14))

Let $Bord_n$ be the [[(∞,n)-category of cobordisms]].

+-- {: .num_prop #HomsFromBordIntoSpan}
###### Claim

The following data are equivalent

1. Symmetric monoidal $(\infty,n)$-functors

   $$
     Bord_n \to Corr_n(\infty Grpd)
   $$

1. Pairs $(X,V)$, where $X$ is a [[topological space]] and $V \to X$ a [[vector bundle]] of [[rank]] $n$.

=--

This appears as ([Lurie, claim 3.2.4](#Lurie)).


## Related concepts

* [[symplectic category]]

* [[span trace]]


* [[relations]], [[bicategory of relations]]

* [[sheaf with transfer]], [[Mackey functor]]

## References

For references on 1- and 2-categories of spans see at _[[correspondences]]_.

An explicit definition of the [[(∞,2)-category]] of spans in [[∞Grpd]] is in section 10 of 

* {#DyckerhoffKapranov12} Tobias Dyckerhoff, [[Mikhail Kapranov]], _Higher Segal spaces I_, ([arxiv:1212.3563](http://arxiv.org/abs/1212.3563))
 


An inductive definition of the [[symmetric monoidal (∞,n)-category]] $Span_n(\infty Grpd)/C$ of spans of [[∞-groupoid]] over a symmetric monoidal $(\infty,n)$-category $C$ is sketched in section 3.2 of 

* {#Lurie} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_
 

there denoted $Fam_n(C)$. Notice the heuristic discussion on page 59.

A detailed version of this definition is given in 

* {#Haugseng14} [[Rune Haugseng]], _Iterated spans and "classical" topological field theories_ ([arXiv:1409.0837](http://arxiv.org/abs/1409.0837))

Both articles comment on the relation to [[schreiber:Local prequantum field theory]].

The extension to the case when the ambient $\infty$-topos is varied is in

* David Li-Bland, _The stack of higher internal categories and stacks of iterated spans_, ([arXiv](http://arxiv.org/abs/1506.08870))



The generalization to an $(\infty,n)$-category $Span_n((\infty,1)Cat^Adj)$ of spans between [[cobordism hypothesis|(∞,n)-categories with duals]] is discussed on p. 107 and 108.

The application of $Span_n(\infty Grpd/C)$ to the construction of [[FQFT]]s is further discussed in section 3 of 

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_

Discussion of $Span_n(\mathbf{H}) \simeq Alg_{E_n}(\mathbf{H}^{op})$ is around remark 1.17 of

* {#BenZviNadler13} [[David Ben-Zvi]], [[David Nadler]], _Nonlinear traces_ ([arXiv:1305.7175](http://arxiv.org/abs/1305.7175))
 


A discussion of a version $Span(B)$for $B$ a [[2-category]] with $Span(B)$ regarded as a [[tricategory]] and then as a 1-object [[tetracategory]] is in

* {#Hoffnung} [[Alex Hoffnung]], _Spans in 2-Categories: A monoidal tricategory_ ([arXiv:1112.0560](http://arxiv.org/abs/1112.0560))
 

A discussion that $Span_2(-)$ in a [[2-category]] with weak [[finite limits]] is a [[compact closed 2-category]]:

* {#Stay13} [[Mike Stay]], _Compact Closed Bicategories_ ([arXiv:1301.1053](http://arxiv.org/abs/1301.1053))
 

[[!redirects (∞,n)-category of spans]]
[[!redirects (∞,n)-categories of spans]]

[[!redirects (infinity,n)-categories of spans]]

[[!redirects (∞,n)-category of correspondences]]
[[!redirects (∞,n)-categories of corespondences]]

[[!redirects (infinity,n)-category of correspondences]]
[[!redirects (infinity,n)-categories of correspondences]]

[[!redirects (∞,1)-category of correspondences]]
[[!redirects (∞,1)-categories of corespondences]]

[[!redirects (infinity,1)-category of correspondences]]
[[!redirects (infinity,1)-categories of correspondences]]

[[!redirects higher correspondence]]
[[!redirects higher correspondences]]

[[!redirects higher category of correspondences]]
[[!redirects higher categories of correspondences]]

[[!redirects Span]]

[[!redirects (∞,n)-category of n-fold correspondences]]
[[!redirects (infinity,n)-category of n-fold correspondences]]

[[!redirects phased tensor product]]
[[!redirects phased tensor products]]


