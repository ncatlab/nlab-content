
# Hessians
* table of contents
{: toc}

##Idea

In all cases, a Hessian is a symmetric [[bilinear form]] on a [[tangent space]], encoding second-order information about a twice-[[differentiable function]].  (Compare the [[differential]] of a once-differentiable function, which is a [[1-form]] on the tangent space.)

For the purpose of this page, a tangent vector "is" a local [[derivation]] on [[germ]]s of functions.  If you don't like this model, take it that the natural isomorphism is unwritten, but trivial to insert; we do not actually name any derivations, but only germs.


## Trivial preliminary lemma

If an $\mathbb{R}$-bilinear form $G$ on germs $X,Y$ of $T M$ at a point $x$ of a twice-[[differentiable manifold]] $M$ is $C^2$-linear in one argument and symmetric, then it descends to a bilinear form on the tangent space $T_x M$.


## Definitions 

Given a $C^2$ manifold $M$ and $C^2$ function $\varphi:M\to \mathbb{R}$, the (ordered) second [[derivative]] of $\varphi$, for germs $X$ and $Y$ of tangent fields, is simply
$$ X (Y \varphi).$$
At a [[critical point]] $x$, (i.e., $(d\varphi)_x = 0$) [[exercise|one checks]] that
$$ X (Y \varphi) = Y (X \varphi) $$
so that for a real function germ $f$,
$$ X ((f\cdot Y)\varphi) = f \cdot (X (Y \varphi)) $$
and hence the symmetric bilinear form
$$ Hesse_{\varphi,x} (X,Y) = X(Y \varphi)$$
descends to the tangent space at $x$, and is pronounced as the __Hessian__ of $\varphi$ at the critical point $x$.

When $M$ carries a torsion-free [[connection]] $\nabla$, (e.g., the [[Levi-Civita connection]] of a [[Riemannian structure]]), one may define a global Hessian, defined for germs by
$$ Hesse_{\varphi,\nabla} (X,Y) = X(Y \varphi) - (\nabla_X Y) \varphi $$
which again is symmetric, and hence descends to the tangent space.  Note, however, this obviously depends on the particular connection used.


[[!redirects Hessian]]
[[!redirects Hessians]]
[[!redirects Hessian matrix]]
[[!redirects Hessian matrixes]]
[[!redirects Hessian matrices]]
