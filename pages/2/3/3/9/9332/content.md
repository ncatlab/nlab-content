
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

The generalization of the notion of [[tensor product of modules]] to [[∞-modules]].

## Definition

We start by defining a collection of [[colored operad|colored]] [[symmetric operad]] $Tens^\otimes$ parameterized by the [[simplex category]] $\Delta$ such that for each $k$-[[simplex]] $[k] \in Delta$ the [[algebras over an operad]] over $Tens^\otimes_{[k]}$ are $(n+1)$-tuples of [[associative algebras]] $(A_i)$ together with a consecutive sequence of [[bimodules]] over these (the right algebra of every bimodule being the left algebra of the next one).

The definition is a straightforward generalization of the of the [[operad for modules]] and the [[operad for bimodules]]. 

+-- {: .num_defn }
###### Definition

Write $Tens^\otimes$ for the category (to be thought of as a family of [[categories of operators]] of [[symmetric operads]]) whose

* [[objects]] are triples consisting of 

  * an object $\langle n\rangle \in Assoc^\otimes$ of the [[category of operators]] of the [[associative operad]];

  * an object $[k] \in \Delta$ of the [[simplex category]];

  * two [[functions]] $c_-, c_+ \colon \langle n\rangle^\circ \to [k]$ such that for all $i in \langle n\rangle^\circ$ either $c_+(i) = c_-(i)$ or $c_+(i) = c_-(i) + 1$;

* [[morphisms]] consist if

  * a morphism $\alpha \colon \langle n\rangle \to \langle n'\rangle$ in $Assoc^\otimes$

  * a morphism $\lambda \colon [k'] \to [k]$ in $\Delta$

  such that (...)

=--

([Lurie, def. 4.3.4.1](#Lurie))

We disuss how an object of this category is to be thought of as labeled with "algebra labels $\mathfrak{a_i}$" for vertices of a simplex, an "bimodule lables $\mathfrak{n}_{i, j}$" for edges of the simplex.

+-- {: .num_remark }
###### Remark

By construction there are [[forgetful functors]]

$$
  \Delta^{op}
  \leftarrow
  Tens^\otimes
  \rightarrow
  \mathcal{Ass}^\otimes
  \,.
$$

=--

([Lurie, 4.3.4.1](#Lurie))


+-- {: .num_defn #NotationForTensS}
###### Definition (Notation)

For $S \to \Delta^{op}$ an [[(∞,1)-functor]] (given as a map of simplicial sets from a [[quasi-category]] $S$ to the [[nerve]] of the [[simplex category]]), write

$$
  Tens^\otimes_{S} 
   \coloneqq
  Tens^\otimes \underset{\Delta^{op}}{\times} S
$$ 

for the [[fiber product]] in [[sSet]].

=--

([Lurie, notation 4.3.4.5, 4.3.4.15](#Lurie))

+-- {: .num_prop #SegalConditionOfTens}
###### Proposition

We have 

* $Tens^\otimes_{[0]} \simeq Assoc^\otimes$, the [[associative operad]];

* $Tens^\otimes_{[1]} \simeq BM^\otimes$ the [[operad for bimodules]].

* $Tens^\otimes_{[k]} 
    \simeq 
   Tens^\otimes_{\{0,1\}} 
    \underset{Tens^\otimes_{\{1\}}}{\coprod} 
   Tens^\otimes_{\{1,2\}} 
     \underset{Tens^\otimes_{\{2\}}}{\coprod} 
     \cdots 
     \underset{Tens^\otimes_{\{k-1\}}}{\coprod} 
   Tens^\otimes_{\{k-1,k\}} 
  $

  as an [[(∞,1)-colimit]] in the [[(∞,1)-category]] of [[(∞,1)-operads]] (a dual _[[Segal condition]]_)


=--

([Lurie, example 4.3.4.6, 4.3.4.7, prop. 4.3.4.11](#Lurie))

+-- {: .num_remark}
###### Remark

Prop. \ref{SegalConditionOfTens} implies that for 
$\mathcal{C}^\otimes$ an [[(∞,1)-operad]], the [[(∞,1)-algebras over an (∞,1)-operad]] over the fiber $Tens^\otimes_{[k]}$ in $\mathcal{C}$

$$
  Alg_{Tens^\otimes_{[k]}}(\mathcal{C})
  \simeq
  \underbrace{
  BMod(\mathcal{C}) 
   \underset{Alg(\mathcal{C})}{\times}
  BMod(\mathcal{C})
   \underset{Alg(\mathcal{C})}{\times}
  \cdots
   \underset{Alg(\mathcal{C})}{\times}
  BMod(\mathcal{C})
  }_{k\;factors}
  \,.
$$

=--

([Lurie, 4.3.5](#Lurie))

+-- {: .num_defn #NotationForAlS}
###### Definition (Notation)


For $\mathcal{C}^\otimes \to Tens^\otimes_S$ a [[fibration]] in the [[model structure for quasi-categories]] which exhibits $\mathcal{C}^\otimes$ as an $S$-[[family of (∞,1)-operads]], write

$$
  Alg_S(\mathcal{C}) \hookrightarrow Fun_{Tens^\otimes_S}(Step_S, \mathcal{C}^\otimes)
$$

for the full [[sub-(∞,1)-category]] on those [[(∞,1)-functors]] which send inert morphisms to inert morphisms.

=--

([Lurie, notation 4.3.4.15](#Lurie))




+-- {: .num_prop }
###### Proposition

For an [[(∞,1)-functor]] $S \to \Delta^{op}$ and a [[fibration]] in the [[model structure for quasicategories]] $q \colon \mathcal{C}^\otimes \to Tens_S^\otimes$ exhibiting $\mathcal{C}^\otimes$ as an $S$-[[family of (∞,1)-operads]], then there is an [[equivalence of (∞,1)-categories]]

$$ 
  Alg_{/Tens_S}(\mathcal{C})
  \to 
  Alg_S(\mathcal{C})
  \,.
$$

=--

([Lurie, prop. 4.3.4.17](#Lurie)).

+-- {: .num_defn #NotationForTensGt}
###### Definition (Notation)

Let $\Delta^1 \to \Delta^{op}$ be the map that picks the morphism $\{0,2\} \hookrightarrow \Delta^2$ in the [[simplex category]]. With def. \ref{NotationForTensS} write
 
$$
  Tens^\otimes_{\gt}
  \coloneqq
  Tens_{\Delta^1}^\otimes
  \coloneqq
  Tens^\otimes \underset{\Delta^{op}}{\times} \Delta^1
  \,.
$$

=--

([Lurie, notation 4.3.5.1](#Lurie))

+-- {: .num_remark #BilinearInfinityMap}
###### Remark 

The $Tens^\otimes_{\gt}$ of def. \ref{NotationForTensGt} is a [[correspondence]] of [[(∞,1)-operads]] which exhibits bilinear maps as follows:

An [[∞-algebra over an (∞,1)-operad]] $\gamma_1 \colon Tens^\otimes_{\gt} \times_{\Delta^1} \{1\}$ is equivalently a bimodule 

$$
  X \in {}_{A'} Mod(\mathcal{C})_{C'}
  \,,
$$ 

while an $\infty$-algebra
$\gamma_0 \colon Tens^\otimes_{\gt} \times_{\Delta^1} \{0\}$ is equivalently a pair of bimodules 

$$
  N_1 \in {}_A Mod(\mathcal{C})_B
  \;\;, \;\;
  N_2 \in {}_B Mod(\mathcal{C})_C
 \,.
$$

An extension of $(\gamma_0, \gamma_1)$ through the correspondence hence to a map of [[generalized (∞,1)-operads]] $Tens^\otimes_{\gt} \to \mathcal{C}^\otimes$ is equivalently a pair of [[A-∞ algebra]] maps $A \to A'$ and $B \to B'$ together with a bilinear map $N_1 \otimes N_2 \to X$.
  
=--

([Lurie, beginning of 4.3.4]).

+-- {: .num_defn #RelativeTensorProduct}
###### Definition
(**relative tensor product of $\infty$-bimodules**)

For $q \colon \mathcal{C}^\otimes \to \mathcal{O}^\otimes$
a [[fibration of (∞,1)-operads]], consider a morphism of 
[[generalized (∞,1)-operads]]

$$
  F \colon Tens_{\gt}^\otimes \to \mathcal{C}^{\otimes}
  \,.
$$

This exhibits three [[A-∞ algebras]] $A_i \coloneqq F|_{\{i\}}$, a pair of bimodule objects

$$
  (N_1, N_2) = F|_{[2]}
$$

over $A_0$-$A_1$ and over $A_1$-$A_2$, respectively, 
and a bimodule object $N = F|_{[1]}$ over $A_0$-$A_2$. We say that $N$ exhibits the **relative [[tensor product of ∞-modules]]** of $N_1$ with $N_2$ over $A_1$

$$
  N \simeq N_1 \otimes_{A_1} N_2
$$

if $F$ is an operadic $q$-[[(∞,1)-colimit]]-[[diagram]].
 
=--

([Lurie, def. 4.3.5.3](#Lurie)).

+-- {: .num_remark #TensorProductFunctor}
###### Remark 

Let $\mathcal{C}^\otimes \to Assoc^\otimes$ exhibit a [[monoidal (∞,1)-category]] such that $\mathcal{C}$ has [[geometric realization]] of [[simplicial objects in an (∞,1)-category|simplicial objects]] and the tensor product preserves these separately in each argument. 

Then the tensor product of $\infty$-modules def. \ref{RelativeTensorProduct} extends to an [[(∞,1)-functor]]

$$
  BMod(\mathcal{C})
  \underset{Alg(\mathcal{C})}{\times}
  BMod(\mathcal{C})
  \to 
  BMod(\mathcal{C})
  \,.
$$


=--

([Lurie, example 4.3.5.11](#Lurie))

## References

Section 4.3.5 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

[[!redirects tensor product of ∞-modules]]
