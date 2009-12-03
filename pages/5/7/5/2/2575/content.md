
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
#Contents#
* automatic table of contents goes here
{:toc}

#Background and history#

The words "Chern-Simons theory" can mean various things to various people, but here it generally refers to the three-dimensional [[TQFT|topological quantum field theory]] introduced by [[Edward Witten]] in his seminal paper from 1989, ["Quantum field theory and the Jones polynomial"](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.cmp/1104178138), the paper which went a large way to him obtaining the Fields medal. 

In this paper, Witten showed that the new [[knot invariant|polynomial invariant]] of [[knot]]s invented by Vaughan Jones in the context of [[von Neumann algebra]]s can be given a beautiful heuristic geometric interpretation: the [[Jones polynomial]] V(q) a knot $K$ in a 3-manifold $M$ can be viewed as the [[path integral]] over all $SU(2)$-connections on $M$ of the exponential of the [[Chern-Simons form|Chern-Simons]] [[action functional]] $S[A]$:
\[
 V_K(q) = \int_{all\,connections\,A\,on\,M} Tr Hol_A (K) exp iS[A]
\]
where
\[
S[A] = \frac{k}{4\pi} \int_M Tr (A \wedge dA + \frac{2}{3} A \wedge A \wedge A)
\]
is the integral of the  [[Chern-Simons form|Chern-Simons action]], 
\[
 Tr Hol_A (K) 
\]
is the trace of the holonomy of the connection around the knot $K$ in the fundamental representation of $SU(2)$, and  
\[
q = e^{\frac{2 \pi i}{k+2}}.
\]
Said heuristically: the [[Jones polynomial]] of the knot $K$ can be understood as the "average value" over all connections of the _trace of the holonomy of the connection_ around the knot $K$. Note that this idea can be generalized by varying the gauge group $G$ from $SU(2)$ to some other Lie group; the representation in which the trace is evaluated can also be altered. Each of these modifications gives rise to a knot invariant.  

# Viewpoint from extended topological quantum field theory#

The beautiful thing about Chern-Simons theory is that Witten was able use the _locality_ property of the [[path integral]] to give a _nonperturbative_ way to actually compute it. In this way Chern-Simons theory has become the 'poster-child' of [[extended topological quantum field theory]] since it exemplifies the main idea: take advantage of the higher gluing laws in order to compute geometric quantities. 

One of the major mathematical projects around Chern-Simons theory has therefore been to try and understand it rigorously as a 3-2-1-0 [[extended topological quantum field theory]]. For the abelian case the major paper in this regard is [Topological quantum field theories from Compact Lie Groups](http://arxiv.org/abs/0905.0731) by [[Dan Freed|Freed]], [[Mike Hopkins|Hopkins]], [[Jacob Lurie|Lurie]] and Teleman. No-one has yet made rigorous sense of the nonabelian theory as an extended [[TQFT]]. However, the invariants that the theory assigns to closed [[manifold]]s of dimension 0,1,2 and 3 are heuristically expected to be:

A closed 3-manifold $M$ $\mapsto$ the path integral given above (a number).

A closed 2-manifold $\Sigma$ $\mapsto$ the space of sections of the line bundle over the moduli space of flat [[connection on a bundle|connection]]s on $\Sigma$ (a finite-dimensional [[vector space]]).  (Reshetikhin and Turaev give an alternate quantum-groupy description of this space).

A circle $S^1$ $\mapsto$ the [[category]] of [[positive-energy representation]]s of the [[loop group]] $\Omega_k (G)$ at level $k$ (a [[linear category]]).

+-- {: .query}
The R-T construction sticks on the circle the [[modular tensor category]] of representations of a [[quantum group]] at a root of unity, modulo "unphysical representations."  Are these supposed to be the same?  Is this just the Kazhdan-Lusztig equivalence?

[[Urs Schreiber]]: the [[Reshetikhin-Turaev construction]] works with any [[modular tensor category]], I'd say. Using one coming from reps of loops group is expected to produce the Chern-Simonss QFT as a cobordism rep. But I think a full proof of that, i.e. a formalization of the CS path integral that would after turning the crank yield the RT construction, is not available to date. There is just lots of "circumstancial evidence".

=--

The 2-category assigned to the point is the most interesting piece of data since in principle all the other invariants can be derived from it using the gluing law. In the paper _Topological quantum field theories from Compact Lie Groups_, it is proposed that

A point $\mapsto$ the category of skyscraper sheaves on ---, thought of as a 2-category via ---.

+-- {: .query}
Bruce: I've run out of time here and I can't precisely fill in those blanks above.  Any help?

[[Ben Webster]]: My understanding is that nobody is quite sure how to fill in those blanks.  One line of thinking is that it should be an object in a 3-category with is **not** 2Cat.
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

> The main new idea that Witten was using was that the contributions of different critical points p (including complex ones), could be calculated by choosing   appropriate contours $\mathcal{C}_p$ using [[Morse theory]] for the Chern-Simons functional. This sort of Morse theory involving holomorphic Morse functions gets used in mathematics in [[Picard-Lefshetz theory]]. The contour is given by the downward flow from the critical point, and the flow equation turns out to be a variant of the self-duality equation that Witten had previously encountered in his work with Kapustin on [[geometric Langlands]]. One tricky aspect of all this is that the contours one needs to integrate over are sums of the $\mathcal{C}_p$ with integral coefficients and these coefficients jump at "Stokes curves" as one varies the parameter in one's integral (in this case, $x=k/n$, $k$ and $n$ are large). In his talk, Witten showed the answer that he gets for the case of the figure-eight knot.

For slides of Witten's talk, click [here](http://www.princeton.edu/~tklose/adscft/EdwardWittenPCTS.pdf) and for video, click [here](http://echo360.princeton.edu:8080/ess/echo/presentation/2730cd4e-39b0-4d97-a825-165e7d4b819f). Pilfering material from the slides, the basic idea is as follows. Consider a general oscillatory integral in $n$ dimensions:
 \[
 I(\lambda) = \int_{\mathbb{R}^n} d^n exp(i\lambda f(x_1, \ldots, x_n)).
\]
We want to make sense of the integral when the function $f$ is allowed to take on imaginary values (naively, the integral diverges). To do this, we use Morse theory: we choose as our Morse function the real part of the exponent, that is $h = \Re(i \lambda f)$. For every critical point $p$ of $h$, the descending manifold $C_p$ is an $n$-cycle in the relative homology group $H_n (X, X_{\ll0})$. (Basically this means that it's a new "contour" for the integral). Moreover Morse theory tells us that the cycles we obtain in this way form a basis for the homology, so we can express our original cycle $C$ (the $\mathbb{R}^n$ appearing in the integral over $\mathbb{R}^n$) as a linear combination of these Morse theory cycles:
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

* [Chern-Simons Gauge Theory: 20 years after](http://www.hausdorff-center.uni-bonn.de/event/2009/gauge_theory/) was a workshop at the Max Planck Institute in Bonn from 3--7 August 2009.
* (More here...)

## Geometric quantization and Chern-Simons theory?
In [Quantum field theory and the Jones polynomial](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.cmp/1104178138), Witten makes the tantalizing observation that the "trace" occuring in the "trace of the holonomy around the knot" term in the path integral should _itself_ be seen as a path integral. In this way one hopes to obtain a much more unified formalism. See [[Bruce Bartlett:Geometric quantization and the path integral in Chern-Simons theory]] (password required).   

##Chern-Simons theory and knot homology

One question that's been bugging me (Ben Webster) recently is what fills in the analogy "[[Jones polynomial]] is to Chern-Simons theory as [[Khovanov homology]] is to ??"

Which is to say _What 3/4-dimensional structure is Khovanov homology hinting at?_  I'm inclined to think there must be one, as it seems that all of the knot homologies associated by Chern-Simons theory to representations have categorifications (I have a [mostly finished paper](http://math.mit.edu/~bwebster/KI-HRT.pdf) on this).  Presumably these all glue together into something, possibly by a similar trick to the Reshetikhin-Turaev construction of 3-manifold invariants, but it's not so easy for me to see how.

## References  

Long list of references should eventually go here. For the moment there is:

* [[Dan Freed]], _Remarks on Chern-Simons theory_ ([arXiv](http://arxiv.org/abs/0808.2507))

  * _Classical Chern-Simons theory, part II_ ([pdf](http://www.ma.utexas.edu/users/dafr/cs2.pdf))