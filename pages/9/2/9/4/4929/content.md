Transition systems are a well established semantic model for both sequential and concurrent systems.
+--{: . un-definition}
##Definition##
A _transition system_ is a structure $T = (S,i,L,Trans)$, where

* $S$ is a set of _states_ with initial state, $i$;

* $L$ is a set of _labels_, sometimes referred to also as _events_;

* $Tran\subseteq S\times L\times S$ is the _transition relation_.

=--

Let $(S, i, L, Tran )$ be a transition system. We write 

$$s\stackrel{a}{\to} s'$$ 
 
to indicate that $(s, a, s')\in Tran$. 

+--{: . un-definition}
##Definition##
 A _morphism_ from one transition system, $T$, to another 
$T'$  will be a pair $(\sigma, \lambda)$, in which 

* $\sigma$ is a function from the states of $T$ to those of $T'$ 
 
* $\lambda$ is a [[partial function]] from the labels of $T$ to those of $T'$ such that for any transition $s\stackrel{a}{\to} s'$ of $T$ if $\lambda(a)$ is defined, then $\sigma(s)\stackrel{\lambda(a)}{\to} \sigma(s')$ is a 
transition of $T'$; otherwise, if $\lambda(a)$ is undefined, then $\sigma(s) = \sigma(s')$. 
=--

It is useful to rework this definition of morphism using a variant of the idea, discussed at [[partial function]], that replaces a partial function by a total function using the neat trick of adding an additional element $\bot$ to the codomain. (We will use the notation from [[partial function]] freely in what follows.)   This is done here simply by introducing **idle transitions** $(s,\bot,s)$ thought of as going from $s$ to itself, and working with $L_\bot$ as a set of labels instead of  $L$.  (This is very neat here as it corresponds the label $\bot$ to 'do nothing' to the states.)  After completing everything in this way we get new transition systems $T_\bot = (S,i,L_\bot, Tran_\bot)$, etc. and will work with these. (Of course, $Tran_\bot = Tran \cup \{s,\bot,s)\mid s\in S\}$.)  Now a morphism $f$ is the same as given by a pair $\sigma: S\to S'$, as before, and $\lambda: L_\bot\to L'_\bot$, satisfying the compatibility condition that if $(s,a,s')\in Tran_\bot$, then $(\sigma(s),\lambda(a),\sigma(s'))\in Tran'_\bot$, (and that $\lambda_\bot(\bot) = \bot'$).

This way we get a category, $TS$, of transition systems.

+--{: .query}
[[Tim Porter|Tim]]: In [[partial function]] there is a description of partial functions as spans. I think I have seen a source which uses spans to define a mild generalisation of morphisms for transition systems, but I cannot remember where (and whether it was worth it).  

=--

The notions of transition system and of morphisms between them is clearly related to (low dimensional) cubical sets / labelled directed graphs, but we need to consider labelled  cubical sets.



##References##


* G. Winskel and M. Nielsen, Models for concurrency. vol. 3, Handbook of Logic in Computer Science, pages 100 - 200, Oxford Univ. Press, 1994. (see also [online technical report](http://www.daimi.au.dk/PB/463/PB-463.pdf)).