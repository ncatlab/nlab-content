The **localization** of a [[category]] $C$ at a class of [[morphism]]s $W$ is the universal solution to making the morphisms in $W$ into [[isomorphism]]s; it is written $C[W^{-1}]$ or $W^{-1}C$.

This (perhaps confusing) terminology is by analogy with localization of rings, and also gives its name to [[Bousfield localization]] of [[model category|model categories]].  In 2-categorical language, $C[W^{-1}]$ is the [[coinverter]] of the canonical natural transformation $s\to t$, where $s,t:W\to C$ are the "source" and "target" functors and $W$ is considered as a full subcategory of the [[arrow category]] $C ^{\mathbf{2}}$.

+-- { .query}
[[Zoran Skoda]] Mike, why do you say confusing? First of all localization of a ring induces localization of categories of 1-sided modules by tensoring with the localized ring over original ring and conversely applying localization functor to a ring itself produces the localized ring. The canonical morphism from the ring to its localization, sometimes also called localization, is the adjunction morphism indexed by the ring. The localization functor is just a natural extension of the localization from a ring to all modules over the ring not just the ring itself. The same for corresponding (components of) the adjunction morphisms 
in that case.

Second, if one does special case when localizations can be made via categories of fractions then Ore conditions are literally Ore conditions from the theory of localization of monoids 
or rings (besides a monoid is just a category with one object). Third, [[Bousfield localization]] in triangulated setup is a localization associated to an idempotent monad just like usual flat localization (or any localization having faithfully flat right adjoint), just
the functors are triangulated, and the monad is Z-graded.
Finally Cohn universal localization is just H_0 of Bousfield localization and in the matrix form one is essentially solving the Ore condition, as it is shown by Malcolmson and 
independently and earlier Gerasimov. In fact when one restricts the Cohn localization to finitely generated projectives one has a flat localization. So it is not just an analogy -- these are all special cases of the **same** picture and mechanism. 
=--

If $C$ is [[large category|large]], then the existence of $C[W^{-1}]$ may depend on [[foundations]], and it will not necessarily be [[locally small category|locally small]] even if $C$ is.  The tools of [[homotopy theory]], and in particular [[model category|model categories]], can be used to address this question.
