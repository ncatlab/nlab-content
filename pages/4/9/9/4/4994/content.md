
# Deterministic automata
* automatic table of contents goes here
{:toc}

## Definitions

(For the moment, mostly as an example of a [[coalgebra for an endofunctor]].)

This will give the classical definition as a state-based system and then show how to turn that form into the coalgebraic form.  The point is that other coalgebras should then be easier to interpret.

+-- {: .un_defn}
###### Definition
A **deterministic automaton** consists of the following data:
 
* a set of _states_, $Q$;

* a set, $\Sigma$, of _inputs_ ;

* a function, $\delta : Q\times \Sigma \to Q$, called the _next state function_,

and

* a predicate, $final : Q \to bool = \{\bot, \top\}$, the [[boolean domain]].
=--

In the usual interpretation if the automaton is in state $q$, and is 'given' the input $\sigma$, then it changes to being in state $\delta(q,\sigma)$.  

The 'final' predicate, of course, returns $\top$ if a state is a _final state_ and $\bot$ otherwise. (There will, in general, be a set of final or 'accept' states.) 

(For the moment we will not look in any detail at the links between automata and languages.)


## Currying $\delta$

The first step in transforming this to the coalgebraic form is to [[currying|curry]] $\delta$, so as to obtain it in the form $\delta : Q\to Q^\Sigma$. We thus have for a state, $q\in Q$, $\delta(q,) : \Sigma \to Q$.  We then also have a product function

$$\alpha = \delta \times (final) : Q \to  Q^\Sigma\times bool.$$

If we now write $HQ = Q^\Sigma\times bool$, we get a functor (for you to check) $H : Set \to Set$ and the deterministic automaton corresponded precisely to a [[coalgebra for an endofunctor|coalgebra]], $(Q,\alpha)$, for $H$.


## ... and the morphisms?

Rather than start with a classically defined morphism of automata, we will take a morphism $f : (Q,\alpha)\to (Q',\alpha')$ of coalgebras. We thus have that $f : Q\to Q'$ is a mapping of states, and that $\alpha'\circ f = H(f)\circ \alpha$. Now let $q\in Q$ and $\sigma\in \Sigma$, then the equation tells us that $\delta'(f(q),\sigma) = f(\delta(q,\sigma)$ and that the final states of $Q$ are mapped onto those of $Q'$.  In other words the concept of morphism of these $H$-coalgebras is precisely that of functional simulation of deterministic automata. 


## Terminal coalgebra

The [[terminal coalgebra]], $(T,\alpha_T)$, for this endofunctor is neat. It has state space, $T = \mathcal{P}(\Sigma^*)$, the power set of the [[free monoid]]/ Kleene star of the set of 'symbol labels'. This power set is precisely the set of all languages over the alphabet $\Sigma$, as a [[language]] is defined to be a subset of $\Sigma^*$.

The next state function for $(T,\alpha_T)$ is defined by $\delta_T(L,s) = \{w\in \Sigma^* |sw \in L\}$.


## References

For a summary of automata theory , look at the [Wikipedia](http://en.wikipedia.org/wiki/Automata_theory).

For a thorough treatment, see

*  [[M. V. Lawson]], _Finite Automata_, [Google books](http://books.google.co.uk/books?id=MDQ_K7-z2AMC&dq=automata+theory+lawson&source=bl&ots=0w-Xp8AaDa&sig=6dXKjG0tVY6aUlvlAc5UaT-ObX8&hl=en&ei=Ywy6TPmtCJSOjAfzgYXYDg&sa=X&oi=book_result&ct=result&resnum=1&sqi=2&ved=0CBoQ6AEwAA)

or other texts on the subject.

For the coalgebraic treatment, this is discussed in: 

*  [[A. Kurz]]:  _Coalgebras and Modal Logic._ Course Notes for ESSLLI 2001, Version of October 2001. Appeared on the CD-Rom ESSLLI'01, Department of Philosophy, University of Helsinki, Finland, available from [site](http://www.cs.le.ac.uk/people/akurz/works.html).

category: computer science
[[!redirects deterministic automaton]]
[[!redirects deterministic automata]]
