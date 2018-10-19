
Which can be restated in terms of representable profunctors as follows.
A cwf consists of

1. a category $C$,
2. a presheaf $Ty : \hat C$ of types in context.
3. a presheaf $Tm : \widehat {\int Ty}$ of typed terms in context.
4. a functor $ext : \widehat {\int Ty} \to C$ of context extension that represents the profunctor ${\int Tm}(-,ty=) \odot {\int Tm}(ctx(ty(-)),=) : \int Ty &#8696; C$ where $ty : \int Tm \to \int Ty$ and $ctx : \int Ty \to C$ are the projections of the [[Grothendieck construction]].

Writing the profunctor as P, it is equivalent to the following definition:

$$P(\Delta, (\Gamma, A)) = (\gamma : \Delta \to \Gamma) \times (a : Tm(\Gamma, A[\gamma]))$$

then the universal property of the context extension is that there is a natural isomorphism $\Delta \to ext(\Gamma, A) \cong P(\Delta,(\Gamma,A))$