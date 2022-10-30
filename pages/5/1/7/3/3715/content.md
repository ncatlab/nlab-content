


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Deformation quantization_ is one formalization of the general idea of [[quantization]] of a [[classical mechanical system]]/[[classical field theory]] to a [[quantum mechanical system]]/[[quantum field theory]].

Deformation quantization focuses on the [[algebras of observables]] of a physical system (hence on the [[Heisenberg picture]]): it provides rules for how to [[deformation theory|deform]] the commutative algebra of classical observables to a non-commutative algebra of quantum observables. (This is in contrast to [[geometric quantization]], which focuses on the [[spaces of states]] and hence on the [[Schrödinger picture]].)

Usually and traditionally, _deformation quantization_ refers to (just) _formal_ deformations, in the sense that it produces [[formal power series]] expansions in a formal parameter $\hbar$ (physically: [[Planck's constant]]) of the product in the deformed algebra of observables. 

| [[classical mechanics]] | [[semiclassical approximation]] |  ... | [[formal deformation quantization]] | [[quantum mechanics]] |
|--|--|--|--|--|
| $\mathcal{O}(\hbar^0)$ | $\mathcal{O}(\hbar^1)$ | $\mathcal{O}(\hbar^n)$ | $\mathcal{O}(\hbar^\infty)$  |  |

(This is related to [[perturbation theory]], which is about [[formal power series]] in [[coupling constants]], instead of in [[Planck's constant]].)


But there are refinements of this to [[C-star algebraic deformation quantization]] which studies the proper deformation to a genuine [[C-star algebra]] of observables. (This in turn is related to genuine [[geometric quantization]] via the notion of [[geometric quantization of symplectic groupoids]].)

One can, therefore, argue that only [[C-star algebraic deformation quantization|strict deformation quantization]] is genuine [[quantization]]. For instance in ([Gukov-Witten 09, section 1.4](#GukovWitten09)) it says

> Generally speaking, [[physics]] is based on $[$ strict $]$ quantization, rather than $[$ formal $]$ deformation quantization, although conventional quantization sometimes leads to problems that can be treated by deformation quantization.


As other methods of quantization, deformation quantization has as input a description of a [[classical mechanical system]], which is in this case most often a smooth [[Poisson manifold]]. The deformation quantization replaces the algebra of [[smooth functions]] on the Poisson manifold with the same [[vector space]], but equipped with new noncommutative [[associative algebra|associative unital product]] whose [[commutator]] agrees, up to order $\hbar$, with the underlying [[Poisson bracket]]. Of course the proper study of quantization of Poisson manifolds studied the appropriate notion at the level of [[sheaves]] of algebras. Gluing local solutions to the quantization problem furthermore involves [[stacks]] and specifically [[gerbes]].  

## Definition

If the result of deformation quantization is an algebra over the [[power series]] [[ring]] $\mathbb{R}[ [ \hbar ] ]$ of a formal parameter $\hbar$ (thought of as [[Planck's constant]]) such that the limit $\hbar \to 0$ reproduces the starting point of the deformation, then one speaks of 

* [Formal deformation quantization](#FormalDeformationQuantization)

In much of the literature this is regarded as the default meaning of "deformation quantization". But this is really the case corresponding to [[perturbation theory]] in [[quantum field theory]]. A "genuine" or "strict" deformation quantization 

* [Strict deformation quantization](#StrictDeformationQuantization)

is supposed to result in a non-formal deformation, which in terms of the above formal power series at least means that one can set $\hbar = 1$ such that all expressions in $\hbar$ converge, but which in general is taken to mean something stronger, such as that there is a continuous field of [[C-star algebraic deformation quantization]].


### Formal deformation quantization
 {#FormalDeformationQuantization}

We first give the traditional

* [Explicit definition of traditional deformation quantization](#ExplicitDefinitionOfTraditionalDeformationQuantization)

of a [[Poisson manifold]]/[[Poisson algebra]]. Thought of in terms of [[physics]] this describes a [[quantization]] of a [[physical system|system]] of [[quantum mechanics]], as opposed to full [[quantum field theory]]. 

More abstractly, this may be formulated and generalized in terms of lifts of [[algebras over an operad]] over a [[P-n operad]] to a [[BD-n operad]] and hence an [[E-n operad]], for $n = 1$. This we discuss in 

* [Formulation as lifts from P-n algebras to BD-n algebras](#FormulationAsLiftsFromPnAlgebrasToBDAlgebras)

In this formulation one sees that for genral $n$ the construction applies  to $n$-dimensional [[quantum field theory]] (with [[quantum mechanics]] for $n = 1$ be 1-dimensional quantum field theory, for instance the [[sigma-model]] "on the [[worldline]]" of a [[particle]]). A formulation of deformation quantization to _[[local quantum field theory|local]]_ quantum field theory formulated in terms of [[factorization algebras of observables]] over [[spacetime]]/[[worldvolume]] is then discussed in

* [Deformation quantization of field theory to factorization algebras of observables](#DeformationQuantizationToFactotrizationAlgebras)


#### Explicit definition of deformation of Poisson manifolds/Poisson algebras
 {#ExplicitDefinitionOfTraditionalDeformationQuantization}

Let $M$ be a [[Poisson manifold]] and let $A = C^\infty(M)$ be the [[Poisson algebra]] of smooth functions.

+-- {: .num_defn}
###### Definition
A **$\ast$-product** ([[star product]]) on $A$ is a product on the 
[[power series]] $A [ [ t ] ]$ that is (1) bilinear over $\mathbb{R}[ [ t ] ]$, (2) associative, and (3) for $a,b \in A$ it can be written out as a [[formal power series]]
\[ a \ast b = \sum_{n=0}^\infty B_n(a,b) t^n \]
where $B_n$ are bilinear maps on $A$ such that $B_0(a,b) = ab$.
=--

+-- {: .num_defn}
###### Definition
A (formal) **deformation quantization** of $M$ is a [[star product]] on $A = C^\infty(M)$ such that the [[Poisson bracket]] $\{a,b\} = B_1(a,b) - B_1(b,a)$ for $a,b \in A$; by bilinearity over $\mathbb{R}[ [ t ] ]$, this characterizes it.
=--


#### Formulation as lifts from $P_n$-algebras to $BD_n$-algebras and $E_n$-algebras
 {#FormulationAsLiftsFromPnAlgebrasToBDAlgebras}
 
(...)

([Costello-Gwilliam, section 2.3, 2.4](#CostelloGwilliam))

(...)

[[!include deformation quantization - table]]

#### Deformation quantization of field theory to factorization algebras of observables
 {#DeformationQuantizationToFactotrizationAlgebras}

(...)


([Costello-Gwilliam, chapter 5](#CostelloGwilliam))

(...)

### Strict deformation quantization
 {#StrictDeformationQuantization}

(...)
[[C-star algebraic deformation quantization]]
(...)

## Properties

### Existence results

[[Vladimir Drinfel'd]] has sketched a proof (and gave main ingredients) to show that every [[Poisson Lie group]] can be deformation quantized to a [[Hopf algebra]]; this proof has been completed by Etingof and Kazhdan. [[Maxim Kontsevich]] proved a certain *[[Kontsevich formality|formality theorem]]* (formality is here in the sense of _[[formal dg-algebra]]_ in [[rational homotopy theory]]) whose main corollary (and motivation) was the statement that every [[Poisson manifold]] has a deformation quantization ([Kontsevich 97](#Kontsevich97)). 

For [[symplectic manifolds]] and those [[Poisson manifolds]] that have a [[regular foliation]] by [[symplectic leafs]], the theory of deformation quantization is much simpler; [[Boris Fedosov]] gave a construction of [[star products]] on symplectic manifolds using [[symplectic connections]] on [[smooth manifolds]] ([Fedosov 94](#Fedosov94)).  An analogous argument was given by [[Roman Bezrukavnikov]] and [[Dmitry Kaledin]] in the context of an algebraic symplectic form ([BK 04](#BK)).  

+-- {: .standout}
Caution: the following are rough notes from a talk by [[J.D.S. Jones]] (Cambridge, 8.1.2013); there are probably many typos and sign errors.
=--

#### Deformation of Poisson manifolds


+-- {: .num_theorem #Kontsevich}
###### Theorem
**(Kontsevich)**.  Every [[Poisson manifold]] has a (formal) deformation quantization.

=--

This was shown in ([Kontsevich 97](#Kontsevich97)). There the deformed product is constructed by a kind of [[Feynman diagram]] [[perturbation series]]. Later this was identified as the perturbation series of the [[Poisson sigma-model]] for the given Poisson manifold. See there for more details.

#### Gerstenhaber's deformation theory by Hochschild (co)homology

Let $V$ be a $k$-vector space and consider $C^p(V,V) = \Hom(V^{\otimes p}, V)$.  We define a "circle operator" $\circ$ as follows: for $f \in C^p(V,V)$ and $g \in C^q(V,V)$, we define $f \circ g \in C^{p+q-1}(V,V)$ as the map
\[ (f \circ g)(v_1, \ldots v_{p+q-1}) = f(v_1, \ldots, v_{i-1}, g(v_i, \ldots, v_{i+q-1}), v_{i+q}, \ldots, v_{p+q-1}). \]

For $f \in C^\ast(V,V)$, let $A_f(g,h) = (f \circ g) \circ h - f \circ (g \circ h)$.  (This is graded symmetric.)  It follows that the commutator of $\circ$ is given by
\[ [f,g] = f \circ g - (-1)^{(|f| - 1)(|g|-1)} g \circ f \]
where $|f| = p$ when $f \in C^p(V,V)$.  This defines a _graded [[Lie bracket]]_ of degree -1.

+-- {: .num_example}
###### Example
Let $\mu \in C^2(V,V)$ ($\mu : V \otimes V \to V$).  Note that $\mu$ is associative iff $\mu \circ \mu = 0$ iff $[\mu, \mu] = 0$.  Let $d_\mu : C^{p}(V,V) \to C^{p+1}(V,V)$ be defined by $d_\mu(x) = \mu \otimes x \pm x \otimes \mu = [\mu, x]$.  We have $d_\mu \circ d_\mu = 0$ so $(C^\ast(V,V), d_\mu)$ becomes a [[differential graded algebra]].  In fact this is the [[Hochschild cochain complex]] of the [[associative algebra]] $A = (V, \mu)$.
=--

Apply this example to the construction of deformation quantization.  The star product is uniquely determined by $\theta : A \otimes A \to A[ [ t ] ]$ given by $\theta(a,b) = ab + c(a,b)$.  What we want is that
\[ (\mu + c) \otimes (\mu + c) = 0; \]
write this out and we get the equation
\[ d_\mu c + c \circ c = 0, \]
or $d_\mu c + \frac{1}{2}[c,c] = 0$; this is the [[Maurer-Cartan equation]].  Hence we are looking for solutions of the M-C equation but in the Hochschild complex $C^\ast(A,A)[ [ t ] ]$.  One should note that $d_\mu$ is actually a [[derivation]] of the [[Lie bracket]], hence we have a [[dg-Lie algebra]].

+-- {: .num_theorem #HKR}
###### Theorem
**([[HKR theorem]])**. $HH^p(A,A) = \Gamma(M, \Lambda^p TM)$.
=--

(Note that $C^p(C^\infty(M),C^\infty(M))$ should be interpreted as $\Hom_{diff}(C^\infty(M), C^\infty(M))$.)  Under this isomorphism the Poisson bracket is mapped to the [[Poisson tensor]]:
\[ \{ \cdot , \cdot \} \in HH^2(A,A) \quad \mapsto \quad P \in \Gamma(M, \Lambda^2 TM). \]
The bracket in Hochschild cohomology ([[Gerstenhaber bracket]]) goes to the [[Schouten bracket]]:
\[ [ \cdot , \cdot ]_G \quad \mapsto \quad [ \cdot, \cdot ]_S. \]

For vector fields $\xi$ and $\eta$, the [[Schouten bracket]] satisfies (1) $[\xi,\eta]_S = [\xi,\eta]$ (the Lie bracket), and (2) $[\alpha, \beta \wedge \gamma] = [\alpha,\beta] \wedge \gamma \pm [\alpha,\gamma] \wedge \beta$; note that this completely determines it (everything is locally given by wedges...).

In the Hochschild cohomology $HH^\ast(A,A)$ of $A$, $d_\mu P \mapsto 0$ and $[P,P]_S = 0$, so _we have a solution to M-C in $H^\ast(A,A)[ [ t ] ]$_.

#### In terms of differential graded Lie algebras

+-- {: .num_defn}
###### Definition
Let $L_1$ and $L_2$ be [[differential graded Lie algebras]] (dgL).  A **[[quasi-isomorphism]]** $f : L_1 \to L_2$ is a homomorphism of dgLs that induces an isomorphism on homology.  $L_1$ and $L_2$ are **quasi-isomorphic** if there exists $M$ with quasi-isomorphisms $L_1 \leftarrow M \rightarrow L_2$.  It can be verified that this is an equivalence relation.
=--

+-- {: .num_theorem #KontsevichDeformationTheorem}
###### Theorem
**([[Kontsevich]])**.  If $L_1$ is quasi-isomorphic to $L_2$ then there is a solution to the M-C equation in $L_1$ iff there is a solution to the M-C equation in $L_2$.
=--

+-- {: .num_theorem #KontsevichFormality}
###### Theorem
**([[Kontsevich formality]])**.  $C^\ast(A,A)[ [ t ] ]$ is quasi-isomorphic to $H^\ast(A,A)[ [ t ] ]$.  ($A = C^\infty(M)$)
=--

Hence there is a solution to M-C in $C^\ast(A,A)[ [ t ] ]$, and hence there is a deformation quantization (!).

#### The Deligne conjecture

We have $(C^*(A,A), d_\mu)$, the [[Gerstenhaber bracket]], and we also have a [[cup product]]
\[ (f \cup g) (a_1, \ldots, a_{p+q}) = \mu(f(a_1,\ldots,a_p), g(a_{p+1},\ldots,a_{p+q})) \]
for $f : A^{\otimes p} \to A$, $g : A^{\otimes q} \to A$; this satisfies also $d_\mu(f \cup g) = (d_\mu f) \cup g \pm f \cup d_\mu g$.  
The [[Deligne conjecture]] gives a relationship between these things.

In $HH^*(A,A)$, we have:

1. $[\cdot, \cdot]$ is a graded Lie bracket of degree -1.
1. The cup product $\cup$ is graded commutative.
1. The [[Jacobi identity]] for $[\cdot,\cdot]$.
1. $[a, b \cup c] = [a,b] \cup c \pm [a,c] \cup b$.

Such a thing is called a [[Gerstenhaber algebra]].  Note that we do not have these relations in $C^*(A,A)$, they are only true modulo boundaries.

+-- {: .num_theorem #Deligne}
###### Theorem
**([[Deligne conjecture]])**.  $C^*(A,A)$ is a $G_\infty$-algebra, which is a Gerstenhaber algebra _up to coherent homotopy_.
=--

### Motivic Galois group action on the space of quantizations
 {#MotivicGaloisGroup}

In ([Kontsevich 99](Kontsevich99)) it was indicated that a [[quotient group]] of the [[motivic Galois group]] apparently equivalent to the [[Grothendieck-Teichmüller group]] naturally [[action|acts]] on the space of formal deformation quantizations of a finite dimensional manifold. See also at _[[cosmic Galois group]]_.

This has been formalized as follows. The formal deformation quantization of ([Kontsevich 97](#Kontsevich97)) is all induced by the [[Kontsevich formality]] theorem, which states that ober suitable [[manifolds]]/[[varieties]] $X$ there is an [[equivalence]] of [[L-∞ algebras]] 


$$
  \mathcal{X}(X) \stackrel{\simeq}{\to} C^\bullet(X)
$$

identifying the [[multivector fields]] on $X$ with the [[Hochschild cohomology]] complex (of its [[function algebra]]).  Every choice of such an equivalence induces one formal deformation quantization of a [[Poisson manifold]] $X$, and the two quantizations induced by two equivalent (homotopic) equivalences are in turn equivalent.

Therefore one may regard the [[∞-groupoid]] $Maps^{L_\infty}_{equiv}(\mathcal{X}(X), C^\bullet(X))$ as the "space of formal deformation quantizations" of $X$.

In ([Dolgushev 1109, theorem 6.2](#Dolgushev1109), [Dolgushev 1111, theorem 3.1](#Dolgushev1111)) it is shown that the set $\pi_0 Maps^{L_\infty}_{equiv}(\mathcal{X}(X), C^\bullet(X))$ of connected components of this space is, up to a choice of basepoint, the [[Grothendieck-Teichmüller group]], hence is a [[torsor]] over that group. 

(This is based on identifications of the GRT Lie algebra with the degree-0 [[chain cohomology]] of the [[graph complex]], due to [[Thomas Willwacher]]. See at _[Grothendieck-Teichm&#252;ller group -- relation to the graph complex](Grothendieck-Teichm%C3%BCller+tower#RelationToTheGraphComplex)_.

Aspects of the generalization of this statement to more general spaces then $\mathbb{R}^n$ are discussed in [Dolgushev-Rogers-Willwacher 12](#DolgushevRogersWillwacher12).

For discussion of [[motive|motivic structures]] in [[geometric quantization]] see at _[[motivic quantization]]_.

## Examples

* [[Moyal quantization]]

## Related concepts

* [[reductions deformations resolutions in physics]]

* [[quantization]]

  * **deformation quantization**, [[geometric quantization]]

  * [[path integral]]

  * [[semiclassical approximation]]

* [[Jordan algebra]]

[[!include Isbell duality - table]]

[[!include infinitesimal and local - table]]

## References

Deformation quantization of [[symplectic manifolds]] and varieties and also of [[Poisson manifolds]] that have a [[regular foliation]] by [[symplectic leaves]] is discussed in 

* [[Boris Fedosov]], _Formal quantization_, Some Topics of Modern Mathematics and their Applications to Problems of Mathematical Physics (in Russian), Moscow (1985), 129-
136.

* [[Boris Fedosov]], _Index theorem in the algebra of quantum observables_, Sov. Phys. Dokl. 34 (1989), 318-321.

* [[Boris Fedosov]], _A simple geometrical construction of deformation quantization_  J. Differential Geom. Volume 40, Number 2 (1994), 213-238. ([EUCLID](http://projecteuclid.org/euclid.jdg/1214455536))
 {#Fedosov94}

For algebraic forms this is discussed in

* [[Roman Bezrukavnikov]], [[Dmitry Kaledin]], _Fedosov quantization in algebraic context_ Mosc. Math. J., Volume 4, Number 3, (2004) 559&#8211;592 ([AMS pdf](http://www.ams.org/distribution/mmj/vol4-3-2004/bezrukavnikov-kaledin.pdf))
 {#BK09}

More discussion of this approach is in 

* Claudio Emmrich, [[Alan Weinstein]], _The differential geometry of Fedosov's quantization_ ([arXiv:hep-th/9311094](http://arxiv.org/abs/hep-th/9311094))

A direct and general formula for the deformation quantization of any Poisson manifold was given in 

* [[Maxim Kontsevich]], _Deformation quantization of Poisson manifolds_,  Lett. Math. Phys. __66__ (2003),  no. 3, 157--216, ([arXiv:q-alg/9709040](http://arxiv.org/abs/q-alg/9709040)).
 {#Kontsevich97}

This secretly uses the [[Poisson sigma-model]] (see there for more details) induced by the given target [[Poisson Lie algebroid]].

The classification of the space of such formal deformation quantization is discussed in 

* [[Vasily Dolgushev]], _Stable Formality Quasi-isomorphisms for Hochschild Cochains I_ ([arXiv:1109.6031](http://arxiv.org/abs/1109.6031))
 {#Dolgushev1109}

* [[Vasily Dolgushev]], _Exhausting formal quantization procedures_ ([arXiv:1111.2797](http://arxiv.org/abs/1111.2797))
 {#Dolgushev1111}

* [[Vasily Dolgushev]], [[Christopher Rogers]], [[Thomas Willwacher]], _Kontsevich's graph complex, GRT, and the deformation complex of the sheaf of polyvector fields_ ([arXiv:1211.4230](http://arxiv.org/abs/1211.4230))
 {#DolgushevRogersWillwacher12}

See also 

* MO discussion , _[Kontsevich's conjectures on the Grothendieck-Teichm&#252;ller group?](http://mathoverflow.net/questions/42148/kontsevichs-conjectures-on-the-grothendieck-teichmuller-group)_


Deformation quantization in [[quantum field theory]] in the context of [[AQFT]] is discussed in

* [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic quantum field theory and deformation quantization_
Proceedings of the Conference on Mathematical Physics in Mathematics and Physics, Siena June 20-25 (2000) ([arXiv:hep-th/0101079](http://xxx.uni-augsburg.de/abs/hep-th/0101079)) 



The relation [[geometric quantization]] is discussed in

* [[Eli Hawkins]], _The Correspondence between Geometric Quantization and Formal Deformation Quantization_ ([arXiv:math/9811049](http://arxiv.org/abs/math/9811049))

* Christoph N&#246;lle, _Geometric and deformation quantization_ ([arXiv:0903.5336](http://arxiv.org/abs/0903.5336))

and some remarks on the relation are also in section 1.4 of

* [[Sergei Gukov]], [[Edward Witten]], _Branes and Quantization_, Adv. Theor. Math. Phys. 13 (2009) 1&#8211;73, ([arXiv:0809.0305](http://arxiv.org/abs/0809.0305), [euclid](http://projecteuclid.org/euclid.atmp/1282054099))
 {#GukovWitten09}

which is about [[quantization via the A-model]].

The formulation of deformation quantization as lifts from [[P-n operads]] over [[BD-n operads]] to [[E-n operads]] is discussed in section 2.3 and 2.4 of

*[[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in perturbative quantum field theory_ ([wiki](http://math.northwestern.edu/~costello/factorization_public.html), early/partial draft [pdf](http://math.northwestern.edu/~gwilliam/factorization.pdf))
 {#CostelloGwilliam}



See also

* [wikipedia](http://en.wikipedia.org/wiki/Weyl_quantization#Deformation_quantization)
* F. Bayen, M. Flato, C. Fronsdal, A. Lichnerowicz, D. Sternheimer, _Quantum mechanics as a deformation of classical mechanics_, Lett. Math. Phys. 1 (1975/77), [MR674337](http://www.ams.org/mathscinet-getitem?mr=674337), [doi](http://dx.doi.org/10.1007/BF00399745);  _Deformation theory and quantization. I. Deformations of symplectic structures_, Ann. Physics 111 (1978), no. 1, 61&#8211;110, [MR496157](http://www.ams.org/mathscinet-getitem?mr=496157); _Deformation theory and quantization. II. Physical applications_, Ann. Physics 111 (1978), no. 1, 111&#8211;151, [MR496158](http://www.ams.org/mathscinet-getitem?mr=496158)
* M. Flato, A. Lichnerowicz, D. Sternheimer, _Deformations of Poisson brackets, Dirac brackets and applications_, J. Math. Phys. __17__ (1976), no. 9, 1754&#8211;1762, [MR420723](http://www.ams.org/mathscinet-getitem?mr=420723), [doi](http://dx.doi.org/10.1063/1.523104)
* D. Arnal, J.-C. Cortet, _$\ast$-products in the method
of orbits for nilpotent groups_, J. Geom. Phys. 2 (1985), no. 2,
83&#8211;116, <a href="http://dx.doi.org/10.1016/0393-0440(85)90010-5">doi</a>

On the [[stack]] of deformation quantizations:

* [[Maxim Kontsevich]], _Deformation quantization of algebraic varieties_ ([arXiv:math/0106006](http://arxiv.org/abs/math/0106006))

* Pietro Polesello, [[Pierre Schapira]], _Stacks of quantization-deformation modules on complex symplectic manifolds_ ([arXiv:math/0305171](http://arxiv.org/abs/math/0305171))

* [[Amnon Yekutieli]], _Twisted Deformation Quantization of Algebraic Varieties_ , 
[ arxiv:0905.0488 ](http://arxiv.org/abs/0905.0488)

The action of a [[motivic Galois group]] ("[[cosmic Galois group]]") on the space of deformation quantization was observed in 

* [[Maxim Kontsevich]], _Operads and Motives in Deformation Quantization_, Lett. Math. Phys.48:35-72,1999 ([arXiv:math/9904055](http://arxiv.org/abs/math/9904055))
 {#Kontsevich99}

See also at _[[motives in physics]]_.

[[!redirects deformation quantizations]]

[[!redirects algebraic deformation quantization]]

[[!redirects formal deformation quantization]]
[[!redirects formal deformation quantizations]]
