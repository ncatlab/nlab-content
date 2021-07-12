
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let  $\mathcal{A}$ be an [[additive category]]. 

Recall the notion of _[[chain complex]]_, of _[[chain map]]_ between chain complexes and of _[[chain homotopy]]_ between chain maps in $\mathcal{A}$.

Call a [[chain complex]] $C_\bullet$

* **bounded below** if there is $k \in \mathbb{N}$ such that $C_{n \leq k} = 0$;

* **bounded above** if there is $k \in \mathbb{N}$ such that $C_{n \geq k} = 0$;

* **bounded** if it is bounded below and bounded above.
We have 

+-- {: .num_defn }
###### Definition

Write $Ch_\bullet(\mathcal{A})$ for the [[category]] whose [[objects]] are [[chain complexes]] in $\mathcal{A}$ and whose [[morphisms]] are [[chain maps]] between these.

This is the **category of chain complexes** in $\mathcal{A}$.

=--

Several variants of this category are of relevance.

+-- {: .num_defn }
###### Definition

Write $Ch_\bullet^{+,-,b}(\mathcal{A}) \hookrightarrow Ch_\bullet(\mathcal{A})$ for the [[full subcategory]] on the chain complexes which are, respectively, bounded above, bounded below or bounded.

=--

+-- {: .num_defn }
###### Definition

Write $K(\mathcal{A})$ for the category obtained from $Ch_\bullet(\mathcal{A})$ by identifying [[chain homotopy|homotopic]] chain maps.

$$
  K(\mathcal{A})(C_\bullet, D_\bullet)
  \coloneqq
  Ch_\bullet(C_\bullet, D_\bullet)/chain-homotopy
  \,.
$$

Accordingly $K^{+,-,b}(\mathcal{A}) \hookrightarrow K(\mathcal{A})$ denotes the [[full subcategory]] on the chain complexes bounded above, bounded below or bounded, respectively.

=--

This is sometimes called the _[[homotopy category of chain complexes]]_. But see the warning on terminology there, as this term is also appropriate for the category in the following remark.

+-- {: .num_remark }
###### Remark

If $\mathcal{A}$ is moreover an [[abelian category]], then 
there is also the **[[derived category]]**
$D(\mathcal{A})$, obtained from $Ch_\bullet(\mathcal{A})$ or $K(\mathcal{A})$ by [[localization|universally inverting]] all [[quasi-isomorphisms]]. See at _[[derived category]]_ for more on this.

=--

## Properties

### Abelian category 
 {#AbelianCategoryStructure}

+-- {: .num_theorem #IsAbelian}
###### Theorem

For $\mathcal{A}$ an [[abelian category]] also the category of 
chain complexes $Ch_\bullet(\mathcal{A})$ is again an abelian category.

=--

We discuss the ingredients that go into this statement.

(...)

+-- {: .num_prop #KernelsOfChainComplexes}
###### Proposition

For $f : C_\bullet \to D_\bullet$ a [[chain map]], 

* the complex $ker(f)$ of degreewise [[kernels]] in $\mathcal{A}$ is the kernel of $f$ in $Ch_\bullet(\mathcal{A})$;

* the complex $coker(f)$ of degreewise [[cokernels]] in $\mathcal{A}$ is the cokernel of $f$ in $Ch_\bullet(\mathcal{A})$.

=--

+-- {: .num_remark #ShortExactSequencesDegreewise}
###### Remark

A sequence of chain complexes $0 \to A_\bullet \to B_\bullet \to C_\bullet \to 0$ is a [[short exact sequence]] in $Ch_\bullet(\mathcal{A})$ precisely if each component $0 \to A_n \to B_n \to C_n \to 0$ is a short exact sequence in $\mathcal{A}$.

=--

(...)

### Closed monoidal structure

+-- {: .num_prop }
###### Proposition

Equipped with the standard [[tensor product of chain complexes]] $\otimes$
the category of chain complexes is a [[monoidal category]]
$(Ch_\bullet(R Mod), \otimes)$. The [[unit object]]
is the chain complex concentrated in degree 0 on the tensor unit $R$ of $R Mod$. 

=--

+-- {: .num_prop }
###### Proposition

In fact $(Ch_\bullet, \otimes)$ is a [[closed monoidal category]], 
the [[internal hom]] is the standard [[nLab:internal hom of chain complexes]].

=--


## Related concepts

* [[homotopy category of chain complexes]]

* [[model structure on chain complexes]]

* [[derived category]], [[derived functor]]

* [[(∞,1)-category of chain complexes]]

* [[equivariant chain complex]]

## References

A basic introduction is in chapter 1 of 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_



category: category

[[!redirects categories of chain complexes]]

[[!redirects category of cochain complexes]]
[[!redirects categories of cochain complexes]]

[[!redirects category of bounded chain complexes]]
[[!redirects categories of bounded chain complexes]]

[[!redirects category of unbounded chain complexes]]
[[!redirects categories of unbounded chain complexes]]

[[!redirects ChainComplexes]]
[[!redirects ConnectiveChainComplexes]]
