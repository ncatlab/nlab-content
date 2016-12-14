
#Contents#
* table of contents
{:toc}

## Idea 

Chemistry is the branch of physical science that studies the properties of [[condensed matter]], from the scale of [[atom (physics)|atoms]] upwards.

A central part of chemistry is the identification of reaction processes -- _chemical reactions_ -- by which a variety of chemical substances (species of [[atom (physics)|atoms]] or [[molecules]]) interact to form new combinations. Such processes are typically denoted by formulas of the form

$$
  a A + b B \leftrightarrow c C + d D
$$

where the capital letters denote species of [[atom (physics)|atoms]]/[[molecules]], while the lower case letters are [[natural numbers]]. This indicates that $a$ molecules of type $A$ may react with $b$ molecules of type $B$ to $c$ molecules of type $C$ together with $d$ molecules of type $D$. 

In [[thermodynamic equilibrium]] such reactions occur in both directions, whence the double arrow. A reaction of the form

$$
  A \to c C + d D
$$

would be called a _decay_ process. Notice that analogous processes appear elsewhere, for instance there are [[nuclear reactions]] in [[particle physics]] described by the same kind of reaction diagrams. Also [[D-branes]] for the [[topological string]] undergo reaction processes of this form, see [below](#TriangulatedCategoryWithStability).

One might be tempted to recognize [[morphisms]] as in [[category theory]] in this notation, but care needs to be exercised to arrive at a sensible concept. 

## Formalization of reaction processes

It is unlikely that any formalization of reaction processes in category theory will depend on the specific nature of the chemical elements, but more generally attempts include _stochastic Petri nets_ and _triangulated categories with stability conditions_:

### Stochastic Petri nets or Chemical reaction networks

Given a set $S$ of 'species', a **complex** of those species is a function $C : S \to \mathbb{N}$. A **reaction network** is a set of species together with a directed multigraph whose vertices are labelled by complexes of those species. Edges of the multigraph correspond to transitions.

Any reaction network gives rise to a [[Petri net]], and _vice versa_. In either case, we can label each transition by a rate constant in $(0, \infty)$. This gives **stochastic** versions of the nets and networks.

See [BaezNet](#BaezNet)

### Triangulated categories with stability conditions
 {#TriangulatedCategoryWithStability}

One successful formalization in [[category theory]] of the idea of reaction processes appears in the context of [[D-branes]] for the [[B-model]] [[topological string]]. These are (hypothetical) physical objects that appear in different species labeled by [[objects]] in a [[triangulated category|triangulated]] [[derived category]] (of [[quasicoherent sheaves]] on some [[Calabi-Yau variety]]). There are processes

$$
  A \leftrightarrow B \oplus C
$$

by which a brane of type $A$ may decay into a brane of type B and a brane of type C.

While these are not reactions of [[chemical elements]], clearly the general form of reaction processes is similar.

And for the case of these D-branes, there happens to be a well-established and useful mathematical formalization of these reaction processes via [[category theory]]:

Namely every reaction process as above corresponds to a [[homotopy fiber sequence]] (a "distinguished triangle") in the [[triangulated category]], of the form

$$
  B \longrightarrow A \longrightarrow C
  \,.
$$

(See [Aspinwall 04](#Aspinwall04), search the document for the keyword "decay".)


Mathematically such a [[homotopy fiber sequence]] in a [[triangulated category]] precisely expresses the fact that $A$ is a "twisted [[direct sum]]" of $B$ and $C$ ([[extension]], [[semidirect product]]), hence much like the plain [[direct sum]], but with some "interaction" included.

In addition there are _[[Bridgeland stability conditions]]_ on such [[triangulated categories]] of topological D-branes. These determine which of these reaction processes lead to stable compounds, i.e. whether, in the above example, the brane of type $A$ will really decay into branes of type B and C, or if conversely the latter will fuse. (See again [Aspinwall 04](#Aspinwall04), search the document for the keyword "stability".)

After its motivation from [[D-brane]] reaction processes, the study of [[triangulated categories]] with [[Bridgeland stability conditions]] has become a rich and active area of pure [[mathematics]] in itself.




## Related $n$Lab entries

* [[quantum chemistry]]

* [[physics]]

## References

* Wikipedia, _[Chemistry](http://en.wikipedia.org/wiki/Chemistry)_

* Wikipedia, _[Chemical reaction](https://en.wikipedia.org/wiki/Chemical_reaction)_

* {#BaezNet} [[John Baez]], [chemical reaction networks](http://math.ucr.edu/home/baez/networks/)

* {#Aspinwall04} [[Paul Aspinwall]], _D-Branes on Calabi-Yau Manifolds_ ([arXiv:hep-th/0403166](https://arxiv.org/abs/hep-th/0403166))



[[!redirects chemical reaction]]
[[!redirects chemical reactions]]
