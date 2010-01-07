Let $H\colon A &#8696;B$ be a [[profunctor]], i.e. a functor $B^{op}\times A\to Set$.  Its **cograph**, also called its **collage**, is the [[category]] $\bar{H}$ whose set of objects is the [[disjoint union]] of the sets of objects of $A$ and $B$, and where

$$ \begin{aligned}
  \bar{H}(a_1,a_2) &= A(a_1,a_2)\\
  \bar{H}(b_1,b_2) &= B(b_1,b_2)\\
  \bar{H}(b,a) &= H(b,a)\\
  \bar{H}(a,b) &= \emptyset
  \end{aligned}
$$

where composition is defined as in $A$, $B$, and according to the actions of $A$ and $B$ on $H$.

The [[cograph of a functor]] is the special case when $H$ is a "representable profunctor" of the form $B(f-,-)$ for some functor $f\colon A\to B$.

The cograph of a profunctor can be given a universal property: it is the [[lax colimit]] of that profunctor, considered as a single arrow in the [[bicategory]] of profunctors.  (The word "collage" is also sometimes used more generally for any lax colimit, especially in a $Prof$-like bicategory.)  The cograph of a profunctor is also a [[cotabulation]] in the [[proarrow equipment]] of profunctors.  Furthermore, the [[cospans]] $A\to \bar{H} \leftarrow B$ which are cographs of profunctors can be characterized as the [[Grothendieck fibration|two-sided codiscrete cofibrations]] in the [[2-category]] [[Cat]].

All of this can be generalized to [[enriched categories]] and also to [[higher category theory|higher categories]].
