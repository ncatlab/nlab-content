
<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
The Reeh-Schlieder theorem is a theorem about [[local nets]] in the [[Haag-Kastler approach]] to [[quantum field theory]]. It states that for certain nets the set of vectors $\mathcal{M}(\mathcal{O}) \Omega$ (local algebra of a bounded open set applied to the vacuum vector, see [[Haag-Kastler vacuum representation]] for definitions and details) is dense in the given state space, a [[Hilbert space]] $\mathcal{H}$.

The Reeh-Schlieder theorem can be proven to be valid in the [[Haag-Kastler vacuum representation]], but the statement itself is sometimes used as an axiom and called the **Reeh-Schlieder property** in this case.

The Reeh-Schlieder theorem is of central importance for the mathematical structure theory of the [[Haag-Kastler approach]]. The _physical interpretation_ is counterintuitive and therefore to a certain degree controversial: Intuitively one might expect that for a localized observable $A \in \mathcal{M}(\mathcal{O})$ the vector $A \Omega$ should be localized in $\mathcal{O}$, that is the state should look like the vacuum in the causal complement of $\mathcal{O}$. But the Reeh-Schlieder theorem says that every, arbitrary state can be approximated by states of the kind $A \Omega$. This shows that the concept of _localized states_ is nontrivial in [[AQFT]] and needs to be handled with care.

Complementary statements about the asymptotic "vacuum-like appearance" of localized observables exist, too, and are commonly called [[cluster theorem]]s.

## Abstract ##
...

## Definition ##
All necessary definitions can be found at [[Haag-Kastler vacuum representation]].

## the Theorem ##
+-- {: .un_theorem}
###### Reeh-Schlieder
In the [[Haag-Kastler vacuum representation]] the vacuum vector $\Omega$ is cyclic and separating for every local algebra $\mathcal{M}(\mathcal{O})$.
=--

+-- {: .proof}
###### Proof
This proof does not strive for maximal generality, for example we specialize to $d = 4$ dimensions. The generalization to other dimensions can be done by the reader. We will comment on which part of the axioms of the vacuum representation are actually used below.

First some preliminary observations:

The covariance axiom says that we have a strongly continuous representation $U$ of the Poincare group on every local algebra, the SNAG-Theorem (see [[spectral measure]]) therefore provides us with a spectral measure for the translation subgroup $\mathcal{T}$, that we identify with $\mathbb{R}^4$

$$
\mathcal{U}(x) = \int_{k\in \mathbb{R}^4} e^{i \langle x, k\rangle} \mathcal{P}(k) \qquad \forall x \in \mathcal{T} \cong \mathbb{R}^4
$$ 

We may restrict the domain of integration to the closure of the forward lightcone $cloV_+$ by the spectrum condition. The spectral measure can be used to define operators for $z = x + i y \in \mathcal{R}^4 + i V_+$ via

$$
U(z) := \int_{cloV_+} e^{i \langle z, k\rangle} \mathcal{P}(k)
$$

The dominated convergence theorem for spectral integrals (see [[Banach space]]) tells us that the strong limit of the left side of the following equation exists and is equal to the right side:
$$
\lim_{y \downarrow 0} U(x + i y) = U (x)
$$

Next we choose a vector $u \in \mathcal{H}$ from our Hilbert space, a bounded operator $A$ on $\mathcal{H}$ and form the complex-valued function
$$
f_{u, A}(z) := \langle u, U(z) A \Omega \rangle
$$

which is holomorphic on $\mathcal{R}^4 + i V_+$ by definition and continuous on $\mathcal{R}^4 + i (V_+ \cup \{0 \}) $ by our last observation.

We can define a second such function $g$ on $\mathcal{R}^4 - i (V_+ \cup \{0 \}) $ by complex conjugation:
$$
g_{u, A}(z) = \overline{f_{u, A}(\overline z)}
$$

If there is a $U \subset \mathbb{R}^4$ open such that $f_{u, A}$ is real valued on $U$, then $f_{u, A}$ and $g_{u, A}$ coincide on $U$ and we can invoke a suitable version of the [[edge-of-the-wedge theorem]] as stated on [[analytic geometry]] to conclude that $f_{u, A}$ and $g_{u, A}$ are the branches of a unique holomorphic function, that is holomorphic at least on a complex neighborhood of $U$.

Now the proof that $\Omega$ is cyclic for $\mathcal{M}(\mathcal{O})$:

Choose a bounded open $\mathcal{O}_0$ and a neighborhood of zero $V \subset \mathcal{R}^4$ such that $\mathcal{O}_0 + V \subset \mathcal{O}$.

Suppose that $\Omega$ is not cyclic for $\mathcal{M}(\mathcal{O})$, then $\mathcal{M}(\mathcal{O}) \Omega$ is not dense in $\mathcal{H}$ and we can choose a vector $v \in \mathcal{H}, v \neq 0$ such that

$$
 \langle v, U(z) A \Omega \rangle = 0
$$
for all $A \in \mathcal{M}(\mathcal{O})$. In particular we have for all $A_0 \in \mathcal{M}(\mathcal{O}_0)$ and $x \in V$
$$
f_{v, A_0} (x) = \langle v, U(x) A_0 \Omega \rangle = \langle v, U(x) A_0 U(x)^{-1} \Omega \rangle = 0
$$

Now we see from our previous considerations that $f_{v, A_0}$ is holomorphic in a complex neighborhood of $V$, vanishes on $V$ and has therefore to vanish everywhere. 

Recall that weak additivity holds in the vacuum representation. This implies that  $\langle v, R \Omega \rangle = 0$ for all $R \in \mathcal{R}$, the global algebra. But since $\mathcal{R} \Omega$ is dense in $\mathcal{H}$ by assumption (see the axiom about the existence of a vacuum vector), we get that $v$ must be zero, contradiction: $\Omega$ has to be cyclic for $\mathcal{M}(\mathcal{O})$.

Now the proof that $\Omega$ is separating for $\mathcal{M}(\mathcal{O})$:

Choose a bounded open set $\mathcal{O}_2$ such that $\mathcal{O} \perp \mathcal{O}_2$, then by locality we have $\mathcal{M}(\mathcal{O}) \subseteq  (\mathcal{M}(\mathcal{O}_2))'$. We know already that $\Omega$ is cyclic for $(\mathcal{M}(\mathcal{O}_2))$, therefore it is separating for  $\mathcal{M}(\mathcal{O})$.

=--

Remark: TODO: which parts of the axioms are really necessary?

## Consequences ##
As several authors note the fact that the vacuum vector is separable implies that there cannot be a number operator $N$ associated to any bounded open set $\mathcal{O}$, because $N$ would anihilate the vacuum vector.

## References ##

* Wikipedia on the [Reeh-Schlieder Theorem](http://en.wikipedia.org/wiki/Reeh%E2%80%93Schlieder_theorem)

The Reeh-Schlieder theorem can be generalized from [[Minkowski spacetime]] to more general [[spacetimes]], see for example:

* Alexander Strohmaier, Rainer Verch, Manfred Wollenberg: _Microlocal analysis of quantum fields on curved spacetimes: Analytic wavefront sets and Reeh-Schlieder theorems_ ([arXiv](http://xxx.uni-augsburg.de/abs/math-ph/0202003))

About work to avoid the Reeh-Schlieder theorem and its counter intuitive implications see this:

* [[Hans Halvorson]], _Reeh-Schlieder Defeats Newton-Wigner: On alternative localization schemes in relativistic quantum field theory_ ([arXiv](http://xxx.uni-augsburg.de/abs/quant-ph/0007060))

[[!redirects Reeh-Schlieder Theorem]]
[[!redirects Reeh-Schlieder property]]
[[!redirects Reeh-Schlieder Property]]

