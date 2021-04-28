+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Distributivity pullback

* table of contents
{: toc}

## Idea

A **distributivity pullback** is the data which encodes a particular [[exponentiable morphism|exponentiation]] along a [[morphism]] in a [[category]].  In other words, it is a [[cofree object]] with respect to a [[pullback]] functor.

## Definition

+-- {: .un_defn}
###### Definition
For morphisms $g:Z\to A$ and $f:A\to B$ in a category, a **pullback around $(f,g)$** is a diagram
$$\array{ X & \xrightarrow{p} & Z & \xrightarrow{g} & A\\
  ^q\downarrow &&&& \downarrow^f\\
  Y && \xrightarrow{r} && B}
$$
in which the outer rectangle is a [[pullback]].
=--

A morphism of pullbacks around $(f,g)$ consists of $s:X\to X'$ and $t:Y\to Y'$ such that $p's=p$, $q s=t q'$, and $r = r's$.

+-- {: .un_defn}
###### Definition
For $g:Z\to A$ and $f:A\to B$ as above, a **distributivity pullback** around $(f,g)$ is a terminal object of the category of pullbacks around $(f,g)$.
=--

If the above diagram is a distributivity pullback, we say that it exhibits $r$ as a *distributivity pullback of $g$ along $f$*.

## Properties

### Connection to exponentiation

+-- {: .un_theorem}
###### Theorem
A morphism $f:A\to B$ is [[exponentiable morphism|exponentiable]] if and only if all distributivity pullbacks along $f$ exist.
=--
+-- {: .proof}
###### Proof
The universal property of a distributivity pullback says exactly that $Y\xrightarrow{r} B$ is the exponential of $g$ along $f$.
=--

### Connection to distributivity

In a category with pullbacks, for any pullback around $(f,g)$ with $f$ and $q$ exponentiable, we have a canonical Beck-Chevalley isomorphism
$$ r^* f_* \xrightarrow{\cong} q_* p^* g^* . $$
The [[mate]] of the inverse of this is a transformation
$$ \delta_{p,q,r}:r_! q_* p^* \to f_* g_! $$

+-- {: .un_theorem}
###### Theorem
A pullback around $(f,g)$ with $f$ and $q$ exponentiable is a distributivity pullback if and only if $\delta_{p,q,r}$ is an isomorphism.
=--
+-- {: .proof}
###### Proof
See [(Weber, Proposition 2.2.3)](#Weber).
=--

Invertibility of $\delta$ expresses that [[dependent products]] (the functors $f_*$ and $q_*$) distribute over [[dependent sums]] (the functors $g_!$ and $r_!$).

For instance, in the category of sets, if $(C_z)_{z\in Z}$ is a $Z$-indexed family of sets, then
$$ (f_* g_! C)_b = \prod_{f(a)=b} \sum_{g(z)=a} C_z $$
while
$$ (r_! q_* p^* C)_b = \sum_{r(y)=b} \prod_{q(x)=y} C_{p(x)} $$
As a very simple example, if $B=1$, $A=\{0,1\}$, and $Z=\{00,01,02,10,11\}$ with $g(i j) = i$, then $Y$ is the set of sections of $g$, $X$ the set of pairs of a section and an element of $A$, and $p$ the evaluation.  Then if $C = (C_{00}, C_{01}, C_{02}, C_{10}, C_{11})$, we have
$$ f_* g_! C = (C_{00} + C_{01} + C_{02}) \times (C_{10} + C_{11}) $$
and
$$ r_! q_* p^* C = (C_{00}\times C_{10}) + (C_{00}\times C_{11}) + 
(C_{01}\times C_{10}) + (C_{01}\times C_{11}) +
(C_{02}\times C_{10}) + (C_{02}\times C_{11}).
$$

In the [[internal logic|internal]] [[dependent type theory]] of the ambient category, if we express $f$ and $g$ as [[dependent types]]

$$ b:B \vdash A(b) : Type \qquad and \qquad b:B, a:A(b) \vdash Z(b,a) : Type $$

then the exponential $r$ of $g$ along $f$ in a distributivity pullback is the [[dependent product type]]

$$ b:B \vdash \prod_{a:A(b)} Z(b,a) : Type. $$

and the distributivity isomorphism $\delta$ says that for any further dependent type

$$ b:B, a:A(b), z:Z(b,a) \vdash W(b,a,z) : Type$$

in the context of $b:B$ we have an isomorphism

$$ \sum_{\phi:\prod_{a:A(b)} Z(b,a) } \prod_{a:A(b)} W(b,a,\phi(a)) \qquad \cong \qquad  \prod_{a:A(b)} \sum_{z:Z(b,a)} W(b,a,z). $$

This isomorphism (or more specifically the left-to-right map) has traditionally been called the "axiom of choice" in [[Martin-Lof type theory]], since if $\sum$ and $\prod$ are interpreted according to [[propositions as types]] then it looks like the set-theoretic axiom of choice.  However, this is not really appropriate, since this is a provable statement rather than an additional axiom, and does not have any of the usual strong consequences of the set-theoretic axiom of choice.  See [[axiom of choice]] for further discussion.

### Connection to pullback complements

If $p$ is an isomorphism, then a distributivity pullback is also a [[final pullback complement]].

## References

* [[Mark Weber]], "Polynomials in categories with pullbacks", [arXiv](http://arxiv.org/abs/1106.1983), [TAC](http://tac.mta.ca/tac/volumes/30/16/30-16abs.html)
 {#Weber}

[[!redirects distributivity pullbacks]]
