

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fields and quanta
+-- {: .hide}
[[!include fields and quanta - table]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

In [[QCD]] a _meson_ is a [[bound state]] of two [[quarks]] via the [[strong nuclear force]]. 

\linebreak

[[!include flavors of fundamental particles -- table]]



## Examples

### First-generation mesons
 {#FirstGenerationMesons}

The mesons in the first [[generation of fermions]], being [[bound states]] of [[up quarks]] and [[down quarks]] are

* [[π-meson]] (pion)

* [[ρ-meson]]

* [[ω-meson]]

As [[linear representations]] of the [[Lorentz group]] ([[Pin group]]) and [[isospin]] [[flavour (particle physics)|flavour]] group ([[Wigner classification]]) these first-generation meson [[field (physics)|fields]] are given as follows:

\begin{imagefromfile}
    "file_name": "FirstGenerationMesonFieldsPin.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": 0,
        "right": 10,
        "bottom": 0,
        "left": 20
    }
\end{imagefromfile}

Here $\mathbf{n}$ denotes an [[irreducible representation]] of [[dimension]] $n$, and the subscript ${}_{\mathrm{sgn}}$ indicates the one of the two irreps of that dimension which pick up an extra sign under [[orientation]]-reversal ($\mathbf{4}_{{}_{sgn}} = \mathbf{4} \otimes \mathbf{1}_{{}_{sgn}}$ for $\mathbf{1}_{{}_{sgn}}$ the [[sign representation]]).

So the [[pion]] is a [[Lorentz group|Lorentz]]-[[pseudoscalar]], and the [[omega-meson]] and [[rho-meson]] are [[Lorentz group|Lorentz]] [[pseudovector]]  [[field (physics)|fields]].

As bilinears in the [[up-quark]] [[Weyl spinor]] [[field (physics)|field]] $u$ and [[down-quark]] [[Weyl spinor]] [[field (physics)|field]]  $d$ these [[meson]] [[field (physics)|fields]] are given as follows (with $(\sigma^0, \sigma^1, \sigma^2, \sigma^3)$ the [[Pauli matrices]]):


$$
  \sigma^0 
  \underset{
    {\color{blue}omega}
    \atop
    {\color{blue}meson}
  }{
    \underbrace{
      \omega^\mu
    }
  }
  +
  \sigma^i 
  \underset{
    {\color{blue}rho}
    \atop
    {\color{blue}meson}
  }{
    \underbrace{
      \rho^\mu_i
    }
  }
  \;=\;
  \array{
    \bar u \gamma^\mu \gamma^5 u
    &
    \bar u \gamma^\mu \gamma^5 d
    \\
    \bar d \gamma^\mu \gamma^5 u
    &
    \bar d \gamma^\mu \gamma^5 d
  }
$$


### Second-generation mesons

Mesons containing [[strange quarks]] from the second [[generation of fermions]]:

* [[kaon]]

### Third-generation mesons

Mesons containing [[bottom quarks]] from the second [[generation of fermions]]:


* [[B meson]]

### See also

* [[quarkonium]]

## Properties

### Conceptualization and computation in AdS/QCD
 {#ConceptualizationAndComputationInAdSQCD}



In the [[Witten-Sakai-Sugimoto model]] for [[non-perturbative effect|strongly coupled]] [[QCD]] via an [[intersecting D-brane model]], the [[hadrons]] in [[QCD]] correspond to [[string theory|string-theoretic]]-phenomena in an ambient [[bulk field theory]] on an approximately [[anti de Sitter spacetime]]:

1. the [[mesons]] ([[bound states]] of 2 [[quarks]]) correspond to [[open strings]] in the bulk, whose two endpoints on the [[asymptotic boundary]] correspond to the two [[quarks]];

1. [[baryons]] ([[bound states]] of $N_c$ [[quarks]]) appear in two different but equivalent ([Sugimoto 16, 15.4.1](#Sugimoto16)) guises:

   1. as [[wrapped brane|wrapped]] [[D4-branes]] with $N_c$ [[open strings]] connecting them to the [[D8-brane]]

      ([Witten 98b](#Witten98b), [Gross-Ooguri 98](#GrossOoguri98))

   1. as [[skyrmions]] 

      ([Sakai-Sugimoto 04, section 5.2](#SakaiSugimoto04), [Sakai-Sugimoto 05, section 3.3](#SakaiSugimoto05), see [Bartolini 17](#Bartolini17)). 

For review see [Sugimoto 16](#Sugimoto16), also [Rebhan 14, around (18)](#Rebhan14).

<center>
<img src="https://ncatlab.org/nlab/files/BaryonsAsD4Branes.jpg" width="700">
</center>

> graphics grabbed from [Sugimoto 16](#Sugimoto16)

This produces [[baryon]] [[mass]] spectra with moderate quantitative agreement with [[experiment]] ([HSSY 07](#HSSY07)):


<center>
<img src="https://ncatlab.org/nlab/files/BaryonSpectrumInSakaiSugimoto.jpg" width="700">
</center>

> graphics grabbed from [Sugimoto 16](#Sugimoto16)



## Related concepts

* [[hadron]], [[baryon]]

* [[Skyrmion]]

* [[confinement]]

  * [[chiral perturbation theory]]

  * [[quark bag model]], [[Cheshire cat principle]]

  * [[vector meson dominance]]

## References

### General

Origin of [[effective field theory]] of [[mesons]] in [[nuclear physics]], via [[hidden local gauge symmetry]]:

* [[Jun John Sakurai]], _Theory of strong interactions_, Annals Phys. 11 (1960) 1-48 ([spire:3218](http://inspirehep.net/record/3218), <a href="https://doi.org/10.1016/0003-4916(60)90126-3">doi:10.1016/0003-4916(60)90126-3</a>)

Introduction:

* [[Jun John Sakurai]], _Currents and Mesons_, Chicago Lectures in Physics, based on notes by George Barry, University of Chicago Press (1969) ([ISBN: 9780226733838](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3622598.html))


* {#MachleidtEntem11} [[Rupert Machleidt]], [[David Rodríguez Entem]], _Chiral effective field theory and nuclear forces_, Phys. Rept. 503:1-75, 2011 ([arXiv:1105.2919](https://arxiv.org/abs/1105.2919), [doi:10.1016/j.physrep.2011.02.001](https://doi.org/10.1016/j.physrep.2011.02.001))

See also

* Wikipedia, _[Meson](http://en.wikipedia.org/wiki/Meson)_

* Wikipedia, _[Vector meson](https://en.wikipedia.org/wiki/Vector_meson)_


### In chiral perturbation theory

See the references at _[[chiral perturbation theory]]_.



### In the large $N$ limit

In the [[large N limit]]:

* {:Witten79} [[Edward Witten]], _Baryons in the $1/n$ Expansion_, Nucl. Phys. B160 (1979) 57-115 ([spire:140391](http://inspirehep.net/record/140391), <a href="https://doi.org/10.1016/0550-3213(79)90232-3">doi:10.1016/0550-3213(79)90232-3</a>)


### In Witten-Sakai-Sugimoto model for AdS-QCD


* {#Witten98b} [[Edward Witten]], _Baryons And Branes In Anti de Sitter Space_, JHEP 9807:006, 1998 ([arXiv:hep-th/9805112](https://arxiv.org/abs/hep-th/9805112))

* {#GrossOoguri98} [[David Gross]], [[Hirosi Ooguri]], _Aspects of Large N Gauge Theory Dynamics as Seen by String Theory_, Phys.Rev.D58:106002,1998 ([arXiv:hep-th/9805129](https://arxiv.org/abs/hep-th/9805129))

* {#SakaiSugimoto04} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _Low energy hadron physics in holographic QCD_, Prog.Theor.Phys.113:843-882, 2005 ([arXiv:hep-th/0412141](https://arxiv.org/abs/hep-th/0412141))

* {#SakaiSugimoto05} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _More on a holographic dual of QCD_, Prog.Theor.Phys.114:1083-1118, 2005 ([arXiv:hep-th/0507073](https://arxiv.org/abs/hep-th/0507073))

* {#HSSY07} Hiroyuki Hata, [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], Shinichiro Yamato, _Baryons from instantons in holographic QCD_, Prog.Theor.Phys.117:1157, 2007 ([arXiv:hep-th/0701280](https://arxiv.org/abs/hep-th/0701280))


Review

* {#Rebhan14} Anton Rebhan, _The Witten-Sakai-Sugimoto model: A brief review and some recent results_, 3rd International Conference on New Frontiers in Physics, Kolymbari, Crete, 2014 ([arXiv:1410.8858](https://arxiv.org/abs/1410.8858))


* {#Sugimoto16} [[Shigeki Sugimoto]], _Skyrmion and String theory_, chapter 15 in [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))


[[!redirects mesons]]

[[!redirects meson field]]
[[!redirects meson fields]]

[[!redirects vector meson]]
[[!redirects vector mesons]]

[[!redirects pseudovector meson]]
[[!redirects pseudovector mesons]]
[[!redirects pseudo-vector meson]]
[[!redirects pseudo-vector mesons]]

[[!redirects scalar meson]]
[[!redirects scalar mesons]]

[[!redirects meson field]]
[[!redirects meson fields]]

[[!redirects vector meson field]]
[[!redirects vector meson fields]]


