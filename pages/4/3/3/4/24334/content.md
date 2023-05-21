
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Directed Type Theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

*Simplicial type theory* ([Riehl & Shulman 2017, §3](#RiehlShulman17)) is a [[homotopy type theory]] which introduces additional non-fibrant layers on top of [[Martin-Löf type theory]] to provide a logical calculus for a [[directed homotopy theory|directed]] [[interval type]] and with it for [[geometric shape for higher structures|geometric shapes]], consisting of [[Segal space]]-types, [[Rezk completion|Rezk complete]]-types, and covariant fibrations. 

## Formal presentations

There are many different ways to formalize the directed interval primitive in simplicial type theory: 

* one could simply postulate via inference rules and axioms a directed interval primitive in a separate layer. 

* one could use [[two-level type theory]] consisting of a non-fibrant layer, and then axiomatise a directed interval primitive in the non-fibrant layer 

* one could use [[type theory with shapes]] consisting of a non-fibrant layer of cubes which is a [[simple type theory]] and a non-fibrant layer of topes which is a [[propositional logic]] over the cube layer, and then define the directed interval primitive using the cube and tope layers

### Two-level type theory

We use $\Xi$ to represent the context in the non-fibrant layer, and $\Gamma$ to represent the context in the fibrant layer. Type judgments in the non-fibrant layer are represented by $A \; \mathrm{exotype}$, while type judgments in the fibrant layer are just represented by $A \; \mathrm{type}$. 

#### Directed interval primitive

The directed interval primitive $\mathbb{2}$ in simplicial type theory is a non-trivial bounded [[total order]]. Bounded total orders have many definitions in mathematics, such as a bounded [[partial order]] satisfying totality, or a [[lattice]] satisfying totality. As such, there are multiple possible sets of inference rules one could use to present the directed interval in the two-level type theory formalization. 

The inference rules for the directed interval primitive $(\mathbb{2}, \leq)$ as a [[partial order]] in the two-level type theory formalization are as follows:

$$\frac{\Xi \; \mathrm{ctx}}{\Xi \vdash \mathbb{2} \; \mathrm{exotype}} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi \vdash 0:\mathbb{2}} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi \vdash 1:\mathbb{2}} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash x \leq y \; \mathrm{exotype}} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash \tau_\leq(x, y):\mathrm{isProp}(x \leq y)}$$

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2} \vdash \mathrm{refl}_\leq(x):x \leq x} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2}, z:\mathbb{2}, p:x \leq y, q:y \leq z \vdash \mathrm{trans}_\leq(x, y, z, p, q):(x \leq z)}$$

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash \mathrm{antisym}_\leq(x, y):\mathrm{isEquiv}(idtoleqgeq(x, y))} \quad \mathrm{where} \quad 
\begin{array}{l}
idtoleqgeq(x, y):(x =_\mathbb{2} y) \to (x \leq y) \times (y \leq x) \\
idtoleqgeq(x, x)(\mathrm{id}_\mathbb{2}(x)) \coloneqq (\mathrm{refl}_\leq(x), \mathrm{refl}_\leq(x))
\end{array}
$$

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash \mathrm{totl}_\leq(x, y):[(x \leq y) + (y \leq x)]} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2} \vdash \mathrm{bot}_\leq(x):0 \leq x} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2} \vdash \mathrm{top}_\leq(x):x \leq 1}$$

$$\frac{\Xi \; \mathrm{ctx}}{\Xi \vdash \mathrm{nontriv}_\leq:(0 =_\mathbb{2} 1) \to \mathbb{0}}$$

The inference rules for the directed interval primitive $\mathbb{2}$ as a [[lattice]] in the two-level type theory formalization are as follows:

$$\frac{\Xi \; \mathrm{ctx}}{\Xi \vdash \mathbb{2} \; \mathrm{exotype}} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi \vdash \tau_0:\mathrm{isSet}(\mathbb{2})} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi \vdash 0:\mathbb{2}} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi \vdash 1:\mathbb{2}} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash x \wedge y:\mathbb{2}} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash x \vee y:\mathbb{2}}$$

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2} \vdash \mathrm{idem}_\wedge(x):x \wedge x =_{\mathbb{2}} x} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash \mathrm{comm}_\wedge(x, y):x \wedge y =_{\mathbb{2}} y \wedge x}$$ 

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2}, z:\mathbb{2} \vdash \mathrm{assoc}_\wedge(x, y, z):(x \wedge y) \wedge z =_{\mathbb{2}} x \wedge (y \wedge z)}$$

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2} \vdash \mathrm{lunit}_\wedge(x):1 \wedge x =_{\mathbb{2}} x} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2} \vdash \mathrm{runit}_\wedge(x):x \wedge 1 =_{\mathbb{2}} x}$$ 

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2} \vdash \mathrm{idem}_\vee(x):x \vee x =_{\mathbb{2}} x} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash \mathrm{comm}_\vee(x, y):x \vee y =_{\mathbb{2}} y \vee x}$$ 

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2}, z:\mathbb{2} \vdash \mathrm{assoc}_\vee(x, y, z):(x \vee y) \vee z =_{\mathbb{2}} x \vee (y \vee z)}$$

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2} \vdash \mathrm{lunit}_\vee(x):0 \vee x =_{\mathbb{2}} x} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2} \vdash \mathrm{runit}_\vee(x):x \vee 0 =_{\mathbb{2}} x}$$ 

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash \mathrm{asorp}_\wedge(x, y):x \wedge (x \vee y) =_{\mathbb{2}} x} \qquad \frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash \mathrm{asorp}_\vee(x, y):x \vee (x \wedge y) =_{\mathbb{2}} x}$$ 

$$\frac{\Xi \; \mathrm{ctx}}{\Xi, x:\mathbb{2}, y:\mathbb{2} \vdash \mathrm{totl}(x, y):[(x \wedge y =_{\mathbb{2}} x) + (x \wedge y =_{\mathbb{2}} y)]} \quad \frac{\Xi \; \mathrm{ctx}}{\Xi \vdash \mathrm{nontriv}_\leq:(0 =_\mathbb{2} 1) \to \mathbb{0}}$$

#### Simplicies and subshapes

We inductively define the $n$-simplices as the following family of non-fibrant types:

* The $0$-simplex is the unit type in the non-fibrant layer
$$\Delta^0 \coloneqq \mathbf{1}$$

* In the non-fibrant layer, let $\mathrm{Fin}(n) \coloneqq \sum_{i:\mathbb{N}} i \lt n$ be the canonical [[finite type]] with $n$ elements. The $n+1$-simplex is defined as the type
$$n:\mathbb{N} \vdash \Delta^{n + 1} \coloneqq \sum_{t:\mathrm{Fin}(n + 1) \to \mathbb{2}} \prod_{i:\mathrm{Fin}(n)} t(\pi_1(i + 1)) \leq t(\pi_1(i))$$

The first few simplicies can be explicitly written as 

$$\Delta^1 \coloneqq \mathbb{2}$$
$$\Delta^2 \coloneqq \sum_{t:\mathrm{Fin}(2) \to \mathbb{2}} t(1) \leq t(0)$$
$$\Delta^3 \coloneqq \sum_{t:\mathrm{Fin}(3) \to \mathbb{2}} (t(2) \leq t(1)) \times (t(1) \leq t(0))$$

Subshapes of the simplicies could also be defined. 

* The boundary of the $1$-simplex is defined as
$$\partial \Delta^1 \coloneqq \sum_{t:\Delta^1} [(t =_{\Delta^1} 0) + (t =_{\mathbb{2}} 1)]$$

* The boundary of the $2$-simplex is defined as
$$\partial \Delta^2 \coloneqq \sum_{t:\mathrm{Fin}(2) \to \mathbb{2}} [(t(0) =_{\mathbb{2}} 0) \times (t(0) \leq t(1)) + (t(0) =_{\mathbb{2}} t(1)) + (t(0) \leq t(1)) \times (t(1) =_{\mathbb{2}} 1)]$$

### Type theory with shapes

...

## See also

* [[Reedy model structure]]

* [[bisimplicial set]]

* [[synthetic (infinity,1)-category theory|synthetic $(\infty,1)$-category theory]]

* [[type theory with shapes]]

* [[two-level type theory]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Mike Shulman]], *A type theory for synthetic ∞-categories*, Higher Structures **1** 1 (2017) &lbrack;[arxiv:1705.07442](https://arxiv.org/abs/1705.07442), [published article](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/RiehlShulman)&rbrack;


* [[Jonathan Weinberger]], *A Synthetic Perspective on $(\infty,1)$-Category Theory: Fibrational and Semantic Aspects* $[$[arXiv:2202.13132](https://arxiv.org/abs/2202.13132)$]$

* [[Jonathan Weinberger]], *Strict stability of extension types* $[$[arXiv:2203.07194](https://arxiv.org/abs/2203.07194)$]$

A talk on [[synthetic (infinity,1)-category theory]] in [[simplicial type theory]] and [[infinity-cosmos]] theory:

* [[Emily Riehl]], *The synthetic theory of infinity-categories vs the synthetic theory of infinity-categories*, [[Homotopy Type Theory Electronic Seminar Talks]], 1 March 2018, ([video](https://www.youtube.com/watch?v=ge-9m1SsEmc), [slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Riehl-2018-03-01-HoTTEST.pdf))

A [[proof assistant]] implementing simplicial type theory: 

* [rzk](https://github.com/fizruk/rzk)

[[!redirects simplicial homotopy type theory]]