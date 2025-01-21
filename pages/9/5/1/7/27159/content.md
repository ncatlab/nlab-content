
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

> See also at *[[Kähler differential]]* the section *[Over smooth rings regarded as ordinary rings](Kähler+differential#SmoothOrPlain)*.

\tableofcontents

## Idea

In [[algebraic geometry]], the module of [[Kähler differentials]] of a [[commutative ring]] $R$ corresponds under the [[Serre–Swan theorem]] to the [[cotangent bundle]] of the [[Zariski spectrum]] of $R$.

In contrast, the module of [[Kähler differentials]] of the [[commutative real algebra]] of [[smooth functions]] on a [[smooth manifold]] $M$ receives a canonical map from the module of smooth sections of the [[cotangent bundle]] of $M$ that is quite far from being an isomorphism.

An example illustrating this point is $M=\mathbf{R}$, since in the module of (traditionally defined) [[Kähler differentials]] of $C^\infty(M)$ we have 
$
  \mathrm{d}
  \big(exp(x)\big)
  \ne 
  exp(x)\,\mathrm{d}x
$
(at least when assuming the [[axiom of choice]], cf. [Speyer 2009](#Speyer09)), 
where $
\exp\colon\mathbf{R}\to\mathbf{R}$ is the [[exponential function]] and $x=id_{\mathbf{R}}$.
That is to say, the traditional algebraic notion of a [[Kähler differential]] is unable to deduce that $\exp'=\exp$ using the [[Leibniz rule]].


However, this is not a defect in the conceptual idea itself, but merely a failure to use the correct formalism.  The appropriate notion of a ring in the context of [[differential geometry]] is not merely a commutative real algebra, but a more refined structure, namely, a [[C^∞-ring]].

This notion comes with its own variant of [[commutative algebra]].  Some of the resulting concepts turn out to be exactly the same as in the traditional case.  For example, ideals of [[C^∞-rings]] and [[modules over C^∞-rings]] happen to coincide with ideals and modules in the traditional sense.  Others, like derivations, must be defined carefully, and definitions that used to be equivalent in the traditional algebraic context need not remain so in the context of [[C^∞-rings]].

Observe that a map of sets $\mathrm{d} \colon A\to M$ (where $M$ is an $A$-module) is a derivation if and only if for any real [[polynomial]] $f(x_1,\ldots,x_n)$ the [[chain rule]] holds:
$$
 \mathrm{d}
 \big(
   f(a_1,\ldots,a_n)
 \big)
  =
  \sum_i {\partial f\over\partial x_i}(x_1,\ldots,x_n) 
 \mathrm{d}x_i
 \,.
$$
Indeed, taking $f(x_1,x_2)=x_1+x_2$ and $f(x_1,x_2)=x_1 x_2$ recovers the additivity and [[Leibniz rule|Leibniz property]] of derivations, respectively.

Observe also that $f$ is an element of the free commutative real algebra on $n$ elements, i.e., $\mathbf{R}[x_1,\ldots,x_n]$.

If we now substitute [[C^∞-rings]] for commutative real algebras, we arrive at the correct notion of a derivation for [[C^∞-rings]]:

\begin{definition}
A __C^∞-derivation__ of a [[C^∞-ring]] $A$ is a map of sets $A\to M$ (where $M$ is a [[module]] over $A$) such that the following [[chain rule]] holds for every smooth function $f\in\mathrm{C}^\infty(\mathbf{R}^n)$:
$$
 
 \mathrm{d}\big(
   f(a_1,\ldots,a_n)
  \big)
 =
  \sum_i 
  {
   \partial f\over\partial x_i
  }(x_1,\ldots,x_n) \mathrm{d} x_i
 \,,
$$
where both sides use the structure of a [[C^∞-ring]] to evaluate a smooth real function on a collection of elements in $A$.
\end{definition}

The module of Kähler C^∞-differentials can now be defined in the same manner as ordinary [[Kähler differentials]], using C^∞-derivations instead of ordinary derivations.

\begin{theorem}
\linebreak
The module of Kähler C^∞-differentials of the [[C^∞-ring]] of smooth functions on a [[smooth manifold]] $M$ is canonically isomorphic to the module of sections of the [[cotangent bundle]] of $M$.
\end{theorem}
([Dubuc & Kock 1984](#DubucKock84))


## Related concepts

* [[Kähler differential]], [[derivation]]

* [[C^∞-ring]], [[module over a C^∞-ring]]


## References

* {#DubucKock84} [[E. J. Dubuc]], [[A. Kock]], _On 1-form classifiers_, Communications in Algebra **12** 12 (1984) 1471–1531 &lbrack;[doi:10.1080/00927878408823064](https://doi.org/10.1080/00927878408823064)&rbrack;

* {#Speyer09} [[David Speyer]]: *Kähler differentials and ordinary differentials*, MathOverflow reply (2009) &lbrack;[MO:a/9723](https://mathoverflow.net/a/9723/381)&rbrack;


