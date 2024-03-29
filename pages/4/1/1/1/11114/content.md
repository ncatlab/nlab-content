
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

So-called _Trimble rewiring_ refers to a certain type of transformation on [[graphs]] which were introduced in [Trimble's thesis](#TT94), intended to refine [[Kelly-Mac Lane graphs]] or classical [[proof nets]] in multiplicative [[linear logic]] so as to capture properties of the [[monoidal category|monoidal unit]] in [[symmetric monoidal category|symmetric]] [[closed monoidal categories]]. These unit-extended proof nets may be interpreted as morphisms in [[free construction|free]] [[symmetric monoidal category|symmetric monoidal]] [[closed category|closed categories]], and it turns out that two unit-extended proof nets are interpretable as the same morphism if and only if they are "rewiring equivalent". 

Rewirings can be organized into a confluent and strongly normalizing rewrite system, where a rewrite called "directed rewiring". The normal forms of graphs can then be used to state a full coherence theorem, extending the [[coherence theorem]] of [Kelly and Mac Lane](#KM71) for symmetric monoidal closed categories. 

The concept of rewiring equivalence extends to [[weakly distributive category|weakly distributive categories]] and $\ast$-[[star-autonomous category|autonomous]] categories as well, and likewise is used to give [coherence theorems](#BCST96) for these structures. 

## Definition 

(For now this is just the very rough idea. More details to come.) 

Recall from [[proof net]] the notion of (cut-free) proof structure and the notion of (cut-free) proof net (a proof structure of the form $S(\pi)$ where $\pi$ is a sequent proof). 

+-- {: .num_defn} 
###### Definition 
A _unit-extended proof structure_ of type $\Delta \to B$ is a proof structure of type $\Delta \to B$ equipped with a function $u: Unit^-(\Delta^-, B^+) \to Subform(\Delta^-, B^+)$ from the set of negatively signed subformula occurrences of $I$ to the set of subformulas of $\Delta$ and $B$. 
=-- 

We draw such a unit-extended proof structure as a graph: the graph of the proof
structure together with an edge from each occurrence $R$ of $I^-$ to $u(R)$. We think of this unit edge as connoting a subterm of the form $r t$, where $r$ is a variable term of type $I$ (a "scalar"), and $t$ is a term of type $u(R)$. 

Let $UStruct(\Delta, B)$ denote the set of unit-extended proof structures of type $\Delta \to B$, and let $Proof(\Delta, B)$ denote the set of sequent proofs of the sequent $\Delta \vdash B$. We define a relation from $Proof(\Delta, B)$ to $UStruct(\Delta, B)$, i.e., a function 

$$Proof(\Delta, B) \to P(UStruct(\Delta, B))$$ 

by induction along the sequent proof, as follows. (Details to be filled in. The most important sequent rule to consider is 

$$\Gamma(\frac{\displaystyle \pi: \Delta, \Sigma \vdash A}{\displaystyle \Delta, I, \Sigma \vdash A}\; unit_{-})$$ 

where a related unit-extended proof net is obtained from a proof net for $\pi$ by introducing a fresh unit edge from the occurrence of $I^-$ introduced in the last step to any subformula of $\Delta, \Sigma \vdash A$. The other rules are straightforward.) 

+-- {: .num_defn} 
###### Definition 
A _unit-extended proof net_ is a proof structure that is related to some sequent deduction. 
=-- 

Theorem on graphical criterion for a unit-extended proof structure to be a unit-extended proof net, similar to the criterion of Danos-Regnier. 

+-- {: .num_defn} 
###### Definition 
Two unit-extended proof nets $\gamma, \gamma'$ of type $\Delta \to B$ are _rewiring-equivalent_ if there is a sequence of unit-extended proof nets $\gamma = \gamma_0, \gamma_1, \ldots, \gamma_n = \gamma'$ of type $\Delta \to B$ such that each successive pair of graphs $\gamma_i, \gamma_{i+1}$ differ only by a single unit edge $u(R)$. 
=-- 

Theorem that two sequent proofs $\pi, \pi'$ produce the same morphism in the free smc category $V[T]$ iff any two of their unit-extended proof nets $\gamma, \gamma'$ are rewiring-equivalent. 

Notion of directed rewiring... 


## References

* [[Todd Trimble]], _Linear logic, bimodules, and full coherence for autonomous categories. PhD thesis, Rutgers University, 1994 
 {#TT94} 

* {#KM71} [[Max Kelly]], [[Saunders MacLane]], _Coherence in closed categories_, JPAA 1 (1971), 97-140 ([web](http://www.sciencedirect.com/science/article/pii/0022404971900132)) 

* [[Richard Blute]], Robin Cockett, [[R. A. G. Seely|Robert Seely]], [[Todd Trimble]], _Natural deduction and coherence for weakly distributive categories_, JPAA 113 (1996), 229-296. ([web](http://www.sciencedirect.com/science/article/pii/002240499500159X)) 
 {#BCST96}



[[!redirects Trimble rewirings]]
