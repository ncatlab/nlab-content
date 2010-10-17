
# Non-deterministic automata
* automatic table of contents goes here
{:toc}

## Definitions

(For the moment, mostly as an example of a [[coalgebra for an endofunctor]] and to start discussion of models for non-determinism.)

This will give the classical definition as a non-deterministic state-based system and then show how to turn that form into the coalgebraic form.

+-- {: .un_defn}
###### Definition

A **non-deterministic automaton** consists of the following data:
 
* a set of _states_, $Q$;

* a set, $\Sigma$, of _input symbols_ ;

* a function, $\delta : Q\times \Sigma \to \mathcal{P}(Q)$, called the _next state relation_,

and

* a predicate, $final : Q \to bool = \{\bot, \top\}$, the [[boolean domain]].
=--

In the usual interpretation if the automaton is in state $q$, and is 'given' the input $\sigma$, then it changes to being in one of the states in the subset, $\delta(q,\sigma)$, of $Q$.  

The 'final' predicate, of course, returns $\top$ if a state is a _final state_ and $\bot$ otherwise. (There will, in general, be a set of final or 'accept' states.) 

(For the moment we will not look at the links between automata and languages.)


## Currying $\delta$

The first step in transforming this to the coalgebraic form is to [[currying|curry]] $\delta$, so as to obtain it in the form $\delta : Q\to \mathcal{P}(Q)^\Sigma$. We thus have for a state, $q\in Q$, $\delta(q,) : \Sigma \to \mathcal{P}(Q)$.  We then also have a product function

$$\alpha = \delta \times (final) : Q \to  Q^\Sigma\times bool.$$

If we now write $HQ = \mathcal{P}(Q)^\Sigma\times bool$, we get a functor (for you to check) $H : Set \to Set$ and the non-deterministic automaton corresponded precisely to a [[coalgebra for an endofunctor|coalgebra]], $(Q,\alpha)$, for $H$.


## References

For a summary of automata theory , look at the [Wikipedia](http://en.wikipedia.org/wiki/Automata_theory).

For a thorough treatment, see

*  M. V. Lawson, _Finite Automata_, [Google books](http://books.google.co.uk/books?id=MDQ_K7-z2AMC&dq=automata+theory+lawson&source=bl&ots=0w-Xp8AaDa&sig=6dXKjG0tVY6aUlvlAc5UaT-ObX8&hl=en&ei=Ywy6TPmtCJSOjAfzgYXYDg&sa=X&oi=book_result&ct=result&resnum=1&sqi=2&ved=0CBoQ6AEwAA)

or other texts on the subject.

For the coalgebraic treatment, this is discussed in: 

*  A.Kurz:  _Coalgebras and Modal Logic._ Course Notes for ESSLLI 2001, Version of October 2001. Appeared on the CD-Rom ESSLLI'01, Department of Philosophy, University of Helsinki, Finland, available from [site](http://www.cs.le.ac.uk/people/akurz/works.html).


[[!redirects nondeterministic automaton]]
[[!redirects nondeterministic automata]]
[[!redirects non-deterministic automaton]]
[[!redirects non-deterministic automata]]
