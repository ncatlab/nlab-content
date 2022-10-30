
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A **covering space** (or **wrapping space**) is a [[bundle]] $p: E \to B$ in which is locally trivial and with [[discrete space|discrete]] fiber. 


## Definition

In [[topology]], for $B$ a [[topological space]]

then a [[continuous function]] $p: E \to B$ is a covering space over $B$ if for each point $x \in B$, there exists an [[open neighborhood]] $U$ of $x$ which is **evenly covered** by $p$ in that the [[pullback]] of $p$ over $U$ is isomorphic to a product bundle with discrete fiber $E_x = p^{-1}(x)$: 

$$\array{
U \times E_x & \cong & p^{-1}(U) & \to & E\\
& \pi \searrow & \downarrow & & \downarrow p\\
& & U & \hookrightarrow & B
}$$

(the square is a pullback and the isomorphism maps $(x, e \in E_x) \mapsto e$). 

Covering spaces over $B$ form an evident [[full subcategory]] $Cov/B \hookrightarrow Top/B$ of the [[slice category]] of [[Top]] over $B$, the _[[category of covering spaces]]_. These may be put together to form a [[replete subcategory|replete]], [[wide subcategory|wide]] subcategory $Cov$ of $Top$, so that $Cov/B$ is an [[over category]], just as the notation suggests.

+-- {: .num_remark}
###### Remark

Different points in $B$ may have non-isomorphic fibers. However, if open sets $U$ and $V$ are evenly covered by $p: E \to B$ and have nonempty intersection, then there are canonical identifications 
$$E_x \cong E_z \cong E_y$$ 
between typical fibers over $x \in U$, $y \in V$, and $z \in U \cap V$. If $B$ is path-connected, then all the fibers match up to isomorphism (by the unique path-lifting lemma (lemma \ref{CoveringSpacePathLifting} below)). 

=--

+-- {: .num_remark}
###### Remark

Fibers of a covering space may be empty. Some authors choose to forbid that, adding the condition that $p$ be a surjection, but the resulting category of covering projections over a space $B$ is not as nice as it would be without that condition. 


=--


+-- {: .num_remark}
###### Remark

The terms "covering space" and "covering projection", while traditional, are certainly not optimal: they mislead by being too close to (open) "[[cover|coverings]]". [[James Dolan]] has suggested "wrapping space" as an alternative (as in the image of thread wrapping around a spool, to evoke the archetypal example of a covering projection, $p: \mathbb{R} \to S^1: x \mapsto \exp(i x)$). 

=--

+-- {: .num_remark}
###### Remark

There is a generalizatin to "semi-coverings" ([Brazas12](#Brazas12)). Semicoverings satisfy the "[[2 out of 3]] rule". I.e,, if $f=g h$ and two of $f,g,h$ are semicoverings , then so is the third. This is not true for covering maps. 

=--



## Properties

### Basic properties
 {#BasicProperties}

+-- {: .num_prop #CoveringProjectionsAreOpenMaps}
###### Proposition
**(covering projections are [[open maps]])**

If $p \colon E \to X$ is a covering space projection, then $p$ is an [[open map]].


=--

+-- {: .proof}
###### Proof

By definition of covering space there exists an [[open cover]] $\{U_i \subset X\}_{i \in I}$ and [[homeomorphisms]] $p^{-1}(U_i) \simeq U_i \times Disc(F_i)$ for all $i \in I$. Since the [[projections]] out of a [[product topological space]] are [[open maps]] ([this prop.](product+topological+space#ProjectionsAreOpenMaps)), it follows that $p$ is an open map when restricted to any of the $p^{-1}(U_i)$. But a general open subset $W \subset E$ is the union of its restrictions to these subspaces:

$$
  W = \underset{i \in I}{\cup} (W \cap p^{-1}(U_i))
  \,.
$$

Since images preserve unions ([this prop.](interactions+of+images+and+pre-images+with+unions+and+intersections#PreservationOfUnionsAndIntersectionsOfSets)) it follows that 

$$
  p(W) = \underset{i \in I}{\cup} p(W \cap p^{-1}(U_i))
$$

is a union of open sets, and hence itself open.

=--

+-- {: .num_lemma #CoveringSpaceFiberwiseDiagonalOpenAndClosed}
###### Lemma
**([[fiber product|fiber-wise]] [[diagonal]] of covering space is [[open subset|open]] and [[closed subset|closed]])**

Let $E \overset{p}{\to} X$ be a covering space. Consider the [[fiber product]]

$$
  E \times_X E \coloneqq \{ (e_1, e_2) \in E \times E \;\vert\; p(e_1) = p(e_2) \}
$$

hence (by the discussion at [Top - Univeral constructions](Top#UniversalConstructions)) the [[topological subspace]] of the [[product space]] $E \times E$, as shown on the right. By the [[universal property]] of the [[fiber product]], there is the [[diagonal]] [[continuous function]]

$$
  \array{
    E &\longrightarrow& E \times_X E
    \\
    e &\mapsto& (e,e)
  }
  \,.
$$

Then the [[image]] of $E$ under this function is an [[open subset]] and a [[closed subset]]:

$$
  \Delta(E) \subset E \times_X E
  \;\;\;
  \text{is open and closed}
  \,.
$$

=--

+-- {: .proof}
###### Proof

First to see that it is an open subset. It is sufficient to show that for any $e \in E$ there exists an open neighbourhood of $(e,e) \in E \times_X E$.

Now by definition of covering spaces, there exists an open neighbourhood $U_{p(e)} \subset X$ of $p(e) \in X$ such that 

$$
  \array{
    U_{p(e)} \times Disc(p^{-1}(p(e))) && \overset{\simeq}{\longrightarrow} & E\vert_{U_{p(e)}}
    \\
    & {}_{\mathllap{pr_1}}\searrow && \swarrow_{\mathrlap{p}}
    \\
    && U_{p(e)}
  }
  \,.
$$

It follows that $U_{p(e)} \times \{e\} \subset E$ is an open neighbourhood. Hence by the nature of the [[product topology]], $U_{p(e)} \times U_{p(e)} \subset E \times E$ is an open neighbourhood of $(e,e)$ in $E \times E$ and hence by the nature of the [[subspace topology]] the restriction 

$$
  (E \times_X E) \cap (U_{p(e)} \times U_{p(e)}) \subset E \times_X E
$$

is an open neighbourhood of $(e,e)$ in $E \times_X E$.

Now to see that the diagonal is closed, hence that the complement $(E \times_X E) \setminus \Delta(E)$ is an open subset, it is sufficient to show that every point $(e_1, e_2)$ with $e_1 \neq e_2$ but $p(e_1) = p(e_2)$ has an open neighbourhood in this complement.

As before, there is an open neighbourhood $U \subset X$ of $p(e_1) = p(e_2)$ over which the cover trivializes, and hence $U \times \{e_1\}, U \times \{e_2\} \subset E$ are open neighbourhoods of $e_1$ and $e_2$, respectively. These are disjoint by the assumption that $e_1 \neq e_2$. As above, this means that the intersection

$$
  (E \times_X E) \cap ( (U \times \{e_1\}) \times (U \times \{e_2\}) )
  \subset
  (E \times_X E) \setminus \Delta(E)
$$

is an open subset of the complement of the diagonal in the fiber product.


=--


### Relation to &#233;tale spaces

Every covering space (even in the more general sense not requiring any connectedness axiom) is an [[etale space]], but not vice versa: 

* for a covering space the inverse image of some open set in the base $B$ needs to be, by the definition, a disjoint union of homeomorphic open sets in $E$; however the 'size' of the neighborhoods over various $e$ in the same stalk required in the definition of &#233;tal&#233; space may differ, hence the intersection of their projections does not need to be an open set, if there are infinitely many points in the stalk.

* even if the the stalks of the etale space are finite, it need not be locally trivial. For instance the disjoint union $\coprod_i Ui$ of a collecton of open subsets of a space $X$ with the obvious projection $(\coprod_i U_i) \to X$ is etale, but does not have a typical fiber: the fiber over a given point has cardinality the number of open sets $U_i$ that contain this particular point.


### Lifting properties
 {#LiftingProperties}

We discuss [[left lifting properties]] satisfied by covering spaces.

1. [path-lifting property](#CoveringSpacePathLifting),

1. [homotopy-lifting propery](#CoveringSpacesHomotopyLifting),

1. the [lifting theorem](#TheTheoremLifting).




+-- {: .num_lemma #LiftsOverConnectedSpaceIntoCoveringSpaceAreUniqueRelativePoint}
###### Lemma
**([[lifts]] out of [[connected topological space|connected space]] into [[coverign spaces]] are unique relative to any point)**

Let 

1. $E \overset{p}{\to} X $ be a covering space, 

1. $Y$ a [[connected topological space]]

1. $f \;\colon\; Y \longrightarrow X$ a [[continuous function]].

1. $\hat f_1, \hat f_2 \;\colon\; Y \longrightarrow E$ two [[lifts]] of $f$, in that the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       && E
       \\
       & {}^{\mathllap{\hat f_i}}\nearrow & \downarrow^{\mathrlap{p}}
       \\
       Y &\underset{f}{\longrightarrow}& X
     }
   $$

   for $i \in \{1,2\}$.

If there exists $y \in Y$ such that $\hat f_1(y) = \hat f_2(y)$ then the two lifts already agree everywhere: $\hat f_1 = \hat f_2$.

=--

+-- {: .proof}
###### Proof

By the [[universal property]] of the [[fiber product]] 

$$
  E \times_X E \coloneq \left\{ (e_1, e_2) \in E \times E \;\vert\; p(e_1) = p(e_2) \right\} \subset E \times E
$$

the two lifts determine a fingle continuous function of the form

$$
  (\hat f_1, \hat f_2) 
    \;\colon\;
  Y \longrightarrow E \times_X E
  \,.
$$

Write 

$$
  \Delta(E)  \coloneqq \left\{ (e,e) \in E \times_X E \;\vert\; e \in E  \right\}
$$

for the [[diagonal]] on $E$ in the fiber product. By lemma \ref{CoveringSpaceFiberwiseDiagonalOpenAndClosed} this is an open subset and a closed subset of the fiber product space. Hence by continuity of $(\hat f_1, \hat f_2)$ also its pre-image 

$$
  (\hat f_1, \hat f_2)^{-1}(\Delta(E)) \subset Y
$$

is both closed and open, hence also its [[complement]] is open in $Y$.

Moreover, the assumption that the functions $\hat f_1$ and $\hat f_2$ agree in at least one point means that the above pre-image is [[inhabited set|non-empty]]. Therefore the assumption that $Y$ is [[connected topological space|connected]] implies that this pre-image coincides with all of $Y$. This is the statement to be proven.

=--

+-- {: .num_lemma #CoveringSpacePathLifting}
###### Lemma
**(path lifting property)**

Let $p \colon E \to X$ be any [[covering space]].  Given 

1. $\gamma \colon [0,1] \to X$ a [[path]] in $X$, 

1. $\hat x_0 \in E$ be a lift of its starting point, hence such that $p(\hat x_0) = \gamma(0)$

then there exists a unique path $\hat \gamma \colon [0,1] \to E$ such that

1. it is a lift of the original path: $p \circ \hat \gamma = \gamma$;

1. it starts at the given lifted point: $\hat \gamma(0) = \hat x_0$.

In other words, every [[commuting diagram]] in [[Top]] of the form

$$
  \array{
    \{0\} &\overset{\hat x_0}{\longrightarrow}& E
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    [0,1] &\underset{\gamma}{\longrightarrow}& X
  }
$$

has a unique [[lift]]:

$$
  \array{
    \{0\} &\overset{\hat x_0}{\longrightarrow}& E
    \\
    \downarrow &{}^{\mathllap{\hat \gamma}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    [0,1] &\underset{\gamma}{\longrightarrow}& X
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof


First consider the case that the covering space is trival, hence of the [[Cartesian product]] form 

$$
  pr_1 \;\colon\;  X \times Disc(S) \longrightarrow X
  \,.
$$

By the [[universal property]] of the [[product topological spaces]] 
in this case a lift $\hat \gamma \colon [0,1] \to X \times Disc(S)$ is equivalently a [[pair]] of continuous functions

$$
  pr_1(\hat \gamma) \colon [0,1] \to X  \phantom{AAAA} pr_2(\hat \gamma) \colon [0,1] \to Disc(S)
  \,,
$$

Now the lifting condition explicitly fixes $pr_1(\hat \gamma) = \gamma$. nMoreover, a continuous function into a [[discrete topological space]] $Disc(S)$ is [[locally constant function|locally constant]], and since $[0,1]$ is a [[connected topological space]] this means that $pr_2(\hat \gamma)$ is in fact a [[constant function]] ([this example](connected+space#LocallyConstantFunctionsOnConnectedSpaces)), hence uniquely fixed to be $pr_2(\hat \gamma) = \hat x_0$.

This shows the statement for the case of trivial covering spaces.

Now consider any covering space $p \colon E \to X$. By definition of covering spaces, there exists for every point $x \in X$ a [[open neighbourhood]] $U_x \subset X$ such that the restriction of $E$ to $U_x$ becomes a trivial covering space:

$$
  p^{-1}(U_x) \simeq U_x \times Disc(p^{-1}(x))
  \,.
$$

Consider such a choice 

$$
  \{U_x \subset X\}_{x \in X}
  \,.
$$

This is an [[open cover]] of $X$. Accordingly, the [[pre-images]]

$$
  \left\{
    \gamma^{-1}(U_x)
    \subset 
    [0,1]
  \right\}_{x \in X}
$$

constitute an open cover of the [[topological interval]] $[0,1]$. 

Now $[0,1]$ is a [[sequentially compact topological space|compact]] [[metric space]] and therefore the [[Lebesgue number lemma]] implies that there is a [[positive number]] $\epsilon \in (0,\infty)$ and cover of $[0,1]$ by [[open intervals]] of the form $(-\epsilon + x , x  + \epsilon) \cap [0,1] \subset [0,1]$ which [[refinement|refines]] this cover. Again since $[0,1]$ is a [[compact topological space]] there is a [[finite set]] of such intervals which covers $[0,1]$. This means that we find a [[finite number]] of points 

$$
  t_0 \lt t_1 \lt \cdots \lt_{n+1} \in [0,1]
$$ 

with $t_0 = 0$ and $t_{n+1} = 1$ such that for all $0 \lt j \leg n$ there is $x_j \in X$ such that the corresponding path segment

$$
  \gamma([t_j, t_{j+1}]) \subset X
$$

is contained in $U_{x_j}$ from above. 

Now assume that $\hat \gamma\vert_{[0,t_j]}$ has been found. Then by the triviality of the covering space over $U_{x_j}$ and the first argument above, there is a unique lift of $\gamma\vert_{[t_j, t_{j+1}]}$ to a continuous function $\hat \gamma|_{[t_j,t_{j+1}]}$ with starting point $\hat \gamma(t_j)$. Since $[0,t_{j+1}]$ is the [[pushout]] $[0,t_j] \underset{\{t_j\}}{\sqcup} [t_j,t_{j+1}]$ ([this example](Top#TopologicalnSphereIsPushoutOfBoundaryOfnBallInclusionAlongItself)), it follows that $\hat \gamma|_{[0,t_j]}$ and $\hat \gamma\vert_{[t_j,t_{j+1}]}$ uniquely glue to a continuous function $\hat \gamma\vert_{[0,t_{j+1}]}$ which lifts $\gamma\vert_{[0,t_{j+1}]}$.

By [[induction]] over $j$, this yields the required lift $\hat \gamma$.

Conversely, given any lift, $\hat \gamma$, then its restrictions $\hat \gamma\vert_{[t_j, t_{j+1}]}$ are uniquely fixed by the above inductive argument. Therefore also the total lift is unique. Altrnatively, uniqueness of the lifts is a special case of lemma \ref{LiftsOverConnectedSpaceIntoCoveringSpaceAreUniqueRelativePoint}.

=--


+-- {: .num_prop #CoveringSpacesHomotopyLifting}
###### Proposition
**([[homotopy lifting property]] of [[covering spaces]])**

Let $p \colon E \to X$ be a [[covering space]]. Then given a [[homotopy]] relative the starting point between two [[paths]] in $X$, there is for every lift of these two paths to paths in $E$ with the same starting point a unique homotopy between the lifted paths that lifts the given homotopy:

For [[commuting squares]] of the form

$$
  \array{
    \{0\} \times \{0,1\} &\longrightarrow& \ast
    \\
    \downarrow && \downarrow
    \\ 
    [0,1] \times \{0,1\}
      &\overset{}{\longrightarrow}&
    E
    \\
    {}^{\mathllap{}}\downarrow 
      &{}^{\mathllap{\hat \eta}}\nearrow& 
    \downarrow^{\mathrlap{p}}
    \\
    [0,1] \times [0,1] &\underset{\eta}{\longrightarrow}& X
  }
$$

there is a unique diagonal [[lift]] in the lower diagram, as shown.

Moreover if the homotopy $\eta$ also fixes the endpoint, then so does the lifted homotopy $\hat \eta$.


=--

+-- {: .proof}
###### Proof

The proof is analogous to that of lemma \ref{CoveringSpacePathLifting}: The [[Lebesgue number lemma]] gives a partition of $[0,1] \times [0,1]$ into a [[finite number]] of squares such that the image of each under $\gamma$ lands in an open subset over which the covering space trivializes. Then there is [[induction|inductively]] a unique appropriate lift over each of these squares.

Finally, if the homotopy in $X$ is constant also at the endpoint, hence on $\{1\} \times [0,1]$, then the function constant on $\hat \eta(1,1)$ is clearly a lift of the path $eta\vert_{\{1\}\times [0,1]}$ and by uniqueness of the path lifting (lemma \ref{CoveringSpacePathLifting}) this means that also $\hat \eta$ is constant on $\{1\} \times [0,1]$.

=--

+-- {: .num_example #IfFundamentalGroupsIncludeThenfLoopsLiftToLoops}
###### Example


Let $(E,e) \overset{p}{\longrightarrow} (X,x)$ be a [[pointed topological space|pointed]] [[covering space]]
and let $f \colon (Y,y) \longrightarrow (X,x)$ be a point-preserving [[continuous function]] such that the image of the [[fundamental group]] of $(Y,y)$ is contained within the image of the fundamental group of $(E,e)$ in that of $(X,x)$:

$$
  f_\ast(\pi_1(Y,y)) \subset p_\ast(\pi_1(E,e))
  \phantom{AA}
  \subset 
  \pi_1(X,x)
  \,.
$$

Then for $\ell_Y$ a [[path]] in $(Y,y)$ that happens to be a [[loop]], every lift of its image path $f \circ \ell$ in $(X,x)$ to a path $\widehat{f\circ \ell_Y}$ in $(E,e)$ is also a loop there.

=--

+-- {: .proof}
###### Proof

By assumption, there is a loop $\ell_E$ in $(E,e)$ and a homotopy fixing the endpoints of the form

$$
  \eta_{X} \;\colon\; p \circ \ell_E \Rightarrow f\circ \ell_Y
  \,.
$$

Then by the homotopy lifting property (lemma \ref{CoveringSpacesHomotopyLifting}), there is a homotopy in $(E,e)$ fixing the starting point, of the form

$$
  \eta_{E} \;\colon\; \ell_E \Rightarrow \widehat{f \circ \ell_Y}
$$

and lifting the homotopy $\eta_X$. Since $\eta_X$ in addition fixes the endpoint, the uniqueness of the path lifting (lemma \ref{CoveringSpacePathLifting}) implies that also $\eta_{E}$ fixes the endpoint. Therefore $\eta_E$ is in fact a homotopy between loops, and so $\weidehat{f \circ \ell_Y}$ is indeed a loop.

=--

+-- {: .num_prop #TheTheoremLifting}
###### Proposition
**(lifting theorem)**

Let 

1. $p \colon E \to X$ be a [[covering space]];

1. $e \in E$ a point, with $x \coloneqq p(e)$ denoting its image,

1. $Y$ be a [[connected topological space|connected]] and [[locally path-connected topological space|locally path-connected]] [[topological space]];

1. $y \in Y$ a point

1. $f \colon (Y,y) \longrightarrow (X,x)$ a [[continuous function]] such that $f(y) = x$.

Then the following are equivalent:

1. There exists a lift $\hat f$ in the diagram

   $$
     \array{
       && (E,e)
       \\
       & {}^{\mathllap{\hat f}}\nearrow & \downarrow^{\mathrlap{p}}
       \\
       (Y,y) &\underset{f}{\longrightarrow}& (X,x)
     }
   $$

   of [[pointed topological spaces]].

1. The [[image]] of the [[fundamental group]] of $Y$ under $f$ in that of $X$ is contained in the image of the fundamental group of $E$ under $p$:

   $$
     f_\ast(\pi_1(Y,y)) \subset p_\ast( \pi_1(E,e) )
     \,
   $$

Moreover, if $Y$ is path-connected, then the lift in the first item is unique.


=--

+-- {: .proof}
###### Proof

The implication $1) \Rightarrow 2)$ is immediate. We need to show that the second statement already implies the first.

Since $Y$ is connected and locally path-connected, it is also a [[path-connected topological space]] ([this prop.](locally+path-connected+space#ForLocallyPathConnectedTheConnectedComponentsCoincideWithThePathConnectedComponents)). Hence for every point $y' \in Y$ there exists a [[path]] $\gamma$ connecting $y$ with $y'$ and hence a path $f \circ \gamma$ connecting $x$ with $f(y')$.  By the path-lifting property (lemma \ref{CoveringSpacePathLifting}) this has a unique lift

$$
  \array{
    \{0\} &\overset{e}{\longrightarrow}& E
    \\
    \downarrow &{}^{\mathllap{\widehat{f \circ \gamma}}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    [0,1]
     &\underset{f \circ \gamma}{\longrightarrow}&
    X
  }
  \,.
$$

Therefore

$$
  \hat f(y') \coloneqq \widehat{f \circ \gamma}
$$

if a lift of $f(y')$.

We claim now that this pointwise construction is independent of the choice $\gamma$, and that as a function of $y'$ it is indeed continuous. This will prove the claim.

Now by the path lifting lemma \ref{CoveringSpacePathLifting} the lift $\widehat{\f \circ \gamma}$ is unique given $f \circ \gamma$, and hence $\hat f(y')$ depends at most on the choice of $\gamma$.

Hence let $\gamma' \colon [0,1] \to Y$ be another path in $Y$ that connects $y$ with $y'$. We need to show that then $\widehat{f \circ \gamma'} = \widehat{f \circ \gamma}$.

First observe that if $\gamma'$ is related to $\gamma$ by a [[homotopy]], so that then also $f \circ \gamma'$ is related to $f \circ \gamma$ by a homotopy, then this is the statement of the homotopy lifting property of lemma \ref{CoveringSpacesHomotopyLifting}.

Next write $\bar\gamma'\cdot \gamma$ for the [[path concatenation]] of the path $\gamma$ with the [[reverse path]] of the path $\gamma'$, hence a loop in $Y$, so that $f \circ (\bar\gamma'\cdot \gamma)$ is a loop in $X$. The assumption that $f_\ast(\pi_1(Y,y)) \subset p_\ast(\pi_1(E,e))$ implies (example \ref{IfFundamentalGroupsIncludeThenfLoopsLiftToLoops}) that the path $\widehat{f \circ (\bar \gamma' \cdot \gamma)}$ which lifts this loop to $E$ is itself a loop in $E$.

By uniqueness of path lifting, this means that the lift of $f \circ ( \gamma' \cdot (\bar\gamma' \cdot \gamma) )$ coincides with that of $f \circ \gamma'$. But $\bar \gamma' \cdot (\gamma' \cdot \gamma)$ is homotopic (via reparameterization) to just $\gamma$. Hence it follows now with the first statement that the lift of $f \circ \gamma'$ indeed coincides with that of $f \circ \gamma$.

This shows that the above prescription for $\hat f$ is well defined. 

It only remains to show that the function $\hat f$ obtained this way is continuous.

Let $y' \in Y$ be a point and $W_{\hat f(y')} \subset E$ an open neighbourhood of its image in $E$. It is sufficient to see that there is an open neighbourhood $V_{y'} \subset Y$ such that $\hat f(V_y) \subset W_{\hat f(y')}$. 

Let $U_{f(y')} \subset X$ be an open neighbourhood over which $p$ trivializes. Then the restriction

$$
  p^{-1}(U_{f(y')}) \cap W_{\hat f(y')} 
    \;\subset\; 
  U_{f(y')} \times Disc(p^{-1}(f(y')))
$$ 

is an open subset of the product space. Consider its further restriction 

$$
  \left( U_{f(y')} \times \{\hat f(y')\} \right)
    \cap 
  \left( 
    p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
  \right) 
$$

to the [[leaf]] 

$$
  U_{f(y')} \times \{\hat f(y')\} \;\subset\; U_{f(y')} \times p^{-1}(f(y'))
$$

which is itself an open subset. Since $p$ is an [[open map]] ([this prop.](covering+space#CoveringProjectionsAreOpenMaps)), the subset 

$$
  p\left(
    \left(
      U_{f(y')} \times \{\hat f(y')\}
    \right)
      \cap 
    \left( 
      p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
    \right) 
  \right)
  \subset X
$$

is open, hence so is its pre-image

$$
  f^{-1}
  \left(
    p
      \left(
        \left(
          U_{f(y')} \times \{\hat f(y')\}
        \right)
          \cap 
        \left( 
          p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
        \right) 
    \right)
  \right)
    \;\subset\; 
  Y
  \,.
$$


Since $Y$ is assumed to be [[locally path-connected topological space|locally path-connected]], there exists a path-connected open neighbourhood

$$
  V_{y'}
    \subset 
  f^{-1}\left(p\left(
    \left(U_{f(y')} \times \{\hat f(y')\}\right)
      \cap 
    \left( 
      p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
    \right) 
  \right)
  \right)
  \,.
$$

By the uniqueness of pah lifting, the image of that under $\hat f$ is

$$
  \begin{aligned}
    \hat f(V_{y_'}) 
    & = 
    f(V_{y'}) \times \{\hat f(y')\} 
    \\
     & \subset
    p\left(
      \left(U_{f(y')} \times \{\hat f(y')\}\right)
        \cap 
      \left( 
        p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
      \right) 
    \right) \times \{\hat f(y')\}
    \\
    & \simeq
      \left( U_{f(y')} \times \{\hat f(y')\} \right)
        \cap 
      \left( 
        p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
      \right)   
     \\
     & \subset W_{\hat f(y')}
  \end{aligned}
  \,.
$$

It remains to show that this lift is unique if $Y$ is path-connected. (...)

=--


### Monodromy


+-- {: .num_defn #CoveringSpaceMonodromy}
###### Definition
**([[monodromy]] of a covering space)

Let $X$ be a [[topological space]] and $E \overset{p}{\to} X$ a [[covering space]]. Write $\Pi_1(X)$ for the [[fundamental groupoid]] of $X$.

Define a [[functor]]

$$
  Fib_E
    \;\colon\;
  \Pi_1(X)
    \longrightarrow
  Set
$$

to the [[category]] [[Set]] of [[sets]] as follows:

1. to a point $x \in X$ assign the [[fiber]] $p^{-1}(\{x\}) \in Set$;

1. to the [[homotopy class]] of a [[path]] $\gamma$ connecting $x \coloneqq \gamma(0)$ with $y \coloneqq \gamma(1)$ in $X$ assign the function $p^{-1}(\{x\}) \longrightarrow p^{-1}(\{y\})$ which takes $\hat x \in p^{-1}(\{x\})$ to the endpoint of a path $\hat \gamma$ in $E$ which lifts $\gamma$ through $p$ with starting point $\hat \gamma(0) = \hat x$

   $$
     \array{
       p^{-1}(x) &\overset{}{\longrightarrow}& p^{-1}(y)
       \\
       (\hat x = \hat \gamma(0)) &\mapsto& \hat \gamma(1)
     }
     \,.
   $$

This construction is well defined for a given representative $\gamma$ due to the unique path-lifting property of covering spaces ([this lemma](covering+space#CoveringSpacePathLifting)) and it is independent of the choice of $\gamma$ in the given homotopy class of paths due to the homotopy-lifting property ([this lemma](covering+space#CoveringSpacesHomotopyLifting)).  Similarly, these two lifting properties give that this construction respects composition in $\Pi_1(X)$ and hence is indeed a [[functor]].

=--

+-- {: .num_prop}
###### Proposition

Given a [[homomorphism]] between two [[covering spaces]] $E_i \overset{p_i}{\to} X$, hence a [[continuous function]] $f \colon E_1 \to E_2$ which respects [[fibers]] in that the [[diagram]]

$$
  \array{
    E_1 && \overset{f}{\longrightarrow} && E_2
    \\
    & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && X
  }
$$

[[commuting diagram|commutes]], then the component functions

$$
  f\vert_{\{x\}} \;\colon\; p_1^{-1}(\{x\}) \longrightarrow p_2^{-1}(\{x\})
$$

are compatible with the monodromy $Fib_{E}$ (def. \ref{CoveringSpaceMonodromy}) along any [[path]] $\gamma$ between points $x$ and $y$ from def. \ref{CoveringSpaceMonodromy} in that the following [[diagrams]] of [[sets]] [[commuting diagram|commute]]

$$
  \array{
     p_1^{-1}(x) &\overset{f\vert_{\{x\}}}{\longrightarrow}& p_2^{-1}(x)
     \\
     {}^{\mathllap{Fib_{E_1}([\gamma])}}\downarrow
       &&
     \downarrow^{\mathrlap{ Fib_{E_2}([\gamma]) }}
     \\
     p_1^{-1}(y) &\underset{f\vert_{\{y\}}}{\longrightarrow}& p_2^{-1}(\{y\})
  }
  \,.
$$

This means that $f$ induces a [[natural transformation]] between the monodromy functors of $E_1$ and $E_2$, respectively, and hence that constructing monodromy is itself a functor from the [[category]] of [[covering spaces]] of $X$ to that of [[permutation representations]] of the [[fundamental groupoid]] of $X$:

$$
  Fib
   \;\colon\;
  Cov(X)
    \longrightarrow
  Set^{\Pi_1(X)}
  \,.
$$

=--


+-- {: .num_example #CoveringSpaceFundamentalGroupoid}
###### Example
**([[fundamental groupoid]] of covering space)

Let $E \overset{p}{\longrightarrow} X$ be a covering space.

Then the [[fundamental groupoid]] $\Pi_1(E)$ of the total space $E$ is
[[equivalence of categories|equivalently]] the [[Grothendieck construction]]
of the [[monodromy]] functor $Fib_E \;\colon\; \Pi_1(X) \to Set$

$$
  \Pi_1(E)
   \;\simeq\;
  \int_{\Pi_1(X)} Fib_E
$$

whose

* [[objects]] are pairs $(x,\hat x)$ consisting of a point $x \in X$ and en element $\hat x \in Fib_E(x)$;

* [[morphisms]] $[\hat \gamma] \colon (x,\hat x) \to (x', \hat x')$ are morphisms $[\gamma] \colon x \to x'$ in $\Pi_1(X)$ such that $Fib_E([\gamma])(\hat x) = \hat x'$.

=--


+-- {: .proof}
###### Proof

By the uniqueness of the path-lifting, lemma \ref{CoveringSpacePathLifting} and the very definition of the [[monodromy]] functor.

=--

+-- {: .num_prop #CoveringConnectivityViaMonodromy}
###### Proposition

Let $X$ be a [[path-connected topological space]] and let $E \overset{p}{\to} X$ be a [[covering space]]. Then the total space $E$ is 

1. [[path-connected topological space|path-connected]] precisely if the [[monodromy]] $Fib_E$ is a [[transitive action]];

1. [[simply connected topological space|simply connected]] precisely if the [[monodromy]] $Fib_E$ is [[free action]].

=--

+-- {: .proof}
###### Proof

By example \ref{CoveringSpaceFundamentalGroupoid}.

=--




### Reconstructing covering spaces from monodromy

Given a [[permutation representation]] of the [[fundamental groupoid]]
of a locally path-connected and semi-locally simply connected space, there is a construction of _[[reconstructing covering spaces from monodromy]]_, which is a [[functor]] of the form

$$
  Rec \;\colon\; Set^{\Pi_1(X)} \longrightarrow Cov(X)
  \,.
$$


### Fundamental theorem of covering spaces
 {#FundamentalTheoremOfCoveringSpaces}


+-- {: .num_theorem #FundamentalTheoremOfCoveringSpaces}
###### Theorem
**([[fundamental theorem of covering spaces]])**

Let $X$ be a [[locally path-connected topological space|locally path-connected]] and [[semi-locally simply-connected topological space]]. Then the operations on 

1. extracting the [[monodromy]] $Fib_{E}$ of a [[covering space]] $E$ over $X$ 

1. [[reconstructing a covering space from monodromy]] $Rec(\rho)$

constitute an [[adjoint equivalence|adjoint]] [[equivalence of categories]]

$$
  Cov(X)
    \underoverset
      {\underset{Fib}{\longrightarrow}}
      {\overset{Rec}{\longleftarrow}}
      {\bot}
  Set^{\Pi_1(X)}
$$

between the [[category of covering spaces]] and the [[permuation representation|permutation]] [[groupoid representations]] of the [[fundamental groupoid]] of $X$.

=--




### Universal covering space


... _[[universal covering space]]_ 


## Examples 


### Universal covering space in terms of homotopy fibers {#HomotopyFibs}

We want to describe here how the universal covering space of $X$ is the [[homotopy fiber]] of the canonical morphism $X \to \Pi_1(X)$, hence the $\Pi_1(X)$-[[principal bundle]] classified by this [[cocycle]].

We place ourselves in the context of [[topological ∞-groupoid]]s and regard both the space $X$ as well as its [[schreiber:path ∞-groupoid]] $\Pi(X)$ and its truncation to the [[fundamental groupoid]] $\Pi_1(X)$ as objects in there.

The canonical morphism $X \to \Pi(X)$ hence $X \to \Pi_1(X)$ given by the inclusion of contant paths may be regarded as a [[cocycle]] for a $\Pi(X)$-[[principal ∞-bundle]], respectively for a $\Pi_1(X)$-principal bundle.

Let $\pi_0(X)$ be the set of connected components of $X$, regarded as a topological $\infty$-groupoid, and choose any [[section]]  $\pi_0(X) \to \Pi(X)$ of the projection $\Pi(X) \to \pi_0(X)$.

Then the $\Pi(X)$-principal $\infty$-bundle classified by the [[cocycle]] $X \to \Pi(X)$ is its [[homotopy fiber]], i.e. the [[homotopy pullback]]

$$
  \array{
    UCov(X) &\to& \pi_0(X)
    \\
    \downarrow && \downarrow
    \\
    X &\to& \Pi(X)
  }
  \,.
$$

We think of this topological $\infty$-groupoid $UCov(X)$ as the **universal covering $\infty$-groupoid** of $X$. To break this down, we check that its [[decategorification]] gives the ordinary universal covering space: 

for this we compute the [[homotopy pullback]]

$$
  \array{
    UCov_1(X) &\to& {*}
    \\
    \downarrow && \downarrow^{\mathrlap{x}}
    \\
    X &\to& \Pi_1(X)
  }
  \,,
$$

where we assume $X$ to be connected with chosen baspoint $x$ just to shorten the exposition a little. By the laws of [[homotopy pullback]]s in general and [[homotopy fiber]]s in particular, we may compute this as the ordinary [[pullback]] of a weakly equivalent diagram, where the point $*$ is resolved to the [[generalized universal bundle|universal]] $\Pi_1(X)$-principal bundle

$$
  \mathbf{E}_x \Pi_1(X) = T_x \Pi_1(X)
  \,.
$$

> (More in detail, what we do behind the scenes is this: we regard the diagram as a diagram in the _global_ [[model structure on simplicial presheaves]] on [[Top]]. In there all our topological groupoids are fibrant, hence all we have to ensure is that one of the morphisms of the diagram becomes a fibration, which is what the passage to $\mathbf{E}_x \Pi_1(X)$ achieves. Then the ordinary pullback in the category of simplicial presheaves is the homotopy pullback in $\infty$-prestacks. Then by left exactness of $\infty$-stackification, the image of that in $\infty$-stacks is still a homotopy pullback. )

The topological groupoid $\mathbf{E}_x \Pi_1(X)$ has as objects homotopy classes rel endpoints of paths in $X$  starting at $x$ and as morphisms $\kappa : \gamma \to \gamma'$ it has commuting triangles

$$
  \array{
    && x
    \\
    &{}^{\mathllap{\gamma}}\swarrow && \searrow^{\mathrlap{\gamma'}}
    \\
    y &&\stackrel{\kappa}{\to}&& y'
  }
$$

in $\Pi_1(X)$. The topology on this can be deduced from thinking of this as the [[pullback]]


$$
  \array{
   \mathbf{E}_x \Pi_1(X) &\to& {*}
   \\
   \downarrow && \downarrow^{\mathrlap{x}}
   \\
   \Pi_1(X)^I &\stackrel{d_0}{\to}& \Pi_1(X)
  }
$$

in simplicial presheaves on [[Top]]. Unwinding what this means we find that the open sets in $Mor(\mathbf{E}_x \Pi_1(X))$ are those where the endpoint evaluation produces an open set in $X$.

Now it is immediate to read off the homotopy pullback as the ordinary pullback

$$
  \array{
    UCov_1(X) &\to& \mathbf{E}_x \Pi_1(X)
    \\
    \downarrow && \downarrow
    \\
    X &\to& \Pi_1(X)
    \,.
  }
$$

Since $X$ is categorically discrete, this simply produces the space of objects of $\mathbf{E}_x \Pi_1(X)$ over the points of $X$, which is just the space of all paths in $X$ starting at $x$ with the projection $UCov_1(X) \to X$ being endpoint evaluation. 

This indeed is then the usual construction of the universal covering space in terms of paths, as described for instance in  ([Dahlke](#Dahlke))



## Related concepts

* [[branched covering space]]

## References

A textbook acccount is in 

* {#tomDieck06} [[Tammo tom Dieck]], sections 2 an 3 of _Algebraic Topology_, EMS 2006 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/diecktop.pdf))


Review includes

* {#Moller11} [[Jesper Møller]], _The fundamental group and covering spaces_ (2011) ([pdf](http://www.math.ku.dk/~moller/f03/algtop/notes/covering.pdf))

* [[Ronnie Brown]], chapter 11 of _[Topology and Groupoids](http://pages.bangor.ac.uk/~mas010/topgpds.html)_

* {#Dahlke} Karl Dahlke, _[Covering spaces, Building a universal cover](http://www.mathreference.com/at-cov,build.html)_ , [Math Reference Project](http://www.mathreference.com/) 

Some of the problems of generalising covering spaces to deal with  wild spaces are dealt with in:

* {#Brazas12} Jeremy Brazas, _Semicoverings_, Homology, Homotopy and Applications, 14 (2012), No. 1, 33-63. 





[[!redirects covering spaces]]
[[!redirects wrapping space]]
[[!redirects wrapping spaces]]
[[!redirects covering groupoid]]


