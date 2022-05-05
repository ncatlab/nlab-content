[[!redirects knowledge in a multiagent system]]


##Idea 
To quote from a book on the subject:

''Multiagent systems are a new paradigm for understanding and building distributed systems, where it is assumed that the computational components are autonomous: able to control their own behaviour in the furtherance of their own goals.''


The area is a very wide one and this entry only deals with some generalities especially links between local `knowledge' and more global forms and the models of this that involve the use of [[modal logic]].

##Introduction

In many studies of distributed systems, a multiagent model is
used.  

* An agent is a processor, sensor or finite state machine,
interconnected by a communication network with other `agents'.

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
$K_i\phi$, the statement that agent $i$ `knows' proposition
$\phi$, we clearly expect within the logic of that system that
we have as an axiom:

$$K_1\phi\Rightarrow K_2\phi \wedge K_3\phi,$$

in other words, if 1 knows something then we have that both 2 and 3 know it.


The logic $S5_n$ is obtained from ordinary [[propositional logic]] by
adding `knowledge operators', $K_i$ as above. (In the literature
the notation $K_i\phi$ is often replaced by $\Box_i\phi$.)  It
models a community of *ideal* knowledge agents who have
the properties of 

* veridical knowledge (everything they know is
true), 

* positive introspection (they know what they know) 

and
*  negative introspection (they know what they do not know). 

These
properties are reflected in the axiom system for the logic.  For more on this see   the entry [[the logic S5(m)|S5(n)]].
##References

###Wikipedia 

* [Wikipedia article](http://en.wikipedia.org/wiki/Multi-agent_system)

###Books

* [[Michael Wooldridge]] _An Introduction to MultiAgent Systems_ Wiley, 2009


###Articles

 * [[A. Lomuscio]] and [[M. D. Ryan]], _An algorithmic approach to knowledge evolution_, Artificial Intelligence for Engineering Design, Analysis and Manufacturing (AIEDAM), Vol. 13, No. 2 (Special issue on Temporal Logic in Engineering), 23pp, 1999. 


* [[A. Lomuscio]], R. van der Meyden, and [[M. D. Ryan]], _Knowledge in Multi-Agent 
Systems: Initial Configurations and Broadcast_, ACM Transactions on Computational Logic (TOCL), Volume 1, Issue 2, pp. 247- 284. ACM Press. October 2000. 
