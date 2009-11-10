#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A _fibration sequence_ is a "long right-[[exact sequence]]" (or left-exact, I keep mixing that up) in an [[(∞,1)-category]].

Traditionally fibration sequences have been considered in the context of [[homotopical category|homotopical categories]] such as [[model category|model categories]] and [[category of fibrant objects|Brown category of fibrant objects]] which [[presentable (infinity,1)-category|present]] the [[(∞,1)-category]] in question. In particular, classically this was considered for [[Top]] itself.



#Definition#

Let $C$ be an [[(∞,1)-category]] with small [[limits]] and consider [[pointed objects]] of $C$, i.e. morphisms ${*} \to A$ from the [[terminal object]] ${*}$ ([[generalized the|the]] [[point]]) to some object $A$. All unlabeled morphisms from the point in the following are these chosen ones and all other morphisms are taken with respect to these points.

Notice that in the case that $C$ happens to be a [[stable (∞,1)-category]] for which ${*} = 0$ all objects are canonically pointed and the notions of left- and right-exact fibration sequences coincide.

But for the notion of fibration sequence to make sense, we do not need to assume that $C$ is a stable $(\infty,1)$-category. In particular, in the context of [[nonabelian cohomology]] (see [[gerbe]] and [[principal 2-bundle]]) one considers fibration sequences in non-stable $(\infty,1)$-categories.


Now let $f : A \to B$ be a morphism in $C$.

The **homotopy fiber** or **homotopy kernel** of $f$ is [[generalized the|the]] [[pullback]] (which in our $(\infty,1)$-categorical context means [[homotopy limit|homotopy pullback]]) of the point along $f$:

$$
  \array{
     ker(f) &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     A &\stackrel{f}{\to}& B
  }
  \,.
$$

In particular the homotopy fiber of the point ${*} \to B$ is the [[loop space object]] $\Omega B$ of $B$ (by definition):

$$
  \array{
     \Omega B &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     {*} &\stackrel{}{\to}& B
  }
  \,.
$$

Notice that the ordinary 1-categorical [[pullback]] of a point to itself is necessarily just the point again. Much of what makes [[(∞,1)-category]]-theory richer than ordinary category theory is this fact that the kernel of the point is not trivial, but loops. This implies in particular that **the kernel of the kernel is in general nontrivial**.

Namely the homotopy kernel of the morphism $ker(f) \to A$ constructed above is by definition the homotopy limit in the diagram

$$
  \array{
    ker(ker(f)) &\to& ker(f)
    \\
    \downarrow && \downarrow
    \\
    {*} &\to & A
  }
$$

This is the same kind of diagram as before, just depicted after taking its mirror image along a diagonal. The point of drawing it this way is that this suggests to form the pasting diagram with the one that defines $ker(f)$

$$
  \array{
    ker(ker(f)) &\to& ker(f) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& A &\stackrel{f}{\to}& B
  }
  \,.
$$


Since the $(\infty,1)$-categorical homotopy pullback comopose just as ordinary [[pullback]] diagrams do, it follows that the total outer square obtained this way is itself a homotopy pullback. But by definition of te [[loop space object]] $\Omega B$ this means that the kernel of the kernel is loops:

$$
  ker(ker(f)) \simeq \Omega B
  \,.
$$

I.e. all three squares in 

$$
  \array{
    \Omega B &\to& ker(f) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& A &\stackrel{f}{\to}& B
  }
$$

are (homotopy) pullback squares.

Continuing this way to the left, we obtain a long sequence of morphisms to the left

$$
  \cdots
  \to
  \Omega \Omega B
  \to
  \Omega A \stackrel{\bar \Omega f}{\to}
  \Omega B \to ker(f) \to A \stackrel{f}{\to} B
  \,.
$$

Here the $\bar \Omega$ indicates that the map involves reversing the direction of loops. This comes about by looking closely at the pullback diagrams that this comes from

$$
  \array{
    \Omega(A) &\to& {*}
    \\
    \downarrow^{\bar \Omega f} && \downarrow
    \\
    \Omega B &\to& ker(f) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} &\to &A &\stackrel{f}{\to}& B
  }
  \,.
$$

Again, all squares and all pasting squares appearing here are homtopy pullback squares. If I had labeled to two morphisms to the point out of the loop object one would see that $\bar \Omega f$ indeed reverses orientation of loops. 

Anyway.

Usually, when looking at fibration sequences in 1-categorical contexts of the [[homotopy category of an (∞,1)-category]], one doesn't see these long fibration squences directly, but only "in cohomology".

This can be usefully understood as follows:

recall from [[cohomology]] that for $X$ and $A$ objects in an [[(∞,1)-category]] $C$ that is an [[(∞,1)-topos]], the $\infty$-groupoid of $A$-valued cocycle on $X$ is just $Hom_C(X,A)$, so that the corresponding cohomology classes are

$$
  H(X,A) = \Pi_0 Hom_C(X,A) = Ho_C(X,A)
  \,,
$$

where $Ho_C$ is the corresponding [[homotopy category of an (∞,1)-category]].

The upshot being that in the right $(\infty,1)$-context cohomology is just the [[hom-object]].

But the [[hom-functor]] has the crucial property that it is an [[exact functor]] in both arguments. This holds for $(\infty,1)$-categories just as well as for ordinary categories. For our context this means in particular that for 

$$
  \array{
    A \times_C B &\to& B
    \\
    \downarrow && \downarrow
    \\
    A &\to& C
  }
$$

a homotopy pullback in $C$, for every $X \in C$ the induces diagram

$$
  \array{
    Hom_C(X,A) \times_{Hom_C(X,C)} Hom_C(X,B) &\to& Hom_C(X,B)
    \\
    \downarrow && \downarrow
    \\
    Hom_C(X,A) &\to& Hom_C(X,C)
  }
$$

is again homotopy pullback diagram (of [[∞-groupoids]]).

So in particular for

$$
  \cdots
  \to
  \Omega \Omega B
  \to
  \Omega ker(f)
  \to
  \Omega A \stackrel{\bar \Omega f}{\to}
  \Omega B \to ker(f) \to A \stackrel{f}{\to} B
$$

a fibration sequence and for $X$ any object, there is a fibration sequence

$$
  \cdots
  \to
  Hom_C(X,\Omega \Omega B)
  \to
  Hom_C(X,\Omega ker(f))
  \to
  Hom_C(X,\Omega A) \stackrel{Hom_C(X,\bar \Omega f)}{\to}
  Hom_C(X,\Omega B) \to Hom_C(X,ker(f)) \to Hom_C(X,A) \stackrel{Hom_C(X,f)}{\to} Hom_C(X,B)
$$

is again a fibration sequence, now of $\infty$-groupoids. By projecting everything to connected components with $\Pi_0$ this then yields an ordinary long exact sequence of pointed sets


$$
  \cdots
  \to
  Ho_C(X,\Omega \Omega B)
  \to
  Ho_C(X,\Omega ker(f))
  \to
  Ho_C(X,\Omega A) \stackrel{Ho_C(X,\bar \Omega f)}{\to}
  Ho_C(X,\Omega B) \to Ho_C(X,ker(f)) \to Ho_C(X,A) \stackrel{Ho_C(X,f)}{\to} Ho_C(X,B)
  \,.
$$

Due to the identitfication of [[cohomology]] with these homotopy hom-sets via $Ho_C(X,A) =: H(X,A)$, this is a "long exact sequence in cohomology"


$$
  \cdots
  \to
  H(X,\Omega \Omega B)
  \to
  H(X,\Omega ker(f))
  \to
  H(X,\Omega A) \stackrel{H(X,\bar \Omega f)}{\to}
  H(X,\Omega B) \to H(X,ker(f)) \to H(X,A) \stackrel{H(X,f)}{\to} H(X,B)
  \,.
$$

#Examples#

Fibration sequences are familiar from the context of [[principal bundles]].

Let $G$ be a [[group]] and let $\mathbf{B}G$ denote the corresponding one-object [[groupoid]] (in the world of [[∞-groupoids]]) or else the [[classifying space]] $\mathcal{B}G$.

Notice that 

$$
  G \simeq \Omega \mathbf{B} G
  \,.
$$

Then that a $G$-[[principal bundle]] $P \to X$ is classified by morphism $X \to \mathbf{B}G$ means that it is the homotopy fiber of this morphism.

Indeed, as indicated at [[generalized universal bundle]] and at [[homotopy limit]], we may compute the homotopy pullback

$$
  \array{
  P &\to& {*}
  \\
  \downarrow && \downarrow
  \\
  X &\to& \mathbf{B}G
 }
$$

by first forming the standard _fibrant replacement_ of the diagram $X \to \mathbf{B}G \leftarrow {*}$. That is given by
the diagram

$$
  X \to \mathbf{B}G \leftarrow \mathbf{E}G  
  \,,
$$

where $\mathbf{E}G \simeq {*}$ is the total "space" (or 2-groupoid) of the universal $G$-bundle. Once we have done this weakly equivalent replacement, the [[homotopy pullback]] may be computed as the _ordinary_ pullback

$$
  \array{
   P &\to & \mathbf{E}G
   \\
   \downarrow && \downarrow
   \\
   \hat X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,, 
$$

in the ordinary 1-category of $n$-groupoids or spaces, using a replacement $\hat X \stackrel{\simeq}{\twoheadrightarrow} X$ of $X$ by an acyclic fibration (called "[[hypercover]]" in this context) (for instance the &#268;ech groupoid associated with an open cover of $X$). 

One recognizes the usual statement that principal $G$-bundles all arise as pullbacks of the universal $G$-principal bundle. 

The fact that such pullbacks really are bundles whose fiber is $G$ is the statement of the long fibration sequence induced by $g$ which says that picking any point ${*} \to X$ of $X$ and then pulling back $P$ to that point (i.e. restricting it to that point) yields $\Omega \mathbf{B}G = G$:

$$
  \array{
   G \simeq
   \Omega \mathbf{B}G
   &\to&
   P &\to & \mathbf{E}G
   \\
   \downarrow && \downarrow && \downarrow
   \\
   {*}&\stackrel{x}{\to}& \hat X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,, 
$$

The same logic -- even the same diagrams -- work for [[principal 2-bundles]] and generally for [[principal ∞-bundles]].


[[!redirects fibration sequences]]
[[!redirects cofibration sequence]]
[[!redirects homotopy fiber]]
[[!redirects homotopy cofiber]]
[[!redirects cofibration sequences]]
[[!redirects homotopy fibers]]
[[!redirects homotopy cofibers]]