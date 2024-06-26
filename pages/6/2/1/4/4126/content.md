
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[quantum mechanics]], the _Kochen-Specker theorem_ -- developed in 1967 by [[Simon Kochen]] and [[Ernst Specker]] -- is a [[no-go theorem]] that places limits on the types of [[hidden variable theories]] that may be used to explain the (apparent) [[probability theory|probabilistic]] nature of [[quantum mechanics]] in a causal way.  It roughly asserts that it is impossible to assign values to all physical [[observables]] while simultaneously preserving the functional relations between them.  It is a complement to [[Bell's theorem]], developed by [[John Bell]] in 1964, and is related to [[Gleason's theorem]], proven by ([Gleason (1957)](#Gleason57)) (who incidentally is the person who communicated the original Kochen-Specker paper to the _Journal of Mathematics and Mechanics_ ).  Later in ([Butterfield-Hamilton-Isham 98](#ButterfieldHamiltonIsham)) it was observed that the Kochen-Specker theorem is equivalent to the statement that the [[spectral presheaf]] has no [[global elements]], which led to the proposal that the [[phase space]] in [[quantum mechanics]] is naturally to be understood as a ([[ringed topos|ringed]]) [[topos]], the "[[Bohr topos]]".

## Kochen-Specker theorem

+-- {: .num_defn #Valuation}
###### Definition

Let $B(\mathcal{H})$ be the algebra of [[bounded operator]]s on some [[Hilbert space]] $\mathcal{H}$. (In physics $\mathcal{H}$ is the space of states of a [[quantum mechanics|quantum mechanical]] system, and the elements $\hat A \in B(\mathcal{H})$ represent quantum observables.) 

A **valuation** on $B(\mathcal{H})$ is a [[function]] 

$$
  \lambda : B(\mathcal{H}) \to \mathbb{R}
$$ 

to the [[real number]]s, satisfying two conditions:


1. _value rule_ -- the value $\lambda(\hat{A})$ belongs to the spectrum of $\hat{A}$;

2. _functional composition principle_ (FUNC) -- for any pair of [[self-adjoint operators]] $\hat{A}$, $\hat{B}$ such that $\hat{B}=h(\hat{A})$ for some real-valued function $h$ we have $\lambda(\hat{B})=h(\lambda(\hat{A}))$.

=--

+-- {: .num_remark}
###### Remark

This has the following equivalent reformulation, which is crucial for the [[sheaf and topos theory|sheaf-theoretic]] interpretation discussed below.

Observed that if $\hat{A}_{1}$ and $\hat{A}_{2}$ commute, then it follows from the [[spectral theorem]] that there exists an operator $\hat{C}$ and [[continuous functions]] $h_{1}$ and $h_{2}$ such that $\hat{A}_{1}=h_{1}(\hat{C})$ and $\hat{A}_{2}=h_{2}(\hat{C})$.  Then the [[axiom]] FUNC in def. \ref{Valuation} implies that a valuation satisfies

$$
  \lambda(\hat{A}_{1} + \hat{A}_{2}) = \lambda(\hat{A}_{1}) + \lambda(\hat{A}_{2})
$$

and

$$
  \lambda(\hat{A}_{1}\hat{A}_{2})=\lambda(\hat{A}_{1})\lambda(\hat{A}_{2})
  \,,
$$

hence that on  [[poset of commutative subalgebras|commutative subalgebras]] it is a [[ring]] [[homomorphism]].

Therefore a valuation as in def. \ref{Valuation} is equivalently a function on the algebra which is an algebra homomorphism on each [[poset of commutative subalgebras|commutative subalgebra]].

(Observe the difference to [[quasi-states]] ([[quantum states]]), which are positive linear functions on commutative subalgebras, not necessarily respecting the ring structure.)

=--

Now we have:

+-- {: .num_theorem}
###### Theorem 
**(Kochen-Specker)**

No valuations on $B(\mathcal{H})$ exist if dim($\mathcal{H}$)>2.

=--

+-- {: .num_remark}
###### Remark

If a valuation _did_ exist and was restricted to a [[poset of commutative subalgebras|commutative sub-algebra of operators]], it would be an element of the [[Gelfand spectrum]] of the commutative sub-algebra.  Since such elements _do_ exist, valuations do exist on any commutative sub-algebra of operators even if not on the whole _non_-commutative algebra, $\mathcal{B}(\mathcal{H})$, of all bounded operators.  Isham calls these valuations on commutative subalgebras _local_. In the [[Bohr topos]] of the algebra of observables (see there for more), the local valuations are just the [[internal language|internal]] valuations.

=--

## Sheaf-theoretic interpretation

[[Chris Isham]] and [[Jeremy Butterfield]] gave a [[topos theory|topos theoretic]] reformulation of the Kochen-Specker theorem as follows.

+-- {: .num_defn}
###### Definition
**(category of contexts)**

Let $\mathcal{V}(\mathcal{H})$ be a [[category]] (the [[poset of commutative subalgebras]] of the algebra $B(\mathcal{H})$ of [[bounded operator]]s) whose

* [[object]]s are _commutative_ [[von Neumann algebra|von Neumann subalgebras]] $V \subset B(\mathcal{H})$;

* [[morphism]]s $V_1 \to V_2$ are inclusions $V_1 \subset V_2$.

=--

Isham calls this the **category of (classical) contexts** of $B(\mathcal{H})$.
Each commutative algebra is viewed as a context within which to view a quantum system in an essentially classical way in the sense that the physical quantities in any such algebra can be given consistent values (as they can in a classical context). These classical contexts were maybe first amplified by [[Niels Bohr]] as being the contexts through which all of [[quantum mechanics]] is to be perceived. (Therefore the word "[[Bohr topos]]" for the concept that is meant to formalize this perspective of Bohr.)

+-- {: .num_defn}
###### Definition
**(spectral presheaf)**

Let $\Sigma : \mathcal{V}(\mathcal{B})^{op} \to Set$ be the [[presheaf]] on the category of contexts such that

* to $V \subset B(\mathcal{H})$ it assigned the set underlying the 
  spectrum of $V$: the set of multiplicative [[linear functional]]s 
  $\kappa : V \to \mathbb{R}$;

* to an inclusion $i : V_1 \hookrightarrow V_2$ it assigns the corresponding 
  function $i^* : \Sigma(V_2) \to \Sigma(V_1)$ that sends a functional
  $V_2 \stackrel{\kappa}{\to} \mathbb{R}$ to its restriction
  $V_1 \hookrightarrow V_2 \stackrel{\kappa}{\to} \mathbb{R}$.

This is called the _[[spectral presheaf]]_.

=--


Recall that the [[terminal object]], $* = 1_{Set^{\mathcal{V}(\mathcal{H})^{op}}}$ in the [[category of presheaves]] on $\mathcal{V}(\mathcal{H})$ is the [[presheaf]] that assigns the singleton set $*$ (the [[terminal object]] in [[Set]]) to each commutative algebra.  

A [[global element]] of the spectral presheaf $\Sigma$ is a morphism $e : * \to \Sigma$ in the presheaf topos. Being a [[natural transformation]] of functors, such a global element $\lambda : 1_{Set^{\mathcal{V}(\mathcal{H})^{op}}} \to \underline{\Sigma}$ of the spectral presheaf, would associate an element of the [[Gelfand spectrum]] of an algebra $V$ to that algebra such that all local valuations are global, i.e. for $V \subseteq W$ valuations on $V$ are local valuations on $W$ but global on $V$.  

Because a multiplicative linear functional $\kappa : V \to\mathbb{R}$ satisfies the axioms of a valuation, def. \ref{Valuation}, when restricted to the self-adjoint elements of $V$.

By the Kochen-Specker theorem these cannot exist, hence a global element of $\Sigma$ cannot exist. Hence we have:

+-- {: .num_prop}
###### Proposition
(Hamilton, Isham, Butterfield)

The Kochen-Specker theorem is equivalent to the statement that the [[spectral presheaf]] $\Sigma$ of the algebra of bounded operators has no [[global elements]] if the dimension of the Hilbert space is greater than 2.

=--

([Butterfield-Hamilton-Isham 98](#ButterfieldHamiltonIsham))

For more see at _[[Bohr topos]]_.

## Related theorems

Other theorems about the foundations of [[quantum mechanics]] include:

* [[order-theoretic structure in quantum mechanics]]

  * [[Gleason's theorem]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[Bell's theorem]]

* [[Wigner theorem]]

* [[Bub-Clifton theorem]]


## Related concepts

* [[beable]]

* [[quantum contextuality]]

* [[Bohr topos]]

* [[interpretation of quantum mechanics]]

  * [[hidden variable theory]]

* [[Bell's inequalities]]


Other theorems about the foundations and [[interpretation of quantum mechanics]] include:

* [[order-theoretic structure in quantum mechanics]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[Fell's theorem]]

* [[Gleason's theorem]]

* [[Wigner theorem]]

* [[Bell's theorem]]

* [[Bub-Clifton theorem]]

* [[Kadison-Singer problem]]


## References

The original article:

* {#KochenSpecker67} [[Simon Kochen]], [[Ernst Specker]], _The problem of hidden variables in quantum mechanics_, Journal of Mathematics and Mechanics **17** (1967) 59-87 &lbrack;[pdf](http://www.iumj.indiana.edu/IUMJ/FTDLOAD/1968/17/17004/pdf), [jstor:24902153](https://www.jstor.org/stable/24902153), [doi:10.1007/978-94-010-1795-4_17](https://doi.org/10.1007/978-94-010-1795-4_17)&rbrack;

Relation to [[Bell's theorem]]:

* [[N. David Mermin]], *Hidden Variables and the Two Theorems of John Bell*, Reviews of Modern Physics **65** (1993) 803-815 &lbrack;[doi:10.1103/RevModPhys.65.803](https://doi.org/10.1103/RevModPhys.65.803), [arXiv:1802.10119](https://arxiv.org/abs/1802.10119)&rbrack;
  

Alternative proofs:

* Del Rajan, Matt Visser, _Kochen-Specker theorem revisited_ ([arXiv:1708.01380](https://arxiv.org/abs/1708.01380))

Review:

* Costantino Budroni, Adán Cabello, Otfried Gühne, Matthias Kleinmann, Jan-Åke Larsson, *Kochen-Specker Contextuality* &lbrack;[arXiv:2102.13036](https://arxiv.org/abs/2102.13036)&rbrack;



The [[sheaf and topos theory|sheaf-theoretic]] interpretation of the theorem was proposed in

* {#IshamButterfield98} [[Chris Isham]], [[Jeremy Butterfield]], _A topos perspective on the Kochen-Specker theorem: I. Quantum States as Generalized Valuations_ ([arXiv:quant-ph/9803055](http://arxiv.org/abs/quant-ph/9803055))
  

The formulation in terms of presheaves on the category of commutative sub-algebra of $B(\mathcal{H})$ was proposed in part III of

* {#ButterfieldHamiltonIsham} [[Jeremy Butterfield]], John Hamilton, [[Chris Isham]], _A topos perspective on the Kochen-Specker theorem_, 

  _I. quantum states as generalized valuations_, Internat. J. Theoret. Phys. 37(11):2669--2733, 1998, [MR2000c:81027](http://www.ams.org/mathscinet-getitem?mr=1669557), [doi](http://dx.doi.org/10.1023/A:1026680806775); 

  _II. conceptual aspects and classical analogues_ Int. J. of Theor. Phys. 38(3):827--859, 1999, [MR2000f:81012](http://www.ams.org/mathscinet-getitem?mr=1697983), [doi](http://dx.doi.org/10.1023/A:1026652817988); 

  _III. Von Neumann algebras as the base category_, Int. J. of Theor. Phys. 39(6):1413--1436, 2000, [arXiv:quant-ph/9911020](http://arxiv.org/abs/quant-ph/9911020), [MR2001k:81016](http://www.ams.org/mathscinet-getitem?mr=1788498),[doi](http://dx.doi.org/10.1023/A:1003667607842); 

  _IV. Interval valuations_, Internat. J. Theoret. Phys. __41__ (2002), no. 4, 613&#8211;639, [MR2003g:81009](http://www.ams.org/mathscinet-getitem?mr=1902067), [doi](http://dx.doi.org/10.1023/A:1015276209768)    


The original paper outlining [[Bell's theorem]]:

* [[John S. Bell]], *On the Einstein Podolsky Rosen Paradox*, Physics, [pdf](http://www.drchinese.com/David/Bell_Compact.pdf).

The original paper outlining [[Gleason's theorem]] is

* {#Gleason57} [[Andrew M. Gleason]], _Measures on the closed subspaces of a Hilbert space_, Journal of Mathematics and Mechanics,  Indiana Univ. Math. J. 6 No. 4 (1957), 885&#8211;893 ([web](http://www.iumj.indiana.edu/IUMJ/FULLTEXT/1957/6/56050))
  
A technical discussion on the interplay of [[Gleason's theorem|Gleason's]] and Kochen-Specker theorems and various issues regarding non-contextuality, locality and [[Bell's inequality]]: 

* [[Valter Moretti]], §5.1.2 of: *Fundamental Mathematical Structures of Quantum Theory: Spectral Theory, Foundational Issues, Symmetries, Algebraic Formulation*
Springer (2019) &lbrack;[doi:10.1007/978-3-030-18346-2](https://doi.org/10.1007/978-3-030-18346-2)&rbrack;

The hierarchy of strengths of no-go theorems in quantum context is studied from sheaf theoretic perspective in

* [[Samson Abramsky]], Adam Brandenburger, _The sheaf-theoretic structure of non-locality and contextuality_, [arxiv/1102.0264](https://arxiv.org/abs/1102.0264)

Strengthening of the Kochen-Specker theorem and relation to the "[[free will theorem]]":

* [[Simon Kochen]], *On the Free Will Theorem* &lbrack;[arXiv:2207.06295](https://arxiv.org/abs/2207.06295)&rbrack;

  > The new theorem &lbrack;...&rbrack; does require any use of free will on the experimenter’s part. The theorem also strengthens the Kochen-Specker Theorem

Relation of Kochen-Specker to [[Bell's inequalities]]:

* [[Leandro Aolita]], Rodrigo Gallego, Antonio Acín, Andrea Chiuri, Giuseppe Vallone, Paolo Mataloni, Adán Cabello, *Fully nonlocal quantum correlations*, Phys. Rev. A **85** 032107 (2012) &lbrack;[arXiv:1105.3598](https://arxiv.org/abs/1105.3598), [doi:10.1103/PhysRevA.85.032107](https://doi.org/10.1103/PhysRevA.85.032107)&rbrack;

[[!redirects Kochen-Specker theorems]]

[[!redirects Bell-Kochen-Specker theorem]]
[[!redirects Bell-Kochen-Specker theorems]]


[[!redirects free will theorem]]


