#Contents
* automatic table of contents goes here
{:toc}

## Idea

In functional analysis, a distribution (or generalized function) is a functional on a space of functions which typically is not representable by a function itself. They are often used to give a notion of derivative of a function which has no derivative in the classical sense, and to give an abstract framework in which one can describe fundamental solutions to partial differential equations. 

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
F^\dagger(\iota phi)(\psi) = \iota(F(\phi))(\psi) = \langle F(\phi), \psi \rangle
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

Thus derivatives of distributions are defined to all orders. Some examples are given in the following section. 

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

As a distribution, the Heaviside measure is the famous **Dirac distribution**. The long-standing intuitive practice among physicists and engineers is to write 

$$d H(x) = \delta_0(x) d x$$ 

where of course the function $H(x)$ doesn't have a derivative in the classical sense (i.e., as a function), but as a distribution, it does. Meanwhile, $H(x)$ is itself the derivative of a continuous function: $G(x) = \max\{x, 0\}$. 

For an example of a distribution on $\mathbb{R}$ which does not arise from a measure, consider the derivative of the Dirac distribution. (As a functional, it maps a test function $\phi$ to $-\phi'(0)$.) 

These examples are by no means curiosities. A fairly deep theorem is that _every_ distribution arises as a linear combination of derivatives of continuous functions:  

**Theorem:** Let $S$ be a distribution on an open domain $U \subseteq \mathbb{R}^n$. Then, there exist a finite collection $A$ of multi-indices $\alpha$ and continuous functions $g_\alpha$ defined on $U$ for which 

$$S = \sum_{\alpha \in A} \partial^\alpha g_\alpha$$ 

## Applications 

(Anyone want to give some?) 


## in synthetic differential geometry 

The theory of distributions may be formulated axiomatically in [[smooth topos]]es that model the axioms of [[synthetic differential geometry]] and support a suitable notion of invertible [[infinitesimal object]]s and infinitely large integers.

This is discussed in chapter VII, section 3 of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]]

Models supporting these axioms are the toposes $\mathcal{Z}$ and $\mathcal{B}$ described there.