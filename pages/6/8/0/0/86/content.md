<div class="rightHandSide toc">
[[!include physicscontents]]
</div>



#Idea#

BV theory is the answer to the second of two different questions:

 * **Hamiltonian BFV**: taking quotients of constraint surfaces in [[Poisson manifold]]s by group actions and more generally by the foliation determined by first class constraints;

 * **Lagrangian BV**: integrating forms over [[NQ-supermanifolds]].

##Hamiltonian BFV## 

The F is for Fradkin.
In this context, the BFV-complex is a [[homological resolution]] of the problem of taking quotients of symplectic manifolds by group actions. 

+-- {: .query}

_Question_: Can you explain more about this? What do you mean by a "homological resolution of the problem"? Is there a nice example? I went over the [blog entry](http://golem.ph.utexas.edu/category/2008/07/poisson_reduction.html) but it seemed to talk about symplectic/Poisson reduction in its own right and didn't yet make the link with the BV formalism. (Bruce)

(Jim)  Thanks, Bruce.  My initial edit here is just to set the record straight - BV $\neq$ BFV. Will expand further and try to answer your query.

=--

See [[homological resolution]].

+-- {: .query}

_Comment_: Kevin Costello is preparing a [book](http://www.math.northwestern.edu/~costello/renormalization) on _Renormalization of quantum field theories_, available on his webpage. He has a section entitled _The BV construction as symplectic reduction_ [](http://www.math.northwestern.edu/~costello/chap3.pdf#page=7). Could you somehow link your explanation to that in some way?

_Urs says:_ I have (only) a vague hunch that Lagrangian and Hamiltonian BV are related in some way by "holography" of sorts, in a way that explains why the master equation in Lagrangian BV -- $\Delta exp(S) = 0$ -- looks like a Schr&ouml;dinger equation if one re-interprets the space of histories with the space of states of a system of one dimension higher. Some very useful observations in this regard are in S.L. Lyakhovich, A.A. Sharapov,
_Quantization of Donaldson-Uhlenbeck-Yau theory_
[arXiv](http://arxiv.org/abs/0705.1871), which I talk about at the end of [this](http://golem.ph.utexas.edu/category/2007/08/lyakhonov_and_sharapov_on_qft.html).

(Jim)  I would hope they were related by a homological version of the usual Hamiltonian - Lagrangian correspondence.

=--


### Poisson/symplectic reduction ###

 * _Basics of Poisson reduction_ ([blog](http://golem.ph.utexas.edu/category/2008/07/poisson_reduction.html))

 * Alejandro Cabrera, _Homological BV-BRST methods: from QFT to Poisson reduction_ ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Charla_IMPA_BRST.pdf))

 * J. Butterfield, _On symplectic reduction in classical mechanis_ ([pdf](http://philsci-archive.pitt.edu/archive/00002373/01/ButterfieldNHSympRed.pdf))


### Homological interpretation of BV-Poisson reduction

* Jim Stasheff, _Homological Reduction of Constrained Poisson Algebras_ ([arXiv](http://arxiv.org/abs/q-alg/9603021))

* Jim Stasheff, _The (secret?) homological algebra of the Batalin-Vilkovisky approach_ ([arXiv](http://arxiv.org/abs/hep-th/9712157))

The latter is NOT in a Poisson context, any more than Lagrangians are only for symplectic manifolds.

##Lagrangian BV## 

###Idea###

* Lagrangian BV-formalism is a means to describe 
[[integration over supermanifolds]] for [[NQ-supermanifolds]] given by $L_\infty$-[[Lie infinity-algebroid|algebroid]]s.
  +-- {: .query}
  Maybe nowadays?, but not originally.  It was meant for
  Lagrangians with symmetries.
  =--
  (Recall that in the physics literture the function algebra of these [[NQ-supermanifolds]] is addressed as the [[BRST complex]].)



The path integral in quantum field theory is supposed to be the integral over a space $X$ of field configurations
using a measure $d\mu_S$ which is conceived in the form
$$
  \mu_S(\phi) = \exp(\frac{i}{\hbar} S(\phi)) \mu(\phi)
  \;\;\;\;
  \phi \in X
  \,,
$$
for $\mu$ some other measure and $S : X \to \mathbb{R}$ the _action functional_.

If one thinks of $X$ as an ordinary $(d \lt \infty)$-dimensional smooth manifold, $d\mu_S$ will be given by a volume form, $\mu_S \in \Omega^d(X)$. By contraction of multivector fields with forms, every choice of volume form on $X$ induces an isomorphism between differential forms and multivectors
$$
  \mu : \Omega^\bullet(X) \stackrel{\simeq}{\to}
  \wedge^{-\bullet} \Gamma(T X)
  \,,
$$
which is usefully thought of as reversing degrees. Under this isomorphism the deRham differential maps to a divergence operator conventionally denoted
$$
  \mu : d \mapsto \Delta
$$
which interacts naturally with the canonical bracket on multivector fields: the [Schouten bracket](http://en.wikipedia.org/wiki/Schouten-Nijenhuis_bracket)
This idea can be found recalled for instance on p.3 of Willwacher, Calaque [Formality of cyclic cochains](http://arxiv.org/PS_cache/arxiv/pdf/0806/0806.4095v2.pdf#page=3).

The point to notice now is

* if we think of 

  * the measure $\mu$ as some closed reference differential form on $X$;

  *  the exponentiated action functional $exp(\frac{i}{\hbar}S(-))$ as a multivector field on $X$;

  * the expression $exp(\frac{i}{\hbar}S(-)) \mu$ as the contraction of this multivector field with $\mu$

* then the **BV quantum master equaton**
$\Delta \exp(\frac{i}{\hbar}S) = 0$ says nothing but that
$exp(\frac{i}{\hbar}S(-)) \mu$ is a _closed differential form_.

* If we furthermore take into account that in the presence of gauge symmetries the space $X$ is not a plain manifold but the $L_\infty$-[[Lie infinity-algebroid|algebroid]] of the gauge symmetries acting on the space of fields, hence an [[NQ-supermanifold]] (whose Chevalley-Eilenberg algebra is the **BRST complex**), then this just says that $\exp(\frac{i}{\hbar}S) \mu$ is an [[integration over supermanifolds|integrable form]] in the sense of [[integration over supermanifolds|integration theory of supermanifolds]].

This means that Lagrangian BV formalism is nothing but a way of describing closed differential forms on $L_\infty$-[[Lie infinity-algebroid|algebroid]]s in terms of multivectors contracted into a reference differention form. The multivectors dual to degree 0 elements in the $L_\infty$-[[Lie infinity-algebroid|algebroid]] are the so-called "**anti-fields**", while those dual to the higher degree elements are the so-called "**anti-ghosts**".

###Examples###

See [[examples for Lagrangian BV]].


### Relation to groupoid cardinality ###

There ought to be a close relation between the 
integration over $L_\infty$-[[Lie infinity-algebroid|algebroid]]s using BV-formalism and the notion of [[groupoid cardinality]]
for finite groupoids, which was recently generalized to 
a notion of [[volume of a Lie groupoid]].



#Literature#

A comprehensive recent review is

* Carlo Albert, Bea Bleile and J&#252;rg Fr&#246;hlich, _Batalin-Vilkovisky Integrals in Finite Dimensions_ ([arXiv](http://eprintweb.org/S/article/math-ph/0812.0464))

Other introductions include


* D. Fiorenza, An introduction to the Batalin-Vilkovisky formalism, Lecture given at the Recontres Math&#233;matiques de Glanon, July 2003. ([arXiv](http://arxiv.org/abs/math/0402057))

*  A. Cattaneo, From Topological Field Theory to Deformation Quantization and Reduction, ICM 2006. ([pdf](http://www.math.uzh.ch/fileadmin/math/preprints/icm.pdf))

*  M. B&auml;chtold, On the finite dimensional BV formalism, 2005. ([pdf](http://www.math.uzh.ch/reports/04_05.pdf))



The interpretation of the BV quantum master equation as a description of closed differential forms acting as measures on infinite-dimensional spaces of fields is described in

* E. Witten, 
_A note on the antibracket formalism_
Modern Physics Letters A, 5 7, 487--494
([scan](http://ccdb4fs.kek.jp/cgi-bin/img_index?9004090))




#Related entries#

* [[homotopy BV algebra]]

#Further discussion#

We had a discussion of some aspects of BV-formalism over at the $n$-Category Caf&eacute; at [Frobenius Algebras and the BV Formalism](http://golem.ph.utexas.edu/category/2008/11/frobenius_algebras_and_the_bv.html).


[[!redirects BV-theory]]