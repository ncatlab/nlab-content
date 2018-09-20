[[!redirects knowledge in a multiagent system]]
# Multiagent systems
* table of contents
{:toc}


##Idea 
To quote from a book on the subject:

>"Multiagent systems are a new paradigm for understanding and building distributed systems, where it is assumed that the computational components are autonomous: able to control their own behaviour in the furtherance of their own goals." ([Wooldridge09](#Wooldridge09))


The area is a very wide one and this entry only deals with some generalities especially links between local `knowledge' and more global forms and the models of this that involve the use of various types of [[modal logic]].

##Introduction

In many studies of [[distributed system]]s, a multiagent model is
used.  

* An agent is a processor, sensor or finite state machine,
interconnected by a communication network with other 'agents'.

Typically each agent has a local state that is a function of its
initial state, the messages received from other agents,
observations of the external environment and possible internal
actions.  It has become customary when using formal models of
distributed systems to use modal [[epistemic logics]] as one of the
tools for studying the knowledge of such systems. The basic such
logic for handling a system with $n$-agents is one known as
[[the logic S5(m)|S5(n)]]. Unless the system is very simple the actual logic will be
an extension of that basic one, that is, it may have more axioms.

For instance, the way the various agents are connected influences
the logic in subtle ways. Suppose that agent 1 sends all its
information immediately to agents 2 and 3, then if we denote by
$K_i \phi$, the statement that agent $i$ 'knows' proposition
$\phi$, we clearly expect within the logic of that system that
we have as an axiom:

$$K_1 \phi \Rightarrow K_2\phi \wedge K_3 \phi,$$

in other words, if 1 knows something then we have that both 2 and 3 know it.


The logic $S5_n$ is obtained from ordinary [[propositional logic]] by
adding 'knowledge operators', $K_i$, as above. (In the literature
the notation $K_i\phi$ is often replaced by $\Box_i\phi$.)  It
models a community of *ideal* knowledge agents who have
the properties of 

* veridical knowledge (everything they know is true), 

* positive introspection (they know what they know) 

and

*  negative introspection (they know what they do not know). 

These properties are reflected in the axiom system for the logic.  For more on this see   the entry [[the logic S5(m)|S5(n)]].

##Models for these logics 


The classical models for multimodal logics, and for $S5_n$ and its extensions in particular, are combinatorial models known as [[Kripke frames]] and, for $S5_n$, Kripke equivalence frames.  These consist of a set $W$, called the _set of possible worlds_, and $n$-equivalence relations $\sim_i$, one for each agent.  The interpretation of $\sim_i$ is that if $w_1$, $w_2$ are two possible worlds and $w_1\sim_i w_2$, then agent $i$ cannot tell these two worlds apart.

##Interpreted systems

 Fagin, Halpern, Moses and Vardi, in various combinations, have put forward a simpler combinatorial model known as an _interpreted system_.  These have the same formal expressive power as Kripke frames, but are nearer the intuition of interacting agents than is the more abstract Kripke model.

 As before one has a set, $A = \{1,2, \ldots, n\}$, of agents, and now one assumes each agent $i$ can be in any state of a set $L_i$ of local states.  In addition one assumes given a set $L_e$ of possible states of the `environment'.  More formally:
 
+-- {: .un_defn}
###### Definition

A set of global states (SGS) for an interpreted system is a subset $S$ of the product $L_e \times L_1 \times \ldots \times L_n$ with each $L_e$, $L_i$ non-empty.  If $S = L_e \times L_1 \times \ldots \times L_n$, then the SGS is called a _hypercube_.
=--

##References

###Wikipedia 

* [Wikipedia article](http://en.wikipedia.org/wiki/Multi-agent_system)

###Books

* {#Wooldridge09} [[Michael Wooldridge]], _An Introduction to MultiAgent Systems_, Wiley, 2009


###Articles

 * [[A. Lomuscio]], [[M. D. Ryan]], _An algorithmic approach to knowledge evolution_, Artificial Intelligence for Engineering Design, Analysis and Manufacturing (AIEDAM), Vol. 13, No. 2 (Special issue on Temporal Logic in Engineering), 23pp, 1999. 


* [[A. Lomuscio]], R. van der Meyden, [[M. D. Ryan]], _Knowledge in multi-agent systems: initial configurations and broadcast_, ACM Transactions on Computational Logic (TOCL), Volume 1, Issue 2, pp. 247- 284. ACM Press. October 2000. 

category: computer science