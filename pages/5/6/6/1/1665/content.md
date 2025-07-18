
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _Kan lift_ in a [[2-category]] or in a [[bicategory]] is [[duality|dual]] to the notion of [[Kan extension]], by a process of turning the 1-cells around, much in the same way as a [[homotopy lifting property]] is dual to a [[homotopy extension property]] (in [[model category|model category theory]], for instance). 

Informally, a Kan lift is a best approximate solution to the problem of finding a lift $\widetilde{f}: A \to B$ of an arrow ([[morphism]]) $f: A \to C$ through an arrow $p: B \to C$, as in the [[diagram]]

\begin{tikzcd}
	& B \\
	A & C
	\arrow["p", from=1-2, to=2-2]
	\arrow["{\mathrm{Rift}_p f}", dashed, from=2-1, to=1-2]
	\arrow["f"', from=2-1, to=2-2]
\end{tikzcd}

Of course, lifts typically don't literally exist in the sense of an equation $p \circ \widetilde{f} = f$ or an [[isomorphism]] $p \circ \widetilde{f} \cong f$. But in good situations, one may have the next best thing: a [[2-morphism|2-cell]] $p \circ \widetilde{f} \Rightarrow f$ which is universal among 2-cells of this form. This gives the notion of _right_ Kan lift. The notion of _left_ Kan lift is similar, but with 2-cells in the opposite direction. 

### Terminology ###

Usually, when working within a 2-categorical context, Kan lifts are simply refered to as _lifts/liftings_, just as what happens with [[Kan extension|Kan extensions]].

## Definition ## 

As in the discussion at [[Kan extension]], there is a local notion of Kan lift and a global notion. Expanding on the informal description above, we give the local notion first, followed by the (conceptually more perspicuous) global notion in terms of [[adjoint functor]]s. 

### Local description ###

Given 1-cells $p: B \to C$, $f: A \to C$ in a [[bicategory]], a **right Kan lift** of $f$ through $p$, denoted $Rift_p f$, is a 1-cell $\widetilde{f}: A \to B$ equipped with a 2-cell 

$$\varepsilon: p \circ \widetilde{f} \Rightarrow f$$ 

satisfying the [[universal property]]: given any pair $(g: A \to B, \eta: p \circ g \Rightarrow f)$, there exists a unique 2-cell 

$$\zeta: g \Rightarrow \widetilde{f}$$ 

such that $\varepsilon \bullet (p \circ \zeta) = \eta$. (Here $\circ$ refers to composition across a 0-cell, and $\bullet$ to composition across a 1-cell.) As with any universal description, the pair $(Rift_p f, \varepsilon)$ is unique up to unique 2-cell isomorphism. 

A **left Kan lift** of $f$ through $p$, denoted $Lift_p f$, is a 1-cell $\widetilde{f}: A \to B$ equipped with a 2-cell 

$$\eta: f \Rightarrow p \circ \widetilde{f}$$ 

such that given any pair $(g: A \to B, \theta: f \Rightarrow p \circ g)$, there exists a unique 2-cell 

$$\zeta: \widetilde{f} \Rightarrow g$$ 

such that $(p \circ \zeta) \bullet \eta = \theta$. 

### Global description ### 

Given $p: B \to C$ and a 0-cell $A$ in a bicategory, if the right Kan lift $Rift_p f$ exists for any $f: A \to C$, then we speak of a **global** Kan lift. When this is the case, we may define a functor between hom-categories 

$$Rift_p: [A, C] \to [A, B]$$ 

which at the object level is of course $f \mapsto Rift_p f$. At the morphism level, given a 2-cell 

$$\eta: f \Rightarrow g: A \to C$$ 

there is an induced 2-cell $Rift_p f \Rightarrow Rift_p g$, the one which corresponds (by the universal property of $Rift_p g$) to the composite 

$$p \circ Rift_p f \overset{\varepsilon}{\Rightarrow} f \overset{\eta}{\Rightarrow} g.$$ 

A standard universality argument shows that $Rift_p$ thus defined is functorial. 

**Proposition:** $Rift_p$ is right adjoint to the functor 
$[A, p]: [A, B] \to [A, C]$ obtained by postcomposing with $p$, i.e., the functor $f \mapsto p \circ f$. 

This is the easier, more conceptual way to remember right Kan lifts: in a global sense, they are right adjoint to postcomposition. Similarly, global left Kan lifts are left adjoint to postcomposition. 

* In a [post](http://golem.ph.utexas.edu/category/2009/06/kan_lifts.html) at the nCaf&#233;, [[David Corfield]] put the question: why are Kan extensions more frequently mentioned than Kan lifts? One proposed [answer](http://golem.ph.utexas.edu/category/2009/06/kan_lifts.html#c024705) is that in many cases a left or right Kan lift will exist for a trivial reason: namely that $p$ itself has a left or right adjoint. Other examples will be given below.

## Properties ##

Dual to the situation in Kan extensions, one is interested in whether a Kan lift is _respected_ by a 1-cell with codomain the domain of the lift. This is defined as follows:

- given $(\widetilde{f}, \varepsilon) = \mathop{Rift}_p f$, $g$ is said to _respect_ this right lift if $(\widetilde{f}g, \varepsilon \bullet g) = \mathop{Rift}_p(f g)$

and analogously for left Kan lifts. A Kan lift $\widehat{f}$ is _absolute_ if it is respected by any 1-cell into $\mathop{dom}(\widehat{f})$. Absolute Kan lifts subsume adjunctions and relative adjunctions, and are prominently present in the axioms of a [[Yoneda structure]]; for more see the examples below.

## Examples ## 

* Let $Mod$ denote the [[framed bicategory]] of small categories $C$, bimodules $r: C \to D$ (i.e., functors $r: D^{op} \times C \to Set$), and transformations between such bimodules. Then global right Kan lifts exist (as do global right Kan extensions). These may be computed as [[weighted limit]]s or via [[end]] formulas, e.g., 
$$(Rift_r s)(b, c) = \int_{d: D} hom(r(d, c), s(d, b))$$

Examples of this construction abound in mathematics, especially when generalized to the [[enriched category theory]] context. For example, in the bicategory $Rel$, which corresponds to enrichment in $\mathbf{2}$, the right Kan lift is essentially a universally quantified predicate of the form 

$$\forall_{d: D} r(d, c) \Rightarrow s(d, b)$$ 

("for all $d$ satisfying condition $r$, we impose condition $s$"). 

* More generally, a [[biclosed bicategory]] is precisely a bicategory where global right Kan extensions and right Kan lifts exist for every 1-cell $p$. Monoidal bicategories provide instances of this. 

* adjunctions in a 2-category can be defined in terms of Kan lifts: a 1-cell $u\colon A \to B$ has a left adjoint iff $\mathop{Lift}_u 1_B$ exists and is absolute; in this case putting $(f,\iota) = \mathop{Lift}_u 1_B$ we have $f \dashv u$ with unit $\iota \colon 1_B \Rightarrow u f$. The universal property of the left Kan lift plus absoluteness are enough to construct the counit and to verify the triangular equations. There's of course a dual definition in terms of absolute right Kan lifts.

* relative adjoints in $\mathbf{Cat}$ can also be expressed as absolute kan lifts; see [[relative adjoint]] for a precise statement.

* representably fully faithful 1-cells, meaning those for which $B(X,f)$ is fully faithful in $\mathbf{Cat}$ for every object $X\colon B$, are those for which $(1_A, 1_f) = \mathop{Lift}_f f$, and this lifting is absolute.

* In $Cat$, if $A$ is small and $B$ is locally small, and if $F: A \to B$ is a functor, then we have a Yoneda embedding $y: A \to P A = Set^{A^{op}}$ and a functor $B(F-, -): B \to P A$, and there is a canonical map 
$$y_A \to B(F-, -) \circ f$$ 
(essentially, $hom(a, b) \to hom(F a, F b)$ taking $f: a \to b$ to $F f: F a \to F b$). This arrow exhibits $F$ as a left Kan lift of $y$ through $B(F-, -)$, which is moreover absolute. This example is important in the theory of [[Yoneda structure|Yoneda structures]], due to Street and Walters; see Mark Weber's updated [development](http://www.pps.jussieu.fr/~weber/Two-toposes4.pdf) in the context of 2-topos theory.

## References

Kan lifts were mentioned in passing in Definition I.12.6 of:

* [[John Gray]], *[[Adjointness for 2-Categories|Formal category theory: adjointness for $2$-categories]]*, Lecture Notes in Mathematics, **391**, Springer (1974) &lbrack;[doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280)&rbrack;

where it is mentioned the concept does not have a name since they had never been considered before in [[Cat]].

Kan lifts were called "liftings" in:

* [[Ross Street]], [[Bob Walters]], *Yoneda structures on 2-categories*,  JPAA **50** (1978) 350-379 &lbrack;<a href="https://doi.org/10.1016/0021-8693(78)90160-6">doi:10.1016/0021-8693(78)90160-6</a>&rbrack;

The terminology "Kan lifting" is used in:

* Charles Grellois, *Algebraic theories, monads, and arities* (2011) &lbrack;[arXiv:1110.3294](https://arxiv.org/abs/1110.3294), [hal:00670841](https://inria.hal.science/hal-00670841)&rbrack; 

The terminology "Kan lift" seems to first appear in:

* Weng Kin Ho, *Characterising E-projectives via Co-monads*, Electronic Notes in Theoretical Computer Science **301** (2014) 61-77 &lbrack;[doi:10.1016/j.entcs.2014.01.006](https://doi.org/10.1016/j.entcs.2014.01.006)&rbrack;

[[!redirects Kan lifts]]
[[!redirects Kan lifting]]
[[!redirects Kan liftings]]
