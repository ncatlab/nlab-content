
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

String theory is a [[theory (physics)|theory]] in fundamental [[physics]].

Below we indicate the basic idea and provide pointers to further details. See also the _[[string theory FAQ]]_.


### Conceptually: String perturbation theory from QFT worldline formalism

_Perturbative string theory_ is something at least close to a [[vertical categorification|categorification]] of the following description of _[[perturbation theory|perturbative]] [[quantum field theory]]_ in terms of sums over [[Feynman diagrams]].

Recall that in [[quantum field theory]] one approach to make sense of the [[path integral]] is the _[[perturbation series]] expansion_,  which interprets the path integral for the [[scattering amplitudes]] (the _[[S-matrix]]_) as a certain sum over [[graphs]] of certain numbers assigned to each [[graph]].

The graphs are called _[[Feynman diagrams]]_, the numbers assigned to them are called _([[renormalization|renormalized]]) [[scattering amplitudes]]_ and the sum over graphs of (renormalized) amplitudes is the _[[perturbation series]]_ or [[S-matrix]].

The amplitude assigned to a single graph with $n$ external edges is interpreted as the amplitude for $n$ "quanta" or "[[particles]]" of the [[field (physics)|fields]] in question to interact in the way indicated by the graph. 

Crucial for the motivation of the idea of string theory is the observation that this (renormalized) amplitude assigned to a graph is itself the _correlator_ of a 1-dimensional quantum field theory on that graph: the "worldline quantum field theory" describing the (relativistic) quantum mechanics of these particles. This is usually a [[sigma-model]] with parameter space the given graph and target space the spacetime on which the fields live for which the perturbation series computes the path integral.

When made explicit this is called the _[[worldline formalism]]_ for computing the quantum field perturbation series. (See there for more details.)

The premise of perturbative string theory is to replace the [[perturbation series]] over correlators of a 1-d QFT over graphs by a sum of correlators of a 2-dQFT over 2-dimensional surfaces -- called _[[worldsheets]]_ and hence produce an [[S-matrix]] this way. Again in simple cases this 2d QFT is a [[sigma-model]] whose target is the spacetime in which one computes interactions. 

In analogy to the previous case, one thinks of the amplitude assigned this way to a surface as the amplitude for the boundary arcs -- the _string_s -- to interact in the way given by the surface.

Some of the motivations for considering this replacement of  graphs by surfaces have been the following:

* the 2-d correlators are better behaved in that they don't have to be renormalized. The "counterterms" appearing in renormalization of ordinary QFT can be identified with contributions to the correlators that come from the linear extension of the strings (see the above reference for more on this);

* there are fewer choices involved: a Feynman graph is really a decorated graph with the decoration from some more or less arbitrary index set, describing the nature of the particles associated with a given edge and the nature of the interaction associated with a given vertex. In the sum over surfaces there is no extra decoration (except on the boundary of the surfaces) and one finds that instead a single string diagram (a 2d QFT correlator for a given surface) encodes already a sum over (infinitely) many particle species decorations and all possible interaction decorations for them;

* while there are fewer choices to be made by hand, it turns out that the effective particle content that does arise automatically from this prescription happens to be structurally of the kind one would hope for: the massless effective particles described by the string perturbation series happen to be _gauge bosons_, _fermions_ charged under them, and, notably, _graviton_s. This is structurally exactly the [[Yang-Mills theory]] input of the [[standard model of particle physics]] combined with perturbative [[quantum gravity]] that one would hope to see.

These aspects have motivated the impression that the string perturbation series might be considerably closer to the true formalism of fundamental physics than ordinary perturbative quantum field theory. This impression is however offset by the following problems:

* while the worldsheet 2d QFT whose correlators are summed over surfaces are themselves much easier to handle than the full target space quantum physics they are used to encode, a fully complete and rigorous theory of 2d QFT is available only in simple special cases. 

* In particular, even though there are fewer arbitrary choices involved in the string perturbation series as compared to the ordinary Feynman perturbation series, one crucial choice still present is that of this worldsheet 2d QFT. By the above, every choice of worldsheet QFT (called a choice of "vacuum") corresponds to a choice of effective target space geometry (to be thought of as the one that the perturbation series computes the quantum perturbations about) and particle content (see [[2-spectral triple]] for more on that). One would therefore like to understand the space of all worldsheet QFTs whose effective target space geometry and particle content is close to the one experimentally observed. After many years of rather na&#239;ve approaches to handle or not to handle this, it has more recently at least come to the general attention that there is something to be better understood here.

* More fundamentally, already the role of the original perturbation series in quantum field theory is actually not fully understood. Its main success is the observation that truncating or resumming the perturbation series in a more or less ad hoc way, it does yield values that very well describe a plethora of real world measurements.  One imagines that there is a _non-perturbative_ definition of [[quantum field theory]] such that in certain well-defined circumstances the perturbation series does yield an approximation to it and is _a posteriori_ justified. If so, there should be an analogous nonperturbative definition of string theory. There is a large ratio of speculations as to what that might be over solid results about it.

### Phenomenologically
 {#IdeaPhenomenology}

While therefore the premise of perturbative string theory is conceptually suggestive for various reasons, there is to date no connection to experimental [[phenomenology]] (apart from the fact that conceptual insights into string theory have helped analyze quantum field theoretic data, see at _[[string theory results applied elsewhere]]_). As a result much of the substantial outcome of string theory research is more in [[mathematical physics]] (if done well, at least), exploring the general theory space of [[quantum field theories]] and their [[UV-completions]], than in realistic [[model (in theoretical physics)|model building]] (though there is no lack of trying), where it remains very speculative. This has led to public or semi-public debates about the value of string theory for actual physics. See at _[[criticism of string theory]]_ for pointers.




## Critical string theories and quantum anomalies
 {#CriticalStringsAndQuantumAnomalies}

The [[action functional]] for the [[string]]-[[sigma model]] in general has a [[quantum anomaly]] of both kinds:

1. For both the bosonic string and the superstring the corresponding [[Polyakov action]] has a [gauge anomaly]() for the [[conformal field theory|conformal symmetry]], depending on the [[dimension]] $d$ of [[target space]], and on the strength of the [[dilaton]] background field. For vanishing dilaton field this anomaly vanishes exactly for $d = 26$ for the bosonic model, and in $d = 10$ for the [[superstring]]. 

   For target spaces of these dimensions one speaks of **critical string theory**. In as far as string theory is expected to have relevance for physics at all, it is usually expected to be in this critical dimension. But also noncritical string models can and have been considered.

1. Apart from the gauge anomaly, the [[action functional]] of the [[string]]-[[sigma-model]] also in general has an _[anomalous action functional](http://ncatlab.org/nlab/show/quantum+anomaly#AnomalousActionFunctional)_ , for two reasons:

   1. The [[holonomy|higher holonomy]] of the higher [[background gauge field]]s is in general not a function, but a [[section]] of a [[line bundle]];

   1. The fermionic [[path integral]] over the [[worldsheet]]-[[spinor]]s of the [[superstring]] produces as section of a [[Pfaffian line bundle]].

   In order for the action functional to be well-defined, the [[tensor product]] of these different anomaly [[line bundle]]s over the bosonic [[configuration space]] must have trivial class (as [[connection on a bundle|bundles with connection]], even). This gives rise to various further anomaly cancellation conditions:

   1. For the [[heterotic string]] (necessarily closed) the anomaly cancellation condition is known as the _[[Green-Schwarz mechanism]]_ : it says that the background fields of [[gravity]] and [[B-field]] must organize to a [[twisted differential string structure]] whose twist is given by the background [[Yang-Mills field]].

   1. For the open [[type II string]] the condition is known as the [[Freed-Witten anomaly cancellation]] condition: it says that the restriction of the [[B-field]] to any [[D-brane]] must consistute the twist of a [[twisted spin^c structure]] on the brane.

      A more detailed analysis of these type II anomalies is in ([DFMI](#DFMI)) and ([DFMII](#DFMII)).

      See also _[[Diaconescu-Moore-Witten anomaly]]_.
## Subtopics


### Ingredients

* [[quantum field theory]]

* [[sigma-model]], 

  * [[2d CFT]], [[2d SCFT]], [[2-spectral triple]]

    * [[Dirac-Ramond operator]]

    * [[Witten genus]]

    * [[Gepner model]], [[flop transition]]

  * [[world sheets for world sheets]]

* [[perturbation theory]]

  * [[string scattering amplitude]], [[S-matrix]]

* [[effective QFT|effective background QFT]]

  * [[gravity]], [[supergravity]], [[Yang-Mills theory]], [[quantum gravity]]

  * [[quantum anomaly]]

  * [[twisted smooth cohomology in string theory]]

### Critical string models

* [[heterotic string theory]]

  * [[Green-Schwarz mechanism]], [[differential string structure]],

  * [[dual heterotic string theory]]

    * [[differential fivebrane structure]]

  * [[Witten genus]], [[string orientation of tmf]]

* [[type II string theory]]

  * [[type II geometry]]

  * [[elliptic genus]]

  * [[Diaconescu-Moore-Witten anomaly]]

* [[little string theory]]

* [[Kaluza-Klein mechanism]]

  * [[double dimensional reduction]]

  * [[moduli stabilization]]

  * [[flux compactification]]

  * [[landscape of string theory vacua]]

* [[string field theory]]

* [[duality in string theory]]

  * [[T-duality]], [[mirror symmetry]]

  * [[S-duality]], [[electric-magnetic duality]]

  * [[U-duality]]

  * [[open/closed string duality]]

    * [[AdS/CFT]], [[holographic principle]]

    * [[KLT relations]]

* [[11-dimensional supergravity]], [[M-theory]]

  * [[Ho?ava-Witten theory]]

### Extended objects

* [[brane]]

* **[[D-brane]]**

  * [[D0-brane]], [[D2-brane]], [[D4-brane]]

  * [[D1-brane]], [[D3-brane]], [[D5-brane]]

  * [[RR-field]], [[differential K-theory]]

* [[black brane]]

  * [[black holes in string theory]]

* **[[NS-brane]]**

  * [[string]], [[sigma-model]]

    * [[spinning string]], [[superstring]]

    * [[B2-field]]

  * [[NS5-brane]]

    * [[B6-field]]

* **[[M-brane]]**

  * [[M2-brane]]

    * [[C3-field]]

    * [[ABJM theory]], [[BLG model]]

  * [[M5-brane]]

    * [[C6-field]]

    * [[6d (2,0)-supersymmetric QFT]]


[[!include table of branes]]


### Elliptic genera, elliptic cohomology and tmf
  {#EllipticGenera}

> A properly developed theory of [[elliptic cohomology]] is likely to shed some light on what string theory really means. ([Witten 87, very last sentence](#Witten87))

The [[large volume limit]] of the [[partition function]] of the [[superstring]] on a given [[target space|target]] [[spacetime]] is an [[elliptic genus]] of that manifold ([Witten 87](#Witten87)), the _[[Witten genus]]_ (see there for more). 

Since the [[Witten genus]] in turn is the [[decategorification]] of the [[string orientation of tmf]], this suggests that [[tmf]]-[[generalized (Eilenberg-Steenrod) cohomology]] classifies full string theories, in refinement of how the classification of [[D-brane charge]] (just the [[boundary conditions]] for [[open strings]]) is given by [[K-theory]]. 

A non-trivial conistency check of this idea is announced in ([Nikolaus 14](#Nikolaus14)).
 
### Topological strings

* [[A-model]], [[B-model]]


### String phenomenology

* [[string phenomenology]]

  * [[G2-MSSM]]

### String theory results applied elsewhere

Beyond the speculative hypothetized role of string theory as a theory behind observed [[particle physics]], the theory has shed light on many aspects of [[quantum field theory]], both on the conceptual structure of quantum field theory as such as well as on concrete theories and their concrete properties. Some of these string theory results enter crucially in computations that are used to interpret particle physics experiments such as the [[LHC]].

For more see

* [[string theory results applied elsewhere]]

## References

### General

A large body of references is organized at the

* [String Theory Wiki](http://www.stringwiki.org/w/index.php?title=String_Theory_Wiki)

For another list of literature see the entry

* [[books about string theory]].

A useful survey of the status of string theory as a theory of [[quantum gravity]] is in

* [[Matthias Blau]], _String theory as a theory of quantum gravity -- A status report_ Talk at _[Quantum theory and Gravitation](http://www.conferences.itp.phys.ethz.ch/doku.php?id=qg11:programme)_ Z&#252;rich (2011) ([pdf](http://www.conferences.itp.phys.ethz.ch/lib/exe/fetch.php?media=qg11:zurichblau.pdf))

An article summarizing information about [[cohomology|cohomological]] models for aspects of string theory and listing plenty of useful further references is

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_

A book trying to summarize the state of the art of capturing mathematical structures fundamental to the definition of perturbative string theory is

* [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_

### Technical details

#### Elliptic genera, elliptic homology and tmf

The [[partition function]] of the [[superstring]] was understood to be an [[ellkiptic genus]] (the [[Witten genus]]) in 

* {#Witten87} [[Edward Witten]],  _Elliptic Genera And Quantum Field Theory_ , Commun.Math.Phys. 109 525 (1987) ([Euclid](http://projecteuclid.org/euclid.cmp/1104117076))

A nontrivial consistency check on the suggestion that this means that string backgrounds are classified in [[tmf]] is given in

* {#Nikolaus14} [[Thomas Nikolaus]], _[[T-Duality in K-theory and Elliptic Cohomology]]_, talk at _String Geometry Network Meeting_, Feb 2014, ESI Vienna ([website](http://www.ingvet.kau.se/juerfuch/conf/esi14/esi14_34.html))

#### Quantum anomalies


Discussion of type II [[quantum anomalies]] is in 

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))
 {#DFMI}

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Spin structures and superstrings_ ([arXiv:1007.4581](http://arxiv.org/abs/1007.4581))
  {#DFMII} 

Discussion of [[superstring]] [[perturbation theory]] is in 

* [[Edward Witten]], _Superstring Perturbation Theory Revisited_ ([arXiv:1209.5461](http://arxiv.org/abs/1209.5461))

### Fields medal work induced by string theory

Pure [[mathematics]] work which came out of string theory and was awared with a [[Fields medal]] includes the following.

* [[Edward Witten]]'s medal in 1990

* [[Maxim Kontsevich]]'s medal in 1998

(...)

(see behind the name links for more...)

[[!redirects string theories]]

[[!redirects superstring theory]]
[[!redirects superstring theories]]

[[!redirects string perturbation series]]
[[!redirects perturbative string theory]]