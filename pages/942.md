The **profinite completion** $G^$ of a group $G$ is the limit over the diagram with objects the quotient groups $G/N_{fin}$ where $N_{fin}$ is a finite index, normal subgroup of $G$, and arrows induced from the lattice of subgroups of $G$. Note that the profinite completion actually is a [[profinite group]], and there is a canonical homomorphism $G \to G^$.

+-- {: .query}
I can't seem to get the caret to work, having tried the usual LaTeX command, and variations, I'll leave it to the next TeXpert to come along.

=-- {: .query}

More abstractly, the profinite completion can be defined as a profinite group $P$ with a homomorphism $\phi:G\to P$, such that if we are given any other profinite group $P'$ and homomorphism $\psi:G \to P'$, there is a unique homomorphism $P \to P'$ making the obvious triangle commute.


An example that comes up in practice is the profinite completion of the fundamental group of an complex projective variety $X$. Since $X$ has an underlying topological space, its fundamental group of loops $\pi_1^{top}(X)$ can be defined in the usual way. But one can also define the [[fundamental group a la Grothendieck]] $\pi_1^{alg}(X)$, as the automorphisms of the fibre functor from the category of finite covering spaces of $X$. This is a profinite group, which isomorphic to the profinite completion of $\pi_1^{top}(X)$.