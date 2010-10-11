
# Contents
* automatic table of contents goes here
{:toc}

##Transition systems.##
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

The notions of transition system and of morphisms between them is clearly related to (low dimensional) cubical sets / labelled directed graphs,/labelled transition systems, but we will need to consider labelled  cubical sets.


##Labeled transition systems.##

In the above, we have used the notation $L$ to stand for the set of _events_ and the set of _labels_ for those events. It is sometimes useful to make a distinction between the events themselves and their labels and to explicitly give a labelling as a function.  This is important, for instance, in treating 'relabelling' which leads to [[fibration|fibrational situations]] (see the paper by Winskel and Nielsen, cited below.) In order to make the distinction clearer, we will replace $L$ by $E$ and refer to its elements as 'events' in what follows.

+--{: . un-definition}
##Definition##

 A _labeled transition system_ consists of a transition 
system $T = (S, i, E, Tran)$ together with a set $L$ of _labels_, a function $l : E \to L$.  We denote it by $(T,L,l)$.
 
A _morphism_, $(\sigma, \tau , \lambda) : (T_1 , L_1 , l_1) \to (T_2 , L_2 , l_2 )$ between labeled transition 
systems consists of a morphism $(\sigma, \tau) : T_1 \to T_2$ between the underlying transition 
systems together with a [[partial function]] $\lambda : L_1 \to L_2$ such that $l_2 \circ \tau = \lambda \circ l_1$. 
=--
We 
write $LTS$ for the category of labeled transition systems.


##References##


* G. Winskel and M. Nielsen, Models for concurrency. vol. 3, Handbook of Logic in Computer Science, pages 100 - 200, Oxford Univ. Press, 1994. (see also [online technical report](http://www.daimi.au.dk/PB/463/PB-463.pdf)).

*   [[Eric Goubault]] and [[Samuel Mimram]], [Formal Relationships Between Geometrical and Classical Models for Concurrency](http://fr.arxiv.org/abs/1004.2818)