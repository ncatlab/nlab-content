[[!redirects category of interest]]
## Motivation  

Many categories of algebraic objects have similar properties. Classically [[abelian categories]], abstracted from categories of modules were central to homological algebra, but many important contexts were non-abelian, some as central as that of groups. In these non-abelian contexts, research has centred on finding common frameworks to understand better both the resulting objects and morphisms and the interpretation of their homological algebra.

There are many types of algebraic object which are 'based' on some type of groups.  Examples include groups themselves, [[modules]] over a ring, including, of course, vector spaces, then, adding more structure, [[associative algebras]], [[commutative algebras]], [[Lie algebras]], [[Leibniz algebras]], [[Poisson algebras]], and then the dialgebras and trialgebras introduced by [[Loday]], as well as [[crossed module]]s of groups. We will call these examples of _group-based universal algebras_. 

The similarities of the homological algebra of these settings suggested a study of what parts of that theory is common to all of these, and, conversely, what parts depend on particular properties of an example.


####Remark on terminology

Before giving the definition,  we note that categories of such group-based universal algebras are more often called _categories of interest_ in the literature.  This term was introduced by Orzech in the first paper on their theory and, although very uninformative, has become fairly standard. Our preference for the title given here is that, hopefully, it does say more of the context of the ideas than merely saying they are 'of interest'.


##Idea

In all these cases, the category, $\mathcal{C}$, of such 'algebras' is [[monadic]] over $Set$.  The monad, $\mathbf{T}=(T,\eta,\mu)$, involved  is such that $T(\emptyset)$ is a singleton, the category $\mathcal{C}$ is [[pointed]], with the algebra $(T(\emptyset),\mu_\emptyset)$, that is the free algebra on the empty set, as its [[zero object]], and is complete and cocomplete. In fact,  $\mathcal{C}$ is monadic over the category, $Set_*$, of _pointed sets_.

Again in all these cases, the forgetful functor, $U:\mathcal{C}\to Set_*$ factors through the category of groups and all the operations in the corresponding algebraic theory of $\mathcal{C}$ are finitary, so $\mathcal{C}$ can be thought of as a category of _groups with extra structure_, much as in the more general [[Omega-groups]].  We have, thus, that $\mathcal{C}$ is equivalent to a category $Grps^{\hat{\mathbf{T}}}$ for some monad $\hat{\mathbf{T}}$. 

Within this abstract setting, one can formulate notions of subobject, center, etc, but to formulate in this setting the criteria for an object to be an ideal or normal subobject, it is useful to make the assumption that the theory of $\mathcal{C}$ can be presented by a set of operations and identities satisfying some extra conditions, most of which are versions of obvious ones from 'algebra'.


##Definition

(Revision in progress)

By a *group-based universal algebra*, we will mean an algebra for a theory, in the classical sense, which contains

* a unique constant, denoted $0$;
* a set, $\Omega$ of finitary operations;

and

* a set, $\mathbb{E}$, of idenities or equations,

which are to satisfy

* $\Omega=\Omega_0\cup \Omega_1\cup \Omega_2$ where $\Omega_i$ is the set of $i$-ary operations;

* $\Omega_0=\{0\}$; $\Omega_1$ contains an operation $-$, $\Omega_2$ contains an operation $+$, (but $+$ is not assumed to be commutative) and $\mathbb{E}$ contains the group laws for $0,-,+$.

We define $\Omega^\prime_i$ to be the set of 'extra' specified operations, so $\Omega^\prime_0 = \Omega_0\setminus \{0\}$, and so on.


We have the following conditions on the equations/identities:

* for any $*\in \Omega^\prime_2$, $\Omega^\prime_2$  also contains $\ast^{op}$, where $x\ast^{op}y= y\ast x$;
* for any $\omega \in \Omega^\prime_1$, $\mathbb{E}$ includes the identity $\omega(x+y)=\omega(x)+ \omega(y)$;
* for any $\ast \in \Omega^\prime_2$, $\mathbb{E}$ includes the distributive law: $x\ast (y+z)= x\ast y+x\ast z$;
* for any $\omega \in \Omega^\prime_1$ and $\ast \in \Omega^\prime_2$, $\mathbb{E}$ includes the identity $\omega(x)\ast y = \omega(x\ast y)$;
* for any $\ast \in \Omega^\prime_2$, $\mathbb{E}$ includes the identity $x+(y\ast z)=(y\ast z)+x$;
* for any $\ast, \circ \in \Omega^\prime_2$, there is a word $W$ such that $\mathbb{E}$ includes the identity:
$(x*y)\circ z = W(x\ast_1(y\circ_1 z),\ldots, x\ast_m(y\circ_m z), y\ast_{m+1}(x\circ_{m+1} z),\ldots, y\ast_{n}(x\circ_{n} z)$, where $\ast_1\ldots,\ast_n$ and $\circ_1,\ldots,  \circ_n$ are operations in $\Omega^\prime_2$.

## Properties


Any category of group-based universal algebras is a variety of $\Omega$-groups (in the sense of Higgins) and so is automatically a [[semi-abelian category]]. This provides a useful set of fairly concrete examples for study in the semi-abelian /  proto-modular context. In fact, they are [[protomodular category|strongly protomodular]], (and hence [[strongly semi-abelian]]). This means that in such categories you can deal with internal [[actions]] in more or less the same way as you do in the category of groups.


Moreover categories of group-based universal algebras are action accessible in the sense of Bourn-Janelidze, meaning that actions are not so far from being representable, allowing a Schreier-MacLane-like obstruction theory for the classification of extensions.


##Related entries

* [[Omega-group]]

* [[semi-abelian category]]

* [[protomodular category]]

* [[variety of algebras]]

##References

The original idea is in 

* Grace Orzech, _Obstruction theory in algebraic categories I, II_, J. Pure Appl. Algebra __2__ (1972) 287-340, 315 - 340. 

The point about actions is in 

* [[G. Metere]], _A note on strong protomodularity, actions and quotients,_ Journal of Pure and Applied Algebra, 221 (2017) 75 - 88.

[[!redirects category of interest]]
