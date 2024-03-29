
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Statement

The **chain rule** is the statement that [[differentiation]] $d : Diff \to Diff$  is a [[functor]] on [[Diff]]:

given two [[smooth function]]s between [[smooth manifold]]s $f : X \to Y$ and $g : Y \to Z$ we have

$$
  d(g \circ f) : 
  T X 
  \stackrel{d f}{\to}
  T Y 
  \stackrel{d g}{\to}
  T Z
  \,.
$$

If one thinks of a [[tangent vector]] $v \in T_x X$ to be an equivalence class of a smooth path $\gamma_v : [-\epsilon,\epsilon] \to X$, for some $\epsilon\gt 0$, with $\gamma(0) = x$, then the chain rule is the [[associativity]] of the composite

$$
  [-\epsilon,\epsilon] \stackrel{\gamma_v}{\to} X \stackrel{f}{\to} Y \stackrel{g}{\to} Z
  \,.
$$

Bracketed as $(g \circ f)\circ \gamma_v$ this represents $d(g \circ f)(v)$. Bracketed as $g \circ (f \circ \gamma_v)$ is represents $d g (d f (v))$.

Alternatively, in a context of [[synthetic differential geometry]] where with $D$ being the [[infinitesimal space|infinitesimal interval]] we may _identify_ $v$ with $v : D \to X$, the chain rule is the associativity of

$$
  D \stackrel{v}{\to} X \stackrel{f}{\to} Y \stackrel{g}{\to} Z
  \,.
$$


## Examples

### Elementary calculus

Let $X = Y = Z = \mathbb{R}$ the [[real line]]. Then the [[tangent bundle]] $T X$ is canonically identified with $\mathbb{R} \times \mathbb{R}$.

Given two functions, $f, g : \mathbb{R} \to \mathbb{R}$ their derivatives are traditionally regarded again as functions $f', g' : \mathbb{R} \to \mathbb{R}$, though strictly speaking we are to think of them as the maps

$$
  d f, d g : \mathbb{R} \times \mathbb{R} = T \mathbb{R}  \to T \mathbb{R}  = \mathbb{R} \times \mathbb{R}
$$

given by

$$
  d f : (x,v) \mapsto (f(x), v f'(x))
$$

and

$$
  d g : (x,v) \mapsto (g(x), v g'(x))
  \,.
$$

The composite

$$
  d (g \circ f) : \mathbb{R} \times \mathbb{R} = 
  T \mathbb{R} \to T \mathbb{R} = \mathbb{R} \times \mathbb{R}
$$

is therefore the map

$$
  d(g \circ f) : (x,v) \mapsto (f(x), v f'(x)) 
   \mapsto 
     (g(f(x)), v f'(x) g'(f(x)))
  \,.
$$

Therefore we have

$$
  (g \circ f)'(x) = f'(x) g'(f(x))
  \,.
$$

This is the form in which the chain rule is usually introduced in elementary calculus. 


#### Remarks

While the chain rule is of great theoretical importance, it is completely unnecessary for the working out of derivatives of elementary functions in ordinary calculus (including the multivariable case).  Every result giving the derivative of an elementary function corresponds to a rule (along the lines of the [[product rule]]) for the operation of that function to any expression.  For example, instead of learning that
$$ \frac{\mathrm{d}}{\mathrm{d}x} (\sin x) = \cos x $$
and then applying both this fact *and* the chain rule to find the derivative of an expression of the form $\sin u$, just learn
$$ \frac{\mathrm{d}}{\mathrm{d}x} (\sin u) = \cos u \,\frac{\mathrm{d}u}{\mathrm{d}x} $$
and apply this rule directly; the original fact is the special case in which $u \coloneqq x$.  Even better, learn the rule as
$$ \mathrm{d}(\sin u) = \cos u \,\mathrm{d}u ;$$
then it applies without further modification to multivariable calculus (as well as implicit differentiation, related rates, integration by substitution, and other stock features of one-variable calculus).

The chain rule could still be used in the *proof* of this 'sine rule'.  Even so, it is quite possible to prove the sine rule directly (much as one proves the product rule directly rather than using the two-variable chain rule and the partial derivatives of the function $x, y \mapsto x y$).  In any case, the chain rule is not directly needed when working out specific derivatives.  As a *rule* of differentiation, the chain rule is needed only when an unspecified [[differentiable function]] $f$ appears, and then may be given in the form
$$ \frac{\mathrm{d}}{\mathrm{d}x} \bigl(f(u)\bigr) = f'(u) \,\frac{\mathrm{d}u}{\mathrm{d}x} $$
or
$$ \mathrm{d}\bigl(f(u)\bigr) = f'(u) \,\mathrm{d}u $$
to match other rules.

Although the chain rule is often written as

\[ 
  \frac{\mathrm{d}y}{\mathrm{d}x} = \frac{\mathrm{d}y}{\mathrm{d}u} 
  \,
  \frac{\mathrm{d}u}{\mathrm{d}x} ,\label{trivial} 
\]

this is an oversimplification.  Upon choosing an independent variable, it is possible (and easy) to give a rigorous definition of the [[derivative|differential]] $\mathrm{d}u$, and then (eq:trivial) is a triviality (assuming no division by zero).  However, with such a definition of differential, (eq:trivial) is *not* the chain rule!  The reason is that, when (eq:trivial) is used as a mnemonic for the chain rule, ${\mathrm{d}u}/{\mathrm{d}x}$ uses $x$ as the independent variable, but ${\mathrm{d}y}/{\mathrm{d}u}$ uses $u$.  Either may be chosen to define differentials[^invertibility], but one must (a priori) be consistent.  Now, it so happens that the choice of independent variable is entirely irrelevant; differentials have the same meaning no matter which independent variable is used.  But *this* fact requires proof; *it* is the chain rule (or at least a prerequisite for using (eq:trivial) as the chain rule), and it is *not* a triviality.  In this form, the chain rule is also known as **Cauchy's invariant rule**.

[^invertibility]:  Well, either may be chosen as long as their differentials are nowhere zero, which is exactly what must be true for (1) to make sense.  More precisely, given that $x$ works as an independent variable, the Chain Rule tells us that $u$ works just as well so long as $\mathrm{d}u$ (as defined using $x$) is nowhere zero.  This may be related to the easy but wrong proof of the Chain Rule that founders on a division by zero in exactly the same place (where $\mathrm{d}u$ would be), although I don't see a direct connection. 


### Formal algebra {#FormalAlgebra}

The chain rule can also be discussed as a piece of formal algebra of [[power series]] (over a general [[commutative ring]] $A$). We present a conceptual proof based on considerations of [[synthetic differential geometry|SDG]]. 

The statement is that if $q, p \in A[ [x] ]$ are power series, with $0$ the $0^{th}$ (constant) [[coefficient]] of $p$, then $(q \circ p)'(x) = q'(p(x))p'(x)$ under standard definitions. 

Let $D = A[y]/(y^2)$ be the [[representing object]] for [[derivations]]. Let $\delta: A[ [x] ] \to A[ [x] ] \otimes_A D \cong A[ [x] ][y]/(y^2)$  be the unique topological $A$-algebra map (under the $(x)$-[[adic topologies]]) that sends $x$ to $x + y$.  (If it helps, think $\delta(q) = q(x + y)$.)  For $p \in A[ [x] ]$, define $p'$ via the equation $\delta(p) = p(x) + p'(x)y$. 

Let $\pi: A[ [x] ] \otimes_A D \to A[ [x] ] \otimes_A D$ be the unique [[topological algebra]] map taking $x$ to $p(x)$ and $y$ to $p'(x)y$.  Let $- \circ p: A[ [x] ] \to A[ [x] ]$ denote the unique topological algebra map that takes $x$ to $p$. Then the diagram 

$$\array{
A[ [x] ] & \stackrel{\delta}{\to} &  A[ [x] ] \otimes_A D \\ 
\mathllap{- \circ p} \downarrow & & \downarrow \mathrlap{\pi} \\ 
A[ [x] ] & \underset{\delta}{\to} & A[ [x] ] \otimes_A D
}$$ 

commutes in the category of topological algebras, since the two legs agree when evaluated at the generator $x$. But then, evaluating each leg at a power series $q \in A [ [x]]$, we have 

$$[\delta(- \circ p)](q) = \delta(q \circ p) = (q \circ p)(x) + (q \circ p)'(x)y$$ 

and 

$$[\pi \delta](q) = \pi(\delta(q)) = \pi(q(x) + q'(x)y) = q(p(x)) + q'(p(x))(p'(x)y)$$ 

whence the coefficients of $y$ agree: $(q \circ p)'(x) = q'(p(x))p'(x)$.


## Related concepts

* [[natural bundle]]

* [[total derivative]]

* [[(∞,1)-category theory|(∞,1)-]][[categorification]]: [[Goodwillie chain rule]]

## References

A [[synthetic mathematics|synthetic]] formalization of the chain rule in [[differential cohesion|differential]] [[cohesive homotopy type theory]] is given in


* {#Wellen18} [[Felix Wellen]], Lemma 3.5 of _[[schreiber:thesis Wellen|Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966))


See also

* Wikipedia, _[Chain rule](https://en.wikipedia.org/wiki/Chain_rule)_

On the [[Goodwillie chain rule]] in [[Goodwillie calculus]]:

* John R. Klein, [[John Rognes]], _A chain rule in the calculus of homotopy functors_, Geom. Topol. 6 (2002) 853-887 ([arXiv:math/0301079](http://arxiv.org/abs/math/0301079))

* [[Jacob Lurie]], section 6.3 of _[[Higher Algebra]]_


[[!redirects chain rule]]
[[!redirects chain law]]
[[!redirects Cauchy's invariant rule]]
