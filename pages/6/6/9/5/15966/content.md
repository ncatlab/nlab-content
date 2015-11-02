[[!redirects Global analytic index theory]]
[[!redirects global analytic index theory]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## A new formulation for classical index theory

Classical real or [[complex analytic geometry|complex analytic]] [[index theory]] may be described as a setting that contains:

* [[Riemann-Roch theorem|Riemann-Roch]] type theorems, such as Bismut's Riemann-Roch theorem for a general smooth proper morphism of complex analytic spaces, Grothendieck's Riemann-Roch theorem for a morphism of schemes, or Riou's motivic Riemann-Roch theorem for a projective morphism of schemes, and

* Index theorems for elliptic operators or elliptic complexes on real analytic manifolds (that actually also give Riemann-Roch results, when the elliptic complex is induced by the $\bar{\partial}$-operator on differential forms).

* Equivariant [[Atiyah-Singer index theorems]] and noncommutative Connes-Moscovisci local index theorems.

One may formulate many of these results in an essentially unified setting by using index theory on derived analytic stacks over $\mathbb{R}$ or $\mathbb{C}$.

Recall also that one may solve a linear partial differential equation
$$P(\partial)=0$$
when $P$ has constant coefficients by using the analytic continuation of the complex-valued function $(x,s)\mapsto P(x)^s$. This method is called the Bernstein-Sato method for finding the fundamental solution. There are also other methods, but a natural constraint on the given system is to try to do everything in the analytic setting, and it is thus natural to use complex powers to try to solve it. This will be discussed in more details later. 

## The challenge of global analytic index theory

Global analytic index theory should give a setting for index theory on [[global analytic spaces]] that gives back usual index theorems when one works over $\mathbb{C}$ or $\mathbb{R}$, but that gives new interesting theorems when one works with analytic spaces or even analytic stacks over $\mathbb{Z}$ equipped with its archimedean norm. It should also give back the p-adic index theorems of Christol-Mebkhout when one works in a Frobenius-equivariant setting over $\mathbb{Z}_p$ or $\mathbb{Q}_p$.

The starting point of this approach should be given by the settlement of a global analytic derived version of Kashiwara and Schapira's microlocal formulation of various index theorems. It is essential, for this approach to work, to have a viewpoint on the microlocalization techniques that is very close to Toen and Vezzosi's loop space approach to the Chern character, through Hochschild and negative cyclic homology of rigid symmetric monoidal stacks of $\infty$-categories over $\infty$-stacks, with an additional microlocal fashion. One also needs a version of [[Grothendieck duality]] adapted to global analytic derived geometry, because it is necessary to define microlocal Hochschild homology in Kashiwara and Schapira's approach to index theory.

## An important difficulty

A difficulty to be overcome in the seek for a global analytic index theory is
that the theory of $D$-modules without denominators, or in characteristic $p$,
lacks of a good notion of de Rham cohomology: the usual definition of it gives
etale cohomology with $k$-coefficients on an algebraically closed field $k$ of characteristic $p$ (Ogus' article on the infinitesimal site). There is also not yet a
clear idea of what the analog of $\mathbb{R}$-constructible coefficients could
be on a general global analytic space.

For example, if one mimicks the approach of Kashiwara and Schapira in the characteristic $p$ setting, one has to replace
$\mathbb{C}/\mathbb{R}$ by $\bar{\mathbb{F}}_p/\mathbb{F}_p$, which is an infinite extension. The natural analog in this situation of the elliptic pair
$(\mathcal{O}_X,\mathbb{C}_M)$ associated to $M/\mathbb{R}$, for $M/\mathbb{F}_p$ a projective smooth variety, has de Rham cohomology an $\bar{\mathbb{F}}_p$-module that doesn't seem to be finite dimensional.

Two approaches to $\mathcal{D}$-modules in characteristic $p$ were developed by Berthelot and Mebkhout-Narvaez-Macarro. One may try to extend this last approach (using weak formal schemes over $\mathbb{Z}_p$) to a global base, but one will face the problem of dealing with (naive) $\mathcal{D}$-modules in characteristic $p$, that are not well behaved.

Another (maybe more promising) approach is to get inspiration from Buium's differential calculus over the integers and Madsen/Hesselholt's results on topological cyclic homology: making a topological version of $\mathcal{D}$-modules in the setting of [[spectral global analytic geometry]].

## Pursuing global analytic trace kernels

Recall that a trace kernel in Kashiwara and Schapira's sense
is a $k_{M\times M}$-module $K$ together with a sequence of morphisms
$$k_\Delta\to K\to \omega_\Delta$$
and the corresponding class is a section of $\mu hom(k_\Delta,\omega_\Delta)$.

In the coherent setting, the analog of a trace kernel associated to a coherent $\mathcal{O}$-module $\mathcal{F}$ is given by the sequence
$$
\mathcal{O}_\Delta\to \mathcal{F}\boxtimes D\mathcal{F}\to \omega^{hol}_\Delta.
$$

In the $\mathcal{D}$-module setting, the analog of a trace kernel of a coherent
$\mathcal{D}$-module $\mathcal{M}$ is given by the sequence
$$
\mathcal{B}_\Delta\to \mathcal{M}\boxtimes D_\mathcal{D}\mathcal{M}\to \mathcal{B}^\vee_\Delta
$$
and one sends it to the trace kernel given by taking the de Rham functor (tensor product operation $\omega_{X\times X}\otimes_\mathcal{D}-$. The corresponding microlocal euler class is given by the microlocalization of the above sequence
$$
\mathcal{B}_\Delta^E\to \mathcal{M}^E\boxtimes D_\mathcal{E}\mathcal{M}^E\to \mathcal{B}^{E\vee}_\Delta
$$
because one has a canonical isomorphism
$$
\mathbb{R}Hom_{\mathcal{E}}(\mathcal{B}_\Delta^E,\mathcal{B}_\Delta^{E\vee})
\overset{\sim}{\longrightarrow}
\mu hom(\mathbb{C}_\Delta,\omega_\Delta).
$$

The problem is now the following: given an $R$-constructible sheaf $F$ on $M$,
one may define a trace kernel by using the sequence
$$\mathbb{C}_\Delta\to F\boxtimes DF\to \omega_\Delta.$$
How can one formulate this construction in terms of $\mathcal{E}$-modules (maybe with an additional structure, such as a kind of filtration, if one takes inspiration from $p$-adic Hodge theory, with filtered modules with connections, or $p$-adic Riemann-Hilbert, with $p$-adic differential equations with Frobenius structure)?

The easiest thing to try is to simply use the (awful) sheaf of rings $\mathcal{E}^\infty$ of infinite order microdifferential operators. Indeed, if $F$ is an $R$-constructible sheaf, then $\mu Hom(F,\mathcal{O})$ is naturally an $\mathcal{E}^\infty$-module. Moreover, any coherent $\mathcal{D}$-module gives rise to an $\mathcal{E}$-module, and thus an $\mathcal{E}^\infty$-module. It is thus quite tempting to try to define a global version of $\mathcal{E}^\infty$ and to find a nice class of $\mathcal{E}^\infty$-modules, containing both (non-torsion) constructible sheaves and the images of coherent $\mathcal{D}$-modules.

A first step in this global direction is to develop an index theory that works in a uniform way over $\mathbb{Q}_p$ and $\mathbb{R}$. This seems to be an almost done theory (because there is no lack of denominators): the notion of constructible sheaf is replaced by its de Rham version. More precisely, a constructible sheaf is constructible for the, say, sub-analytic overconvergent etale topology, i.e., sub-analytically etaly isomorphic to $\mathrm{DR}(\mathcal{O})$, in the sense of $\mathcal{D}^\infty$-modules, and not as usual to a locally constant sheaf: this only works in the complex setting because smooth analytic spaces are locally isomorphic for the semi-analytic topology in the complex case/semi-analytic etale topology in the p-adic case to discs only in the complex situation/to rational domains in the $p$-adic situation, and one may not try to solve $p$-adic differential equations on a rational domain too naively because the exponential doesn't converge so nicely as in the complex case.

One should not try to develop a theory of $p$-adic locally constant coefficients
because the $p$-adic etale cohomology of the unit disc is infinite dimensional:
only de Rham $p$-adic coefficients make sense in (overconvergent) $p$-adic analytic geometry. This is also a good reason to try to develop a global version of de Rham coefficients through the use of topological methods (to encode the de Rham Witt vector constructions in a canonical way).

Once the theory of $p$-adic constructible coefficients is developed, it becomes easy to copy Kashiwara and Schapira's index theory.

## A possible set of constraints for a coherent theory

One should be able to define global analytic analogs of:

1. The derived duality functor on coherent $\mathcal{D}$-modules and in particular coherent $\mathcal{O}$-modules (carefully defined as modules on the underlying dagger algebra, locally for the $G$-topology, even in the affinoid case).

1. The Grothendieck six operations on:
* coherent $\mathcal{O}$-modules,
* coherent $\mathcal{O}^t$-modules, where $\mathcal{O}^t$ (definition due to P. Schapira) is the sheaf for the $G$-topology given on a rational domain $R$ with Berkovich interior $\overset{\circ}{R}$ by the subsheaf of $\mathcal{O}_{\overset{\circ}{R}}$ given by functions $f$ with temperate growth, that one may define as the $\mathcal{D}$-module generated by the ---G-topological--- sheaf $\mathcal{O}^b$ of bounded holomorphic functions.
* sub-analytic torsion &#233;tale (i.e., Artin-Verdier) or more generally motivic analytic sheaves (using the sheaf-cosheaf formalism of Lurie's book higher algebra, generalized to the $1$-localic topos of &#233;tale sheaves on global analytic spaces; one must use the associated etale Berkovich topos to define properly the notion of properness, that is needed for the definition of direct images with proper support; in the strict or generalized Arakelov compactified case, one may need to restrict to morphism of proper logarithmic spaces to get the six operations; this is in some sense analogous to the fact that schemes always have a stacky compactification, i.e., a proper smooth hypercovering, following Deligne), and
* global analytic holonomic $\mathcal{D}$-modules and global analytic exponential motivic sheaves; the $\mathcal{D}$-module situation should involve also global microlocalization techniques (to get natural conditions for the definition of inverse images) and maybe also the Ran space approach with the $*$-tensor product $\overset{*}{\otimes}$.
* One may also define the Grothendieck six operations on general $\mathcal{D}^\infty$-modules.

1. The Grothendieck six operations on sub-analytic Hodge structures (given by a loop space construction of the Hodge filtration, without denominators, together with a Betti structure, given by topological $K$-theory with the $\Lambda$-structure on the Chern character; this may involve the use of topological/spectral methods to take care of Witt vector constructions on an integral or characteristic $p$ base).

1. The Chern character in various situations, using either the formalism of Toen-Vezzosi or the formalism of Kashiwara-Schapira, applied to the following stacks of rigid (maybe non) symmetric monoidal $\infty$-categories on the $\infty$-topos of derived dagger analytic stacks with its pro-etale, Nisnevich or usual analytic topology:
* the stack $X\mapsto Perf(X)$ of perfect $\mathcal{O}$-modules (derived analog of coherent modules),
* the stack $X\mapsto Const_{proet}(X,\mathcal{C})$ of constructible pro-etale sub-analytic sheaves with values in a symmetric monoidal stable presentable $\infty$-category, with their natural tensor product and duality; be careful, the pro-etale constructibility is meant in the above de Rham sense: one should not use locally constant coefficients because they don't work well even over $\mathbb{Q}_p$. The problem with this stack is that it doesn't take care of the derived (infinitesimal) information, so its treatment should be given in a Kashiwara-Schapira approach, using loop space microlocalization and some additional structure that will probably be necessary to encode an R-constructible sheaf in a microdifferential structure.
* one would also like to treat the case of (at least holonomic) $\mathcal{D}$-modules, either using the Ran space or another construction. It seems that Toen-Vezzosi's approach has to be modified to treat this case properly because of the compound tensor structure $(\otimes^!,\otimes^*)$ on $\mathcal{D}$-modules on the Ran space.

1. The treatment of $\mathcal{D}$-modules and $\mathcal{D}_q$-modules in a uniform setting may involve the following generalization of the Kashiwara and Schapira approach (in a Toen-Vezzosi type of setting) due to F. Petit: one must work with trace kernels, and compute the trace of their action on the Hochschild or cyclic homology of ---non-symmetric--- monoidal categories of (typically) bimodules on an associative algebra. The proper treatment of this theory will be discussed in the section [[non-commutative global analytic index theory]].

## Derived index theory

Using the methods of [[derived microlocalization]] and Kashiwara and Schapira's [[microlocal formulation of index theory]], one may develop a derived index theory.

## References

[[Masaki Kashiwara]] and [[Pierre Schapira]] _Microlocal Euler classes and Hochschild homology_ [arXiv](http://arxiv.org/abs/1203.4869)

One may be very tempted to use the following reference, to get a better way of looking at Deligne (or global analytic motivic) cohomology, in use for the Grothendieck-Riemann-Roch theorem:

* J. P. Pridham, _A K-theoretic interpretation of real Deligne cohomology_ [arXiv](http://arxiv.org/pdf/1411.5705v1.pdf)