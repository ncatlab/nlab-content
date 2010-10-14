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

Let $(E,\le, \sharp)$ be an event structure. Define its set of _configurations_, 
$D(E,\le, \sharp)$, to consist of those subsets $X \subseteq E$, which are 
 
* conflict-free: if $e, e'\in X$ then $\neg (e\sharp e')$,

and 

*  downward closed:  if $e\in X$, $\downarrow e\subseteq X$.
=--