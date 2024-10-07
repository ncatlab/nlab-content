s
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

Now, the standard perspective is certainly not wrong, but various authors have inevitably suggested that the "geometrical formulation"  (more descriptive would be: "symplectic formulation") of quantum mechanics may point to some deeper truth, and if only to show some kind of conceptual unity where one is used to amplifying the dichotomy.

## Explanation

Let $(M^{2n},\omega)$ be a [[symplectic manifold]] and let $d\mu$ be a [[measure]] on $M$ (which is always of the form $h\omega^n$ for some function $h$). Let $\mathcal{L}\to M$ be a [[prequantum line bundle]] and let $\Delta:M^3\to\mathbb{C}$ be a [[smooth function]]. There is an [[equivalence of categories]] between:

1. Quantizations obtained via a [[path integral]] over [[curves]] in $M,$ whose amplitude is given by [[parallel transport]] and whose [[3-point function]] is $\Delta.$

2. A [[subcategory]] of [[Hilbert spaces]] given by a [[subspace]] of [[sections]] of the [[prequantum line bundle]], such that pointwise [[evaluation]] is [[continuous function|continuous]].

3. Maps $q \colon M\to P(\mathcal{H})\subset B(\mathcal{H}),$ with the overcompleteness property: $1_{\mathcal{H}} = \int_M q\,d\mu$ and whose [[3-point function]] is $\Delta.$

Item 2 presents by far the most common way of thinking about [[geometric quantization]], with the other two (especially 1) being nearly completely overlooked. However, it can be argued that 2 is really just a way of computing 3 or 1, where the latter is the only one which really generalizes to Poisson manifolds. This is because the path integral is a section of 

$$\pi_0^*\mathcal{L}^*\otimes \pi_1^*\mathcal{L}\to M\times M\,,$$

and for [[Poisson manifolds]] we can replace $M\times M$ by the [[symplectic groupoid]]. More specifically, the path integral is a Hermitian, idempotent section of the twisted convolution algebra. For symplectic manifolds, it is formally given by 
$$\Omega(a,b)=\int_{\gamma(0)=a}^{\gamma(1)=b}\mathcal{D}\gamma\,P(\gamma)\in\text{Hom}(\mathcal{L}_{a},\mathcal{L}_{b})\,,
$$
where $P(\gamma)$ is parallel transport over $\gamma.$

In the most common examples, 2 is given by holomorphic sections of a [[Kähler manifold]]. In 3, $q$ is a [[classifying map]] for $\mathcal{L}$ and points in its image are called *[[coherent states]]* -- it is not just any classifying map though, it has an overcompleteness property. This is [[Felix Berezin|Berezin]]'s formulation of [[quantization]], whereas 1 is how Klauder conceived of quantization. For a quote: by 

> "all these different procedures to quantize phase space \[can physically\] be thought of as just different ways of regularizing and defining properly the path integral" &lbrack;[[Davide Gaiotto]], [yt](https://youtu.be/EwwGAf2K1uQ?si=eG8E6ILPOtN10obr&t=220)&rbrack;

That something like this was true seems to have been first made explicit in [Odzijewicz 1992] (#Odzijewicz92), who stated a related equivalence of categories and understood the relationship to path integrals.

The simplest and most natural example of this is when $\mathcal{H}$ is finite dimensional and $M=P(\mathcal{H})$ with $\omega$ being the Fubini–Study form. Items 1 and 3 are very natural to describe here, while item 2 is a bit more complicated but quickly follows from the description of 1. We'll first describe item 3. 

In this example, $q$ is the identity.
It's not immediately obvious that this example satisfies the overcompleteness property, but it does with respect to the Fubini–Study measure (up to a constant). There is a natural map
$$\langle\rangle: B(\mathcal{H})\to C^{\infty}(P(\mathcal{H}))\,,\quad \langle H\rangle([v])=\langle v|H|v\rangle\,,$$
where $v$ is any normalized representative of $[v].$ This is just the expectation value of $H$ in the state $[v].$ This map is a morphism of Lie algebras, with respect to the commutator on $B(\mathcal{H})$ and the Poisson bracket on $P(\mathcal{H}).$ This is a bit surprising, because it is so commonly stated that there is no physically reasonable morphism of Lie algebras in the other direction, while this direction receives relatively little attention. The significance of $\langle \rangle$ being a Lie algebra morphism is that, with respect to classical observables of the form $\langle H\rangle\,,$ the classical and quantum mechanics are the same. That is,  
$$i\frac{\partial}{\partial t}\Psi=H\Psi$$
if and only if $t\mapsto [\Psi](t)$ is the Hamiltonian flow of the Hamiltonian vector field of $\langle H\rangle.$ Equivalently, $A\in B(\mathcal{H})$ satisfies Heisenberg's equation of motion with respect to $H$ if and only if $\langle A\rangle$ satisfies Hamilton's equations of motion with respect to $\langle H\rangle.$
 
In fact, the expectation value map is just the adjoint of [[Felix Berezin|Berezin]]'s quantization map, which is given by (up to a constant)
$$Q_f=\int_M fq\,\, \omega^n\,.$$
More precisely, $\langle \rangle=Q^{\dagger},$
where $B(\mathcal{H})$ is equipped with the Hilbert–Schmidt inner product, ie.
$$Tr(Q_f^*A)=\int_{P(\mathcal{H})} f^*\langle A\rangle \omega^n\,.$$
The overcompleteness property says that $Q_1=1_{\mathcal{H}},$ which means that $\langle \rangle$ intertwines the trace map with integration.

As for item 1, the line bundle is the canonical bundle and the path integral 
$$\Omega([x],[y])=\int_{\gamma(0)=[x]}^{\gamma(1)=[y]}\mathcal{D}\gamma\,P(\gamma)\in\text{Hom}(\mathcal{L}_{x},\mathcal{L}_{y})$$
is the map $\langle x|\mapsto \langle x|y\rangle\langle y|\,.$

There are now two ways of describing item 2. The traditional way is by taking the Hilbert space to be that of holomorphic sections. The second way of describing it is by taking the Hilbert space to be the image of the orthogonal projection defined by the path integal, ie.
$$\Psi\mapsto\Big([y]\mapsto\int_{P(\mathcal{H})}\Psi([x])|y\rangle\langle y|\omega^n\Big)\,.$$
These two Hilbert spaces are the same as this is the orthogonal projection onto holomorphic sections. 

Mark $S^1$ with the cyclically ordered points. The 3-point function is given by 
$$\Delta([x],[y],[z])=\int_{\gamma_{[x],[y],[z]}}\mathcal{D}\gamma\,P(\gamma)\, ,$$
where the path integral is over all maps $S^1\to P(\mathcal{H})$ such that the marked points map to $[x],[y],[z].$ Explicitly, $\Delta$ is defined by the equation
$$|x\rangle\langle x|y\rangle\langle y|z\rangle\langle z|x\rangle\langle x|=\Delta([x],[y],[z])|x\rangle\langle x|\,.$$

This tells most of the story for $P(\mathcal{H}).$ There is another class of examples that is just as natural and almost just as simple. These are symplectic submanifolds of $P(\mathcal{H})$ which satisfy the overcompleteness condition. These are more interesting because the quantum mechanics and classical mechanics are different, however there are still Hamiltonians for which they agree.

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

Discussion of dynamics of [[mixed states]] ([[density matrices]]), now via [[Poisson geometry]]:

* Pritish Sinha, Ankit Yadav, *Poisson Geometric Formulation of Quantum Mechanics* &lbrack;[arXiv:2312.05615](https://arxiv.org/abs/2312.05615)&rbrack;



[[!redirects symplectic formulation of quantum mechanics]]




