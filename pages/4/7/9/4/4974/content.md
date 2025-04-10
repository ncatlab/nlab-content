
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
 is a subset $x \subseteq E$ which is consistent ($x \in \Con$) and down-closed (if $e\in x$ and $e' \leq e$ then $e' \in x$). The set of _finite_ configurations of $E$ is denoted $\mathscr{C}(E)$. 

\end{definition}


##The category of event structures##

\begin{definition}
A **map of event structures** from $(E, \leq, \Con)$ to $(E', \leq', \Con')$ is a function $f : E \to E'$ such that:

* $f$ preserves configurations: if $x\in \mathscr{C}(E)$, then $f(x) \in \mathscr{C}(E')$.

* $f$ is locally injective: if $e, e' \in x \in \mathscr{C}(E)$ and $f(e) = f(e')$, then $e = e'$.
 
\end{definition}

Intuitively, a map $E \to E'$ expresses that all executions of $E$ can be faithfully simulated within $E'$. 

*Partial* maps of event structures are also important in the literature, for example in the event structure model of CCS. The definition is the same when $f$ is a partial function, and the condition $f(e) = f(e')$ means in particular that they are both defined. Winskel and Nielsen explain this definition as follows: 

_A morphism $f : E\to E'$ between event structures expresses how behaviour in $E$ determines behaviour in $E'$. The partial function, $f$, expresses how the occurrence of an event in $E$ implies the simultaneous occurrence of an event in $E'$; the fact that $f(e) = e'$ can be understood as expressing that the event $e$ is a ''component'' of the event $e'$ and, in this sense, that the occurrence of $e$ implies the simultaneous occurrence of $e'$. If two distinct events in $E$ have the same image in $E'$ under $f$ then they cannot belong to the same configuration._

With this definition of morphism, and the obvious notions of identity and composition, we get the category $\mathbf{ES}$ of event structures (and total maps). 

##Event structures as presheaves 

Let $\mathbf{P}$ denote the full subcategory of $\mathbf{ES}$ consisting of finite event structures with no conflicts. Equivalently, this is the category of finite posets and (not necessarily monotone) maps that preserve down-closed subsets.

Then the functor
$$\mathbf{ES} \longrightarrow PSh(\mathbf{P})$$
that maps $E$ to the presheaf $P \mapsto \mathbf{ES}(P, E)$ is full and faithful, because the inclusion $\mathbf{P} \hookrightarrow \mathbf{ES}$ is dense.

The essential image of this functor is a subcategory of nonempty [[separated presheaves]] (for the [[Grothendieck topology]] generated by families of jointly surjective maps) satisfying two additional conditions (see [Winskel](#Representation)). 

(If we restrict the morphisms in $\mathbf{ES}$ and $\mathbf{P}$ to maps of event structures which are also monotone (these are often called _rigid_ maps) then a similar result holds, and the characterization of the essential image is a bit simpler.)


##Event structures with symmetry

Symmetry on an event structure is given by additional structure: an equivalence relation on configurations, such that equivalent configurations are [[bisimulation|bisimilar]]. Formally, this is defined in terms of _open maps_.  

\begin{definition}
A map $f : E \to E'$ is _open_ if it satisfies a path-lifting condition: writing $\mathbf{P}$ for the subcategory of paths defined above, the condition requires that for $P, Q \in \mathbf{P}$ and a commutative square as in the diagram below, there must be a factorization in terms of two commutative triangles:
\begin{tikzcd}
	P & E \\
	Q & {E'}
	\arrow[from=1-1, to=1-2]
	\arrow[from=1-1, to=2-1]
	\arrow[from=1-2, to=2-2]
	\arrow[dashed, from=2-1, to=1-2]
	\arrow[from=2-1, to=2-2]
\end{tikzcd}
\end{definition}


\begin{definition}
An _event structure with symmetry_ is an event structure $E$ equipped with an internal [equivalence relation](congruence), i.e. a span 
$$E \longleftarrow R \longrightarrow E $$
of [[jointly monic morphisms|jointly monic]] maps, which is reflexive, symmetric and transitive (this definition uses the fact that $\mathbf{ES}$ has pullbacks), and such that the two legs of the span are open maps. 
\end{definition}

This can be defined more concretely: an event structure with symmetry is an event structure $E$ equipped with a collection of set-theoretic bijections $\theta : x \cong y$ between configurations of $E$, closed under inverses and compositions and containing all identities (so the set $\mathscr{C}(E)$ of configurations becomes a subcategory of $\mathbf{Set}$, and a groupoid), such that, for every  bijection $\theta : x \to y$ in $\mathscr{C}(E)$:
* if $x' \subseteq x$ for some configuration $x'$, then the restriction of $\theta$ to $x'$ is also in $\conf{E}$;
* if $x \subseteq x'$ for some configuration $x'$, then there is an extension of the bijection $\theta$ to some bijection $\theta' : x' \to y'$ in the symmetry.

We say a map $E \to E'$ preserves symmetry if, for every $\theta : x \cong y$ in the symmetry of $E$, the bijection  
\[ 
f x \cong x \cong y \cong f y
\] 
(determined by the injectivity of $f$ on configurations) is in the symmetry $E'$. This gives a category $\mathbf{ESS}$ of event structures with symmetry.  

\begin{definition}
Two parallel maps $f, g : E \to E'$ in $\mathbf{ESS}$ are homotopic (written $f \sim g$) if for every $x \in \mathscr{C}(E)$ the bijection $f x \cong x \cong g x$ (determined by the injectivity on configurations of $f$ and $g$) is in the symmetry of $E'$. 
\end{definition}

### Event structures with symmetry and presheaves  

It is shown in [Staton & Winskel](#StatonWinskel) that with the introduction of symmetry, event structures represent all presheaves over $\mathbf{P}$. Here the functor $\mathbf{ESS} \to \mathrm{PSh}(\mathbf{P})$ takes $E$ to the presheaf $P \mapsto \mathbf{ESS}(P, E)/~$, where we quotient by homotopy of maps. 

##References##

Event structures were introduced in:

* [[G. Winskel]], _Event Structures_, in _Advances in Petri Nets 1986_. Springer Lecture Notes in Computer Science 255, 1987, ([pdf](https://www.cl.cam.ac.uk/~gw104/Winskel1987_Chapter_EventStructures.pdf)).

Other papers on event structures:

* M. Nielsen, G. D. Plotkin, and [[G. Winskel]], _Petri nets, event structures and domains, part I_, Theoretical Computer Science, vol. 13, pp. 85–108, 1981. [doi:10.1016/0304-3975(81)90112-2](https://doi.org/10.1016/0304-3975%2881%2990112-2)

* [[G. Winskel]] and M. Nielsen, Models for concurrency. vol. 3, Handbook of Logic in Computer Science, pages 100 - 200, Oxford Univ. Press, 1994. (see also [online technical report](http://www.daimi.au.dk/PB/463/PB-463.pdf)).

* {#Representation} [[G. Winskel]], _Event Structures as Presheaves -- Two Representation Theorems_ [BRICS report](https://www.brics.dk/RS/99/7/BRICS-RS-99-7.pdf)

* {#Symmetry} [[G. Winskel]], _Event Structures with Symmetry_ [pdf](https://www.cl.cam.ac.uk/~gw104/EvStrswSymm-Corrected.pdf)

* [[G. Winskel]], _Events, causality, and symmetry_, (an earlier version appeared in the BCS conference 'Visions in Computer Science.' September 2008. The final version appears in a special issue of The Computer Journal 2009; doi: 10.1093/comjnl/bxp052; see also  an [online version](http://www.cl.cam.ac.uk/~gw104/CJVision-Revised.pdf)).

* {#StatonWinskel} [[Sam Staton]] and [[G. Winskel]], On the expressivity of symmetry in event structures, [LICS 2010](http://www.cl.cam.ac.uk/~gw104/lics2010final.pdf)

* R.J. van Glabbeek, [[Gordon Plotkin]], _Configuration Structures, Event Structures and Petri Nets_ &lbrack;[arXiv:0912.4023](https://arxiv.org/abs/0912.4023)&rbrack;


[[!redirects event structure]]
[[!redirects event structures]]
