[[!redirects transition systems]]

# Contents
* table of contents
{:toc}

##Transition systems.##

Transition systems are a well established [[semantics|semantic model]] for both sequential and concurrent systems.

+--{: .un_defn}
######Definition######

A _transition system_ is a structure $T = (S,i,L,Tran)$, where

* $S$ is a set of _states_ with initial state, $i$;

* $L$ is a set of _labels_, sometimes referred to also as _events_;

* $Tran\subseteq S\times L\times S$ is the _transition relation_.

=--

Let $(S, i, L, Tran )$ be a transition system. We write 

$$s\stackrel{a}{\to} s'$$ 
 
to indicate that $(s, a, s')\in Tran$. 

+--{: .un_defn}
######Definition######

 A _morphism_ from one transition system, $T$, to another 
$T'$  will be a pair $(\sigma, \lambda)$, in which 

* $\sigma$ is a function from the states of $T$ to those of $T'$ 
 
* $\lambda$ is a [[partial function]] from the labels of $T$ to those of $T'$ such that for any transition $s\stackrel{a}{\to} s'$ of $T$ if $\lambda(a)$ is defined, then $\sigma(s)\stackrel{\lambda(a)}{\to} \sigma(s')$ is a 
transition of $T'$; otherwise, if $\lambda(a)$ is undefined, then $\sigma(s) = \sigma(s')$. 
=--

It is useful to rework this definition of morphism using a variant of the idea, discussed at [[partial function]], that replaces a partial function by a total function using the neat trick of adding an additional element $\bot$ to the codomain. (We will use the notation from [[partial function]] freely in what follows.)   This is done here simply by introducing **idle transitions** $(s,\bot,s)$ thought of as going from $s$ to itself, and working with $L_\bot$ as a set of labels instead of  $L$.  (This is very neat here as it corresponds the label $\bot$ to 'do nothing' to the states.)  After completing everything in this way we get new transition systems $T_\bot = (S,i,L_\bot, Tran_\bot)$, etc. and will work with these. (Of course, $Tran_\bot = Tran \cup \{ (s,\bot,s)\mid s\in S\}$.)  Now a morphism $f$ is the same as given by a pair $\sigma: S\to S'$, as before, and $\lambda: L_\bot\to L'_\bot$, satisfying the compatibility condition that if $(s,a,s')\in Tran_\bot$, then $(\sigma(s),\lambda(a),\sigma(s'))\in Tran'_\bot$, (and that $\lambda_\bot(\bot) = \bot'$).

This way we get a category, $TS$, of transition systems.



The notions of transition system and of morphisms between them is clearly related to (low dimensional) [[cubical sets]] / labelled [[directed graphs]]/labelled [[transition systems]], but we will need to consider labelled  cubical sets.


##Labeled transition systems.##

In the above, we have used the notation $L$ to stand for the set of _events_ and the set of _labels_ for those events. It is sometimes useful to make a distinction between the events themselves and their labels and to explicitly give a labelling as a function.  This is important, for instance, in treating 'relabelling' which leads to [[fibration|categorical fibrational situations]] (see the paper by Winskel and Nielsen, cited below.) In order to make the distinction clearer, we will replace $L$ by $E$ and refer to its elements as 'events' in what follows.

+--{: .un_defn}
######Definition######

A _labelled transition system_ consists of a transition 
system $T = (S, i, E, Tran)$ together with a set $L$ of _labels_, and a function $l : E \to L$.  We denote it by $(T,L,l)$.
 
A _morphism_, $(\sigma, \tau , \lambda) : (T_1 , L_1 , l_1) \to (T_2 , L_2 , l_2 )$ between labeled transition 
systems consists of a morphism $(\sigma, \tau) : T_1 \to T_2$ between the underlying transition 
systems together with a [[partial function]] $\lambda : L_1 \to L_2$ such that $l_2 \circ \tau = \lambda \circ l_1$. 
=--
We 
write $LTS$ for the category of labeled transition systems.

\begin{remark}
The term *labelled transition system* can also refer to the data of a domain, a set of labels and a transition relation, without any distinguished initial or final sets.
\end{remark}

##TSs as relational structures##

We can view a transition system as a [[relational structure]]. The set of states is the 'set of worlds' and for each event, $e \in E$ we define a relation $R_e \subseteq S\times S$ by $(s,s')\in R_e$ if and only if, $(s,e,s')\in Trans$.  We thus derive a relation for each event and, conversely, if we know the family $\{R_e \mid e\in E\}$, then we can rebuild $Trans$ in the obvious way.  

##Higher dimensional analogues


There are tentative definitions of


[[higher dimensional transition system]],


which take a more [[nPOV]] of this theory.

## See also ##

* [[bisimulation]]

* [[models for concurrency]]

## References

* [[Mogens Nielsen]], [[Glynn Winskel]]: *Models for concurrency*, in: *Handbook of Logic in Computer Science* vol 4, Oxford Univ. Press (1994) 1-148 &lbrack;[pdf](https://www.cl.cam.ac.uk/~gw104/winskel-nielsen-models-for-concurrency.pdf), [[WinskelNielsen-Concurrency.pdf:file]], [doi:10.5555/218623.218630](https://dl.acm.org/doi/10.5555/218623.218630), [ISBN:9780198537809](https://global.oup.com/academic/product/handbook-of-logic-in-computer-science-9780198537809?lang=en&cc=at)&rbrack;

* [[Eric Goubault]] and [[Samuel Mimram]], *[Formal Relationships Between Geometrical and Classical Models for Concurrency](http://arxiv.org/abs/1004.2818)*


Discussion in relation to [[bisimulations]] and [[open morphisms]]:

* {#JoyalNielsenWisnkel94} [[André Joyal]], [[Mogens Nielsen]], [[Glynn Winskel]]: *Bisimulation from open maps*, [[BRICS]] report series RS-94-7 (1994) &lbrack;[doi:10.7146/brics.v1i7.21663](https://doi.org/10.7146/brics.v1i7.21663), [pdf](http://www.brics.dk/RS/94/7/BRICS-RS-94-7.pdf)&rbrack;, Information and Computation **127** 2 (1996) 164-185 &lbrack;[doi:10.1006/inco.1996.0057](https://doi.org/10.1006/inco.1996.0057)&rbrack;


[[!redirects labeled transition system]]
[[!redirects labelled transition system]]
[[!redirects labeled transition systems]]
[[!redirects labelled transition systems]]

category:computer science