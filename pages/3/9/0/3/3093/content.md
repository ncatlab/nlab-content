Various more or less geometrical concepts are called [[spaces]], to name a few [[vector spaces]], [[topological spaces]], [[algebraic spaces]], ....  If such objects form a [[category]], it is natural to look for the [[subobject]]s and to call them _subspaces_.  However, often the natural subspaces in the field are the [[regular subobjects]]; convsersely, it is also often the case that variants which are not subobjects in categorical sense are allowed, such as an [[immersed submanifold]] (whose image topological subspace is not a manifold in general).


## Definitions and examples

### Vector subspaces

These are very well behaved; as a [[vector space]] $X$ is simply a [[module]] over a [[field]], so a subspace of $X$ is simply a [[submodule]].  More generally, this is a special case of a [[subalgebra]].

Vector subspaces are precisely the [[subobjects]] in [[Vect]].


### Topological subspaces

In the $n$lab, often by a space we mean some variant of the concept of a [[topological space]].  

Given a topological space $X$ in the sense of [[Bourbaki]] (that is, a set $X$ and a topology $\tau_X$) and a [[subset]] $Y$ of $X$, a topology $\tau_Y$ on a set $Y$ is said to be the topology **[[induced topology|induced]]** by the [[inclusion function|set inclusion]] $Y\subset X$ if $\tau_Y = \tau_X \cap_{pw} \{Y\} = \{ U \cap Y | U\in\tau_X \}$. The pair $(Y,\tau_Y)$ is then said to be a (topological) **subspace** of $(X,\tau_X)$.

If a [[continuous map]] $f:Z\to X$ is a [[homeomorphism]] onto its image $f(Z)$ in the induced topology on $f(Z)$, this *inclusion* map is sometimes called an [[embedding]] (by some schools even a neat but nonstandard pun name *moneomorphism* (not a typo!)); $Z$ is thus isomorphic in $Top$ to a subspace of $X$.


### Topological vector subspaces

A 'subspace' of a [[topological vector space]] usually means simply a linear subspace, that is a subspace of the underlying discrete vector space.

However, the subspaces that we really want in categories such as [[Ban]] are the *closed* linear subspaces.  (Essentially, this is because we want our subspaces to be [[complete space|complete]] whenever our objects are complete.)


### Sublocales

... [[sublocale]] ...


### Submanifolds

... [[submanifold]] ...


## Subsites

For Grothendieck topologies, one instead of a subspace has a concept of a [[subsite]]. 


[[!redirects subspace]]
[[!redirects topological subspace]]
