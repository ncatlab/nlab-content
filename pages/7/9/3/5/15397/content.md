
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
The definition of a [[smooth manifold]] is, as usual, given by

: A smooth $n$-manifold is a topological space $M$ equipped with an open cover $U_\alpha$ with homeomorphisms $\phi_\alpha: U_\alpha \to \mathbb{R}^n$ such that the transition maps $\phi_\beta \circ \phi_\alpha^{-1}: \phi_\alpha(U_\alpha \cap U_\beta) \to \phi_\beta(U_\alpha \cap U_\beta)$ are smooth.

If we replace $\mathbb{R}^n$ with some other topological space $X$ (eg. $\mathbb{C}^n$), and "smooth" with some other suitable restriction (eg. analytic), then we get a different kind of manifold. A pseudogroup is a structure we put on $X$ to specify what transition maps are allowed. The usage of pseudogroups to define the corresponding notion of manifolds is described at [[manifolds]].

## Definition

+-- {: .num_defn #Pseudogroup}
###### Definition
Let $X$ be a [[topological space]] (or [[locale]]) and let $H$ be the groupoid whose objects are the open subsets of $X$ and morphisms are the homeomorphisms between them. A **pseudogroup** (also called transformation pseudogroup) on $X$ is a [[wide subcategory|wide]] sub-groupoid $G$ of $H$ (ie. $G$ contains all open subsets of $X$) satisfying the [[sheaf]] property:

* If $g: U \to V$ is a homeomorphism and $U_\alpha$ is a cover of $U$, then $g$ is in $G$ if and only if each restriction $g|_{U_\alpha}: U_\alpha \to g(U_\alpha)$ is in $G$.

Note that in particular the restriction of a map in $G$ remains in $G$.
=--

+-- {: .num_example}
###### Example
We have the following correspondence between common pseudogroups and kinds of manifolds (the precise correspondence is defined in [[manifold]]):

| Topological space | Morphisms | Manifold |
|--|--|--|
| [[real n-dimensional space]] $\mathbb{R}^n$ | [[smooth maps]] | (n-dimensional) [[smooth manifolds]] |
| [[complex n-dimensional space]] $\mathbb{C}^n$ | [[analytic functions]] | (n-dimensional) [[complex manifolds]] |
| n-dimensional upper half-space $H^n = \{(x_1, \ldots, x_n) \in \mathbb{R}^n: x_1 \geq 0\}$ | [[smooth maps]] | [[manifolds with boundary]]|
| the $n$-[[cube]] $I^n = [0, 1]^n$ | [[smooth maps]] | [[manifolds with boundary|manifold with corners]] | 

=--

+-- {: .num_defn #AbstractPseudogroup}
###### Definition
More generally, an **abstract pseudogroup** is a sub-[[inverse semigroup]] of the inverse semigroup of partial bijections of a set (or, even more generally, local automorphisms of an object in more general context).
=--

## Properties

### Relation to effective &#233;tale stacks

In the language of [[topological groupoids]]/[[Lie groupoids]] and their associated [[geometric stacks]], pseudogroups correspond to [[effective Lie groupoid|effective]] [[étale stacks]].  ([Lawson-Lenz 11](#LawsonLenz11), [Carchedi 12, section 2](#Carchedi12)).


## Related concepts

* [[manifold]]
* [[inverse semigroup]]

## References

The concept was introduced in

* {#Cartan05} [[Élie Cartan]], _Sur la structure des groupes infinis de transformation (suite)_ Ann. Sci. &#201;cole Norm. Sup. (3), 22:219&#8211;308, 1905 ([Numdam](http://www.numdam.org/item?id=ASENS_1904_3_21__153_0))

* {#Cartan09} [[Élie Cartan]], _Les groupes de transformations continus, infinis, simples_. Annales Scientifiques de l'&#201;cole Normale Sup&#233;rieure 26: 93&#8211;161, 1909 ([Numdam](http://www.numdam.org/item?id=ASENS_1909_3_26__93_0))

* {#Golab39} St. Golab, _&#220;ber den Begriff der "Pseudogruppe von Transformationen"_ Mathematische Annalen 116: 768&#8211;780 (1939)

The history of the concept is reviewed in 

* B. L. Reinhart, _Differential Geometry of Foliations: The Fundamental Integrability Problem_. Germany: Springer-Verlag, 1983. See the discussion at the end of I &sect;1.

who attributes the term "pseudogroup" to 

* Veblen, Whitehead 1932


The relation of pseudogroups to [[Lie groupoids]] originates with Haefliger, see at _[[Haefliger groupoid]]_. 

Further discussion of the relation of pseudogroups to [[étale groupoids]]/[[étale stacks]] includes

* {#LawsonLenz11} [[Mark Lawson]], [[Daniel Lenz]], _Pseudogroups and their &#233;tale groupoids_ ([arXiv:1107.5511](http://arxiv.org/abs/1107.5511))

* {#Carchedi12} [[David Carchedi]], section 2 of _&#201;tale Stacks as Prolongations_ ([arXiv:1212.2282](http://arxiv.org/abs/1212.2282))

A textbook account is in 

* Alan Paterson, _Groupoids, Inverse Semigroups, and their Operator Algebras_

See also

* Wikipedia, _[Pseudogroup](http://en.wikipedia.org/wiki/Pseudogroup)_

Abstract pseudogroups are studied in  the [[inverse semigroup]] literature, e.g.

* [[Mark V. Lawson]], _Inverse semigroups: the theory of partial symmetries_, World Scientific, 1998.

[[!redirects pseudogroups]]
[[!redirects pseudogroup of transformations]]