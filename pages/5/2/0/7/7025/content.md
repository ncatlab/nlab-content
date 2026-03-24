
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



\tableofcontents



## Idea

For the moment, see the standard reference [Chari and Pressley (1994)](#CP94).

## Definition

A *Lie bialgebra* is a [[Lie algebra]] $\mathfrak{g}$ equipped with a skew-symmetric [[linear map]] (the *cobracket*)

$$    
\delta \colon
{\mathfrak{g}}\to {\mathfrak{g}}\otimes {\mathfrak{g}},
$$

such that

1. its [[dual linear map]] $\delta^\ast: \mathfrak{g}^\ast \otimes \mathfrak{g}^\ast \to \mathfrak{g}^\ast$ is a [[Lie bracket]] on the [[dual vector space]] $\mathfrak{g}^\ast$,

1. it is a [[cocycle]] for $[-,-]$ in that:
   $$
     \delta\big(
        [x,y]
     \big) 
     = 
     (ad_x \otimes id 
      + 
     id \otimes ad_x)
     \delta(y)
     -
     (ad_y \otimes id 
       + 
     id \otimes ad_y)
     \delta(x)   
    \mathrlap{\,,}
   $$
   
   where $ad$ denotes the [[adjoint action]] of $\mathfrak{g}$ on itself.



## Quantization
 {#Quantization}

### Idea

[[quantum group|Quantum groups]] were introduced independently by Drinfeld and Jimbo around 1984. One of the most important examples of quantum groups are deformations of 
[[universal enveloping algebras]]. These [[deformations]] are closely related to Lie bialgebras. In particular, every deformation of a universal enveloping algebra induces
a Lie bialgebra structure on the underling Lie algebra. In ([Drinfeld](#Drinfeld)) Drinfeld asked if the converse of this statement holds: 

> "Does there exist a universal quantization for Lie bialgebras?"

This was answered to the positive by [Etingof & Kazhdan](#EtingofKazhdan).



## References

* {#Drinfeld} [[Vladimir Drinfeld]]: _On some unsolved problems in quantum group theory_,  Lecture Notes in Math., **1510**, Springer (1992)
 

* {#EtingofKazhdan} P. Etingof , D. Kazhdan: _Quantization of Lie bialgebras_ (in five parts) ([arXiv:q-alg/9506005](https://arxiv.org/abs/q-alg/9506005)), ([arXiv:q-alg/9701038](https://arxiv.org/abs/q-alg/9701038)), ([arXiv:q-alg/9610030](https://arxiv.org/abs/q-alg/9610030)), ([arXiv:math/9801043](https://arxiv.org/abs/math/9801043)), ([arXiv:math/9808121](https://arxiv.org/abs/math/9808121)).
 

* {#CP94} V. Chari and A. Pressley: *A Guide to Quantum Groups*. Cambridge University Press, Cambridge (1994)

* Wikipedia, _[Lie biablgebra](http://en.wikipedia.org/wiki/Lie_bialgebra)_

* &#352;tefan Sak&#225;lo&#353;, [[Pavol Ševera]], _On quantization of quasi-Lie bialgebras_, [arxiv/1304.6382](http://arxiv.org/abs/1304.6382)

[[!redirects Lie bialgebras]]