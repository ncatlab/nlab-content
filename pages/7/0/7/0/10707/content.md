
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[moduli stack]] $\mathcal{M}_{FG}$ of all [[formal groups]]. Often meant are 1-dimensional commutative formal groups-

## Definition

Let $L = \pi_\bullet MU$ be the [[Lazard ring]]. 

Write $G^+$ for the [[group scheme]] given on a [[ring]] $R$ by 

$$
  G^+(R) 
    \;\coloneqq\; 
  \big\{
    g\in R[ [x] ] 
    \;\big\vert\; 
    g(t) = b_1 t + b_2 t^2 + \cdots 
    \;\text{with}\; b_1 \in R^\times 
  \big\}
  \,.
$$

There is a canonical [[group action|action]] of $G^+$ on $Spec(L)$. The [[quotient stack]] of this action is the [[moduli stack]] of (1d commutative) formal groups

$$
  \mathcal{M}_{fg} 
  \;=\;
  \big(Spec(L)\big)\sslash G^+
  \,.
$$

(e.g. [Lurie, lecture 11, def. 2](#LurieLect11))

## Properties

### Chromatic height stratification

The moduli stack of formal groups $\mathcal{M}_{FG}$ admits a natural [[stratification]] whose open [[strata]] are labeled by a [[natural number]] called the _[[height of a formal group|height of formal groups]]_.

The [[complex oriented cohomology theories]] associated to these [[formal groups]] by the [[Landweber exact functor theorem]] accordingly also inherit such an integer label, called _[[chromatic filtration]]_. Studying this is the topic of [[chromatic homotopy theory]].

[[!include Lurie spectral sequences -- table]]


### Morava stabilizer group

Write $\overline{\mathbb{F}_{\mathrm{p}}}$ for the [[algebraic closure]] of $\mathbb{F}_p$.

The [[stratum]] $\mathcal{M}_{FG}^n$ can be identified with the [[homotopy quotient]] $Spec (\overline{\mathbb{F}}_{\mathrm{p}})// \mathbb{G}$, where the [[group]] $\mathbb{G}$ is the _Morava stabilizer group_. 

This is ([Lurie 10, lect. 19, prop. 1](#LurieLect19)) See also the beginning of [Lurie 10, lect 21](#LurieLect21).

### Deformation theory

The [[deformation theory]] around these [[strata]] is [[Lubin-Tate theory]].

### Relation to moduli of elliptic curves and tori

Inside the moduli stack of formal groups sit, in that order, that of [[cubic curves]], the [[moduli stack of elliptic curves]], the [[moduli stack of tori]].


## Related concepts

* [[Spec(S)]]

[[!include moduli spaces -- contents]]


[[!include moduli stack of curves -- table]]

## References

* [[Niko Naumann]], _Comodule categories and the geometry of the stack of formal groups_, Advances in Mathematics **215** (2007) pp 569-600, doi:[10.1016/j.aim.2007.04.007](http://dx.doi.org/10.1016/j.aim.2007.04.007), arXiv:[math/0503308](http://arxiv.org/abs/math/0503308).

* Brian D. Smithling, _On the moduli stack of commutative, 1-parameter formal Lie groups_ ([arXiv:0708.3326](http://arxiv.org/abs/0708.3326))

* {#LurieLect11} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 11 _Formal groups_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture11.pdf)) 


* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 14 _Classification of formal groups_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture14.pdf)) 

* {#LurieLect19} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 19 _Morava stabilizer groups_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture19.pdf))
 
 
* {#LurieLect21} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 21 _Lubin-Tate theory_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture21.pdf))

* [[Jeroen van der Meer]], _A Stack-Theoretic Perspective on $\mathrm{KU}$-Local Stable Homotopy Theory_, Chapter 3 _The Moduli Stack of Formal Groups_. 2019 ([pdf](https://www.universiteitleiden.nl/binaries/content/assets/science/mi/scripties/master/2018-2019/jvd-meer-thesisroot.pdf))
 
On [[quasicoherent sheaves]] over $\mathcal{M}_{fg}$:

* [[Paul Goerss]], _Realizing Families of Landweber Exact Homology Theories_ ([arXiv:0905.1319](http://arxiv.org/abs/0905.1319))

* [[Paul Goerss]], _Quasi-coherent sheaves on the moduli stack of formal groups_ ([arXiv:0802.0996](http://arxiv.org/abs/0802.0996))

[[!redirects moduli stacks of formal groups]]

[[!redirects height filtration]]

[[!redirects moduli stack of formal group laws]]

[[!redirects moduli space of formal groups]]
[[!redirects moduli spaces of formal groups]]
