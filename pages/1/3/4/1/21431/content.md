
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

[[!redirects Theory of flat functors]]
[[!redirects theory of continuous flat functors]]
[[!redirects theory of J-continuous flat functors]]


## Idea

The **theory of J-continuous flat functors** on a [[site]] $(\mathcal{C},J)$ is the [[geometric theory]] $\mathbb{T}_J^{\mathcal{C}}$ whose models in a Grothendieck topos $\mathcal{E}$ correpond precisely to J-continuous flat functors $\mathcal{C}\to\mathcal{E}$ and, by well known representation theorems, to [[geometric morphisms]] $\mathcal{E}\to Sh(\mathcal{C},J)$ whence $\mathbb{T}_J^{\mathcal{C}}$ provides a uniform albeit (in general) uneconomical axiomatization of the [[geometric theory]] classified by $Sh(\mathcal{C},J)$.

## Definition

Let $(\mathcal{C},J)$ be a small site. The **theory of J-continuous flat functors** is given by the following geometric theory $\mathbb{T}_J^{\mathcal{C}}$ over the signature $\Sigma$ which has a sort $\lceil A\rceil$ for every object $A$ of $\mathcal{C}$ and function symbols $\lceil f\rceil :\lceil A\rceil\to\lceil B\rceil$ for every function $f:A\to B$:

* axioms $\top\vdash_x \lceil i\rceil(x)=x$ for all identity morphisms $i$.

* axioms $\top\vdash_x\lceil f\rceil(x)=\lceil h\rceil(\lceil g\rceil (x))$ for all triples $f,g,h$ with $f=g\circ h$.

* an axiom $\top\vdash\underset{A\in\mathcal{C}}{\bigvee} (\exists x:\lceil A\rceil) \top$.

* axioms $\top\vdash_{x:A,y:B}\underset{A\overset{f}{\leftarrow} C\overset{g}{\rightarrow B}}{\bigvee}\exists (z:\lceil C\rceil)\big(\lceil f\rceil (z:\lceil C\rceil)=x:\lceil A\rceil\wedge \lceil g\rceil (z:\lceil C\rceil)=y:\lceil B\rceil\big)$ where the disjunction ranges over all cones on the discrete diagram consisting of $A$ and $B$.

* axioms $\lceil f\rceil (x:\lceil A\rceil)=\lceil g\rceil (x:\lceil A\rceil)\vdash_{x:\lceil A\rceil}\bigvee_{h:C\to A|f\circ h=g\circ h} \exists(z:\lceil C\rceil)\big(\lceil h\rceil(z:\lceil C\rceil)=x:\lceil A\rceil\big)$ for any pair $f,g:A\to B$, the disjunction ranging over all $h$ equalizing $f,g$.

* axioms $\top\vdash_{x:\lceil A\rceil}\bigvee_{i\in I}\exists (y_i:\lceil B_i\rceil) \big(\lceil f_i\rceil(y_i:\lceil B_i\rceil)=x:\lceil A\rceil\big)$ for each J-covering $\{f_i:B_i\to A|i\in I\}$.

### Remark

The first two axiom schemata correspond to functoriality, the third to fifth to [[filtered category|filteredness]] (this being a notion equivalent to flatness), and the last to J-continuity (turning J-covers into epimorphic families).

Given a small category $\mathcal{C}$, $Set^{\mathcal{C}^{op}}\simeq Sh(\mathcal{C},J_0)$ where $J_0$ is the [[trivial topology]]. The theory of flat functors on $\mathcal{C}$ coincides with $\mathbb{T}_{J_0}^{\mathcal{C}}$ since the last axiom schema becomes redundant for the maximal sieves whence the first five axiom schemata axiomatize the notion of a flat functor on $\mathcal{C}$ and the resulting **theory of flat functors** is seen to be of [[theory of presheaf type|presheaf type]].


## Examples

* Let $(\emptyset,\emptyset)$ be the empty site. Then the signature $\Sigma$ is empty and only the third condition takes hold, yielding $\mathbb{T}_\emptyset^{\emptyset}=\{\top\vdash\bot\}$ i.e. the empty topos $Sh(\emptyset,\emptyset)=\mathbf{1}$ classifies the **inconsistent theory**.


## Related entries

* [[flat functor]]

* [[geometric theory]]

* [[Diaconescu's theorem]]

* [[theory of objects]]

## References

* [[Olivia Caramello]], _Lattices of theories_ , arXiv:0905.0299 (2009). ([abstract](https://arxiv.org/abs/0905.0299), p.11)

* [[Olivia Caramello]], _Theories, Sites, Toposes_ , Oxford UP 2018. (p.58f)

* [[Peter Johnstone]], _Sketches of an Elephant vol.II_ , Oxford UP 2002. (p.897)