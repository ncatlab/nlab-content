
\tableofcontents

## Idea ##

The [[HoTT book complex number]] are the [[complex numbers]] constructed over the [[HoTT book real number]], as developed in Section 11.3 of [UFP 2013](#UFP13).

Let $\mathbb{R}_H$ denote the [[type]] of [[HoTT book real numbers]]. The corresponding complex number type $\mathbb{C}_H$ is defined as the [[Cartesian product]] $\mathbb{R}_H \times \mathbb{R}_H$, equipped with the usual complex addition and multiplication.

Although the underlying construction is elementary, establishing its algebraic properties within [[constructive mathematics]] is non-trivial and depends on the corresponding properties of the HoTT book reals. In particular, the treatment of nonzero elements and multiplicative [[inverse]]s requires distinguishing constructive [[apartness]] from the mere [[negation]] of [[equality]].

The resulting [[group of units|multiplicative group of units]], $\mathbb{C}_H^\times$, admits a [[delooping]] $B\mathbb{C}_H^\times$. This provides a natural setting for studying [[group action]]s on complex numbers, [[local system]]s, and [[monodromy]] in [[homotopy type theory]].



## Definition ##

###Classical construction###

We define the [[HoTT book complex number]] as an [[ordered pair]] of [[HoTT book real number]]s:

$$
\mathbb{C}_H \coloneqq \{z = (a,b) \mid a,b \in \mathbb{R}_H\} = \mathbb{R}_H \times \mathbb{R}_H.
$$

By the [[formation rule]] for the [[product type]], $\mathbb{C}_H$ belongs to the same [[universe]] as $\mathbb{R}_H$.

Since $\mathbb{R}_H$ is a [[set]] ([[0-type]]), for any two complex numbers $z = (a,b)$ and $w = (c,d)$, there is an equivalence of [[identity types]]:

$$
(z = w) \simeq (a = c) \times (b = d).
$$

Since the product of two [[proposition]]s is again a proposition, $\mathbb{C}_H$ is also a set. In other words,

$$
\mathrm{isSet}(\mathbb{C}_H)
\coloneqq
\prod_{x,y:\mathbb{C}_H} \mathrm{isProp}(x=y)
$$

is inhabited.


### As a product type ###

Unlike the [[HoTT book real number]], which is constructed as a [[higher inductive-inductive type]], the [[HoTT book complex number]] is defined by an ordinary [[product type]], without introducing additional higher inductive constructors.

### Algebraic operations ###

Let $z=(a,b)$ and $w=(c,d)$ be elements of $\mathbb{C}_H$. The addition and multiplication are defined by

$$
z+w := (a+c,b+d), \qquad zw := (ac-bd,ad+bc).
$$

The additive and multiplicative identities are $0_{\mathbb{C}_H}:=(0,0)$ and $1_{\mathbb{C}_H}:=(1,0)$, respectively. The imaginary unit $i:=(0,1)$ satisfies $i^2=-1_{\mathbb{C}_H}$.

The additive inverse is $-(a,b):=(-a,-b)$, while the complex conjugate is $\overline{(a,b)}:=(a,-b)$.

These operations give $\mathbb{C}_H$ the structure of a [[commutative ring]], inherited from the algebraic properties of $\mathbb{R}_H$.


## Properties ##

### Constructive apartness ###

In [[constructive mathematics]], the [[negation]] of [[equality]] does not in general provide sufficient information to construct a multiplicative inverse. Hence, the notion of [[apartness]] plays an important role in the algebraic structure of $\mathbb{C}_H$.

Recall that the [[HoTT book real number]] is equipped with a [[strict order]], which induces the apartness relation $a \# b$ defined by $a \lt b$ or $b \lt a$.

For any $z=(a,b)$ and $w=(c,d)$ in $\mathbb{C}_H$, define the complex apartness relation by

$$
z \# w \coloneqq (a \# c) \lor (b \# d).
$$

In particular, $z \# 0_{\mathbb{C}_H}$ expresses that at least one of its real components is apart from zero.

This is stronger than merely assuming $\neg(z=0_{\mathbb{C}_H})$ in [[constructive logic]].

### Multiplicative inverses ###

For $z=(a,b)$, define its squared modulus by $N(z):=a^2+b^2$. By the algebraic properties of the [[HoTT book real number]], one has $N(z)=z\overline{z}$, where the right-hand side is identified with a real number embedded in $\mathbb{C}_H$.

If $z \# 0_{\mathbb{C}_H}$, then $N(z) \gt 0$. Hence $N(z)$ is multiplicatively invertible in $\mathbb{R}_H$, and the inverse of $z$ is given by

$$
z^{-1} \coloneqq \left(\frac{a}{a^2+b^2},-\frac{b}{a^2+b^2}\right).
$$

This construction satisfies $zz^{-1}=z^{-1}z=1_{\mathbb{C}_H}$.

Conversely, every multiplicatively invertible element of $\mathbb{C}_H$ is apart from zero. Thus, the multiplicatively invertible elements may be characterized by their apartness from zero.

### Multiplicative group of units ###

The [[group of units]] of $\mathbb{C}_H$ consists of its multiplicatively invertible elements. We denote it by $\mathbb{C}_H^\times$.

Equivalently, using the apartness characterization above, its underlying [[type]] may be written as

$$
\mathbb{C}_H^\times \coloneqq \sum_{z:\mathbb{C}_H}(z \# 0_{\mathbb{C}_H}).
$$

The group operation is inherited from complex multiplication, with [[identity element]] $1_{\mathbb{C}_H}$ and inverses as defined above.

Since $\mathbb{C}_H$ is a [[set]] and apartness is [[proposition]]-valued, $\mathbb{C}_H^\times$ is also a set. Hence it defines an ordinary [[group]] in [[homotopy type theory]].

In the following discussion, $\mathbb{C}_H^\times$ is regarded as a [[discrete group]], without imposing any additional topological or continuity structure on its multiplication.

### Delooping ###

For a [[group]] $G$ whose underlying type is a set, a [[delooping]] $BG$ is a [[pointed connected type|pointed connected]] [[1-type]] whose [[loop space]] recovers $G$ as a group.

In particular, the multiplicative group $\mathbb{C}_H^\times$ admits a delooping $B\mathbb{C}_H^\times$, satisfying

$$
\Omega(B\mathbb{C}_H^\times,\mathrm{base}) \simeq \mathbb{C}_H^\times.
$$

One construction of this delooping uses the moduli type of $G$-[[torsor]]s, with the regular torsor as the distinguished [[base point]].

Thus, $B\mathbb{C}_H^\times$ may be represented by the moduli type of $\mathbb{C}_H^\times$-torsors.

Its nontrivial loop structure arises from the multiplicative group, rather than from any nontrivial higher homotopy of the underlying complex number type.

### Group actions and monodromy ###

The multiplicative group $\mathbb{C}_H^\times$ acts on the [[additive group]] $(\mathbb{C}_H,+)$ by scalar multiplication:

$$
\rho:\mathbb{C}_H^\times \longrightarrow \mathrm{Aut}(\mathbb{C}_H,+), \qquad \rho(\lambda)(z):=\lambda z.
$$

Since each $\lambda\in\mathbb{C}_H^\times$ is invertible, $\rho(\lambda)$ is an additive group [[automorphism]].

By the correspondence between [[group action]]s and [[dependent type]] families over their deloopings, this action determines a dependent family of sets

$$
P:B\mathbb{C}_H^\times \longrightarrow \mathcal{U},
$$

whose [[fiber]] over the base point is equivalent to $\mathbb{C}_H$.

[[transport]] along the [[loop]] corresponding to $\lambda\in\mathbb{C}_H^\times$ recovers multiplication by $\lambda$, up to the chosen identifications and conventions for group actions and path composition.

This gives a homotopy-theoretic interpretation of complex scalar multiplication in terms of [[transport]] and [[monodromy]].


## Formalization ##

### Constructive Complex Algebra and Computational Delooping in Cubical Agda ###

The formalization of the [[HoTT book complex number]] and its multiplicative [[delooping]] is an ongoing research project at the [[Center for Quantum and Topological Systems]] (CQTS).

The project develops the constructive algebraic structure of $\mathbb{C}_H$ in [[Cubical Agda]], based on the [[HoTT book real number]], with the aim of obtaining a reusable formalization of the [[discrete group]] $\mathbb{C}_H^\times$ and its delooping $B\mathbb{C}_H^\times$.

The mathematical development involves the following constructions:

- The complex number type and its [[commutative ring]] structure over the HoTT book reals.
- Constructive [[apartness]], multiplicative invertibility, and the [[group of units]] $\mathbb{C}_H^\times$.
- The delooping $B\mathbb{C}_H^\times$ through [[torsor]]s.
- The multiplicative [[group action]] of $\mathbb{C}_H^\times$ on $\mathbb{C}_H$ and the corresponding [[dependent type]] family.
- The relation between [[transport]], [[monodromy]], and complex-valued twisting data.

These constructions are intended to be accompanied by machine-checked definitions and [[formal proof]]s, together with mathematical explanations of their correspondence to the formal code.

The formalization is work in progress. The definitions and mathematical properties described above should not be interpreted as claims that their complete Cubical Agda implementations have already been verified.

### Motivation ###

The motivation is to connect constructive number systems in [[homotopy type theory]] with the computational interpretation of topological transformations through [[dependent type]]s.

Although the underlying complex number type is simply a [[product type]] of two real number types, constructing its multiplicative group in a fully constructive setting requires careful treatment of [[apartness]] and invertibility.

The resulting [[group]] $\mathbb{C}_H^\times$ provides a concrete instance of the general correspondence between groups, their [[delooping]]s, and [[monodromy]] actions on dependent [[fiber]]s.

The computational question is whether these abstract correspondences can be realized through explicit operations in [[Cubical Agda]], such that [[transport]] along [[loop]]s recovers the intended complex multiplication and admits meaningful computational behavior.

This is distinct from merely establishing the existence of the corresponding [[equivalence]]s and [[group action]]s.

### Relation to topological quantum gates ###

In the homotopy-theoretic formulation of [[topological quantum computation]], complex coefficients and multiplicative twisting play a central role in the construction of [[local system]]s and [[twisted cohomology]].

In particular, the homotopy-theoretic description of [[topological quantum gate|topological quantum gates]] by [MySS 2024](#MySS24) involves twisting data valued in the delooping of the discrete multiplicative group of nonzero complex numbers.

Such twisting data may be expressed by a map of the form

$$
  \tau:X\longrightarrow B\mathbb{C}_H^\times.
$$

The associated complex-valued [[dependent type]] family provides a setting in which [[transport]] along [[path]]s in $X$ induces [[monodromy]] on the corresponding [[fiber]]s.

For the topological quantum gate construction, the relevant spaces include [[classifying space]]s associated with [[braid group]]s, while the twisting data enter the definition of complex-valued [[twisted cohomology]].

The formalization of $\mathbb{C}_H^\times$ and its delooping is therefore a foundational component of a broader programme aimed at the computational realization of topological quantum transformations in [[Cubical Agda]].

A complete computational realization of the quantum gate construction requires further formalization beyond the complex number system and its delooping.

## See also ##

- [[HoTT book real number]]
- [[complex number]]
- [[constructive mathematics]]
- [[apartness]]
- [[group of units]]
- [[delooping]]
- [[torsor]]
- [[monodromy]]
- [[homotopy type theory]]
- [[Cubical Agda]]
- [[topological quantum computation]]
- [[Center for Quantum and Topological Systems]]


## References ##

* {#ConstructiveComplexDelooping} [[nLab materials]]: *Constructive Complex Units and Their Torsor Delooping in Cubical Agda* (2026-11-23) &lbrack;<a href="https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/main/papers/ConstructiveComplexDelooping/main.pdf">main.pdf</a>, <a href="https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/tree/main/src/ConstructiveComplex">agda</a>, <a href="https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda">GitHub</a>&rbrack;
  > (constructive complex commutative ring, multiplicative units group and torsor delooping; Cubical Agda type-checked)



* {#UFP13} [[Univalent Foundations Project]], Section 11.3 of: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* Jackson Brough, *Formalizing the Real Numbers in Homotopy Type Theory with Cubical Agda*, 2026. [arXiv:2604.24782](https://arxiv.org/abs/2604.24782).

* {#MySS24} [[David Jaz Myers]], [[Hisham Sati]] [[Urs Schreiber]]: : *[[schreiber:Topological Quantum Gates in Homotopy Type Theory]]*, Comm. Math. Phys. **405** 172 (2024) &lbrack;[doi:10.1007/s00220-024-05020-8](https://doi.org/10.1007/s00220-024-05020-8), [arXiv:2303.02382](https://arxiv.org/abs/2303.02382)&rbrack;

