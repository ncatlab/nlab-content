# Contents 
* table of contents
{: toc}

## Idea
 
For an object $X$ of a [[coherent category]] $C$, consider $\mathcal{B}(X)$, the Boolean algebra of complemented subobjects of $X$, and then $\mathcal{F}(\mathcal{B}(X))$, the set of all non-empty [[filters]] of $\mathcal{B}(X)$, partially ordered by reverse inclusion. 

There is a canonical (bounded) [[lattice]] homomorphism 

$$\phi_X: Sub(X) \to \mathcal{F}(\mathcal{B}(X))$$ 

taking a subobject $A \hookrightarrow X$ to the filter of complemented subobjects over it. Then $X$ is said to be **filtral** if $\phi_X$ is an isomorphism. 

Furthermore, the category $C$ is said to be **filtral** if each of its objects is covered by a filtral one, that is, for every $Y$ in $C$ there is a [[regular epimorphism]] with $X$ filtral ([Marra-Reggio 18, Sec. 4](#MarraReggio)).

## Examples

* The category of [[compacta]] 

(Presumably because free compact Hausdorff spaces $\beta X$ are filtral.) 


## References

* {#MarraReggio} Vincenzo Marra, Luca Reggio, _A characterisation of the category of compact Hausdorff spaces_, ([arXiv:1808.09738](https://arxiv.org/abs/1808.09738))

