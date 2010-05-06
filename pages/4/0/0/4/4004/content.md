## Definition

Let $T\colon A\to B$ be a [[functor]] such that $A$ has a [[terminal object]] $1$.  Then $T$ can be factored as the composite
$$ A \overset{T_1}{\to} B/T1 \overset{\Sigma_{T1}}{\to} B.$$
We say that $T$ is a **parametric right adjoint**, or **p.r.a.**, if the functor $T_1$ has a left adjoint.

A [[monad]] is called **p.r.a.** if its functor part is p.r.a. and moreover its unit and multiplication are [[cartesian natural transformation|cartesian]].

## Properties

Since $\Sigma_{T1}$ [[created limit|creates]] [[connected limits]], if $T$ is p.r.a. then it [[preserved limit|preserves]] connected limits, and in particular preserves [[pullbacks]].  It follows that any p.r.a. monad is a [[cartesian monad]].  Conversely, an [[accessible functor]] between [[presheaf categories]] is p.r.a. if and only if it preserves [[connected limits]].

Any [[polynomial functor]] $\Sigma_h \Pi_g f^*$ is p.r.a., since then $T_1$ can be identified with $\Pi_g f^*$, which has the left adjoint $\Sigma_f \; g^*$.
## Generic morphisms

Central to the theory of parametric right adjoints is the notion of *$T$-generic* morphisms.  For any functor $T$, a morphism $f\colon B\to T A$ is (strictly) **$T$-generic** if any commutative square of the following form:
$$\array{B & \overset{\alpha}{\to} &T X \\
  ^f\downarrow && \downarrow^{T\gamma}\\
  T A& \underset{T \beta}{\to} & T Z}$$
has a unique filler $T A \to T X$.  A **generic factorization** of a map $f\colon B\to T A$ is a factorization
$$ B \overset{g}{\to} T D \overset{T h}{\to} T A $$
such that $g$ is $T$-generic.  Note that by the definition of genericity, generic factorizations are unique whenever they exist.  If $T$ is a monad and any map $B \to T A$ has a generic factorization, then there is an induced [[orthogonal factorization system]] on the [[Kleisli category]] of $T$ in which $T$-generic maps are the left class and the right class are the "free" maps, i.e. those which factor through the unit of $T$.

+-- {: .un_prop}
###### Proposition
A functor $T$ is a parametric right adjoint iff every map $B\to T A$ has a generic factorization.
=--
+-- {: .proof}
###### Proof
This is Proposition 2.6 of "Familial 2-functors and parametric right adjoints."
=--

P.r.a. functors between presheaf categories have an especially nice form.

+-- {: .un_prop}
###### Proposition
A functor $T\colon [I^{op},Set] \to [J^{op},Set]$ between presheaf categories is p.r.a. iff any map $y(j)\to T 1$ has a generic factorization, where $y(j)$ is the representable presheaf on an object $j\in J$.
=--
+-- {: .proof}
###### Proof
This is Proposition 2.10 of "Familial 2-functors and parametric right adjoints."  The "only if" direction is the previous proposition, while for the "if" direction, the given hypothesis allows us to define the functor
$$ E_T \colon y/T1 \to [I^{op},Set] $$
sending an object $(y(j) \to T 1)$ to the object occurring in its generic factorization.  Note that $y/T1$ is equivalently the [[category of elements]] of $T1$.  The definition of genericity, along with the Yoneda lemma, then shows that
$$ T(Z)(j) = \coprod_{x\in T1(j)} [I^{op},Set](E_T(x),Z) $$
which preserves connected limits, since it is a coproduct of representables.
=--

In particular, a p.r.a. functor $T\colon [I^{op},Set] \to [J^{op},Set]$ is determined by giving the object $T1\in [J^{op},Set]$ together with the functor $E_T\colon y/T1 = el(T1) \to [I^{op},Set]$.  We can think of $T1(j)$ as the setof all possible "shapes" which $T$ allows us to "glue together" to obtain an element of shape $j$, and $E_T$ as specifying exactly what each of those shapes looks like.  Then the above formula for $T(Z)(j)$ says that we look at all possible shapes $x\in T1(j)$ we can glue to get something of shape $j$, and for each such $x$ we look at all the "diagrams" in $Z$ of the corresponding shape $E_T(x)$.

## Examples

...

## References

* [[Mark Weber]], _Generic morphisms, parametric representations, and weakly cartesian monads_, Theory and applications of categories, 13:191&#8211;234, 2004. [link](http://www.tac.mta.ca/tac/volumes/13/14/13-14abs.html)

* [[Mark Weber]], _Familial 2-functors and parametric right adjoints_, 2008 [link](http://www.tac.mta.ca/tac/volumes/18/22/18-22abs.html)

[[!redirects parametric right adjoints]]
[[!redirects p.r.a. functor]]
[[!redirects p.r.a. functors]]
[[!redirects p.r.a. monad]]
[[!redirects p.r.a. monads]]
