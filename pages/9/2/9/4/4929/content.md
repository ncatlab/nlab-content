Transition systems are a well established semantic model for both sequential and concurrent systems.
+--{: . un-definition}
##Definition##
A _transition system_ is a structure $(S,i,L,Trans)$, where

* $S$ is a set of _states_ with initial state, $i$;

* $L$ is a set of _labels_;

* $Tran\subseteq S\times L\times S$ is the _transition relation_.

=--
Let $(S, i, L, Tran )$ be a transition system. We write 

$$s\stackrel{a}{\to} s^\prime$$ 
 
to indicate that $(s, a, s^\prime)\in Tran$. It is convenient to introduce idle transitions associated with any state.  This has to do with the representation of partial functions, in the usual way.  We can view a partial function from a set $L$ to a set $L^'$ as a (total) function from $l$ to $L'\cup \{*\}$, by sending all the elements of $L$ on which $\lambda$ is not defined to the new element $*$.  (Of course, this presupposes that we have reserved $*$ for this purpose and that it does not occur in any of the other sets that may occur here.) 