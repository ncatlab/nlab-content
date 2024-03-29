# Subspaces
* table of contents
{: toc}

## Idea

Various more or less geometrical concepts are called [[spaces]], to name a few [[vector spaces]], [[topological spaces]], [[algebraic spaces]], ....  If such objects form a [[category]], it is natural to look for the [[subobjects]] and to call them _subspaces_.  However, often the natural subspaces in the field are the [[regular subobjects]]; conversely, it is also often the case that variants which are not subobjects in the categorical sense are allowed, such as an [[immersed submanifold]]. (These may have self-intersections, and then the immersion map is not monic, nor can this map be replaced by the inclusion of the image, since this image is usually not a manifold.)


## Definitions and examples

### Vector subspaces

These are very well behaved; as a [[vector space]] $X$ is simply a [[module]] over a [[field]], so a subspace of $X$ is simply a [[submodule]].  More generally, this is a special case of a [[subalgebra]].

Vector subspaces are precisely the [[subobjects]] in [[Vect]].


### Topological subspaces

Given a [[topological space]] $X$ (in the sense of [[Bourbaki]], that is: a set $X$ and a topology $\tau_X$) and a [[subset]] $Y$ of $X$, a topology $\tau_Y$ on a set $Y$ is said to be the topology **[[induced topology|induced]]** by the [[inclusion function|set inclusion]] $Y\subset X$ if $\tau_Y = \tau_X \cap_{pw} \{Y\} = \{ U \cap Y | U\in\tau_X \}$. The pair $(Y,\tau_Y)$ is then said to be a (topological) **subspace** of $(X,\tau_X)$.

If a [[continuous map]] $f:Z\to X$ is a [[homeomorphism]] onto its [[image]] $f(Z)$ in the induced topology on $f(Z)$, this *inclusion* map is sometimes called an [[embedding]]; $Z$ is thus isomorphic in [[Top]] to a subspace of $X$.

See at _[[topological subspace]]_.


### Topological vector subspaces

A 'subspace' of a [[topological vector space]] usually means simply a [[linear subspace]], that is a subspace of the underlying discrete vector space.

However, the subspaces that we really want in categories such as [[Ban]] are the *closed* linear subspaces.  (Essentially, this is because we want our subspaces to be [[complete space|complete]] whenever our objects are complete.)


### Sublocales

Given a [[locale]] $L$, which can also be thought of as a [[frame]], a [[sublocale]] of $L$ is given by a [[nucleus]] on the frame $L$.  Even if $L$ is [[topological locale|topological]], so that $L$ can be identified with a [[sober space|sober]] [[topological space]], still there are generally many more sublocales of $L$ than the topological ones.


### Submanifolds

... [[submanifold]] ...


## Subsites

For [[Grothendieck topology | Grothendieck topologies]], one instead of a subspace has a concept of a [[subsite]]. 


## Related concepts

* [[subobject]]

* [[linear subspace]]


[[!redirects subspace]]
[[!redirects subspaces]]
