
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[real analysis]], the notion of lifting a function from the [[real numbers]] $\mathbb{R}$ to some [[sequentially Cauchy complete]] [[pseudometric space]] $\mathbb{R}^\mathcal{L}$ of real numbers equipped with computational structure. The pseudometric space $\mathbb{R}^\mathcal{L}$ comes with a function $\pi_1:\mathbb{R}^\mathcal{L} \to \mathbb{R}$ whose [[image]] is the [[Cauchy real numbers]]. The computational structures which can be used for lifting functions include

* [[locators]], 

* [[Cauchy sequences]] of [[rational numbers]], with [[modulus of continuity]] or defined constructively using the [[BHK interpretation]],

* base $b$ signed-digit representations, for a given natural number $b$ greater than $1$. 

## Definition

### Using locators

Let $\mathbb{R}$ be a sequentially Cauchy complete Archimedean ordered field, and let 
$$\mathbb{R}^\mathcal{L} \coloneqq \sum_{x:\mathbb{R}} \mathrm{locator}(x)$$ 
be the set of all pairs of real numbers and [[locators]], with canonical projection function $\pi_1:\mathbb{R}^\mathcal{L} \to \mathbb{R}$. This projection function is not an [[injection]] because in general a real number may have more than one locator; however, the [[image]] of this projection function is the [[Cauchy real numbers]] $\mathbb{R}_C$, which is a [[subset]] of $\mathbb{R}$ and thus does have an injection into $\mathbb{R}$. A [[function]] $f:\mathbb{R} \to \mathbb{R}$ **lifts to [[locators]]** if it comes with a function $f^\mathcal{L}:\mathbb{R}^\mathcal{L} \to \mathbb{R}^\mathcal{L}$ such that the following [[square]] in [[Set]] [[commutative square|commutes]]:

$$
  \array{& \mathbb{R}^\mathcal{L} & \overset{f^\mathcal{L}}\rightarrow & \mathbb{R}^\mathcal{L} & \\
          \pi_1 & \downarrow &&\downarrow & \pi_1\\
          &\mathbb{R} & \underset{f}\rightarrow& \mathbb{R} & \\
}$$

### Using Cauchy sequences of rational numbers

Let $\mathbb{R}$ be a sequentially Cauchy complete Archimedean ordered field, and let 
$$\mathbb{R}^\mathcal{L} \coloneqq \sum_{l:\mathbb{R}} \sum_{x:\mathbb{N} \to \mathbb{Q}} \prod_{\epsilon:\mathbb{Q}_+} \sum_{N:\mathbb{N}} \prod_{n:\mathbb{N}} (n \geq N) \to (\vert x(n) - l \vert \lt \epsilon)$$ 
be the set consisting of a real number and a Cauchy sequence of rational numbers constructively converging to the real number, in the sense of the [[BHK interpretation]], with canonical function $\pi_1:\mathbb{R}^\mathcal{L} \to \mathbb{R}$. A [[function]] $f:\mathbb{R} \to \mathbb{R}$ **lifts to [[Cauchy sequences]] of [[rational numbers]]** if it comes with a function $f^\mathcal{L}:\mathbb{R}^\mathcal{L} \to \mathbb{R}^\mathcal{L}$ such that the following [[square]] in [[Set]] [[commutative square|commutes]]:

$$
  \array{& \mathbb{R}^\mathcal{L} & \overset{f^\mathcal{L}}\rightarrow & \mathbb{R}^\mathcal{L} & \\
          \pi_1 & \downarrow &&\downarrow & \pi_1\\
          &\mathbb{R} & \underset{f}\rightarrow& \mathbb{R} & \\
}$$

Alternatively, one can define the set $\mathbb{R}^\mathcal{L}$ directly as the set of [[Cauchy sequences]] of [[rational numbers]], defined constructively using the [[BHK interpretation]]

$$\mathbb{R}^\mathcal{L} \coloneqq \sum_{x:\mathbb{N} \to \mathbb{Q}} \prod_{\epsilon:\mathbb{Q}_+} \sum_{N:\mathbb{N}} \prod_{n:\mathbb{N}} \prod_{m:\mathbb{N}} (n \geq N) \times (m \geq N) \to (\vert x(n) - x(m) \vert \lt \epsilon)$$ 

Quotienting $\mathbb{R}^\mathcal{L}$ by a suitable [[equivalence relation]] - there are many different options available used in the constructive analysis literature, yields the [[Cauchy real numbers]] $\mathbb{R}_C$ with a quotient map $[-]:\mathbb{R}^\mathcal{L} \to \mathbb{R}_C$, and the Cauchy real numbers [[embedding|embed]] into any sequentially Cauchy complete Archimedean ordered field $\mathbb{R}$, with [[uniqueness quantifier|unique]] [[ring homomorphism]] $\eta:\mathbb{R}_C \to \mathbb{R}$, yielding a function $\lambda x.\eta([x]):\mathbb{R}^\mathcal{L} \to \mathbb{R}$. A [[function]] $f:\mathbb{R} \to \mathbb{R}$ **lifts to [[Cauchy sequences]] of [[rational numbers]]** if it comes with a function $f^\mathcal{L}:\mathbb{R}^\mathcal{L} \to \mathbb{R}^\mathcal{L}$ such that the following [[square]] in [[Set]] [[commutative square|commutes]]:

$$
  \array{& \mathbb{R}^\mathcal{L} & \overset{f^\mathcal{L}}\rightarrow & \mathbb{R}^\mathcal{L} & \\
          \lambda x.\eta([x]) & \downarrow &&\downarrow & \lambda x.\eta([x])\\
          &\mathbb{R} & \underset{f}\rightarrow& \mathbb{R} & \\
}$$

## Examples

* The field operations on $\mathbb{R}$ lifts to locators or Cauchy sequences of rational numbers

* Hence, any [[real polynomial function]] or [[rational function]] lifts to locators or Cauchy sequences of rational numbers. 

* Given any convergent sequence of functions $f:\mathbb{N} \to \mathbb{R} \to \mathbb{R}$ such that each $f_n$ lifts to locators or Cauchy sequences of rational numbers, then the limit function $\lim_{n \to \infty} f_n$ lifts to locators or Cauchy sequences of rational numbers, since for each real number $x:\mathbb{R}$ equipped with a locator or Cauchy sequence of real numbers, the limit of the pointwise sequence $f_{(-)}(x)$ also comes with a locator or Cauchy sequence of real numbers.

* Hence, any [[smooth function]] or [[analytic function]] lifts to locators or Cauchy sequences of rational numbers. 

* The [[absolute value]], [[minimum]] and [[maximum]] [[lattice]] operations, [[real square root]], and more generally real $n$-th root partial functions all lift to locators or Cauchy sequences of rational numbers. These (partial) functions aren't smooth at $0$, but can nevertheless be defined as the limit of a convergent sequence of functions. 

## See also

* [[locator]]

* [[Cauchy sequence]] of [[rational numbers]]

* [[Cauchy real number]]

* [[Dedekind real numbers]]

* [[intermediate value theorem]]

* [[computable analysis]]

## References

* [[Auke Booij]], *Extensional constructive real analysis via locators*, ([abs:1805.06781](https://arxiv.org/abs/1805.06781))

* [[Auke Booij]], *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

[[!redirects lifting a function]]
[[!redirects lift a function]]
[[!redirects lifts a function]]

[[!redirects lifting functions]]
[[!redirects lift functions]]
[[!redirects lifts functions]]

[[!redirects lifting to locators]]
[[!redirects lift to locators]]
[[!redirects lifts to locators]]

[[!redirects lifting to Cauchy sequences of rational numbers]]
[[!redirects lift to Cauchy sequences of rational numbers]]
[[!redirects lifts to Cauchy sequences of rational numbers]]

[[!redirects lifting a function to locators]]
[[!redirects lift a function to locators]]
[[!redirects lifts a function to locators]]

[[!redirects lifting a function to Cauchy sequences of rational numbers]]
[[!redirects lift a function to Cauchy sequences of rational numbers]]
[[!redirects lifts a function to Cauchy sequences of rational numbers]]

[[!redirects lifting functions to locators]]
[[!redirects lift functions to locators]]
[[!redirects lifts functions to locators]]

[[!redirects lifting functions to Cauchy sequences of rational numbers]]
[[!redirects lift functions to Cauchy sequences of rational numbers]]
[[!redirects lifts functions to Cauchy sequences of rational numbers]]