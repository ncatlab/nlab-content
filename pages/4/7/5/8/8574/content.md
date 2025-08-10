
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Yang-Mills equations_ are the [[equations of motion]]/[[Euler-Lagrange equations]] of [[Yang-Mills theory]]. They generalize [[Maxwell's equations]].

## Details

### General form

(...)

### Abelian case
 {#AbelianCase}

For an [[abelian group|abelian]] [[Lie group]] as [[structure group]], its [[Lie algebra]] is also abelian and hence all [[Lie brackets]] vanish and makes the [[Yang-Mills equation]] reduce to the *[[Maxwell equation]]*:

$$
  \mathrm{d}\star\mathrm{d}A
  \;=\;
  0
  \,.
$$



## Properties

### Relation to generalized Laplace equation

Let:

$$
  \Delta_A
  \;\coloneqq\;
  \delta_A\mathrm{d}_A
  \,+\,
  \mathrm{d}_A \delta_A
  \;\colon\;
  \Omega^k\big(
    B,\, Ad(E)
  \big)
  \longrightarrow
  \Omega^k\big(
    B,\, Ad(E)
  \big)
$$

be a [[generalized Laplace operator]].

The [[Bianchi identity]] $\mathrm{d}_A F_A=0$ and the [[Yang-Mills equation]] $\delta_A F_A=0$ combine to:

$$
  \Delta_A F_A
  \;=\;
  0
  \,.
$$


## Related concepts

* [[Yang-Mills instanton]]

* [[Yang-Mills monopole]]

* [[F-Yang-Mills equation]]

* [[Bi-Yang-Mills equation]]

## References

(For full list of references see at _[[Yang-Mills theory]]_)


### General


* {#Uhlenbeck12} [[Karen Uhlenbeck]], notes by [[Laura Fredrickson]], _Equations of Gauge Theory_, lecture at Temple University, 2012 ([pdf](https://web.stanford.edu/~ljfred4/Attachments/TempleLectures.pdf), [[UhlenbeckGaugeTheory.pdf:file]])

* DispersiveWiki, _[Yang-Mills equations](https://dispersivewiki.org/DispersiveWiki/index.php?title=Yang-Mills_equations)_

* [TP.SE](http://theoreticalphysics.stackexchange.com/), _[Which exact solutions of the classical Yang-Mills equations are known?](http://theoreticalphysics.stackexchange.com/questions/317/which-exact-solutions-of-the-classical-yang-mills-equations-are-known)_ 

### Solutions

#### General

Wu and Yang (1968) found a static solution to the sourceless $SU(2)$ [[Yang-Mills equations]]. Recent references include

* J. A. O. Marinho, O. Oliveira, B. V. Carlson, T. Frederico, _Revisiting the Wu-Yang Monopole: classical solutions and conformal invariance_ 

	
There is an old review, 

* Alfred Actor, _Classical solutions of $SU(2)$ Yang&#8212;Mills theories_, Rev. Mod. Phys. 51, 461&#8211;525 (1979), 

that provides some of the known solutions of $SU(2)$ gauge theory in [[Minkowski spacetime|Minkowski]] ([[monopoles]], plane waves, etc) and [[Euclidean space]] ([[instantons]] and their cousins). For general [[gauge groups]] one can get solutions by embedding $SU(2)$'s. 

#### Instantons and monopoles

For [[Yang-Mills instantons]] the most general solution is known, first worked out by

* [[Michael Atiyah]], [[Nigel Hitchin]], [[Vladimir Drinfeld]], [[Yuri Manin]], _Construction of instantons_, Physics Letters 65 A, 3, 185--187 (1978) [pdf](http://www.new.ox.ac.uk/system/files/ADHM.pdf)

for the [[classical groups]] [[special unitary group|SU]], [[special orthogonal group|SO]] , [[symplectic group|Sp]], and then by 

* C. Bernard, N. Christ, A. Guth, E. Weinberg, _Pseudoparticle Parameters for Arbitrary Gauge Groups_, Phys. Rev. __D16__, 2977 (1977)  

for [[exceptional Lie groups]]. The latest twist on the [[Yang-Mills instanton]] story is the construction of solutions with non-trivial [[holonomy]]: 

* Thomas C. Kraan, Pierre van Baal, _Periodic instantons with nontrivial holonomy_, Nucl.Phys. B533 (1998) 627-659, [hep-th/9805168](http://arxiv.org/abs/hep-th/9805168)

There is a nice set of lecture notes 

* David Tong, _TASI Lectures on Solitons_ ([hep-th/0509216](http://arxiv.org/abs/hep-th/0509216)), 

on topological solutions with different co-dimension ([[Yang-Mills instantons]], [[Yang-Mills monopoles]], vortices, domain walls). Note, however, that except for instantons these solutions typically require extra scalars and broken U(1)'s, as one  may find in [[super Yang-Mills theories]].

Some of the material used here has been taken from 

* [TP.SE](http://theoreticalphysics.stackexchange.com/), _[Which exact solutions of the classical Yang-Mills equations are known?](http://theoreticalphysics.stackexchange.com/questions/317/which-exact-solutions-of-the-classical-yang-mills-equations-are-known)_ 

Another model featuring Yang-Mills fields has been proposed by Curci and Ferrari, see [[Curci-Ferrari model]].

[[!redirects Yang-Mills equations]]
[[!redirects Yang-Mills connection]]
[[!redirects Yang-Mills connections]]


