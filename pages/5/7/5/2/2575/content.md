
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
#Contents#
* automatic table of contents goes here
{:toc}

#Background and history#

The words "Chern-Simons theory" can mean various things to various people, but here it generally refers to the three-dimensional [[TQFT|topological quantum field theory]] introduced by [[Edward Witten]] in his seminal paper from 1989, ["Quantum field theory and the Jones polynomial"](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.cmp/1104178138), the paper which went a large way to him obtaining the Fields medal. 

In this paper, Witten showed that the new [[knot invariant|polynomial invariant]] of [knot]]s invented by Vaughan Jones in the context of [[von Neumann algebra]]s can be given a beautiful heuristic geometric interpretation: the [[Jones polynomial]] V(q) a knot $K$ in a 3-manifold $M$ can be viewed as the [[path integral]] over all $SU(2)$-connections on $M$ of the exponential of the [[Chern-Simons|Chern-Simons form]] [[action functional]] $S[A]$:
\[
 V_K(q) = \int_{all\,connections\,A\,on\,M} Tr Hol_A (K) exp iS[A]
\]
where
\[
S[A] = \frac{k}{4\pi} \int_M Tr (A \wedge dA + \frac{2}{3} A \wedge A \wedge A)
\]
is the [[Chern-Simons action|Chern-Simons form]], 
\[
 Tr Hol_A (K) 
\]
is the trace of the holonomy of the connection around the knot $K$ in the fundamental representation of $SU(2)$, and 
and 
\[
q = e^{\frac{2 \pi i}{k+2}}.
\]
Said heuristically: the [[Jones polynomial]] of the knot $K$ can be understood as the "average value" over all connections of the _trace of the holonomy of the connection_ around the knot $K$. Note that this idea can be generalized by varying the gauge group $G$ from $SU(2)$ to some other Lie group; the representation in which the trace is evaluated can also be altered. Each of these modifications gives rise to a knot invariant.  

# Viewpoint from extended topological quantum field theory#

The beautiful thing about Chern-Simons theory is that Witten was able use the _locality_ property of the [[path integral]] to give a _nonperturbative_ way to actually compute it. In this way Chern-Simons theory has become the 'poster-child' of [[extended topological quantum field theory]] since it exemplifies the main idea: take advantage of the higher gluing laws in order to compute geometric quantities. 

One of the major mathematical projects around Chern-Simons theory has therefore been to try and understand it rigorously as a 3-2-1-0 [[extended topological quantum field theory]]. For the abelian case the major paper in this regard is [Topological quantum field theories from Compact Lie Groups](http://arxiv.org/abs/0905.0731) by Freed, Hopkins, [[Jacob Lurie|Lurie]] and Teleman. No-one has yet made rigorous sense of the nonabelian theory as an extended [[TQFT]]. However, the invariants that the theory assigns to closed [[manifold]]s of dimension 0,1,2 and 3 are heuristically expected to be:

A closed 3-manifold $M$ $\mapsto$ the path integral given above (a number).

A closed 2-manifold $\Sigma$ $\mapsto$ the space of sections of the line bundle over the moduli space of flat [[connection on a bundle|connection]]s on $\Sigma$ (a finite-dimensional [[vector space]]).

A circle $S^1$ $\mapsto$ the [[category]] of [[positive-energy representation]]s of the [[loop group]] $\Omega_k (G)$ at level $k$ (a [[linear category]]).

The 2-category assigned to the point is the most interesting piece of data since in principle all the other invariants can be derived from it using the gluing law. In the paper _Topological quantum field theories from Compact Lie Groups_, it is proposed that

A point $\mapsto$ the category of skyscraper sheaves on ---, thought of as a 2-category via ---.

+-- {: .query}
Bruce: I've run out of time here and I can't precisely fill in those blanks above.  Any help?
=--

Other groups have conceptualized this differently (but most likely equivalently at the end of the day as)

A point $\mapsto$ the 2-category of unitary [[2-representation]]s of the [[group]] $G$.

Still others think of the [[2-category]] assigned to the [[point]] in different terms.

# Other features of Chern-Simons theory#

We have only focused on the "purely [[higher category theory|n-categorical]]" aspects of Chern-Simons theory so far and ignored hundreds of tremendously important topics, such as: 

* The idea of [[transgression]], and the significance of the [[Chern-Simons form]]
* Chern-Simons theory as a [[string theory]]
* Large $N$ duality
* The [[BV-theory|Batalin-Vilkovisky]] viewpoint
* Much more...

But there are two other recent features of Chern-Simons theory which I would personally (Bruce Bartlett) like to mention.

## Chern-Simons theory and modular forms

Trying to interest your [[number theory]] friends with Chern-Simons theory? How about this: the Chern-Simons [[path integral]] $Z(k)$ above is (in a certain precise sense) a _[[modular form]]_. This correspondence between the Chern-Simons quantum invariants and [[modular form]]s sheds light in both directions, and is a fascinating idea to [[Bruce Bartlett|me]]. The key words here (which I don't understand) are "Eichler integral" and  "mock theta function". See:

* Lawrence and Zagier, Modular forms and quantum invariants of 3-manifolds, Asian Journal of Mathematics vol 3 no 1 (1999).

* Hikami, Quantum invariant, modular forms, and lattice points, [arXiv](http://arxiv.org/abs/math-ph/0409016). See also the follow ups to this paper. 

## The Morse theory of Chern-Simons theory

In a recent [talk](http://www.math.columbia.edu/~woit/wordpress/?p=2357), Witten outlined a new approach to Chern-Simons theory which perhaps gives an alternative nonperturbative definition of the [[path integral]]. Quoting from [Not Even Wrong](http://www.math.columbia.edu/~woit/wordpress/?p=2357):

> The main new idea that Witten was using was that the contributions of different critical points p (including complex ones), could be calculated by choosing   appropriate contours $\mathcal C_p$ using [Morse theory]] for the Chern-Simons functional. This sort of Morse theory involving holomorphic Morse functions gets used in mathematics in [[Picard-Lefshetz theory]]. The contour is given by the downward flow from the critical point, and the flow equation turns out to be a variant of the self-duality equation that Witten had previously encountered in his work with Kapustin on [[geometric Langlands]]. One tricky aspect of all this is that the contours one needs to integrate over are sums of the $\mathcal C_p$ with integral coefficients and these coefficients jump at "Stokes curves" as one varies the parameter in one's integral (in this case, $x=k/n$, $k$ and $n$ are large). In his talk, Witten showed the answer that he gets for the case of the figure-eight knot.

For slides of Witten's talk, click [here](http://www.princeton.edu/~tklose/adscft/EdwardWittenPCTS.pdf) and for video, click [here](http://echo360.princeton.edu:8080/ess/echo/presentation/2730cd4e-39b0-4d97-a825-165e7d4b819f). Pilfering material from the slides, the basic idea is as follows. Consider a general oscillatory integral in $n$ dimensions:
 \[
 I(\lambda) = \int_{\mathbb{R}^n} d^n exp(i\lambda f(x_1, \ldots, x_n)).
\]
We want to make sense of the integral when the function $f$ is allowed to take on imaginary values (naively, the integral diverges). To do this, we use Morse theory: we choose as our Morse function the real part of the exponent, that is $h = \Re(i \lambda f)$. For every critical point $p$ of $h$, the descending manifold $C_p$ is an $n$-cycle in the relative homology group $H_n (X, X_{&lt; &lt; 0})$. (Basically this means that it's a new "contour" for the integral). Moreover Morse theory tells us that the cycles we obtain in this way form a basis for the homology, so we can express our original cycle $C$ (the $\mathbb{R}^n$ appearing in the integral over $\mathbb{R}^n$) as a linear combination of these Morse theory cycles:
 \[
 C = \sum_p n_p C_p
\]
In this way we can make sense of the integral $I$ by {\em defining} it as the integral over these new cycles ("contours"): 
\[
 I(\lambda)  = \sum_{\text{crit. points} p} n_p I_p(\lambda)
\]
This new definition actually converges, and makes sense. Apparantly the same technique can be used to interpret the Chern-Simons path integral in the case of complex $k$. Witten argues that this viewpoint is useful if we try to interpret Chern-Simons theory as a theory of three-dimensional gravity, 

## Chern-Simons theory: 20 years on

This year marked the 20th anniversary of Witten's seminal paper _Quantum field theory and the Jones polynomial_ and there were a number of conferences marking this event. If anyone has notes for these conferences please say so, I ([[Bruce Bartlett|Bruce]]) would be very grateful!

* [Chern-Simons Gauge Theory: 20 years after](http://www.hausdorff-center.uni-bonn.de/event/2009/gauge_theory/) was a workshop at the Max Planck Institute in Bonn from 3-7 August 2009.
* (More here...)

## Geometric quantization and Chern-Simons theory?
+-- {: goal}
[[Bruce Bartlett]]: This connection between geometric quantization and the Chern-Simons path integral which I've laid out below is something I've been mulling about for some time. If anyone is interested in working on this, please contact me.
=--
On page 22 of  [Quantum field theory and the Jones polynomial](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.cmp/1104178138), Witten remarks:

> However, there is a much better way to quantize the Chern-Simons theory with static charges... A useful point of view is the following. A representation $R_i$ of a group $G$ should be seen as a quantum object. This representation should be obtained by quantizing a classical theory. The Borel-Weil-Bott theorem gives a canonical way to exhibit for every irreducible representation $R$ of a compact group $G$ a problem in classical physics, with $G$ symmetry, such that the quantization of this classical problem gives back $R$ as the quantum Hilbert space. One introduces the [[flag manifold]] $G/T$, with $T$ being a maximal torus for $G$, and for each representation $R$ one introduces a symplectic structure $\omega_R$ on $G/T$, such that the quantization of the classical phase space $G/T$, with the symplectic structure $\omega_R$, gives back the representation $R$. Many aspects of representation theory find natural explanations by thus regarding representations of groups as quantum objects that are obtained by quantization of classical phase spaces. 

Then he makes the following fascinating comment:

> Finally, let us note that the Borel-Weil-Bott theorem should not be used simply as a tool in quantization. It should be built into the three-dimensional description. One should use the theorem to replace the Wilson lines that appear above with a functional integral over maps of the circle $S^1$ into $G/T$ (or actually an integral over sections of a $G/T$ bundle, twisted by the restriction to $S^1$ of the $G$-bundle $E$). This gives a much more unified formalism.

It would be great to work this out explicitly (any takers?). The point that Witten is making is that in a path integral, one is supposed to integrate over classical quantities in order to arrive at a quantum quantity. But the "trace of the holonomy" term in the path integral above is _already_ a quantum quantity! In fact, this trace should be viewed _itself_ as a path integral in its own right - an integral over loops in the flag manifold.  This brings us into the realm of "equivariant index theory" such as in Chapter 6-8 of ["Heat kernels and Dirac operators"](http://books.google.co.za/books?id=_e2FjvLbO94C&dq=berline+getzler+heat+kernels&printsec=frontcover&source=bl&ots=noleO0BvDl&sig=26LzgZqUnGwxsdklAXbccmws7l0&hl=en&ei=a4HoStOcMeShjAf-sZS4CA&sa=X&oi=book_result&ct=result&resnum=1&ved=0CAwQ6AEwAA#v=onepage&q=&f=false) by Berline, Getzler and Vergne. So now the Chern-Simons path integral for a knot consists of two integrals: one over all connections, and the other over all loops in the flag manifold. Set in its naked geometric context like this, there are bound to be new insights. For instance, _perhaps we can change the order of integration_. 

Similar sentiments can be found on page 10 of Atiyah's original math paper on TQFT, ["Topological quantum field theories"](http://www.springerlink.com/index/365574223623W045.pdf):

> The question now arises as to the origin of the vector space $V$, the Hilbert space of the quantum theory (Bruce: in our case, this refers to the representation vector space in which we take the trace). A standard way to get the quantum Hilbert space is first to give a classical symplectic manifold (or phase space) and then to quantize this. In particular an interesting class of examples arise  from _compact Lie groups_ $G$ and their homogenous symplectic manifolds; these are coadjoint orbits, generically copies of the flag manifold. If we take "integral" orbits for which the symplectic structure comes from a line bundle, then quantizing leads to the irreducible representations $V$ of $G$. This is the physical interpretation of the Borel-Weil theorem which is usually formulated in algebraic-geometric language. _The Lagrangian of these theories is the classical action (holonomy of the line bundle)._ (italics addded).

In other words, once express the Chern-Simons path integral for a knot into its bare-bones geometric components, _even the trace itself_ is the path integral of a holonomy of a line bundle! The whole thing is one big holonomy. This ties in with of Urs Schreiber and Konrad Waldorf (see for instance [this paper](http://arxiv.org/abs/0802.0663) ) . 

+-- {: .query}
Bruce: Urs, I'm talking about how when you explained to me how the "trace" appearing in the path integral should be interpreted in terms of holonomy, and that 1 dimension higher, we need to take the trace over a surface, like in your paper with Konrad. 
=--

