
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contens#
* automatic table of contents goes here
{:toc}


## Idea 

The **electromagnetic field** is a [[gauge field]]. A configuration of the **electromagnetic field** on a space $X$ in the _absence_ of [[magnetic charge]] is modeled by a [[cocycle]] $\hat F$ in degree 2 [[ordinary differential cohomology]].

This may be realized in particular equivalently by

* a $U(1)$-[[principal bundle]] [[connection on a bundle|with connection]] on $X$; 

* a degree 2 [[Deligne cohomology|Deligne cocycle]] on $X$.

In the presence of [[magnetic charge]] the electromagnetic field is modeled by a coycle in differential [[twisted cohomology]], where the twist is given by the differential 3-cocycle that models the [[magnetic current]].

The analogous field modeled by a degree 3 [[Deligne cohomology|Deligne cocycle]] is the [[Kalb-Ramond field]].

## History

...historical section eventually goes here..


...electricity and magnetism were discovered independently, Maxwell's equations in classical vector analysis which allows the formulation as a tensor $F$ as below, and "magnetism is a consequence of electrostatics and covariance, hence the composite noun electromagnetism"...

(...)




## Mathematical model from physical input

Physical experiment shows that the electromagnetic [[field strength]] on a pseudo-Riemannian spacetime $X$ has the following properties.

1. Maxwell's equations
  
   The electromagnetic [[field strength]] (in the absence of [[magnetic charge]]s) is given by a 2-form $F \in \Omega^2(X)$ and an [[electric current]] 3-form $j_{el} \in \Omega^3(X)$ satisfying **Maxwell's equations**

   $$
     d F = 0
   $$

   $$
    d \star F = j_{el}
   $$

   The first equation with Stokes' theorem this implies that one may find 

   * on a good [[cover]] of $X$ by open subsets $\{U_i \to X\}$ 

   * a collection $(A_i \in \Omega^1(U))_i$ of differential 1-forms, such that $d A_i = F|_{U_i}$

   * and a collection $(\lambda_{i j} \in C^\infty(U_i \cap U_j), \mathbb{R})_{i,j}$ of real valued functions on double overlaps such that $A_j|_{U_i \cap U_j} -  A_i|_{U_i \cap U_j} = d \lambda_{i j}$.


2. Dirac quantization condition

   The above data is subject to the additional constraint that it induces well-defined $U(1)$-valued holonomy -- this is **Dirac's quantization condition**, a necessary requirement for the existence of quantum mechanical particles on $X$ that are charged under the background electromagnetic field.

   Concretely: for any smooth curve $\gamma : S^1 \to X$ and any [[cover]] $\{V_i \to S^1\}$ of $S^1$ refining the pullback of the cover $U$ to $S^1$, and for every triangulation $\{v, e\}$ of $S^1$ subordinate to $\{U_i \to X\}$, i.e. such that there is an index map $\rho$ such that $\gamma(e) \subset U_{\rho(e)}$ and $\gamma(v) \subset U_{\rho(v)}$

   the expression

   $$
     hol(\gamma) :=
     \prod_v \exp(i \int_{v} \gamma^* A_{\rho(v)})
     \prod_{e} \exp(i (-1)^{\sigma_{e,v}}
       \gamma^*\lambda_{\rho(e) \rho(v)}
      (v)
   $$

   (where $\sigma_{e,v} = 1$ if $v$ is the final vertex of $e$ and $-1$ otherwise)

   -- the interaction action functional of the charge particle -- has to be a well defined element in $U(1)$ (independent of all the choice made).

   This implies in particular that cancelling from the triangulation an edge $e_i$ of vanishing length must have no effect on the formula, which in turn means that for all $i,j,k$ we have

   $$
     \exp(i \gamma^*\lambda_{i j}(v_{i j}))
     \exp(i \gamma^*\lambda_{j k}(v_{j k}))
     =
     \exp(i \gamma^*\lambda_{i k}(v_{i k}))
   $$

   and hence

   $$
     \lambda_{i j} + \lambda_{j k} =
     \lambda_{i k} mod 2\pi
     \,.
   $$


In total this says precisely that the data

$$
  (A_i, \lambda_{i j})
$$   

is a [[?ech cohomology|?ech cocycle]] with coefficients in the degree 2 [[Deligne cohomology|Deligne complex]] whose [[differential cohomology|projection to deRham cohomology]] is the given Maxwell 2-form.


The following describes more physical and historical details behind this argument.


## The local picture #

In modern notation what Maxwell discovered in the 1860s is that locally, when physical spacetime is well approximated by a patch of its tangent space, i.e. by a patch of 4-dimensional Minowski space $U \subset (\mathbb{R}^4, g = diag(-1,1,1,1))$, the electric field $\vec E = \left[ \array{E_1 \\ E_2 \\ E_3} \right]$ and magnetic field $\vec B = \left[ \array{B_1 \\ B_2 \\ B_3} \right]$ combine into a differential [[differential form|2-form]]

$$
  \begin{aligned}
    F & := E \wedge d t + B
      \\
      &:= 
        E_1 d x^1 \wedge d t + 
        E_2 d x^2 \wedge d t + 
        E_3 d x^3 \wedge d t  
     \\
      & +
        B_1 d x^2 \wedge d x^3 +
        B_2 d x^3 \wedge d x^1 +
        B_3 d x^1 \wedge d x^2
  \end{aligned}
$$

in $\Omega^2(U)$ and the [[electric charge]] density and current density combine to a differential 3-form

$$
\begin{aligned}
    j_{el} &:= j\wedge dt - \rho d x^1 \wedge d x^2 \wedge d x^3 \\
& :=    j_1 d x^2 \wedge d x^3 \wedge d t +
        j_2 d x^3 \wedge d x^1 \wedge d t +
        j_3 d x^1 \wedge d x^2 \wedge d t
        -
        \rho \; d x^1 \wedge d x^2 \wedge d x^3
\end{aligned}
$$
 
in $\Omega^3(U)$ such that the following two equations of differential forms are satisfied

$$
  \begin{aligned}
    d F = 0
    \\
    d \star F  = j_{el}
  \end{aligned}
  \,,
$$

where $d$ is the de Rham differential operator and $\star$ the [[Hodge star]] operator. If we decompose $\star F$ into its components as before as 

$$
\begin{aligned}
\star F 
&= -D + H\wedge dt \\
&= -D_1 \; d x^2 \wedge d x^3 
   -D_2 \; d x^3 \wedge d x^1
   -D_3 \; d x^1 \wedge d x^2
     \\
     & +
     H_1 \; d x^1 \wedge d t
     +
     H_2 \; d x^2 \wedge d t
     +
     H_3 \; d x^3 \wedge d t
  \end{aligned}
$$

then in terms of these components the filed equations -- called **Maxwell's equations** -- read as follows.

$d F = 0$

* **magnetic Gauss law**: $div B = 0$

* **Faraday's law**: $\frac{d}{d t} B + rot E = 0$

$d \star F = 0$

* **Gauss' law**: $div D = \rho$

* **Amp&#232;re's law** $- \frac{d}{d t} D + rot H = j_{el}$


## The global picture ##

Maxwell's original equations determine what the 
electromagnetic field is _locally_. After a while it was dicovered that globally the situation is more complicated.

* First Einstein figured out that in the presence of a gravitational field spacetime is not in general globally given by [[Minkowski space]], but may be given by a more general [[Lorentzian manifold]].

With the differential geometry sorted out, there is an obvious generalizaton of Maxwell's equations from Minkowski space to an arbitrary [[Lorentzian manifold]]. 

In the modern notation

$$
  \begin{aligned}
    d F = 0
    \\
    d \star F  = j_{el}
  \end{aligned}
$$

already holds unmodified in this case, too.

But this still turns out to be too naive. While 
it is true that the equations do generalize in this way in princple, another physical effect discovered later may prevent them from generalizing this way in every case.

This happens when the manifold in question has nontrivial topology, or if there is magnetic charge around.

* Dirac discovered that the existence of magnetically charged quantum mechanical particles implies that

  * a) the electromagnetic field strength 2-form $F$ is required to have integral cycles (in some normalization);

  * b) moreover, the electromagnetic field is not just encoded in $F$, but in a degree 2 [[differential cohomology|differential refinement]] of integral cohomology -- for instance thought of as a $U(1)$-[[principal bundle]] [[connection on a bundle|with connection]], of which $F$ is only the image in deRham cohomology (the curvature 2-form).

The reasoning underlying Dirac's argument is described in the next subsection.


### The quantization condition ###

In this section we describe how one finds from physical arguments that, indeed, the electromagnetic field is modeled by a differential refinement of an cocycle in degree 2 integral cohomology.

A central idea in this argument is famously due to Dirac. He thought of it as an argument for the quantization of [[margnetic current|magnetic charge]] (DR: surely this should be electric charge :-). But from a modern perspective he identified the magnetic (DR: electric?) charge with the _Chern class_ of the line bundle with connection that represents the electromagnetic field outside of the support of the magnetic charge distribution.

The **experimental input from physics** 
is the following

1. **Maxwell's equations**  say that, at least locally on contractible patches $U \subset X$ of the underlying space(time), the electromagnetic field in the absence of magnetic current is encoded by a closed smooth 2-form $F \in \Omega^2(U)$ -- as described above. Poincar&#233;'s lemma implies then that there is a smooth 1-form $A \in \Omega^1(U)$ such that $F = d A$.

1. The **Lorentz force law** implies that the _action functional_ of an electrically charged particle is the functional that assigns to each local trajectory, i.e. to each path 
   $$
     \gamma : [0,1] \to U \subset X
   $$
   the integral of $A$ along this path
   $$
     \gamma \mapsto S_{int}(\gamma) \propto \int_{[0,1]} \gamma^* A
   $$
   at 
   (Here "$int$" is for INTeraction: the interaction of the particle with the back electromagnetic field. There are other contributions to the particle's action, such as the kinetic contribution, which are not considered here).

1. The classical mechanics of the particle subject to the force of the electromagnetic background field only depends on the critical points of this action functional. These critical points are the trajectories that satisfy the Lorentz force law and depend not on the choice of $A$ but only on the field strength $F = d A$.

   **But** when one considers the **quantum theory** of the electrically charged particle in the background field of classical electromagnetism, one is to perform the [[path integral]] over the _exponentiated_ action functional. For that to make any sense at all, the exponentiated action functional
   $$
    \gamma \mapsto \exp( i c \int_{[0,1]} \gamma^* A )
   $$
   has to be a well-defined function of $\gamma$, for some real constant $c$.
   What is more, since contrary to the computation of the classical equations of motion this cannot be restricted to local paths, there must be some assignment
   $$
     tra :   X^{[0,1]} \to U(1)
   $$
   from all paths in $X$ to unimodular complex numbers that is well defined, and is locally given by the above formula, for some choice of $A$. 

1. Moreover, by the **sewing law** or **locality** of the path integral the assignment $tra : X^{[0,1]} \to U(1)$ must respect composition of paths in that for 
$\gamma_1 : [0,1/2] \to X$ and $\gamma_2 : [1/2,1] \to X$ 
the restrictions of $\gamma$ to the left and the right half of the interval, we have
   $$
     tra(\gamma_2)\cdot tra(\gamma_1) = tra(\circ\gamma_1)
     \,.
   $$


In **summary** this says that the interaction part of the exponentiated action of the electrically charged in the background of an electromagnetic field in the absence of magnetic current is

* functor from the [[path groupoid]] to the [[delooping]] [[groupoid]] $\mathbf{B} U(1)$ of the [[group]] $U(1)$:
  $$
    tra : P_1(X) \to \mathbf{B} U(1)
  $$
  which depends smoothly on paths for fixed endpoints (not if the endpoints are allowed to move) is such that locally it is given by the above formula in terms of some 1-form $A$ with $d A = F$ the prescribed electromagnetic field. 

As described at [[path groupoid]] and at [[connection on a bundle]], this does encode a $U(1)$-[[principal bundle]] with connection, i.e. a differential refinement degree 2 integral cohomology.

There are other slight variants of formalizations the above physical input that yield or come close to yield this same information.

* Dirac in his original original argument considered the above problem for the special case of $X = S^3$ the 3-sphere and derived from this that the field strength 2-form $F \in \Omega^2(X)$ must have integral cycles. This at least finds the crucial [[differential cohomology|differential cohomological]] quantization condition for that special case.

* As recalled in the history section at [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]] an old result by Barrett and others shows that the restriction of $tra$ to based closed paths, assuming only that it is a smooth map on the space of such loops, is already sufficient to deduce that it defines a $U(1)$-[[principal bundle]] [[connection on a bundle|with connection]].


* More manifestly, with a little more work one may extract from the above setup the fact that the value of $tra : X^{[0,1]} \to U(1)$ on contractible _closed_ paths, i.e. on contractible loops $\gamma(0) = \gamma(1)$ in $X$, must be determined by the integral of the 2-form $F$ over any surface $\Sigma : D^2 \to X$ with boundary $\partial \Sigma = \gamma$ in $X$ by
  $$
    tra(\gamma) = \exp(i c  \int_{D^2} \Sigma^* F )
    \,.
  $$
  Locally this is just the Stokes theorem.

  In this form now, the object $tra$ manifestly satisfies the axioms of a [[Cheeger-Simons differential character]]. These are well known to represent cocycle in degree 2 integral [[differential cohomology]].


### Dirac's original argument ###

Dirac originally presented the following reasoning, which captures the main point of the above considerations.

He considered $X$ to be $\mathbb{R}^3$ without the origin, 
$$
  X := \mathbb{R}^3 \backslash \{0\}
  \,,
$$ 

which is a manifold of the topology of the 3-sphere $S^3$.

He imagined a situation with a magnetic charge supported on the point located at the origin and removed that point in order to keep the field strength $F$ to be a _closed_ 2-form on all of $X$. 

(Indeed,  if one does not remove the support of magnetic charge, the argument becomes much more sophisticated and involves higher differential cocycles given by [[bundle gerbe]]s. This was not understood before Dan Freed's
[Dirac charge quantization and generalized differential cohomology](http://arxiv.org/abs/hep-th/0011220).)

Then he considered a single coordinate patch

$$
  U := \mathbb{R}^3 \backslash \{x^1 \geq 0\} \subset X
$$

given by $X$ minus the right half of the first coordinate axis. 

Traditionally physicist try to give that half-line a physical interpretation by imagining that it is the body of an idealized infinitely-thin and to one side infinitely-long solenoid. Indeed, such a solenoid would have a magnetic monopole charge on each of its ends, so if the one end is imagined to have disappeared to infinity, then the other one is the magentic charge that Dirac imagines to sit at the origin of our setup.

In this context the half-line $\{x^1 \geq 0\}$ is called a **Dirac string**. While there is the possibility to sensibly discuss the idea that this Dirac string actually models a physical entity like an idealized solenoid, its main purpose histroically is to confuse physics students and keep them from understanding the theory of [[fiber bundle]]s. Therefore here we shall refrain from talking about Dirac strings and consider $U := \mathbb{R}^3 \backslash \{x^1 \geq 0\} \subset X$ as exactly what it is, by itself: an open subset that is part of a [[cover]] of $X$.  Unfortunately, of course, Dirac didn't mention the other open subsets in that [[cover]] (at least one more is needed for a decent discussion), so that the Dirac string keeps haunting physicists. 

...running out of time...just quickly now...

...Dirac effectively considered the overlap cocycle condition $A_j - A_i = something$, found that by the requirement that $A$ has well defined holonomy it follows that there must be $g_{ij}$ a function with values in $U(1)$ such that  $A_j - A_i = d log g_{ij}$, then did away with the $j$-patch (considering a kind of limit as we encircle the half axis) and concluded that $A$ must be the log-differential of a $U(1)$-valued function, whose winding number around the half-axis he identified with the magnetic charge, which in terms of bundles one identifies with the Chern-class of the bundle in question ... 

...have to run...

#Geometric origins of inhomogeneous media#

>This section is tentative and probably even controversial. By no means is it generally accepted to be correct, but it is worth writing down if for no other reason than to elicit disagreement in which case we'd learn something.

As inhabitants of the earth, we all sit in a bath of electromagnetic radiation, both man made and natural. This radiation permeates our bodies which are made up of dielectric, magnetic, and conducting materials, i.e. body tissue. Just as geometry is encoded in the metric tensor and manifests itself via the Hodge star, so too do the electromagnetic constitutive equations. For example, in linear media we have the simple constitutive relations

$$E = \frac{1}{\epsilon} D \quad\text{and}\quad B = \mu H.$$

In 4d, we have

$$F = B + E\wedge dt$$

The 4d constitutive relation is 

$$G = \star F,$$

which under assumptions of linearity gives

$$\star F = -\eta(D-H\wedge dt),$$

where $\eta = \sqrt{\frac{\mu}{\epsilon}}$. This may be written in a form that more closely mimics the tradition relations via

$$\star(v dt\wedge E) = \frac{1}{\epsilon} D\quad\text{and}\quad\star B = \mu H\wedge v dt,$$

where $v = \frac{1}{\sqrt{\mu\epsilon}}$ (Note: $v = c$ in vacuum). For more details see [page 111](http://ncatlab.org/ericforgy/show/Dissertation).

What this means is the the electromagnetic properties of matter can be interpreted geometrically and are encoded in the Hodge star. Conversely, it means that geometrical properties of matter can be interpreted electromagnetically.

# References #

Maxwell's equations originate in

* James Clerk Maxwell, _[A Dynamical Theory of the Electromagnetic Field](http://en.wikipedia.org/wiki/A_Dynamical_Theory_of_the_Electromagnetic_Field),_ Philosophical Transactions of the Royal Society of London 155, 459--512 (1865).

Dirac's quantization argument appeared in

* P.A.M. Dirac _Quantized Singularities in the Electromagnetic Field_,  Proceedings of the Royal Society, A133 (1931) pp 60--72.

* [Differential Forms in Electromagnetic Theory](http://eceformsweb.groups.et.byu.net/forms-home.html)

#Discussion#

+--{.query}

[[Eric]]: Once a query box gets more than a few lines long, it becomes difficult to read, so I'm removing the query box. Hope that's alright.

=--

(From [[latest changes]])

[[Urs]]: Eric, why don't you make the material on electromagnetism in media that you added into a proper section at [[electromagnetic field]]? Then we could move what is proper discussion between us into a query box, after all, while having the genuine material visible in the netry and not hidden in the section Discussion.

[[Eric]]: I've thought about this some more and something still bothers me about the idea. If electromagnetic properties, i.e. $\mu$, $\epsilon$, $\sigma$ can be geometrically incorporated into the Hodge star via the metric, this implies: 1.) Maxwell's equations in inhomogeneous media are _wrong_ (although in vacuum they reduce to the familiar form) and 2.) that the Hodge star should involve _convolution_, i.e. the metric should have a _memory_. Has anyone put forward any serious theories of a "metric with memory"? Asking that questions give me a sense of deja vu (getting old sucks).


***

[[Eric]]: I remember the first time I saw you discuss EM theory in this context. It, at first, seems like a good motivation for more general concepts, but then, as now, a second wave of doubt crossed my mind. Throughout this article, there is no mention of any physical question as to the existence of magnetic charges. Do we just take their existence for granted? If magnetic charges do not exist, is this a good motivating example for more general concepts? If we were paranoid, we could then start asking if we were on a wild goose chase.

> [[Urs Schreiber]]: but so far the article explicitly excludes magnetic charges! It is true that Dirac imagined a magnetic charge to have been where he then removes a point, but that you have to fight out with Dirac, not with me :-)

> The real point about including magnetic charges is that taking them into account one gets the more complete formal picture of differential cocyclic description of higher gauge fields. This is crucial for the discussion of effects like the [[Green-Schwarz mechanism]], where it is explicitly a (higher) magnetic charge that is introduced in order to cancel a fermion anomaly. You are free to think that none of this is related to observable physics until proven otherwise, but it is an interesting differential cohomological effect which deserves to be discussed here in more detail, eventually.

There are two other topological/geometrical aspects of EM theory worth mentioning. One is the hypothetical "perfect electrical conductor". Consider a perfectly conducting sphere. This will trace out a tube in spacetime. I might have the details slightly confused because its been a while since I've thought about this, but you can model perfect conductors via nontrivial topology, i.e. you remove the sphere and its world volume from spacetime. Let me say that again a different way and maybe one of the ways will make sense. 

>Removing a world volume from spacetime is equivalent to introducing a perfectly conducting body.

There has got to be something interesting category theory can say about this. Perhaps you can relate it to "relative cohomology" or something.

Another thing that might be worth mentioning is the geometric character of material properties. After all, we all sit in a bath of electromagnetic radiation, both man made and natural. This radiation permeates our bodies which are made up of dielectric, magnetic, and conducting materials, i.e. body tissue. I always found it interesting that just as geometry is encoded in the metric and manifests itself via the Hodge star, so too do the constitutive equations. For example, in linear media we have the simple constitutive equations

$$E = \frac{1}{\epsilon} D \quad\text{and}\quad B = \mu H.$$

In 4d, we have

$$F = B + E\wedge dt$$

The 4d constitutive relation is 

$$G = \star F,$$

which under assumptions of linearity gives

$$\star F = -\eta(D-H\wedge dt),$$

where $\eta = \sqrt{\frac{\mu}{\epsilon}}$. This may be written in a form that more closely mimics the tradition relations via

$$\star(v dt\wedge E) = \frac{1}{\epsilon} D\quad\text{and}\quad\star B = \mu H\wedge v dt,$$

where $v = \frac{1}{\sqrt{\mu\epsilon}}$ (Note: $v = c$ in vacuum). For more details see [page 111](http://ncatlab.org/ericforgy/show/Dissertation).

What this means is the the electromagnetic properties of matter can be interpreted geometrically and are encoded in the Hodge star.

It would be nice to see the importance of the Hodge star amplified a bit.

[[Bruce Bartlett]]: I agree with Eric on the importance of the Hodge star in electromagnetic properties of matter. For one thing, this is now borne out in the whole field of cloaking! See for instance section 2.1 and appendix A of [this paper](http://arxiv.org/abs/cond-mat/0607418). There was a fantastic reference on this (supplementing Eric's appendix in his thesis) which I came across on the net somewhere, some kind of dissertation/write-up about differential forms and electromagnetic properties of matter. I wish I could find it again. To summarize: the "differential forms" / "Hodge star" picture of electromagnetism is the most convenient way to understand the "D" and "H" fields as well. 

[[Eric]]: Hi Bruce. I'm guessing you might be talking about either Karl Warnick or Fernando Teixeira. Both are good friends of mine from grad school. I added a reference above to some of Karl's old stuff:

* [Differential Forms in Electromagnetic Theory](http://eceformsweb.groups.et.byu.net/forms-home.html)

The cloaking stuff is interesting. When I was in grad school, it was known how to "perfectly absorb" electromagnetics waves for sources inside a close surface, but it was thought to be impossible to perfectly absorb electromagnetic wave for a source outside a closed surface, which is what one probably means when they talk about "cloaking". I'm skeptical, but open.

I would be remiss not to mention an unofficial mentor of mine, i.e. someone whose work I've always admired greatly, Alain Bossavit. It could very well have been some of his earlier papers you're thinking about.

By the way, Bruce, after glancing at that paper, you might find a comment I recently made at the n-Forum [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=1034&Focus=7775#Comment_7775) interesting. In grad school, I simulated a 1-dimensional event horizon as a potential boundary condition for electromagnetic simulations. It is pretty fun :) I don't think it is a secret that you can map various solutions of Einstein's field equations to analogous electromagnetic media in flat Minkowski space. The analogy between geometry and media is deeper than the attention it receives would suggest.