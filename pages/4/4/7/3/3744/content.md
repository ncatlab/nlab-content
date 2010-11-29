
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea
This page lays down a specific set of axioms of the [[Haag-Kastler axioms]] to [[AQFT]], knowing that this set is not _the set_ of Haag-Kastler axioms, but one specific choice. The purpose is to state and prove some of the classical results of the theory in a mathematically precise and model independent way. In fact some experts will find the chosen axioms to be stronger than necessary, this is deliberately so to ease the exposition.

It is possible to construct examples that fulfill the axioms, to show that they are not empty, but we will not engage in this task here, at least not now. Note however that up to now there was no success in the task to construct systems in 4 dimensions with interactions, which has led to some doubts about the usefulness of this approach in the physics community: It has yet to be shown if the approach does or does not capture the essential features that makes possible the tremendous success of the standard model of particle physics.

## Abstract
We first collect some terms that are needed to then formulate the axioms of the vacuum representation. A few simple consequences are cited and some links to further concepts are provided.

###Notation

####The Poincar&#233; Group
The universal covering $SL(2, \C) \ltimes \R^4$ of the restricted Poincar&#233; group $\mathcal{P}^{\dagger}_+$ will be denoted by $\mathcal{P}$, the abelian subgroup of all translations by $\mathcal{T}$.

####The Minkowski Spacetime
We talk about 4-dimensional Minkowski spacetime $\mathcal{Min}$ only, i.e. $\mathcal{Min}$ is the vector space $\R^{4} = \R \times \R^{3}$ equipped with the scalar product $\lt x, y \gt := x_0 y_0 - (\vec x, \vec y)$ with $( \cdot , \cdot  )$ being the Euclidean scalar product on $\R^{3}$.
Open bounded subsets of $\mathcal{Min}$ will be denoted by $\mathcal{O}$. The union of these $\mathcal{O}$ form an index set $\mathcal{J}$, that is partially ordered by inclusion. 

If two sets are spacelike separated, this will be denoted by $\mathcal{O}_1 \perp \mathcal{O}_2$, the interior of the spacelike complement of a given set $\mathcal{O}$ will be denoted by $\mathcal{O}'$ or $\mathcal{O}^{\perp}$. The bounded open sets thus form a [[causal index set]].

We denote the open forward (light)cone at x by $V_+(x)$, similar $V_-(x)$ is the open backward cone at $x$, if $x=0$ we simply write $V_+$ and $V_-$.
A **double cone** or **diamond** is an intersection of an open forward cone and an open backward cone that is nonempty and will be denoted by $\mathcal{K}$. 

An important class of unbounded regions are the **wedges**: Choose an inertial frame and define the right wedge as
$$
       W_R := \{ x = (t, x_1, x_2, x_3) \in \mathbb{R}^4 \mid x_1 \gt \shortmid t \shortmid \}
$$
The set of wedges is then defined to be
$$
      \mathcal{W} := \{\lambda W_R \mid \lambda \in \mathcal{P}^{\dagger}_+ \}
$$
While the definition of the right wedge depends on the chosen initial frame, the definition of the set of wedges does not.

####Operator Algebras
See [[operator algebra]] and [[von Neumann algebra]] here on the nLab.

Von Neumann algebras $\mathcal{M}$ will always be concrete operator algebras acting on a given Hilbert space $\mathcal{H}$, as is the rule in the literature (see also [[von Neumann algebra]]). The commutant of $\mathcal{M}$ will be denoted by $\mathcal{M}'$, the positive cone by $\mathcal{M}^+$. The minimal von Neumann algebra that contains two given ones $\mathcal{M}_1$ and $\mathcal{M}_2$ will be denoted by:
$$
      \mathcal{M}_1 \vee \mathcal{M}_2 :=  {(\mathcal{M}_1 \cup \mathcal{M}_2)}''
$$
As in this formula we will make frequently use of the [bicommutant theorem] (http://en.wikipedia.org/wiki/Von_Neumann_bicommutant_theorem) to denote by $\mathcal{M}''$ the weak resp. strong closure resp. the generated von Neumann algebra of a give set of bounded operators.

An automorphismus of an algebra $\alpha \mathcal{M} \rightarrow \mathcal{M}$ is called an **inner** automorphismus if there is an invertible element $u \in \mathcal{M}$ such that $\alpha$ is given by conjugation with $u: \alpha(m) = u \quad m \quad u^{-1} \qquad \forall m\in \mathcal{M}$ (note that our convention here differs from that used by [Wikipedia] (http://en.wikipedia.org/wiki/Inner_automorphism)).

####Group Representations
In this paragraph we will collect some links and remarks about unitary representations of topological groups on Hilbert spaces that are relevant to our topic and less commonly used in the literature.
In the following $\mathcal{G}$ will be a topological group, $\mathcal{H}$ a (complex) Hilbert space and $\mathcal{U}$ an unitary representation of $\mathcal{G}$ in the algebra of bounded operators of $\mathcal{H}$.

Definition (**analytical vector**): Let $\mathcal{G}$ be a n-dimensional real Lie group. Fix a $f \in \mathcal{H}$, a neighbourhood B of 0 in $\R^n$ and a parametrization $\phi: B \to \mathcal{G}$ of a neighbourhood of 1 in $\mathcal{G}$. Then we can define a function $\mathcal{U}_f$ by
$$
      \mathcal{U}_f: B \to \mathcal{H}
$$
$$
                     x \mapsto \mathcal{U}(\phi(x)) f    
$$
If $\mathcal{U}_f$ has an extension to an analytic function on a neighbourhood of 0 in $\C^n$, the vector $f$ is called an analytic vector (for $\mathcal{U}$).

See [planetmath] (http://planetmath.org/encyclopedia/BanachSpaceValuedAnalyticFunctions.html) for the definition of Banach space valued analytic functions.

###Definition of Vacuum Representations
A net of von Neumann algebras $\mathcal{M}(\mathcal{O})$ on a common Hilbert space $(\mathcal{H})$, indexed by $\mathcal{O} \in \mathcal{J}$, is called a **vacuum respresentation** (on the 4-dimensional Minkowski spacetime) if it satisfies the following axioms:

+-- {: .num_theorem #isotony}
* (V1) **isotony**: $\mathcal{O}_1 \subset \mathcal{O}_2$ implies $\mathcal{M}(\mathcal{O}_1) \subseteq \mathcal{M}(\mathcal{O}_2)$
=--

+-- {: .num_theorem #additivity}
* (V2) **additivity**: $\mathcal{O} = \bigcup_j \mathcal{O}_j$  implies   $\mathcal{M}(\mathcal{O}) = ( \bigcup_j \mathcal{M}(\mathcal{O}_j) )'' $ 
=--

+-- {: .num_theorem #locality}
* (V3) **locality**, see [[local net]]: $\mathcal{O}_1 \perp \mathcal{O}_2 implies \mathcal{M}(\mathcal{O}_1) \subseteq  (\mathcal{M}(\mathcal{O}_2))' $
=--

+-- {: .num_theorem #covariance}
* (V4) **covariance**: There is a strongly continuous unitary representation $\mathcal{U}(\mathcal{P})$ of $\mathcal{P}$ such that for each $g \in \mathcal{P}$ the following holds: $\mathcal{M}(g\mathcal{O}) = \mathcal{U}(g) \mathcal{M}(\mathcal{O}) \mathcal{U}(g)^{-1}$
=--

+-- {: .num_theorem #spectrum_condition}
* (V5) **spectrum condition**: $spec\mathcal{U}(\mathcal{T}) \subseteq clo \mathcal{V}_+$
=--

_Remark_ (mathematical viewpoint): $\mathcal{T}$ is the abelian subgroup of translations, and $\mathcal{V}_+$ is the (open) forward cone at 0, see above. For the definiton of the spectrum of the representation $\mathcal{U}(\mathcal{T})$ see [[spectral measure]].

+-- {: .num_theorem #existence_of_vacuum_vector}
* (V6) **existence of a vacuum vector**: There exists a vector $\Omega \in \mathcal{H}, \|\Omega\| = 1$, such that $\bigl( \bigcup_{\mathcal{O}\in\mathcal{J}}\mathcal{M}(\mathcal{O}) \bigr) \Omega$ is dense in $\mathcal{H}$ and $\mathcal{U}(g)\Omega = \Omega$ for all $g \in \mathcal{P}$
=--

+-- {: .un_remark}
###### Remark
**(choice of axioms)** The _uniqueness_ is sometimes part of the axioms, but not here. Instead we will cite theorems that will specify necessary and sufficient conditions to ensure that there is a _unique_ vacuum vector. 

=--

###Additional Notations and Notions of Vacuum Representations
A short hand notation for vacuum representations will be $\mathcal{M}(\mathcal{J})$ in the following.

The algebras $\mathcal{M}(\mathcal{O})$ are sometimes called **local algebras**.

The $C^*-$algebra $\mathcal{A} := clo_{\| \cdot \|} \bigl( \bigcup_{\mathcal{O}\in\mathcal{J}}\mathcal{M}(\mathcal{O}) \bigr) $ is called **quasilocal algebra**, the smallest von Neuman algebra that contains $\mathcal{A}$ is called the **global algebra** and denoted by $\mathcal{R}$. 

A vacuum representation is called **irreducible** if $\mathcal{R} = \mathcal{L}(\mathcal{H})$ (the global algebra is the whole algebra of all bounded linear operators on the given Hilbert space), it is called **factorial** if $\mathcal{R}$ is a factor.

* Wikipedia on [factors] (http://en.wikipedia.org/wiki/Von_Neumann_algebra#Factors) of von Neumann algebras.

The subspace of $\mathcal{H}$ that is invariant under the action of the translation group $\mathcal{T}$ is not trivial due to the axiom \ref{existence_of_vacuum_vector}. If it is one-dimensional, we will say that the vacuum representation has a **unique vacuum vector** (the space is then necessarily the subspace $\C\Omega$).

### first consequences and the Reeh-Schlieder theorem

* **Definition (algebras of unbounded open set)**
To any unbounded open set $\mathcal{U}$ we associate a von Neumann algebra by
$$
           \mathcal{M}(U) := \bigl( \bigcup_{\mathcal{O} \subset \mathcal{U}} \mathcal{M}(\mathcal{O}) \bigr)''
$$

* **Theorem (weak additivity)**
Let $\mathcal{O} \in \mathcal{J}$ be arbitrary, then we have
$$
         \bigl( \bigcup_{a \in \mathcal{T}} \mathcal{M}(a \mathcal{O}) \bigr)'' = \mathcal{R}
$$

_Remark_ (choice of axioms): Weak additivity of our nets are a direct consequence of our axioms, but this is often enough not so in the literature: Depending on the choice of axioms, it is either stated as an axiom or an auxiliary property of a net that is called for when needed.

_Proof_: Let $\mathcal{O}_0$ be given (arbitrary but fixed).
Let us first note that thanks to isotony and additivity we can restrict the index set of the union in the definition of $\mathcal{R}$ from open bounded sets to diamonds, since every bounded set is contained in a diamond:
$$
\bigl( \bigcup_{\mathcal{O} \in \mathcal{J}} \mathcal{M}(\mathcal{O}) \bigr)'' = \bigl( \bigcup_{\mathcal{K}} \mathcal{M}(\mathcal{K}) \bigr)'' = \mathcal{R}
$$
Given an arbitrary diamond $\mathcal{K}$ we have $\mathcal{K} \subset \bigl( \bigcup_{a \in \mathcal{K}}(\mathcal{O}_0 + a) \bigr)$ while the latter is a bounded open subset $\in \mathcal{J}$. This means that we arrive at
$$
\bigcup_{\mathcal{K}} \mathcal{M}(\mathcal{K}) = \bigcup_{a\mathcal{O}_0, a \in {\mathcal{T}}} \mathcal{M}(a\mathcal{O}_0)
$$
which implies that the generated von Neumann algebras coincide, too, of course.

* **Theorem (Borchers, translations are inner)**: The representatives of the translations are elements of the global algebra $\mathcal{R}$, i.e. they are inner automorphisms of $\mathcal{R}$: $\mathcal{U}(\mathcal{T}) \subseteq \mathcal{R}$.

* **Theorem (uniqueness of vacuum)**: Every factorial vacuum representation is irreducible. A vacuum representation is irreducible iff it has an unique vacuum vector.

* **[[Reeh-Schlieder Theorem]]**: The vacuum vector is cyclic and separating for all local algebras.

Let $x, y \in \R^4$ and define $[x, y] := \{\lambda x + \mu y | \lambda, \mu \geqq 0, \lambda + \mu = 1\} $.
Define

$$
           \mathcal{M}[x, y] := \cap_{[x, y] \subset \mathcal{O}} \mathcal{M}(\mathcal{O})
$$

+-- {: .un_theorem}
###### Theorem
**triviality of algebras of spacelike segments**

If the segment $[x, x + b]$ is spacelike, i.e. $\langle b, b \rangle \lt 0$, and the vacuum respresentation has a unique vacuum vector, then $\mathcal{M}[x, x + b] = \mathbb{C} \mathbb{1}$, i.e. the algebra associated with the segment is trivial.
=--

+-- {: .un_theorem}
###### Theorem
**triviality of algebras of points**
The conclusion of the preceding statement holds if we put $b = 0$, i.e. if we consider the algebra associated with one point.
=--

_Remark_ (physical viewpoint): The preceding theorem is sometimes summarized as _there are no non-trivial observables at the point_. There are two possible ways to interpret this result: The pragmatic approach says that, since no detector can be built that measures observables precisley at one point of spacetime, there is no need of a theory to support the concept of observables localized at a point. The philosophical approach takes this one step further and states that our relativistic quantum theory tells us that the concepts of points and observables localized at points are an idealization with no relevance to nature.

The local algebras fulfill the [[Borchers property]].

There are several directions one can pursue next, for example 

* the [[classification of local algebras]] or

* [[superselection theory]]

## References
This page is based upon:

* Hellmut Baumg&#228;rtel: Operator algebraic Methods in Quantum Field Theory. A series of lectures. Akademie Verlag 1995 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0839.46063&format=complete))

A secondary reference is this:

* Hellmut Baumg&#228;rtel, Manfred Wollenberg: Causal nets of operator algebras, Berlin: Akademie Verlag 1992 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0749.46038&format=complete))