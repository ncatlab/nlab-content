
> This entry is about the concept of distributional densities in functional analysis. For the concept in differential geometry and Lie theory see at _[[distribution of subspaces]]_.

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
* table of contents
{:toc}


## Idea
 {#Idea}

In [[functional analysis]], the concept of _distributional density_, usually just called _distribution_ for short, is a generalization of the concept of [[density]], hence of something that may be [[integration|integrated]] against a [[bump function]] to produce a [[number]]. If a non-degenerate background [[density]]/[[volume form]] $dvol$ is fixed, then each other density is a [[function]] relative to $dvol$, and hence with such an identification understood distributional densities are _[[generalized functions]]_, namely objects that may arise as potentially singular [[limit of a sequence|limits]] of [[sequences]] of [[smooth functions]] (i.e. of [[non-singular distributions]]).  Famous examples of such are the [[delta distributions]] and the [[Heaviside distribution]] which behave like constant functions with an infinitely sharp spike or kink, respectively.

Distributional densities appear notably as [[fundamental solutions]] to linear [[partial differential equations]] (such as for the [[wave equation]]/[[Klein-Gordon equation]], whose fundamental solutions are the [[propagators]] of [[free fields|free quantum fields]]), which is the context in which the concept was originally introduced. The study of their singularity structure (encoded by their [[singular support]] and their [[wave front set]]) is a fundamental tool in [[PDE theory]] (for instance in the [[propagation of singularities theorem]]), known as _[[microlocal analysis]]_. Distributions are also fundamental in the rigorous construction of [[perturbative quantum field theory]], where they appear in the variant as [[operator-valued distributions]].


Often distributions are considered by default just on [[open subsets]] of [[Euclidean space]] with its canonical [[volume form]] tacitly understood. But the concept of distributions makes sense more generally on general [[smooth manifolds]] (at least). If these are equipped with the structure of a ([[pseudo-Riemannian manifold|pseudo-]]) [[Riemannian manifold]] then the induced [[volume form]] again identifies distributions with generalized functions. 

More in detail, given an actual [[density]]/[[volume form]] $dvol$ on some [[smooth manifold]] $X$, then the operation of [[integration]] of [[bump functions]] (elements in the [[topological vector space]] $C^\infty_c(X)$) against $dvol$ yields the [[continuous linear functional]]

$$
  \array{
    C^\infty_c(X)
      &\longrightarrow&
    \mathbb{R}
    \\
    b &\mapsto& \int_{x \in X} b(x) dvol(x)
  }
  \,.
$$

However, not every [[continuous linear functional]] on $C^\infty_c(X)$ arises this way. For example for $x_0 \in X$ any point, the simple [[evaluation]] map

$$
  \delta_{x_0}
  \;\colon\;
  b
  \mapsto
  b(x_0)
$$

is also a continuous linear functional on $C^\infty_c(X)$ (the "[[delta distribution]]"). While this is not the integral against any [[bump function]] times a fixed density, it is the [[limit of a sequence|limit]] of integrations against any [[sequence]] of bump functions (times the fixed density) whose [[support]] narrows in on $x_0$. Therefore one defines a distributional density simply to be _any_ [[continuous linear functional]] on $C^\infty_c(X)$. 

Various immediate variants of this definition may be considered. For instance if the space of "test functions" $C^\infty_c(X)$ is generalized to that of all [[smooth functions]], then one speaks of _[[compactly supported distributions]]_, or if it is enlarged just to the [[Schwartz space]] of functions with all [[derivatives]] rapidly decreasing, then one speaks of [[tempered distributions]]. These are important as on them there is a a good concept of [[Fourier transform of distributions]]. 

Most of the usual constructions of [[differential calculus]] generalize from [[smooth functions]] to distributions, notably there is a concept of [[derivative of distributions]] (defined by generalizing the formula for [[integration by parts]]). A key subtlety is that, however, some standard operations on functions become only [[partial function|partially defined]] on distributions, namely only when their singularity structure is compatible. In particular there is a concept of [[pullback of distributions]] and the [[product of distributions]] compatible with that of smooth functions, but defined only whenever the [[wave front sets]] of the distributions involved satisfy suitable compatibility conditions. Taking this subtlety into account for the [[operator-valued distributions]] appearing in [[perturbative quantum field theory]] is what leads to the concept of [[Wick algebras]] ("normal ordering"), see there for more.

Due to their potentially singular nature, there is more freedom in the [[extension of distributions]] than there is for smooth functions. Notably for extensions from the complement of a single point to that point the freedom is in choosing a [[point-supported distribution]], and these are precisely the [[derivative of a distribution|derivatives]] of [[delta-distributions]]. In the construction of [[time-ordered products]] of [[operator-valued distributions]] it is precisely this freedom in choosing point-[[extensions of distributions]] which in [[perturbative quantum field theory]] is known as "[[renormalization]]".


## Definition
 {#Definitions}

We first recall the 

* [Traditional definition](#TraditionalDefinition).

Then we consider the axiomatic reformulation in terms of [[monads]] following [Kock 11](#Kock11).

* [Characterization by monads](#CharacterizationByMonads)


### As continuous linear functionals
 {#TraditionalDefinition}

Distributions come in various flavors, depending on what spaces of functions they act on. The functions they act on are called **test functions**; typically they are smooth functions on domains in Euclidean space satisfying some boundedness property. 

The widest (and generally the default) notion is as follows. 


+-- {: .num_defn #CompactlySupportedTestFunctions}
###### Definition
**(compactly supported test functions)**

For $X \subset \mathbb{R}^n$ a [[smooth manifold]] given as an [[open subset]] of a [[Euclidean space]], the [[topological vector space]] $C^\infty_c(X)$ of _compactly supported test functions_ is the following

1. the underlying set is the set of [[bump functions]], hence of [[smooth functions]] $X \to \mathbb{R}$ to the [[real numbers]] with [[compact support]];

1. equipped with evident [[real vector space]] structure given by pointwise addition and pointwise multipication of functions.

1. equipped with the [[topological space|topology]] which is the [[metric topology]] induced from the family of [[seminorms]]

   $$\rho_{K, \alpha}(f) = \sup_{x \in K} |\partial^{\alpha} f|$$ 

   where $K \subseteq U$ is [[compact topological space|compact]] and $\alpha = (\alpha_1, \ldots, \alpha_n)$ is a multi-index and 

   $$\partial^{\alpha} = \frac{\partial^{\alpha_1}}{\partial x^{\alpha_1}} \ldots \frac{\partial^{\alpha_n}}{\partial x^{\alpha_n}}$$ 

   is the corresponding [[differential operator]]. 

=--

+-- {: .num_prop}
###### Proposition

The [[topological vector space]] $C^\infty_c(X)$ of compactly supported test functions (def. \ref{CompactlySupportedTestFunctions}) is [[locally convex topological vector space|locally convex]] and [[complete space|complete]] with respect to its [[uniformity]]; it is in fact an LF-space: an [[inductive limit]] of [[Fréchet spaces]] $C_c^{\infty}(K)$ (each of which has [[empty set|empty]] [[interior]] as a [[subspace]] of $C_c^{\infty}(U)$, so by the [[Baire category theorem]], $C_c^{\infty}(U)$ is not itself a [[Fréchet space]]). 

=--

+-- {: .num_defn #DistributionOnOpenSubsetOfEuclideanSpace}
###### Definition
**(distribution on Euclidean space)**

Let $X \subset \mathbb{R}^n$ be a [[smooth manifold]] given as an [[open subset]] of [[Euclidean space]].

A **distribution on** $X$ is a [[continuous linear functional]] of the form

$$C^\infty_c(X) \longrightarrow \mathbb{R}$$ 

from the [[locally convex space|locally convex]] [[topological vector space]] of compactly supported test functions (def. \ref{CompactlySupportedTestFunctions}) to the [[real numbers]].

The space of distributions on $X$ is denoted $\mathcal{D}'(X)$ (see also remark \ref{NotationForSpaceOfDistributions}). There is an obvious bilinear pairing 

$$
  \array{
    \mathcal{D}'(X) \times C_c^{\infty}(X) &\longrightarrow& \mathbb{R}
    \\
    (S, \phi) &\mapsto& S(\phi)
  }
$$ 

given by [[evaluation]]. 

Often one writes $\langle S, \phi\rangle$ instead of $S(\phi)$. The space of distributions can be given the weak $*$-topology, meaning the smallest topology rendering the maps 

$$\langle -, \phi\rangle \;\colon\; \mathcal{D}'(U) \to \mathbb{R}$$ 

continuous for all test functions $\phi$.  As $C_c^\infty(U)$ is reflexive, this agrees with the weak topology.  

=--

See at _[[locally convex topological vector space]]_ the section _[Continuous linear functionals](locally+convex+space#ContinuousLinearFunctionals)_ for alternative characterizations of the continuity of distributions according to def. \ref{DistributionOnOpenSubsetOfEuclideanSpace}.

Notice that other natural topologies exist, such as [[uniform convergence]] on compact subsets of $C_c^\infty(U)$ (in this case, this agrees with uniform convergence on bounded subsets which usually goes by the name of the *strong* topology).


+-- {: .num_remark #NotationForSpaceOfDistributions}
###### Remark
**(notation)**

On general grounds the symbols $D(X)$ or $\mathcal{D}(X)$ or similar would seem evident notation for the space of distributions on a smooth manifold $X$. However, [[Laurent Schwartz]] in his seminal work ([Schwartz 50](#Schwartz50)) used $\mathcal{D}(X)$ to denote the space $C^\infty_c(X)$ of compactly supported continuous functions, and then $\mathcal{D}'(X)$ for its linear continuous dual, hence for the space of distributions (see also [H&#246;r#mander 90, below def. 2.1.1](#Hoermander90)). 

=--

+-- {: .num_example}
###### Example

If $f \colon X \to \mathbb{R}$ is [[locally integrable function|locally integrable]], then for all test functions $\phi$ the [[Lebesgue integral]] 

$$\langle f, \phi\rangle = \int_X f(x)\phi(x) d x $$ 

is defined; in this way a function $f$ locally integrable over $X$ may be regarded as a distribution on $X$ (explaining both the sense in which distributions are "generalized functions" and a reason for the angle-bracket notation for the evaluation pairing). In particular, there is an obvious inclusion 

$$C_c^{\infty}(X) \hookrightarrow \mathcal{D}'(X)$$ 

and this inclusion turns out to be [[dense subset|dense]]. 

=--

Other notions of spaces of distributions, each endowed with the weak $*$-topology, include 

* [[compactly supported distributions]] on $U$. These are functionals on $C^{\infty}(U)$ (test functions without compact support). 

* [[tempered distributions]] (usually on $U = \mathbb{R}^n$). These are functionals on what is called the _[[Schwartz space]]_ $\mathcal{S}$: the space of smooth functions each of whose [[derivatives]] (of any order) decays rapidly (goes to zero more quickly than any negative power of $|x|$ as $|x| \to \infty$). The topology on Schwartz space is induced by the family of seminorms 
$$\rho_{K, \alpha, \beta}(\phi) = \sup_{x \in K} |x^\alpha \partial^\beta \phi|$$ 
where $\alpha$, $\beta$ are multi-indices. 

* Rapidly decaying distributions (usually on $U = \mathbb{R}^n$). These are functionals on the space of smooth functions each of whose partial derivatives (of any order) has "tempered" or moderate growth (i.e., bounded by polynomial growth). 


+-- {: .num_prop #PullbackOfDistributionAlongSubmersion}
###### Proposition
**([[pullback of distributions]] along [[submersions]])**

If $X_1, X_2 \subset \mathbb{R}^n$ are two [[open subsets]] of [[Euclidean space]], and if

$$
  f \;\colon\; X_1 \overset{}{\longrightarrow} X_2
$$

is a [[submersion]] (i.e. its [[differential]] is a [[surjective function]] $d f_x \;\colon\; T_x X_1 \to T_{f(x)} X_2$ for all $x \in X_1$), then there is a unique [[continuous linear functional]]

$$
  f^\ast \;\colon\; \mathcal{D}'(X_2) \longrightarrow \mathcal{D}'(X_1)
$$

between spaces of distributions (def. \ref{DistributionOnOpenSubsetOfEuclideanSpace}) which extends the [[pullback of functions]] in that on a distribution represented by a [[bump function]] $b$ it is given by precomposition

$$
  f^\ast b = b \circ f
  \,.
$$

This is hence called the _[[pullback of distributions]]_.

=--

([H&#246;rmander 90, theorem 6.1.2](#Hoermander90))

+-- {: .num_defn #DistributionsOnSmoothManifolds}
###### Definition
**(distributions on smooth manifolds)**

Let $X$ be a [[smooth manifold]]. Then a distribution on $X$ is an [[equivalence class]] of 

1. a choice of smooth [[atlas]] $\{\mathbb{R}^n \underoverset{\simeq}{\psi_i}{\longrightarrow} U_i \subset X\}_{i \in I}$;

1. for each $i \in I$ a distribution $\phi_i \;\colon\; C^\infty(\mathbb{R}^n)\to \mathbb{R}$ on the $i$th [[chart]], as above;

1. such that for all pairs $(i,j) \in I \times I$ these component distributions are related on intersections of charts by pullback of distributions (def. \ref{PullbackOfDistributionAlongSubmersion}) along the coordinate change maps:

   $\phi_j =  (\psi_i^{-1} \circ \psi_j)^\ast  \phi_i $.

=--

([H&#246;rmander 90, def. 6.3.3](#Hoermander90))


### As smooth linear functionals
 {#CharacterizationByMonads}

Since [[smooth functions]] on [[smooth manifolds]] are the subject of [[differential geometry]], and since spaces of [[smooth functions]] are naturally themselves [[generalized smooth spaces]], it makes sense to ask whether distribution theory is actually a native topic to [[differential geometry]].

In particular we may ask how distributions in the [[functional analysis|functional analytic]] sense relate to the _smooth linear functions_ on smooth spaces of smooth functions. Indeed, with respect to the natural formulation of differential geometry via [[functorial geometry]] ([[topos theory]]) in terms of [[diffeological spaces]], [[smooth sets]] etc. it turns out that distributional densities are equivalently the smooth linear functionals on smooth spaces of smooth functions.

This is discussed at 

* _[[distributions are the smooth linear functionals]]_.

## Operations on distributions 

### Inducing operations by dual extension

As $\mathcal{D}'(U)$ is dual to $C_c^\infty(U)$, each continuous linear operator on $C_c^\infty(U)$ induces a corresponding linear operator on $\mathcal{D}'(U)$ in the obvious way.  Given

$$
F\colon C_c^\infty(U) \to C_c^\infty(U)
$$

we define

$$
F^*\colon \mathcal{D}'(U) \to \mathcal{D}'(U)
$$

according to the usual formula for dualities

$$
F^* S(\phi) = S(F \phi).
$$

However, since there is an obvious inclusion $C_c^\infty(U) \to \mathcal{D}'(U)$ induced by the standard inner product on $C_c^\infty(U)$, what is more usually desired is not this dual operator but an **extension** operator.  That is, instead of $F^*$ we want an operator $F^\dagger \colon \mathcal{D}'(U) \to \mathcal{D}'(U)$ with the property that for $\phi \in C_c^\infty(U)$ then $F^\dagger(\phi) = F(\phi)$ (identifying $C_c^\infty(U)$ with its image in $\mathcal{D}'(U)$).  Being slightly more careful, let us write $\iota \colon C_c^\infty(U) \to \mathcal{D}'(U)$ for the inclusion induced by the inner product.  Then we want $F^\dagger(\iota \phi) = \iota (F(\phi))$.

If the extension exists, we have

$$
F^\dagger(\iota \phi)(\psi) = \iota(F(\phi))(\psi) = \langle F(\phi), \psi \rangle
$$

Now suppose that $F$ has an adjoint, say $F^+$, with respect to the inner product.  Note that this is not automatic since $C_c^\infty(U)$ is not a Hilbert space.  Moreover, even if $F$ extends to the Hilbert completion the Hilbertian adjoint may not work since it may not define a continuous linear map on the subspace $C_c^\infty(U)$.  But if $F^+$ does exist then we have

$$
F^\dagger(\iota \phi)(\psi) = \langle F(\phi), \psi \rangle = \langle \phi, F^+(\psi) \rangle
$$

In this case, the definition of $F^\dagger$ on the whole of $\mathcal{D}'(U)$ is obvious: simply take ${F^+}^*$.  That is, the dual operator to the adjoint to $F$.  In full, $F^\dagger \colon \mathcal{D}'(U) \to \mathcal{D}'(U)$ is defined via the formula

$$
\langle F^\dagger(S),\phi\rangle = \langle S, F^+(\phi) \rangle
$$

If the ground field is $\mathbb{C}$ then this carries through essentially unchanged except for the fact that one does **not** use the inner product on $C_c^\infty(U)$ but rather the associated bilinear pairing

$$
(\phi,\psi) = \int_U \phi \psi
$$

This is to ensure that the inclusion $C_c^\infty(U) \to \mathcal{D}'(U)$ is complex linear and not conjugate linear.  Otherwise extending operators becomes complex.

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
 {#MultiplicationsOfDistributions}

See at _[[multiplication of distributions]]_

## Examples 

As explained above, any locally integrable function on $U$ defines a distribution on $U$. Other examples may be produced fairly cheaply by restriction of functionals on various TVS which contain the test functions. 

For instance: if $C_c(U)$ denotes the space of real-valued continuous functions with compact support in $U$ (topologized by uniform convergence on compacts), then a functional $\mu: C_c(U) \to \mathbb{R}$ is essentially the same as a signed measure on $U$ (Riesz-Markov theorem), i.e., there is a unique signed measure $d m$ for which 

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

The theory of distributions (and more generally of [[microlocal analysis]]) is central in [[perturbative quantum field theory]] in its rigorous incarnation via [[causal perturbation theory]]/[[perturbative algebraic quantum field theory]].

For example the reason for [[normal ordered products]] in [[Wick algebras]] is given by the H&#246;rmander criterion on [[wave front sets]] for the [[product of distributions]] to be well defind, and [[renormalization]] is understood to be the freedom in choosing [[extension of distributions]] of the resulting products of [[Feynman propagators]]. 

See also _[[operator-valued distribution]]_ and _[[Wightman axioms]]_. 

A brief survey of applications of distribution theory to perturbative quantum field theory may be found [here](http://www1.jinr.ru/Archive/Pepan/v-31-7a/I_ktp_04_t.pdf). 
  

Within mathematics, distributions are quite commonplace; for example, de Rham appropriated them for his theory of [[currents]]. Distribution theory has also long been used in the theory of partial differential equations. Here is a sample theorem: 

* **Theorem (Ehrenpreis, Malgrange):** Let $D$ be a linear differential operator on $\mathbb{R}^n$ with constant coefficients. Given a compactly supported smooth function $f$ on $\mathbb{R}^n$, there exists a smooth solution $u$ to the equation $D u = f$. 

A proof is given in these [notes](http://www-math.mit.edu/~helgason/hormander.pdf) by Helgason. The basic idea is to prove there exists a **fundamental solution** of $D$, i.e., a distribution $T$ such that $D T = \delta_0$. Then $u = f * T$ is smooth. The existence of a fundamental solution involves a theorem of Paley-Wiener type. 

## Variants

### In synthetic differential geometry 

There is another point of view on distributions: that they _can_ be modeled by actual functions provided that one admits infinite and infinitesimal quantities of the type used in Robinson [[nonstandard analysis]]. One particular approach is to formulate axiomatically the theory of distributions so that it can be interpreted in [[smooth toposes]] that model the axioms of [[synthetic differential geometry]] and support a suitable notion of invertible [[infinitesimal object]]s and infinitely large integers.

This is discussed in ([Moerdijk-Reyes 91](#MoerdijkReyes91)).

which closely mirrors the original treatment in Robinson's book Non-standard Analysis. Examples of models that support these axioms are the toposes $\mathcal{Z}$ and $\mathcal{B}$ described there. 

### Currents

In $\mathbb{R}^n$ the distributions and generalized functions boil down to the same thing, so the terminology identifies them. But on a manifold, the distributions/generalized densities (functionals on test functions) and generalized functions (functionals on test *densities*) do not agree. See V. Guillemin, S. Sternberg: _Geometric asymptotics_ ([free online](http://www.ams.org/online_bks/surv14)). While generalized functions pull back, distributions/generalized densities push forward (under some conditions, though). 

More generally one can study generalized differential $k$-forms in local coordinates they look like $\sum f_\alpha dx^{\alpha_1}\wedge \cdot \wedge dx^{\alpha_k}$. Usually they are called **currents**. They are useful e.g. in the study of higher dimensional residua in higher dimensional complex geometry (cf. *Principles of algebraic geometry* by Griffiths and Harris) and in geometric measure theory (cf. the monograph by Federer).  

### Hyperfunctions and Coulombeau distributions

Sometimes one considers larger spaces of distributions, where worse singularities than in Schwarz theory are allowed. Most well known are the theory of _[[hyperfunctions]]_ and the theory of **Coulombeau distributions**. 

### Distributions from nonstandard analysis

Distributions can be alternatively described using [[nonstandard analysis]], see there. 

## Related concepts

* [[non-singular distribution]]

* [[order of a distribution]]

* [[support of a distribution]]

  * [[point-supported distribution]]

* [[scaling degree of a distribution]]

* [[product of a distribution with a smooth function]]

* [[derivative of a distribution]]

* [[generalized solution of a partial differential equation]]

* [[extension of distributions]]

* [[tensor product of distributions]]

* [[product of distributions]]

* [[convolution product of distributions]]

* [[Hörmander topology]]

* [[Fourier transform of distributions]]

* [[Lawvere distribution]] ([[categorification]] of the concept of distributions)

## References

See also _[[hyperfunction]]_, [[ultradistribution]] and references therein.

### Traditional

Generalized functions were introduced by S. L. Sobolev in 1935, and independently (under the name _distributions_) by [[Laurent Schwartz]] in the 1940's, who unaware of Sobolev's work developed an extensive theory for them. For an infinite-dimensional variant used in the foundation of Feynman [[path integral]] see also [[Connes distribution]].

The original articles include

* {#Schwartz50} [[Laurent Schwartz]], _Th&#233;orie des distributions_, 1&#8211;2 , Hermann  (1950&#8211;1951)

* [[I. M. Gel'fand]], G.E. Shilov, _Generalized functions_, 1&#8211;5 , Acad. Press  (1966&#8211;1968) transl. from &#1048;. &#1052;. &#1043;&#1077;&#1083;&#1100;&#1092;&#1072;&#1085;&#1076;, &#1043;. &#1045;. &#1064;&#1080;&#1083;&#1086;&#1074; &#1054;&#1073;&#1086;&#1073;&#1097;&#1077;&#1085;&#1085;&#1099;&#1077; &#1092;&#1091;&#1085;&#1082;&#1094;&#1080;&#1080;, &#1074;&#1099;&#1087;. 1-3, &#1052;.:&#1060;&#1080;&#1079;&#1084;&#1072;&#1090;&#1075;&#1080;&#1079;, 1958; 1: &#1054;&#1073;&#1086;&#1073;&#1097;&#1077;&#1085;&#1085;&#1099;&#1077; &#1092;&#1091;&#1085;&#1082;&#1094;&#1080;&#1080; &#1080; &#1076;&#1077;&#1081;&#1089;&#1090;&#1074;&#1080;&#1103; &#1085;&#1072;&#1076; &#1085;&#1080;&#1084;&#1080;, 2: &#1055;&#1088;&#1086;&#1089;&#1090;&#1088;&#1072;&#1085;&#1089;&#1090;&#1074;&#1072; &#1086;&#1089;&#1085;&#1086;&#1074;&#1085;&#1099;&#1093; &#1086;&#1073;&#1086;&#1073;&#1097;&#1077;&#1085;&#1085;&#1099;&#1093; &#1092;&#1091;&#1085;&#1082;&#1094;&#1080;&#1081;, 3: &#1053;&#1077;&#1082;&#1086;&#1090;&#1086;&#1088;&#1099;&#1077; &#1074;&#1086;&#1087;&#1088;&#1086;&#1089;&#1099; &#1090;&#1077;&#1086;&#1088;&#1080;&#1080; &#1076;&#1080;&#1092;&#1092;&#1077;&#1088;&#1077;&#1085;&#1094;&#1080;&#1072;&#1083;&#1100;&#1085;&#1099;&#1093; &#1091;&#1088;&#1072;&#1074;&#1085;&#1077;&#1085;&#1080;&#1081;

* E. Magenes, G. Stampacchia, _Teoria delle distribuzioni_, Lectures Given at a Summer School of the Centro Internazionale Matematico Estivo (C.i.m.e.) Held in Saltino (Firenza) Italy, September 1-9, 1961; C.I.M.E., Ed. Cremonese, Roma, 1961; reprinted as CIME __24__, Springer 2011 [doi](http://dx.doi.org/10.1007/978-3-642-10967-6)

* {#Treves67} [[François Trèves]], _Topological Vector Spaces, Distributions and Kernels_ (Academic Press, New York, 1967)
    
Modern accounts include

* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

* Walter Rudin, chapter 6 of _Functional analysis_, McGraw-Hill, 1991

* M. Grosser, E. Farkas, M. Kunzinger, R. Steinbauer, _On the foundations of nonlinear generalized functions I, II_, Mem. Amer. Math. Soc. __153__ (2001)

* M. Kunzinger, R. Steinbauer, _Foundations of a nonlinear distributional geometry_, Acta Appl. Math. __71__, 179-206 (2002)



Lecture notes include

* Hasse Carlsson, _Lecture notes on distributions_ ([pdf](http://www.math.chalmers.se/~hasse/distributioner_eng.pdf))

and several chapters of the course

* Erik P. van den Ban, _Analysis on manifolds_ (2009) ([web](https://www.staff.science.uu.nl/~ban00101/anman2009/anman2009.html) - especially lectures 1-3)

Applications of distributions in [[physics]] are discussed in 

* V. S. Vladimirov, _Generalized functions in mathematical physics_. Moskva, Nauka 1980, Mir 1979; _Equations of mathematical physics_, Mir 1984

* [[Nikolay Bogolyubov]], A. A. Logunov, I.T. Todorov, _Introduction to axiomatic quantum field theory_, Benjamin  (1975)

Application of distributions in [[perturbative quantum field theory]] is discussed in

* {#Scharf95} [[Günter Scharf]] _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Springer 1995 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0844.53052&format=complete))

For more on this see the references at _[[perturbative AQFT]]_.

See also 

* Springer online [[eom]], _[generalized function](http://eom.springer.de/g/g043810.htm)_

References on [[Colombeau algebra]] include

* J. F. Colombeau, _New generalized functions and multiplications of distributions_, North Holland, Amsterdam (1984); _Elementary introduction in new generalized functions_, North Holland (1985)
* N. Djapi&#263;, S. Pilipovi&#263;, _Microlocal analysis of Colombeau's generalized functions on a manifold_, Indag. Math. N.S. 7, 293&#8211;309 (1996)
* Stevan Pilipovi&#263;, Milica &#381;igi&#263;, _Suppleness of the sheaf of algebras of generalized functions on manifolds_, J. Math. Anal. Appl. __379__:2 (2011) 482&#8211;486, [arxiv/1101.4552](http://arxiv.org/abs/1101.4552), [MR2784335](http://www.ams.org/mathscinet-getitem?mr=2784335), [doi](http://dx.doi.org/10.1016/j.jmaa.2010.12.060)




### In terms of smooth toposes
 {#InTermsOfSmoothToposes}

Discussion of distributions in terms morphisms out of [[internal homs]] in a [[smooth topos]] ([[distributions are the smooth linear functionals]]) is in

* {#MoerdijkReyes91} [[Ieke Moerdijk]], [[Gonzalo Reyes]], around prop. 3.6 of _[[Models for Smooth Infinitesimal Analysis]]_, Springer 1991

and for the [[Cahiers topos]] in

* {#KockReyes03} [[Anders Kock]], [[Gonzalo Reyes]], _Some calculus with extensive quantities: wave equation_, Theory and Applications of Categories , Vol. 11, 2003, No. 14, pp 321-336 ([TAC](http://www.tac.mta.ca/tac/volumes/11/14/11-14abs.html))

* {#KockReyes04} [[Anders Kock]], [[Gonzalo Reyes]], _Categorical distribution theory; heat equation_ ([arXiv:math/0407242](https://arxiv.org/abs/math/0407242))

* {#Kock11} [[Anders Kock]], _Commutative monads as a theory of distributions_ ([arxiv/1108.5952](http://arxiv.org/abs/1108.5952)) 

using results of

* {#FroelicherKriegl88} [[Alfred Frölicher]], [[Andreas Kriegl]], section 5 of  _Linear spaces and differentiation theory_, Wiley 1988 ([pdf](http://www.fuw.edu.pl/~kostecki/scans/froelicherkriegl1988.pdf))

and following the general conception of "[[intensive and extensive]]" in 

* {#Lawvere86} [[William Lawvere]], Introduction to _[[Categories in Continuum Physics]], Lectures given at a Workshop held at SUNY, Buffalo 1982. Lecture Notes in Mathematics 1174. 1986

Similar [[sheaf theory|sheaf theoretic]] discussion of distributions as morphisms of [[smooth spaces]] is in 

* {#Paugam12} [[Frédéric Paugam]], section 3.2 of _Towards the mathematics of quantum field theory_, 2012 ([pdf](https://webusers.imj-prg.fr/~frederic.paugam/documents/enseignement/master-mathematical-physics.pdf)) 



category: analysis

[[!redirects distributions]]


[[!redirects Schwartz distribution]]
[[!redirects Schwartz distributions]]


[[!redirects linear distribution]]
[[!redirects linear distributions]]

[[!redirects distributional density]]
[[!redirects distributional densities]]
