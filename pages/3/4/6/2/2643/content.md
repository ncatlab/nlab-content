+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


\tableofcontents


## Idea

In [[quantum mechanics]] one routinely speaks of [[eigenstates]] of [[quantum observables]] with continuous [[spectrum]], notably of eigenstates of position and of [[momentum]], written in [[bra-ket]] notation as $\vert x \rangle$ and $\vert p \rangle$ and "normalized", following [[Paul Dirac|Dirac]], in terms of the [[Dirac delta distribution]], $\langle x \vert x' \rangle = \delta(x - x')$. But these [[self-adjoint operator|self-adjoint]] [[unbounded operators]] have no actual [[eigenvectors]] in the [[Hilbert space]] of states (see [below](#NoEigenvectorsInL2)). The [[spectral theorem]] in its Hilbert space form makes rigorous sense of such operators by trading their eigenvectors for [[spectral measures]] (projection-valued measures), but in doing so it gives up the transparent picture of expanding any state in a "basis" of eigenstates, which is what makes Dirac's formalism so effective in practice.

The notion of _rigged Hilbert spaces_ (also: _equipped Hilbert spaces_, closer to the Russian original, or _[[Gelfand triples]]_) restores this picture rigorously, by enlarging the given Hilbert space $\mathcal{H}$ to a space of _generalized vectors_ in which the missing eigenvectors do exist --- much as [[distributions]], such as the [[Dirac distribution]], enlarge the space of ordinary functions. To this end one chooses a [[dense subspace]] $\Phi \subset \mathcal{H}$ (notation following [Gel'fand & Vilenkin 1961 §4.2--3](#GelfandVilenkin61)) of particularly well-behaved vectors, equipped with its own [[topological vector space|topology]], [[fine topology|finer]] than the one induced from $\mathcal{H}$ (typically making $\Phi$ a [[nuclear space|nuclear]] [[Fréchet space]], such as a [[Schwartz space]] of test functions). Since continuity with respect to this finer topology is a weaker condition, there are _more_ [[continuous map|continuous]] [[antilinear map|antilinear]] [[functionals]] on $\Phi$ than on $\mathcal{H}$ --- the latter being, by the [[Riesz representation theorem]], just the vectors of $\mathcal{H}$ themselves. This yields a triple of continuous inclusions

\[
  \Phi
  \;\subset\;
  \mathcal{H}
  \;\subset\;
  \Phi^\times
  \mathrlap{\,,}
\]

where $\Phi^\times$ denotes the space of [[continuous map|continuous]] [[antilinear map|antilinear]] [[functionals]] on $\Phi$, into which $\psi \in \mathcal{H}$ embeds as $\langle - \vert \psi \rangle$.

If now a [[self-adjoint operator]] $A$ on $\mathcal{H}$ restricts to a continuous [[linear operator]] $A \colon \Phi \to \Phi$, then it extends by duality to an operator $A^\times \colon \Phi^\times \to \Phi^\times$ on generalized vectors, given by $(A^\times F)(\phi) \coloneqq F(A \phi)$, and a _generalized eigenvector_ of $A$ with _generalized eigenvalue_ $\lambda$ is an element $F \in \Phi^\times$ with $A^\times F = \lambda F$. The _nuclear spectral theorem_ (due to Gel'fand & Kostyuchenko and to Maurin, hence also called the _Gel'fand-Maurin theorem_, see [Gel'fand & Vilenkin 1961, Ch. I](#GelfandVilenkin61), [Blanchard & Brüning 2015, Ch. 29](#BlanchardBruening15)) says that when $\Phi$ is nuclear, then $A$ has a _complete_ system of generalized eigenvectors $\vert \lambda \rangle \in \Phi^\times$, indexed by (almost all) points $\lambda$ of its spectrum (and in general also by a multiplicity label, here suppressed), in that there is a [[measure]] $\mu$ on the spectrum such that

$$
  {\langle \phi \vert \psi \rangle}
  \;=\;
  \int
    {\langle \phi \vert \lambda \rangle}
    \,
    {\langle \lambda \vert \psi \rangle}
  \;
  \mathrm{d}\mu(\lambda)
  \;\;\;\;\;\;
  \text{for all}\; \phi, \psi \in \Phi
  \,.
$$

This is the rigorous form of Dirac's _completeness relation_ "$\int {\vert \lambda \rangle} {\langle \lambda \vert} \, \mathrm{d}\mu(\lambda) = \mathrm{id}$".

In this way, rigged Hilbert spaces provide a rigorous home for Dirac's [[bra-ket]] formalism: Kets ${\vert F \rangle}$ are elements of $\Phi^\times$, the corresponding bras $\langle F \vert$ are their complex conjugates, which are elements of the dual space $\Phi'$ of continuous _linear_ functionals, and a bracket

$$
  \langle \phi \vert F \rangle \;\coloneqq\; F(\phi)
  \,,
  \;\;\;\;\;\;
  \langle F \vert \phi \rangle \;\coloneqq\; \overline{F(\phi)}
$$

is well-defined as long as at least one of its two entries is a test vector in $\Phi$. (Brackets between two generalized vectors, such as $\langle x \vert x' \rangle$, are not defined in general; see [below](#BraKetDictionary) for what they stand for.)


## Examples
 {#Examples}

### Position and momentum on the line
 {#PositionAndMomentum}

The archetypical example is the [[quantum mechanics]] of a particle on the line, with the eigenstates of position and of momentum as generalized vectors. Throughout, let

$$
  \mathcal{H}
  \;\coloneqq\;
  L^2(\mathbb{R})
  \,,
  \;\;\;\;\;\;
  \langle \phi \vert \psi \rangle
  \;\coloneqq\;
  \int_{\mathbb{R}}
    \overline{\phi(x)} \, \psi(x)
  \, \mathrm{d}x
$$

be the [[Hilbert space]] of square-integrable functions on the real line, with respect to [[Lebesgue measure]], with inner product (as usual in physics) antilinear in its first argument.

#### The problem
 {#TheProblem}

The _position operator_ $X$ and the _momentum operator_ $P$ (in units with $\hbar = 1$)

$$
  (X \psi)(x)
  \;\coloneqq\;
  x \cdot \psi(x)
  \,,
  \;\;\;\;\;\;\;\;
  (P \psi)(x)
  \;\coloneqq\;
  - i \frac{\mathrm{d}}{\mathrm{d}x} \psi(x)
$$

are [[unbounded operator|unbounded]] [[self-adjoint operators]] on $\mathcal{H}$, defined not on all of $\mathcal{H}$ but on [[dense subspace|dense]] domains (for instance $D(X) = \big\{ \psi \in L^2(\mathbb{R}) \,\big\vert\, x \cdot \psi \in L^2(\mathbb{R}) \big\}$). Both have [[spectrum]] all of $\mathbb{R}$, but:

+-- {: .num_remark #NoEigenvectorsInL2}
###### Remark
**(no eigenvectors in the Hilbert space)**

Neither $X$ nor $P$ has a single [[eigenvector]] in $\mathcal{H}$:

* If $X \psi = \xi \psi$, then $(x - \xi) \psi(x) = 0$ for almost all $x$, whence $\psi = 0 \in L^2(\mathbb{R})$.

* If $P \psi = k \psi$, then $\psi' = i k \psi$ in the sense of [[distributions]], whence $\psi(x) = c \, e^{i k x}$, which is square-integrable only for $c = 0$.

The would-be eigenfunctions, namely the [[Dirac distribution]] $\delta(x - \xi)$ and the plane wave $e^{i k x}$, do make sense, but as [[distributions]] instead of as elements of $L^2(\mathbb{R})$. The rigged Hilbert space makes this precise.

=--

#### The rigging
 {#TheRigging}

As the space of test vectors take the [[Schwartz space]] $\mathcal{S}(\mathbb{R})$ of [[smooth functions]] all of whose derivatives are [[rapidly decreasing function|rapidly decreasing]], with its [[Fréchet space]]-topology given by the [[seminorms]]

$$
  p_{m,n}(\phi)
  \;\coloneqq\;
  \sup_{x \in \mathbb{R}}
  \left\vert
    x^m \, \phi^{(n)}(x)
  \right\vert
  \,,
  \;\;\;\;\;\;
  m, n \in \mathbb{N}
  \,,
$$

and write

$$
  \widehat{\phi}(k)
  \;\coloneqq\;
  \frac{1}{\sqrt{2\pi}}
  \int_{\mathbb{R}}
    e^{- i k x} \, \phi(x)
  \, \mathrm{d}x
$$

for the [[Fourier transform]].

+-- {: .num_prop #PropertiesOfTheSchwartzRigging}
###### Proposition
**(Schwartz space as test space for position and momentum)**

1. The inclusion $\mathcal{S}(\mathbb{R}) \hookrightarrow L^2(\mathbb{R})$ is continuous with dense image.

1. $X$ and $P$ restrict to continuous linear operators $\mathcal{S}(\mathbb{R}) \to \mathcal{S}(\mathbb{R})$.

1. The Fourier transform restricts to a linear automorphism of $\mathcal{S}(\mathbb{R})$ which preserves the inner product (by the Plancherel theorem) and turns $P$ into multiplication by the momentum variable, $\widehat{P\phi}(k) = k \, \widehat{\phi}(k)$ (and $X$ into $i \frac{\mathrm{d}}{\mathrm{d}k}$).

1. $\mathcal{S}(\mathbb{R})$ is a [[nuclear space]].

=--

+-- {: .proof}
###### Proof
Using $1 + x^2 \leq (1 + \vert x \vert)^2$ we have

$$
  \Vert \phi \Vert^2_{L^2}
  \;=\;
  \int_{\mathbb{R}}
    \frac{
      (1 + x^2) \, \vert \phi(x) \vert^2
    }{
      1 + x^2
    }
  \, \mathrm{d}x
  \;\leq\;
  \pi
  \,
  \big(
    p_{0,0}(\phi) + p_{1,0}(\phi)
  \big)^2
  \,,
$$

which gives the continuity in the first item, while density holds since already the compactly supported smooth functions are dense in $L^2(\mathbb{R})$. For the second item, the Leibniz rule gives

$$
  p_{m,n}(X \phi)
  \;\leq\;
  p_{m+1,n}(\phi) + n \, p_{m,n-1}(\phi)
  \,,
  \;\;\;\;\;\;
  p_{m,n}(P \phi)
  \;=\;
  p_{m,n+1}(\phi)
$$

(with $p_{m,-1} \coloneqq 0$). The last two items are standard, see at *[[Schwartz space]]* and at *[[nuclear space]]*.
=--

Now let $\mathcal{S}^\times(\mathbb{R})$ be the space of continuous antilinear functionals $F \colon \mathcal{S}(\mathbb{R}) \to \mathbb{C}$. Since $\mathcal{S}(\mathbb{R})$ is closed under complex conjugation, $F \mapsto F\big(\overline{(-)}\big)$ is a linear isomorphism onto the usual space $\mathcal{S}'(\mathbb{R})$ of [[tempered distributions]], so that $\mathcal{S}^\times(\mathbb{R})$ is just the space of tempered distributions in a guise adapted to the inner product. Concretely, every locally integrable function $f$ of at most polynomial growth defines an element of $\mathcal{S}^\times(\mathbb{R})$ by

$$
  \langle \phi \vert f \rangle
  \;\coloneqq\;
  \int_{\mathbb{R}}
    \overline{\phi(x)}
    \,
    f(x)
  \,\mathrm{d}x
  \,,
$$

and so does every $f \in L^2(\mathbb{R})$, continuously so by the Cauchy-Schwarz inequality and the first item of Prop. \ref{PropertiesOfTheSchwartzRigging}. The resulting map $L^2(\mathbb{R}) \to \mathcal{S}^\times(\mathbb{R})$ is injective, since $\mathcal{S}(\mathbb{R})$ is dense in $L^2(\mathbb{R})$, and so we have the rigged Hilbert space

$$
  \mathcal{S}(\mathbb{R})
  \;\subset\;
  L^2(\mathbb{R})
  \;\subset\;
  \mathcal{S}^\times(\mathbb{R})
  \;\simeq\;
  \mathcal{S}'(\mathbb{R})
  \,.
$$

For $F \in \mathcal{S}^\times(\mathbb{R})$ and $\phi \in \mathcal{S}(\mathbb{R})$ we write, as in the Idea section, $\langle \phi \vert F \rangle \coloneqq F(\phi)$ and $\langle F \vert \phi \rangle \coloneqq \overline{F(\phi)}$, which for $F \in L^2(\mathbb{R})$ reproduces the inner product.

Finally, for $A \in \{X, P\}$ define $A^\times \colon \mathcal{S}^\times(\mathbb{R}) \to \mathcal{S}^\times(\mathbb{R})$ by

$$
  \langle \phi \vert A^\times F \rangle
  \;\coloneqq\;
  \langle A \phi \vert F \rangle
  \,.
$$

By self-adjointness of $A$, this restricts on the domain $D(A) \subset L^2(\mathbb{R}) \subset \mathcal{S}^\times(\mathbb{R})$ to the original operator $A$, while under the identification $\mathcal{S}^\times(\mathbb{R}) \simeq \mathcal{S}'(\mathbb{R})$ it is the usual action of $x \cdot (-)$ and of $-i \frac{\mathrm{d}}{\mathrm{d}x}$ on tempered distributions.

#### Generalized eigenvectors
 {#GeneralizedEigenvectors}

For $\xi, k \in \mathbb{R}$ consider the generalized vectors $\delta_\xi, e_k \in \mathcal{S}^\times(\mathbb{R})$ given by

$$
  \langle \phi \vert \delta_\xi \rangle
  \;\coloneqq\;
  \overline{\phi(\xi)}
  \,,
  \;\;\;\;\;\;\;\;
  e_k(x)
  \;\coloneqq\;
  \frac{1}{\sqrt{2\pi}} e^{i k x}
  \,,
$$

hence with

$$
  \langle \delta_\xi \vert \phi \rangle
  \;=\;
  \phi(\xi)
  \,,
  \;\;\;\;\;\;\;\;
  \langle e_k \vert \phi \rangle
  \;=\;
  \widehat{\phi}(k)
  \,.
$$

(These are continuous on $\mathcal{S}(\mathbb{R})$, since $\vert \langle \phi \vert \delta_\xi \rangle \vert \leq p_{0,0}(\phi)$ and $\vert \langle \phi \vert e_k \rangle \vert \leq \sqrt{\pi/2} \, \big( p_{0,0}(\phi) + p_{2,0}(\phi) \big)$.)

+-- {: .num_prop #PositionAndMomentumEigenvectors}
###### Proposition
**(generalized position and momentum eigenvectors)**

For all $\xi, k \in \mathbb{R}$ we have

$$
  X^\times \delta_\xi \;=\; \xi \, \delta_\xi
  \,,
  \;\;\;\;\;\;\;\;
  P^\times e_k \;=\; k \, e_k
  \,.
$$

=--

+-- {: .proof}
###### Proof
For all $\phi \in \mathcal{S}(\mathbb{R})$ we have, using that $\xi$ is real,

$$
  \langle \phi \vert X^\times \delta_\xi \rangle
  \;=\;
  \langle X\phi \vert \delta_\xi \rangle
  \;=\;
  \overline{\xi \, \phi(\xi)}
  \;=\;
  \xi \, \langle \phi \vert \delta_\xi \rangle
  \,,
$$

and, by integration by parts (the boundary terms vanishing since $\phi$ is rapidly decreasing while $e_k$ is bounded),

$$
  \begin{aligned}
    \langle \phi \vert P^\times e_k \rangle
    & =\;
    \langle P \phi \vert e_k \rangle
    \;=\;
    \int_{\mathbb{R}}
      i \, \overline{\phi'(x)}
      \, e_k(x)
    \,\mathrm{d}x
    \\
    & =\;
    - i
    \int_{\mathbb{R}}
      \overline{\phi(x)}
      \, e_k'(x)
    \,\mathrm{d}x
    \;=\;
    k \, \langle \phi \vert e_k \rangle
    \,.
  \end{aligned}
$$

=--

#### Completeness and Dirac's notation
 {#CompletenessAndDiracNotation}

+-- {: .num_prop #CompletenessRelations}
###### Proposition
**(completeness relations)**

For all $\phi, \psi \in \mathcal{S}(\mathbb{R})$ we have

$$
  \langle \phi \vert \psi \rangle
  \;=\;
  \int_{\mathbb{R}}
    \langle \phi \vert \delta_\xi \rangle
    \,
    \langle \delta_\xi \vert \psi \rangle
  \,\mathrm{d}\xi
  \;=\;
  \int_{\mathbb{R}}
    \langle \phi \vert e_k \rangle
    \,
    \langle e_k \vert \psi \rangle
  \,\mathrm{d}k
  \,;
$$

equivalently, every test vector $\psi$ has the generalized eigenvector expansions

$$
  \psi
  \;=\;
  \int_{\mathbb{R}}
    \psi(\xi)
    \,
    \delta_\xi
  \,\mathrm{d}\xi
  \;=\;
  \int_{\mathbb{R}}
    \widehat{\psi}(k)
    \,
    e_k
  \,\mathrm{d}k
  \,,
$$

where the integrals converge weakly in $\mathcal{S}^\times(\mathbb{R})$, i.e. after pairing with any $\phi \in \mathcal{S}(\mathbb{R})$.

=--

+-- {: .proof}
###### Proof
The integrands are $\overline{\phi(\xi)} \, \psi(\xi)$ and $\overline{\widehat{\phi}(k)} \, \widehat{\psi}(k)$, respectively. Hence the first equality is the definition of the inner product on $L^2(\mathbb{R})$, and the second is the Plancherel theorem. In the weak form, the second expansion of $\psi$ is thereby [[Fourier transform|Fourier inversion]].
=--

+-- {: .num_remark #BraKetDictionary}
###### Remark
**(Dirac's notation)**

In Dirac's [[bra-ket]] notation, $\delta_x$ is the position eigenket $\vert x \rangle$ and $e_p$ is the momentum eigenket $\vert p \rangle$, and the above says precisely that:

* $\langle x \vert \psi \rangle = \psi(x)$ and $\langle p \vert \psi \rangle = \widehat{\psi}(p)$ are the wavefunctions of $\psi$ in the position and in the momentum representation, respectively;

* $\int \vert x \rangle \langle x \vert \, \mathrm{d}x = \mathrm{id} = \int \vert p \rangle \langle p \vert \, \mathrm{d}p$ are the completeness relations of Prop. \ref{CompletenessRelations};

* $\langle x \vert p \rangle = \frac{1}{\sqrt{2\pi}} e^{i p x}$ --- here, exceptionally, a bracket between two generalized vectors makes sense, because $e_p$ is a smooth function, whose value at $x$ is defined.

On the other hand, formulas such as $\langle x \vert x' \rangle = \delta(x - x')$ and $\langle p \vert p' \rangle = \delta(p - p')$ pair two generalized vectors and have no literal meaning in the rigged Hilbert space; they are mnemonics for the completeness relations, obtained by formally inserting $\psi = \vert x' \rangle$ (resp. $\psi = \vert p' \rangle$) into the expansions of Prop. \ref{CompletenessRelations}.

=--

+-- {: .num_remark #DependenceOnTestSpace}
###### Remark
**(dependence on the choice of test space)**

In this example, the generalized eigenvalues of $X$ and $P$ on $\mathcal{S}^\times(\mathbb{R})$ are exactly the points of their spectrum $\mathbb{R}$: For $\lambda \in \mathbb{C} \setminus \mathbb{R}$, multiplication by the function $1/(x - \overline{\lambda})$ (all of whose derivatives are bounded) is a continuous inverse to $X - \overline{\lambda}$ on $\mathcal{S}(\mathbb{R})$, so that $X^\times - \lambda = (X - \overline{\lambda})^\times$ is invertible on $\mathcal{S}^\times(\mathbb{R})$ and hence has trivial kernel; similarly for $P$, via Fourier transform.

But the generalized eigenvalues do depend on the choice of test space:

* A smaller test space has a larger antidual, which may contain spurious generalized eigenvectors. For instance, with the space $C^\infty_c(\mathbb{R})$ of compactly supported smooth functions (also nuclear and also preserved by $X$ and $P$) as test space, the antidual (equivalently: all [[distributions]]) contains $e^{i k x}$ for every complex number $k$, and these are generalized eigenvectors of $P$ with non-real eigenvalue $k$, which do not contribute to the completeness relation.

* A larger test space with coarser topology may lose the generalized eigenvectors. For instance, on the domain $D(X)$ with its graph norm, point evaluations $\phi \mapsto \phi(\xi)$ are not even defined (elements of $D(X)$ being only $L^2$-classes), and so its antidual contains no $\delta_\xi$.

The Schwartz space sits well between these extremes, simultaneously for $X$ and for $P$, which is no accident:

=--

+-- {: .num_remark #HermiteRealization}
###### Remark
**(intrinsic characterization via the harmonic oscillator)**

The Schwartz space is intrinsically determined by $X$ and $P$: It is the space of smooth vectors of the Schrödinger representation of the [[Heisenberg group]] on $L^2(\mathbb{R})$, and coincides with the intersection $\bigcap_{n} D(N^n)$ of the domains of all powers of the [[harmonic oscillator]] Hamiltonian $N \coloneqq \tfrac{1}{2}(X^2 + P^2)$. Expanding in the orthonormal basis of Hermite functions $h_n$, which are honest eigenvectors $N h_n = (n + \tfrac{1}{2}) h_n$, identifies the above rigged Hilbert space with

$$
  s
  \;\subset\;
  \ell^2
  \;\subset\;
  s^\times
  \,,
$$

where $s$ is the space of rapidly decreasing sequences and $s^\times$ that of sequences of at most polynomial growth. In this form the nuclearity of $\mathcal{S}(\mathbb{R}) \simeq s$ is manifest: $s$ is the intersection of the weighted Hilbert spaces $\ell^2_m \coloneqq \big\{ (c_n)_{n \in \mathbb{N}} \,\big\vert\, \sum_n (n+1)^{2m} \vert c_n \vert^2 \lt \infty \big\}$, and the inclusions $\ell^2_{m+1} \hookrightarrow \ell^2_m$ are [[Hilbert-Schmidt operator|Hilbert-Schmidt]].

=--


## Related concepts

* [[Gelfand triple]]

* [[spectral theorem]], [[spectral measure]]

* [[distribution]], [[tempered distribution]]

* [[bra-ket]]


## References

The notion of rigged Hilbert spaces, together with the nuclear spectral theorem for them, is due to:

* {#GelfandVilenkin61} [[I. M. Gel'fand]], N. Ya. Vilenkin, §I.4 of: *Generalized Functions, Vol. 4: Applications of Harmonic Analysis*, Fizmatgiz, Moscow (1961); English translation: Academic Press (1964); reprint: AMS Chelsea (2016) &lbrack;[doi:10.1090/chel/380](https://doi.org/10.1090/chel/380)&rbrack;

Early treatments in the context of Dirac's [[bra-ket]] formalism:

* [[John E. Roberts]]: *The Dirac Bra and Ket Formalism*, J. Math. Phys. **7** (1966) 1097--1104 &lbrack;[doi:10.1063/1.1705001](https://doi.org/10.1063/1.1705001)&rbrack;

* [[John E. Roberts]]: *Rigged Hilbert spaces in quantum mechanics*, Communications in Mathematical Physics **3** (1966) 98--119 &lbrack;[doi:10.1007/BF01645448](https://doi.org/10.1007/BF01645448)&rbrack;

Textbook account, including the nuclear spectral theorem:

* {#BlanchardBruening15} Philippe Blanchard, Erwin Brüning, Ch. 29 of: *Mathematical Methods in Physics -- Distributions, Hilbert Space Operators, Variational Methods, and Applications in Quantum Physics*, Progress in Mathematical Physics **69**, Birkhäuser (2015) &lbrack;[doi:10.1007/978-3-319-14045-2](https://doi.org/10.1007/978-3-319-14045-2)&rbrack;

Pedagogical introduction aimed at physicists, via an exactly solvable example:

* Rafael de la Madrid: *The role of the rigged Hilbert space in Quantum Mechanics*, Eur. J. Phys. **26** (2005) 287--312 &lbrack;[doi:10.1088/0143-0807/26/2/008](https://doi.org/10.1088/0143-0807/26/2/008), [arXiv:quant-ph/0502053](https://arxiv.org/abs/quant-ph/0502053)&rbrack;

Claim of a unification of various inequivalent approaches:

* M. Gadella, F. Gómez, _A Unified Mathematical Formalism for the Dirac Formulation of Quantum Mechanics_, Foundations of Physics **32** (2002) 815--869 &lbrack;[doi:10.1023/A:1016069311589](https://doi.org/10.1023/A:1016069311589)&rbrack;

See also:

* S. Wickramasekara, A. Bohm, _Symmetry Representations in the Rigged Hilbert Space Formulation of Quantum Mechanics_ &lbrack;[arXiv:math-ph/0302018](http://arxiv.org/abs/math-ph/0302018)&rbrack;

* MathOverflow: *[Good references for Rigged Hilbert spaces?](https://mathoverflow.net/questions/43313/good-references-for-rigged-hilbert-spaces)*


[[!redirects rigged Hilbert spaces]]

[[!redirects equipped Hilbert space]]
[[!redirects equipped Hilbert spaces]]

[[!redirects nuclear spectral theorem]]