#Idea#

The _action groupoid_ $S//G$ of the [[action]] $\rho$ of a [[group]] $G$ on a set $S$ is a [[homological resolution|resolution]] of the quotient set $S/G$ (the set of $G$-orbits): instead of taking the elements in $S$ on the same $G$-orbit as being [[equality|equal]] in $S/G$, in the action groupoid they are just [[isomorphism|isomorphic]].

#Definition#

In components, the action [[groupoid]] $S//G$ 
of the [[action]] 
$\rho : S \times G \to S$ of a group $G$ on the set $S$
(or, more precisely, $S//_\rho G$) is the [[groupoid]]
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

$S//G$ is the [[pseudo colimit]] of $\rho$,

$$
  S//G \simeq weakcolim_{\mathbf{B}G} \rho
  \,.
$$

The weak universal cocone consists of cells of the form

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


#References#

* John Armstrong's article, [Groupoids (and more group actions)](http://unapologetic.wordpress.com/2007/06/09/groupoids-and-more-group-actions/)

* John Baez, [TWF 249](http://math.ucr.edu/home/baez/week249.html)