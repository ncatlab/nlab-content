
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Contents
* table of contents 
{: toc}


## Idea 

In [[proof theory]], **primitive recursive arithmetic**, or **PRA**, is a [[finitist mathematics|finitist]], [[quantifier]]-free formalization of the [[natural numbers]].

**PRA** can express arithmetic propositions involving natural numbers and any [[primitive recursive function]], including the operations of addition, multiplication, and exponentiation. 

## As a Skolem theory 

Let $T$ be a [[Lawvere theory]], i.e., a category with finite products $T$ equipped with a bijective-on-objects product-preserving functor $X: Fin^{op} \to T$ where $Fin$ is the category of finite [[cardinals]] and functions. Recall that a [[Skolem theory]] is a Lawvere theory $(T, X: Fin^{op} \to T)$ in which $N = X(1)$ carries a structure of parametrized [[natural numbers object]] in $T$. 

Abstractly, PRA can be described as the initial Skolem theory. Precise statements to this effect are difficult to pin down in the literature. (More later)

## Related pages

* [[ordinal analysis]]
* [[finite mathematics]]

## References

For a [[dependent type theory]] [[conservative extension]] of [[primitive recursive arithmetic]]:

* [[Ulrik Buchholtz]], [[Johannes Schipp von Branitz]], *Primitive Recursive Dependent Type Theory*, LICS '24: Proceedings of the 39th Annual ACM/IEEE Symposium on Logic in Computer Science, Article No. 18, pages 1-12, 08 July 2024 ([arXiv:2404.01011](https://arxiv.org/abs/2404.01011), [doi:10.1145/3661814.3662136](https://doi.org/10.1145/3661814.3662136))