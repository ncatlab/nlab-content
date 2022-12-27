
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
{:toc}

## Idea 

*Hölder's inequality* is a basic [[inequality]] in [[analysis]], used to prove that if the sum of positive numbers $p, q$ equals their product, then the [[L-p space|Banach spaces]] $L^p, L^q$ are Banach duals of one another. 

## Statements 

Let $(X, \mu)$ be a [[measure space]], and for $p \gt 0$ let $L^p$ denote $L^p(X, \mu)$, the Banach space of complex-valued functions on $X$ with finite [[p-norm]]  considered modulo almost everywhere equality. Suppose $p, q$ are positive real numbers such that $\frac1{p} + \frac1{q} = 1$ (that is, $q+p=q p$). Then **Hölder's inequality** states that for any $f \in L^p, g \in L^q$ we have 

$$\int_X \left| f g \right| \leq {\|f\|_p} {\|g\|_q}$$ 

(in particular, $f g$ is an $L^1$ function). 

The "[[nPOV]]" meaning is this: in this situation there is a canonical pairing $\langle -, - \rangle$ between $L^p$ and $L^q$, 

$$L^p \times L^q \to \mathbb{C}: (f, g) \mapsto \langle f, g \rangle \coloneqq \int_X f \cdot g,$$ 

which gives a bounded linear map $L^p \otimes L^q \to \mathbb{C}$ between Banach spaces. The point of Hölder's inequality is that this pairing is a *short* map, i.e., a map of norm bounded above by $1$. In other words, this is morphism in the [[symmetric monoidal closed category]] [[Ban]] consisting of Banach spaces and short linear maps between them. Accordingly, the map $L^p \otimes L^q \to \mathbb{C}$ induces (by [[currying]]) a map from $L^p$ to the Banach dual of $L^q$: 

$$L^p \to (L^q)^\ast \coloneqq [L^q, \mathbb{C}]$$ 

(again a short map of course), and reciprocally a map $L^q \to (L^p)^\ast$. 

It is a short step to prove that in fact the norm of the pairing $L^p \otimes L^q \to \mathbb{C}$ is *exactly* $1$, and even better that the maps $L^p \to (L^q)^\ast$ and $L^q \to (L^p)^\ast$ are in fact [[isometry|isometric]] embeddings. With a little more work (with the help of the [[Radon-Nikodym theorem]]; see for example [here](https://www.math.ucdavis.edu/~hunter/measure_theory/measure_notes_ch7.pdf)), one sees these maps are [[surjective map|surjective]] and thus [[isomorphisms]] in $Ban$. 

+-- {: .num_remark} 
###### Remark 
Throughout we are working in the range $1 \lt p, q \lt \infty$. We also have a H&#246;lder inequality in the extreme case where $p = 1$, $q = \infty$, something which is easily seen directly, and it is true also that $(L^1)^\ast \cong L^\infty$, *but* it is not true that $(L^\infty)^\ast$ is isomorphic to $L^1$. Or, it is at least not true in [[ZFC]], although it may be true in [[dream mathematics]]. 
=-- 

## Proof of Hölder's inequality 

The proof is remarkably simple. First, if $p, q \gt 0$ and $\frac1{p} + \frac1{q} = 1$, then we have *[[Young's inequality]]*, viz. for $a, b \gt 0$ 

$$
  a b 
  \;\leq\;
  \frac{a^p}{p} 
    + 
  \frac{b^q}{q}
  \,,
$$ 

with equality precisely when $a^p = b^q$. This is quickly derived from the (strict) convexity of the [[exponential function]], that $0 \leq t \leq 1$ implies  

$$
  e^{t x + (1-t)y} 
  \leq 
  t e^x + (1-t)e^y
  \,,
$$ 

where equality holds iff $e^x = e^y$. All one has to do is put $t = \frac{1}{p}$ and arrange $x, y$ so that $e^x = a^p$ and $e^y = b^q$. 

Then, to prove ${|\langle f, g \rangle|} \leq {\|f\|_p} {\|g\|_q}$, we may assume $f, g$ nonzero (so their norms are positive) and normalize them to unit vectors $u = f/{\|f\|_p}, v = g/{\|g\|_q}$, so that now the object is to prove 

$$\int_X {|u|} \cdot {|v|} \leq 1.$$ 

But since we are dealing with unit vectors, we have $\int_X {|u|^p} = 1$ and $\int_X {|v|^q} = 1$, and now what we want follows straightaway from Young's inequality applied to integrands: 

$$\int_X {|u|} \cdot {|v|} \leq \int_X \frac{|u|^p}{p} + \frac{|v|^q}{q} = \frac1{p} + \frac1{q} = 1$$ 

and so the proof of Hölder's inequality is complete. 

To prove that the norm of the pairing $\langle -, - \rangle$ is exactly $1$ (is not less than $1$), it's enough to take any $u \in L^p$ of norm $1$, so $f = {|u|}$ is a nonnegative function of norm $1$, and then put $g = f^{p-1} = f^{p/q}$. We then have $f^p = g^q$ (almost) everywhere, where we then have $f g = \frac{f^p}{p} + \frac{g^q}{q}$, and now 

$$\int_X f g = \int_X \frac{f^p}{p} + \frac{g^q}{q} = \frac1{p} + \frac1{q} = 1.$$ 

Actually these calculations do a little better: they show that upon [[currying]], the map 

$$
  \begin{array}{ccc}
    L^p 
    &\longrightarrow& 
   [L^q, \mathbb{C}]
   \\
   f 
   &\mapsto& 
   \lambda g. \langle f, g \rangle
  \end{array}
$$ 

preserves the norm, so that $L^p$ [[isometry|isometrically]] embeds into $(L^q)^\ast$. 

## Properties

### Relation to Minkowski's inequality 

Recall that [[Minkowski's inequality]] is just the [[triangle inequality]] in the context of [[L-p space]]. There is a well-known trick, covered in just about every [[functional analysis]] text, that allows one to deduce Minkowski's inequality as a corollary of Hölder's inequality. You can look it up for instance in the English Wikipedia, [here](https://en.wikipedia.org/wiki/Minkowski_inequality). 

What seemingly most such presentations lack is motivation for the trick, so let us try to say something about this. 

First, [[Minkowski's inequality]] can be restated as asserting the convexity of the unit ball $B = \{f \in L^p: {\|f\|_p} \leq 1\}$ of $L^p$. If we place ourselves for a moment in the context of $L^p$ *real*-valued functions, then it suffices to show that $B$ is the intersection of a collection of [[affine space|affine]] half-spaces, say $H_\lambda = \{f \in L^p: \lambda(f) \leq 1\}$ where $\lambda: L^p \to \mathbb{R}$ is a (continuous) linear functional. But with hindsight into the meaning of H&#246;lder's inequality, seen as paving the way to characterizing linear functionals on $L^p$ as those of the form $\lambda(g) = (f \mapsto \langle f, g \rangle)$ for some $g \in L^q$, it's only natural to see whether we can find a sufficiently large collection $B'$ of such $g$ such that $B = \bigcap_{g \in B'} H_{\lambda(g)}$, and in fact the intuition is that the unit ball $B'$ in $L^q$ ought to work. 

Thus the idea is clear, and it's just a matter of technique from here. We let the relation ${|\langle f, g \rangle|} \leq 1$ on $L^p \times L^q$ set up a [[Galois connection]] between subsets of $L^p$ and subsets of $L^q$. The connection takes the unit ball $B'$ in $L^q$ to 

$$
  (B')^\perp 
  \coloneqq 
  \big\{
    f \in L^p 
     \colon 
   (\forall_{g \in B'})
   \; 
   {|\langle f, g \rangle|} 
    \leq 1
  \big\}
  \,,
$$ 

which is clearly convex, being an intersection of convex sets $\{f: {|\langle f, g \rangle|} \leq 1\}$, one for each $g \in B'$. H&#246;lder's inequality itself just asserts the containment $B \subseteq (B')^\perp$. If we show the other inclusion $(B')^\perp \subseteq B$, then $B = (B')^\perp$ is convex. So we want to show that if ${|\langle f, g \rangle|} \leq 1$ whenever ${\|g\|_q} \leq 1$, then ${\|f\|_p} \leq 1$. But we already did that calculation when we proved $L^p \hookrightarrow (L^q)^\ast$ is an isometry. Explicitly: take $h = {|f|^p}/f$ (with $h = 0$ where $f = 0$). Then ${|h|} = {|f|^{p-1}} = {|f|^{p/q}}$, so ${|h|^q} = {|f|^p}$ whence ${\|h\|_q^q} = {\|f\|_p^p}$. Put $g = \frac{h}{{\|h\|_q}}$; since ${\|g\|_q} \leq 1$, it follows by the hypothesis on $f$ that $1 \geq {|\langle f, g \rangle|}$. But this gives 

$$1 \geq \frac1{{\|h\|_q}} \int_X f h = \frac1{{\|f\|_p^{p/q}}} \int_X {|f|^p} = {\|f\|_p^{p - p/q}} = {\|f\|_p}$$ 

as was to be shown. 

The standard derivation of Minkowski's inequality from Hölder's inequality is nothing more than a very tidied-up rendering of this argument, but without the additional conceptual explanation given here. 

### Relation to Log-convex functions

Let $D$ be a [[convex space]], e.g. an [[affine space]]. We say that a [[function]] $f: D \to (0, \infty)$ is *log-convex* if its [[logarithm]] $\log(f)$ is a [[convex function]]. 

Hölder's inequality is closely related to the notion of log-convexity. On the one hand, we saw that the inequality follows from the convexity of the [[exponential function]], which is the most basic log-convex function of all. On another hand, we have the following result which uses Hölder's inequality. 

+-- {: .num_theorem} 
###### Theorem 
The collection of log-convex positive functions on a convex domain $D$ is closed under pointwise multiplication, pointwise addition, and pointwise sups. 
=-- 

+-- {: .proof} 
###### Proof 
The statement for multiplication is clear since $\log(f \cdot g) = \log(f) + \log(g)$ and any sum of convex functions is convex. 

Similarly, $\log: (0,\infty) \to \mathbb{R}$ is an isomorphism of [[partially ordered sets]] and so $\log (\sup\{f_i\}) = \sup\{\log(f_i)\}$. It thus suffices to show that if $f_i$ is a collection of convex functions on $D$, then so is $\sup\{f_i\}$. For $x, y \in D$ and $a, b \geq 0$ such that $a + b = 1$, we must show 

$$\sup\{f_i\}(a x + b y) \leq a \sup\{f_i\}(x) + b\sup\{f_i\}(y);$$ 
 
letting $c$ denote the right side, this holds iff $f_i(a x + b y) \leq c$ for all $i$ (by definition of $\sup$). But 

$$\array{
f_i(a x + b y) & \leq & a f_i(x) + b f_i(y) & since\; f_i\; is\; convex \\
 & \leq & a\sup\{f_i\}(x) + b\sup\{f_i\}(y) & 
}.$$ 

Finally, for the sum $f + g$, in order to show $\log(f + g)$ is convex, it suffices to show that 

$$\label{sum} (f + g)\left(\frac1{p}x + \frac1{q}y\right) \leq (f+g)(x)^{\frac1{p}} (f+g)(y)^{\frac1{q}}$$ 

for $p, q \gt 1$ such that $\frac1{p} + \frac1{q} = 1$. But setting 

$$s = f(x)^{\frac1{p}}, \qquad t = g(x)^{\frac1{p}}, \qquad u = f(y)^{\frac1{q}}, \qquad v = g(y)^{\frac1{q}},$$ 

the right side of (eq:sum) is $(s^p + t^p)^{\frac1{p}} \cdot (u^q + v^q)^{\frac1{q}}$. By H&ouml;lder's inequality, this is greater than or equal to 

$$\array{
s u + t v & = & f(x)^{\frac1{p}} f(y)^{\frac1{q}} + g(x)^{\frac1{p}} g(y)^{\frac1{q}} \\ 
 & \geq & f\left(\frac1{p} x + \frac1{q} y\right) + g\left(\frac1{p} x + \frac1{q} y\right)
}$$ 

where the last inequality is by log-convexity of $f$ and $g$. 
=-- 

This last theorem enters into the account of [Artin (1931)](#Artin31) of the basic theory of the [[Gamma function]]: 

+-- {: .num_cor} 
###### Corollary 
The [[Gamma function]] 

$$\Gamma(x) = \int_0^\infty t^x e^{-t} \frac{d t}{t}$$ 

is log-convex over the domain $x \gt 0$. 
=--

+-- {: .proof} 
###### Proof 
The function $x \mapsto t^{x-1}$ is log-linear, hence log-convex. Hence the integral defining $\Gamma(x)$ over $x \gt 0$ is a sup over suitable Riemann sums that are positive-linear combinations of the form 

$$\sum_{i=1}^n t_i^{x-1} e^{-t_i} \Delta t_i$$ 
and these, and together with their sup, are log-convex by the Theorem. 
=-- 

The main fact underlying Artin's 1931 discussion is the [Bohr-Haagerup theorem](Gamma+function#BohrMollerupTheorem) ([Artin (1931), Thm. 2.1](#Artin31)): 

+-- {: .num_theorem #CharacterizationOgGamma} 
###### Theorem 
The [[Gamma function]] is characterized as the unique function $\Gamma: \{x \in \mathbb{R}|\; -x \notin \mathbb{N}\} \to \mathbb{R}$ satisfying the following conditions: 

* $\Gamma(1) = 1$, 

* $\Gamma(x+1) = x\Gamma(x)$, 

* $\Gamma$ is log-convex over $(0, \infty)$. 

=--

## References 

* {#Artin31} [[Emil Artin]], *Einführung in die Theorie der Gammafunktion*, Hamburger Mathematische Einzelschriften
l. Heft, Verlag B. G. Teubner, Leipzig (1931)

  English translation by Michael Butler: *The Gamma Function*, Holt, Rinehart and Winston (1931) &lbrack;[[Artin-TheGammaFunction.pdf:file]]&rbrack;

[[!redirects Hölder inequality]] 

[[!redirects Holder inequality]] 
[[!redirects Holder's inequality]] 

[[!redirects Hoelder inequality]]
[[!redirects Hoelder's inequality]]

