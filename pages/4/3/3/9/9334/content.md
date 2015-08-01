
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

## Definition


### $(\infty,1)$-Category of $(\infty,1)$-Bimodules and intertwiners

Write $BMod^\otimes$ for the [[(∞,1)-category of operators]] of the [[(∞,1)-operad]] [[operad for bimodules]]. Write 

$$
  \iota_{\pm} \colon Assoc \to BMod
$$

for the two canonical inclusions of the [[associative operad]] (as discussed at _[operad for bimodules - relation to the associative operad](#RelationToTheAssociativeOperad)_).

+-- {: .num_defn #NotationForWeaklyBiEnrichedInfinityCategory}
###### Definition (Notation)

For $p \colon \mathcal{C}^\otimes \to BMod^\otimes$ a [[fibration of (∞,1)-operads]], write

$$
  \mathcal{C}^\otimes_{\pm}
  \coloneqq
  \mathcal{C}^\otimes \underset{BMod^\otimes}{\times}^\pm Assoc^\otimes 
$$

for the two [[fiber products]] of $p$ with the inclusions $\iota_\pm$. The canonical [[projection]] maps

$$
  \mathcal{C}^\otimes_{\pm}
  \to 
  Assoc^\otimes
$$

exhibit these as two [[planar (∞,1)-operads]].

Finally write 

$$
  \mathcal{C} 
    \coloneqq 
  \mathcal{C}^\otimes \underset{BMod^\otimes}{\times} \{\mathfrak{n}\}
$$

for the [[(∞,1)-category]] over the object labeled $\mathfrak{n}$.

=--

([Lurie, notation 4.3.1.11](#Lurie)).

+-- {: .num_remark }
###### Remark

This exhibits $\mathcal{C}$ as equipped with [[weak tensoring]] over $\mathcal{C}_-$ and reverse weak tensoring over $\mathcal{C}_+$.

=--

The most familiar special case of these definitions to keep in mind is the following.

+-- {: .num_remark #MonoidalCategoryAsBitensoredOverItself}
###### Remark

For $\mathcal{C}^\otimes \to Assoc^\otimes$ a [[coCartesian fibration of (∞,1)-operads]], hence exhibiting $\mathcal{C}^\otimes$ as a [[monoidal (∞,1)-category]], [[pullback]] along the canonical map $\phi \colon BMod^\otimes \to Assoc^\otimes$ gives a fibration

$$
  \phi^* \mathcal{C}^\otimes \to BMod^\otimes
$$ 

as in def. \ref{NotationForWeaklyBiEnrichedInfinityCategory} above. In the terminology there this exhibts $\mathcal{C}$ as weakly enriched (weakly [[tensoring|tensored]]) over itself from the left and from the right. 

This is the special case for which bimodules are traditionally considered.

=--

([Lurie, example 4.3.1.15](#Lurie))




+-- {: .num_defn }
###### Definition

For $\mathcal{C}^\otimes \to BMod^\otimes$ a [[fibration of (∞,1)-operads]] we say that the corresponding [[(∞,1)-category]] of [[(∞,1)-algebras over an (∞,1)-operad]]

$$
  BMod(\mathcal{C}) \coloneqq Alg_{/BMod}(\mathcal{C})
$$

is the **$(\infty,1)$-category of $(\infty,1)$-bimodules** in $\mathcal{C}$.

Composition with the two inclusions $\iota_{1,2}\colon Assoc BMod$ of the [[associative operad]] yields a [[fibration]] in the [[model structure for quasi-categories]] $BMod(\mathcal{C}) \to Alg(\mathcal{C}_-)\times Alg(\mathcal{C}_+)$. Then for $A_- \in Alg_{\mathcal{C}_-}$ and $A_+ \in Alg_{\mathcal{C}_+}$ two algebras the [[fiber product]]

$$
  {}_A BMod_{B}(\mathcal{C})
  \coloneqq
  \{A\} 
   \underset{Alg(\mathcal{C}_-)}{\times}
  BMod(\mathcal{C})
   \underset{Alg(\mathcal{C}_-)}{\times}
  \{B\}  
$$

we call the **$(\infty,1)$-category of $A$-$B$-bimodules**.

=--

([Lurie, def. 4.3.1.12](#Lurie))

+-- {: .num_example}
###### Example

For the special case of remark \ref{MonoidalCategoryAsBitensoredOverItself} where the bitensored structure on $\mathcal{C}$ is induced from a monoidal structure $\mathcal{C}^\otimes \to Asoc^\otimes$, we have by the [[universal property]] of the [[pullback]] that

$$
  BMod(\mathcal{C})
  \simeq
  {Alg_{BMod}}_{/Assoc}(\mathcal{C})
  \simeq
  \left\{
    \array{
       && \mathcal{C}
       \\
       &{}^{\mathllap{(A,B,N)}}\nearrow& \downarrow 
       \\
       BMod^\otimes &\to& Assoc^\otimes
    }
  \right\}
$$

=--

+-- {: .num_remark}
###### Remark

Let $\mathcal{C}$ be a [[1-category]], for simplicity. 
Then a [[morphism]] 

$$
  (A_1,B_1,N_1) \to $(A_2,B_2,N_2)$ 
$$

in $BMod(\mathcal{C})$ is a pair $\phi_1 \colon A_1 \to A_1$, $\rho \colon B_1 \to B_2$ of algebra homomorphisms and a morphism $\kappa \colon N_1 \to N_2$ which is "linear in both $A$ and $B$" or "is an [[intertwiner]]" with respect to $\phi$ and $\rho$ in that for all $a \in A$, $b \in B$ and $n \in N$ we have 

$$
  \kappa(a \cdot n \cdot b) = \phi(a) \cdot \kappa(n)    
  \,.
$$

It is natural to depict this by the square diagram

$$
  \array{
    A_1 &\stackrel{N_1}{\to}& B_1
    \\
    {}^{\mathllap{\phi}}\downarrow
    &
    \Downarrow^{\kappa}
    &
    \downarrow^{\mathrlap{\rho}}
    \\
    A_2 &\underset{N_2}{\to}& B_2
  }
  \,.
$$

This notation is naturally suggestive of the existence of the further [[horizontal composition]] by [[tensor product of (∞,1)-modules]], which we come to [below](#TensorProductOfBimodules).

On the other hand, a morphism $N_1 \to N_2$ in ${}_A BMod(\mathcal{C})_B$ is given by the special case of the above for $\phi = id$ and $\rho = id$.


=--


### Tensor products of $(\infty,1)$-Bimodules
 {#TensorProductOfBimodules}


+-- {: .num_defn #NotationForTensS}
###### Definition (Notation)

Write $Tens^\otimes$ for the [[generalized (∞,1)-operad]]
discussed at _[[tensor product of ∞-modules]]_.

For $S \to \Delta^{op}$ an [[(∞,1)-functor]] (given as a map of simplicial sets from a [[quasi-category]] $S$ to the [[nerve]] of the [[simplex category]]), write

$$
  Tens^\otimes_{S} 
   \coloneqq
  Tens^\otimes \underset{\Delta^{op}}{\times} S
$$ 

for the [[fiber product]] in [[sSet]].

Moreover, for $\mathcal{C}^\otimes \to Tens^\otimes_S$ a [[fibration]] in the [[model structure for quasi-categories]] which exhibits $\mathcal{C}^\otimes$ as an $S$-[[family of (∞,1)-operads]], write

$$
  Alg_S(\mathcal{C}) \hookrightarrow Fun_{Tens^\otimes_S}(Step_S, \mathcal{C}^\otimes)
$$

for the full [[sub-(∞,1)-category]] on those [[(∞,1)-functors]] which send inert morphisms to inert morphisms.

=--

([Lurie, notation 4.3.4.15](#Lurie))




### The $(\infty,2)$-Category of $(\infty,1)$-algebras and -bimodules


We discuss the generalization of the notion of bimodules to [[homotopy theory]], hence the generalization from [[category theory]] to [[(∞,1)-category theory]]. ([Lurie, section 4.3](#Lurie)).

Let $\mathcal{C}$ be [[monoidal (∞,1)-category]] such that 

1. it admits [[geometric realization]] of [[simplicial objects in an (∞,1)-category]] (hence a [[left adjoint|left]] [[adjoint (∞,1)-functor]] ${\vert-\vert} \colon \mathcal{C}^{\Delta^{op}} \to \mathcal{C}$ to the constant simplicial object functor), true notably when $\mathcal{C}$ is a [[presentable (∞,1)-category]];

1. the [[tensor product]] $\otimes \colon \mathcal{C}\times \mathcal{C} \to \mathcal{C}$ preserves this geometric realization separately in each argument.


Then there is an 
[[(∞,2)-category]] $Mod(\mathcal{C})$ which given as an [[(∞,1)-category object]] internal to [[(∞,1)Cat]] has

* $(\infty,1)$-category of objects

  $$
    Mod(\mathcal{C})_{[0]} \simeq Alg(\mathcal{C})
  $$

  the [[A-∞ algebras]] and [[∞-algebra]] [[homomorphisms]] in $\mathcal{C}$;

* $(\infty,1)$-category of morphisms

  $$
    Mod(\mathcal{C})_{[1]} \simeq BMod(\mathcal{C})
  $$

  the $\infty$-bimodules and bimodule homomorphisms ([[intertwiners]]) in $\mathcal{C}$

This is ([Lurie, def. 4.3.6.10, remark 4.3.6.11](#Lurie)).

Morover, the [[horizontal composition]] of bimodules in this [[(∞,2)-category]] is indeed the relative 
[[tensor product of ∞-modules]]

$$
  \circ_{A,B,C}
  =
  (-) \otimes_B (-)
  \;\colon\;
  {}_A Mod_{B} \times {}_{B}Mod_C \to {}_A Mod_C
  \,.
$$

This is ([Lurie, lemma 4.3.6.9 (3)](#Lurie)).

Here are some steps in the construction:


The **idea** of the following constructions is this: 
we start with a [[generalized (∞,1)-operad]] 
$Tens^\otimes \to FinSet_* \times \Delta^{op}$ which is such that 
the [[(∞,1)-algebras over an (∞,1)-operad]] over its fiber over $[k] \in \Delta^{op}$ is equivalently the collection of $(k+1)$-tuples of 
[[A-∞ algebras]] in $\mathcal{C}$ together with a string of $k$ $\infty$-bimodules between them. Then we turn that into a [[simplicial object in an (∞,1)-category|simplicial object]] in [[(∞,1)Cat]]

$$
  Mod(\mathcal{C}) \in ((\infty,1)Cat)^{\Delta^{op}}
  \,.
$$

This turns out to be an [[internal (∞,1)-category]] object in [[(∞,1)Cat]], hence an [[(∞,2)-category]] whose object of objects is the category $Alg(\mathcal{C})$ of [[A-∞ algebras]] and [[homomorphisms]] in $\mathcal{C}$ between them, and whose object of morphisms is the category $BMod(\mathcal{C})$ of $\infty$-bimodules and [[intertwiners]].

+-- {: .num_defn}
###### Definition

Define $Mod(\mathcal{C}) \to \Delta^{op}$ as the map of [[simplicial sets]] with the [[universal property]] that for every other map of simplicial set $K \to \Delta^{op}$ there is a canonical bijection

$$
  Hom_{sSet/\Delta^{op}}(K, Mod(\mathcal{C}))
  \simeq
  Alg_{Tens_K / Assoc}( \mathcal{C} )
  \,,
$$

where 

* on the left we have the hom-simplicial set in the [[slice category]]

* on the right we have the [[(∞,1)-category]] of [[(∞,1)-algebras over an (∞,1)-operad]] given by lifts $\mathcal{A}$ in

  $$
    \array{
       && \mathcal{C}^\otimes
       \\
       &{}^{\mathcal{A}}\nearrow& \downarrow
       \\
      Tens_K &\to& Assoc
    }
    \,.
  $$

=--

This is ([Lurie, cor. 4.3.6.2](#Lurie)) specified to the case of ([Lurie, lemma 4.3.6.9](#Lurie)). Also ([Lurie, def. 4.3.4.19](#Lurie))




## References

The general theory in terms of [[higher algebra]] of [[(∞,1)-operads]] is discussed in section 4.3 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_

Specifically the homotopy theory of [[A-infinity bimodules]] is discussed in

* Volodymyr Lyubashenko, Oleksandr Manzyuk, _A-infinity-bimodules and Serre A-infinity-functors_ ([arXiv:math/0701165](http://arxiv.org/abs/math/0701165))

and section 5.4.1 of 

* [[Boris Tsygan]], _Noncommutative calculus and operads_ in 
Guillermo Cortinas (ed.) _Topics in Noncommutative geometry_, Clay Mathematics Proceedings volume 16

The generalization to [[(infinity,n)-modules]] is in 

* {#Haugseng14} [[Rune Haugseng]], _The higher Morita category of $E_n$-algebras_ ([arXiv:1412.8459](http://arxiv.org/abs/1412.8459))


[[!redirects (infinity,1)-bimodules]]


[[!redirects ∞-bimodule]]
[[!redirects ∞-bimodules]]
[[!redirects (∞,1)-bimodule]]
[[!redirects (∞,1)-bimodules]]

[[!redirects (∞,1)-category of (∞,1)-bimodules]]
[[!redirects (infinity,1)-category of (∞,1)-bimodules]]

[[!redirects (∞,1)-categories of (∞,1)-bimodules]]
[[!redirects (infinity,1)-categories of (∞,1)-bimodules]]

[[!redirects infinity-bimodule]]
[[!redirects infinity-bimodules]]