[[!redirects Cauchy structures]]
[[!redirects Cauchy structure homomorphism]]
[[!redirects Cauchy structure homomorphisms]]
[[!redirects category of Cauchy structures]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

Let $\mathbb{Q}$ be the [[rational numbers]] and let 

$$\mathbb{Q}_{+} \coloneqq \{x \in \mathbb{Q} \vert 0 \lt x\}$$ 

be the set of positive rational numbers. 

A __Cauchy structure__ is a [[Booij premetric space]] $(S, \sim)$ with a function $rat:\mathbb{Q}_{+} \to S$ and a function $lim:C(S) \to S$, where $C(S)$ is the set of [[rational Cauchy approximation]]s in $S$, such that

* for all elements $a \in S$ and $b \in S$ and all positive rational numbers $\epsilon$, $a \sim_\epsilon b$ implies $a = b$. 

* for all elements $a \in S$ and $b \in S$ and all positive rational numbers $\epsilon$, $\vert a - b \vert \lt \epsilon$ implies that $rat(a) \sim_\epsilon rat(b)$

* for all elements $a \in S$ and rational Cauchy approximations $b \in C(S)$ and all positive rational numbers $\epsilon$ and $\eta$, $rat(a) \sim_\epsilon b(\eta)$ implies that $rat(a) \sim_{\epsilon + \eta} lim(b)$

* for all rational Cauchy approximations $a \in C(S)$ and elements $b \in S$ and all positive rational numbers $\delta$ and $\epsilon$, $a(\delta) \sim_\epsilon rat(b)$ implies that $lim(a) \sim_{\delta + \epsilon} rat(b)$

* for all rational Cauchy approximations $a \in C(S)$ and $b \in C(S)$ and all positive rational numbers $\delta$, $\epsilon$ and $\eta$, $a(\delta) \sim_\epsilon b(\eta)$ implies that $lim(a) \sim_{\delta + \epsilon + \eta} lim(b)$

For two Cauchy structures $S$ and $T$, a __Cauchy structure homomorphism__ is a function $f:S \to T$ such that

* for all elements $a \in S$ and $b \in S$ and all positive rational numbers $\epsilon$, $a \sim_{\epsilon} b$ implies $f(a) \sim_{\epsilon} f(b)$. 

* for all rational numbers $r \in \mathbb{Q}$, $f(rat(r)) = rat(r)$

* for all rational Cauchy approximations $r \in C(S)$, $f(lim(r)) = lim(f \circ r)$

* for all elements $a \in S$ and $b \in S$, suppose $P(a, b)$ is the predicate that if for all positive rational numbers $\epsilon$ $a \sim_\epsilon b$ is true, then $a = b$, and $Q(a, b)$ is the predicate that for all positive rational numbers $\epsilon$ $f(a) \sim_\epsilon f(b)$ is true, then $f(a) = f(b)$. Then for all elements $a \in S$ and $b \in S$, $P(a, b)$ implies $Q(a, b)$

The __category of Cauchy structures__ is a [[category]] $CauchyStr$ whose objects $Ob(CauchyStr)$ are Cauchy structures and whose morphisms $Mor(A, B)$, for objects $A \in Ob(CauchyStr)$ and $B \in Ob(CauchyStr)$, are Cauchy structure homomorphisms. The initial object in the category of Cauchy structures is the [[HoTT book real numbers]]. 

### In homotopy type theory ###

Let $\mathbb{Q}$ be the [[rational numbers]] and let 

$$\mathbb{Q}_{+} \coloneqq \sum_{x:\mathbb{Q}} 0 \lt x$$

be the positive rational numbers. 

A __Cauchy structure__ is a [[Booij premetric space]] $S$ with 

* a function $inj: \mathbb{Q} \to S$

* a function $lim: C(S) \to S$, where $C(S)$ is the type of [[rational Cauchy approximation]]s in $S$

* dependent families of terms

$$a:S, b:S \vdash eq(a, b): \Vert \prod_{\epsilon:\mathbb{Q}_{+}} (a \sim_{\epsilon} b) \Vert \to (a =_S b)$$
$$a:\mathbb{Q}, b:\mathbb{Q}, \epsilon:\mathbb{Q}_{+} \vdash \mu_{\mathbb{Q}, \mathbb{Q}}(a, b, \epsilon): (\vert a - b \vert \lt \epsilon) \to (inj(a) \sim_{\epsilon} inj(b))$$
$$a:\mathbb{Q}, b:C(S), \epsilon:\mathbb{Q}_{+}, \eta:\mathbb{Q}_{+} \vdash \mu_{\mathbb{Q}, C(S)}(a, b, \epsilon, \eta): (inj(a) \sim_{\epsilon} b_{\eta}) \to (inj(a) \sim_{\epsilon + \eta} lim(b))$$
$$a:C(S), b:\mathbb{Q}, \delta:\mathbb{Q}_{+}, \epsilon:\mathbb{Q}_{+} \vdash \mu_{C(S), \mathbb{Q}}(a, b, \delta, \epsilon): (a_{\delta} \sim_{\epsilon} inj(b) ) \to (lim(a) \sim_{\delta + \epsilon} inj(b))$$
$$a:C(S), b:C(S), \delta:\mathbb{Q}_{+}, \epsilon:\mathbb{Q}_{+}, \eta:\mathbb{Q}_{+} \vdash \mu_{C(S), C(S)}(a, b, \delta, \epsilon, \eta): (a_{\delta} \sim_{\epsilon} b_{\eta} ) \to (lim(a) \sim_{\delta + \epsilon + \eta} lim(b))$$

For two Cauchy structures $S$ and $T$, a __Cauchy structure homomorphism__ consists of

* a function $f:S \to T$ 

* a dependent family of functions 
$$a:S, b:S, \epsilon:\mathbb{Q}_{+} \vdash \pi(a, b, \epsilon): (a \sim_{S\epsilon} b) \to (f(a) \sim_{T\epsilon} f(b))$$

* a dependent family of types 
$$r:\mathbb{Q} \vdash \iota(r): f(inj_S(r)) = inj_T(r)$$

* a dependent family of types 
$$r:C(S) \vdash \lambda(r): f(lim_S(r)) = lim_T(f \circ r)$$

* a dependent family of types 
$$a:S, b:S, c:\Vert \prod_{\epsilon:\mathbb{Q}_{+}} (a \sim_{\epsilon} b) \Vert \vdash \eta(a, b, c): f(eq_S(a, b, c)) = eq_T(f(a), f(b), f(c))$$

## See also ##

* [[Booij premetric space]]
* [[Cauchy approximation]]
* [[HoTT book real numbers]]

## References ##

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))