
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

Let 

1. $X$ be a [[smooth manifold]] with [[de Rham algebra]] denoted $\big( \Omega^\bullet(X), d_{dR} \big)$,

1. $G$ a [[Lie group]] with [[Lie algebra]] denoted $\big(\mathfrak{g}, [-,-]\big)$,

1. $X \times G \overset{\rho}{\longrightarrow} X$ a [[smooth function|smooth]] [[action]] of $G$ on $X$.



Various [[dg-algebras]] are used to model the corresponding $G$-equivariant de Rham cohomology $X$, known as 

* _[the Weil model](#TheWeilModel)_

* _[the Kalkman model](#TheKalkmanModel)_

* _[the Cartan model](#TheCartanModel)_


#### The Weil model
 {#TheWeilModel}


Let $\big( W(\mathfrak{g}), d_W \big)$ denote the [[Weil algebra]] of $\mathfrak{g}$. If $\{t_a\}$ is a [[linear basis]] for $\mathfrak{g}$ 

\[
  \label{LinearBasisForG}
  \mathfrak{g}
  \;=\;
  span\big(  \{t_a\} \big)
\]

with induced structure constants for the [[Lie bracket]] being $\big\{f_{b c}^a\big\}_{a,b,c}$ 

$$
  [t_a, t_b] \;=\; f_{a b}^c t^b \wedge t^c
$$

(using the [[Einstein summation convention]] throughout)

then the [[Weil algebra]] is the [[dgc-algebra]] explicitly given by [[generators and relations]] as follows:

\[
  \label{ExplicitWeilAlgebra}
  W(\mathfrak{g})
  \;\coloneqq\;
  \mathbb{R}\big[ 
    \{ 
      \underset
        { deg = 1 }
        {
          \underbrace{ t^a } 
        }
      \}_a,
    \{ 
      \underset
        { deg = 2 }
        {
          \underbrace{ r^a } 
        }
      \}_a
  \big]
  \Big/
  \left(
    \begin{aligned}
      d_W \, t^a & =  - \tfrac{1}{2}f^a_{b c} t^b \wedge t^c + r^a
      \\
      d_W \, r^a & = f^a_{b c} t^b \wedge r^c
    \end{aligned}
  \right)
\]

Now consider the [[tensor product of algebras|tensor product of]] [[dgc-algebras]] of the [[de Rham algebra]] of $X$ with the [[Weil algebra]] of $\mathfrak{g}$

\[
  \label{TensorProductOfdeRhamAlgebraWithWeilAlgebra}
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g}), 
    \, 
    d_{dR} + d_W
  \Big)  
  \,.
\]

On this consider the following joint [[Cartan calculus]] operations: for each basis element $t_a$ (eq:LinearBasisForG) a graded [[derivation]] of degree -1 (contraction)

\[
  \label{WeilModelContractionOperation}
  \iota_a
  \;\colon\;
  \Big(
    \Omega
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)^\bullet
  \longrightarrow
  \Big(
    \Omega
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)^{\bullet - 1 }
\]

and a graded derivation of degree 0 (generalized [[Lie derivative]])

\[
  \label{WeilModelLieDerivative}
  \mathcal{L}_a
  \;\colon\;
  \Big(
    \Omega
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)^\bullet
  \longrightarrow
  \Big(
    \Omega
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)^{\bullet}
\]

defined on $\omega \in \Omega^\bullet(X)$ any [[differential form]] and $t^a, r^a$ as in (eq:ExplicitWeilAlgebra) as follows

\[
  \label{WeilModelContractionOnGenerators}
  \iota_a \;\colon\;
  \left\{
    \begin{aligned}
      \omega & \mapsto \iota_{v^a} \omega
      \\
      t^b &\mapsto \delta^a_b
      \\
      r^b & \mapsto 0
    \end{aligned}
  \right.
\]

and

\[
  \label{WeilModelLieDerivativeOnGenerators}
  \mathcal{L}_a 
  \;\colon\;
  \left\{
    \begin{aligned}
      \omega & \mapsto \mathcal{L}_{v^a} \omega
      \\
      t^b &\mapsto f_{a c}^b t^c
      \\
      r^b & \mapsto f_{a c}^b r^c
    \end{aligned}
  \right.
\]


where 

$$
  v^a
  \;\colon\;
  X 
  \overset{
    \big( (e,t_a), 0 \big)
  }{\hookrightarrow}
  T G \times T X
  \simeq
  T ( G \times X )
  \overset{ d \rho } {\longrightarrow}
  T X
$$

is the [[vector field]] on $X$ which is the [[derivative]] of the [[action]] $\rho$ of $G$ along the [[Lie algebra]]-element $t_a \in \mathfrak{g} \simeq T_e G$, 

and where $\iota_{v^a}$ is ordinary contraction of [[vector fields]] into [[differential forms]] and $\mathcal{L}_{v^a} = [d_{dR}, \iota-{v^a}]$ is [[Lie derivative]] of differential forms.

With this one defines the sub-[[dgc-algebra]] of _basic differential forms_, which are those in the joint [[kernel]] of all these derivations (eq:WeilModelContractionOperation) and (eq:WeilModelLieDerivative)

$$
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)_{basic}
  \overset{
    ker\big( \{\iota_a\}_a, \{\mathcal{L}_a\}_a \big)
  }{\hookrightarrow}
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)_{basic}
$$

Since the [[differential]] $d_{dR} + d_W$ (eq:TensorProductOfdeRhamAlgebraWithWeilAlgebra) graded-commutes with $\iota_a$ to $\mathcal{L}_a$ (by definition and by [[Cartan's magic formula]]) and hence graded-commutes with the [[Lie derivative]] $\mathcal{L}_a$ itself, it restricts to this joint [[kernel]], thus defining a sub-[[dgc-algebra]] (just no longer [[semi-free dg-algebra|semi-free]], in generaL)

\[
  \label{WeilModel}
  \Big(
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)_{basic}
  , 
  d_{dR} + d_W
  \Big)
\]

This [[dgc-algebra]] is called the _Weil model_ for $G$-equivariant de Rham cohomology of $X$. 

([Atiyah-Bott 84](#AtiyahBott84), see e.g. [Kalkman 93, Sec.2.1](#Kalkman93), [Miettinen 96, Sec. 2](#Miettinen96)).


#### The Kalkman/BRST model
 {#TheKalkmanModel}

Consider the Weil model (eq:WeilModel) but equipped instead with the alternative [[differential]]

$$
  d_{K}
  \;\coloneqq\;
  d
  \;+\;
  d_W
  \;+\;
  t^a \wedge \mathcal{L}_a
  \;-\;
  r^a \wedge \iota_a
$$

with $t^a$, $r^a$ from (eq:ExplicitWeilAlgebra) and $\iota_a$ from (eq:WeilModelContractionOnGenerators) and $\mathcal{L}_a$ from (eq:WeilModelLieDerivativeOnGenerators).

This [[dgc-algebra]]

\[
  \label{WeilModel}
  \Big(
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)_{basic}
  , 
  d_K
  \coloneqq
  d_{dR} + d_W 
  +
  t^a \wedge \mathcal{L}_a
  -
  r^a \wedge \iota_a
  \Big)
\]

is called the _[[BRST-complex|BRST]]-model_ in ([Kalkman 93, section 3](#Kalkman93), see e.g. [Miettinen 96](#Miettinen96)) or now the _Kalkman model_ by some authors, for the $G$-equivariant de Rham cohomology of $X$.

This is [[quasi-isomorphism|quasi-isomorphic]] to the Weil model (eq:WeilModel), the [[quasi-isomorphism]] given by [[conjugation]] with the [[exponential]] $exp\big(  t^a \wedge \iota_a \big)$ ([Kalkman 93, section 3](#Kalkman93))

$$
  \begin{aligned}
    d_K
    \;=\;
    \exp\big(  -t^a \wedge \iota_a \big)
    \big(
      d_{dR} + d_W 
    \big)
    \exp\big( t^a \wedge \iota_a \big)
  \end{aligned}
$$

(...)


#### The Cartan model
 {#TheCartanModel}

reviews include ([Mathai-Quillen 86](#MathaiQuillen86), [Kalkman 93, section 2.2](#Kalkman93))



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



## Related concepts

* [[gauged WZW model]]

* [[action Lie algebroid]], [[BRST complex]]

## References
  {#References}

Review is in 

* Oliver Goertsches, Leopold Zoller, _Equivariant de Rham Cohomology: Theory and Applications_, São Paulo J. Math. Sci. (2019) ([arXiv:1812.09511](https://arxiv.org/abs/1812.09511), [doi:10.1007/s40863-019-00129-4](https://doi.org/10.1007/s40863-019-00129-4))

Early discussion of the Weil model includes

* {#AtiyahBott84} [[Michael Atiyah]], [[Raoul Bott]], _The moment map and equivariant cohomology_, Topology 23, 1 (1984) (<a href="https://doi.org/10.1016/0040-9383(84)90021-1">doi:10.1016/0040-9383(84)90021-1</a>, [pdf](https://www.math.stonybrook.edu/~mmovshev/MAT570Spring2008/BOOKS/atiyahbott_moment.pdf))
 

A good account of the Cartan model is in 

* {#MathaiQuillen86} [[Varghese Mathai]], [[Daniel Quillen]], _Superconnections, Thom classes and equivariant differential forms_, Topology 25, 85 (1986)  (<a href="https://doi.org/10.1016/0040-9383(86)90007-8">doi:10.1016/0040-9383(86)90007-8</a>)
 

A review of the Weil model and the Cartan model and the introduction of the "BRST model" (Kalkman model) is in

* {#Kalkman93} Jaap Kalkman, _BRST model applied to symplectic geometry_, Ph.D. Thesis, Utrecht, 1993 ([arXiv:hep-th/9308132](https://arxiv.org/abs/hep-th/9308132), [cds:9308132](http://cds.cern.ch/record/568522), [euclid:1104252784](http://projecteuclid.org/euclid.cmp/1104252784))

  (original arXiv pdf broken)

Discussion in the broader context of [[equivariant cohomology|equivariant]] [[differential cohomology]] is in

* Andreas Kübel, [[Andreas Thom]], _Equivariant Differential Cohomology_, Transactions of the American Mathematical Society (2018) ([arXiv:1510.06392](https://arxiv.org/abs/1510.06392))
 

Discussion in the context of the [[gauged WZW model]] includes

* {#Witten92} [[Edward Witten]], appendix of _On holomorphic factorization of WZW and coset models_,  Comm. Math. Phys. Volume 144, Number 1 (1992), 189-212. ([EUCLID](http://projecteuclid.org/euclid.cmp/1104249222))

* {#FigueroaOFarrillStanciu94} [[José Figueroa-O'Farrill]], S Stanciu, _Gauged Wess-Zumino terms and Equivariant Cohomology_, Phys.Lett. B341 (1994) 153-159 ([arXiv:hep-th/9407196](http://arxiv.org/abs/hep-th/9407196))

* [[José de Azcárraga]],  J. C. Perez Bueno, _On the general structure of gauged Wess-Zumino-Witten terms_ ([arXiv:hep-th/9802192](http://arxiv.org/abs/hep-th/9802192))

Discussion in view of [[supersymmetry]]:

* {#Miettinen96} Mauri Miettinen, _Weil Algebras and Supersymmetry_ ([arXiv:hep-th/9612209](https://arxiv.org/abs/hep-th/9612209), [cds:317377](http://cds.cern.ch/record/317377), [spire:427720](http://inspirehep.net/record/427720))

* {#GuilleminSternberg99} [[Victor Guillemin]], [[Shlomo Sternberg]], _Supersymmetry and equivariant de Rham theory_, Springer, (1999) ([doi:10.1007/978-3-662-03992-2](https://link.springer.com/book/10.1007/978-3-662-03992-2))
  
 

[[!redirects Weil model]]
[[!redirects Weil models]]
[[!redirects Cartan model]]
[[!redirects Cartan models]]
[[!redirects Kalkman model]]
[[!redirects Kalkman models]]

[[!redirects Weil model for equivariant cohomology]]
[[!redirects Cartan model for equivariant cohomology]]
[[!redirects Kalkman model for equivariant cohomology]]