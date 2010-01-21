

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Equivariant homotopy theory is [[homotopy theory]] for the case that a [[group]] $G$ acts on all the [[topological space]]s involved.


## Homotopy category of $G$-spaces

Let $G$ be a discrete [[group]].

There are (at least) the following two different ways to define the $G$-equivariant stable homtopy theory. They yield equivalent results.

A **$G$-space** is a [[topological space]] equipped with a $G$-[[action]].

A $G$-[[homotopy]]  between $G$-maps $f,g$ is a $G$-map $X \times I \to Y$ where $G$ acts trivially on the factor $I$ in $X \times I$. 

Consider the subcategory of $G$-[[CW-complex]]es and make it a [[category with weak equivalences]] using the $G$- [[homotopy equivalence]]s with the above definition. Then the corresponding [[homotopy category]] $G\mathcal{T}$ is the $G$-**equivariant homotopy category**.

Alternatively, let $O_G$ be the [[orbit category]] of $G$. Let $SPSh(O_G)$ be the category of [[simplicial presheaf|simplicial presheaves]] on $O_G$. Use the global (objectwise) weak equivalences to make this a [[category with weak equivalence]]s. Write $Ho(SPSh(O_G)_{glob})$ for the corresponding [[homotopy category]].

Equivalently, this is the homotopy category of the projective or injective [[model structure on simplicial presheaves]].

**Elmendorf's theorem**

The canonical functor

$$
  G \mathcal{T} \to Ho(SPSh(O_G)_{glob})
$$

that sends a $G$-space to the presheaf that it representes is an [[equivalence of categories]].




## Related concepts

Equivariant homotopy theory is to [[equivariant stable homotopy theory]] as [[homotopy theory]] is to [[stable homotopy theory]].

## References

* [[Peter May]], _Equivariant homotopy and cohomology theory_ ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/alaska1.pdf))

* B. Guillou, _A short note on models for equivariant homotopy theory_ ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf))