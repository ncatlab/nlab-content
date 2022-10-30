
# Pure and mixed states
* table of contents
{: toc}

## Idea

In [[physics]], recall that a [[state]] of a [[physical system]] is (in the Bayesian interpretation) a specification of the information that one might have about the system (typically relative to some fixed background information).  States form (at least) a [[poset]] where $\psi \leq \phi$ means that $\phi$ contains all of the information of $\psi$ (and possibly more).  A __pure state__ is a [[maximal element]] of this poset: a state that specifies as much information as possible about the system.  A __mixed state__ is a state that is not pure.


## Definitions

Fairly generally, a physical system has a complex $C^*$-[[C-star-algebra|algebra]] $A$ of [[observables]] and a __state__ is a positive-semidefinite linear operator $\rho\colon A \to \mathbb{C}$ such that $\rho(1) = 1$.  We might write $\rho$ as a convex-linear combination of two other states:
\[ \rho = a \sigma + b \tau ,\label{combo}\]
where necessarily $0 \leq a, b \leq 1$ and $a + b = 1$.

The state $\rho$ is __pure__ if, whenever (eq:combo) holds for $\sigma \neq \tau$, then either $a = 0$ (hence $b = 1$ and $\rho = \tau$) or $a = 1$ (hence $b = 0$ and $\rho = \sigma$); conversely, $\rho$ is __mixed__ if we ever have (eq:combo) for $\sigma \neq \tau$ and $0 \lt a \lt 1$ (hence $0 \lt b \lt 1$ and $\rho \neq \sigma, \tau$).

Really, this definition makes sense as long as the states form a [[convex space]].

To define when one state gives at least as much information as another (the [[partial order]] from the Idea section), let $\rho \leq \sigma$ mean that the [[mutual information]] $I(\rho,\sigma)$ equals the [[entropy]] $H(\rho)$, or equivalently that the conditional entropy $H(\rho|\sigma)$ is zero.  (In the classical case, this partial order is attributed to [Shannon (1953)](#Shannon1953), which I have not read, by [Li & Chong (2011)](#LiChong2011), which I have only skimmed.)  The [[maximal elements]] under this partial order should be precisely the pure states, but the direct definition of pure states is much simpler.

+-- {: .query}
I need to check this claim.  &#8212;Toby
=--


## Special cases

If $A$ is the algebra of continuous complex-valued functions on some [[compactum]] $X$, then the __pure states__ on $A$ correspond precisely to the [[points]] in $X$; so pure states here are the states of [[classical mechanics]] (at least for a compact [[phase space]]).  The mixed states, however, correspond more generally to [[Radon measure|Radon]] [[probability measures]] on $X$, with the pure states as the [[Dirac delta measure]]s.

On the other hand, if $A$ is the algebra of all [[bounded operators]] on some [[Hilbert space]] $H$, then the pure states on $A$ correspond precisely to the rays in $H$, as is usual in [[quantum mechanics]].  The mixed states, however, correspond more generally to [[density matrices]] on $H$, with the pure states those matrices of the form ${|\psi\rangle}{\langle\psi|}$ for some unit vector ${|\psi\rangle}$.


## Classical versus quantum

In any case, a pure state is a state of maximal information, while a mixed state is a state with less than maximal information.  In the classical case, we may say that a pure state is a state of *complete* information, but this does not work in the quantum case; from the perspective of the information-theoretic or Bayesian interpretation of quantum physics, this inability to have complete information, even when having maximal information, is the key feature of [[quantum physics]] that distinguishes it from [[classical physics]].


## References

Not really references on this subject, but ones referred to in the text:

*  [[Claude Shannon]] (1953): The lattice theory of information, IEEE Transactions on Information Theory 1, 105--107.
   {#Shannon1953}

*  Hua Li and Edwin Chong (2011): On a connection between information and group lattices, Entropy 13, 683--708; [web](http://www.mdpi.com/1099-4300/13/3/683).
   {#LiChong2011}



[[!redirects pure state]]
[[!redirects pure states]]
[[!redirects mixed state]]
[[!redirects mixed states]]
