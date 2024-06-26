
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

[[end|Ends]] and [[coends]] are special sorts of [[limit]] and [[colimit]], respectively, and have corresponding sorts of [[homotopy limits]] and colimits -- [[homotopy ends]] and coends.  Since a [[derivator]] is a formal structure for computing homotopy limits and colimits, there are corresponding notions of ends and coends in a derivator.

## Definitions

Let $D$ be a [[derivator]] indexed on a 2-category $Dia$ of diagram shapes, let $A\in Dia$, and let $H\in D(A^{op}\times A)$; we wish to define the *coend* of $H$ (obvious dualizations will yield its *end*).  We will give four equivalent definitions, each of which generalizes a classical construction of ordinary coends in terms of colimits.

### As a colimit over simplices

One classical construction of a coend as a colimit proceeds by constructing an auxiliary category $A^{tw}$, whose objects are the objects and arrows of $A$, with morphisms from each arrow of $A$ (regarded as an object of $A^{tw}$) to its domain and codomain.  There is a functor $p\colon A^{tw}\to A^{op}\times A$ which sends each object $x$ to $(x,x)$ and each arrow $f\colon x\to y$ to $(y,x)$, and the coend of $H\colon A^{op}\times A\to C$ can be constructed as the colimit of $p^* H\colon A^{tw}\to C$.

We can mimic this in a derivator, except that we need to "homotopify" $A^{tw}$ by including higher information as well.  Thus, let $(\Delta / A)^{op}$ denote the opposite of the category of simplices of $A$.  Thus its objects are functors $x\colon [n]\to A$, and its morphisms from $x\colon [n]\to A$ to $y\colon [m]\to A$ are functors $[m]\to [n]$ making the evident triangle commute.  There is a functor $p\colon (\Delta / A)^{op} \to A^{op}\times A$ which sends $x\colon [n]\to A$ to $(x(n), x(0))$.

Note that $A^{tw}$, as constructed above, is the full subcategory of $(\Delta / A)^{op}$ containing only the 0-simplices and 1-simplicies.  The inclusion of this subcategory is [[final functor|final]], but not [[homotopy final functor|homotopy final]].  Thus, for ordinary colimits it suffices to consider $A^{tw}$, but for homotopy colimits we need all of $(\Delta / A)^{op}$.

Hence, we define the **(homotopy) coend** of $H\in D(A^{op}\times A)$ to be the (homotopy) colimit of $p^* H \in D((\Delta / A)^{op})$.

### As a colimit over arrows

Another classical construction of a coend as a colimit involves a different auxiliary category, the opposite [[twisted arrow category]] $Tw(A)^{op}$.  The objects of $Tw(A)^{op}$ are arrows $f\colon x\to y$ in $A$, and its morphisms from $f\colon x\to y$ to $g\colon z\to w$ are commutative squares
$$ \array{
  x & \to & z\\
  ^f \downarrow & & \downarrow^g\\
  y & \leftarrow & w }
$$
in $A$.  There is a projection
$$ r \colon Tw(A)^{op} \to A^{op}\times A $$
sending $f\colon x\to y$ to $(y,x)$, and the coend of $H\colon A^{op}\times A\to C$ can be constructed as the colimit of $r^* H\colon Tw(A)^{op} \to C$.

Amazingly, this version needs no modification to become homotopical.  Given $H\in D(A^{op}\times A)$ in a derivator, we can simply restrict along $r$ to $Tw(A)^{op}$, then take the (homotopy) colimit.  To see that this agrees with the previous definition, it suffices to factor $q$ through $r$ via a [[homotopy final functor]] $s$:
$$ \array{ & & Tw(A)^{op} \\
  & ^{s}\nearrow & & \searrow^{r}\\
  (\Delta / A)^{op} & & \underset{q}{\to} & & A^{op}\times A } $$
The definition of $s$ is simple: we regard an $n$-simplex as a string of $n$ composable arrows in $A$ and take its composite.  The morphisms in the two categories match nicely.  To show that $s$ is homotopy final, we must show that
$$\array{(\Delta / A)^{op} & \xrightarrow{s} & Tw(A)^{op} \\
  \downarrow & & \downarrow \\
  * & \to & * }$$
is a [[homotopy exact square]].  For this, it suffices to show that it becomes homotopy exact when pasted with any [[comma square]]
$$\array{Q_{f} & \overset{}{\to} & *\\
  \downarrow & \swArrow & \downarrow^{f}\\
  (\Delta / A)^{op}& \underset{}{\to} & Tw(A)^{op}.}$$
The objects of the category $Q_{f}$ are strings of composable $n\ge 2$ arrows whose composite is $f$.  Its morphisms are like those of $(\Delta / A)^{op}$, but the first and last face maps are also given by composition instead of forgetting.  In fact, it is precisely the category of simplices of the fiber of the [[two-sided bar construction]] $B(A(-,b),A,A(a,-))$ over $f$.

However, the simplicial map $B(A(-,b),A,A(a,-)) \to A(a,b)$, with $A(a,b)$ a discrete simplicial set, is well-known to be a [[simplicial homotopy equivalence]] and thus a weak equivalence of simplicial sets.  Thus, each of its fibers is simplicially contractible, and hence each $Q_f$ has contractible nerve.  This implies that
$$ \array{ Q_f & \to & * \\ \downarrow & & \downarrow \\ * & \to & * } $$
is homotopy exact, and thus $s$ is homotopy final.

### As a bar construction

Another classical construction of a coend as a colimit is as the [[coequalizer]] of a [[parallel pair]]
$$ \coprod_{f\colon x\to y} H(y,x) \;\rightrightarrows\; \coprod_{x} H(x,x). $$
This can be obtained in a straightforward way from the previous construction.  If $Ppr$ denotes the [[walking structure|walking]] parallel pair $(1 \rightrightarrows 0)$, then there is a functor $q\colon A^{tw}\to Ppr$ sending each object of $A$ to 0, each arrow of $A$ to 1, and sorting the morphisms by whether they map an arrow to its domain or to its codomain.

Then the above parallel pair is the (pointwise) [[left Kan extension]] of $p^* H \colon A^{tw} \to C$ along $q$.  Because $q$ is a [[discrete opfibration]], left Kan extension along it can be computed with colimits over its fibers -- since each fiber is discrete, we obtain the coproducts above.  And since the colimit of $p^*H$ is equivalently its left Kan extension to the [[point]], the functoriality of Kan extensions means that $\colim^{A^{tw}} p^* H$ is isomorphic to $\colim^{Ppr} Lan_q p^* H$, the latter being precisely the above coequalizer.

We can homotopify this in a straightforward way as well.  Let $p\colon (\Delta / A)^{op} \to A^{op}\times A$ be as above, and let $q\colon (\Delta / A)^{op} \to \Delta^{op}$ be the obvious forgetful functor (whose target is the opposite of the [[simplex category]]).  Note that as before, $Ppr$ is a final, but not homotopy-final, subcategory of $\Delta^{op}$.  The functoriality of homotopy Kan extensions in a derivator means that the homotopy colimit of $p^* H\in D((\Delta / A)^{op})$ can equivalently be calculated as the homotopy colimit of $q_! p^* H \in D(\Delta^{op})$.

Note that since an object $D(\Delta^{op})$ is a [[simplicial object]] of $D$, it makes sense to call its colimit [[geometric realization]].  Moreover, the homotopy version of $q$ is also a discrete opfibration, and since pullbacks of fibrations are [[homotopy exact square|homotopy exact]], homotopy Kan extensions along $q$ are also computed as colimits over its fibers.  These fibers are also discrete, so we obtain a simplicial diagram of the following sort:

$$ \cdots \coprod_{x_0\xrightarrow{f_1} x_1 \xrightarrow{f_2} x_2} H(x_2,x_0)
\underoverset{\to}{\to}{\underoverset{\leftarrow}{\leftarrow}{\to}}
\coprod_{x_0\xrightarrow{f_1} x_1} H(x_1,x_0)
\underoverset{\to}{\to}{\leftarrow}
\coprod_{x} H(x,x)
$$

This is a derivator version of the [[bar construction]] of $H$.  (A bar construction is perhaps the most classical construction of homotopy coends.)

### As a weighted colimit

A last classical construction of a coend is as a [[weighted colimit]] of $H\colon A^{op}\times A\to C$, weighted by the [[hom-functor]] $hom\colon A^{op}\times A \to Set$.

In order to homotopify this, recall that weighted colimits can be constructed in terms of Kan extensions by first Kan extending to the [[collage]] of the weighting (pro)functor, then restricting to the target object.  Thus, let $B$ denote the collage of $hom\colon A^{op}\times A \to Set$ regarded as a profunctor $1 &#8696; A^{op}\times A$, with inclusions $u\colon 1\to B$ and $v\colon A^{op}\times A \to B$.  We can therefore define the **homotopy coend** of $H\in D(A^{op}\times A)$ to be $u^* v_! H$.

To show that this is the same as the previous definitions, we simply observe that there is a comma square
$$\array{Tw(A)^{op}& \overset{r}{\to} & A^{op}\times A\\
  ^!\downarrow & \swArrow_\alpha & \downarrow^v\\
  1& \underset{u}{\to} & B}
$$
Thus, by one of the axioms of a derivator, $u^* v_! H \cong \colim (r^* H)$.

[[!redirects end in a derivator]]
[[!redirects ends in a derivator]]
[[!redirects ends in derivators]]
[[!redirects coend in a derivator]]
[[!redirects coends in a derivator]]
[[!redirects coends in derivators]]
