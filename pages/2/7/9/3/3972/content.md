

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea ##

The _Cauchy principal value_ of a [[function]] which is [[integrable function|integrable]] on the [[complement]] of one point is, if it exists, the [[limit of a sequence|limit]] of the [[integrals]] of the function over subsets in the [[complement]] of this point as these integration [[domains]] tend to that point _symmetrically_ from all sides.

One also subsumes the case that the "point" is "at infinity", hence that the function is [[integrable function|integrable]] over every [[bounded subsets|bounded]] [[domain]]. In this case the Cauchy principal value is the [[limit of a sequence|limit]], if it exists, of the [[integrals]] of the function over bounded domains, as their bounds tend _symmetrically_ to infinity.

The operation of sending a [[compactly supported function|compactly supported]] [[smooth function]] ([[bump function]]) to Cauchy principal value of its pointwise product with a function $f$ that may be singular at the origin defines a [[distribution]], usually denoted $PV(f)$.  

When the Cauchy principal value exists but the full [[integral]] does not (hence when the full integral "diverges") one may think of the Cauchy principal value as "exracting a finite value from a diverging quantity". This is similar to the _intuition_ of the early days of [[renormalization]] in [[perturbative quantum field theory]] ([[Schwinger-Tomonaga-Feynman-Dyson]]), but one has to be careful not to carry this analogy too far.

One point where the Cauchy principal value really does play a key role in [[perturbative quantum field theory]] is in the computation of [[Green functions]] ([[propagators]]) for the [[Klein-Gordon operator]] and the [[Dirac operator]]. See at _[[advanced and retarded propagator]]_ for more on this.



## Definition 


### As an integral

+-- {: .num_defn #CauchyIntegralValueOfIntegralOverRealline}
###### Definition
**(Cauchy principal value of an integral over the real line)**

Let $f \colon \mathbb{R} \to \mathbb{R}$ be a [[function]] on the [[real line]] such that for every [[positive real number]] $\epsilon$ its [[restriction]] to $\mathbb{R}\setminus (-\epsilon, \epsilon)$ is [[integrable function|integrable]]. Then the _Cauchy principal value_ of $f$ is, if it exists, the [[limit of a sequence|limit]]

$$
  PV(f) \coloneqq \underset{\epsilon \to 0}{\lim} 
  \underset{\mathbb{R} \setminus (-\epsilon, \epsilon)}{\int} f(x) \, d x
  \,.
$$

=--


### As a distribution


+-- {: .num_defn #CauchyPrincipalValueAsDistributionOnRealLine}
###### Definition
**(Cauchy principal value as distribution on the real line)**

Let $f \colon \mathbb{R} \to \mathbb{R}$ be a [[function]] on the [[real line]] such that for all [[bump functions]] $b \in C^\infty_{cp}(\mathbb{R})$ the Cauchy principal value of the pointwise product function $f b$ exists, in the sense of def. \ref{CauchyIntegralValueOfIntegralOverRealline}. Then this assignment

$$
  PV(f)
  \;\colon\;
  b \mapsto PV(f b)
$$

defines a [[distribution]] $PV(f) \in \mathcal{D}'(\mathbb{R})$.

=--

## Examples

### The principal value of $1/x$



+-- {: .num_example }
###### Example

Let $f \colon \mathbb{R} \to \mathbb{R}$ be an [[integrable function]] which is symmetric, in that $f(-x) = f(x)$ for all $x \in \mathbb{R}$. Then the principal value integral (def. \ref{CauchyIntegralValueOfIntegralOverRealline}) of $x \mapsto \frac{f(x)}{x}$ exists and is zero:

$$
  \underset{\epsilon \to 0}{\lim}
  \underset{\mathbb{R}\setminus (-\epsilon, \epsilon)}{\int}
  \frac{f(x)}{x} d x
  \; = \; 0
$$


This is because, by the symmetry of $f$ and the skew-symmetry of $x \mapsto 1/x$, the the two contributions to the integral are equal up to a sign:

$$
  \int_{-\infty}^{-\epsilon} \frac{f(x)}{x} d x
  \;=\;
  -
  \int_{\epsilon}^\infty \frac{f(x)}{x} d x
  \,.
$$

=--



+-- {: .num_example #PrincipalValueOfInverseFunctionCharacteristicEquation}
###### Example

The principal value distribution $PV\left( \frac{1}{x}\right)$ (def. \ref{CauchyPrincipalValueAsDistributionOnRealLine}) solves the distributional equation

$$
  \label{DistributionalEquationxfOfxEqualsOne}
  x PV\left(\frac{1}{x}\right) = 1
  \phantom{AAA}
  \in \mathcal{D}'(\mathbb{R}^1)
  \,.
$$

Since the [[delta distribution]] $\delta \in \mathcal{D}'(\mathbb{R}^1)$ solves the equation

$$
  x \delta(x) = 0
  \phantom{AAA}
  \in \mathcal{D}'(\mathbb{r}^1)
$$

we have that more generally every [[linear combination]] of the form

$$
  \label{GeneralDistributionalSolutionToxfEqualsOne}
  F(x)
  \coloneqq
  PV(1/x) + c \delta(x)   
  \phantom{AAA}
  \in \mathcal{D}'(\mathbb{R}^1)
$$

for $c \in \mathbb{C}$, is a distributional solution to $x F(x) =  1$.

=--


+-- {: .proof}
###### Proof

This is immediate from the definition: For $b \in C^\infty_c(\mathbb{R}^1)$ any [[bump function]] we have that 

$$
  \begin{aligned}
    \left\langle x PV\left(\frac{1}{x}\right), b \right\rangle
    & \coloneqq
    \underset{\epsilon \to 0}{\lim}
    \underset{\mathbb{R}^1 \setminus (-\epsilon, \epsilon)}{\int}
    \frac{x}{x}b(x) \, d x
    \\
    & =
    \int b(x)  d x
    \\
    & =
    \langle 1,b\rangle 
  \end{aligned}
$$


=--

+-- {: .num_prop}
###### Proposition

In fact (eq:GeneralDistributionalSolutionToxfEqualsOne) is the most general distributional solution to (eq:DistributionalEquationxfOfxEqualsOne).

=--

> Proof?


+-- {: .num_defn #IntegrationAgainstInverseOfxWithImaginaryOffset}
###### Definition
**(integration against inverse variable with imaginary offset)**


Write 

$$
  \tfrac{1}{x + i0^\pm}
  \;\in\;
  \mathcal{D}'(\mathbb{R})
$$

for the [[distribution]] which is the [[limit]] in $\mathcal{D}'(\mathbb{R})$ of the [[non-singular distributions]] which are given by the [[smooth functions]] $x \mapsto \tfrac{1}{x \pm i \epsilon}$ as the [[positive real number]] $\epsilon$ tends to zero:

$$
  \frac{1}{
     x + i 0^\pm
  }
  \;\coloneqq\;
  \underset{ { \epsilon \in (0,\infty) } \atop { \epsilon \to 0 }  }{\lim}
  \tfrac{1}{x \pm i \epsilon}
$$

hence the distribution which sends $b \in C^\infty(\mathbb{R}^1)$ to 

$$
  b \mapsto
  \underset{\mathbb{R}}{\int}
    \frac{b(x)}{x \pm i \epsilon} \, d x
  \,.
$$

=--


+-- {: .num_prop #CauchyPrincipalValueEqualsIntegrationWithImaginaryOffsetPlusDelta}
###### Proposition
**([[Cauchy principal value]] equals integration with [[imaginary number|imaginary]] offset plus [[delta distribution]])**

The Cauchy principal value distribution $PV\left( \tfrac{1}{x}\right) \in \mathcal{D}'(\mathbb{R})$ (def. \ref{CauchyPrincipalValueAsDistributionOnRealLine}) is equal to the sum of the integration over $1/x$ with imaginary offset (def. \ref{IntegrationAgainstInverseOfxWithImaginaryOffset}) and a [[delta distribution]].

$$
 PV\left(\frac{1}{x}\right)
  \;=\;
 \frac{1}{x + i 0^\pm}
  \pm i \pi \delta
  \,.
$$

In particular, by prop. \ref{PrincipalValueOfInverseFunctionCharacteristicEquation} this means that $\tfrac{1}{x + i 0^\pm}$ solves the distributional equation

$$
  x \frac{1}{x + i 0^\pm}
  \;=\;
  1
  \phantom{AA}
  \in \mathcal{D}'(\mathbb{R}^1)
  \,.
$$

=--


+-- {: .proof}
###### Proof


Using that

$$
  \begin{aligned}
    \frac{1}{x \pm i \epsilon}
    & =
    \frac{
       x \mp i \epsilon
    }{
      (x + i \epsilon)(x - i \epsilon)
    }
    \\
    & =
    \frac{ x \mp i \epsilon }{(x^2 + \epsilon^2)}
  \end{aligned}
$$

we have for every [[bump function]] $b \in C^\infty_{cp}(\mathbb{R}^1)$
 
$$
  \begin{aligned}
    \underset{\epsilon \to 0}{\lim}
    \underset{\mathbb{R}^1}{\int}
    \frac{b(x)}{x \pm i \epsilon}
    d x
    & \;=\; 
    \underset{
      (A)
    }{
    \underbrace{
    \underset{\epsilon \to 0}{\lim}
    \underset{\mathbb{R}^1}{\int}
    \frac{x^2}{x^2 + \epsilon^2} \frac{b(x)}{x}   
    d x
    }
    }
    \mp i \pi
    \underset{(B)}{ 
    \underbrace{
    \underset{\epsilon \to 0}{\lim}
    \underset{\mathbb{R}^1}{\int}
    \frac{1}{\pi}
    \frac{\epsilon}{x^2 + \epsilon^2} b(x)
    \,
    d x
    }}
  \end{aligned}
$$

Since 

$$
  \array{
     && \frac{x^2}{x^2 + \epsilon^2}
     \\
     & {}^{\mathllap{ { {\vert x \vert} \lt \epsilon } \atop { \epsilon \to 0 }  }}\swarrow 
     && 
     \searrow^{\mathrlap{ {{\vert x\vert} \gt \epsilon} \atop { \epsilon \to 0 }  }}
     \\
     0 && && 1
  }
$$

it follows (...) that $(A) = PV\left( \frac{b(x)}{x} \right)$.

Similarly $(B) = b(0)$. (...)

=--

## Examples ##

...

## Related concepts

* [[zeta function regularization]]

## References ##

Named after [[Augustin Cauchy]]

* [[Ram Kanwal]], section 8.3 of _Linear Integral Equations_ Birkh&#228;user 1997

See also

* Wikipedia, _[Cauchy principal value](http://en.wikipedia.org/wiki/Cauchy_principal_value)_

* Wikipedia, _[Hadamard principal value](http://en.wikipedia.org/wiki/Hadamard_finite_part_integral)_


[[!redirects Cauchy principal values]]

[[!redirects principal value]]
[[!redirects principal vaues]]
