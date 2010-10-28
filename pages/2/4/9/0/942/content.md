##Idea##

The **profinite completion** $\hat{G}$ of a (discrete) group $G$ is the limit (in the category of [[topological group]]s) over the diagram with objects the [[quotient group]]s $G/N_{fin}$ where $N_{fin}$ is a [[normal subgroup]] of $G$ with finite index, and arrows induced from the lattice of subgroups of $G$. Note that the profinite completion actually is a [[profinite group]], and there is a canonical homomorphism $G \to \hat{G}$.

+-- {: .query}
I can't seem to get the caret to work, having tried the usual LaTeX command, and variations, I'll leave it to the next TeXpert to come along.

[[Tim Porter|Tim]]:  Three points: (i) I suggest a hat $\hat{G}$ as notation for completion, (ii) in taking limits you have to specify in what category your are living at that instant!  Here it is not the limit in the category of groups that has to be taken but withing the category of topological groups, so you have to consider each finte group as a discrete topological group.  Because of this (iii) the actual entry on [[profinite group]] takes one to be a [[pro-object]] in the category of finite groups. (The way to handle this may need to be discussed to get consensus on which we all like best.)

I am not sure what name the [[SGA1]] type fundamental group should be called. I do not particularly like the one you use below.

[[David Roberts]]: This was a knock-together job, I must admit. Actually I think the SGA1 fundamental group is called the algebraic fundamental group - in the case of schemes its also called the etale fundamental group, but I personally think 'algebraic' would fit better in this example - it is changed!

I'll also leave off the description of this object to its own page. Sometime I'll also get around to writing about [[Grothendieck's Galois theory]].

[[Mike Shulman|Mike]]: Of course, it would be more consistent to use the same definition of profinite group here as at [[profinite group]].  As I said there, I prefer the cofiltered-system definition since it is more "basic"  and explains why you have to consider topological groups if you want to actually take the limit.  Would you object if we defined $\hat{G}$ to be the cofiltered diagram consisting of all finite quotients of $G$, and then observed that, just as always for a profinite group, we could instead take the limit as a topological group?

[[Tim Porter|Tim]]:  That was what I was hinting at in (iii).  I think also that the universal property is not yet in its optimal form as it mixes topological ond non-topological things too much. I may try to put together a categorical formulation as a 'gloss' on this.
=-- {: .query}
##Definition##
More formally, we note that for any group $G$, the family of its normal finite index subgroups forms a [[filtered category|cofiltered category]] under inclusion. (Denote it by $\Omega_G$.)  The assignment of $G/N$ to $N$ gives a functor from  $\Omega_G^{op}$ to the category of finite groups. It is thus a [[profinite group]] in the sense given in that entry, i.e. a [[pro-object]] in the category of finite groups. This pro-object is the profinite completion of $G$.  

The above topological version of this, with which we started, is obtained by means of the equivalence between the category of pro-(finite groups) and that of the groups internal to profinite spaces  that is by taking the limit in the category of topological groups of the diagram of (discrete) finite groups that thee above construction gives one.

##Categorical gloss on the profinite completion##
The inclusion functor $inc$ from the category, $FinGrps$, of finite groups, into that of groups does not have a left adjoint.  It does have a left *pro-adjoint*, that is to say, it induces a functor on procategories
$$pro\!-\!inc : pro\!-\! FinGrps\to pro\!-\Grps$$
and that functor _does_ have a left adjoint. If we restrict that 'pro-adjoint' to the subcategory of $pro\!-\! FinGrps$ given by the 'constant' pro-objects, then the result is the pro-finite completion construction that is given above. Because of this, if we think of the natural functor $C\to pro\!-\! C$ to be an inclusion, i.e. think of an object as a pro-object indexed by the one arrow category, we can give a universal property for the pro-finite completion of a group $G$. This universal property gives a universal cone from $G$  to finite groups, and just encodes the obvious fact that any homomorphism from $G$ to a finite group factors through one of its finite quotient groups. If we write $\hat{G}$ for the pro-finite completion, the universal cone is a map $G\to \hat{G}$ in $pro\!-\! FinGrps$.


##Example##
An example that comes up in practice is the profinite completion of the fundamental group of an complex projective variety $X$. Since $X$ has an underlying topological space, its [[fundamental group]] of loops $\pi_1^{top}(X)$ can be defined in the usual way. But one can also define the [[algebraic fundamental group]] $\pi_1^{alg}(X)$. This is a profinite group, which is isomorphic to the profinite completion of $\pi_1^{top}(X)$.

[[!redirects profinite completion]]
