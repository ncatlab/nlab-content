
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


#Contents#
* table of contents
{: toc}


### Introduction ###

Let $M$ be a finite dimensional [[smooth manifold]]. Its [[smooth
loop space]], $L M \coloneqq C^{\infty}(S^{1},M)$, is an example of a [[mapping space]] and is one of the simplest and most
commonly encountered mapping spaces. It has many interesting
submanifolds: some are defined by *coincidences*, such as the
[[based loop space]], and others are defined by considering fixed
point sets of the natural circle action. An extremely useful tool
when studying a submanifold is a [[tubular neighbourhood]]. Not all submanifolds have tubular neighbourhoods, so it is good to
establish some results that establish that they exist. The
situation for coindicence submanifolds is considered in [[tubular
neighbourhood of a mapping space]]. Here we shall consider
submanifolds defined by the circle action.

Although in the above we concentrated on the loop space, these
results generalise to more general mapping spaces.

+-- {: .num_theorem}
###### Theorem ######
Let $E \to B$ be a fibre bundle with typical fibre $S$. Suppose
that $E$ is compact, and that $S$ has a measure such that the
transition functions are measure-preserving. Consider the
submanifold of $C^{\infty}(E,M)$ of maps $E \to M$ which are
constant on the fibres of $E \to B$. Then this submanifold has a
tubular neighbourhood which is invariant under fibrewise
measure-preserving diffeomorphisms of $E \to B$.
=--

As a corollary of this, $G \subseteq S^{1}$ is a compact subgroup
then the fixed point set $L M^{G}$ is a submanifold of $L M$ with an [[equivariant tubular neighbourhood]].

This theorem is itself a corollary of a more specific situation
where the base consists of a single point. In this case, we
consider maps $S \to M$ and look at the submanifold of constant
maps. We construct a tubular neighbourhood for this that is
invariant as described, and the invariance allows us to extend
the result to the more general situation.

The construction of the tubular neighbourhood depends on the
existence of a *local averaging* function. This should be
compared with the [[local addition]] which was needed to
construct the [[manifold structure of mapping spaces|manifold
structure]] on the mapping space in the first place. A *local
addition* is a way of saying: if two points are close, we can
move one of them to the other. A *local averaging* function
generalises this to a family of points indexed by some group and
says that if such a family is close then we can move all of them
towards each other in an equivariant fashion.

The reason that this is needed is because we want to define what
it means for a map to be close to one in the fixed point set. The
simplest case is where the source is a two point set, say
$\{1,-1\}$. We want to say what it means for a map $\{1,-1\} \to
M$ to be "close" to a constant map, but we want to say this in
such a way that if we swap the labels, nothing changes.

### A Local Averaging Function ###

The crucial ingredient in this is what we call a *local averaging
function*. For a local averaging function, we need to be able to
take a smooth map $\alpha \colon S \to M$ which is "small" in
some sense, and define a single point in $M$ which is the
"average" of $\alpha$. This should invariant under the action of
measure-preserving diffeomorphisms of $S$ on $\alpha$.

Let us illustrate this with $S = \{1,-1\}$. So we have $\alpha
\colon \{1,-1\} \to M$, which means two points $a_{1}, a_{-1} \in
M$. We need to give a general rule as to how to move them
together to a point $a_{0} \in M$ with the property that if we
swap $a_{1}$ and $a_{-1}$ then we produce the same point. Once we
have $a_{0}$ we can use a local addition (based at $a_{0}$) to
move both $a_{1}$ and $a_{-1}$ towards it. This will be invariant
under the group action because it only depends on the points
$a_{1}$ and $a_{-1}$ and not on the labels.
Thus the key is to find $a_{0}$, the "average" of $a_{1}$ and
$a_{-1}$. If $M = \mathbb{R}^{n}$ then there is an obvious such
point: $\frac{1}{2}a_{1} + \frac{1}{2}a_{-1}$. However, this will
not work on $M$ because the sum does not make sense. A local
addition could solve this, except that a local addition requires
a choice of point and that is precisely what we are trying to
avoid.

Our solution is to put $M$ inside $\mathbb{R}^{n}$. In
$\mathbb{R}^{n}$, we can form $a_{0} \coloneqq \frac{1}{2}a_{1} +
\frac{1}{2}a_{-1}$. However, the point $a_{0}$ may not lie on
$M$, so we need a way to return it to $M$. We can do that if we
know that $a_{0}$ is in a tubular neighbourhood of $M$. Then
having found $a_{0}$, we can use a local addition at $a_{0}$ to
move $a_{1}$ and $a_{-1}$ together.

There is one more subtlety. As we move $a_{1}$ and $a_{-1}$
together, we want to ensure that their "average" point stays at
$a_{0}$. That is, we need to ensure that the local addition and
the local average are independent. To see that this is a
reasonable thing, note that the local addition is defined using
the tangent space of $M$ whilst the tubular neighbourhood uses
the normal bundle of the embedding. Thus their effects should be
separable. To make this concrete, we use the orthogonal structure
on the ambient Euclidean space.

Thus we start with an embedding of $M$ in some Euclidean space,
say $\iota \colon M \to \mathbb{R}^{n}$. Then $d_{p} \iota \colon
T_{p} M \to T_{\iota(p)} \mathbb{R}^{n}$ embeds $T_{p} M$ in
$T_{\iota(p)} \mathbb{R}^{n}$. Using the orthogonal structure on
$\mathbb{R}^{n}$, we can form the [[orthogonal complement]] of $T_{p}
M$ in $T_{\iota(p)} \mathbb{R}^{n}$. Let us write this as
$N_{p}$. Then $N_{p}$ is the fibre of the normal bundle of the
embedding at $p$.

Let us identify $M$ with its image. Let us also identify $T_{x}
\mathbb{R}^{n}$ with $\mathbb{R}^{n}$ except that we translate it
so that the origin lies at $x$. The identification of $M$ with
its image also allows us to identify $T_{p} M$ and $N_{p}$ with
their images in $T_{p} \mathbb{R}^{n}$, and thus with their
images in $\mathbb{R}^{n}$. They are then affine spaces anchored
at $p$ and are orthogonal (once the translation is taken into
account).

Our first task is to construct a tubular neighbourhood. From the
above, we have a map $\nu \colon N \to \mathbb{R}^{n}$ which
restricts on the zero section to the inclusion of $M$. At the
zero section, the derivative of this map is the identification of
$T_{p} M \oplus N_{p}$ with $T_{p} \mathbb{R}^{n}$. As this is an
isomorphism, the [[inverse function theorem]] comes in to play
and says that there is a neighbourhood $W$ of the zero section in
$N$ and a neighbourhood $X$ of $M$ in $\mathbb{R}^{n}$ such that
$\nu$ restricts to a diffeomorphism $W \to X$, which we shall
also denote by $\nu$. Reversing $\nu$, we get a map $X \to W
\subseteq N$ which we can combine with the projection to $M$. Let
us write $\mu \colon X \to M$ for this composition.

This map $\mu$ is the **local averaging function** that we need.
Well, technically the local averaging function is a bit more
complicated but to define it in full one needs more data.
However, that data will depend on the source of our maps so $\mu$
is the data that is solely dependent on $M$ that goes in to the
mix that defines the local averaging function and so deserves
that name.

### A Compatible Local Addition ###

The local averaging function is only half of what we need to
construct a suitable tubular neighbourhood. The other half is
provided by a [[local addition]]. It needs to be compatible with
the local averaging function and so we assume that the
construction of the previous section has been carried out.

Turning to the tangent spaces, for $p \in M$, the space $T_{p} M$
sits as an affine subspace in $\mathbb{R}^{n}$ with complement
$N_{p}$. There is an orthogonal projection map $\mathbb{R}^{n}
\to T_{p} M$, projecting along $N_{p}$. Restricting this to $M$,
we obtain a map $\lambda_{p} \colon M \to T_{p} M$.

Note that $\lambda_{p}(p) = p$, which is the zero of $T_{p} M$,
and that $d \lambda_{p} \colon T_{p} M \to T_{p}(T_{p} M) = T_{p}
M$ is the identity. Allowing $p$ to vary, we obtain a smooth map
$\lambda \colon M \times M \to T M$. If we think of $M \times M$
as a bundle over $M$ (via the projection on to the first factor)
then $\lambda \colon M \times M \to T M$ is a bundle map.

Now we don't actually need this to be defined on the whole of
$M$, just on a small piece of it near $p$, but what "small" means
here depends on $X$. Using the metric on $\mathbb{R}^{n}$ coming
from the orthogonal structure, we choose a continuous function
$\epsilon \colon M \to (0,\infty)$ with the property that the
closed ball of radius $\epsilon(p)$ at $p$ is contained in $X$.
Let us write $X_{p}$ for the corresponding *open* ball. Then we
restrict $\lambda_{p}$ to $X_{p} \cap M$ and thus restrict
$\lambda$ to the set 
$$
X_{M} \coloneqq \{(p,q) \in M \times M : q \in X_{p}\} = \{(p,q) \in M \times M : d(p,q) \lt \epsilon(p)\}
$$
which is an open neighbourhood of the diagonal.

From the above, we see that (again by the inverse function
theorem), there is a neighbourhood $V$ of the diagonal and a
neighbourhood $U$ of the zero section such that $\lambda$
restricts to a diffeomorphism $\lambda \colon V \to U$. As we
have already restricted $\lambda$ to $X_{M}$, $V$ is a subset of
it.

Let $\eta \colon U \to M$ be the composition:
$$
T M \supseteq
U \xrightarrow{\lambda^{-1}}V \subseteq M \times M \to M
$$
where
the projection is on to the second factor. As $\lambda$ is a
bundle map, $\lambda^{-1} = \pi \times \eta$ and thus $\eta$ is a
[[local addition]].

Let $U_{p} = U \cap T_{p} M$. Then $\eta(U_{p})$ is a subset of
$\{p\} \times M$. Let $\eta_{p} \colon U_{p} \to V_{p} \subseteq
M$ be the obvious restriction. Since $\lambda^{-1} = \pi \times
\eta$ and the domain of $\lambda$ is a subset of $X_{M}$, the set
$\eta(U_{p})$ is a subset of $X_{M} \cap \{p\} \times M = \{p\}
\times X_{p}$. Thus $\eta_{p}(U_{p}) \subseteq X_{p}$. What this
means is that the set $\eta_{p}(U_{p})$, which is a subset of $M$
and therefore may be all twisted and turned, nevertheless has the
property that the closure of its convex hull is contained inside
$X$, the tubular neighbourhood of $M$.

Thus we have the maps
$$
\begin{aligned}
\eta &\colon T M \supseteq U \xrightarrow{\cong}V \subseteq M
\times M, \\   \eta_{p} & \colon T_{p} M \supseteq U_{p}
\xrightarrow{\cong}V_{p} \subseteq M, \\   \nu &\colon N
\supseteq W \xrightarrow{\cong}X \subseteq \mathbb{R}^{n}, \\ \mu
&\colon \mathbb{R}^{n} \supseteq X \xrightarrow{\cong}W \subseteq
N \xrightarrow{\pi}M.
\end{aligned}
$$
The map $\eta_{p}$ works by projecting $U_{p} \subseteq T_{p}
M$ on to $M$ along $N_{p}$. The map $\mu$ projects $X$ on to $M$
also by projecting along $N_{p}$.

What we have so far can be portrayed in the following diagram.

+-- {: style="text-align: center"}
<svg width="383" height="281" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="59931">
 <g>
  <title>Layer 1</title>
  <path id="svg_59931_29" d="m78,30c-27.333328,22.333328 20.666656,71.666687 49,93c28.333344,21.333313 52,26.333313 97,22c45,-4.333313 96,-30.666672 62,-73l40,-30c68.666656,11.333328 69,24 31,88c-38,64 -95.666687,72.666656 -155,73c-59.333328,0.333344 -128.333344,-10.666687 -169,-64c-40.666664,-53.333328 -41.666664,-136.666672 -3,-138l48,29z" stroke-width="2" stroke="#cccccc" fill="#bfbfbf"/>
  <line transform="rotate(90, 198, 175.002)" id="svg_59931_1" y2="276.002475" x2="198" y1="74" x1="198" stroke-width="2" stroke="#000000" fill="none"/>
  <path id="svg_59931_5" d="m61,20.000061c-79,21.333328 23,151.666687 141,154c118,2.333313 181,-116.333344 100,-114.000015" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_59931_6" y2="280.034629" x2="202" y1="49" x1="202" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_59931_7" y="49" x="195">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>N</mi>
       <mi>p</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">N_p</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_59931_8" y="178" x="289">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>T</mi>
       <mi>p</mi>
      </msub>
      <mi>M</mi>
     </mrow>
     <annotation encoding="application/x-tex">T_p M</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_marker_end_svg_59931_9)" id="svg_59931_9" y2="155" x2="193" y1="71" x1="193" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_59931_10" y="82" x="158">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#956;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\mu</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_marker_end_svg_59931_11)" id="svg_59931_11" y2="121" x2="92" y1="63" x1="142" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject id="svg_59931_12" height="20" width="48" font-size="16" y="62" x="93">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#956;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\mu</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_marker_end_svg_59931_18)" id="svg_59931_18" y2="148.977284" x2="105" y1="171" x1="105" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_59931_19)" id="svg_59931_19" y2="154.96878" x2="292" y1="171" x1="292" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_59931_20" y="148" x="64">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>&#951;</mi>
       <mi>p</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">\eta_p</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_59931_21" height="20" width="48" font-size="16" y="151" x="286">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>&#951;</mi>
       <mi>p</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">\eta_p</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_59931_30" y="8" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>X</mi>
     </mrow>
     <annotation encoding="application/x-tex">X</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_59931_9">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_59931_11">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_59931_18">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_59931_19">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
 </defs>
</svg>
=--

### The Tubular Neighbourhood ###

At this point it is time to we reintroduce our group, although at
this stage it isn't important that our source be a group. We need
a compact [[smooth space]]; let us write this as $S$. We also
need a measure on $S$ with the property that $S$ has measure $1$.
The idea is to consider smooth maps $S \to M$ with the property
that the closed convex hull of the image of $S$ is contained in
$X$. Then given such a smooth map $\alpha \colon S \to M$ we can
consider it as a map in to $\mathbb{R}^{n}$ and take its
integral. As the closed convex hull of the image of $S$ is in
$X$, the value of this integral will also be in $X$ and thus can
be projected to $M$ via $\mu$. Let us write $\Cvx(S,M)$ for the
set of smooth maps $S \to M$ with the property that the closed
convex hull of $S$ lies in $X$ and let us write $\tau \colon
\Cvx(S,M) \to M$ for this *local averaging* map.

Now that we know what is the "average" of a "small" map $\alpha
\colon S \to M$, we can consider the question as to whether or
not we can use the local addition to contract $\alpha$ to its
average. To be able to do this, we need to further restrict our
attention to those maps $\alpha \colon S \to M$ with the property
that $(\tau \alpha, \alpha(s)) \in V$ for all $s \in S$. Knowing
this, we can compose $\alpha$ with $\eta_{\tau \alpha}^{-1}$ to
produce a map $S \to U$.

The construction is set up so that the resulting map $S \to U$
lies in a single fibre and has the property that it averages to
$0$ (viewed in $T_{p} M$). This will define a diffeomorphism
between the set of smooth maps $S \to U$ with those properties
and an open subset of $C^{\infty}(S,M)$. Let us define:
$$
C^{\infty}_{0}(S,U) \coloneqq \{ \alpha \colon S \to U : \pi
\alpha\; \text{is constant}, \int_{S} \alpha = 0_{\pi \alpha}\}.
$$

The reverse map is straightforward to describe: given a map
$\alpha \in C^{\infty}_{0}(S,U)$, we compose it with $\eta_{\pi
\alpha}$ to produce a map $S \to M$.

+-- {: .num_lemma}
###### Lemma ######
The map $C^{\infty}_{0}(S,U) \to C^{\infty}(S,M)$ defined by
composition with $\eta$ is a diffeomorphism on to its image which
is open in $C^{\infty}(S,M)$.
=--

+-- {: .proof}
To see that its image is open, let us first note that $\Cvx(S,M)$
is open since $X$ is open in $\mathbb{R}^{n}$ and $S$ is compact.
Then within that, the condition on a map $\alpha \colon S \to M$
that $(\tau \alpha, \alpha(s)) \in V$ for all $s \in S$ is also
an open condition, again because $S$ is compact. Hence the set of
smooth maps $\alpha \colon S \to M$ with the property that the
closed convex hull of $\alpha(S)$ lies in $X$ (whence $\tau
\alpha$ is defined) and that $(\tau \alpha, \alpha(s)) \in V$ for
all $s \in S$ is an open subset of $C^{\infty}(S,M)$.

Let us write this as $Y$. We have a map $C^{\infty}_{0}(S,U) \to
Y$ given by composition: $\alpha \mapsto \eta_{\pi \alpha} \circ
\alpha$; and a map $Y \to C^{\infty}_{0}(S,U)$ given by
$\eta_{\tau \beta}^{-1} \circ \beta$. That the second is
well-defined is not completely obvious: although $\eta_{\tau
\beta}^{-1} \circ \beta$ lies in $U_{\tau \beta}$ by
construction, we also have to show that its average is the zero
in $T_{\tau \beta} M$.

This follows from the way that $\eta_{\tau \beta}$ and $\tau$
were constructed. Since averaging is a linear map, the average of
$\beta$ splits as the sum of a point in $T_{\tau \beta} M$ and a
point in $N_{\tau \beta} M$. However, by definition, $\tau \beta$
lies in $N_{\tau \beta}$ and thus the contribution from $T_{\tau
\beta} M$ must be the zero vector.

To show that these are inverse, it is enough to show that $\tau
(\eta_{\pi \alpha} \circ \alpha) = \pi \alpha$ and
$\pi(\eta_{\tau \beta}^{-1} \circ \beta) = \tau \beta$.

The second is by construction: $\eta_{\tau \beta}$ has image in
$U_{\tau \beta}$. The first follows by the argument on splitting
the average: the average of $\eta_{\pi \alpha} \circ \alpha$
splits as the average of its projection to $T_{\pi \alpha} M$
plus the average of its projection to $N_{\pi \alpha}$. Since the
former is $0_{\pi \alpha}$, the average of $\eta_{\pi \alpha}
\circ \alpha$ lies in $N_{\pi \alpha}$ and hence $\tau \eta_{\pi
\alpha} \circ \alpha = \pi \alpha$.
=--

The last step in constructing the tubular neighbourhood is to
construct a diffeomorphism between $C^{\infty}_{0}(S,U)$ and
$C^{\infty}_{0}(S,T M)$. This is straightforward: we restrict $U$
(if necessary) so that it is diffeomorphic as a fibre bundle to
$T M$, say via $\rho \colon U \to T M$, and then define the map
$C^{\infty}_{0}(S,U) \to C^{\infty}_{0}(S, T M)$ via:
$$
\alpha \mapsto \rho \circ \alpha - \int_{S} \rho \circ \alpha.
$$

### Invariance ###
The above construction produces a tubular neighbourhood of the
space of constant maps $S \to M$ in the space of smooth maps $S
\to M$. The construction is invariant under measure-preserving
diffeomorphisms of $S$. In particular, if $S$ is a group and the
measure is invariant under the group action, the tubular
neighbourhood is equivariant.

### Fixed Point Submanifolds ###

This construction extends to the case where the source is a fibre
bundle $E \to B$ with fibre $S$ and the submanifold under
consideration are those maps $E \to M$ which are constant on the
fibres of $E \to B$. We need to assume that the transition
functions preserve the measure on the fibres. The required
tubular neighbourhood consists of those maps $E \to M$ with the
property that when restricted to a fibre (identified with $S$ via
a measure-preserving diffeomorphism), the map lies in the image
of $C^{\infty}_{0}(S,M)$.

[[!redirects equivariant tubular neighbourhoods in mapping spaces]]
