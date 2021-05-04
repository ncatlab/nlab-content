
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[string theory]] the term _swampland_ had been introduced ([Vafa 05](#Vafa05)) to publicly highlight the basic fact that many [[effective quantum field theory]] [[vacuum state|vacua]] will not admit a [[UV-completion]] to a [[string theory vacuum]], hence that admitting a completion to a [[string theory vacuum]] is a strong constraint, hence that [[string theory]] predicts many more conditions to be satisfied by [[gauge groups]], [[field (physics)|field content]] and [[coupling constants]] than predicted by plain [[quantum field theory]].

The terminology was motivated since the collection of [[string theory vacua]] had previously come to be called the _[[landscape of string theory vacua]]_. The idea is to imagine the remaining [[effective field theory|EFTs]] not "in" this landscape to form a space "away from the landscape", whence the colorful imagery of a swampland.

More in detail, there is supposedly a map

\[
  \label{PointParticleLimitMap}
  \text{String Vacua}
  \overset{\;\;ppl\;\;}{\longrightarrow}
  \text{effective QFT Vacua}
\]

that takes [[string theory vacua]] to their low-energy approximation by [[vacuum state|vacua]] of [[effective quantum field theories]]. One way to possibly formalize this is to take the point-particle limit (ppl) of [[2d SCFTs]] to obtain [[spectral triples]] (as discussed at _[[2-spectral triple]]_) taking [[string]] [[worldsheets]] to [[Feynman diagrams]]:

<img src="https://ncatlab.org/nlab/files/PointParticleLimitOfStringDiagram.png" width="300">

> graphics grabbed from [Schubert 96](worldline+formalism#Schubert96)

Then with language of [[homological algebra]] or more generally of [[category theory]] we may begin to formalize the situation as follows:

1. the [[domain]] of (eq:PointParticleLimitMap) is the [[landscape of string theory vacua]];

1. the [[image]] of (eq:PointParticleLimitMap) is the landscape of corresponding [[effective quantum field theories|eQFTs]] that admit stringy [[UV-completion]];

1. the [[cokernel]] of (eq:PointParticleLimitMap) is the _swampland_;

1. the [[kernel]] of (eq:PointParticleLimitMap), or more generally its [[fiber]] over any [[effective quantum field theory|EFT]], is the space of different choices of stringy [[UV-completion]] of the same [[effective quantum field theory]].

Making this fully precise requires saying more about what the [[domain]] and [[codomain]] in (eq:PointParticleLimitMap) actually are, and in which ambient [[category]] (they will be some kind of [[moduli stacks]] in an ambient [[(∞,1)-category]] which may not quite be [[stable (∞,1)-category|stable]], whence "[[cokernel]]" may need to be interpreted in a non-abelian sense; but such details don't change the general idea here).

For example, part of what it means to specify a [[string theory vacuum]] is to declare the [[D-brane charge]] contained in this vacuum (subject to [[RR-field tadpole cancellation]] against [[O-plane]]-charges). In actual [[string theory]] this [[RR-field]] [[charge]] is supposed to be (see [there](D-brane#ReferencesKTheoryDescription)) a [[cocycle]] in some flavour of [[topological K-theory]] ([[twisted K-theory|twisted]] [[equivariant K-theory|equivariant]] [[differential K-theory|differential]] [[KR-theory]]), while its image in the underlying [[effective field theory]] is in the corresponding flavour of [[ordinary cohomology]]/[[de Rham cohomology]]. The map that relates the two incarnations of RR-field charge is the _[[Chern character]]_, which is what formalizes the map (eq:PointParticleLimitMap) in in the D-brane charge "sector" of the theory

$$
  \array{
    \text{String Vacua}
    &\overset{\;\;ppl\;\;}{\longrightarrow}&
    \text{effective QFT Vacua}
    \\
    \left\{
    \array{
      \text{D-brane RR-charge}
      \\
      \text{in K-theory}
    }
    \right\}
    &\overset{\text{Chern character}}{\longrightarrow}&
    \left\{
    \array{
      \text{flux forms in}
      \\
      \text{ordinary cohomology}
    }
    \right\}
  }
$$

The [[Chern character]] in general does have non-trivial [[cokernel]] ("swampland RR-fields") and [[kernel]] (choices of [[UV-completion]] of the effective RR-fields). In fact it fits not just in a [[short exact sequence]], but in the [[differential cohomology hexagon]] (see there for more) of [[K-theory]].

<center>
<img src="https://ncatlab.org/nlab/files/CohomotopySwampland.jpg" width="700">
</center>

> graphics grabbed from [SS 18](#SS18)

In contrast to this example, the literature on the "swampland" phenomenon is currently dominated by informal hand-wavy arguments. Starting with [Ooguri-Vafa 06](#OoguriVafa06) is an attempt to guess semi-precise rules-of-thumb for recognizing [[effective field theory|EFTs]] in the swampland, now known as the _swampland conjectures_. Motivated by the re-opening of the question whether [[de Sitter spacetime]] actually appears in [[string theory vacua]] or not ([Danielsson-van Riet 18](#DanielssonVanRiet18)), these swampland conjecture currently revolve around bounds on the [[cosmological constant]] in relation to [[scalar fields]] in the theory.

An argument that much of the existing swampland literature does not even live up to the level of rigour of [[folklore]] string theory, and in fact that it is fundamentally flawed, is made in [Banks 19](#Banks19).


## Swampland conjectures
 {#SwamplandConjectures}

The following list of statements have come (around 2020-2021) to be widely discussed in a sector of the [[string phenomenology]] community which associates with the "swampland" imagery. They are now commonly referred to and known as  "conjectures", specifically "the swampland conjectures", but the terms used tend to remain vague/undefined and may change their intended meaning with context (not the least the notion of "state in quantum gravity", which however in most of these statements really means: classical solitonic [[black brane]]-solution in some [[supergravity]]-theory -- e.g. in Conj. \ref{ElectricWeakGravityConjecture}). 

But some of these statements have been interpreted in special cases as more precise statements about [[moduli spaces]] of [[Calabi-Yau manifolds]], and in this form they may be closer to [[conjectures]] in the sense of established sense of [[mathematics]].


### No global symmetries conjecture

\begin{conjecture}
A theory coupled to [[gravity]] must have no global symmetries, which means that they are either broken or gauged. 
\end{conjecture}

This includes global $p$-form symmetries as well as global discrete symmetries. 

### Completeness hypothesis

\begin{conjecture}
A [[gauge theory]] coupled to [[gravity]] must contain physical states with all possible gauge charges consistent with [[Dirac charge quantization]].
\end{conjecture}

\begin{remark}
This immediately implies that any continuous [[gauge group]] (i.e. a [[Lie group]]) must be [[compact]].
However, this does not restrict discrete gauge groups, which can be non-compact (e.g. [[duality]] groups).
\end{remark}

### BPS completeness hypothesis

\begin{conjecture}
If a given charge can be populated by [[BPS states]], then the physical spectrum must contain a BPS state with this charge.
\end{conjecture}

### Weak gravity conjecture

#### Electric weak gravity conjecture

\begin{conjecture}\label{ElectricWeakGravityConjecture}
Given a $U(1)$-[[gauge theory]] weakly coupled to [[gravity]] with [[gauge coupling]] $g$, there exists an electrically charged state with mass $m$ and charge $q$ satisfying

$$ m \leq \sqrt{2} g q M_p, $$

where $M_p$ is the [[Planck mass]].
\end{conjecture}

#### Magnetic weak gravity conjecture

\begin{conjecture}
Given a $U(1)$-[[gauge theory]] weakly coupled to [[gravity]] with [[gauge coupling]] $g$, The cutoff scale $\Lambda$ of the [[effective field theory]] is bounded from above by the [[gauge coupling]] as

$$ \Lambda \leq g M_p^{(d-2)/2}, $$

where $M_p$ is the [[Planck mass]] and $d$ is the [[dimension]].
\end{conjecture}

#### Convex hull weak gravity conjecture

(...)

#### Sublattice (or tower) weak gravity conjecture

(...)

### Swampland distance conjecture

\begin{terminology}
Consider the [[moduli space]] $\mathcal{M}$ of a theory coupled to [[gravity]], which is parametrized by the expectation values of some field $\phi^i$ that has no [[potential]]. Starting from any point $P \in \mathcal{M}$ there always exists another point $Q \in \mathcal{M}$ such that their [[geodesic distance]] $d(P,Q)$ is infinite. This is called *infinite field distance limit*.
\end{terminology}

\begin{example}
The decompactification limit in compactified [[string theory]] is the standard example of infinite field distance limit.
\end{example}

\begin{conjecture}
There exists an infinite tower of states with a mass scale $M$ that becomes exponentially light at any infinite field distance limit as

$$ M(Q) \sim M(P)e^{-c d(P,Q)}, $$

where $c$ is a positive constant.
\end{conjecture}

### Emergent string conjecture

\begin{conjecture}
Any infinite field distance limit is either 
 
* a decompactification limit, or

* a limit in which a weakly coupled string becomes tensionless.

\end{conjecture}

This is a refinement of the *swampland distance conjecture* which explicits the nature of the tower of states.

### AdS distance conjecture

\begin{conjecture}
Any [[AdS]] [[vacuum]] has an infinite tower of states that becomes light in the flat spacetime limit $\Lambda\rightarrow 0$, satisfying

$$ m\sim|\Lambda|^c, $$

where $c$ is a constant.
\end{conjecture}

### AdS instability conjecture

\begin{conjecture}
Any [[non-supersymmetric vacuum]] is at best metastable (and eventually has to decay).
\end{conjecture}

### dS conjecture

\begin{conjecture}
The scalar potential $V$ of an [[effective field theory]] weakly coupled to gravity must satisfy the following bound on its derivatives:

$$ |\nabla V| \geq \frac{c}{M_p}V, $$

where $c\sim\mathcal{O}(1)$ is positive.
\end{conjecture}

The dS conjecture was further refined as it follows.

\begin{conjecture}
The previous bound needs to be imposed only if the condition 
$$ \mathrm{min}(\nabla_i\nabla_j V) \leq -\frac{c'}{M_p^2}V, $$
for some $c'\sim\mathcal{O}(1)$, on the second derivative of the potential is violated.
\end{conjecture}

Thanks to this refinement, only proper dS minima are excluded and not general critical points.

### Transplanckian censorship conjecture

(...)

### Asymptotic dS conjecture

\begin{conjecture}
The scalar potential $V$ of an [[effective field theory]] weakly coupled to [[gravity]] presents a runaway behavior when approaching an infinite field distance point, i.e.

$$ |\nabla V| \geq c V, $$

where $c\sim\mathcal{O}(1)$.
\end{conjecture}

This is an asymptotic version of the *dS conjecture*.

### Swampland cobordism conjecture
 {#SwamplandCobordismConjecture}

From [McNama & Vafa 17](#McNamaVafa17):

\begin{conjecture}\label{OriginalSwamplandCobordismConjecture}
For any [[quantum gravity]] theory [[KK-compactification|compactified]] on a $d$-dimensional internal manifold, some kind of "quantum-gravity version" of a [[cobordism group]] must vanish in degree $d$. In heuristic symbols:

$$ \Omega^{\mathrm{QG}}_d = 0. $$
\end{conjecture}

\begin{remark}
A rigorous discussion of a possible role of [[cobordism cohomology]] in [[M-theory]], assuming [[schreiber:Hypothesis H]], is in [Sati & Schreiber 21a](#SatiSchreiber21a); for relation to discussion of Conj. \ref{OriginalSwamplandCobordismConjecture} see [p. 83](https://arxiv.org/pdf/2103.01877.pdf#page=83) there.
\end{remark}


## References

### General

The terminology "swampland", in the context of [[string phenomenology]], originates with:

* {#Vafa05} [[Cumrun Vafa]], _The String Landscape and the Swampland_ ([arXiv:hepth/0509212](http://arxiv.org/abs/hepth/0509212))

Review and lecture notes:

* [[Eran Palti]], _The Swampland: Introduction and Review_, lecture notes ([arXiv:1903.06239](https://arxiv.org/abs/1903.06239))

* Marieke van Beest, José Calderón-Infante, Delaram Mirfendereski, Irene Valenzuela, _Lectures on the Swampland Program in String Compactifications_ ([arXiv:2102.01111](https://arxiv.org/abs/2102.01111))


Further discussion:

* {#OoguriVafa06} [[Hirosi Ooguri]], [[Cumrun Vafa]], _On the Geometry of the String Landscape and the Swampland_, Nucl.Phys.B766:21-33, 2007 ([arXiv:hep-th/0605264](https://arxiv.org/abs/hep-th/0605264))

* {#BrennanCartaVafa17} T. Daniel Brennan, Federico Carta, [[Cumrun Vafa]], _The String Landscape, the Swampland, and the Missing Corner_ ([arXiv:1711.00864](https://arxiv.org/abs/1711.00864))

* [[Ben Heidenreich]], [[Matthew Reece]], [[Tom Rudelius]], _Emergence and the Swampland Conjectures_ ([arXiv:1802.08698](https://arxiv.org/abs/1802.08698))

* Hee-Cheol Kim, Houri-Christina Tarazi, [[Cumrun Vafa]], _Four Dimensional $\mathcal{N}=4$ SYM and the Swampland_ ([arXiv:1912.06144](https://arxiv.org/abs/1912.06144))

See also 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Swampland_(physics)">Swampland_(physics)</a>_

Beware that the landscape literature is presently dominated by non-rigorous hand-wavy [[string phenomenology]]:

* {#Banks19} [[Tom Banks]], _On the Limits of Effective Quantum Field Theory: Eternal Inflation, Landscapes, and Other Mythical Beasts_ ([arxiv:1910.12817](https://arxiv.org/abs/1910.12817))

  from pages 14-22:

  > these considerations lead to conclusions at odds with the seemingly similar arguments of $[$ the [[swampland conjectures]] $]$. $[\cdots]$  Perturbative moduli space completely distorts the true nature of the class of consistent models.

  > It’s important to realize that the entire procedure just outlined for finding (meta) stable AdS minima of a non-perturbative effective potential is purely hypothetical and has no basis in well founded string theory calculations. $[\cdots].$ 

  > The hypothesis of the String Landscape is entirely based on low energy effective field theory ideas about finding "vacua" by minimizing an effective potential.  Everything that’s been said above indicates that this idea has no validity in genuine models of quantum gravity. $[\cdots]$

  > The most serious issue,  in  my  opinion,  is  the  contention  that  one  can  make  the  AdS  radius  much  larger  thanthe size of the compact manifold.  All well established examples of large radius AdS/CFT havea compact manifold of dimension 2 or greater whose radius is comparable to that of the AdSspace.  In Appendix A we’ll present an argument based on the properties of AdS black holes,that this is in fact necessary.

  > The next step in the construction of "realistic" models involves "adding an anti-brane to break supersymmetry and make the c.c.  positive".  This is supposed to be a small modification of the model, calculable in low energy effective field theory, and that seems manifestly incorrect. $[\cdots]$.

  > even if one believes that the construction of meta-stable dS models is reliable, there is no clear argument about  what  the  proper  observables  of  the  model  are  nor  that different  dS  constructions are part of the same model.  Neither is there an interpretation of these correlators as transition amplitudes in a quantum mechanical model. $[\cdots]$

  > The conclusion  that  effective  field  theorists  should  draw  from  this is that unlike super-symmetric string models in flat or AdS space-time, many of which have at least perturbative definitions as mathematical models obeying the axioms of quantum mechanics, all literature on the String Landscape is speculation based on the unfounded notion that all string models with a given amount of SUSY are part of one single model and that it makes sense to define an effective action that encompasses all string models. Every single non-perturbative construction of string models contradicts this claim $[\cdots]$

Identification of the swampland charge structure with the [[cokernel]] of the [[Chern character]]:

* {#SS18} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Lift of fractional D-brane charge to equivariant Cohomotopy theory|Lift of fractional D-brane charge to equivariant Cohomotopy theory]]_ ([arXiv:1812.09679](https://arxiv.org/abs/1812.09679), [Python code](https://arxiv.org/src/1812.09679v1/anc))


### de Sitter vacua

On the question whether [[de Sitter spacetime]]-[[vacua]] belong to the [[swampland]] or not:

* {#DanielssonVanRiet18} [[Ulf Danielsson]], [[Thomas Van Riet]],  _What if string theory has no de Sitter vacua?_, International Journal of Modern Physics D, Vol. 27, No. 12, 1830007 (2018)  ([arXiv:1804.01120](https://arxiv.org/abs/1804.01120), [doi:10.1142/S0218271818300070](https://doi.org/10.1142/S0218271818300070))

* {#vanRiet18} [[Thomas Van Riet]], _Is dS space in the Swampland_, talk at [StringPheno18](http://sp18.fuw.edu.pl/) ([pdf slides](http://sp18.fuw.edu.pl/wp-content/uploads/participants-database/thomasvanriet.pdf))

* {#vanRiet18a} [[Thomas Van Riet]], _Status of KKLT_, talk at _[Simons summer workshop 2018](http://scgp.stonybrook.edu/archives/24870)_ ([recording](http://scgp.stonybrook.edu/video_portal/video.php?id=3730))

* {#ObiedOoguriSpodyneikoVafa18} Georges Obied, [[Hirosi Ooguri]], Lev Spodyneiko, [[Cumrun Vafa]], _De Sitter Space and the Swampland_ ([arXiv:1806.08362](https://arxiv.org/abs/1806.08362))

* {#AgrawalObiedSteinhardtVafa18} Prateek Agrawal, Georges Obied, Paul Steinhardt, [[Cumrun Vafa]], _On the Cosmological Implications of the String Swampland_ ([arXiv:1806.09718](https://arxiv.org/abs/1806.09718))

* {#Vafa18} [[Cumrun Vafa]], _Cosmology and the String Swampland_, talk at _[Strings 2018](https://indico.oist.jp/indico/event/5/)_ ([pdf slides](https://indico.oist.jp/indico/event/5/picture/96.pdf), [recording](https://www.youtube.com/watch?v=fU8sJRCRz24&t=1904s))

* [[Frederik Denef]], Arthur Hebecker, Timm Wrase, _The dS swampland conjecture and the Higgs potential_ ([arXiv:1807.06581](https://arxiv.org/abs/1807.06581))

* {#Danielsson18} [[Ulf Danielsson]], _The quantum swampland_ ([arXiv:1809.04512](https://arxiv.org/abs/1809.04512))

  (argues that the issue with [[string theory|stringy]] de Sitter [[moduli stabilization]] raised in [Sethi 17](#Sethi17) is related to the de Sitter instability seen in QFT, according to the references [above](de+Sitter+spacetime#InPerturbativeQuantumGravity))


* Georges Obied, [[Hirosi Ooguri]], Lev Spodyneiko, [[Cumrun Vafa]], _De Sitter Space and the Swampland_ ([arXiv:1806.08362](https://arxiv.org/abs/1806.08362))


* Jakob Moritz, Ander Retolaza, Alexander Westphal, _On uplifts by warped anti-D3-branes_ ([arXiv:1809.06618](https://arxiv.org/abs/1809.06618))

* Iosif Bena, Emilian Dudas, Mariana Graña, Severin Lüst, _Uplifting Runaways_ ([arXiv:1809.06861](https://arxiv.org/abs/1809.06861))

* [[Clay Cordova]], G. Bruno De Luca, [[Alessandro Tomasiello]], _Classical de Sitter Solutions of Ten-Dimensional Supergravity_ ([arXiv:1812.04147](https://arxiv.org/abs/1812.04147))

On  [[de Sitter spacetime]] [[cosmology]] realized in [[brane world models]] in ambient $\sim$[[anti de Sitter spacetime|AdS]]-[[bulk]] [[spacetime]]:

* {#BDDGS18} Souvik Banerjee, [[Ulf Danielsson]], Giuseppe Dibitetto, Suvendu Giri, Marjorie Schillo, _Emergent de Sitter cosmology from decaying AdS_ ([arXiv:1807.01570](https://arxiv.org/abs/1807.01570))

* Souvik Banerjee, [[Ulf Danielsson]], Giuseppe Dibitetto, Suvendu Giri, Marjorie Schillo, _de Sitter Cosmology on an expanding bubble_ ([arXiv:1907.04268](https://arxiv.org/abs/1907.04268))


Discussion in the context of [[M-theory on G2-manifolds]]:

* Beatriz de Carlos, Andre Lukas, Stephen Morris, _Non-perturbative vacua for M-theory on G2 manifolds_, JHEP 0412:018, 2004 ([arxiv:hep-th/0409255](https://arxiv.org/abs/hep-th/0409255))

  which concludes that with taking [[non-perturbative effects]] from [[membrane instantons]] into account one gets 4d vacua with vanishing and negative [[cosmological constant]] ([[Minkowski spacetime]] and [[anti-de Sitter spacetime]]) but not with positive [[cosmological constant]] ([[de Sitter spacetime]]). They close by speculating that [[M5-brane]] instantons might yield [[de Sitter spacetime]].


* Johan Blåbäck, [[Ulf Danielsson]], Giuseppe Dibitetto, Suvendu Giri, _Constructing stable de Sitter in M-theory from higher curvature corrections_ ([arXiv:1902.04053](https://arxiv.org/abs/1902.04053))

  which suggests that including [[higher curvature corrections]] makes it work


* Iosif Bena, Alex Buchel, Severin Lüst, _Throat destabilization (for profit and for fun)_ ([arxiv:1910.08094](https://arxiv.org/abs/1910.08094))



[[!include swampland cobordism conjecture -- references]]




[[!redirects swampland conjecture]]
[[!redirects swampland conjectures]]


[[!redirects swampland cobordism conjecture]]

