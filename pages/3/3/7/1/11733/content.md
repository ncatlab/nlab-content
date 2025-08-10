
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

[[cohomology|Cohomology theories]] often have two aspects, which one might refer to as _geometric_ and _arithmetic_. A prototypical example is the [[l-adic cohomology]] $H^{i}(X, \mathbb{Z}_{l})$ of a (sufficiently nice) [[scheme]] $X$ over a field $k$ of [[positive characteristic|characteristic]] $p$, with $l$ coprime to $p$. This is not only an abelian group (the geometric aspect), but a representation of the [[absolute Galois group]] of $k$ (the arithmetic aspect). 

In the case of the [[singular cohomology]] of a complex manifold, the 'arithmetic' aspect arises as the [[Hodge structure]] on the cohomology groups. It has been speculated (for example by Manin?) that there should be some kind of '[[Galois group]]' whose representations are Hodge structures, (and similarly for mixed Hodge modules vs [[perverse sheaves]], and so on) but this remains mysterious; it may be that a good theory of algebraic geometry over $\mathbb{F}_{1}$ (the would-be "[[field with one element]]") would provide an explanation. 

Tate twists play an important role in cohomology theories with this dual geometric and arithmetic aspect, allowing one to express [[Poincaré duality]] canonically, that is, without choosing an orientation of one's geometric object (scheme, complex manifold, ...). 

In [[étale cohomology]] in [[positive characteristic|characteristic]] $p$, the Tate twist of a $\mathbb{Z} / p\mathbb{Z}$-[[module]], or [[sheaf of modules|sheaf of such modules]], $A$ is, concretely, $A \otimes_{\mathbb{Z} / p\mathbb{Z}} \mathbb{Z}(1)$, where $\mathbb{Z}(1)$ is the abelian group $\mu_{p}$ of $p^{th}$ roots of unity with respect to the algebraic closure of $\mathbb{Z} / p\mathbb{Z}$. For $n \geq 0$, the $n^{th}$ Tate twist of $A$, often denoted $A(n)$, is defined to be the result of carrying out the above construction $n$ times. One defines $\mathbb{Z}(-n)$ to be the dual of $\mathbb{Z}(n)$, that is to say $\mathsf{Hom}_{\mathbb{Z} / p\mathbb{Z} -\mathsf{mod}}(\mathbb{Z}(n), \mathbb{Z} / p\mathbb{Z})$, and defines $A(-n)$ to be $A \otimes_{\mathbb{Z} / p\mathbb{Z}} \mathbb{Z}(-n)$. 

The $l$-adic Tate twist $\mathbb{Z}_{l}(1)$ is defined by means of the inverse system consisting of the groups $\mu_{l^{i}}$ along with the morphisms $\mu_{l^{i+1}} \rightarrow \mu_{l^{i}}$ given by $a \mapsto a^{l}$, for $i \geq 1$, and one can then define $\mathbb{Z}_{l}(n)$ for any integer $n$.

The significance of $\mathbb{Z}_{l}(1)$ is that it is the first $l$-adic homology (or equivalently the étale fundamental group) of $\mathbb{G}_{m}$, the multiplicative group of $\mathbb{Z} / p\mathbb{Z}$ as a scheme (i.e. $\mathbb{A}^{1} \setminus \{ 0 \}$, the affine line over $\mathbb{Z} / p\mathbb{Z}$ minus the origin). It is a free $\mathbb{Z}_{l}$-module of rank $1$, and one therefore deduces that the first $l$-adic cohomology group of $\mathbb{G}_{m}$ is the dual of $\mathbb{Z}_{l}(1)$, that is to say, $\mathbb{Z}_{l}(-1)$. Some basic considerations in $l$-adic cohomology show that $H^{2}(\mathbb{P}^{1}, \mathbb{Z}_{l}(1))$ is canonically isomorphic to $H^{1}(\mathbb{G}_{m}, \mathbb{Z}_{1}(1))$, and thus that $H^{2}(\mathbb{P}^{1}, \mathbb{Z}_{l}(1))$ is canonically isomorphic to $\mathbb{Z}_{l}$ (all of the cohomology groups here are $l$-adic cohomology).

The point of this is that it shows that $\mathbb{Z}_{l}(1)$, that is to say, the Tate twist of $\mathbb{Z}_{l}$, is the correct choice of orientation sheaf in $l$-adic cohomology. And from this follow (with effort!) many things: Tate twists are involved in the canonical formulation of Poincaré duality, as already mentioned, of the Thom isomorphism, of the cycle map, and so on. 

There are variations on how to tell the above story (Deligne's discussion in 1.6 of SGA 4$\frac{1}{2}$, via étale cohomology with compact support, can be recommended for instance), but they all ultimately come down to the fact that $\mathbb{Z}_{l}(1)$ is the correct choice of orientation sheaf in an $l$-adic setting.

To return to our starting point, a crucial remark here is that whilst $\mathbb{Z}_{l}(1)$ is non-canonically isomorphic to $\mathbb{Z}_{l}$ as a $\mathbb{Z}_{l}$-module, the two are not isomorphic as Galois representations. Thus the presence of Tate twists is indispensable to the arithmetic aspect of cohomology.

The analogue of this story goes through for singular cohomology of a complex manifold. The roots of unity in this case are a choice of a square root of $-1$, namely either $i$ or $-i$. The choice is invisible in the geometric part of singular cohomology, namely as an abelian group, but it can be seen in the Hodge structure. The analogue of the computations involving $\mathbb{G}_{m}$ and $\mathbb{P}^{1}$ are that the kernel of the exponential map $\mathbb{C} \rightarrow \mathbb{C}^{\times}$ is $\mathbb{Z}$, and the inclusion of $\mathbb{Z}$ in $\mathbb{C}$ is via $1 \mapsto 2 \pi i$. Thus the Tate twist in singular cohomology is tensoring with $2 \pi i \mathbb{Z}$. 

Tate twists are so fundamental that they are built into Grothendieck's definition of the category of [[pure motives]]: one formally inverts (this is the analogue of taking the dual in the above story) the Lefschetz motive, namely the motive of a pointed $\mathbb{P}^{1}$.

Tate twists are also fundamental in the various approaches to mixed motives, including Voevodsky's. Indeed, in the definition of motivic cohomology via hypercohomology or via the derived category of mixed motives, 'all the interesting part' comes from a certain complex of presheaves with transfers built from $\mathbb{G}_{m}$ in a way which is formally entirely analogous to the story we told above. In the definition of motivic cohomology via motivic homotopy theory, 'all the interesting part' comes from the inversion of smashing with the 'algebraic circle', namely a pointed $\mathbb{G}_{m}$. 

As a final remark, rational Tate twists can also be made sense of, and are used for instance in geometric representation theory.


## Definition

For $n \in \mathbb{N}$ write $\mu_n \to \mathbb{G}_m \stackrel{(-)^n}{\longrightarrow}\mathbb{G}_m$ for the $n$th [[Kummer sequence]]. Then for $k \in \mathbb{N}$ the $k$-fold [[tensor power]] of the group of $n$th [[roots of unity]]

$$
  \mathbb{Z}/n\mathbb{Z}(k) \coloneqq \mu_n^{\otimes k}
$$

is called the $k$th _Tate twist_.

(...)

## References

* Kanetomo Sato, _$p$-adic &#233;tale Tate twists and arithmetic duality_ ([arXiv:0610426](http://arxiv.org/abs/math/0610426))

[[!redirects Tate twists]]