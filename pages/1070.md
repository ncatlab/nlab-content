#Idea#

For $C$ an [[abelian category]], notice that
naturally associated to $C$ is

* the [[category|1-category]] $K(C)$ of [[chain complexes]]  in $C$ which
is naturally a [[homotopical category]];

* the [[stable ∞-category]] $K_\infty(C)$ of [[chain complexes]] in $C$.


The  _derived category_ $D(C)$ of $C$ is equivalently

* the [[homotopy category|1-categorical homotopy category]] of $K(C)$;

* the [[homotopy category of an (infinity,1)-category|(∞,1)-categorical homotopy category]] of $K_\infty(C)$.

In either case, this means that under the canonical localization functor
$$
  Q : K(C) \to D(C)
$$
the [[quasi-isomorphisms]] of [[chain complexes]] become true [[isomorphisms]]
and that $D(C)$ is [[universal property|universal]] with respect to this
property.




#1-Categorical definition#

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



## Remark ##

This is a special case of the construction of a homotopy category
of a [[triangulated category]] with respect to a [[null system]].

Let $N(C) \subset K(C)$ be the 
full subcategory of $K(C)$ on those [[chain complexes]] $V$ whose 
[[homology]] vanishes, $H(V) = 0$. Then $f : V \to W$ is a
quasi-isomorphism iff there exists a distinguished triangle
$$
  V \stackrel{f}{\to} W \to cone(f)
$$
with the [[mapping cone]] $cone(f) \in N(C)$.


##References##

For instance [section 13]() of

* Kashiwara-Schapira, [[Categories and Sheaves]]



#$(\infty,1)$-Categorical definition#


##References##

For instance [section 13, p. 53](http://www-math.mit.edu/~lurie/topoibook/DAGI.pdf#page=53)
of

* [[Jacob Lurie]], [[Stable ∞-Categories]]



#Remarks#

* The derived category is still naturally a [[triangulated category]] 
itself. 

[[!redirects derived categories]]