# Contents 
* table of contents 
{:toc}

## Definition

An [[object]] $x$ in a category $C$ is said to be **rigid** if its [[automorphism group]] is trivial, in other words if any [[isomorphism]] $f : x \cong x$ must be equal to the [[identity morphism]] $f = 1_x : x \to x$.

More generally, an object of an [[n-category]] (or [[(n,r)-category]], etc.) is **rigid** if its higher category $Aut(x)$ of automorphisms is [[terminal object|terminal]].

## Idea

Certain types of questions are made much more difficult to answer by the presence of non-trivial automorphisms (or "symmetries").  In such settings, sometimes it is helpful to first consider the question for rigid objects, and then try to extend the answer to non-rigid objects.  It can even be useful to artificially "point" or "root" the objects of the original category $C$ by moving to a larger category $C_\bullet$ (with a [[forgetful functor]] $C_\bullet \to C$) in which _all_ objects are rigid.

## Examples

* As trivial examples, any [[initial object]] or [[terminal object]] is rigid, as is every object of a [poset](https://ncatlab.org/nlab/show/partial+order#AsACategoryWithExtraProperties). (While trivial, such examples are also significant; e.g., [[universal properties]] may be formulated in terms of initial or terminal objects in suitable categories.) 

* In [[graph theory]], a rigid object in the category of undirected graphs is called an _asymmetric graph_.

* Let $C$ be the category of [[transitive action|transitive]] [[G-sets]] for some group $G$.  Although a transitive $G$-set may in general have non-trivial automorphisms, these symmetries can be killed off by moving to the larger category $C_\bullet$ of _pointed_ transitive $G$-sets, whose objects are pairs of a transitive $G$-set $X$ equipped with an element $r \in X$, and whose morphisms $f : (X,r) \to (Y,s)$ are $G$-equivariant functions $f : X \to Y$ preserving the point $f(r) = s$.  Indeed, suppose $f : (X,r) \to (X,r)$ is any endomorphism of $(X,r)$, and let $x \in X$ be any element.  By the assumption that $G$ acts transitively on $X$, there exists $g \in G$ such that $x = g * r$.  But then by equivariance and preservation of the point we have that
$$f(x) = f(g*r) = g*f(r) = g*r = x.$$
Note that this example is relevant to the combinatorics of [[embedded graphs]] (see at [[combinatorial map]]).

* In [[point-set topology]], there are constructions of [[continua]] whose only [[continuous map|continuous]] [[endomorphisms]] are [[constant maps]] and the identity. Examples include so-called "Cook continua". Note that the interest is not merely in the pleasure of concocting exotic and pathological spaces: there is also some import for category theory, for instance in better understanding the problem of characterizing [[reflective subcategories]] of [[Top]]. See [Kannan and Rajagopolan](#Kannan) (and references therein) for some discussion. 

* In the [[(∞,1)-category]] [[Grpd]], an [[Eilenberg-MacLane space]] $K(G,1)$ is rigid if $G$ has trivial [[center]] and also trivial [[outer automorphism]] group, since $Aut(K(G,1))$ is a homotopy 1-type with $\pi_0(Aut(K(G,1)))=Out(G)$ and $\pi_1(Aut(K(G,1)))=Z(G)$.  In particular, this is the case for $G=S_n$ the [[symmetric group]] on $n$ letters, where $n\ge 3$ and $n\neq 6$.  This allows us to construct an [[monomorphism in an (∞,1)-category|embedding]] of $\mathbb{N}$ into the [[object classifier]]. 

* A [[real closed field]] is a rigid object in the category [[Field]] of [[fields]]. 

## Related concepts

* [[groupoid cardinality]]

## References

For a discussion of the example of pointed transitive $G$-sets (among other things), see

* [[Qiaochu Yuan]], "The categorical exponential formula", blog post at Annoying Precision, November 4, 2015. ([web](https://qchu.wordpress.com/2015/11/04/the-categorical-exponential-formula/)) 

Rigid topological spaces are discussed in 

* V. Kannan and M. Rajagopolan, _Constructions and applications of rigid spaces, I_, Adv. Math., Vol. 29 Iss. 1 (July 1978), 89-130. ([web](http://www.sciencedirect.com/science/article/pii/0001870878900063)) 
 {#Kannan}

[[!redirects rigid objects]]
[[!redirects rigid]]