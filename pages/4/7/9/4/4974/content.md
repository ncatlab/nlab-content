# Contents
* automatic table of contents goes here
{:toc}

##Idea##

Event structures were introduced i order to abstract away from the precise 'places' and times at which events occur in distributed systems. The structre focuses on the events and the causal ordering between them.
+--{: . un-definition}
##Definition##
An _event structure_, $(E,\le, \sharp)$, consists of a [[poset]] $(E,\le)$ of _events_, where the partial order relation expresses _causal dependency_, together with a symmetric irreflexive relation $\sharp$, called _incompatibility_  .  This data is to satisfy

*  finite causes: for every event $e$ the set $\downarrow e = \{e'\mid e'\le e\}$ is finite; 

and

* _hereditary incompatibility_: for any $e,e',e'' \in E$, $e\sharp e'$ and $e'\le e''$ implies $e\sharp e''$.
=--

+--{: . un-definition}
##Definition## 

Let $\mathbb{E} = (E,\le, \sharp)$ be an event structure. Define its set of _configurations_, 
$D(\mathbb{E}) = D(E,\le, \sharp)$, to consist of those subsets $X \subseteq E$, which are 
 
* conflict-free: if $e, e'\in X$ then $\neg (e\sharp e')$,

and 

*  downward closed:  if $e\in X$, $\downarrow e\subseteq X$.
=--

A morphism $f : \mathbb{E}\to \mathbb{E}'$ of event structures consists of a [[partial function]] $f : E \to  E'$ such that 

* if 
$X\in D(\mathbb{E})$, then $f(X) \in D(\mathbb{E}')$

and 

*  if $e_0$ and $e_1$ are in $X$ with both $f(e_0)$ and $f(e_1)$ defined and  $f(e_0)=f(e_1)$ then $e_0 = e_1$. 



####Gloss####
This second condition says that if both $f(e_0)$ and $f(e_1)$ are defined and either $f(e_0)\sharp' f(e_1)$ or $f(e_0)=f(e_1)$, then either $e_0\sharp e_1$, or $e_0 = e_1$. 


Winskel and Neilsen explain the definition as follows: 

A morphism $f : \mathbb{E}\to \mathbb{E}'$ between event structures expresses how behaviour in $\mathbb{E}$ determines behaviour in $\mathbb{E}'$. The partial function, $f$, expresses how the occurrence of an event in $\mathbb{E}$ implies the simultaneous occurrence of an event in $\mathbb{E}'$; the fact that $f(e) = e'$ can be understood as expressing that the event $e$ is a ''component'' of the event $e'$ and, in this sense, that the occurrence of $e$ implies the simultaneous occurrence of $e'$. If two distinct events in $\mathbb{E}$ have the same image in $\mathbb{E}'$ under $f$ then they cannot belong to the same configuration. 

(There is more discussion of the notion of morphism of event structures in the notes referred to  below.)


With this definition of morphism, we get the category, $\mathbf{ES}$ of event structures.

##References##

* G. Winskel and M. Nielsen, Models for concurrency. vol. 3, Handbook of Logic in Computer Science, pages 100 - 200, Oxford Univ. Press, 1994. (see also [online technical report](http://www.daimi.au.dk/PB/463/PB-463.pdf)).

