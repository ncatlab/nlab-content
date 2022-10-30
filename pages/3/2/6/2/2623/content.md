
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Idea

One way to make sense of the [[path integral]] used for [[quantization]] of [[classical field theory]] to [[quantum field theory]] is to _define_ it as a resummation of the the [[Feynman perturbation series]] of [[Feynman diagram]]s. 

But for a generic [[action functional]] this prescription produces in each term of this series an ill-defined diverging term. _Renormalization_ is a process of _adjusting_ the [[action functional]] such that the [[classical field theory]] remains the same, but while at the same time adding interactions whose effect is to counteract these divergences to yield a series that is termwise finite. The terms for these extra interactions in the [[action functional]] are therefore called **counterterms**.

A well-developed method for renormalization, described in more detail below, expresses each of the terms in the perturbation series as a [[Laurent series]] in a certain parameter which is divergent at the parameter value of interest. In this description the process of renormalization corresponds to discarding the poles of this series.

The precise way in which this Laurent series is constructed has recently been understood to have an elegant desciption in terms of [[Hopf algebra]] and is now known as _Hopf algebraic renormalization_ .


## St&#252;ckelberg-Bogoliubov-Epstein-Glaser renormalization

(...)

## BPHZ Hopf-algebraic renormalization 

### The phenomenon 

In the study of [[perturbative quantum field theory]] one is concerned with functions -- called _amplitudes_ -- that take a collection of graphs -- called [[Feynman graph]]s -- to [[Laurent polynomial]]s in a complex variable $z$ -- called the **(dimensional) regularization parameter** --

$$
  Amplitude : CertainGraphs \to LaurentPolynomials
$$

and wishes to extract a "meaningful" finite component when evaluated at vanishing regularization parameter $z = 0$. 

A prescription -- called **renormalization scheme** -- for adding to a given amplitude in a certain recursive fashion further terms -- called **counterterms** -- such that the resulting modified amplitude -- called the **renormalized amplitude** -- is finite at $z=0$ was once given by physicists  and is called the **BPHZ-procedure** .

This procedure justifies itself mainly through the remarkable fact that the numbers obtained from it match certain numbers measured in particle accelerators to fantastic accuracy.

### Its combinatorial Hopf-algebraic interpretation 

The combinatorial Hopf algebraic approach to perturbative quantum field theory, see for instance

* Hector Figueroa, Jose M. Gracia-Bondia, _Combinatorial Hopf algebras in quantum field theory I_ ([arXiv](http://arxiv.org/abs/hep-th/0408145)),

starts with the observation that the BPHZ-procedure can be understood 

* by noticing that there is secretly a natural [[group]] structure on the collection of amplitudes;

* which is induced from the fact that there is secretly a natural [[Hopf algebra]] structure on the vector space whose basis consists of graphs;

* and with respect to which the BPHZ-procedure is simply the [[Birkhoff decomposition]] of group valued functions on the circle into a divergent and a finite part.

The Hopf algebra structure on the vector space whose basis consists of graphs can be understood most conceptually in terms of [[pre-Lie algebra|pre-Lie algebras]].

### The Connes-Kreimer theorem 

A [[Birkhoff decomposition]] of a loop $\phi : S^1 \to G$ in a complex group $G$ is a continuation of the loop to 

* a [[holomorphic function]] $\phi_+$ on the standard disk inside the circle;

* a holomorphic function $\phi_-$ on the complement of this disk in the projective [[complex plane]]

* such that on the unit circle the original loop is reproduced as

  $$
    \phi = \phi_+ \cdot (\phi_-)^{-1}
    \,,
  $$

  with the product and the inverse on the right taken in the group $G$. 

  Notice that by the assumption of holomorphicity $\phi_+(0)$ is a well defined element of $G$.



+-- {: .un_theorem}
###### Theorem
**(Connes-Kreimer)**

1. If $G$ is the group of [[character]]s on any graded connected commutative [[Hopf algebra]] $H$ 

   $$
    G = Hom(H,\mathbb{C})
   $$ 

   then the Birkhoff decomposition always exists and is given by the formula
 
   $$
    \phi_- :  (X \in H) \mapsto Counit(X) 
          -
        PolePartOf(
             Product(\phi_- \otimes \phi) 
            \circ (1 \otimes (1 - Counit)) 
         \circ Coproduct (X)
        ) 
    \,.
   $$

1. There is naturally the structure of a [[Hopf algebra]], $H = Graphs$, on the graphs considered in [[quantum field theory]]. As an algebra this is the free commutative algebra on the "1-particle irreducible graphs". Hence QFT amplitudes can be regarded as characters on this Hopf algebra.

 

1. The BPHZ renormalization-procedure for amplitudes is nothing but the first item applied to the special case of the second item.
 
=--

+-- {: .proof}
###### Proof

The proof is given in 

* [[Alain Connes]], [[Dirk Kreimer]], _Renormalization in quantum field theory I_ ([arXiv](http://arxiv.org/abs/hep-th/9912092))

=--



### The Hopf-algebra perspective on QFT

This result first of all makes [[Hopf algebra]] an organizational principle for (re-)expressing familiar operations in [[quantum field theory]].

Computing the renormalization $\phi_+$ of an amplitude $\phi$ amounts to using the above formula to compute the counterterm $\phi_-$ and then evaluating the right hand side of

$$
  \underbrace{\phi_+}_{renormalized amplitude} = \underbrace{\phi}_{amplitude} \underbrace{\cdot}_{convolution product} \underbrace{\phi_-}_{counterterm}
  \,,
$$

where the product is the group product on characters, hence the [[convolution product]] of characters.

Every elegant reformulation has in it the potential of going beyond mere reformulation by allowing to see structures invisible in a less natural formulation. For instance [[Dirk Kreimer]] [claims](http://golem.ph.utexas.edu/category/2007/03/recent_developments_in_quantum.html#c010903) that the Hopf algebra language allows him to see patterns in perturbative quantum gravity previously missed.

### Gauge theory and BV-BRST with Hopf algebra

Walter von Suijlekom is thinking about the Hopf-algebraic formulation of [[BV theory|BRST-BV methods]] in nonabelian [[gauge theory]] 

In his nicely readable 

* [[Walter von Suijlekom]], _Renormalization of gauge fields using Hopf algebra_, ([arXiv](http://arxiv.org/abs/0801.3170)) 

he reviews the central idea: the [[BRST]] formulation of [[Yang-Mills theory]] manifests itself at the level of the resulting _bare_ i.e. unnormalized amplitudes in certain relations satisfied by these, the **Slavnov-Taylor identities** .

Renormalization of gauge theories is consistent only if these relations are still respected by renormalized amplitudes, too. We can reformulate this in terms of Hopf algebra now:

the relations between amplitudes to be preserved under renormalization must define a [[Hopf ideal]] in the Hopf algebra of graphs. 

Walter von Suijlekom proves this to be the case for Slavnov-Taylor in his [theorem 9 on p. 12](http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3170v1.pdf#page=12)

As a payoff, he obtains a very transparent way to prove the generalization of **Dyson's formula** to nonabelian gauge theory, which expresses renormalized Green's functions in terms of unrenormalized Green's functions "at bare coupling". This is his [corollary 12 on p. 13](http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3170v1.pdf#page=12).

In the context of [[BV theory|BRST-BV quantization]] these statements are subsumed, he says, by the structure encoded in the Hopf ideal which corresponds to imposing the BV-master equation.  See also

* W. van Suijlekom: _Representing Feynman graphs on BV-algebras_ , ([arXiv](http://arxiv.org/abs/0807.0999))

## Related concepts

* [[perturbation theory]]

* **renormalization**

## References {#References}

### General
 {#General}

A solid mathematical formulation of perturbation theory and renormalization has been given in

* K. Hepp.: _Th&#233;orie de la Renormalisation_ Lect. Notes in Phys. Springer (1969)

A review is in

* [[R. E. Borcherds]], _Renormalization and quantum field theory_, [arxiv/1008.0129](http://arxiv.org/abs/1008.0129) 

A modern mathematical account relativing to [[BV-BRST formalism]] is in 

* [[Kevin Costello]], _Renormalization and Effective Field Theory_ AMS (2011) ([publisher webpage](http://www.ams.org/publications/authors/books/postpub/surv-170))

with precursors in 

* [[Kevin Costello]], _Renormalisation and the Batalin-Vilkovisky formalism_ ([arXiv:0706.1533](http://arxiv.org/abs/0706.1533))

### In AQFT

A discussion of renormalization in the context of [[AQFT]], as well as a detailed comparison of major renormalization schemes is in

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_  Commun.Math.Phys.208:623-661 (2000) ([arXiv](http://arxiv.org/abs/math-ph/9903028))


* [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_ Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](http://arxiv.org/abs/0901.2038))


### Hopf algebraic BPHZ formulation

* [[Alain Connes]], [[Dirk Kreimer]], _Renormalization in quantum field theory and the Riemann-Hilbert problem. I. The Hopf algebra structure of graphs and the main theorem_, Comm. Math. Phys. __210__ (2000), no. 1, 249&#8211;273, [hep-th/9912092](http://arxiv.org/abs/hep-th/9912092), [MR2002f:81070](http://www.ams.org/mathscinet-getitem?mr=1748177), [doi](http://dx.doi.org/10.1007/s002200050779), _II. The $\beta$-function, diffeomorphisms and the renormalization group_, Comm. Math. Phys. __216__ (2001), no. 1, 215--241; [hep-th/0003188](http://arxiv.org/abs/hep-th/0003188), [MR2002f:81071](http://www.ams.org/mathscinet-getitem?mr=1748177), [doi](http://dx.doi.org/10.1007/PL00005547)

An introduction and review to the Hopf-algebraic description of renormalization is in 

* Christian Brouder, _Quantum field theory meets Hopf algebra_ ([arxiv:hep-th/0611153](http://de.arxiv.org/abs/hep-th/0611153))

A textbook treatment is

* [[Dirk Kreimer]], _Knots and Fenyman diagrams_ , Cambridge Lecture Notes in Physics. 13. Cambridge: Cambridge University Press.
* Joseph C. Varilly, _The interface of noncommutative geometry and physics_, [hep-th/0206007](http://arxiv.org/abs/hep-th/0206007)  

Some heavywheight automated computations using this formalism are discussed in 

* D. J. Broadhurst, [[Dirk Kreimer]], _Renormalization automated by Hopf algebra_ ([arXiv:hep-th/9810087](http://arxiv.org/abs/hep-th/9810087))

### Operadic description

* [[Jean-Louis Loday]], Nikolay M. Nikolov, _Operadic construction of the renormalization group_ ([arXiv:1202.1206](http://arxiv.org/abs/1202.1206))


[[!redirects renormalizable]]
[[!redirects renormalizable theory]]

[[!redirects Hopf-algebraic renormalization]]
