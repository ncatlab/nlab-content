
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _hypothèse inspiratrice_ or _inspiring assumption_  is an assumption formulated by [[Grothendieck]] in _[[Pursuing Stacks]]_, that the [[category]] of auto-[[equivalence of categories|equivalences]] of the [[classical homotopy category]] is [[equivalence of categories|equivalent]] to the [[final category]]. See below for Grothendieck's own formulation of it. It has not been proven in its original form.

## Proofs of lifts of the assumption

The _hypothèse inspiratrice_ can be proven relatively easily if one re-formulates the question for a lift of the homotopy category to [[derivator|derivators]], [[(∞,1)-category theory|(∞,1)-category]], or some other such setting for [[homotopy theory]]. One such [[proof]] is given in [Cisinski 08](#Cisinski08). A different proof is given in [Toën-Vezzosi 02](#ToenVezzoi02), as the case $X=1$ of Corollary 5.2.2. 

## Proof of the analogous statement for the category of sets

\begin{prpn} The category of auto-equivalences of [[Set]] is equivalent to the final category. \end{prpn}

\begin{proof} Any equivalence of categories preserves [[colimit|colimits]]. Since [[Set]] is the [[free co-completion]] of the final category $1_{\mathsf{Cat}}$, and since $1_{\mathsf{Cat}}$ is sent to $1_{\mathsf{Set}}$ under the Yoneda embedding, any auto-equivalence $F$ of [[Set]] is determined uniquely, up to isomorphism, by $F(1_{\mathsf{Set}})$. 

Now, equivalences of categories also preserve [[final object|final objects]]. Thus we have that $F(1_{\mathsf{Set}}) = 1_{\mathsf{Set}}$ for all $F$.

The proposition follows immediately from these two observations. \end{proof}

This argument is rather canonical. In principle, it 'should' lift to a proof of the hypothèse inspiratrice, simply by replacing set-theoretic notions by homotopy-theoretic ones: colimits by homotopy colimits, and so on. And this does work, but with the caveat that such a proof can only be formulated if one works inside 'homotopy category theory' rather than ordinary category theory. 

## Undirected version

The original hypothèse inspiratrice is about the homotopy *1-category*, and its lifted versions are about the corresponding *$(\infty,1)$-category* of homotopy types ($\infty$-groupoids).  One might formulate an analogous conjecture about the *$\infty$-groupoid* of $\infty$-groupoids (or about its 0-truncation, the set of equivalence classes of $\infty$-groupoids).  But here the situation is rather different.

If we assume the law of [[excluded middle]], then there definitely exist nontrivial automorphisms of the $\infty$-groupoid of homotopy types.  For instance, if $X$ and $Y$ are two homotopy types that themselves have no nontrivial automorphisms (such as the [[empty set]] and the [[terminal set]]), then there is an automorphism of the $\infty$-groupoid of homotopy types that switches $X$ and $Y$ and leaves everything else fixed.  See for instance [[Vladimir Voevodsky|Voevodsky]]'s comment in [this thread](https://groups.google.com/d/msg/homotopytypetheory/Wyxmcvo5K2Y/SUm3nwYECQAJ) on the HoTT mailing list.  This requires excluded middle because we have to decide, for each homotopy type, whether it is equivalent to $X$ or to $Y$ or to neither.

It is not known whether any nontrivial automorphisms of the $\infty$-groupoid of homotopy types can be constructed without excluded middle.  (To talk about homotopy types without assuming excluded middle, it is best to work in constructive [[homotopy type theory]].)  But it is known that certain kinds of such automorphisms (e.g. those that move the empty set) do imply excluded middle or some other nonconstructive axiom; see [BELS](#BELS17).


## Grothendieck's formulation

The original formulation in _[[Pursuing Stacks]]_ (page 30 in the pagination of the original document, section 28, 8th of March 1983) is preceded by

> Now this maybe isnt [sic] so silly after all, in view of the following 
>
> Assumption: The category of equivalences of $(Hot)$ with itself, and of natural isomorphisms (possibly even any morphisms) between such, is equivalent to the one point category.
>
>   This means 1) any equivalence $(Hot) \stackrel{\approx}{\to} (Hot)$ is isomorphic to the identity functor, and 2) any automorphism of the identity functor (possibly even any endomorphism ?) is the identity.
>
>   Maybe these are facts well-known to the experts, maybe not - it is not my business here anyhow to prove such kind of things. It looks pretty plausible , because if there was any non trivial autoequivalence of $(Hot)$, or automorphism of its identity functor, I guess I would have heard about it, or something of the sort would flip to my mind. It would not be so if we abelianized $(Hot)$ some way or other, as there would be the loop and suspension functor, and homotheties by $-1$ of $id_{(Hot)}$.

It most copies of Pursuing Stacks available, the assumption itself is blacked out. Tim Porter suggests that this is likely due to the text having been highlighted, probably in yellow, leading to the blacking out upon photocopying. Because of the blacking out, the assumption is also not available in circulating typed versions of Pursuing Stacks. Happily, Tim Porter has scanned _[[page 30.pdf|here:file]]_ the relevant page from his personal copy of Pursuing Stacks. The assumption is about mid-page. 

Later on (page 71 in the pagination of the original document, section 41, around the 24th of March 1983), Grothendieck writes the following.

> One comment still, upon the role played in the theory I am developing of the assumption (p.30) that the category of autoequivalences of $(Hot)$ is equivalent to the final category. This assumption has been a crucial guide for putting the emphasis where it really belongs, namely upon the set $W \subset Fl(H)$ of weak equivalences within a category $H$ [letter is a bit illegible] which one would like to take in some sense as a category of models for homotopy types -  the functors $H \rightarrow (Hot)$ following along automatically. However, in no statement whatever I proved so far, was this assumption ever used. On the other hand, the notion of a _modelizer_ introduced in the wake of the `assumption'' (of p.31) [this seems like a typo, presumably it should be p.30] was tacitly changed during the reflection, ...

Slightly later again (page 73, section 42, 25th of March 1983, the following is written, introducing the phrase "inspiring assumption":

> This is indeed very much in the spirit of the "inspiring assumption" of p.30, that the category of autoequivalences of $(Hot)$ is equivalent to the unit category, which implies indeed that for two categories $H, H'$ equivalent to $(Hot)$, there is a unique isomorphism between them.

A further reference comes on page 80-81, section 44, 26th of March 1983.

> But it is so if we grant the "inspiring assumption", implying that any autoequivalence of $(Hot)$ is isomorphic to the identity functor

And again on page 86, still on the same day.

> If we admit the "inspiring assumption" that any autoequivalence of $(Hot)$ is uniquely isomorphic to the identity functor, it will follow that the autoequivalence $(Hot) \rightarrow (Hot)$ induced by (11) (where again $i$ is any weak test functor) is canonically isomorphic to the identity.

Next is a reference on pg.93, section 46, probably the 28th or 29th of March 1983.

> (If we admit the "inspiring assumption", there is no real choice, as a matter of fact - but we don't want to use this in a technical sense, but only as a guide and motivation.)

There is also a reference on pg.216-217, section 72, 10th of June 1983.

> This is of course very much in keeping with the "inspiring assumption" (section 28), which just means that up to unique isomorphism, there is indeed but _one_ equivalence from $Hot_B$ to $Hot_A$ (both categories being equivalent to $Hot(\underline{W})$. Here we are thinking of the extension of the "assumption" contemplated earlier, when usual weak equivalence is replaced by a basic localizer $\underline{W}$ as above. It seems plausible that the assumption holds true in all cases - anyhow we did'nt [sic] have at any moment to make explicit use of it (besides at a moment drawing inspiration from it...).

The final reference is on pg.273, section 83, probably the 27th or 28th of June 1983.

> Here also arises the question whether a functor $\phi: M \rightarrow Hot_{\underline{W}}$ stemming from a contractibility structure $M_{c}$ on $M$ can have non trivial automorphisms - a question closely connected to the "inspiring assumption" of section 28.

## References

* {#Cisinski08} [[Denis-Charles Cisinski]], _Propriétés universelles et extensions de Kan dérivées_, Theory Appl. Categ. 20, 605-649 (2008). [Link to article](http://www.tac.mta.ca/tac/volumes/20/17/20-17abs.html)

* {#ToenVezzoi02} [[Bertrand Toën]] and [[Gabriele Vezzosi]], _Segal topoi and Segal stacks over them_, [arXiv:math/0212330](https://arxiv.org/abs/math/0212330).

* {#BELS17} [[Auke Booij]], [[Martín Escardó]], [[Peter Lumsdaine]], [[Michael Shulman]].  _Parametricity, automorphisms of the universe, and excluded middle_, [arXiv:1701.05617](https://arxiv.org/abs/1701.05617)


[[!redirects inspiring assumption]]