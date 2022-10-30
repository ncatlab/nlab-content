If $A$ is a category and $I$ a small category then we can consider the [[category of functors]] $A^I$, whose objects are the functors from $I$ to $A$. If $A$ admits limits of shape $I$, then the limit $lim = lim_I:A^I\to A$ is a functor which is right adjoint to the constant diagram functor hence it commutes with limits, and in particular it is left exact. 

If $A$ has some notion of homotopy theory then usually $A^I$ has the notion as well (e.g. if we work with model category structures or say Abelian categories) hence we can then form right derived functors of $lim$ which are usually denoted $lim^n$ and called the derived limit functors. As usual we can also assemble them into the [[total right derived functor]] $\mathbb{R}lim$. 

An important example is where $A$ is a category of modules over a commutative ring, then one has $Ch(A)$ and any $M:I\to A$ can be thought of as $M:I\to Ch(A)$ by thinking of each $M(i)$ as being a chain complex concentrated in dimension 0.


Related entries include [[homotopy limit]], [[lim^1 and Milnor sequences]]


##References
A proof that derived limit functors give invariants of a corresponding pro-obect can be found in

* [[John Duskin]], _Pro-objects (after Verdier)_, S&#233;m. Heidelberg- Strasbourg1966 -67, Expos&#233; 6, I.R.M.A.Strasbourg.

Some results on the vanishing of 'derived limits' are in

* [[Barbara Osofsky]], _The subscript of $\aleph_n$ projective dimension, and the vanishing of $lim^{(n)}$_, Bull. Amer. Math. Soc. Volume 80, Number 1 (1974), 8-26.

[[!redirects derived limit functors]]
[[!redirects lim^n]]