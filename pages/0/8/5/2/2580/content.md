
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents
* automatic table of contents goes here
{:toc}

## Idea

In [[functional analysis]], a _distribution_ (or generalized function) is a [[functional]] on a [[topological space|space]] of functions which typically is not representable by a function itself. They are often used to give a notion of derivative of a function which has no derivative in the classical sense of Lebesgue integration theory, and to give an abstract framework in which one can describe fundamental solutions to partial differential equations. 

Generalized functions were introduced by Sobolev in 1935, and independently (under the name _distributions_) by Laurent Schwartz in the 1940's, who unaware of Sobolev's work developed an extensive theory for them. 

## Definitions 

Distributions come in various flavors, depending on what spaces of functions they act on. The functions they act on are called **test functions**; typically they are smooth functions on domains in Euclidean space satisfying some boundedness property. 

The widest (and generally the default) notion is as follows. Let $U \subseteq \mathbb{R}^n$ be open. Let $C_{c}^{\infty}(U)$ denote the vector space of smooth functions with compact support on $U$ (also called **bump functions**; these are the test functions in this case). Endow this space with the topology induced from the family of seminorms 

$$\rho_{K, \alpha}(f) = \sup_{x \in K} |\partial^{\alpha} f|$$ 

where $K \subseteq U$ is compact and $\alpha = (\alpha_1, \ldots, \alpha_n)$ is a multi-index and 

$$\partial^{\alpha} = \frac{\partial^{\alpha_1}}{\partial x^{\alpha_1}} \ldots \frac{\partial^{\alpha_n}}{\partial x^{\alpha_n}}$$ 

is the corresponding differential operator. The resulting [[topological vector space|TVS]] is locally convex and complete with respect to its uniformity; it is in fact an LF-space: an inductive limit of Fr&#233;chet spaces $C_c^{\infty}(K)$ (each of which has empty interior as a subspace of $C_c^{\infty}(U)$, so by the Baire category theorem, $C_c^{\infty}(U)$ is not itself Fr&#233;chet). 

A **distribution on** $U$ is a continuous linear functional 

$$C_c^{\infty}(U) \to \mathbb{R}$$ 

The space of distributions on $U$ is denoted $\mathcal{D}(U)$. There is an obvious bilinear pairing 

$$\mathcal{D}(U) \times C_c^{\infty}(U) \to \mathbb{R}: (S, \phi) \mapsto S(\phi)$$ 

given by evaluation; often one writes $\langle S, \phi\rangle$ instead of $S(\phi)$. The space of distributions can be given the weak $*$-topology, meaning the smallest topology rendering the maps 

$$\langle -, \phi\rangle: \mathcal{D}(U) \to \mathbb{R}$$ 

continuous for all test functions $\phi$.  As $C_c^\infty(U)$ is reflexive, this agrees with the weak topology.  Other natural topologies exist, such as uniform convergence on compact subsets of $C_c^\infty(U)$ (in this case, this agrees with uniform convergence on bounded subsets which usually goes by the name of the *strong* topology).

If $f: U \to \mathbb{R}$ is locally integrable, then for all test functions $\phi$ the Lebesgue integral 

$$\langle f, \phi\rangle = \int_U f(x)\phi(x) d x $$ 

is defined; in this way a function $f$ locally integrable over $U$ may be regarded as a distribution on $U$ (explaining both the sense in which distributions are "generalized functions" and a reason for the angle-bracket notation for the evaluation pairing). In particular, there is an obvious inclusion 

$$C_c^{\infty}(U) \hookrightarrow \mathcal{D}(U)$$ 

and this inclusion turns out to be dense. 

Other notions of spaces of distributions, each endowed with the weak $*$-topology, include 

* Compactly supported distributions on $U$. These are functionals on $C^{\infty}(U)$ (test functions without compact support). 

* Rapidly decaying distributions (usually on $U = \mathbb{R}^n$). These are functionals on the space of smooth functions each of whose partial derivatives (of any order) has "tempered" or moderate growth (i.e., bounded by polynomial growth). 

* Tempered distributions (usually on $U = \mathbb{R}^n$). These are functionals on so-called **Schwartz space**: the space of smooth functions each of whose derivatives (of any order) decays rapidly (goes to zero more quickly than any negative power of $|x|$ as $|x| \to \infty$). The topology on Schwartz space is induced by the family of seminorms 
$$\rho_{K, \alpha, \beta}(\phi) = \sup_{x \in K} |x^\alpha \partial^\beta \phi|$$ 
where $\alpha$, $\beta$ are multi-indices. 

## Operations on distributions 

As $\mathcal{D}(U)$ is dual to $C_c^\infty(U)$, each continuous linear operator on $C_c^\infty(U)$ induces a corresponding linear operator on $\mathcal{D}(U)$ in the obvious way.  Given

$$
F\colon C_c^\infty(U) \to C_c^\infty(U)
$$

we define

$$
F^*\colon \mathcal{D}(U) \to \mathcal{D}(U)
$$

according to the usual formula for dualities

$$
F^* S(\phi) = S(F \phi).
$$

However, since there is an obvious inclusion $C_c^\infty(U) \to \mathcal{D}(U)$ induced by the standard inner product on $C_c^\infty(U)$, what is more usually desired is not this dual operator but an **extension** operator.  That is, instead of $F^*$ we want an operator $F^\dagger \colon \mathcal{D}(U) \to \mathcal{D}(U)$ with the property that for $\phi \in C_c^\infty(U)$ then $F^\dagger(\phi) = F(\phi)$ (identifying $C_c^\infty(U)$ with its image in $\mathcal{D}(U)$).  Being slightly more careful, let us write $\iota \colon C_c^\infty(U) \to \mathcal{D}(U)$ for the inclusion induced by the inner product.  Then we want $F^\dagger(\iota \phi) = \iota (F(\phi))$.

If the extension exists, we have

$$
F^\dagger(\iota \phi)(\psi) = \iota(F(\phi))(\psi) = \langle F(\phi), \psi \rangle
$$

Now suppose that $F$ has an adjoint, say $F^+$, with respect to the inner product.  Note that this is not automatic since $C_c^\infty(U)$ is not a Hilbert space.  Moreover, even if $F$ extends to the Hilbert completion the Hilbertian adjoint may not work since it may not define a continuous linear map on the subspace $C_c^\infty(U)$.  But if $F^+$ does exist then we have

$$
F^\dagger(\iota \phi)(\psi) = \langle F(\phi), \psi \rangle = \langle \phi, F^+(\psi) \rangle
$$

In this case, the definition of $F^\dagger$ on the whole of $\mathcal{D}(U)$ is obvious: simply take ${F^+}^*$.  That is, the dual operator to the adjoint to $F$.  In full, $F^\dagger \colon \mathcal{D}(U) \to \mathcal{D}(U)$ is defined via the formula

$$
\langle F^\dagger(S),\phi\rangle = \langle S, F^+(\phi) \rangle
$$

If the ground field is $\mathbb{C}$ then this carries through essentially unchanged except for the fact that one does **not** use the inner product on $C_c^\infty(U)$ but rather the associated bilinear pairing

$$
(\phi,\psi) = \int_U \phi \psi
$$

This is to ensure that the inclusion $C_c^\infty(U) \to \mathcal{D}(U)$ is complex linear and not conjugate linear.  Otherwise extending operators becomes complex.

Two instances are of particular importance: 

* Multiplication by a smooth function $\theta$. If $\theta$ is any smooth function on $U$ (not necessarily compactly supported), then we can define $\theta \cdot S$ by observing that this multiplication is self-adjoint: 
$$\langle \theta \cdot \phi, \psi \rangle = \langle \phi, \psi \cdot \theta\rangle$$
where $\phi, \psi$ are arbitrary test functions.  Thus we define $\theta \cdot S$ by
$$\langle \theta \cdot S, \psi \rangle = \langle S, \theta \cdot \psi$$

* Differentiation. If $\partial^i$ is partial differentiation with respect to the $i^{th}$ coordinate, then for test functions $\psi$, $\phi$ we have 
$$\int_U \partial^i(\psi)(x) \phi(x)\; d x = -\int_U \psi(x) \partial^i(\phi)(x)\; d x$$ 
by simple integration by parts and the fact that $\phi$, $\psi$ are compactly supported.  Thus differentiation is _skew_-adjoint and so we define the extension to distributions by 
$$\langle \partial^i(S), \phi\rangle = -\langle S, \partial^i(\phi) \rangle$$ 
for all test functions $\phi$. In general, 
$$\langle \partial^\alpha S, \phi\rangle = (-1)^{|\alpha|}\langle S, \partial^\alpha \phi \rangle$$
where $|\alpha| = \alpha_1 + \ldots + \alpha_n$ is the total degree of the multi-index. 

Thus derivatives of distributions are defined to all orders. Some examples are given in the section "examples".

### Multiplication of Distributions
Distributions fail to address some uses to which physicists would like to put them (as in [[path integral]]s), since there is no good way to multiply distributions in a way that extends multiplication of functions. 
In certain mathematical interpretations of [[quantum field theory]], a quantum field is a (operator valued) distribution and the [[Lagrangian]] of the [[standard model of particle physics]] contains products of those.

The fact that there is no extension of multiplication to distributions is a famous no-go theorem of Laurent Schwartz.

#### Heuristics of Why Multiplication is Impossible
Two heuristic explanations why multiplication is not possible:

In the construction of distributions we consider the _algebra_ of compactly supported smooth functions, forget about the multiplication and see it as a [[TVS]] only, and then take the dual. The _algebra_ structure therefore does not enter the construction in any way.

Let $H(x)$ be the Heaviside function, we clearly have
$$
      H(x) = H^{n} (x)
$$
where the product on the right side is the product of classical functions. Applying differentiation and the product rule naivly results in a contradiction immediatly:
$$
      \delta(x) = n H^{n-1} (x) \delta(x)
$$

####When Multiplication is Possible
There is no product defined on the whole [[TVS]] of distributions, but some distributions may nevertheless be multiplied. A deeper explanation of this phenomenon needs the concept of [[wavefront sets]]. An exposition of [[QED]] that avoids divergences by carefully using only rigorously defined products of distributions is this:

* G. Scharf: _Finite quantum electrodynamics. The causal approach._ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0844.53052&format=complete))

####Colombeau 
J.F. Colombeau has developed a theory where multiplication is possible; see this brief Wikipedia [article](http://en.wikipedia.org/wiki/Colombeau_algebra) and for example these [slides](http://fibonacci.dm.unipi.it/cluster-pages/ultramath/slides/vernaeve-slides.pdf).

Briefly: Colombeau considers sequences of functions that converge to distributions (weakly) and defines the product of two distributions as the product of the sequences. This product is not independent of the chosen sequences, which means that the level of abstraction achieved by distribution theory is abandoned.

For further details see:

* Jean Fran&#231;ois Colombeau: _Multiplication of distributions. A tool in mathematics, numerical engineering and theoretical physics._ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0815.35002&format=complete)) 

## Examples 

As explained above, any locally integrable function on $U$ defines a distribution on $U$. Other examples may be produced fairly cheaply by restriction of functionals on various TVS which contain the test functions. 

For instance: if $C_c(U)$ denotes the space of real-valued continuous functions with compact support in $U$ (topologized by uniform convergence on compacta), then a functional $\mu: C_c(U) \to \mathbb{R}$ is essentially the same as a signed measure on $U$ (Riesz-Markov theorem), i.e., there is a unique signed measure $d m$ for which 

$$\mu(\phi) = \int_U \phi d m.$$ 

Since the inclusion $i: C_c^\infty(U) \hookrightarrow C_c(U)$ is continuous, it follows that a measure $\mu$ defines a distribution by simple restriction along $i$: 

$$C_c^\infty(U) \overset{i}{\to} C_c(U) \overset{\mu}{\to} \mathbb{R}$$ 

Specializing further, consider any function of bounded variation on $U = \mathbb{R}$, say a bounded monotone increasing function $\alpha$. Then the Riemann-Stieltjes integral 

$$\int_{\mathbb{R}} f(x) d\alpha(x)$$ 

is defined for all functions $f$ with compact support; this provides a measure $d\alpha$ and hence a distribution. 

A prototypical example of this is provided by the Heaviside function: $H(x) = 1$ if $x \gt 0$, else 0. ("Heaviside": what a great pun!) Here we have, for all $f \in C_c(\mathbb{R})$, 

$$\langle f, d H \rangle = \int_{\mathbb{R}} f(x) d H(x) = f(0)$$ 

As a distribution, the Heaviside measure is the famous **[[Dirac distribution]]**. The long-standing intuitive practice among physicists and engineers is to write 

$$d H(x) = \delta_0(x) d x$$ 

where of course the function $H(x)$ doesn't have a derivative in the classical sense (i.e., as a function), but as a distribution, it does. Meanwhile, $H(x)$ is itself the derivative of a continuous function: $G(x) = \max\{x, 0\}$. 

For an example of a distribution on $\mathbb{R}$ which does not arise from a measure, consider the derivative of the Dirac distribution. (As a functional, it maps a test function $\phi$ to $-\phi'(0)$.) 

These examples are by no means curiosities. A fairly deep theorem is that _every_ distribution arises as a linear combination of derivatives of continuous functions:  

**Theorem:** Let $S$ be a distribution on an open domain $U \subseteq \mathbb{R}^n$. Then, there exist a finite collection $A$ of multi-indices $\alpha$ and continuous functions $g_\alpha$ defined on $U$ for which 

$$S = \sum_{\alpha \in A} \partial^\alpha g_\alpha$$ 

## Applications 

Distributions rigorously address a need long-felt by physicists to mathematically represent objects such as point particles of mass $m$ at position $a$ (where one would use the distribution $m\delta(x-a)$). They thus appear in accounts of quantum theory which attempt to achieve mathematical rigor. An example of this tendency can be seen in axiomatic formulations of quantum field theory such as the [[Wightman axioms]]. 

A brief survey of applications of distribution theory to perturbative quantum field theory may be found [here](http://www1.jinr.ru/Archive/Pepan/v-31-7a/I_ktp_04_t.pdf). 
  

Within mathematics, distributions are quite commonplace; for example, de Rham appropriated them for his theory of [[current]]s. Distribution theory has also long been used in the theory of partial differential equations. Here is a sample theorem: 

* **Theorem (Ehrenpreis, Malgrange):** Let $D$ be a linear differential operator on $\mathbb{R}^n$ with constant coefficients. Given a compactly supported smooth function $f$ on $\mathbb{R}^n$, there exists a smooth solution $u$ to the equation $D u = f$. 

A proof is given in these [notes](http://www-math.mit.edu/~helgason/hormander.pdf) by Helgason. The basic idea is to prove there exists a **fundamental solution** of $D$, i.e., a distribution $T$ such that $D T = \delta_0$. Then $u = f * T$ is smooth. The existence of a fundamental solution involves a theorem of Paley-Wiener type. 

## Related concepts

### In synthetic differential geometry 

There is another point of view on distributions: that they _can_ be modeled by actual functions provided that one admits infinite and infinitesimal quantities of the type used in Robinson nonstandard analysis. One particular approach is to formulate axiomatically the theory of distributions so that it can be interpreted in [[smooth topos]]es that model the axioms of [[synthetic differential geometry]] and support a suitable notion of invertible [[infinitesimal object]]s and infinitely large integers.

This is discussed in chapter VII, section 3 of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]]

which closely mirrors the original treatment in Robinson's book Non-standard Analysis. Examples of models that support these axioms are the toposes $\mathcal{Z}$ and $\mathcal{B}$ described there. 

### Lawvere distributions

See [[Lawvere distribution]].

### Generalizations and variants

In $\mathbb{R}^n$ the distributions and generalized functions boil down to the same thing, so the terminology identifies them. But on a manifold, the distributions/generalized densities (functionals on test functions) and generalized functions (functionals on test *densities*) do not agree. See V. Guillemin, S. Sternberg: _Geometric asymptotics_ ([free online](http://www.ams.org/online_bks/surv14)). While generalized functions pull back, distributions/generalized densities push forward (under some conditions, though). 

More generally one can study generalized differential $k$-forms in local coordinates they look like $\sum f_\alpha dx^{\alpha_1}\wedge \cdot \wedge dx^{\alpha_k}$. Usually they are called **currents**. They are useful e.g. in the study of higher dimensional residua in higher dimensional complex geometry (cf. *Principles of algebraic geometry* by Griffiths and Harris) and in geometric measure theory (cf. the monograph by Federer).  

Sometimes one considers larger spaces of distributions, where worse singularities than in Schwarz theory are allowed. Most well known are the theory of [[hyperfunction]]s and the theory of **Coulombeau distributions**. 

[[!redirects distributions]]
[[!redirects generalized function]]
[[!redirects generalized functions]]