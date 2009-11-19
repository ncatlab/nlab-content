
##Idea and discussion##
In &#268;ech cohomology, in its *traditional* form, you resolve the space by a inverse system  or [[pro-object]], $\check{C}(X,-)$, of nerves of open covers (or if you prefer the nerves of the corresponding sheaf  of groupoids). For constant and Abelian coefficients (and we will keep to those for the moment), $A$, we throw $H^n(-,A)$ at this pro-object.  As cohomology switches 'variance' we get a _direct system_ or _ind-object_ of Abelian groups, and usually we then take its (direct) limit (i.e. its colimit) to get $\check{H}^n(X,A)$.

Now dualise ... .  Replace cohomology by homotopy $[A,-]$, but although there will be some very useful long exact (Puppe) sequences available in homotopy, we cannot go this way to get them!  In dualising, things can go slightly 'wrong'. We have $[A,\check{C}(X,-)]$ is a pro-object and so we should take limits not colimits to get thet thing we want, but $lim$ is not an exact functor on the usual categories available here, such as groups, sets, modules, etc. 

There is another problem, coherence!  $\check{C}(X,-)$ is a pro-object in the homotopy category of simplicial sets, not in the category of simplicial sets itself.  It is a homotopy coherent system, but the choices of covering refinement maps cause the problem.  

We are very near the topics discussed in [[shape theory]], [[Cech methods]] and [[strong shape theory]] (when that has been written!).
One interpretation of &#268;ech homotopy is shape theory, but that does not usually handle the 'homotopy is dual to cohomology' idea so this will need more work here.

##Handling the problem of coherence##


*  **Using homotopy coherence directly** As explained in [[Čech methods]], given an open cover $\beta$ of a space $X$ and a refinement $\alpha$ of $U$
for a given set in $V$ there may be many different sets in $U$ containing it, so the seemingly natural way to get a simplicial map

$$\check{C}(X,\alpha)\to \check{C}(X,\beta)$$

involves a choice, We choose a 'refinement mapping' $\varphi : \alpha \to \beta$ so that 
for each $V\in \alpha$, $V\subseteq \varphi(V)$. There is an obvious extension to $n$-simplices.  We send $\langle V_0, \ldots, V_n\rangle$ to $\langle \varphi(V)_0, \ldots, \varphi(V)_n\rangle$. This still does not get us a functor from $Cov(X)$ to $SSets$. The fact that we had to choose make it unlikely in the extreme that given three (or more) covers, each a refinement of the next, that the resulting diagram of simplicial sets will turn out (by some miracle) to be commutative. However once we choose a refinement maps for each pair $(\alpha,\beta)$, we _do_ get a [[homotopy coherent diagram]]

$$\check{C}(X,-) : Cov(X)\to SSets.$$

with the coherence being spelled out completely.

*  **Using the Vietoris complex** The [[Vietoris complex]] is an alternative way of obtaining a simplicial complex (or simplicial set) from a space $X$ and an open cover $\alpha$. The disadvantage of it is that whilst the nerve of the open cover would be a finite simplicial set if the open cover is finite (for instance this is useful when handling compact spaces as we can replace the indexing set of _all_ open covers by that of _finite open covers_ without changing the result up to isomorphism), the Vietoris complex has as many vertices as there are points in $X$. It has the advantage that the induced maps between the simplicial complexes are independent of the choice of refinement maps so we do get a pro-simplicial set, $V(X,-) : Cov(X)\to SSet$. We therefore get a well defined pro-homotopy type $V(X)$ in the homotopy category $Ho(pro-SSet)$.  (The category $pro-SSet$ has various [[model category]] structures and [[cofibration category]] structures, with the same basic notion of homotopy equivalence.

How are the two ways around the coherence problem related? 

There is a result [[Dowker's Theorem]] which shows that the geometric realisations of $V(X,\alpha)$ and $\check{C}(X,\alpha)$ are homotopy equivalent. (This explains why &#268;ech and Vietoris homology are isomorphic.) Given a commutative diagram of spaces (or simplicial sets), if you change some of the
spaces by homotopy equivalent spaces then you can build from those new spaces a homotopy coherent diagram equivalent to the original one. Using Dowker's theorem we get that $\check{C}(X,-)$ is a homotopy coherent diagram, (by a second route).

+--{: .query}
That is a start on it anyhow!
=--


[[!redirects Čech homotopy]]
