
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

Recall the notion of [[chain complex]], of [[chain map]] and of [[chain homotopy]] in $\mathcal{A}$.

We have 

* $C(A)$, the category of chain complexes and chain chomplex homomorphisms in $C$;

* $K(A)$, the category obtained from $C(A)$ by identifying homotopic chain homomorphisms.

If $A$ is moreover [[abelian category|abelian]], then we also have

* $D(A)$, the [[derived category]] obtained from $C(A)$ (or $K(A)$) by inverting all [[quasi-isomorphism]]s.

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

A sequence of chain complexes $0 \to A_\bullet \to B_\bullet \to C_\bullet \to 0$ is a [[short exact sequence]] in $Ch_\bullet(\mathcal{A})$ precisely if each component $0 \to A_n \to B_n \to C_n \to 0$ is a short exact in $\mathcal{A}$.

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

* [[derived category]], [[derived functor]]

* [[(∞,1)-category of chain complexes]]

## References

A basic introduction is in chapter 1 of 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_



category: category

[[!redirects categories of chain complexes]]

[[!redirects category of cochain complexes]]
[[!redirects categories of cochain complexes]]
