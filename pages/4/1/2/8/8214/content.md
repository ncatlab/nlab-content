
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A natural [[internal hom]] of [[chain complexes]] that makes the [[category of chain complexes]] into a [[closed monoidal category]].

## Definition

Let $R$ be a [[commutative ring]] and $\mathcal{A} = R$[[Mod]] the [[category]] of [[modules]] over $R$. Write $Ch_\bullet(\mathcal{A})$ for the [[category of chain complexes]] of $R$-modules. 


+-- {: .num_defn #ExplicitDefinition}
###### Definition

For $X,Y \in Ch_\bullet(\mathcal{A})$ any two [[objects]], define a chain complex $[X,Y] \in Ch_\bullet(\mathcal{A})$ to have components

$$
  [X,Y]_n 
    \,\coloneqq\, 
  \prod_{i \in \mathbb{Z}} Hom_{R Mod}(X_i, Y_{i+n})
$$ 

(the collection of degree-$n$ maps between the underlying [[graded object|graded]] modules) and whose [[differential]] is defined on homogeneously graded elements $f \in [X,Y]_n$ by

$$
  d f 
    \,\coloneqq\, 
  d_Y \circ f - (-1)^{n} f \circ d_X
  \,.
$$

This defines a [[functor]]

$$
  [-,-] 
   \;\colon\; 
  Ch_\bullet(\mathcal{A})^{op} 
   \times
  Ch_\bullet(\mathcal{A})
  \longrightarrow 
  Ch_\bullet(\mathcal{A})
  \,.
$$

=--


## Properties
 {#Properties}


+-- {: .num_prop}
###### Proposition

The internal hom $[-,-]$ (Def. \ref{ExplicitDefinition}) together with the [[tensor product of chain complexes]] $(\text{-})\otimes (\text{-})$ endow $Ch_\bullet(\mathcal{A})$ with the structure of a [[closed monoidal category]].

=--

+-- {: .num_prop}
###### Proposition

The collection of [[cycles]] of the [[internal hom]] $[X,Y]$ in degree 0 coincides with the external [[hom functor]]

$$
  Z_0\big([X,Y]\big) 
    \,\simeq\, 
  Hom_{Ch_\bullet}(X,Y)
  \,.
$$

The [[chain homology]] of the [[internal hom]] $[X,Y]$ in degree 0 coincides with the [[homotopy classes]] of [[chain maps]].

=--


+-- {: .proof}
###### Proof

By Definition \ref{ExplicitDefinition} the 0-cycles in $[X,Y]$ are collections of morphisms $\{f_k \colon X_k \to Y_k\}$ such that 

$$
  f_{k+1} \circ d_X \;=\; d_Y \circ f_k
  \,.
$$

This is precisely the condition for $f$ to be a [[chain map]].

Similarly, the [[boundaries]] in degree 0 are precisely the collections of morphisms of the form

$$
  \lambda_{k+1} \circ d_X + d_Y \circ \lambda_k
$$

for a collection of maps $\{\lambda_k : X_k \to Y_{k+1}\}$. This are precisely the [[null homotopies]].

=--

From the [remark](tensor+product+of+chain+complexes#CanonicalForgetfulFunctor) at *[[tensor product of chain complexes]]* we have that the canonical forgetful functor $U_{Ch} \coloneqq Ch_\bullet(\mathcal{A})(I_{Ch},-) \colon Ch_\bullet(\mathcal{A}) \to \mathcal{A}$ takes a chain complex to its 0-cycles.

Thus the description of the 0-cycles in the above proposition is equivalent to the statement $U_{Ch}([-,-]) \cong Ch_\bullet(\mathcal{A})(-,-)$, which is true in any closed category.


## Related concepts

* [[tensor product of chain complexes]]

## References

* {#EilenbergKelly65} [[Samuel Eilenberg]], [[G. Max Kelly]],  §IV.6 of: *Closed Categories*, in: *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;



Textbook accounts:

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_

