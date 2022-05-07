
# Contents
* automatic table of contents goes here
{:toc}

##Idea##

Event structures were introduced in order to abstract away from the precise 'places' and times at which events occur in distributed systems. The structure focuses on the events and the causal ordering between them.

Event structures in the sense of this article are sometimes also called *prime* event structures. There are other variants, for example where the partial order $\leq$ is replaced by an *enabling relation* $\vdash$. This is usually more expressive, because an event can have *disjunctive causes*: if $a \vdash e$ and $b \vdash e$, then either of $a$ or $b$ suffices for $e$ to occur. In a prime event structure, if $a \leq e$ and $b \leq e$ then *both* $a$ and $b$ must occur before $e$; these are *conjunctive causes*. 

##Definition##

\begin{definition}
An *event structure* is a tuple $(E,\leq, \mathrm{Con})$ consisting of a [[poset]] $(E,{\le})$ of _events_, and a nonempty set $\mathrm{Con} \subseteq \mathcal{P}(E)$ of _consistent subsets_, satisfying the following axioms:

*  finite causes: for every event $e$ the set $\{e'\mid e'\le e\}$ is finite;

* if $e \in E$ then $\{ e \} \in \mathrm{Con}$;  

* if $X \in \mathrm{Con}$ and $Y \subseteq X$ then $Y \in \mathrm{Con}$; 

* if $X \in \mathrm{Con}$, $e \in X$, and $e' \leq e$, then $X \cup \{ e\} \in \mathrm{Con}$.

\end{definition}

A restricted but simpler definition is as follows: 

\begin{definition}
An *event structure with binary conflict* is a tuple $(E, \leq, \#)$, where $(E, {\leq})$ is a [[poset]] and $\#$ is an irreflexive binary relation on $E$, the *conflict relation*, satisfying: 

* finite causes: for every event $e$ the set $\{e'\mid e'\le e\}$ is finite;

* hereditary conflict: if $e \#  e'$ and $e' \leq e''$ then $e \# e''$. 

\end{definition}

Event structures with binary conflict can be characterised as follows:
\begin{proposition}
If $(E, \leq, \#)$ is an event structure with binary conflict, then defining $\mathrm{Con} = \{ X \subseteq E \mid \forall e, e' \in X. \neg (e \# e') \} $
makes $(E, \leq, \Con)$ an event structure. 

Conversely, if an event structure $(E, \leq, \mathrm{Con})$ satisfies 
\[ 
\forall X \subseteq E. (\forall e, e' \in X. \neg (e \# e')) \implies X \in \mathrm{Con}
\]
then defining $\# = \{ (e, e') \mid \{ e, e'\} \in \mathrm{Con} \}$  makes $(E, \leq, \#)$ an event structure with binary conflict. 
\end{proposition}

That is, event structures with binary conflict correspond to event structures in which pairwise consistency implies mutual consistency.  

We write $E$ for $(E, \leq, \Con)$ whenever possible. The possible states of an event structures are called *configurations*.
 
\begin{definition} 

Let $E$ be an event structure. A **configuration** of $E$
 is a subset $x \subseteq E$ which is consistent ($x \in \Con$) and down-closed (if $e\in x$ and $e' \leq e$ then $e' \in x$). The set of \emph{finite} configurations of $E$ is denoted $\mathscr{C}(E)$. 

\end{definition}


##The category of event structures##

\begin{definition}
A (total) **map of event structures** from $(E, \leq, \Con)$ to $(E', \leq', \Con')$ is a function $f : E \to E'$ such that:

* $f$ preserves configurations: if $x\in \mathscr{C}(E)$, then $f(x) \in \mathscr{C}(E')$.

* $f$ is locally injective: if $e, e' \in x \in \mathscr{C}(E)$ and $f(e) = f(e')$, then $e = e'$.
 
\end{definition}

Intuitively, a map $E \to E'$ expresses that all executions of $E$ can be faithfully simulated within $E'$. 

*Partial* maps of event structures are also important in the literature, for example in the event structure model of CCS. The definition is the same when $f$ is a partial function, and the condition $f(e) = f(e')$ means in particular that they are both defined. Winskel and Nielsen explain this definition as follows: 

_A morphism $f : E\to E'$ between event structures expresses how behaviour in $E$ determines behaviour in $E'$. The partial function, $f$, expresses how the occurrence of an event in $E$ implies the simultaneous occurrence of an event in $E'$; the fact that $f(e) = e'$ can be understood as expressing that the event $e$ is a ''component'' of the event $e'$ and, in this sense, that the occurrence of $e$ implies the simultaneous occurrence of $e'$. If two distinct events in $E$ have the same image in $E'$ under $f$ then they cannot belong to the same configuration. _


With this definition of morphism, and the obvious notions of identity and composition, we get the category $\mathbf{ES}$ of event structures (and total maps). 


##Event structures as presheaves 



##References##

* [[G. Winskel]] and M. Nielsen, Models for concurrency. vol. 3, Handbook of Logic in Computer Science, pages 100 - 200, Oxford Univ. Press, 1994. (see also [online technical report](http://www.daimi.au.dk/PB/463/PB-463.pdf)).

* [[G. Winskel]], _Events, causality, and symmetry_, (an earlier version appeared in the BCS conference 'Visions in Computer Science.' September 2008. The final version appears in a special issue of The Computer Journal 2009; doi: 10.1093/comjnl/bxp052; see also  an [online version](http://www.cl.cam.ac.uk/~gw104/CJVision-Revised.pdf)).

* [[Sam Staton]] and [[G. Winskel]], On the expressivity of symmetry in event structures,
[LICS 2010](http://www.cl.cam.ac.uk/~gw104/lics2010final.pdf)


[[!redirects event structure]]
[[!redirects event structures]]
