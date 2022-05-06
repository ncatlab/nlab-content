
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[equivariant cohomology|equivariant]] version of [[de Rham cohomology]].

## Properties

### Models

Various different [[dg-algebras]] are used to model equivariant de Rham cohomology, known as 

* _[the Weil model](#TheWeilModel)_

* _[the Cartan model](#TheCartanModel)_

* _[the Kalkman model](#TheKalkmanModel)_

#### The Weil model
 {#TheWeilModel}

reviews include ([Atiyah-Bott 84](#AtiyahBott84), [Kalkman 93, section 2.1](#Kalkman93))



#### The Cartan model
 {#TheCartanModel}

reviews include ([Mathai-Quillen 86](#MathaiQuillen86), [Kalkman 93, section 2.2](#Kalkman93))


Let $X$ be a [[smooth manifold]], $G$ a [[Lie group]], and $\rho : X \times G \to X$ a smooth [[action]] of $G$ on $X$.

Write

$$
  (\Omega^\bullet(G, \mathfrak{h}^\ast[1])^G  
  \hookrightarrow
  \Omega(G, \mathfrak{h}^\ast[1])
$$

for the $G$-[[invariant differential forms]] on $G$ with [[coefficients]] in the linear dual of the Lie algebra $\mathfrak{h}$ of $H$, shifted up in degree. So for $\{F^a\} \subset \{t^a\}$ a dual [[basis]] of $\mathfrak{h}$ inside a dual basis for $\mathfrak{g}$, a general element of this space in degree $2 p + q$ is of the form

$$
  \omega = F^{a_1} \wedge \cdots F^{a_p} \wedge \omega_{a_1,\cdots ,a_q}
  \,,
$$

where $\omega_{\cdots}$ are [[differential n-form|differential q-forms]], such that for each $t_a \in \mathfrak{g}$ the [[Lie derivative]] of these forms satisfies

$$
  \mathcal{L}_{t_a} \omega_{a_1, a_2 \cdots , a_p}
  = 
  C_{a a_1}{}^b \omega_{b , a_2, \cdots , a_p}
  + 
  C_{a a_2}^{}^b \omega_{a_1 ,  b,  \cdots , a_p}
  + 
  \cdots
  \,, 
$$ 

where $\{C_{a b}{}^b\}$ are the structure constants of $\mathfrak{g}$, hence such that $[t_a, t_b] = C_{a b}{}^c t_c$.

Equip this [[graded vector space]] $\Omega^\bullet(G, \mathfrak{h}^\ast[1])^G$ with a [[differential]] $d_{CE(\mathfrak{g}//\mathfrak{h})}$ by 

$$
  d_{CE(\mathfrak{g}//\mathfrak{h})} 
   \colon 
  \omega \mapsto 
  d_{dR}\omega - F^a \iota_{t_a} \omega
$$

(e.g. [Kalkman 93 (1.15)](#Kalkman93)).

The resulting [[dg-algebra]] $(\Omega^\bullet(G,\mathfrak{h}^\ast[1])^G, d_{CE}(\mathfrak{g}//\mathfrak{h}))$ is called the **Cartan model** of $H$-equivariant de Rham cohomology of $G$.

Observe that in the special case that $X = G$ equipped with its canonical right [[action]] of $H \coloneqq G$ on itself, this construction reduces to that of the [[Weil algebra]] $W(\mathfrak{g})$, whose cohomology is trivial (is concentrated in degree 0, where it is $\mathbb{R}$).

#### The Kalkman model
 {#TheKalkmanModel}

([Kalkman 93, section 3](#Kalkman93))

(...)


## Related concepts

* [[gauged WZW model]]

* [[action Lie algebroid]], [[BRST complex]]

## References
  {#References}

The Weil model is discussed for instance in 

* {#AtiyahBott84} [[Michael Atiyah]], [[Raoul Bott]], _The moment map and equivariant cohomology_. Topology 23, 1 (1984)
 

A good account of the Cartan model is in 

* {#MathaiQuillen86} [[Varghese Mathai]], , [[Daniel Quillen]], _Superconnections, Thom classes and equivariant differential forms_, Topology 25, 85 (1986) 
 

A review of the Weil model and the Cartan model and the introduction of the "BRST model" (Kalkman model) is in

* {#Kalkman93} Jaap Kalkman, _BRST model applied to symplectic geometry_, Ph.D. Thesis, Utrecht, 1993 ([arXiv:hep-th/9308132](http://cds.cern.ch/record/568522/files/9308132.pdf) (original ArXiv pdf broken)), published versions at  ([projectEuclid](http://projecteuclid.org/euclid.cmp/1104252784))

Discussion in the context of the [[gauged WZW model]] includes

* {#Witten92} [[Edward Witten]], appendix of _On holomorphic factorization of WZW and coset models_,  Comm. Math. Phys. Volume 144, Number 1 (1992), 189-212. ([EUCLID](http://projecteuclid.org/euclid.cmp/1104249222))

* {#FigueroaOFarrillStanciu94} [[José Figueroa-O'Farrill]], S Stanciu, _Gauged Wess-Zumino terms and Equivariant Cohomology_, Phys.Lett. B341 (1994) 153-159 ([arXiv:hep-th/9407196](http://arxiv.org/abs/hep-th/9407196))

* [[José de Azcárraga]],  J. C. Perez Bueno, _On the general structure of gauged Wess-Zumino-Witten terms_ ([arXiv:hep-th/9802192](http://arxiv.org/abs/hep-th/9802192))
  
 

[[!redirects Weil model]]
[[!redirects Weil models]]
[[!redirects Cartan model]]
[[!redirects Cartan models]]
[[!redirects Kalkman model]]
[[!redirects Kalkman models]]

[[!redirects Weil model for equivariant cohomology]]
[[!redirects Cartan model for equivariant cohomology]]
[[!redirects Kalkman model for equivariant cohomology]]