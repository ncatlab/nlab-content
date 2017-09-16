The **profinite completion** $\hat{G}$ of a (discrete) group $G$ is the limit (in the category of [[topological group]]s) over the diagram with objects the [[quotient group]]s $G/N_{fin}$ where $N_{fin}$ is a [[normal subgroup]] of $G$ with finite index, and arrows induced from the lattice of subgroups of $G$. Note that the profinite completion actually is a [[profinite group]], and there is a canonical homomorphism $G \to \hat{G}$.

+-- {: .query}
I can't seem to get the caret to work, having tried the usual LaTeX command, and variations, I'll leave it to the next TeXpert to come along.

[[Tim Porter|Tim]]:  Three points: (i) I suggest a hat $\hat{G}$ as notation for completion, (ii) in taking limits you have to specify in what category your are living at that instant!  Here it is not the limit in the category of groups that has to be taken but withing the category of topological groups, so you have to consider each finte group as a discrete topological group.  Because of this (iii) the actual entry on [[profinite group]] takes one to be a [[pro-object]] in the category of finite groups. (The way to handle this may need to be discussed to get consensus on which we all like best.)

I am not sure what name the SGA1 type fundamental group should be called. I do not particularly like the one you use below.

[[David Roberts]]: This was a knock-together job, I must admit. Actually I think the SGA1 fundamental group is called the algebraic fundamental group - in the case of schemes its also called the etale fundamental group, but I personally think 'algebraic' would fit better in this example - it is changed!

I'll also leave off the description of this object to its own page. Sometime I'll also get around to writing about [[Grothendieck's Galois theory]].
=-- {: .query}

More abstractly, the profinite completion can be defined as a [[profinite group]] $P$ with a homomorphism $\phi:G\to P$, such that if we are given any other profinite group $P'$ and homomorphism $\psi:G \to P'$, there is a unique homomorphism $P \to P'$ making the obvious triangle commute.


An example that comes up in practice is the profinite completion of the fundamental group of an complex projective variety $X$. Since $X$ has an underlying topological space, its [[fundamental group]] of loops $\pi_1^{top}(X)$ can be defined in the usual way. But one can also define the [[algebraic fundamental group]] $\pi_1^{alg}(X)$. This is a profinite group, which is isomorphic to the profinite completion of $\pi_1^{top}(X)$.