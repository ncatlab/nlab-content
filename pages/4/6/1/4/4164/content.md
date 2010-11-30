
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##

The Reeh-Schlieder theorem is a theorem about [[local nets]] in the [[Haag-Kastler approach]] to [[quantum field theory]]. It states that for certain nets the set of vectors $\mathcal{M}(\mathcal{O}) \Omega$ (local algebra of a bounded open set applied to the vacuum vector, see [[Haag-Kastler vacuum representation]] for definitions and details) is dense in the given [[state]] space, a [[Hilbert space]] $\mathcal{H}$.

The Reeh-Schlieder theorem can be proven to be valid in the [[Haag-Kastler vacuum representation]], but the statement itself is sometimes used as an axiom and called the **Reeh-Schlieder property** in this case.

The Reeh-Schlieder theorem is of central importance for the mathematical structure theory of the [[Haag-Kastler approach]]. The _physical interpretation_ is counterintuitive and therefore to a certain degree controversial: Intuitively one might expect that for a localized observable $A \in \mathcal{M}(\mathcal{O})$ the vector $A \Omega$ should be localized in $\mathcal{O}$, that is the state should look like the vacuum in the causal complement of $\mathcal{O}$. But the Reeh-Schlieder theorem says that every, arbitrary state can be approximated by states of the kind $A \Omega$. This shows that the concept of _localized states_ is nontrivial in [[AQFT]] and needs to be handled with care.

Complementary statements about the asymptotic "vacuum-like appearance" of localized observables exist, too, and are commonly called [[cluster theorem]]s.

In other parts of the physics literature, notably in the context of [[CFT]], the Reeh-Schlieder property is also called the **state-operator correspondence**. See also the remark in ([Schroer, footnote 14, page 34](#Schroer)).

## Abstract ##

We state the theorem for a vacuum representation on [[Minkowski spacetime]]. Since the theorem has some controverse consequences for the physical interpretation of the theory, some of which will be mentioned in the corresponding paragraph, we take a quick look at which axioms really enter into the proof of the theorem. The references include work on the generalization of the theorem to more general [[spacetimes]] as well as work concerned with dodging the theorem and its consequences by choosing an alternative set of axioms.

## Definition ##
All necessary definitions can be found at [[Haag-Kastler vacuum representation]].

## the Theorem ##
Both the statement and the proof we mention here refer to the [[Haag-Kastler vacuum representation]], but both the statement and the proof can be generalized resp. translated to different contexts, like e.g. to a [[Wightman theory]], to more general spacetimes and to other states than the vacuum vector.

+-- {: .un_theorem}
###### Reeh-Schlieder
In the [[Haag-Kastler vacuum representation]] the vacuum vector $\Omega$ is [[cyclic vector|cyclic]] and [[separating vector|separating]] for every local algebra $\mathcal{M}(\mathcal{O})$.

=--

+-- {: .proof}
###### Proof
This proof does not strive for maximal generality, for example we specialize to $d = 4$ dimensions. The generalization to other dimensions can be done by the reader. We will comment on which part of the axioms of the vacuum representation are actually used below.

First some preliminary observations:

The covariance axiom says that we have a strongly continuous representation $U$ of the Poincare group, the SNAG-Theorem (see [[spectral measure]]) therefore provides us with a spectral measure for the translation subgroup $\mathcal{T}$, that we identify with $\mathbb{R}^4$

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

Now the proof that $\Omega$ is [[cyclic vector|cyclic]] for $\mathcal{M}(\mathcal{O})$:

Choose a bounded open $\mathcal{O}_0$ and a neighborhood of zero $V \subset \mathcal{R}^4$ such that $\mathcal{O}_0 + V \subset \mathcal{O}$.

Suppose that $\Omega$ is not cyclic for $\mathcal{M}(\mathcal{O})$, then $\mathcal{M}(\mathcal{O}) \Omega$ is not dense in $\mathcal{H}$ and we can choose a vector $v \in \mathcal{H}, v \neq 0$ such that

$$
 \langle v, U(z) A \Omega \rangle = 0
$$
for all $A \in \mathcal{M}(\mathcal{O})$. In particular we have for all $A_0 \in \mathcal{M}(\mathcal{O}_0)$ and $x \in V$
$$
f_{v, A_0} (x) = \langle v, U(x) A_0 \Omega \rangle = \langle v, U(x) A_0 U(x)^{-1} \Omega \rangle = 0
$$

Now we see from our previous considerations that there is a function holomorphic in a complex neighborhood of $V$ that restricts to $f_{v, A_0}$ on $V$, vanishes on $V$ and has therefore to vanish everywhere. That means the previous equality holds for arbitrary translations $U(x), x \in \mathbb{R}^4$. 

Recall that weak additivity holds in the vacuum representation. This together with the previous statement implies that  $\langle v, R \Omega \rangle = 0$ for all $R \in \mathcal{R}$, the global algebra. But since $\mathcal{R} \Omega$ is dense in $\mathcal{H}$ by assumption (see the axiom about the existence of a vacuum vector), we get that $v$ must be zero, contradiction: $\Omega$ has to be cyclic for $\mathcal{M}(\mathcal{O})$.

Now the proof that $\Omega$ is [[separating vector|separating]] for $\mathcal{M}(\mathcal{O})$:

Choose a bounded open set $\mathcal{O}_2$ such that $\mathcal{O} \perp \mathcal{O}_2$, then by locality we have $\mathcal{M}(\mathcal{O}) \subseteq  (\mathcal{M}(\mathcal{O}_2))'$. We know already that $\Omega$ is cyclic for $\mathcal{M}(\mathcal{O}_2)$, therefore it is separating for  $\mathcal{M}(\mathcal{O})$.

=--

## Preconditions Needed for the Proof ##
Since the theorem and its consequences are counterintuitive for the physical interpretation of the theory, it is worthwhile to take a look which axioms enter the proof: Is the theorem a true feature of [[quantum field theory]] or is it an artifact caused by ill chosen assumptions?

The proof that the vacuum vector is cyclic given in the previous paragraph makes use of:

1. Strong representation of the translation subgroup and the spectrum condition.

Note that we do not needed the representation of the whole Poincare group, but really only that of the translations.

2. isotony,

3. weak additivity and

4. of course the existence of the vacuum vector itself and that $\mathcal{R} \Omega$ is dense in $\mathcal{H}$.

Now weak additivity can be proven to hold using isotony and additiviy. 

It is sometimes argued that the Reeh-Schlieder theorem - that is the part that the vacuum vector is cyclic for every local algebra - is somehow a contradiction to _locality_ . The remarkable fact in this context is that  **the locality axiom does not enter the proof** that the vacuum vector is cyclic. (It was used for the proof that the vacuum vector is also separating, though).

For some further elaboration of this point see the paper by Halvorson cited in the references.

## Consequences ##
The fact that the vacuum vector is separating implies that there cannot be a number operator $N$ associated to any bounded open set $\mathcal{O}$, because $N$ would annihilate the vacuum vector. This implies that the notion of _particles_ in relativistic quantum physics cannot be quite as simple as in classical physics or in nonrelativistic quantum physics.

More generally there cannot be a nonzero localized observable that annihilates the vacuum. This implies that the stress-energy tensor, if localized to a bounded region, cannot be a positive operator, since its expectation value in the vacuum is zero, in fact it cannot be bounded from below. This is sometimes mentioned as a pathology occuring in general spacetimes that do not have a global timelike [[Killing vector]] field, but in our context it actually holds in [[Minkowski spacetime]] in the vacuum state.

The fact that the vacuum vector is cyclic means that any arbitrary state in the vacuum representation can be approximated by measurements in an arbitrary small bounded open region applied to the vacuum vector. This fact is sometimes referred to as the existence of [[vacuum fluctuations]]. A direct consequence of the Reeh-Schlieder theorem is therefore that to any regions $\mathcal{O}_1, \mathcal{O}_2$, no matter how far apart, there are many projections in the corresponding local algebras that are positively correlated in the vacuum state.

## References ##

* Wikipedia on the [Reeh-Schlieder Theorem](http://en.wikipedia.org/wiki/Reeh%E2%80%93Schlieder_theorem)

A discussion of the consequences for the physical interpretation of the Reeh-Schlieder theorem and further references can be found here:

* Stephen J. Summers: _Yet More Ado About Nothing: The Remarkable Relativistic Vacuum State_ ([arXiv] (http://de.arxiv.org/abs/0802.1854v2))

The Reeh-Schlieder theorem can be generalized from [[Minkowski spacetime]] to more general [[spacetimes]], see for example:

* Alexander Strohmaier, Rainer Verch, Manfred Wollenberg: _Microlocal analysis of quantum fields on curved spacetimes: Analytic wavefront sets and Reeh-Schlieder theorems_ ([arXiv](http://xxx.uni-augsburg.de/abs/math-ph/0202003))

About work to avoid the Reeh-Schlieder theorem and its counter intuitive implications see this:

* [[Hans Halvorson]], _Reeh-Schlieder Defeats Newton-Wigner: On alternative localization schemes in relativistic quantum field theory_ ([arXiv](http://xxx.uni-augsburg.de/abs/quant-ph/0007060))

The observation that the Reeh-Schlieder property describes what elsewhere is called the _operator-state correspondence_ is made explicit for instance in footnote 14 on page 34 of

* [[Bert Schroer]], _Particle Physics and QFT at the Turn of the Century:
Old principles with new concepts_ ([pdf](http://biblioteca.cat.cbpf.br/pub/apub/nf/2000/nf01900.pdf))
{#Schroer}

[[!redirects Reeh-Schlieder Theorem]]
[[!redirects Reeh-Schlieder property]]
[[!redirects Reeh-Schlieder Property]]

[[!redirects operator-state correspondence]]
[[!redirects state-operator correspondence]]