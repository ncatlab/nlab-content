
# Automata
* table of contents
{: toc}

## Idea

An automaton is an abstract concept of machine, which consists of states and processes between the states.


## Definition

An __automaton__ is formally definable as in [[Joy of Cats]] as a sextuple ($Q$, &#931;, $Y$, &#948;,  $q_{0}$, $y$), where $Q$ is the set of states,  &#931; and $Y$ are the sets of input symbols and output symbols, respectively,  &#948;:  &#931; $\times$ $Q$ $\to$ $Q$ is the transition map, $q_{0}$ &#1013; $Q$ is the initial state, and $y$: $Q$ $\to$ $Y$ is the output map.  Morphisms from an automaton ($Q$, &#931;, $Y$, &#948;,  $q_{0}$, $y$) to an automaton ($Q$&#8242;, &#931;&#8242;, $Y$&#8242;, &#948;&#8242;,  $q_{0}$&#8242;, $y$&#8242;) are triples ($f_{Q}$, $f_{\Sigma}$, $f_{Y}$) of functions $f_{Q}:  Q \to Q\prime$,  $f_{\Sigma}: \Sigma \to \Sigma$,  and $f_{Y}:  Q \to Q$ satisfying the following conditions:

(i) preservation of transition: 
    $\delta\prime(f_{\Sigma}(\gamma), f_{Q}(q)) =      f_{Q}(\delta(\gamma, q))$,

(ii) preservation of outputs: $f_{Y}$($y$($q$)) = $y$$\prime(f_{Q}(q))$,

(iii) preservation of initial state: 
      $f_{Q}(q_{0}) = q_{0}\prime$.    

A __deterministic sequential Moore automaton__ is ....

Given two such automata $A$ and $B$, a __simulation__ of $A$ in $B$ is ....


## The category of automata

There is a [[category]] $Aut$ whose [[object|objects]] are deterministic sequential Moore automata and whose [[morphism|morphisms]] are simulations.


[[!redirects automaton]]
[[!redirects automata]]
[[!redirects Aut]]
