
{:quote: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

String field theory is supposed to be something like a  [[quantum field theory]] which is the [[second quantization]] of the [[string]] in [[string theory]], following this analogy:

[[!include second quantization -- table]]


Recall that [[string theory|perturbative string theory]] is a higher dimensional version of the Feynman [[perturbation series]] in [[quantum field theory]]. This Feynman perturbation series may be understood as computing the path integral over the Lagrangian of the given quantum field theory. _String field theory_ is the attempt to identify this Lagrangian description corresponding to the string perturbation series.

So string field theory is the attempt to complete the following analogy:

Feynman perturbation series : QFT Lagrangian  :: String perturbation theory : String field theory .

### Motivation

The original hope was that string field theory would be a way to embed the string perturbation series prescription into a more coherent non-perturbative framework. 

### Achievements
 {#Achievements}

The most detailed insight that has come out of the study of string field theory is the full understanding of the role of the "tachyon" field in bosonic perturbative string theory. In the bosonic version of the theory one of the excitations of the string is a quantum that appears to have imaginary mass. Such "tachyonic" quanta appear in ordinary field theory when the perturbation series is developed around an extremum of the QFT action functional that is not a local minimum, but a local maximum: it indicates that the  classical configuration around which the perturbation series computes the quantum corrections is dynamically unstable and time evolution will tend to evolve it to the next local minimum. In the perturbative quantum description the movement to the next local minimum manifests itself in the _condensation_ (as in [[Bose-Einstein condensate|Bose-Einstein condensation]]) of the tachyon field. This is called _tachyon condensation_.

Shortly after its conception it was suspected that the tachyon that appears in the perturbation theory of the bosonic string is similarly an indication that the bosonic string's perturbation series has to be understood as being a perturbation about a local maximum of some action functional. String field theory aimed to provide that notion of action functional. And indeed, in bosonic string field theory one has a kind of higher action functional and may compute the "tachyon potential" that it implies. It indeed has a local maximum at the point about which the ordinary bosonic string perturbation series is a perturbative expansion, while a local minimum is foun nearby. 

[[Ashoke Sen]] conjectured the statement -- now known as _[[Sen's conjecture]]_ -- that the depth of this tachyon potential, i.e. the energy density difference between this local maximum and this local minimum corresponds precisely to the energy density of the space-filling [[D25-brane]] that is seen in [[perturbative string theory]]. This would mean that the condensation of the bosonic string's tachyon corresponds to the decay of the unstable space-filling D25 brane. 

The detailed quantitative confirmation of Sen's conjecture has been one of the main successes of string field theory. In the course of this a detailed algebraic description of the "true closed bosonic string vacuum", i.e. of the theory at that local tachyon potential minimum has been found. However, the algebraic expressions involved tend to be hard to handle in their complexity.

There are numerical indications that indeed as the D25-brane decays, the remaining vacuum contains (only) closed strings. See the [references below](#BosonicStringVacuumAndSenConjecture).

### Shortcomings

The shortcoming of the current development of string field theory can probably be summarized as follows:

* it has been studied as a theory of a _classical_ action functional. Little is known about the true quantum effects of the string field theory action functional.

* the best understanding exists for bosonic open string field theory, while closed and supersymmetric string field theory has remained much less accessible.

### In terms of higher category theory

Closed string field theory is governed by an [[L-infinity algebra]] of interactions, open string field theory by an [[A-infinity algebra]] and open-closed string field theory by a mixture of both: an [[open-closed homotopy algebra]].

## Bosonic open string field theory

(...)

## Bosonic closed string field theory

So far string field theory is defined in terms of an [[action functional]]. So, strictly speaking, it is defined as a [[classical field theory]]. The corresponding [[BV-BRST formalism|quantum master action]] is known, but apart from that not much detail about the [[quantization]] of this action has been considered in the literature.


### The interaction terms

The unrestricted [[configuration space]] of string field theory is the subcomplex of the [[BRST complex]] of the closed ([[superstring|super]]-)[[string]], regarded as a $\mathbb{N}$-[[graded vector space]] with respect to the ghost number grading, on those elements $\Psi$ that satisfy

1. $(b_0 - \bar b_0) \Psi = 0$;

1. $(L_0 - \bar L_0) \Psi = 0$ ("level matching condition"),


We shall write $\mathfrak{g}$ for this graded vector space. See ([Markl, section 1](#Markl))

This is equipped for each $k \in \mathbb{N}$ with a $k$-ary operation

$$
  [-,\cdots,-]_k : \mathfrak{g}^{\otimes k} \to \mathfrak{g}
$$

given by the [[correlator|(k+1)-point function]] of the string (the amplitude for $k$ closed strings coming in and merging into a single outgoing string). For $k = 1$ this is the [[BRST complex|BRST operator]]

$$
  [-]_1 = d_{BRST}
  \,.
$$

These operations are graded-symmetric: for all $\{\Psi_j\}$ of homogeneous degree $deg \Psi_j$ and for all $0 \leq i \lt k$ we have

\[
  \label{GradedSymmetrykBracket}
  [\Psi_1 , \cdots, \Psi_i, \Psi_{i+1}, \cdots, \Psi_k]_k
  =
  (-1)^{(deg \Psi_i)(deg \Psi_{i+1})}
  [\Psi_1 , \cdots, \Psi_{i+1}, \Psi_{i}, \cdots, \Psi_k]_k .
\]

([Zwiebach, (4.4)](#Zwiebach93)).

Moreover, there is a bilinear [[inner product]]

$$
  \langle -,- \rangle : \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{C}
$$

coming from the [[Hilbert space]] inner product of string states ([Zwiebach (2.60)](#Zwiebach93)). This is non-degenerate on elements $\Psi$ which are annihilated by the [[BRST complex|ghost]] operator 

$$
  b_0^- := b_0 - \bar b_0
$$

in that for all $A \in \mathfrak{g}$ with  $b_0^- A = 0$ we have

\[
  \label{NonDegeneracyOfInnerProduct}
  (\forall B \in \mathfrak{g} \,:\,
  \langle A,B\rangle = 0)
  \Rightarrow
  A = 0  
  \,.
\]

This is ([Zwiebach 93, (2.61)](#Zwiebach93)).


The inner product satisfies for all $\Psi_1, \Psi_2$ of homogeneous degree the relation

\[
  \label{GradedSymmetryBilinearPairing}
  \langle \Psi_1 , \psi_2 \rangle
  = 
  (-1)^{(deg \Psi_1 + 1) (deg \Psi_2 + 1)}
  \langle \Psi_2, \Psi_1 \rangle
\]

([Zwiebach 93, (2.50)](#Zwiebach93)).


Moreover, it is non-vanishing only on pairs of elements of total degree 5. ([Zwiebach 93, (2.31)(2.44)](#Zwiebach93)).

From this one constructs the $(n+1)$-point functions

\[
  \label{CorrelationFunctions}
  \{ \Psi_0, \Psi_1, \cdots, \Psi_k \}
  :=
  \langle \Psi_0, [\Psi_1, \cdots, \Psi_k]_k \rangle
  \,.
\]

These are still graded-symmetric in all arguments: for all $\{\Psi_j\}$ of homogeneous degree $deg \Psi_j$ and all $0 \leq i \lt k$ we have

\[
  \label{GradedSymmetrykPointFunction}
  \{\Psi_0, \cdots, \Psi_i, \Psi_{i+1}, \cdots, \Psi_k\}
  = 
  (-1)^{(deg \Psi_i)(deg \Psi_{i+1})}
  \{\Psi_0, \cdots, \Psi_{i+1}, \Psi_{i}, \cdots, \Psi_k\}
  \,.
\]

([Zwiebach 93, (4.36)](#Zwiebach93)).


### The action functional

+-- {: .num_defn #LabelConfigurationSpace}
###### Definition

The proper [[configuration space]] of string field theory is the sub-complex of the [[BRST complex]] of the closed ([[superstring|super]]-)[[string]] on those elements $\Psi$ for which

1. $(b_0 - \bar b_0) \vert\Psi\rangle = 0$;

1. $(L_0 - \bar L_0) \vert \Psi \rangle = 0$ ("level matching condition");

1. $\vert \Psi \rangle^\dagger = - (\langle \Psi \vert)$ ("reality");

1. $\vert \Psi\rangle$ is Grassmann even (...define...)

1. $ghostnumber \vert \Psi \rangle = 2$ (...define...)

=--

This is ([Zwiebach 93, (3.9)](#Zwiebach93))


The _[[action functional]]_ of closed string field theory is 

$$
  S : \Psi 
   \mapsto 
   \sum_{k = 1}^\infty
   \frac{1}{(k+1)!}
   \langle \Psi, [\Psi, \cdots, \Psi]_k\rangle
  \,.
$$

([Zwiebach 93, (4.41)](#Zwiebach93))


Since $[-]_1 = d_{BRST}$ is the [[BRST complex|BRST operator]] this starts out as

$$
  S : \Psi 
  = 
  \frac{1}{2}\langle \Psi , d_{BRST} \Psi \rangle
  + 
  \frac{1}{3} \langle \Psi, [\Psi, \Psi]_2\rangle
  + 
  \cdots
  \,.
$$

This immediately gives the [[equations of motion]] by variation with respect to $\Psi$ ([Zwiebach 93, (4.46)](#Zwiebach93)). The analogous statement for the [[superstring]] in in ([Sen 15 (2.22)](#Sen15)).


(See also at _[string theory FAQ -- What are the equations of string theory?](https://ncatlab.org/nlab/show/string+theory+FAQ#WhatAreTheEquations)_).


### As an $\infty$-Chern-Simons theory
 {#AsAnInfinityCSTheory}

The above action functional for closed string field theory turns out to have a general abstract meaning in [[higher category theory]]/[[homotopy theory]]. We spell out here how the action functional for closed string field theory is an example of an [[schreiber:∞-Chern-Simons theory]] in that it arises precisely as the [[Chern-Simons element]] of the binary pairing regarded as a binary [[invariant polynomial]] on the [[L-∞ algebra]] of string fields.

+-- {: .num_prop}
###### Proposition

The string [[BRST complex]] equipped with its $k$-ary interaction genus-0 interaction vertices  

$$
  (\mathfrak{g}, \{[-,\cdots,-]_k\})
$$ 

is an [[L-∞ algebra]].

=--

This is ([Zwiebach 93, (4.12)](#Zwiebach93)). For more details on the $L_\infty$-structure see _[References -- Relation to L-∞- and A-∞-algebra](ReferencesHomotopyAlgebra))_ .

+-- {: .num_prop}
###### Proposition

The inner product $\langle -,-\rangle$ satisfies the definition of a non-degenerate [[invariant polynomial]] on this $L_\infty$-algebra when restricted to fields of even degree as in def. \ref{LabelConfigurationSpace}.

=--

+-- {: .proof}
###### Proof

For simplicity of notation we discuss this as if $\mathfrak{g}$ were finite-dimensional. The argument for the infinite-dimensional case follows analogously.

Let $\{t_a\}$ be a [[basis]] of $\mathfrak{g}$ with dual basis $\{t^a\}$. Then the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ is generated from the $\{t^a\}$ with [[differential]] given by

$$
  d_{CE(\mathfrak{g})} 
   : 
  t^a
  \mapsto
  -
  \sum_{k = 1}^\infty
  \frac{1}{k!} [t_{a_1}, \cdots, t_{a_k}]_k \,\,
  t^{a_1} \wedge \cdots \wedge t^{a_k}
  \,.
$$

The [[Weil algebra]] $W(\mathfrak{g})$ is similarly generated from $\{t^a, r^a\}$ with differential

$$
  d_{W(\mathfrak{g})} 
   : 
  t^a
  \mapsto
  -
  \sum_{k = 1}^\infty
  \frac{1}{k!} [t_{a_1}, \cdots, t_{a_k}] \,\,
  t^{a_1} \wedge \cdots \wedge t^{a_k}
  + r^a
$$

and

$$
  d_{W(\mathfrak{g})} 
  : 
  r^a 
    \mapsto
  \sum_{k = 1}^\infty
  \frac{1}{k!}
  [t_{a_0}, t_{a_1}, \cdots, t_{a_k}]_{k+1}
  \,
  r^{a_0} \wedge t^{a_1} \wedge \cdots \wedge t^{a_k}
  \,.
$$

Write

$$
  P_{a b} := \langle t_a, t_b\rangle
$$

for the components of the bilinear pairing in this basis. By (eq:GradedSymmetryBilinearPairing) it follows that we can indeed regard

$$
  P_{a b} r^a \wedge r^b
  \in W(\mathfrak{g})
$$

as an element in the [[Weil algebra]] (since $deg r^a = deg t^a + 1$).

Therefore to see that this is an [[invariant polynomial]] it remains to check that it is $d_W$-closed. To see this, first introduce the notation

$$
  C_{a_0, \cdots, a_k} :=
  \{t_{a_0}, \cdots, t_{a_k}\}
$$

for the components of the $(k+1)$-point function (eq:CorrelationFunctions). Then compute

$$
  \begin{aligned}
     d_{W(\mathfrak{g})} P_{a b } r^a \wedge r^b
     & = 
     2 P_{a b} r^a \wedge 
     \left(
        \sum_{k = 1}^\infty
        [t_{a_1}, \cdots, t_{a_k}]_k
        \,
        r^{a_1} \wedge t^{a_2}\wedge \cdots \wedge t^{a_k}
     \right)
     \\
     & = 
     2 \sum_{k = 1}^\infty
     C_{a_0, a_1, \cdots, a_k}
     \,
     r^{a_0} \wedge r^{a_1} \wedge t^{a_2} \wedge \cdots \wedge t^{a_k}
  \end{aligned}
  \,.
$$

This expression vanishes term-by-term by the symmetry properties (eq:GradedSymmetrykPointFunction) when restricted to fields of even degree: by first switching the factors in the wedge product and then relabelling the indices we obtain

$$
  \begin{aligned}
  C_{a_0,  a_1, \cdots, a_k} r^{a_0} \wedge r^{a_1}
  &= 
  (-1)^{(deg t_{a_0} + 1)(deg t_{a_1} + 1) + (deg t_{a_0})(deg t_{a_1})}
  C_{a_0,  a_1, \cdots, a_k} r^{a_0} \wedge r^{a_1}
  \\
  & = 
  (-1)^{deg t_{a_0}  + deg t_{a_1} + 1}
  C_{a_0,  a_1, \cdots, a_k} r^{a_0} \wedge r^{a_1}
  \\
  & =
  (-1)
  C_{a_0,  a_1, \cdots, a_k} r^{a_0} \wedge r^{a_1}
  \end{aligned}
  \,,
$$

where in the last step we used the constraints on degrees given by def. \ref{LabelConfigurationSpace}.

This shows that $\langle-,-\rangle$ satisfies the defining equation of an invariant polynomial on the proper configuration space. The non-degeneracy is due to (eq:NonDegeneracyOfInnerProduct).

=--

From the discussion at [[Chern-Simons element]] in the section [Canonical Chern-Simons element](http://ncatlab.org/nlab/show/Chern-Simons+element#CanonicalChernSimonsElement) we have that the [[Lagrangian]] of the [[schreiber:infinity-Chern-Simons theory]] defined by the data $(\mathfrak{g}, \langle -,-\rangle)$ is

$$
  L : A \mapsto 
  \langle A,  d A\rangle
  + 
  \sum_{k = 1}^\infty
  \frac{2}{(k+1)!}
  \langle A , [A, \cdots , A]_k\rangle
$$

for $A$ a $\mathfrak{g}$-[[infinity-Lie algebroid valued differential form|valued differential form]] on some $\Sigma$. So the closed string field theory action looks like that of $\infty$-Chern-Simons theory over an odd-graded $\Sigma$.

## Open-Closed string field theory
 {#OpenClosedStringFieldTheory}

When considering open and closed strings jointly, then in addition to the closed string sector being encoded by an [[L-∞ algebra]] $\mathfrak{g}_{closed}$ as above, the open string sector is encoded in an [[A-∞ algebra]] $A_{open}$ and the former acts on the latter by homotopy [[derivations]] (see also at _[derivations on algebras over a dg-operad](derivation#OfAlgebrasOverADGOperad)_)

$$
  \mathfrak{g}_{closed} \longrightarrow Der (A_{open})
$$

([Kajiura-Stasheff 04](#KajiuraStasheff04), [Markl 04](#Markl04)).

Notice that this is half of the axioms of an $\infty$-[[Lie-Rinehart pair]].

## Superstring field theory
 {#SuperstringFieldTheory}

The maybe most wide-spread attempt to generalize the above to [[superstring]] field theory replaces the Chern-Simons-type action with a [[Wess-Zumino-Witten theory]]-type action, see at _[[WZW-type superstring field theory]]_ .

A formulation of superstring field theory more on line with the Chern-Simons type bosonic theory is proposed in ([Jurco-Muenster 13](#JurcoMuenster13)). See also the introduction there for a survey of the literature



## Related concepts

* [[schreiber:∞-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

  * [[2d Chern-Simons theory]]

  * [[3d Chern-Simons theory]]

  * [[4d Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[6d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

  * [[AKSZ sigma-models]]

  * [[infinite-dimensional Chern-Simons theory]]

Closed string field theory has been argued to arise from the [[dynamics]] of [[Wilson loops]] in the [[IKKT matrix model]] in ([Fukuma-Kawai-Kitazawa-Tsuchiya 97](#FukumaKawaiKitazawaTsuchiya97))




## References

### General


Introduction and survey:

* [[Leonardo Rastelli]], _String Field Theory_ in _Encyclopedia of Mathematical Physics_ ([arXiv:hep-th/0509129](http://arxiv.org/abs/hep-th/0509129))

* W. Siegel, _Introduction to string field theory_ ([arXiv:hep-th/0107094](http://arxiv.org/abs/hep-th/0107094))

* [[Ashoke Sen]], _String Field Theory as World-sheet UV Regulator_ ([arXiv:1902.00263](https://arxiv.org/abs/1902.00263))

* {#Erbin20a} [[Harold Erbin]], *String Field Theory – A Modern Introduction*, Lecture Notes in Physics **980**, Springer (2021) &lbrack;[arXiv:2301.01686](https://arxiv.org/abs/2301.01686), [doi:10.1007/978-3-030-65321-7](https://doi.org/10.1007/978-3-030-65321-7)&rbrack;

* {#Erbin20b} [[Harold Erbin]], _String theory: a field theory perspective_, 2020 ([pdf](http://www.lpthe.jussieu.fr/~erbin/files/reviews/string_theory.pdf))

* [[Harold Erbin]], _[String Field Theory -- Website](http://string-field-theory.org/)_

* [[Theodore Erler]], *Four Lectures on Closed String Field Theory*, Physics Reports **851** (2020) 1-36 &lbrack;[arXiv:1905.06785](https://arxiv.org/abs/1905.06785), [doi:10.1016/j.physrep.2020.01.003](https://doi.org/10.1016/j.physrep.2020.01.003)&rbrack

* Carlo Maccaferri, *String Field Theory*, in: *Oxford Research Encyclopedia of Physics* &lbrack;[arXiv:2308.00875](https://arxiv.org/abs/2308.00875)&rbrack;

* [[Ashoke Sen]], [[Barton Zwiebach]]: *String Field Theory: A Review*, in *[[Handbook of Quantum Gravity]]*, Springer (2023-) &lbrack;[arXiv:2405.19421](https://arxiv.org/abs/2405.19421), [doi:10.1007/978-981-19-3079-9](https://doi.org/10.1007/978-981-19-3079-9)&rbrack;





### Bosonic string field theory
 {#ReferencesBosonicSFT}


#### Open SFT
 {#ReferencesBosonocOSFT}

Original articles:

* {#Witten86} [[Edward Witten]], *Noncommutative Geometry and String Field Theory*, Nucl. Phys B **268** (1986) 253-294 &lbrack;<a href="https://doi.org/10.1016/0550-3213(86)90155-0">doi:10.1016/0550-3213(86)90155-0</a>&rbrack;

  > (cf. also [here](fusion+bundle#RelationToStringFieldTheory) at *[[fusion bundle]]*)
 

* [[Edward Witten]], _On background independent open string field theory_,  Phys.Rev. D46 (1992) 5467. ([arXiv:hep-th/9208027](http://arxiv.org/abs/hep-th/9208027))

See also

* Matej Kudrna, [[Martin Schnabl]], _Universal Solutions in Open String Field Theory_ ([arXiv:1812.03221](https://arxiv.org/abs/1812.03221))

On a proposal for a background-independent formalism for bosonic open string field theory, exhibiting in particular the [[orthosymplectic super Lie algebra|orthosymplectic group]] $OSp(d|2)$ as a symmetry:

* [[Itzhak Bars]], Dmitry Rychkov. *Background Independent String Field Theory* &lbrack;[arXiv:1407.4699](https://arxiv.org/abs/1407.4699)&rbrack;


#### Closed SFT
 {#ReferencesBosonicCSFT}

The fundamental work of Zwiebach on closed SFT is summed up in

* {#Zwiebach93} [[Barton Zwiebach]], *Closed string field theory: Quantum action and the Batalin-Vilkovisky master equation*, Nucl. Phys. B **390** 1 (1993) 33-152 &lbrack;[arXiv:hep-th/9206084](http://arxiv.org/abs/hep-th/9206084), <a href="https://doi.org/10.1016/0550-3213(93)90388-6">doi:10.1016/0550-3213(93)90388-6</a>&rbrack;
  

Brief reviews include

* [[Barton Zwiebach]], _Closed String Field Theory: An Introduction_ ([arXiv:hep-th/9305026](http://arxiv.org/abs/hep-th/9305026))

The explicit identification of the [[Einstein-Hilbert action]] for [[gravity]] coupled to the action for the [[B-field]] and the [[dilaton]] in the lowest orders of the CSFT action is discussed for instance in [Yang-Zwiebach, section 3.1](#YangZwiebach) and in

* Bang-Gui Liu, _General coordinate transformation and gravitational action from closed bosonic string field theory_, Class. Quantum Grav. 6 (1989)

* Masako Asano, Mitsuhiro Kato, _Closed string field theory in a-gauge_ ([arXiv:1206.3901](http://arxiv.org/abs/1206.3901))


Discussion of the expected closed string tachyon [[vacuum]] is in 

* {#YangZwiebach} Haitang Yang, [[Barton Zwiebach]], _A Closed String Tachyon Vacuum ?_, JHEP 0509:054,2005 ([arXiv:hep-th/0506077](http://arxiv.org/abs/hep-th/0506077))
 

* [[Nicolas Moeller]], Haitang Yang, _The nonperturbative closed string tachyon vacuum to high level_ ([arXiv:hep-th/0609208](http://arxiv.org/abs/hep-th/0609208))

* [[Nicolas Moeller]], _A tachyon lump in closed string field theory_ ([arXiv:0804.0697](http://arxiv.org/abs/0804.0697))

and further detailed analysis is in 

* [[Nicolas Moeller]], _Closed Bosonic String Field Theory at Quintic Order: Five-Tachyon Contact Term and Dilaton Theorem_, JHEP 0703:043,2007 ([arXiv:hep-th/0609209](http://arxiv.org/abs/hep-th/0609209))

* [[Nicolas Moeller]], _Closed Bosonic String Field Theory at Quintic Order II: Marginal Deformations and Effective Potential_, JHEP 0709:118,2007 ([arXiv:0705.2102](http://arxiv.org/abs/0705.2102))


### Superstring field theory
 {#ReferencesSuperstringFieldTheory}

The generalization to field theory for the [[superstring]], where [[picture number]] compliates the [[RR-field]]-sector, has (only) more recently seen considerable development, 

* Hiroshi Kunitomo, Yuji Okawa, _Complete action for open superstring field theory_, Prog. Theor. Exp. Phys. (2016) 023B01 ([arXiv:1508.00366](https://arxiv.org/abs/1508.00366))

A survey is in

* {#Okawa16} Yuji Okawa, _Recent developments in the construction of superstring field theory I_, 2016 ([pdf](http://www-het.ph.tsukuba.ac.jp/~ishibash/SFT16/okawa.pdf))

based on

* {#ErlerKonopkaSach13} [[Theodore Erler]], Sebastian Konopka, [[Ivo Sachs]], _Resolving Witten's Superstring Field Theory_, JHEP04(2014)150 ([arXiv:1312.2948](http://arxiv.org/abs/1312.2948))

* {#ErlerKonopkaSach14} [[Theodore Erler]], Sebastian Konopka, [[Ivo Sachs]], _NS-NS Sector of Closed Superstring Field Theory_, JHEP08(2014)158 ([arXiv:1403.0940](http://arxiv.org/abs/1403.0940))

* [[Ashoke Sen]], _Gauge Invariant 1PI Effective Superstring Field Theory: Inclusion of the Ramond Sector_ ([arXiv:1501.00988](https://arxiv.org/abs/1501.00988))

* [[Theodore Erler]], Sebastian Konopka, [[Ivo Sachs]], _Ramond Equations of Motion in Superstring Field Theory_ ([arXiv:1506.05774](https://arxiv.org/abs/1506.05774))

* {#Sen15} [[Ashoke Sen]], _BV Master Action for Heterotic and Type II String Field Theories_, JHEP02(2016)087 ([arXiv:1508.05387](http://arxiv.org/abs/1508.05387))

with further developments in

* Yuji Okawa, [[Barton Zwiebach]], _Heterotic String Field Theory_ ([arXiv:hep-th/0406212](http://arxiv.org/abs/hep-th/0406212))

* Roji Pius, [[Ashoke Sen]], _Cutkosky Rules for Superstring Field Theory_ ([arXiv:1604.01783](http://arxiv.org/abs/1604.01783))

* [[Ashoke Sen]], _Reality of Superstring Field Theory Action_ ([arXiv:1606.03455](http://arxiv.org/abs/1606.03455))

* Hiroshi Kunitomo, Tatsuya Sugimoto, _Type II superstring field theory with cyclic L-infinity structure_ ([arxiv:1911.04103](https://arxiv.org/abs/1911.04103))






Interpretation of [[picture number]] as a grading on [[differential forms on supermanifolds]] induced from a choice of[[integration over supermanifolds|integral top form]] is due to 

* [[Alexander Belopolsky]], _Picture changing operators in supergeometry and superstring theory_ ([arXiv:hep-th/9706033](http://arxiv.org/abs/hep-th/9706033)).

and has been further amplified in

* {#Witten12} [[Edward Witten]], appendix D of _Notes On Super Riemann Surfaces And Their Moduli_ ([arXiv:1209.2459](http://arxiv.org/abs/1209.2459))

* R. Catenacci, P.A. Grassi, S. Noja, _Superstring Field Theory, Superforms and Supergeometry_ ([arXiv:1807.09563](https://arxiv.org/abs/1807.09563))

See also 

* [[Ashoke Sen]], _Background Independence of Closed Superstring Field Theory_, JHEP02(2018)155 ([arXiv:1711.08468](https://arxiv.org/abs/1711.08468))

* Corinne de Lacroix, Harold Erbin, Sitender Pratap Kashyap, [[Ashoke Sen]], Mritunjay Verma, _Closed Superstring Field Theory and its Applications_,  International Journal of Modern Physics AVol. 32, No. 28n29, 1730021 (2017) ([arXiv:1703.06410](https://arxiv.org/abs/1703.06410))

* Ranveer Kumar Singh, *Algebraic Structures In Closed Superstring Field Theory, Homotopy Transfer And Effective Actions* &lbrack;[arXiv:2405.08063](https://arxiv.org/abs/2405.08063)&rbrack;




For previous constructions, the introduction of 

* {#JurcoMuenster13} [[Branislav Jurco]], Korbinian Muenster, _Type II Superstring Field Theory: Geometric Approach and Operadic Description_, JHEP 1304:126 (2013) [arXiv/1303.2323](http://arxiv.org/abs/1303.2323) <a href="http://dx.doi.org/10.1007/JHEP04(2013)126">doi</a>

based on 

* {#Yeh93} Chungsheng James Yeh, _Topics in superstring theory_, PhD thesis, Berkeley 1993 ([SPIRE](http://inspirehep.net/record/366138))

has a useful survey, which we quote now:

+-- {: quote}
###### Quote from ([Jurco-Muenster13](#JurcoMuenster13)):

The first attempt towards a field theory of superstrings was initiated by the work of Witten 

* {#Witten86a} [[Edward Witten]], _Interacting field theory of open superstrings_, Nuclear Physics B, Volume 276, Issue 2 (1986)
 

by seeking a Chern-Simons like action for open superstrings similar to the one of open bosonic string field theory ([Witten 86](#Witten86)). The major obstacle compared to the bosonic string is the necessity of [[picture changing operators]]. Indeed, the cubic superstring theory of ([Witten 86a](#Witten86a)) turns out to be inconsistent due to singularities arising form the collision of picture changing operators

* C. Wendt, _Scattering amplitudes and contact interactions in Witten's superstring field theory_, Nuclear Physics B, Volume 314, Issue 1.

In order to circumvent this problem, another approach was pursued which sets the string field into a different picture 

* C.R. Preitschopf, C.B. Thorn, S. Yost, _Superstring field theory_ Nuclear Physics B, Volume 337, Issue 2.

* I.Ya. Aref'eva, P.B. Medvedev, A.P. Zubarev, _New representation for string field solves the consistency problem for open superstring field theory_, Nuclear Physics B, Volume 341, Issue 2.

but upon including the [[RR-field|Ramond sector]], the modified superstring field theory suffers from similar inconsistencies 

* M. Kroyter, _Superstring field theory equivalence: Ramond sector_, Journal of High Energy Physics, Volume 2009, Issue 10.

These two approaches are based on the small Hilbert space, the state space including the reparametrization [[ghosts]] and superghosts as they arise from gaugefixing. Upon [[bosonization]] of the superghosts, an additional zero mode arises which allows the formulation of a WZW like action for the NS sector of open superstring field theory 

* [[Nathan Berkovits]], _Super-Poincare Invariant Superstring Field Theory_, ([hep-th/9503099](http://arxiv.org/abs/hep-th/9503099))

In contrast to bosonic string field theory, [[BV quantization]] of this theory is more intricate than simply relaxing the ghost number
constraint for the fields of the classical action

* [[Nathan Berkovits]], _Constrained BV description of string field theory_, Journal of High Energy Physics, Volume 2012, Issue 3.


* M. Kroyter, Y. Okawa, M. Schnabl, S. Torii, [[Barton Zwiebach]], _Open superstring eld theory I: gauge xing, ghost structure, and propagator, Journal of High Energy Physics, Volume 2012, Issue 3.

Finally, there is a formulation of open superstring field theory that differs from all other approaches in not fixing the picture of classical fields 

* M. Kroyter, _Superstring field theory in the democratic picture_, Advances in Theoretical and Mathematical Physics, Volume 15, Number 3.

On the other hand, the construction of bosonic closed string field theory ([Zwiebach 92](#Zwiebach)) takes its origin in the [[moduli space]] of closed [[Riemann surfaces]]. Vertices represent a subspace of the moduli space, such that the moduli space decomposes uniquely into vertices and graphs,and do not apriori require a background. Graphs are constructed from the vertices by sewing together punctures along prescribed local coordinates around the punctures. But an assignment of local coordinates around the punctures, globally on the moduli space, is possible only up to rotations. This fact implies the level matching condition and via gauge
invariance also the $b_0^- = 0$ constraint.

In an almost unnoticed work ([Yeh](#Yeh93)), the geometric approach developed in bosonic closed string field theory, as described in the previous paragraph, has been generalized to the context of superstring field theory. Neveu-Schwarz punctures behave quite similar to punctures
in the bosonic case, but a Ramond puncture describes a divisor on a super Riemann surface rather than a point. As a consequence, local coordinates around Ramond punctures, globally defined over super moduli space, can be fixed only up to rotations and translation in the Ramond divisor.

A given background provides forms on super moduli space 

* [[Alexander Belopolsky]], _New Geometrical Approach to Superstrings_ ([arXiv:hep-th/9703183](http://arxiv.org/abs/hep-th/9703183))

* L. Alvarez-Gaume, P. Nelson, C. Gomez, G. Sierra, C. Vafa, _Fermionic strings in the operator formalism_, Nuclear Physics B, Volume 311, Issue 2.

in the sense of [[integration over supermanifolds|geometric integration theory on supermanifolds]], and in particular the geometric meaning
of [[picture changing operators]] has been clarified 

* [[Alexander Belopolsky]], _Picture changing operators in supergeometry and superstring theory_ ([arXiv:hep-th/9706033](http://arxiv.org/abs/hep-th/9706033)).

Integrating along an odd direction in moduli space inevitably generates a picture changing operator. Thus, the ambiguity of defining local coordinates around Ramond punctures produces a picture changing operator
associated with the vector field generating translations in the Ramond divisor. The bpz inner product plus the additional insertions originating from the sewing define the [[symplectic form]] relevant for 
[[BV quantization]]. As in the bosonic case, we require that the symplectic form has to be non-degenerate, but the fact that the picture changing operator present in the Ramond sector has a non-trivial kernel, forces to impose additional restrictions besides the level matching and $b_0^- = 0$ constraint on the state space.
The purpose of ([Jurco-Muenster 13](#JurcoMuenster13)) is to describe the construction of type II superstring field theory in the geometric approach. 

=--


Older reviews include

* [[Nathan Berkovits]], _Review of open superstring field theory_ , ([arXiv:hep-th/0105230](http://arxiv.org/abs/hep-th/0105230))

More recently there is



* Tomoyuki Takezaki, _Open superstring field theory including the Ramond sector based on the supermoduli space_ ([arXiv:1901.02176](https://arxiv.org/abs/1901.02176))

* Hiroshi Kunitomo, *Type II superstring field theory revisited* ([arXiv:2106.07917](https://arxiv.org/abs/2106.07917))



### Effective field theory

Discussion of Wilsonian [[effective field theory]] of string field theory includes

* R. Brustein, S.P.De Alwis, _Renormalization group equation and non-perturbative effects in string-field theory_, Nuclear Physics B
Volume 352, Issue 2, 25 March 1991, Pages 451-468 (<a href="https://doi.org/10.1016/0550-3213(91)90451-3">doi:10.1016/0550-3213(91)90451-3</a>)

* Brustein and K. Roland, _Space-time versus world sheet renormalization group equation in string theory_, Nucl. Phys. B372, 201 (1992) (<a href="https://doi.org/10.1016/0550-3213(92)90317-5">doi:10.1016/0550-3213(92)90317-5</a>)

* {#Sen16} [[Ashoke Sen]], _Wilsonian Effective Action of Superstring Theory_, J. High Energ. Phys. (2017) 2017: 108 ([arXiv:1609.00459](https://arxiv.org/abs/1609.00459))



### Relation to $A_\infty$- and $L_\infty$-algebras
 {#ReferencesHomotopyAlgebra}

The [[L-infinity algebra]] structure on Zwiebach's bosonic closed string fields is apparently due to a comment by [[Jim Stasheff]] to the conference contribution

* {#Zwiebach89} [[Barton Zwiebach]], *Issues In Covariant Closed String Theory*, pp 192-200 in: *Proceedings of [10th and Final Workshop on Grand Unification](http://inspirehep.net/record/966930)*, 20-22 Apr 1989. Chapel Hill, North Carolina &lbrack;[spire:282685](http://inspirehep.net/record/282685)&rbrack;

It appears in print in

* [[Barton Zwiebach]], *Closed string field theory: Quantum action and the Batalin-Vilkovisky master equation*, Nucl. Phys. B **390** 1 (1993) 33-152 &lbrack;[arXiv:hep-th/9206084](http://arxiv.org/abs/hep-th/9206084), <a href="https://doi.org/10.1016/0550-3213(93)90388-6">doi:10.1016/0550-3213(93)90388-6</a>&rbrack;

See also at _[[L-infinity algebras in physics]]_.

The [[A-infinity algebra]] structure of bosonic open string field theory in 

* [[Matthias Gaberdiel]], [[Barton Zwiebach]], _Tensor Constructions of Open String Theories I: Foundations_ ([arXiv:hep-th/9705038](http://arxiv.org/abs/hep-th/9705038))

For the topological string see

* [[Manfred Herbst]], _Quantum A-infinity Structures for Open-Closed Topological Strings_ ([arXiv:hep-th/0602018](http://arxiv.org/abs/hep-th/0602018))

Discussion for [[heterotic string theory|heterotic]] string field theory is in 

* {#KunitomoSugimoto19} Hiroshi Kunitomo, Tatsuya Sugimoto, _Heterotic string field theory with cyclic L-infinity structure_ ([arXiv:1902.02991](https://arxiv.org/abs/1902.02991))

Discussion of the mathematical aspects is in 

* [[Jim Stasheff]], _Closed string field theory, strong homotopy Lie algebras and the operad actions of moduli space_ Talk given at the _Conference on Topics in Geometry and Physics_ (1992) ([arXiv:hep-th/9304061](http://arxiv.org/abs/hep-th/9304061))

* {#Markl} [[Martin Markl]], _Loop Homotopy Algebras in Closed String Field Theory_, Comm. Math. Phys. 221(2):367--384, 2001. ([arXiv:hep-th/9711045](http://arxiv.org/abs/hep-th/9711045))
 
* [[Alessandro Tomasiello]], _A-infinity structure and superpotentials_ ([arXiv:hep-th/0107195](http://arxiv.org/abs/hep-th/0107195))


* [[Hiroshige Kajiura]], _Homotopy Algebra Morphism and Geometry of Classical String Field Theory_ (2001) ([arXiv:hep-th/0112228](http://arxiv.org/abs/hep-th/0112228))

* {#KajiuraStasheff04} [[Hiroshige Kajiura]], [[Jim Stasheff]], _Homotopy algebras inspired by classical open-closed string field theory_, Comm. Math. Phys. 263 (2006) 553&#8211;581 (2004) ([arXiv:math/0410291](http://arxiv.org/abs/math/0410291))

* {#Markl04} [[Martin Markl]], _Operadic interpretation of $A_\infty$-algebras over $L_\infty$-algebras_, appendix to ([Kajiura-Stasheff 04](#KajiuraStasheff04))

* Korbinian M&#252;nster, [[Ivo Sachs]], _Quantum Open-Closed Homotopy Algebra and String Field Theory_ ([arXiv:1109.4101](http://arxiv.org/abs/1109.4101))

* Korbinian M&#252;nster, [[Ivo Sachs]], _On Homotopy Algebras and Quantum String Field Theory_ ([arXiv:1303.3444](http://arxiv.org/abs/1303.3444))

* {#DoubekJurcoMuenster13} [[Martin Doubek]], [[Branislav Jurco]], Korbinian Muenster, _Modular operads and the quantum open-closed homotopy algebra_, J. High Energ. Phys. 2015, 1–55 (2015) ([arXiv:1308.3223](https://arxiv.org/abs/1308.3223), <a href="https://doi.org/10.1007/JHEP12(2015)158">doi:10.1007/JHEP12(2015)158</a>)


Surveys include

* [[Jim Stasheff]], _[[A Survey of Cohomological Physics]]_ 

* [[Hiroshige Kajiura]], [[Jim Stasheff]], _Homotopy algebra of open&#8211;closed strings_ Geometry & Topology Monographs 13 (2008) 229&#8211;259 ([pdf](http://msp.warwick.ac.uk/gtm/2008/13/gtm-2008-13-010s.pdf)) ([arXiv:hep-th/0606283](http://arxiv.org/abs/hep-th/0606283))

* {#Sachs15} [[Ivo Sachs]], _String theory and homotopy algebras_, talk notes, Srni 2015 ([pdf](http://www.math.muni.cz/~srni/Prednasky/Sachs.pdf))

* {#Sachs19} [[Ivo Sachs]], _Homotopy Algebras in String Field Theory_, in: Proceedings of _[[Higher Structures in M-Theory 2018]]_ Fortschritte der Physik, Special Issue Volume 67, Issue 8-9 ([arXiv:1903.02870](https://arxiv.org/abs/1903.02870), [doi:10.1002/prop.201910013](https://doi.org/10.1002/prop.201910013))


Discussion of the CSFT-action as of the form of [[schreiber:∞-Chern-Simons theory]] is in section 4.4 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_



From all this one might expect analogously a [[super L-∞ algebra]] underlying closed superstring field theory. This does not seem to materialzed yet in the literature, though. The closest is maybe the structure described in 

* Yuji Okawa, [[Barton Zwiebach]], _Heterotic string field theory_ ([arXiv:hep-th/0406212](http://arxiv.org/abs/hep-th/0406212))



See also _[[higher category theory and physics]]_ .

#### For Yang-Mills theory
 {#ReferencesOnYMTheoryAspects}


The idea that open strings on $N$ coincident [[D-branes]] exhibit [[gauge enhancement]] to $U(N)$-gauge field theory is due to 

* {#Witten95} [[Edward Witten]], section 3 of _Bound States Of Strings And $p$-Branes_, Nucl.Phys.B460:335-350, 1996 ([arXiv:hep-th/9510135](https://arxiv.org/abs/hep-th/9510135))

There, this is called an "obvious guess" (first line on p. 8). Subsequently,  most authors cite this obvious guess as a fact; for instance the review 

* {#Myers03} [[Robert Myers]], section 3 of _Nonabelian Phenomena on D-branes_, Class.Quant.Grav. 20 (2003) ([arXiv:hep-th/0303072](https://arxiv.org/abs/hep-th/0303072))

By actual computation in [[open string field theory]] "convincing evidence" (see bottom of p. 22) was found, numerically, in

* {#ColettiSigalovTaylor03} Erasmo Coletti, Ilya Sigalov, [[Washington Taylor]], _Abelian and nonabelian vector field effective actions from string field theory_, JHEP 0309 (2003) 050 ([arXiv:hep-th/0306041](https://arxiv.org/abs/hep-th/0306041))

Similar numerical derivation, as well as exact derivation at zero momentum, is in

* [[Nathan Berkovits]], [[Martin Schnabl]], _Yang-Mills Action from Open Superstring Field Theory_, JHEP 0309 (2003) 022 ([arXiv:hep-th/0307019](https://arxiv.org/abs/hep-th/0307019))

The first full derivation seems to be due to

* {#Lee16} [[Taejin Lee]], _Covariant open bosonic string field theory on multiple D-branes in the proper-time gauge_ ([arXiv:1609.01473](https://arxiv.org/abs/1609.01473))

which is surveyed in

* {#Lee17} [[Taejin Lee]], _Deformation of the Cubic Open String Field Theory_, Phys. Lett. B 768 (2017) 248 ([arXiv:1701.06154](https://arxiv.org/abs/1701.06154))

That on [[D0-branes]] this reproduces the [[BFSS matrix model]] and on [[D(-1)-branes]] the [[IKKT matrix model]] is shown in

* [[Taejin Lee]], _Covariant Open String Field Theory on Multiple D$p$-Branes_ ([arXiv:1703.06402](https://arxiv.org/abs/1703.06402))


Discussion of the [[L-infinity algebra]] [[schreiber:infinity-Chern-Simons theory|higher Chern-Simons theory]] of the [[Yang-Mills theory]] that appears to lowest order as the [[effective QFT]] in open string field theory is for instance in

* [[Anton Zeitlin]], 

  _Homotopy Lie Superalgebra in Yang-Mills Theory_ ([arXiv:0708.1773](http://arxiv.org/abs/0708.1773))

  _BV Yang-Mills as a Homotopy Chern-Simons via SFT_ ([arXiv:0709.1411](http://arxiv.org/abs/0709.1411))

  _SFT-inspired Algebraic Structures in Gauge Theories_ ([arXiv:0711.3843](http://arxiv.org/abs/0711.3843))

  _Conformal Field Theory and Algebraic Structure of Gauge Theory_ ([arXiv:0812.1840](http://arxiv.org/abs/0812.1840))

### Background independence
 {#ReferencesBackgroundIndependence}

References discussing independence of string field theories on the [[CFT]] ([[sigma-model]] background) in terms of which they are written down.



#### For closed string field theory
 {#ReferencesBackgroundIndependenceForClosed}

* [[Ashoke Sen]], [[Barton Zwiebach]], _Quantum Background Independence of Closed String Field Theory_ ([arXiv:hep-th/9311009](http://arxiv.org/abs/hep-th/9311009))


* [[Ashoke Sen]], [[Barton Zwiebach]], _Background Independent Algebraic Structures in Closed String Field Theory_ ([arXiv:hep-th/9408053](http://arxiv.org/abs/hep-th/9408053))

A review of the history of some related developments is given in

* Sabbir Rahman, _Manifest background independent formulation of string field theory_ ([newsgroup comment](http://www.natscience.com/Uwe/Forum.aspx/physics-research/503/Manifest-background-independent-formulation-of-string-field))

Closed string field theory has also been argued to arise from the [[dynamics]] of [[Wilson loops]] in the [[IKKT matrix model]] in ([Fukuma-Kawai-Kitazawa-Tsuchiya 97](#FukumaKawaiKitazawaTsuchiya97))

* {#FukumaKawaiKitazawaTsuchiya97} M. Fukuma, H. Kawai, Y. Kitazawa, A. Tsuchiya, _String Field Theory from IIB Matrix Model_, Nucl.Phys.B510:158-174,1998 ([arXiv:hep-th/9705128](http://arxiv.org/abs/hep-th/9705128))
 


#### For open string field theory

* [[Edward Witten]], _On background independent open string field theory_,  Phys.Rev. D46 (1992) 5467. ([arXiv:hep-th/9208027](http://arxiv.org/abs/hep-th/9208027))

* [[Theodore Erler]], Carlo Maccaferri, _String Field Theory Solution for Any Open String Background_ ([arXiv:1406.3021](http://arxiv.org/abs/1406.3021))


### Tachyon dynamics, decaying D-branes and Sen's conjecture
 {#BosonicStringVacuumAndSenConjecture}

[[Sen's conjecture]] about the open [[bosonic string]] [[tachyon]] and the decay of the [[D25-brane]] originates in 

* [[Ashoke Sen]], _Universality of the Tachyon Potential_,  	JHEP 9912:027,1999 ([arXiv:hep-th/9911116](http://arxiv.org/abs/hep-th/9911116))

Hints for the decay of the space-filling [[D25-brane]] in open bosonic string field theory and the resulting closed string vacuum were discussed in articles like

* Ian Ellwood, Washington Taylor, _Open string field theory without open strings_, Phys.Lett. B512 (2001) 181-188 ([arXiv:hep-th/0103085](http://arxiv.org/abs/hep-th/0103085))

* Bo Feng, Yang-Hui He, Nicolas Moeller, _Testing the Uniqueness of the Open Bosonic String Field Theory Vacuum_ ([arXiv:hep-th/0103103](http://arxiv.org/abs/hep-th/0103103))

A breakthrough were then the analytic solutions describing the bosonic string tachyon vacuum in 

* [[Martin Schnabl]], _Analytic solution for tachyon condensation in open string field theory_ ([arXiv:hep-th/0511286](http://arxiv.org/abs/hep-th/0511286))

* Ian Ellwood, [[Martin Schnabl]], _Proof of vanishing cohomology at the tachyon vacuum_, JHEP 0702:096,2007 ([arXiv:hep-th/0606142](http://arxiv.org/abs/hep-th/0606142))

Analogous discussion [[Sen's conjecture]] including also brane/[[anti-brane]] pairs in [[superstring]] theory:

* [[Leonardo Rastelli]], [[Ashoke Sen]], [[Barton Zwiebach]], _Vacuum String Field Theory_ ([arXiv:hep-th/0106010](http://arxiv.org/abs/hep-th/0106010))

* [[Ashoke Sen]], _Tachyon Dynamics in Open String Theory_,  	Int.J.Mod.Phys.A20:5513-5656,2005 ([arXiv:hep-th/0410103](http://arxiv.org/abs/hep-th/0410103))

* L. Bonora, N. Bouatta, C. Maccaferri, _Towards open-closed string duality: Closed Strings as Open String Fields_ ([arXiv:hep-th/0609182](http://arxiv.org/abs/hep-th/0609182))

* [[Theodore Erler]], _Tachyon Vacuum in Cubic Superstring Field Theory_, JHEP 0801:013,2008 ([arXiv:0707.4591](http://arxiv.org/abs/0707.4591))

* [[Theodore Erler]], _Analytic Solution for Tachyon Condensation in Berkovits' Open Superstring Field Theory_, JHEP 1311 (2013) 007 ([arXiv:1308.4400](https://arxiv.org/abs/1308.4400))

### Relation to higher spin gauge theory

The idea that [[higher spin gauge theory]] appears as the limiting case of string field theory where the [[string tension]] vanishes goes back to 

* {#HenneauxTeitelboim87} [[Marc Henneaux]], [[Claudio Teitelboim]], section 2 of _First And Second Quantized Point Particles Of Any Spin_, in [[Claudio Teitelboim]], [[Jorge Zanelli]] (eds.) _Santiago 1987, Proceedings, Quantum mechanics of fundamental systems 2_, pp. 113-152. Plenum Press.

* {#Gross88} [[David Gross]], _High-Energy Symmetries Of String Theory_, Phys. Rev. Lett. 60 (1988) 1229.


and is further developed for instance in

* {#SagnottiTsulaia03} [[Augusto Sagnotti]], M. Tsulaia, _On higher spins and the tensionless limit of String Theory_, Nucl.Phys.B682:83-116,2004 ([arXiv:hep-th/0311257](http://arxiv.org/abs/hep-th/0311257))

* {#Bonelli03} G. Bonelli, _On the Tensionless Limit of Bosonic Strings, Infinite Symmetries and Higher Spins_, Nucl.Phys. B669 (2003) 159-172 ([arXiv:hep-th/0305155](http://arxiv.org/abs/hep-th/0305155))

* [[Augusto Sagnotti]], M. Taronna, _String Lessons for Higher-Spin Interactions_, Nucl.Phys.B842:299-361,2011 ([arXiv:1006.5242](http://arxiv.org/abs/1006.5242))

* {#Sagnotti11} [[Augusto Sagnotti]], _Notes on Strings and Higher Spins_ ([arXiv:1112.4285](http://arxiv.org/abs/1112.4285)) 

And conversely:

* Rakibur Rahman, Massimo Taronna, _From Higher Spins to Strings: A Primer_ in [[Stefan Fredenhagen]] (ed.) _Introduction to Higher Spin Theory_ ([arXiv:1512.07932](https://arxiv.org/abs/1512.07932))

* [[Matthias Gaberdiel]], [[Rajesh Gopakumar]], _String Theory as a Higher Spin Theory_, J. High Energ. Phys. (2016) 2016: 85 ([arXiv:1512.07237](https://arxiv.org/abs/1512.07237), <a href="https://doi.org/10.1007/JHEP09(2016)085">doi:10.1007/JHEP09(2016)085</a>)


[[!redirects String field theory]]

[[!redirects open string field theory]]
[[!redirects closed string field theory]]

[[!redirects bosonic string field theory]]



[[!redirects closed bosonic string field theory]]
[[!redirects open bosonic string field theory]]

[[!redirects superstring field theory]]