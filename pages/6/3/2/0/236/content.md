#Idea#

Given an [[action]] $\rho$ of a [[group]] $G$ on a [[set]] $S$, the action groupoid $S//G$ is a bit like the quotient set $S/G$ (the set of $G$-orbits).  But, instead of taking elements of $S$ in the same $G$-orbit as being [[equality|equal]] in $S/G$, in the action groupoid they are just [[isomorphism|isomorphic]].  We may think of the action groupoid as a [[homological resolution|resolution]] of the usual quotient.  When the action of $G$ on $S$ fails to be free, the action groupoid is generally better-behaved than the quotient set.

The action groupoid also goes by other names, including 'weak quotient'.  It is a special case of a 'pseudo colimit', as explained below. It is also called a "[[semidirect product]]" and then written $S \rtimes G$. The advantage of this is that it accords with the generalisation to the action of a group $G$ on a groupoid $S$, which is relevant to orbit space considerations, since if $G$ acts on a space $X$ it also acts on the fundamental groupoid of $X$ (see "Topology and Groupoids", Chapter 11). 

#Definition#

Given an [[action]] 
$\rho : S \times G \to S$ of a group $G$ on the set $S$, the _action groupoid_ $S//G$ (or, more precisely, $S//_\rho G$) is the [[groupoid]] for which:

* an object is an element of $S$

* a morphism from $s \in S$ to $s' \in S$ is a group element $g \in G$ with $g s = s'$.  So, a general morphism is a pair $(g,s) : s \to g s$.

* The composite of $(g,s) : s \to g s = s'$ and $(g',s'): 
s \to g's'$ is $(g' g, s) : s \to g' g s$.

Equivalently, we may define the _action groupoid_ $S//G$ to be the groupoid
$$
  \array{
     && S \times G
     \\
     & {}^{s := p_1}\swarrow
     &&
     \searrow^{t = \rho}
     \\
     S
     &&&&
     S
  }
$$
with composition 
$$(S \times G) \times_{t,s} (S \times G) \simeq S \times G \times G \to S \times G$$ 
given by the product in $G$.

We can denote the morphisms in $S//G$ by

$$S//G:=\{s\stackrel{g}{\to} \rho(s,g) | s\in S, g\in G\}.$$


#Interpretations#


On top of the above explicit definitions, there are several useful ways to think of action groupoids. 

Recall that the action $\rho$ is equivalently thought of as a functor

$$
  \rho : \mathbf{B}G \to Sets
$$

from the [[group]] $G$ regarded as a one-object groupoid, denoted $\mathbf{B}G$.

This functor sends the single object of $\mathbf{B}G$ to the set $S$.


## As a pseudo colimit ##

$S//G$ is the [[2-limit|2-colimit]] of $\rho$,

$$
  S//G \simeq colim_{\mathbf{B}G} \rho
  \,.
$$

The universal cocone consists of cells of the form

$$
  \array{
     S &&\stackrel{\rho(g)}{\to}&& S
     \\
     & \searrow &\stackrel{\simeq}{\Leftarrow}& \swarrow
     \\
     && S//G
  }
  \,,
$$

where the 2-morphism is uniquely specified and in components given by $s \mapsto (s \stackrel{g}{\to} \rho(s,g))$.

## As associated universal bundle ##

Let $Set_*$ be the category of pointed sets and $Sets_* \to Sets$ be the canonical forgetful functor. 
We can think of this as the "universal $Set$-bundle".

Then $S//G$ is the pullback

$$
  \array{
    S//G
    &\to&
    Sets_*
    \\
    \downarrow
    &&
    \downarrow
    \\
    \mathbf{B}G
    &\stackrel{\rho}{\to}&
    Sets
  }
  \,.
$$


One place where we discussed this is the comment [It was David Roberts who apparently first noticed...](http://golem.ph.utexas.edu/category/2007/08/on_hess_and_lack_on_bundles_of_1.html#c019094).

Notice also that an action of $G$ on the set $S$ gives rise to a morphism $p: S \rtimes G \to G$ which has the property of unique path lifting, or in other words is a discrete opfibration. It is also called a covering morphism of groupoids, and models nicely covering maps of spaces. 

Higgins used this idea to lift presentations of a group $G$ to presentations of the  covering morphism of $G$ derived from the action of $G$ on cosets, and so to apply graph theory to obtain old and new subgroup theorems in group theory. 

##As a stack##

In the case where the action is [[internalization|internal]] to sets with structure, such as internal to [[Diff]] one wants to realize the action groupoid as a [[Lie groupoid]]. That Lie groupoid in turn may be taken to present a [[differentiable stack]] which then usually goes by the same name $S//G$.

#References#

* P.J. Higgins, 1971, "Categories and Groupoids", van
Nostrand, {New   York}. Reprints in Theory and Applications of Categories, 7 (2005) pp 1--195.

* R. Brown, "Topology and groupoids", Booksurge, 2006. 

* John Armstrong's article, [Groupoids (and more group actions)](http://unapologetic.wordpress.com/2007/06/09/groupoids-and-more-group-actions/)

* John Baez, [TWF 249](http://math.ucr.edu/home/baez/week249.html)


[[!redirects action group]]