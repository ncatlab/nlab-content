Given a [[set]] $S$, the __power set__ of $S$ is the set $\mathcal{P}S$ of all [[subset]]s of $S$.  Equivalently, it is the set $\TV^S$ of all [[function]]s from $S$ to the set $\TV$ of [[truth value]]s.  This is often written $2^S$, since there are (at least in [[classical logic]]) exactly $2$ truth values.

One generally needs a specific axiom in the [[foundations]] of mathematics to ensure the existence of power sets.  In [[predicative mathematics]] the existence of power sets (along with other "impredicative" axioms) is not accepted.  One can use power sets to construct [[function set]]s; the converse also works using [[excluded middle]] (or anything else that will guarantee the existence of the set of truth values).  In particular, power sets exist in any theory containing excluded middle and function sets; thus predicative theories which include function sets must also be [[constructive mathematics|constructive]].

The power set $\mathcal{P}S$ is in fact a [[partial order|poset]] ordered by containment: $A$ precedes $B$ means that $A$ is a [[subset]] of $B$ ($A \subseteq B$).

Power sets live in the category [[Set]].  Given an object $S$ of any [[category]], one can similarly form a poset of [[subobject]]s of $S$; the category is called [[well-powered category|well-powered]] when this poset is [[small category|small]].  One also has an internal notion of power set (a [[power object]]) in a [[topos]].

category: foundational axiom