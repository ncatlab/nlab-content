Transition systems are a well established semantic model for both sequential and concurrent systems.
+--{: . un-definition}
##Definition##
A _transition system_ is a structure $T = (S,i,L,Trans)$, where

* $S$ is a set of _states_ with initial state, $i$;

* $L$ is a set of _labels_;

* $Tran\subseteq S\times L\times S$ is the _transition relation_.

=--

Let $(S, i, L, Tran )$ be a transition system. We write 

$$s\stackrel{a}{\to} s'$$ 
 
to indicate that $(s, a, s')\in Tran$. 

+--{: . un-definition}
##Definition##
 A _morphism_ from one transition system $T$ to another 
$T'$ 