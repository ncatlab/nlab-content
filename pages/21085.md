

#Contents#
* table of contents
{:toc}


## Idea

**Optics** are constructions used in [[computer science]] as bidirectional data accessors. They include [[lens (in computer science)|lenses]] and prisms, used to access, respectively, components of product data types and components of coproduct data types.

Unlike [[lens (in computer science)|lenses]], optics do not require a cartesian structure to be around. That's replaced by a bi-[[actegory|actegorical]] structure and a quotient which 'ties' residual and incoming views.

## Definition

Let $(\mathbf M, I, \otimes)$ be a symmetric monoidal category. Let $\mathbf C$ and $\mathbf D$ be $\mathbf M$-actegories, i.e. there are pseudoactions $\bullet$ and $\ast$ of $\mathbf M$ acts on $\mathbf C$ and $\mathbf D$, respectively.

**Definition 1**. The category of optics $(\mathbf C, \mathbf D)$-mixed optics $\mathrm{Optic}_{\bullet, \ast}(\mathbf C, \mathbf D)$ has objects given by pairs $(X : \mathbf C,Y : \mathbf D)$ and hom-sets given by
$$
  \mathrm{Optic}_{\bullet, \ast}(\mathbf C, \mathbf D)((S,T),(A,B)) = \int^{M : \mathbf M} \mathbf C(S, M \bullet A) \times \mathbf D(M \ast B, T)
$$
Optics are morphisms in this category. See ([Riley](#Riley)) for the composition rule.

**Remark 1**. Concretely, an optic $(S,T) \to (A,B)$ is specified by a triple of $(l, M, r)$ where $M : \mathbf M$ is called *residual*, $l : S \to M \bullet A$ is called 'view' or 'get' or 'forward part' or 'left part', and $r : M \ast B \to T$ is called 'update' or 'put' or 'backward part' or 'right part'.

The [[coend]] in the above definition has the effect of making two optics $(l, M, r)$ and $(l', M', r')$ (with same boundaries) equal if there exists a morphism $\alpha : M \to M'$ such that $(\alpha' \bullet A) \circ l = l'$ or a morphism $\beta:M' \to M$ such that $r = r' \circ (\beta \ast B)$.

One says optics are defined _up to sliding_ along the residual, a terminology suggested by the graphical representation of optics as open diagrams, see ([Román](#Roman))

##References

* {#Riley} [[Mitchell Riley]], _Categories of optics_, ([arXiv:1809.00738](https://arxiv.org/abs/1809.00738))

* Bryce Clarke, Derek Elkins, Jeremy Gibbons, Fosco Loregian, Bartosz Milewski, Emily Pillmore, Mario Román, _Profunctor optics, a categorical update_, ([arXiv:2001.07488](https://arxiv.org/abs/2001.07488))

* Emily Pillmore, Mario Román, _Profunctor Optics: The Categorical View_, ([blog post](https://golem.ph.utexas.edu/category/2020/01/profunctor_optics_the_categori.html#more))

* {#Roman} Mario Román, _Open Diagrams via Coend Calculus_, ([arXiv:2004.04526](https://arxiv.org/abs/2004.04526))