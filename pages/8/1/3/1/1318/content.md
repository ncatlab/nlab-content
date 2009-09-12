<div class="rightHandSide toc">
[[!include differential graded objects - contents]]
</div>


##Simplicial local systems

* NB. There is an entry at [[local system|local systems]] together with a blog link to David Speyer: _Three ways of looking at a local system_

  * [Introduction and connection to cohomology theories](http://sbseminar.wordpress.com/2009/04/20/three-ways-of-looking-at-a-local-system-introduction-and-connection-to-cohomology-theories/)

Here we will concentrate on the combinatorial and simplicial version of local systems.



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


+-- {: .query}

[[Urs Schreiber|Urs]]: How does the $n$-grading affect the nature of the following definition? It seems that chain homotopies are not used in the following, just the 1-categorical structure?

=--


In the 'differential' examples, the differential will usually be denoted $d$.  Almost always we will be restricting ourselves to the case $n = 1$.  Extensions of any results or definitions to the general case are usually routine.


Let $K$ be a simplicial set.  A **local system** $F$ on $K$ with values in $\mathcal{C}$ is:


1. a family of objects $F_\sigma =\sum_{p\geq 0} F^p_\sigma$ in $\mathcal{C}$ indexed by the simplices $\sigma$ of $K$;

1. a family of morphism (called the _face_ and _degeneracy_ operators) 

$$d_i :F_\sigma \to F_{d_i\sigma} \quad and\quad s_i : F_\sigma \to F_{s_i\sigma}$$ 

satisfying the simplicial identities.

###Remarks###

* Here we will often just refer to 'local system' rather than the fuller 'simplicial local system', if no confusion will be likely to result.

*  There is an obvious way of assigning a small category to a simplicial set in which the simplices are the objects and the face and degeneracy maps generate the morphisms:

regarding the [[simplicial set]] as a [[functor]] 

$$
  K : \Delta^{op} \to Set
$$

on the [[simplex category]], its category of cells is the [[comma category]]

$$
  (Y, const_K) =
  \left\{
    \array{
       Y(\Delta^n) &&\stackrel{}{\to}&& Y(\Delta^{n'})
       \\
       & {}_c\searrow && \swarrow_{c'}
       \\
       && K
    }
  \right\}
$$

where $Y : \Delta \to [\Delta^{op}, Set]$ is the [[Yoneda embedding]] for which $Y(\Delta^n)$ is the standard simplicial $n$-[[simplex]], so that $c : Y(\Delta^n) \to K$ is an $n$-simplex $c \in K_n$ of the simplicial set $n$.


A simplicial local system is then just a functor 

$$
  F : (Y,const_K) \to \mathcal{C}
$$

from that category to $\mathcal{C}$.

+-- {: .query}

[[Urs Schreiber|Urs]]: Here it says "a local system". I suppose "simplicial local system" is meant? We should have a discussion about how this notion of simplicial local system relates to the functors from fundamental groupoids discussed at [[local system]].

[[Tim Porter|Tim]]: That has been amended! Halperin just calls them 'local systems', so in the notes that were the basis for this so did I. I copied and pasted from them, so this slip may occur elsewhere as well.

=--


###Back to discussion###

Let $\varphi : L \to K$ be a simplicial map and $F$ a local system over $K$.  The _pullback_ of $F$ to $L$ (or along $\varphi$) is the local system $\varphi^*F$ over $L$ given by 

$$(\varphi^*F)_\sigma = F_{\varphi\sigma} ; \quad d_i = d_i ; \quad s_i = s_i.$$

If $\varphi$ is an inclusion of a simplicial subset then we may say that $\varphi^*F$ is the _restriction_ of $F$ to $L$.


Now let $F$ be a local system on $K$ with values in $\mathcal{C}$.  Define a graded space $F(K)$ as follows : an element $\Phi$ of  $F^p(K)$ is a function which assigns to each simplex $\sigma$ of $K$ an element $\Phi_\sigma \in F^p_\sigma$ such that for all $\sigma$


$$\Phi_{d_i\sigma} = d_i(\Phi_\sigma) \quad  and  \quad \Phi_{s_i\sigma}  = s_i(\Phi_\sigma).$$


+-- {: .query}

[[Urs Schreiber|Urs]]: Do I understand correctly that when the simplicial local system is expressed as a functor, then $F(K)$ is the space of natural transformations from the simplicial local system constant on the [[generator]] (if any) of $\mathcal{C}$ (for instance the tensor unit if $\mathcal{C}$ is graded vector spaces).

For ordinary [[local system]]s this gives the flat sections. 

[[Tim Porter|Tim]]: I'm not sure.

=--


The linear structure is the obvious one, defined 'componentwise' and if $\mathcal{C}$ is one of the algebra (resp. differential) variants of the generic receiving category then the multiplication (resp. the differential) is defined componentwise as well. In this way $F(K)$ becomes an object of $\mathcal{C}$, called the **object of global sections** of $F$.

+-- {: .query}
[[Tim Porter|Tim]]: This construction also has (I think) a neat categorical description, that will be worth investigating.  It would seem to be the analogue of the Grothendieck construction / homotopy colimit (at least partially) in this context. (enlightenment sought!!!)
=--

If $\varphi : L \to K$ is a simplicial map, it determines a morphism $F(\varphi) : (\varphi^*F)(L)\to F(K)$ given by 

$$(F(\varphi)\Phi)_\sigma = \Phi_{\varphi\sigma}.$$

If $\varphi$ is an inclusion of $L$ into $K$, then we denote $(\varphi^*F)(L)$ simply by $F(L)$ and call the morphism $F(K)\to F(L)$ _restriction_.

Now suppose $F$ is a local system over $K$.  Assume $M_n \subset K_n$ are subsets ($n \geq 0$) such that $d_i : M_n \to M_{n-1}$  This family $\{M_n\}$ generates a subsimplicial set $L\subset K$ and if $s_i\sigma \in M_{n+1}$ then $\sigma = d_i s_i\sigma \in M_n$.



+-- {: .query}

[[Urs Schreiber|Urs]]: So what are simplicial local systems used for? Is there a good motivating example? Relating it to the other definition of [[local system]], maybe?

[[Tim Porter|Tim]]: Aha! All will be revealed in the next entry 'Differential forms on a simplicial set' ... when I get to putting it in!  There is some more to go here as well, describing special properties, but it was getting late last night. 

=--
+-- {: .un_lemma }
###### Lemma 

Suppose $\Phi_\sigma \in F^p_\sigma$ ( $\sigma \in M_n$), $n \geq 0$, satisfy $\Phi_{d_i\sigma} = d_i\Phi_\sigma$ and $\Phi_{s_i\sigma} = s_i\Phi_\sigma$ (this is with $s_i\sigma\in M_n$, and $n\geq 0$). Then there is a unique element $\Phi\in F^p(L)$ extending $\Phi_\sigma$.
=--

The proof is by induction and can be found in Halperin's notes if required.

For any simplicial set $K$, any $n$-simplex $\sigma \in K_n$ determines a unique simplicial map, which we will also write as $\sigma$ from $\Delta[n]$ to $K$ that sends the unique non-degenerate $n$-simplex of the standard $n$-simplex $\Delta[n]$ to the element $\sigma$. In particular, if $F$ is a local system over $K$, then we can form $\sigma^*F$ over $\Delta[n]$. We will say that $F$ is _extendable_ if for each $\sigma$ the restriction 

$$\sigma^*(F)(\Delta[n]) \to \sigma^*(F)(\partial\Delta[n])$$

is surjective, where $\partial\Delta[n]$ is the boundary of the $n$-simplex.

+-- {: .un_prop }
######Proposition

Suppose $\varphi :L \to K$ is a simplicial map and $F$ is an extendable system over $K$, then $\varphi^*F$ is an extendable local system over $L$.

=--
The proof is easy.

+-- {: .un_prop }
######Proposition
Suppose that $L\subset K$ is a subsimplicial set and $F$ is an extendable local system over $K$.  Then the restriction morphism $F(K)\to F(L)$ is surjective.
=--
The proof is again by induction up the skeleta of $K$ and $L$, for details see Halperin, p.XII 10.


If $F$ is an extendable local system over $K$ and $L\subset K$, we denote the kernel of $F(K)\to F(L)$ by $F(K,L)$ and call it the *space of relative global sections*. (A description of $F(K,L)$ is given in detail in Halperin, p.XII-12.)

It may be useful to have some more of the terminology of local systems available.  A local system $F$ over $K$ is **constant**  if for some $F_0 \in \mathcal{C}$, each $F_\sigma = F_0$ and each $d_i$ and $s_j$ is the identity map on $F_0$. We say $F$ is **constant by dimension** if for some sequence $F_n\in \mathcal{C}$ ($n \geq 0$), $F_\sigma = F_n$, for $\sigma \in K_n$ and $d_i$, $s_j$ depend only on $\dim \sigma$.

 A local system $F$ over $K$ is a **local system of coefficients** if for each $\sigma$ and each $i$, 

$$d_i : F_\sigma \to F_{d_i\sigma} \quad  and s_i : F_\sigma \to F_{s_i \sigma}$$

are isomorphisms.  Finally $F$ is a **local system of differential coefficients** if $\mathcal{C}$ is one of the categories with differentials above, and for each $\sigma$, and $i$

$$d_i^* : H(F_\sigma) \to H(F_{d_i\sigma}) \quad  and  s_i^* : H(F_\sigma) \to H(F_{s_i\sigma})$$

 are isomorphisms, in other words if the corresponding cohomology is a local system of coefficients.


+-- {: .un_theorem }
######Theorem

Let $F$ and $G$ be extendable local systems of differential coefficients over $K$.  Assume we are given morphisms

$$\varphi_\sigma : F_\sigma \to G_\sigma, \quad \sigma \in K,$$ 

compatible with the face and degeneracy operators.  Then  a morphism $\varphi : F(K)\to G(K)$ is given by $(\varphi\Phi)\sigma = \varphi_\sigma (\Phi_\sigma)$, and 

$$\varphi^* : H(F(K))\to H(G(K))$$

is an isomorphism.
=--