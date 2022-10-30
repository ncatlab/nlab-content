
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _derived category_ $D(\mathcal{A})$ of an [[abelian category]] $\mathcal{A}$ is the [[homotopy category of an (infinity,1)-category|homotopy category]] of the [[(∞,1)-category of chain complexes]] in $\mathcal{A}$: the [[localization]] of the [[category of chain complexes]] $Ch_\bullet(\mathcal{A})$ at the [[quasi-isomorphisms]].

More in detail, associated to $\mathcal{A}$ is

* the [[category of chain complexes]] $Ch_\bullet(\mathcal{A})$ in $\mathcal{A}$ which is naturally a [[homotopical category]];

* the "[[homotopy category of chain complexes]]" $K(\mathcal{A})$;

* the [[stable ∞-category]] $K_\infty(\mathcal{A})$ of [[chain complexes]] in $C$.

The  _derived category_ $D(C)$ of $C$ is equivalently

* the [[homotopy category|1-categorical homotopy category]] of $Ch_\bullet(\mathcal{A})$ with respect to the [[quasi-isomorphisms]];

* the [[homotopy category of an (infinity,1)-category|(∞,1)-categorical homotopy category]] of $K_\infty(\mathcal{A})$.

In either case, this means that under the canonical [[localization]] functor

$$
  Q : Ch_\bullet(\mathcal{A}) \to D(\mathcal{A})
$$

the [[quasi-isomorphisms]] of [[chain complexes]] become true [[isomorphisms]]
and that $D(\mathcal{A})$ is [[universal property|universal]] with respect to this property.

This the derived category is an approximation to the full [[simplicial localization]] of $K(\mathcal{A})$. It is or can be equipped with several further [[properties]] and [[structure]] that give a more accurate approximation. Notably every derived category is a _[[triangulated category]]_, wich is a way of remembering the [[suspension]] and de-suspension operations on its objects, hence its "[[stable (infinity,1)-category|stability]]".


## Definition 

Let $C$ be an [[abelian category]] and $K(C)$ its 
[[category of chain complexes]] modulo [[chain homotopy]]. 

Equip $K(C)$ with the structure of a [[homotopical category]]
by declaring the [[weak equivalences]] to be the
**quasi-isomorphisms**: those morphisms
$f : V \to W$
which induce [[isomorphisms]] in [[homology]], 
$H(f) : H(V) \stackrel{\simeq}{\to} H(W)$. 

+-- {: .num_defn}
###### Definition

The **derived category** $D(C)$ is the [[homotopy category]] of
$K(C)$ with respect to these weak equivalences.

=--

+-- {: .num_remark}
###### Remark

This is a special case of the construction of a [[homotopy category]] of a [[triangulated category]] with respect to a [[null system]].

Let $N(C) \subset K(C)$ be the 
full subcategory of $K(C)$ on those [[chain complexes]] $V$ whose 
[[homology]] vanishes, $H(V) = 0$. Then $f : V \to W$ is a
quasi-isomorphism iff there exists a distinguished triangle
$$
  V \stackrel{f}{\to} W \to cone(f)
$$
with the [[mapping cone]] $cone(f) \in N(C)$.

The derived category is still naturally a [[triangulated category]] itself. 

=--

## Properties

### In terms of injective and projective resolutions

In the case that the underlying [[abelian category]] $\mathcal{A}$ has [enough injectives](injective%20object#EnoughInjectives) or [enough projectives](projective%20object#EnoughInjectives), the [[hom sets]] in the derived category may equivalently be obtained as [[homotopy]]-classes of [[chain maps]] from [[projective resolutions]] to [[injective resolutions]] of chain complexes. 

In view of the existence of the injective and projective [[model structure on chain complexes]] this is a special case of the general fact that [[homotopy categories]] of [[model categories]] may be obtained by forming homotopy classes of maps in the model category from  [[cofibrant resolutions]] to [[fibrant resolutions]]. But here we spell out an direct discussion of this fact for chain complexes.

(...)

For instance ([Schapira prop. 7.3.1](#Schapira)).

(...)

## Related concepts

* [[derived functor]]


## References 

A systematic discussion from the point of view of [[localization]] and [[homotopy theory]] is in section 13 of 

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_

and, similarly, in section 7 of 

* [[Pierre Schapira]], _Categories and homological algebra_ (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf))
 {#Schapira}

A pedagogical introduction is 

* R. P. Thomas, _Derived categories for the working mathematician_ ([arXiv:math.AG/0001045](http://arxiv.org/abs/math.AG/0001045))

A good survey of the more general topic of derived categories is 

* [[Bernhard Keller]], _Derived categories and their uses_ ([ps](http://www.google.de/url?sa=t&source=web&ct=res&cd=6&ved=0CC8QFjAF&url=http%3A%2F%2Fwww.math.jussieu.fr%2F~keller%2Fpubl%2Fdcu.ps&rct=j&q=derived+category&ei=Ib76SsSdAsjb-QaAw7moDw&usg=AFQjCNGIgXLHlprAoR70bGLWQmyKGHDjTQ))

See in particular the list of references given there.

For a discussion in the context of [[(∞,1)-category|(∞,1)-categories]] and in particular [[stable (∞,1)-category|stable (∞,1)-categories]] see [section 13, p. 53](http://www.math.harvard.edu/~lurie/papers/DAG-I.pdf#page=53) of

* [[Jacob Lurie]], _[[Stable ∞-Categories]]_




[[!redirects derived categories]]