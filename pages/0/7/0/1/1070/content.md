#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

For $C$ an [[abelian category]], notice that
naturally associated to $C$ is

* the [[category of chain complexes]] $K(C)$ in $C$ which
is naturally a [[homotopical category]];

* the [[stable ∞-category]] $K_\infty(C)$ of [[chain complexes]] in $C$.


The  _derived category_ $D(C)$ of $C$ is equivalently

* the [[homotopy category|1-categorical homotopy category]] of $K(C)$;

* the [[homotopy category of an (infinity,1)-category|(∞,1)-categorical homotopy category]] of $K_\infty(C)$.

In either case, this means that under the canonical [[localization]] functor
$$
  Q : K(C) \to D(C)
$$
the [[quasi-isomorphisms]] of [[chain complexes]] become true [[isomorphisms]]
and that $D(C)$ is [[universal property|universal]] with respect to this
property.




## Definition ##

Let $C$ be an [[abelian category]] and $K(C)$ its 
[[category of chain complexes]] modulo [[chain homotopy]]. 

Equip $K(C)$ with the structure of a [[homotopical category]]
by declaring the [[weak equivalences]] to be the
**quasi-isomorphisms**: those morphisms
$f : V \to W$
which induce [[isomorphisms]] in [[homology]], 
$H(f) : H(V) \stackrel{\simeq}{\to} H(W)$. 

The **derived category** $D(C)$ is the [[homotopy category]] of
$K(C)$ with respect to these weak equivalences.



### Remark ###

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




##References##

A disucssion in a comprehensive [[category theory|category theoretic]] and [[homological algebra]]-context is in [section 13](Categories and Sheaves) of

* Kashiwara-Schapira, [[Categories and Sheaves]]

A pedagogical introduction is 

* R. P. Thomas, _Derived categories for the working mathematician_ ([arXiv](http://arxiv.org/abs/math.AG/0001045))

A good survey of the more general topic of derived categories is 

* [[Bernhard Keller]], _Derived categories and their uses_ ([ps](http://www.google.de/url?sa=t&source=web&ct=res&cd=6&ved=0CC8QFjAF&url=http%3A%2F%2Fwww.math.jussieu.fr%2F~keller%2Fpubl%2Fdcu.ps&rct=j&q=derived+category&ei=Ib76SsSdAsjb-QaAw7moDw&usg=AFQjCNGIgXLHlprAoR70bGLWQmyKGHDjTQ))

See in particular the list of references given there.

For a discussion in the context of [[(∞,1)-category|(∞,1)-categories]] and in particular [[stable (∞,1)-category|stable (∞,1)-categories]] see [section 13, p. 53](http://www-math.mit.edu/~lurie/topoibook/DAGI.pdf#page=53)

of

* [[Jacob Lurie]], [[Stable ∞-Categories]]




[[!redirects derived categories]]