### Introduction ###

The [[path groupoid]] is a groupoid internal to some category of [[generalized smooth spaces]].  Its space of morphisms is defined by taking a quotient of a variant of a [[path space]] by the notion of [[thin homotopy]].  The path space is, generally, the same in all proposed categories of [[generalized smooth space]] but as the path groupoid is formed by taking a quotient, its structure will vary depending on the choice.

### Linear Structure and Non-existence of Manifold Structure ###

Spurred by a [question on Mathoverflow](http://mathoverflow.net), we consider the question as to whether or not the path groupoid can have a manifold structure.  With no conditions, the question is meaningless (or so general as to be not worth answering) so we need to impose some conditions on what we expect the manifold structure to be.

The condition we impose is that its model space be the obvious one, namely the path groupoid in $\mathbb{R}^n$.  So before considering whether or not a general path groupoid (of a smooth manifold) can have a manifold structure, we examine the linear model.

We consider the space of smooth paths in $\mathbb{R}^n$, $P\mathbb{R}^n \coloneqq C^\infty(I,\mathbb{R}^n)$ (here and hereafter, $I = [0,1]$ is the closed interval).  We divide this by the relation of [[thin homotopy]].  Namely, two paths between fixed endpoints are equivalent if there is a thin homotopy relating one to the other.  Let us write $P_{TH}\mathbb{R}^n$ for the resulting space.  The relation is linear and so the resulting quotient is a vector space.  We can put on it the quotient structure from $P\mathbb{R}^n$.  Thus a linear function $T \colon P_{TH}\mathbb{R}^n \to E$ in to a [[LCTVS]] is continuous if and only if the composition $P\mathbb{R}^n \to E$ is continuous.  By taking $E$ to be an appropriate [[Banach space]], we can extend this to semi-norms.  As the family of continuous semi-norms on a LCTVS defines the LCTVS-structure, we see that the semi-norms on $P_{TH}\mathbb{R}^n$ are precisely those that descend from $P\mathbb{R}^n$.

So we wish to find the semi-norms $P_{TH}\mathbb{R}^n \to \mathbb{R}$.  To do this, we observe a subtlety.  Let $F \subseteq I$ be a finite set and let $P_F\mathbb{R}^n$ be the space of paths in $\mathbb{R}^n$ which are [[piecewise smooth map|piecewise-smooth]] where the breaks are constrained to lie in $F$.  We do **not** impose any boundary conditions on these paths, so by "piecewise-smooth" we mean continuous on $I$ and smooth on $I\setminus F$.  In particular, the left and right derivatives need not exist at the points of $F$.
For a fixed $F$, we can choose a smooth surjection $\alpha_F \colon I \to I$ which is stationary as it passes through the points of $F$.  Then for any piecewise-smooth map $\gamma \in P_F\mathbb{R}^n$, $\gamma \circ \alpha_F$ is smooth and the (linear) map $P_F\mathbb{R}^n \to P\mathbb{R}^n$, $\gamma \mapsto \gamma \circ \alpha_F$ is continuous.

+-- {: .query}
[[Andrew Stacey]]: on reflection, this step now seems a little dubious to me now.  It doesn't seem so obvious that if $\gamma \colon I \to \mathbb{R}$ is continuous on $I$ and smooth on the interior then it can be reparametrised to a smooth map on the whole of $I$.  I was getting the chain rule wrong in my workings.  What we really want is for $\gamma$ to be reparametrisable to a smooth map which is flat at the end points.  Certainly if $\gamma$ can be reparametrised to one where the left and right derivatives exist at the end points then it can be made flat, but this is not a necessary condition as evidenced by the function $t \mapsto \sqrt{t}$.  But I strongly suspect that something like $t \mapsto t \sin(t^{-1})$ can't be reparametrised as such.

This, then, casts a bit of doubt on the rest of the argument!
=--

We cannot fit these together to define a map $P_{ps}\mathbb{R}^n \to P\mathbb{R}^n$ (here, $P_{ps}\mathbb{R}^n$ is the colimit of $P_F\mathbb{R}^n$ over all finite subsets $F\subseteq I$) but when we divide out by thin homotopy then this does work.  That is, when we divide out by thin homotopy, the maps $P_{F,TH}\mathbb{R}^n \to P_{TH}\mathbb{R}^n$ are independent of the choices of reparametrisations $\alpha_F$ and so fit together to define a linear map $P_{ps,TH}\mathbb{R}^n \to P_{TH}\mathbb{R}^n$.  As this is continuous when restricted to each $P_{F,TH}\mathbb{R}^n$, it is continuous.

So if $\mu \colon P_{TH}\mathbb{R}^n \to \mathbb{R}$ is a continuous semi-norm, it defines a continuous semi-norm on $P_{ps,TH}\mathbb{R}^n$ and hence pulls-back to a continuous semi-norm on $P_{ps}\mathbb{R}^n$.

However, one of the main results of &lt;http://arxiv.org/abs/0803.0611> is that as a LCTVS, $P_{ps}\mathbb{R}^n$ is a subspace of the space of **continuous** paths.  Thus a continuous semi-norm $P_{TH}\mathbb{R}^n \to \mathbb{R}$ extends to a continuous semi-norm on the space $P^0\mathbb{R}^n$ of continuous paths.

So we can consider the quotient of $P^O\mathbb{R}^n$ by thin homotopy, $P^0_{TH}\mathbb{R}^n$ and $P_{TH}\mathbb{R}^n$ is then a subspace of this space.  As there are continuous paths which cannot be reparametrised to smooth paths, the inclusion is proper.  It is, though, dense and thus $P_{TH}\mathbb{R}^n$ cannot be complete.

Not being complete is an extremely **bad** property for a linear space to have if it wants to be a model space of an (infinite dimensional) manifold.  In particular, it means that integrals and derivatives might not exist even if the corresponding limit is Cauchy.