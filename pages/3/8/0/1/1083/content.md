
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

* **bounded below** if there is $k \in \mathbb{Z}$ such that $C_{n \leq k} = 0$;

* **bounded above** if there is $k \in \mathbb{Z}$ such that $C_{n \geq k} = 0$;

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

### Abelian structure
 {#AbelianCategoryStructure}

+-- {: .num_theorem #IsAbelian}
###### Theorem

For $\mathcal{A}$ an [[abelian category]] also the category of  chain complexes $Ch_\bullet(\mathcal{A})$ is again an abelian category.

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

In fact:

\begin{proposition}\label{ChInGrothAbCatIsGrothAbCat}
When $\mathcal{A}$ is a [[Grothendieck abelian category]] then so is $Ch_\bullet(\mathcal{A})$. 
\end{proposition}
(e.g. [Hovey (1999), p. 3](#Hovey99), see also [this example](Grothendieck+category#ChainComplexesInGrothAbCat) at *[[Grothendieck category]]*).

Since every [[Grothendieck abelian category]] is [[locally presentable category|locally presentable]] ([Beke 2000, Prop. 3.10](locally+presentable+category#Beke00), see [this example](locally+presentable+category#GrothAbCatsAreLocPresntbl)), it follows that:

\begin{corollary}
When $\mathcal{A}$ is a [[Grothendieck abelian category]] then its category of chain complexes $Ch_\bullet(\mathcal{A})$ is [[locally presentable category|locally presentable]]. 
\end{corollary}

\begin{example}
The assumption in Prop. \ref{ChInGrothAbCatIsGrothAbCat} is fulfilled in the usual situation of chain complexes of $R$-[[modules]] (e.g.: of [[vector spaces]], when $R$ is a field), since for any [[commutative ring]] $R$ the category $R$[[Mod]] is a [[Grothendieck abelian category]] (by [this example](Grothendieck+category#CateoriesOfModules)).
\end{example}

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

In fact $(Ch_\bullet(R Mod), \otimes)$ is a [[closed monoidal category]], 
the [[internal hom]] is the standard [[nLab:internal hom of chain complexes]].

=--


## Related concepts

* [[homotopy category of chain complexes]]

* [[model structure on chain complexes]]

* [[derived category]], [[derived functor]]

* [[(∞,1)-category of chain complexes]]

* [[equivariant chain complex]]

## References

The [[closed monoidal category]]-structure on chain complexes:

* {#EilenbergKelly65} [[Samuel Eilenberg]], [[G. Max Kelly]],  §IV.6 of: *Closed Categories*, in: *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;


Textbook account:

* [[Charles Weibel]], Chapter 1 in: _[[An Introduction to Homological Algebra]]_, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9781139644136](https://doi.org/10.1017/CBO9781139644136), [pdf](https://web.math.rochester.edu/people/faculty/doug//otherpapers/weibel-hom.pdf)&rbrack;


Discussion in the context of [[model structures on chain complexes]]:

* {#Hovey99} [[Mark Hovey]], p. 3 of: *Model category structures on chain complexes of sheaves* (1999) &lbrack;[K-theory:0366](https://faculty.math.illinois.edu/K-theory/0366), [pdf](https://faculty.math.illinois.edu/K-theory/0366/sheaves.pdf), [[Hovey-SheavesOfChainComplexesPreprint.pdf:file]]&rbrack;



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
