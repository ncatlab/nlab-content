
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

Throughout, let $\mathcal{V}$ be a [[Bénabou cosmos]] for [[enriched category theory]]. 

+-- {: .num_defn #TensoringAndCotensoring}
###### Definition
**([[tensoring]] and [[cotensoring]])**

Let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]].

1. A _[[powering]]_ (or _[[cotensoring]]_) of $\mathcal{C}$ over $\mathcal{V}$ is 

   1. a [[functor]]

      $$
        [-,-] 
        \;\colon\;
        \mathcal{V}^{op} \times \mathcal{C} \longrightarrow \mathcal{C}
      $$

   1. for each $v \in \mathcal{V}$ a [[natural isomorphism]] of the form

      \[
        \label{NaturalIsomorphismForCotensoring}
        \mathcal{V}(v, \mathcal{C}(c_1,c_2)  )
        \;\simeq\;
        \mathcal{C}(c_1,[v,c_2])
      \]

1. A _[[copowering]]_ (or _[[tensoring]]_) of $\mathcal{C}$ over $\mathcal{V}$ is 

   1. a [[functor]]

      $$
        (-)\otimes(-)
        \;\colon\;
        \mathcal{V} \times \mathcal{C} \longrightarrow \mathcal{C}
      $$

   1. for each $v \in \mathcal{V}$ a [[natural isomorphism]] of the form

      \[
        \label{NaturalIsomorphismForTensoring}
        \mathcal{C}(v \otimes c_1, c_2)
        \;\simeq\;
        \mathcal{V}(v, \mathcal{C}(c_1,c_2)  )
      \]

If $\mathcal{C}$ is equipped with a (co-)powering it is called _(co-)powered_
over $\mathcal{V}$.

=--

## Properties 

+-- {: .num_prop #TensoringLeftAdjointToCotensoring}
###### Proposition
**([[tensoring]] [[left adjoint]] to [[cotensoring]])**

If $\mathcal{C}$ is both [[tensored and cotensored category|tensored and cotensored]] over $\mathcal{V}$ (Def. \ref{TensoringAndCotensoring}), then for fixed $v \in \mathcal{V}$ the operations of [[tensoring]] with $v$ and of [[cotensoring]] with $\mathcal{V}$ form a pair of [[adjoint functors]]

$$
  \mathcal{C}
    \underoverset
      {\underset{ [v,-] }{\longrightarrow}}
      {\overset{ v \otimes (-) }{\longleftarrow}}
      {\phantom{AA}\bot\phantom{AA}}
  \mathcal{C}
$$

=--

+-- {: .proof}
###### Proof

The hom-isomorphism characterizing the pair of [[adjoint functors]] is provided by the [[composition]] of 
the [[natural isomorphisms]] (eq:NaturalIsomorphismForCotensoring) and (eq:NaturalIsomorphismForTensoring):

$$
  \array{
    \mathcal{C}(v \otimes c_1, c_2)
    \;\simeq\;
    \mathcal{V}(v, \mathcal{C}(c_1,c_2)  )
    \;\simeq\;
    \mathcal{C}(c_1,[v,c_2])
  }
$$

=--

It follows that:

+-- {: .num_prop #InTensoredCotensoredCategoryInitialObjectIsEnrichedInitial}
###### Proposition
**(in [[tensored and cotensored categories]] [[initial object|initial]]/[[terminal objects]] are enriched initial/terminal)**

If $\mathcal{C}$ is both [[tensored and cotensored category|tensored and cotensored]] over $\mathcal{V}$ then 

1. an [[initial object]] $\emptyset$ of the underlying [[category]] of $\mathcal{C}$ is also enriched initial, in that the [[hom-object]] out of it is the [[terminal object]] $\ast$ of $\mathcal{V}$

   $$
     \mathcal{C}(\emptyset, c) \;\simeq\; \ast
   $$

1. a [[terminal object]] $\ast$ of the underlying category of $\mathcal{C}$ is also enriched terminal, in that the [[hom-object]] into it is the [[terminal object]] of $\mathcal{V}$:

   $$
     \mathcal{C}(c, \ast) \;\simeq\; \ast
   $$

=--

+-- {: .proof}
###### Proof

We discuss the first claim, the second is [[formal duality|formally dual]].

By prop. \ref{TensoringLeftAdjointToCotensoring}, tensoring is a [[left adjoint]]. Since [[left adjoints preserve colimits]], and since an [[initial object]] is the [[colimit]] over the [[initial category|empty diagram]], it follows that 

$$
  v \otimes \emptyset \;\simeq\; \emptyset
$$

for all $v \in \mathcal{V}$, in particular for $\emptyset \in \mathcal{V}$. Therefore the natural isomorphism (eq:NaturalIsomorphismForTensoring) implies for all $v \in \mathcal{V}$ that 

$$
  \mathcal{C}(\emptyset, c)
  \;\simeq\;
  \mathcal{C}( \emptyset \otimes \emptyset, c )
  \;\simeq\;
  \mathcal{V}( \emptyset, \mathcal{C}(\emptyset, c) )
  \;\simeq\;
  \ast
$$

where in the last step we used that the [[internal hom]] $\mathcal{V}(-,-) = [-,-]$ in $\mathcal{V}$ sends [[colimits]] in its first argument to [[limits]] ([this prop.](hom-functor+preserves+limits#InternalHomPreservesLimits)) and used that a terminal object is [[generalized the|the]] [[limit]] over the [[empty category|empty diagram]].

=--

## Examples

+-- {: .num_example}
###### Example

The [[symmetric monoidal category|symmetric]] [[closed monoidal category]] $\mathcal{V}$ is tensored and cotensored over itself, with tensoring being its [[tensor product]] and [[powering]] being its [[internal hom]].

=--

+-- {: .num_example}
###### Example

For $\mathcal{C}$ a [[small category|small]] $\mathcal{V}$-[[enriched category]], the $\mathcal{V}$-enriched [[category of enriched presheaves]] $[\mathcal{C}^{op}, \mathcal{V}]$ is tensored and cotensored ([this Prop.](geometry+of+physics+--+categories+and+toposes#UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg))

=--

+-- {: .num_example}
###### Example

If $\mathcal{C}$ is a [[partial order|poset]] (or merely a pre-ordered set), then it is enriched over the two-object category of [[truth value|truth values]]. In this case, $\mathcal{C}$ is powered precisely when it has a greatest element, and it is co-powered precisely when it has a least element. If $\mathcal{C}$ is powered, then for all $x\in \mathcal{C}$, $x^1 = x$ and $x^0$ is the greatest element of $\mathcal{C}$. If $\mathcal{C}$ is co-powered, then $1 \cdot x = x$ and $0 \cdot x$ is the least element of $\mathcal{C}$.

=--

## Related concepts

* [[two-variable adjunction]]

* [[enriched model category]]


## References

* [[G. Max Kelly]], *Adjunction for enriched categories*, in: *Reports of the Midwest Category Seminar III*, Lecture Notes in Mathematics **106**, Springer (1969) &lbrack;[doi:10.1007/BFb0059145](https://doi.org/10.1007/BFb0059145)&rbrack;

[[!redirects powered and copowered categories]]

[[!redirects tensored and cotensored category]]
[[!redirects tensored and cotensored categories]]

