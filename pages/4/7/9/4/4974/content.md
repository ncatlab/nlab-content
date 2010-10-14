# Contents
* automatic table of contents goes here
{:toc}

##Idea##

Event structures wee introduced i order to abstract away from the precise 'places' and times at which events occur in distributed systems. The structre focuses on the events and the causal ordering between them.

+--{: .un-definition}
##Definition##
An _event structure_, $(E,\le, \sharp)$, consists of a [[poset]] $(E,\le)$ of _events_, where the partial order relation expresses _causal dependency_, together with a symmetric irreflexive relation $\sharp$, called _incompatibility_  .  This data is to satisfy

*  finite causes: for every event $e$ the set $\downarrow e = \{e'\mid e'\le e\}$ is finite; 

and

* _hereditary incompatibility_: for any $e,e',e'' \in E$, $e\sharp e'$ and $e'\le e''$ implies $e\sharp e''$.
=--
A morphism between two event structures 
An _event structure_, $(E,\le, \sharp)$ and 
An _event structure_, $(E',\le', \sharp')$ consists of a partial function $f : E\to E'$ such that is $f(e)$ is defined then $\downarrowf(e)\subseteq f(\downarrow e)$




##References##

