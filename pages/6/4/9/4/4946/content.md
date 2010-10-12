Asynchronous automata are a generalisation of both [[transition systems]] and [[Mazurkiewicz traces]]. Their study has influences  other models for concurrency such as _transition systems with independence_ (also called _asynchronous transition systems_).  The idea is to decorate transition systems with an independence relation (much as in [[Mazurkiewicz trace alphabet]]s) between actions that allow one to distinguish true concurrency from mutual exclusion (i.e. _non-determinism_).  Following the paper by Goubault and Mimram, we use a slight modification called _automata with concurrency relations_:
+--{: . un-definition}
##Definition##
An _automaton with concurrency relations_  $(S,i,E,Tran,I)$ consists of 

* a [[transition system]] $(S,i,E,Tran)$, such that whenever $(s,a,s')$, and $(s,a,s'')$ are in $Tran$, then $s' = s''$;

and

* $I = \{I_s\mid s\in S\}$ is a family of irreflexive, symmetric binary relations, $I_s$ on $E$ such that whenever $a_1I_s a_2$ (with $a_1,a_2 \in E$), there exist transitions $(s,a_1,s_1)$, $(s,a_2,s_2)$, $(s_1,a_2,r)$, and $(s_2,a_1,r)$ in $Tran$.
=--

##References##


*   [[Eric Goubault]] and [[Samuel Mimram]], [Formal Relationships Between Geometrical and Classical Models for Concurrency](http://fr.arxiv.org/abs/1004.2818)