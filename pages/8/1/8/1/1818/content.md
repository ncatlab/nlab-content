# &#268;ech homotopy
* table of contents
{: toc}


##Idea and discussion##
In &#268;ech cohomology, in its *traditional* form, you resolve the space by an inverse system  or [[pro-object]], $\check{C}(X,-)$, of nerves of open covers (or if you prefer the nerves of the corresponding sheaf  of groupoids). For constant and Abelian coefficients (and we will keep to those for the moment), $A$, we throw $H^n(-,A)$ at this pro-object.  As cohomology switches 'variance' we get a _direct system_ or _ind-object_ of Abelian groups, and usually we then take its (direct) limit (i.e. its colimit) to get $\check{H}^n(X,A)$.

Now dualise ... .  Replace cohomology by homotopy $[A,-]$, but although there will be some very useful long exact (Puppe) sequences available in homotopy, we cannot go this way to get them!  In dualising, things can go slightly 'wrong'. We have $[A,\check{C}(X,-)]$ is a pro-object and so we might want to take limits not colimits to get the thing we want, but $lim$ is not an exact functor on the usual categories available here, such as groups, sets, modules, etc. 

There is another problem, coherence!  $\check{C}(X,-)$ is a pro-object in the homotopy category of simplicial sets, not in the category of simplicial sets itself.  It is a homotopy coherent system, but the choices of covering refinement maps cause the problem.  

We are very near the topics discussed in [[shape theory]], [[Čech methods]] and [[strong shape theory]] (when that has been written!).
One interpretation of &#268;ech homotopy is shape theory, but that does not usually handle the 'homotopy is dual to cohomology' idea so this will need more work here.

##Handling the problem of coherence##


*  **Using homotopy coherence directly** As explained in [[Čech methods]], given an open cover $\beta$ of a space $X$ and a refinement $\alpha$ of $U$
for a given set in $V$ there may be many different sets in $U$ containing it, so the seemingly natural way to get a simplicial map

$$\check{C}(X,\alpha)\to \check{C}(X,\beta)$$

involves a choice. We choose a 'refinement mapping' $\varphi : \alpha \to \beta$ so that 
for each $V\in \alpha$, $V\subseteq \varphi(V)$. There is an obvious extension to $n$-simplices.  We send $\langle V_0, \ldots, V_n\rangle$ to $\langle \varphi(V)_0, \ldots, \varphi(V)_n\rangle$. This still does not get us a functor from $Cov(X)$ to $SSets$. The fact that we had to choose make it unlikely in the extreme that given three (or more) covers, each a refinement of the next, that the resulting diagram of simplicial sets will turn out (by some miracle) to be commutative. However once we choose a refinement maps for each pair $(\alpha,\beta)$, we _do_ get a [[homotopy coherent diagram]]

$$\check{C}(X,-) : Cov(X)\to SSets.$$

with the coherence being spelled out completely.

*  **Using the Vietoris complex** The [[Vietoris complex]] is an alternative way of obtaining a simplicial complex (or simplicial set) from a space $X$ and an open cover $\alpha$. The disadvantage of it is that whilst the nerve of the open cover would be a finite simplicial set if the open cover is finite (for instance this is useful when handling compact spaces as we can replace the indexing set of _all_ open covers by that of _finite open covers_ without changing the result up to isomorphism), the Vietoris complex has as many vertices as there are points in $X$. It has the advantage that the induced maps between the simplicial complexes are independent of the choice of refinement maps so we do get a pro-simplicial set, $V(X,-) : Cov(X)\to SSet$. We therefore get a well defined [[pro-homotopy type]] $V(X)$ in the homotopy category $Ho(pro-SSet)$.  (The category $pro-SSet$ has various [[model category]] structures and [[cofibration category]] structures, with related basic notions of homotopy equivalence. These are discussed in the entry on [[pro-homotopy theory]].)

How are the two ways around the coherence problem related? 

There is a result [[Dowker's Theorem]] which shows that the geometric realisations of $V(X,\alpha)$ and $\check{C}(X,\alpha)$ are homotopy equivalent. (This explains why &#268;ech and Vietoris homology are isomorphic.) Given a commutative diagram of spaces (or simplicial sets), if you change some of the
spaces by homotopy equivalent spaces then you can build from those new spaces a homotopy coherent diagram equivalent to the original one. Using Dowker's theorem we get that $\check{C}(X,-)$ is a homotopy coherent diagram, (by a second route).

### Homotopy groups or homotopy progroups?

One obvious case to investigate of the above is to take a pointed space $X$, apply the $n^th$ homotopy group functor $\pi_n = [S^n, -]$ to the &#268;ech or Vietoris complex to get a progroup $\pi_n(\check{C}(X))$. This will lead to long exact sequences for pairs, fibrations etc., but these will be of progroups so are less amenable to study. If on the other hand you take the limit of these progroups, as mentioned above, you destroy the exactness of the sequences and thus, to a large extent, the simplicity of their use.


## Definition

The **$n^{th}$ &#268;ech homotopy group** of a pointed space $X$ is defined to be $\check{\pi_n}(\check{C}(X)) = lim \pi_n(\check{C}(X))$.


## Examples

If $X$ is compact metric then it has countable cofinal subcategories of covers, so the progroups 
$\pi_n(\check{C}(X))$ can be replaced up to isomorphism by inverse sequences, indexed by the natural numbers.  (These are sometimes called *towers*.) 

Here are two specific examples:

1. The [[Warsaw circle]], $S_W$:  The progroup $\pi_1(\check{C}(S_W))$ is isomorphic to the  constant tower with value $C_\infty$,  the bonding maps being the identity maps.

1. The [[dyadic solenoid]]: This time the progroup is isomorphic in $Pro(Groups)$ to the inverse sequence

$$C_\infty\stackrel{a}{\leftarrow} C_\infty\stackrel{a}{\leftarrow}C_\infty\stackrel{a}{\leftarrow}C_\infty\stackrel{a}{\leftarrow}C_\infty\stackrel{a}{\leftarrow}\ldots $$
where if $c$ is the generator of $C_\infty$, $a(c) = c^2$.

This second example is certainly not isomorphic to a constant one. Note that it has trivial limit group, so is it possible to get some 'useful' limiting information from the progroup by taking some other type of 'limiting' approach?  Yes.  There are two related ways.

* **The [[derived functors of lim]]**.  Applied to the above progroup you get a definite measure of the non-triviality of the progroup. (This example is in that entry.)

* (A second method will be put here but will need additional work over on [[proper homotopy theory]].)

+--{: .query}
That is a start on it anyhow!
=--


[[!redirects Čech homotopy]]
[[!redirects Cech homotopy]]
