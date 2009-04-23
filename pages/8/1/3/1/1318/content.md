{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
+-- {: goal}
###### Lexicon entry on
##simplicial local systems

* NB. There is an entry at [[local system|local systems]] together with a blog link to David Speyer: _Three ways of looking at a local system_

  * [Introduction and connection to cohomology theories](http://sbseminar.wordpress.com/2009/04/20/three-ways-of-looking-at-a-local-system-introduction-and-connection-to-cohomology-theories/)



Here we will concentrate on the combinatorial and simplicial version of local systems.


(The previous entry in this lexicon can be found at [[differential forms on simplices]].) 
=--
##Local Systems in a simplicial context

By the category of **$n$-graded spaces**, we mean the category whose objects are the $n$-graded vector spaces

$$V = \sum_{p_1,\ldots,p_n\geq0}V^{p_1,\ldots,p_n}$$

and whose morphisms are the linear maps, homogeneous of multidegree zero.

The category of $n$-graded differential vector spaces has  for objects pairs $(V,d)$, where $V$ is an $n$-graded vector space, $d$ is a linear map of _total_ degree 1, and $d^2 = 0$.  The morphisms are the linear maps, homogeneous of multidegree zero, which commute with $d$.

We will denote by $\mathcal{C}$ one of the following categories:

* $n$-graded vector spaces.

* The category of $n$-graded algebras,

*  The subcategory of commutative $n$-graded algebras,

* $n$-graded differential vector spaces,

*  The subcategory of $n$-graded differential algebras,

*  The subcategory of  commutative $n$-graded differential algebras.



In the 'differential' examples, the differential will usually be denoted $d$.  Almost always we will be restricting ourselves to the case $n = 1$.  Extensions of any results or definitions to the general case are usually routine.


Let $K$ be a simplicial set.  A **local system** $F$ on $K$ with values in $\mathcal{C}$ is:


1. a family of objects $F_\sigma =\sum_{p\geq 0} F^p_\sigma$ in $\mathcal{C}$ indexed by the simplices $\sigma$ of $K$;

1. a family of morphism (called the _face_ and _degeneracy_ operators) 

$$d_i :F_\sigma \to F_{d_i\sigma} \quad and\quad s_i : F_\sigma \to F_{s_i\sigma}$$ 

satisfying the simplicial identities.

###Remark###

There is an obvious way of assigning a small category to a simplicial set in which the simplices are the objects and the face and degeneracy maps generate the morphisms.  A local system is then just a functor from that category to $\mathcal{C}$.

###Back to discussion###

Let $\varphi : L \to K$ be a simplicial map and $F$ a local system over $K$.  The _pullback_ of $F$ to $L$ (or along $\varphi$) is the local system $\varphi^*F$ over $L$ given by 

$$(\varphi^*F)_\sigma = F_{\varphi\sigma} ; \quad d_i = d_i ; \quad s_i = s_i.$$

If $\varphi$ is an inclusion of a simplicial subset then we may say that $\varphi^*F$ is the _restriction_ of $F$ to $L$.


Now let $F$ be a local system on $K$ with values in $\mathcal{C}$.  Define a graded space $F(K)$ as follows : an element $\Phi$ of  $F^p(K)$ is a function which assigns to each simplex $\sigma$ of $K$ an element $\Phi_\sigma \in F^p_\sigma$ such that for all $\sigma$


$$\Phi_{d_i\sigma} = d_i(\Phi_\sigma) \quad  and  \quad \Phi_{s_i\sigma}  = s_i(\Phi_\sigma).$$

The linear structure is the obvious one, defined 'componentwise' and if $\mathcal{C}$ is one of the algebra (resp. differential) variants of the generic receiving category then the multiplication (resp. the differential) is defined componentwise as well. In this way $F(K)$ becomes an object of $\mathcal{C}$, called the **object of global sections** of $F$.


[[Tim Porter|Tim]]: This construction also has (I think) a neat categorical description, that will be worth investigating.  It would seem to be the analogue of the Grothendieck construction / homotopy colimit (at least partially) in this context. (enlightenment sought!!!)


If $\varphi : L \to K$ is a simplicial map, it determines a morphism $F(\varphi) : (\varphi^*F)(L)\to F(K)$ given by 

$$(F(\varphi)\Phi)_\sigma = \Phi_{\varphi\sigma}.$$

If $\varphi$ is an inclusion of $L$ into $K$, then we denote $(\varphi^*F)(L)$ simply by $F(L)$ and call the morphism $F(K)\to F(L)$ _restriction_.

Now suppose $F$ is a local system over $K$.  Assume $M_n \subset K_n$ are subsets ($n \geq 0$) such that $d_i : M_n \to M_{n-1}$  This family $\{M_n\}$ generates a subsimplicial set $L\subset K$ and if $s_i\sigma \in M_{n+1}$ then $\sigma = d_i s_i\sigma \in M_n$.


