# Contents 
* table of contents 
{:toc} 

## Idea

A property of a mathematical structure is *hereditary* if every substructure also 
satisfies that property. The idea is that substructures "inherit" the property from the structure. 

## Definition 

A general [[model theory|model-theoretic]] definition is as follows: a [[sentence]] $S$ (thought of as a property which may or may not hold for a structure) of a [[language]] $L$ is *hereditary* if, whenever $S$ is true for a [[structure]] $X$ of $L$, then it is also true for every embedded [[substructure]] of $X$. 

This general definition admits variants, some of which are described below. In category theory, a categorical property (a sentence expressed in the language of category theory) may be said to be $M$-*hereditary* (for various classes $M$ of monomorphisms, e.g., the class of [[regular monomorphisms]]) if, whenever it holds for an object $X$, then it also holds for $M$-subobjects of $X$. 

## Examples 

### In topology 

In [[general topology]], the default meaning of "hereditary" is that if the property holds for a [[topological space]] $X$, then it holds also for [[subspaces]] of $X$. (Note that subspaces are equivalent to [[regular subobjects]] in $Top$.) Examples: 

* The [[separation axioms]] abbreviated as $T_0$, $T_1$, $T_2$, $T_3$, and $T_{3 \frac1{2}}$ are hereditary. 

* The [[second-countable space|second-countability axiom]] is hereditary, as is the [[first-countable space|first-countability axiom]]. 

* [[metrizable space|Metrizability]] is hereditary. 

A property is *weakly hereditary* or *closed hereditary* if it is inherited by [[closed subspaces]]. (Note that in the category $Haus$ of [[Hausdorff spaces]], closed subspaces are equivalent to regular subobjects.) Examples: 

* [[compact space|Compactness]] is weakly hereditary.  

* [[paracompact space|Paracompactness]] is weakly hereditary. 

* [[normal space|Normality]] is weakly hereditary. 

### In graph theory 

In [[graph theory]], the default meaning of "hereditary" is that the property be inherited by induced subgraphs. (If $G = (V, E)$ is a [[simple graph]] and $S \subseteq V$, then the subgraph induced by this inclusion is where every edge of $G$ whose incident vertices lie in $S$ is an edge of the subgraph. Induced subgraphs are equivalent to regular subobjects in the [[quasitopos]] of [[category of simple graphs|simple graphs]].) Examples: 

* The property of being a [[forest]] is hereditary. 

* The property of being acyclic is hereditary. 

* The property of being [[planar graph|planar]] is hereditary. 

### In algebra 

The following examples are well-known. 

* In the category of groups, the property of being a [[free group]] [[Nielsen-Schreier theorem|is hereditary]]. 

* In the category of abelian groups, the property of being [[free abelian group|free abelian]] is hereditary. 

* [More generally](/nlab/show/principal+ideal+domain#StructureTheoryOfModules), in the category of [[modules]] over a [[PID]], the property of being [[free object|free]] is hereditary. 

* In the category of modules over any [[commutative ring]], being [[torsionfree module|torsionfree]] is hereditary. 

* In the category of modules over a [[Noetherian ring]], being a [[finitely generated module]] is hereditary. 
