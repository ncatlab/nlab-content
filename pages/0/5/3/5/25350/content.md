+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

What is called the "geometrization of quantum mechanics" by [Kibble (1979)](#Kibble79) who introduced the idea, or "geometrical formulation of quantum mechanics" &lbrack;[Ashtekar & Schilling (1999)](#AshtekarSchilling99)&rbrack; or just "geometric quantum mechanics" &lbrack;[Brody & Hughston (2001)](#BrodyHughston01)&rbrack;, but which ought to be called the "symplectic formulation", is the observation that, in standard [[quantum mechanics]]:

1. the [[complex projective space]] $P \mathscr{H}$ of the [[Hilbert space|Hilbert]] [[space of quantum states|space of]] [[pure quantum states]] $\mathscr{H}$ is canonically a [[Kähler manifold]] (via the [[Fubini-Study metric]]) and so in particular a [[symplectic manifold]],

1. the [[curves]] in $P \mathscr{H}$ which correspond to solutions of the [[Schrödinger equation]] are [[Hamiltonian flows]] with respect to this symplectic structure.

This is fairly immediate to see from mathematical inspection, but the perspective is somewhat surprising from the point of view of standard accounts of [[classical physics|classical]]/[[quantum physics]], which tend to frame [[symplectic geometry]] and its [[Hamiltonian flows]] as the hallmark of [[classical physics|classical]] [[phase spaces]] and [[classical physics]], and to highlight [[quantization]] as a [[deformation]] of this symplectic structure (whence: "[[deformation quantization]]"). 

It follows that instead of thinking of a quantization of a symplectic manifold $(M,\omega)$ as some kind of deformation to operators on a Hilbert space, one can think of it as merely replacing the classical mechanics of $M$ with the classical mechanics of $P(\mathcal{H}).$ 

Now, the standard perspective is certainly not wrong, but various authors have inevitably suggested that the "geometrical formulation"  (more descriptive would be: "symplectic formulation") of quantum mechanics may point to some deeper truth, and if only to show some kind of conceptual unity where one is used to amplifying the dichotomy.

## Explanation

Let $(M^{2n},\omega)$ be a [[symplectic manifold]] and let $d\mu$ be a [[measure]] on $M$ (which is always of the form $h\omega^n$ for some function $h$). Let $\mathcal{L}\to M$ be a [[prequantum line bundle]] and let $\Delta:M^3\to\mathbb{C}$ be a [[smooth function]]. There is an [[equivalence of categories]] between:

1. (Path integral quantization) Quantizations obtained via a [[path integral]] over [[curves]] in $M,$ whose amplitude is given by [[parallel transport]] and whose [[3-point function]] is $\Delta.$

2. (Geometric quantization) The [[category]] of [[Hilbert spaces]] given by a [[subspace]] of [[sections]] of the [[prequantum line bundle]], such that pointwise [[evaluation]] is [[continuous function|continuous]] and whose curvature is $VE(\log{\Delta})$ ($VE$ is the [[van Est]] map).

3. (Berezin quantization) Maps $q \colon M\to P(\mathcal{H})\subset B(\mathcal{H}),$ with the overcompleteness property: $1_{\mathcal{H}} = \int_M q\,d\mu$ and whose [[3-point function]] is $\Delta.$

Item 2 presents by far the most common way of thinking about [[quantization]], with the other two (especially 1) being nearly completely overlooked. However, it can be argued that 2 is really just a way of computing 3 or 1, where the latter is the only one which really generalizes to Poisson manifolds. This is because the path integral is a section of 

$$\pi_0^*\mathcal{L}^*\otimes \pi_1^*\mathcal{L}\to M\times M\,,$$

and for [[Poisson manifolds]] we can replace $M\times M$ by the [[symplectic groupoid]]. More specifically, the path integral is a certain Hermitian, idempotent section of the twisted convolution algebra. For symplectic manifolds, it is formally given by 
$$\Omega(a,b)=\int_{\gamma(0)=a}^{\gamma(1)=b}\mathcal{D}\gamma\,P(\gamma)\in\text{Hom}(\mathcal{L}_{a},\mathcal{L}_{b})\,,
$$
where $P(\gamma)$ is parallel transport over $\gamma.$

In the most common examples, 2 is given by holomorphic sections of a [[Kähler manifold]]. In 3, $q$ is a [[classifying map]] for $\mathcal{L}$ and points in its image are called *[[coherent states]]* -- it is not just any classifying map though, it has an overcompleteness property. This is [[Felix Berezin|Berezin]]'s formulation of [[quantization]], whereas 1 is how [Klauder](#klauder) conceived of quantization. For a quote:  

> "all these different procedures to quantize phase space \[can physically\] be thought of as just different ways of regularizing and defining properly the path integral" &lbrack;[[Davide Gaiotto]], [yt](https://youtu.be/EwwGAf2K1uQ?si=eG8E6ILPOtN10obr&t=220)&rbrack;

That something like this was true seems to have been first made explicit in [Odzijewicz 1992] (#Odzijewicz92), who stated a related equivalence of categories and the relationship to path integrals.

### On Complex Projective Space

The simplest and most natural example of this is when $\mathcal{H}$ is finite dimensional and $M=P(\mathcal{H})$ with $\omega$ being the Fubini–Study form. Items 1 and 3 are very natural to describe here, while item 2 is a bit more complicated but quickly follows from the description of 1. We'll first describe item 3. 

In this example, $q$ is the identity.
It's not immediately obvious that this example satisfies the overcompleteness property, but it does with respect to the Fubini–Study measure (up to a constant). There is a natural map
$$\langle\rangle: B(\mathcal{H})\to C^{\infty}(P(\mathcal{H}))\,,\quad \langle H\rangle([v])=\langle v|H|v\rangle\,,$$
where $v$ is any normalized representative of $[v].$ This is just the expectation value of $H$ in the state $[v].$ This map (multiplied by $i$) is a morphism of Lie algebras, with respect to the commutator on $B(\mathcal{H})$ and the Poisson bracket on $P(\mathcal{H}).$ This is a bit surprising, because it is so commonly stated that there is no physically reasonable morphism of Lie algebras in the other direction, while this direction receives relatively little attention. The significance of $i\langle \rangle$ being a Lie algebra morphism is that, with respect to classical observables of the form $\langle H\rangle\,,$ the classical and quantum mechanics are the same. That is,  
$$i\frac{\partial}{\partial t}\Psi=H\Psi$$
if and only if $t\mapsto [\Psi](t)$ is the Hamiltonian flow of the Hamiltonian vector field of $\langle H\rangle.$ Equivalently, $A\in B(\mathcal{H})$ satisfies Heisenberg's equation of motion with respect to $H$ if and only if $\langle A\rangle$ satisfies Hamilton's equations of motion with respect to $\langle H\rangle.$
 
There is also a natural map from classically mixed states to quantum mixed states, ie. [[density matrix]]. It is given by
$$f\mapsto Q_f=\int_{P(\mathcal{H})}f\,q\,\omega^n\,,$$
where $f\ge 0$ and 
$$\int_{P(\mathcal{H})}f\,\omega^n=1\,.$$
From the overcompleteness property, it follows that
$$Tr(Q_{f}A)=\int_{P(\mathcal{H})} f\,\langle A\rangle \omega^n\,.$$
This means that $\langle \rangle$ also preserves the state structure. Mathematically, $\langle\rangle=Q^{\dagger},$ where the inner product is the Hilbert–Schmidt inner product. $Q_f$ is known as [[Felix Berezin|Berezin]]'s contravariant symbol, and $\langle \rangle$ is known as Berezin's covariant symbol. Of course, $Q$ is really defined on any reasonably nice function — in general it should be interpreted as an operator, not a state. $Q$ agrees with the Berezin–Toeplitz quantization, [Schlichenmaier](#Schlichenmaier).

The 3–point function (which is really a degree 2 cochain on the pair [[groupoid]] and determines a class in [[groupoid cohomology]]) determines the first [[Chern class]] of the prequantum line bundle and is given by
$$\Delta([x],[y],[z])=\langle x|y\rangle\langle y|z\rangle\langle z|x\rangle\,.$$ 
This is the same 3–point function that appears in the [[Poisson sigma-model]] in the context of [[formal deformation quantization]].

As for item 1, the line bundle is the canonical bundle and the path integral 
$$\Omega([x],[y])=\int_{\gamma(0)=[x]}^{\gamma(1)=[y]}\mathcal{D}\gamma\,P(\gamma)\in\text{Hom}(\mathcal{L}_{x},\mathcal{L}_{y})$$
is the map $\langle x|\mapsto \langle x|y\rangle\langle y|\,.$

There are now two ways of describing item 2. The traditional way is by taking the Hilbert space to be that of holomorphic sections. The second way of describing it is by taking the Hilbert space to be the image of the orthogonal projection defined by the path integal, ie.
$$\Psi\mapsto\Big([y]\mapsto\int_{P(\mathcal{H})}\Psi([x])|y\rangle\langle y|\omega^n\Big)\,.$$
These two Hilbert spaces are the same as this is the orthogonal projection onto holomorphic sections. 


This tells most of the story for $P(\mathcal{H}).$ 

### Projective Submanifolds

There is another class of examples that is just as natural and almost just as simple as $P(\mathcal{H}).$ These are symplectic submanifolds $q:M^{2n}\xhookrightarrow{} P(\mathcal{H})\subset B(\mathcal{H}) $ which satisfy the overcompleteness condition, ie. up to a constant
$$1_{\mathcal{H}}=\int_M q\omega^n\,.$$


These are more interesting because the quantum mechanics and classical mechanics are different, ie.
$i\langle \rangle$ is not a morphism of Lie algebras. However, there is a Lie subalgebra on which it is an injective morphism, and otherwise all other formulas discussed in the previous section remain valid. This Lie subalgebra can be identified with the set of operators which, under Schrodinger's equation, preserves $M.$

One can think of $P(\mathcal{H})$ as the pure states, and $q(M)$ as the subset of pure states that are classical states.


### The General Case

In general then, to quantize as a symplectic manifold $M$ it is enough to embed it into $P(\mathcal{H})$ in such a way that the embedded submanifold has the overcompleteness property. It's not clear to what extent this can be done exactly, however it can be done for Kahler manifolds which have a nice enough group of symmetries, eg. $T^*\mathbb{R}^n$ and the upper half plane. However, for all prequantizable compact manifolds (and many non–compact ones) this can be done approximately, ie.
\begin{theorem}
Let $(M,\omega)$ be a prequantizable compact symplectic manifold. Then there exists a sequence of embeddings
$$q_k:M\xhookrightarrow{}P(\mathcal{H}_k)$$
such that 
$$\|q_k^*\omega_{FS}/k-\omega\|_{C^m}=\mathcal{O}(1/k)$$
for all $m\in\mathbb{N},$ and such that $q_k(M)$ is overcomplete with respect to a measure $d\mu_k$ for which $d\mu_{k}/k^n \to \omega^n\,.$
\end{theorem}
Here, $\omega_{FS}$ is the Fubini–Study form. This theorem identifies the structure used to quantize and get star products on general compact symplectic manifolds, [Borthwicke–Uribe] (#Borthwicke–Uribe), [Schlichenmaier](#Schlichenmaier). This theorem follows from theorem 1.1 of [Dai–Liu–Ma](#Dai–Liu–Ma), theorem 3.6 of [Ma–Marinescu] (#Ma–Marinescu), and the observation that the symplectic Kodaira embedding is overcomplete.

Note that, there don't seem to be any (convincing?) examples of quantizations of symplectic manifolds which can't be strenghtened to a quantization of this form, so this perspective seems universal. Eg. Consider the quantization of $T^*\mathbb{R}$ using the polarization with $x=const.$ One can define coherent states using the lowering operator $\hat{x}+i\hat{p}$ and then one immediately gets all of this additional structure.

###Relationship to Kostant-Souriau Operators

Under the equivalence of categories from item 3 to item 2,
$$\langle x|\to \big([y]\mapsto \langle x|y\rangle\langle y|\big)$$

gives a map $I:\mathcal{H}\to \Gamma(M,\mathcal{L}).$ If $H\in B(\mathcal{H})$ is such that the Hamiltonian vector field $X_{\langle H\rangle}$ is tangent to $q:M\xhookrightarrow{} P(\mathcal{H}),$ then
$$H=I^{-1}\circ (\nabla_{X_{\langle H\rangle}}+i\langle H\rangle)\circ I\,.$$
Therefore, $i\langle\rangle$ extends the Kostant-Souriau prequantization map. Note that, generically the Kostant-Souriau prequantization map doesn't work at all, ie. it doesn't quantize any non–constant functions! Eg. a generic genus $g\ge 3$ Riemann surface has no nontrivial automorphisms, and therefore on a generic genus $g\ge 3$ surface the Kostant-Souriau prequantization map only quantizes constants. As a result, it only gives operators which are constant multiples of the identity.

## References
The observation is due to:

* {#Kibble79} [[Tom W. B. Kibble]], *Geometrization of quantum mechanics*, Communications in Mathematical Physics **65** (1979) 189–201 &lbrack;[doi:10.1007/BF01225149](https://doi.org/10.1007/BF01225149)&rbrack;

    
The idea was picked up in:

* {#Odzijewicz92} Anatol Odzijewicz, _Coherent state method in geometric quantization_, in Twenty Years of Bialowiez: a mathematical anthology, Aspects of Differential Geometric Methods in Physics_ (pp 47-78) , World Sci. Monogr. Ser. Math. 8 (2005); _Coherent states and geometric quantization_,  Comm. Math. Phys.  __150__  (1992),  no. 2, 385&#8211;413 [doi](http://ams.mpim-bonn.mpg.de/leavingmsn?url=http://projecteuclid.org/getRecord?id=euclid.cmp/1104251870) [94c:58077](http://www.ams.org/mathscinet-getitem?mr=1194023)

* {#Hughston96} [[Lane P. Hughston]], *Geometry of stochastic state vector reduction*, Proceedings of the Royal Society A **452** 1947 (1996) &lbrack;[doi:10.1098/rspa.1996.0048](https://doi.org/10.1098/rspa.1996.0048), [jstor:52944](https://www.jstor.org/stable/52944)&rbrack;

  > (with speculations on the implication for [[quantum state collapse]])

* {#AshtekarSchilling99} Abhay Ashtekar, Troy A. Schilling, *Geometrical Formulation of Quantum Mechanics*, in: *On Einstein’s Path* Springer (1999) &lbrack;[arXiv:gr-qc/9706069](https://arxiv.org/abs/gr-qc/9706069), [doi:10.1007/978-1-4612-1422-9_3](https://doi.org/10.1007/978-1-4612-1422-9_3)&rbrack;


Further discussion:

* {#BrodyHughston01} [[Dorje C. Brody]], [[Lane P. Hughston]], *Geometric Quantum Mechanics*, J. Geom. Phys. **38** (2001) 19-53 &lbrack;[arXiv:quant-ph/9906086](https://arxiv.org/abs/quant-ph/9906086), <a href="https://doi.org/10.1016/S0393-0440(00)00052-8">doi:10.1016/S0393-0440(00)00052-8</a>&rbrack;

* A Benvegnù, N Sansonetto, M Spera, *Remarks on geometric quantum mechanics*, Journal of Geometry and Physics **51** 2 (2004) 229-243 &lbrack;[doi:10.1016/j.geomphys.2003.10.008](https://doi.org/10.1016/j.geomphys.2003.10.008)&rbrack;

* J. F. Cariñena, J. Clemente-Gallardo & G. Marmo, *Geometrization of quantum mechanics*, Theoretical and Mathematical Physics **152** (2007) 894–903 &lbrack;[doi:10.1007/s11232-007-0075-3](https://doi.org/10.1007/s11232-007-0075-3)&rbrack;

* Secret Blogging Seminar, *[Quantum mechanics and geometry](https://sbseminar.wordpress.com/2009/11/16/quantum-mechanics-and-geometry/)* (2009)

* Hoshang Heydari, *Geometric formulation of quantum mechanics* &lbrack;[arXiv:1503.00238](https://arxiv.org/abs/1503.00238)&rbrack;

* {#klauder} J.R. Klauder. 
Quantization is Geometry, After All. Annals Phys. 188 (1988) 120-141. DOI: 10.1016/0003-4916(88)90092-9


Discussion of dynamics of [[mixed states]] ([[density matrices]]), now via [[Poisson geometry]]:

* Pritish Sinha, Ankit Yadav, *Poisson Geometric Formulation of Quantum Mechanics* &lbrack;[arXiv:2312.05615](https://arxiv.org/abs/2312.05615)&rbrack;


On theorems related to quantizations which induce [[star products]] on general symplectic manifolds:

* {#Borthwicke–Uribe} David Borthwick, Alejandro Uribe. Almost complex structures and geometric quantization (arXiv:dg-ga/9608006)

* {#Dai–Liu–Ma} Xianzhe Dai, Kefeng Liu, Xiaonan Ma. On the asymptotic expansion of Bergman kernel. (arXiv:math/0404494v2)

* {#Ma–Marinescu} Xiaonan Ma, George Marinescu. Generalized Bergman kernels on symplectic manifolds. (arXiv:math/0411559v3)

* {#Schlichenmaier} Martin Schlichenmaier. Berezin-Toeplitz quantization for compact Kaehler manifolds. A Review of Results. (arXiv:1003.2523v1)

[[!redirects symplectic formulation of quantum mechanics]]




