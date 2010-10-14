# Contents
* automatic table of contents goes here
{:toc}

##Idea##

Event structures were introduced in order to abstract away from the precise 'places' and times at which events occur in distributed systems. The structure focuses on the events and the causal ordering between them.


##Original form##

+--{: . un-definition}
##Definition##
An _event structure_, $(E,\le, \sharp)$, consists of a [[poset]] $(E,\le)$ of _events_, where the partial order relation expresses _causal dependency_, together with a symmetric irreflexive relation $\sharp$, called _incompatibility_  .  This data is to satisfy

*  finite causes: for every event $e$ the set $\downarrow e = \{e'\mid e'\le e\}$ is finite; 

and

* _hereditary incompatibility_: for any $e,e',e'' \in E$, $e\sharp e'$ and $e'\le e''$ implies $e\sharp e''$.
=--

+--{: . un-definition}
##Definition## 

Let $\mathbb{E} = (E,\le, \sharp)$ be an event structure. Define its set of **configurations**, 
$C(\mathbb{E}) = C(E,\le, \sharp)$, to consist of those subsets $X \subseteq E$, which are 
 
* conflict-free: if $e, e'\in X$ then $\neg (e\sharp e')$,

and 

*  downward closed:  if $e\in X$, $\downarrow e\subseteq X$.
=--

A morphism $f : \mathbb{E}\to \mathbb{E}'$ of event structures consists of a [[partial function]] $f : E \to  E'$ such that 

* if 
$X\in C(\mathbb{E})$, then $f(X) \in C(\mathbb{E}')$

and 

*  if $e_0$ and $e_1$ are in $X$ with both $f(e_0)$ and $f(e_1)$ defined and  $f(e_0)=f(e_1)$ then $e_0 = e_1$. 



####Gloss####
This second condition says that if both $f(e_0)$ and $f(e_1)$ are defined and either $f(e_0)\sharp' f(e_1)$ or $f(e_0)=f(e_1)$, then either $e_0\sharp e_1$, or $e_0 = e_1$. 


Winskel and Neilsen explain the definition as follows: 

A morphism $f : \mathbb{E}\to \mathbb{E}'$ between event structures expresses how behaviour in $\mathbb{E}$ determines behaviour in $\mathbb{E}'$. The partial function, $f$, expresses how the occurrence of an event in $\mathbb{E}$ implies the simultaneous occurrence of an event in $\mathbb{E}'$; the fact that $f(e) = e'$ can be understood as expressing that the event $e$ is a ''component'' of the event $e'$ and, in this sense, that the occurrence of $e$ implies the simultaneous occurrence of $e'$. If two distinct events in $\mathbb{E}$ have the same image in $\mathbb{E}'$ under $f$ then they cannot belong to the same configuration. 

(There is more discussion of the notion of morphism of event structures in the notes referred to  below.)


With this definition of morphism, we get the category, $\mathbf{ES}$ of event structures.

##Alternative form##

In some sources, rather than stress the _inconsistency relation_, the complementary _consistency relation_.  This leads to the definition of a family, $Con$, of finite subsets of $E$, which satisfy


* $\{e\}\in E$ for all $e\in E$;

* $Y\subseteq X\in Con$ implies $Y\in Con$,

and 

* $X\in Con$ and $e\leq e'\in X$ then $X\cup \{e\}\in Con$.


##References##

* [[G. Winskel]] and M. Nielsen, Models for concurrency. vol. 3, Handbook of Logic in Computer Science, pages 100 - 200, Oxford Univ. Press, 1994. (see also [online technical report](http://www.daimi.au.dk/PB/463/PB-463.pdf)).

* [[G. Winskel]], _Events, causality, and symmetry_, (an earlier version appeared in the BCS conference 'Visions in Computer Science.' September 2008. The final version appears in a special issue of The Computer Journal 2009; doi: 10.1093/comjnl/bxp052; see also  an [online version](http://www.cl.cam.ac.uk/~gw104/CJVision-Revised.pdf)).

* [[G. Winskel]] and S. Staton, On the expressivity of symmetry in event structures,
[LICS 2010](http://www.cl.cam.ac.uk/~gw104/lics2010final.pdf)