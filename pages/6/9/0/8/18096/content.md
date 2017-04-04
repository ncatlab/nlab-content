# Contents 
* table of contents 
{:toc}

## Idea 

H&#246;lder's inequality is a basic inequality in analysis, used to prove that if the sum of positive numbers $p, q$ equals their product, then the [[L-p space|Banach spaces]] $L^p, L^q$ are Banach duals of one another. 

## Statements 

Let $(X, \mu)$ be a [[measure space]], and for $p \gt 0$ let $L^p$ denote $L^p(X, \mu)$, the Banach space of complex-valued functions on $X$ with finite [[p-norm]]  considered modulo almost everywhere equality. Suppose $p, q$ are positive real numbers such that $\frac1{p} + \frac1{q} = 1$. Then **H&#246;lder's inequality** states that for any $f \in L^p, g \in L^q$ we have 

$$\int_X \left| f g \right| \leq {\|f\|_p} {\|g\|_q}$$ 

(in particular, $f g$ is an $L^1$ function). 

The "[[nPOV]]" meaning is this: in this situation there is a canonical pairing $\langle -, - \rangle$ between $L^p$ and $L^q$, 

$$L^p \times L^q \to \mathbb{C}: (f, g) \mapsto \langle f, g \rangle \coloneqq \int_X f \cdot g,$$ 

which gives a bounded linear map $L^p \otimes L^q \to \mathbb{C}$ between Banach spaces. The point of H&#246;lder's inequality is that this pairing is a *short* map, i.e., a map of norm bounded above by $1$. In other words, this is morphism in the [[symmetric monoidal closed category]] [[Ban]] consisting of Banach spaces and short linear maps between them. Accordingly, the map $L^p \otimes L^q \to \mathbb{C}$ induces (by [[currying]]) a map from $L^p$ to the Banach dual of $L^q$: 

$$L^p \to (L^q)^\ast \coloneqq [L^q, \mathbb{C}]$$ 

(again a short map of course), and reciprocally a map $L^q \to (L^p)^\ast$. 

It is a short step to prove that in fact the norm of the pairing $L^p \otimes L^q \to \mathbb{C}$ is *exactly* $1$, and even better that the maps $L^p \to (L^q)^\ast$ and $L^q \to (L^p)^\ast$ are in fact [[isometry|isometric]] embeddings. With a little more work (with the help of the [[Radon-Nikodym theorem]]; see for example [here](https://www.math.ucdavis.edu/~hunter/measure_theory/measure_notes_ch7.pdf)), one sees these maps are [[surjective map|surjective]] and thus [[isomorphisms]] in $Ban$. 

+-- {: .num_remark} 
###### Remark 
Throughout we are working in the range $1 \lt p, q \lt \infty$. We also have a H&#246;lder inequality in the extreme case where $p = 1$, $q = \infty$, something which is easily seen directly, and it is true also that $(L^1)^\ast \cong L^\infty$, *but* it is not true that $(L^\infty)^\ast$ is isomorphic to $L^1$. Or, it is at least not true in [[ZFC]], although it may be true in [[dream mathematics]]. 
=-- 

## Proof of H&#246;lder's inequality 

The proof is remarkably simple. First, if $p, q \gt 0$ and $\frac1{p} + \frac1{q} = 1$, then we have *Young's inequality*, viz. for $a, b \gt 0$ 

$$a b \leq \frac{a^p}{p} + \frac{b^q}{q}$$ 

with equality precisely when $a^p = b^q$. This is quickly derived from the (strict) convexity of the [[exponential function]], that $0 \leq t \leq 1$ implies  

$$e^{t x + (1-t)y} \leq t e^x + (1-t)e^y$$ 

where equality holds iff $e^x = e^y$. All one has to do is put $t = \frac1{p}$ and arrange $x, y$ so that $e^x = a^p$ and $e^y = b^q$. 

Then, to prove ${|\langle f, g \rangle|} \leq {\|f\|_p} {\|g\|_q}$, we may assume $f, g$ nonzero (so their norms are positive) and normalize them to unit vectors $u = f/{\|f\|_p}, v = g/{\|g\|_q}$, so that now the object is to prove 

$$\int_X {|u|} \cdot {|v|} \leq 1.$$ 

But since we are dealing with unit vectors, we have $\int_X {|u|^p} = 1$ and $\int_X {|v|^q} = 1$, and now what we want follows straightaway from Young's inequality applied to integrands: 

$$\int_X {|u|} \cdot {|v|} \leq \int_X \frac{|u|^p}{p} + \frac{|v|^q}{q} = \frac1{p} + \frac1{q} = 1$$ 

and so the proof of H&#246;lder's inequality is complete. 

To prove that the norm of the pairing $\langle -, - \rangle$ is exactly $1$ (is not less than $1$), it's enough to take any $u \in L^p$ of norm $1$, so $f = {|u|}$ is a nonnegative function of norm $1$, and then put $g = f^{p-1} = f^{p/q}$. We then have $f^p = g^q$ (almost) everywhere, where we then have $f g = \frac{f^p}{p} + \frac{g^q}{q}$, and now 

$$\int_X f g = \int_X \frac{f^p}{p} + \frac{g^q}{q} = \frac1{p} + \frac1{q} = 1.$$ 

Actually these calculations do a little better: they show that upon currying, the map 

$$L^p \to [L^q, \mathbb{C}]: f \mapsto \lambda g. \langle f, g \rangle$$ 

preserves the norm, so that $L^p$ isometrically embeds into $(L^q)^\ast$. 

## Relation to Minkowski's inequality 

Recall that [[Minkowski's inequality]] is just the [[triangle inequality]] in the context of [[L-p space]]. There is a well-known trick, covered in just about every functional analysis text, that allows one to deduce Minkowski's inequality as a corollary of H&#246;lder's inequality. You can look it up for instance in the English Wikipedia, [here](https://en.wikipedia.org/wiki/Minkowski_inequality). 

What seemingly most such presentations lack is motivation for the trick, so let us try to say something about this. 

First, Minkowski's inequality can be restated as asserting the convexity of the unit ball $B = \{f \in L^p: {\|f\|_p} \leq 1\}$ of $L^p$. If we place ourselves for a moment in the context of $L^p$ *real*-valued functions, then it suffices to show that $B$ is the intersection of a collection of [[affine space|affine]] half-spaces, say $H_\lambda = \{f \in L^p: \lambda(f) \leq 1\}$ where $\lambda: L^p \to \mathbb{R}$ is a (continuous) linear functional. But with hindsight into the meaning of H&#246;lder's inequality, seen as paving the way to characterizing linear functionals on $L^p$ as those of the form $\lambda(g) = (f \mapsto \langle f, g \rangle)$ for some $g \in L^q$, it's only natural to see whether we can find a sufficiently large collection $B'$ of such $g$ such that $B = \bigcap_{g \in B'} H_{\lambda(g)}$, and in fact the intuition is that the unit ball $B'$ in $L^q$ ought to work. 

Thus the idea is clear, and it's just a matter of technique from here. We let the relation ${|\langle f, g \rangle|} \leq 1$ on $L^p \times L^q$ set up a [[Galois connection]] between subsets of $L^p$ and subsets of $L^q$. The connection takes the unit ball $B'$ in $L^q$ to 

$$(B')^\perp \coloneqq \{f \in L^p: (\forall_{g \in B'}) {|\langle f, g \rangle|} \leq 1\}$$ 

which is clearly convex, being an intersection of convex sets $\{f: {|\langle f, g \rangle|} \leq 1\}$, one for each $g \in B'$. H&#246;lder's inequality itself just asserts the containment $B \subseteq (B')^\perp$. If we show the other inclusion $(B')^\perp \subseteq B$, then $B = (B')^\perp$ is convex. So we want to show that if ${|\langle f, g \rangle|} \leq 1$ whenever ${\|g\|_q} \leq 1$, then ${\|f\|_p} \leq 1$. But we already did that calculation when we proved $L^p \hookrightarrow (L^q)^\ast$ is an isometry. Explicitly: take $h = {|f|^p}/f$ (with $h = 0$ where $f = 0$). Then ${|h|} = {|f|^{p-1}} = {|f|^{p/q}}$, so ${|h|^q} = {|f|^p}$ whence ${\|h\|_q^q} = {\|f\|_p^p}$. Put $g = \frac{h}{{\|h\|_q}}$; since ${\|g\|_q} \leq 1$, it follows by the hypothesis on $f$ that $1 \geq {|\langle f, g \rangle|}$. But this gives 

$$1 \geq \frac1{{\|h\|_q}} \int_X f h = \frac1{{\|f\|_p^{p/q}}} \int_X {|f|^p} = {\|f\|_p^{p - p/q}} = {\|f\|_p}$$ 

as was to be shown. 

The standard derivation of Minkowski's inequality from H&#246;lder's inequality is nothing more than a very tidied-up rendering of this argument, but without the additional conceptual explanation given here. 

[[!redirects Holder's inequality]] 
[[!redirects Holder inequality]] 
[[!redirects Hölder inequality]] 