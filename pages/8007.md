An Introduction to Distributions and Foliations

MTH 864 · Spring 2008
In smooth manifold theory, the notion of a tangent space makes it possi-
ble for differentiation to take place on an abstract manifold. In this paper,
the notion of a distribution will be presented which makes it possible for in-
tegration to take place on an abstract manifold. The first section introduces
terminology and builds intuition via an analogy to the concept of integral
curves. The second section presents the Frobenius theorem–one of the foun-
dational results in smooth manifold theory. The concluding section leaves the
reader with foliations and a brief look at their connection to the Frobenius
theorem.
1 Preliminaries
Let M be an m-dimensional manifold, TpM the tangent space to p ∈ M, and
TM the tangent bundle of M. Throughout this work, things are implicitly
smooth. Recall that a vector field on M is a section of TM and can be thought
of as a choice of tangent vector at every point in the manifold. Given a vector
field V , one can consider an associated integral curve.
Definition. An integral curve of a vector field V is a curve γ : (a, b) → M
(a and b real numbers) such that
γ
′
(t) = Vγ(t)
for all t ∈ (a, b).

1Definition. The Lie bracket of the vector fields V and W is [V, W] = V W −
W V .
It is well known that [V, W] itself defines a (natural) vector field. What
we will find below is that “nice” means given any vector fields V , W with
Vp, Wp ∈ Dp for all p in some neighborhood U, it follows that [Vp, Wp] ∈ Dp.
If this condition is satisfied (it is only necessary to check it on the basis vector
fields), then the distribution D is called involutive.
Lemma. If D is an integrable distribution, then D is necessarily involutive.
Proof. Let V and W be local sections of D ⊂ TM defined on some U ⊂ M
and let p ∈ U. Since D is integrable, we have some S an integral manifold
of D containing p. Since V and W are sections of D, we know that V and
W are tangent to S on U. By properties of the naturality of the Lie bracket,
[V, W] is also tangent to S and so [V, W]p ∈ Dp. This holds for all points in
U and so D is involutive.
As an example, consider the 2-dimensional distribution D on R

Turka Tachloo

3 with
basis vector fields

                                       writer:
                                       NADEEM AHMAD RATHER 
                                       M.PHIL MATHEMATICS
                                     R/O TURKA TACHLOO
                                  ANANTNAG(JAMMU AND KASHMIR)